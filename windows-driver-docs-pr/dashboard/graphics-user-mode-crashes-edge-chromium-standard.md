---
title: 按使用时间规范化的 Microsoft Edge Chromium 中的用户模式崩溃次数小于等于基线目标
description: 该度量将 7 天滑动窗口中的遥测数据聚合成为 Microsoft Edge Chromium 在总运行时（以年为单位）内由显卡驱动程序引起的崩溃比率
ms.topic: article
ms.date: 05/11/2020
ms.localizationpriority: medium
ms.openlocfilehash: fc29cadf3169339ab03b485516729ddcd66162d6
ms.sourcegitcommit: d7b5e6049db3109fdcbe83279875f24f3fa6acdd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/27/2020
ms.locfileid: "84110239"
---
# <a name="number-of-user-mode-crashes-in-microsoft-edge-chromium-normalized-by-usage--baseline-goal"></a>按使用时间规范化的 Microsoft Edge Chromium 中的用户模式崩溃次数小于等于基线目标

## <a name="description"></a>说明

当用户通过 Microsoft Edge Chromium 浏览 Internet 时，显卡组件将处理来自 Web 的可视数据，并在用户屏幕上显示呈现的视图。 该度量监视 Microsoft Edge Chromium 由于显卡驱动程序而崩溃的频率（相对于使用驱动程序的所有设备上的 Microsoft Edge Chromium 运行时）。 如果 Microsoft Edge Chromium 崩溃，用户必须先等待该应用程序恢复，然后才能再次使用它。  

## <a name="measure-attributes"></a>度量属性

|属性|值|
|----|----|
|受众|驱动程序的目标设备|
|时间段|7 天滑动窗口|
|度量标准|实例的聚合|
|最小总体数量|30,000 小时的 Microsoft Edge Chromium 运行时|
|通过标准|每年崩溃次数小于等于 1|
|度量 ID|25481659|

## <a name="calculation"></a>计算

该度量将 7 天滑动窗口中的遥测数据聚合为 Microsoft Edge Chromium 在总运行时（以年为单位）内由显卡驱动程序引起的崩溃比率

Microsoft Edge Chromium 崩溃总次数 = 计数（Microsoft Edge Chromium 在具有驱动程序的计算机上的崩溃次数）

Microsoft Edge Chromium 总运行时 = 总和（具有驱动程序的每台计算机的 Microsoft Edge Chromium 运行时）

运行时（以年为单位）= Microsoft Edge Chromium 总运行时 ∗ 60（分钟）∗ 60（小时）∗ 24（天）∗ 365（年）

### <a name="final-calculation"></a>最终计算

按使用时间规范化的 Microsoft Edge Chromium 的崩溃次数 = Microsoft Edge Chromium 崩溃总次数/运行时（年）
