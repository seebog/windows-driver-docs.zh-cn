---
title: NDIS_STATUS_MEDIA_CONNECT
description: NDIS_STATUS_MEDIA_CONNECT 状态表明设备的网络连接的状态已从 "断开连接" 更改为 "已连接"。
ms.date: 07/18/2017
keywords:
- 从 Windows Vista 开始 NDIS_STATUS_MEDIA_CONNECT 网络驱动程序
ms.localizationpriority: medium
ms.openlocfilehash: 5166f0953f09c284539713ed5c4cb0e93a86b0b5
ms.sourcegitcommit: 418e6617e2a695c9cb4b37b5b60e264760858acd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/07/2020
ms.locfileid: "96801513"
---
# <a name="ndis_status_media_connect"></a>NDIS \_ 状态 \_ 媒体 \_ 连接


NDIS \_ 状态 \_ 媒体 \_ 连接状态表明设备的网络连接的状态已从 "断开连接" 更改为 "已连接"。 例如，当设备进入 (无线设备) 或用户连接设备的网络电缆时，设备会连接。

<a name="remarks"></a>备注
-------

\_ \_ \_ 对于过量的 ndis 6.0 驱动程序，ndis 将 ndis 状态媒体连接状态指示转换为 [**ndis \_ 状态 \_ 链接 \_ 状态**](ndis-status-link-state.md)指示。

NDIS 5。*x* 和更早的微型端口驱动程序指示当微型端口驱动程序确定网络连接已丢失时， [**NDIS \_ 状态 \_ 媒体 \_ 断开连接**](ndis-status-media-disconnect.md) 状态。 在恢复连接时，驱动程序指示 NDIS \_ 状态 \_ 媒体 \_ 连接状态。

有关 NDIS \_ 状态媒体连接的详细信息 \_ \_ ，请参阅 [指示连接状态 (NDIS 5.1) ](/previous-versions/windows/hardware/network/ff546856(v=vs.85)) 和 [802.11 网络的媒体状态指示](/previous-versions/windows/hardware/network/ff549301(v=vs.85))。

<a name="requirements"></a>要求
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>版本</p></td>
<td><p>在 NDIS 6.0 和更高版本中不受支持 (改用 <a href="ndis-status-link-state.md" data-raw-source="[&lt;strong&gt;NDIS_STATUS_LINK_STATE&lt;/strong&gt;](ndis-status-link-state.md)"><strong>NDIS_STATUS_LINK_STATE</strong></a>) 。 只有 Windows Vista 和 Windows XP 中的 NDIS 5.1 驱动程序支持。</p></td>
</tr>
<tr class="even">
<td><p>标头</p></td>
<td> (包含 Ndis .h) </td>
</tr>
</tbody>
</table>

## <a name="see-also"></a>请参阅


[**NDIS \_ 状态 \_ 链接 \_ 状态**](ndis-status-link-state.md)

[**NDIS \_ 状态 \_ 媒体 \_ 断开连接**](ndis-status-media-disconnect.md)

 

