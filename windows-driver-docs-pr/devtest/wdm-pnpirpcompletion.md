---
title: PnpIrpCompletion 规则 (wdm)
description: PnpIrpCompletion 规则验证 FDO 驱动程序将 PnP Irp 传递到较低的驱动程序。
ms.assetid: 32b2ed2c-4222-4d93-8323-3ad442a14d9d
ms.date: 05/21/2018
keywords:
- PnpIrpCompletion 规则 (wdm)
topic_type:
- apiref
api_name:
- PnpIrpCompletion
api_type:
- NA
ms.localizationpriority: medium
ms.openlocfilehash: 4e1367a65d3a8c87cde38ae68c9133846e39d84c
ms.sourcegitcommit: a33b7978e22d5bb9f65ca7056f955319049a2e4c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2019
ms.locfileid: "56526626"
---
# <a name="pnpirpcompletion-rule-wdm"></a>PnpIrpCompletion 规则 (wdm)


**PnpIrpCompletion**规则验证 FDO 驱动程序将 PnP Irp 传递到较低的驱动程序。

此规则不适用于总线驱动程序。

以下 PnP Irp 不在此规则：

-   IRP\_MN\_查询\_接口
-   IRP\_MN\_查询\_停止\_设备
-   IRP\_MN\_查询\_删除\_设备

|              |     |
|--------------|-----|
| 驱动程序模型 | WDM |

<a name="how-to-test"></a>如何测试
-----------

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">在编译时</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>运行<a href="https://msdn.microsoft.com/library/windows/hardware/ff552808" data-raw-source="[Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808)">Static Driver Verifier</a>并指定<strong>PnpIrpCompletion</strong>规则。</p>
使用以下步骤来分析你的代码：
<ol>
<li><a href="https://msdn.microsoft.com/library/windows/hardware/hh454281#preparing-your-source-code" data-raw-source="[Prepare your code (use role type declarations).](https://msdn.microsoft.com/library/windows/hardware/hh454281#preparing-your-source-code)">准备你的代码 （使用角色类型声明）。</a></li>
<li><a href="https://msdn.microsoft.com/library/windows/hardware/hh454281#running-static-driver-verifier" data-raw-source="[Run Static Driver Verifier.](https://msdn.microsoft.com/library/windows/hardware/hh454281#running-static-driver-verifier)">运行的 Static Driver Verifier。</a></li>
<li><a href="https://msdn.microsoft.com/library/windows/hardware/hh454281#viewing-and-analyzing-the-results" data-raw-source="[View and analyze the results.](https://msdn.microsoft.com/library/windows/hardware/hh454281#viewing-and-analyzing-the-results)">查看和分析结果。</a></li>
</ol>
<p>有关详细信息，请参阅<a href="https://msdn.microsoft.com/library/windows/hardware/hh454281" data-raw-source="[Using Static Driver Verifier to Find Defects in Drivers](https://msdn.microsoft.com/library/windows/hardware/hh454281)">以找到缺陷驱动程序中使用 Static Driver Verifier</a>。</p></td>
</tr>
</tbody>
</table>

<a name="applies-to"></a>适用于
----------

[**IoCallDriver**](https://msdn.microsoft.com/library/windows/hardware/ff548336)
[**IoCompleteRequest**](https://msdn.microsoft.com/library/windows/hardware/ff548343)
[**IoForwardIrpSynchronously**](https://msdn.microsoft.com/library/windows/hardware/ff549100)
[**PoCallDriver**](https://msdn.microsoft.com/library/windows/hardware/ff559654)
 

 




