---
title: GpuMmu 模型
description: 在 GpuMmu 模型中， (GPU) 的图形处理单元 (MMU) 将每个进程的 GPU 虚拟地址转换为物理地址。
ms.date: 04/20/2017
ms.localizationpriority: medium
ms.openlocfilehash: 781fdaab9029d8058177296eeb587491b1f79c34
ms.sourcegitcommit: 418e6617e2a695c9cb4b37b5b60e264760858acd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/07/2020
ms.locfileid: "96825747"
---
# <a name="gpummu-model"></a>GpuMmu 模型


在 *GpuMmu* 模型中， (GPU) 的图形处理单元 (MMU) 将每个进程的 GPU 虚拟地址转换为物理地址。

每个进程都有单独的 CPU 和 GPU 虚拟地址空间，它们使用不同的页表。 视频内存管理器管理所有进程的 GPU 虚拟地址空间，并负责分配、增长、更新，确保派驻和释放页表。 GPU MMU 使用的页面表的硬件格式对于视频内存管理器是未知的，通过设备驱动程序接口 (DDIs) 进行了抽象。 抽象支持多级级转换，包括固定大小的页表和可调整大小的根页表。

尽管视频内存管理器负责管理 GPU 虚拟地址空间及其基础页表，但视频内存管理器不会自动向分配分配 GPU 虚拟地址。 此责任落在用户模式驱动程序上。

视频内存管理器向用户模式驱动程序提供了两组服务。 首先，用户模式驱动程序可以通过现有的 [*分配*](/windows-hardware/drivers/ddi/d3dumddi/nc-d3dumddi-pfnd3dddi_allocatecb) 回调分配视频内存，并通过现有的 [*释放*](/windows-hardware/drivers/ddi/d3dumddi/nc-d3dumddi-pfnd3dddi_deallocatecb) 回调释放该内存。 正如今天一样，这将向用户模式驱动程序返回视频内存管理器分配的句柄，可由 GPU 引擎操作。 此类分配仅表示分配的物理部分，并且可以通过分配列表引用进行物理操作引用。

对于在虚拟模式下运行的引擎，需要将 GPU 虚拟地址显式分配给分配，才能真正地访问该地址。 出于此目的，视频内存管理器提供用户模式驱动程序服务来保留或释放 GPU 虚拟地址，并将特定分配范围映射到进程的 GPU 虚拟地址空间。 这些服务非常灵活，允许用户模式驱动程序精细控制进程 GPU 虚拟地址空间。 用户模式驱动程序可能决定将非常具体的 GPU 虚拟地址分配给分配，或让视频内存管理器自动选取可用的虚拟地址，可能会指定一些最小和最大 GPU 虚拟地址约束。 单个分配可能有多个与之关联的 GPU 虚拟地址映射，并且向用户模式驱动程序提供服务以实现 *磁贴资源协定*。

同样，在链接的显示适配器配置中，用户模式驱动程序可以将 GPU 虚拟地址显式映射到特定的分配实例，并为每个映射选择映射应为自身还是特定对等 GPU。 在此模型中，分配给分配的 CPU 和 GPU 虚拟地址是独立的。 用户模式驱动程序可以决定在两个地址空间中保持它们相同，或使它们保持独立。

GPU 虚拟地址在逻辑上通过 DDI 接口在固定的4KB 页粒度进行管理。 GPU 虚拟地址可以引用内存段或系统内存中驻留的分配。 在驱动程序选择时，系统内存在4kb 或64KB 上按4KB 的物理粒度进行管理。 所有视频内存管理器分配都进行了调整，并调整了大小，使之成为驱动程序所选页面大小的倍数。

访问无效的 GPU 虚拟地址范围会导致访问冲突和终止导致访问错误的上下文和/或设备。 若要从这种故障中恢复，视频内存管理器将启动一个引擎重置，该重置会升级到适配器范围的超时检测恢复 (TDR) 如果不成功。

*GpuMmu* 模型如下所示：

![gpummu 模型](images/gpummu-model.1.png)

 

