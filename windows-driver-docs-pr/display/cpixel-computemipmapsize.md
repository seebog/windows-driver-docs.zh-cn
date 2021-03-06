---
title: CPixel ComputeMipMapSize 方法
description: CPixel ComputeMipMapSize 方法确定分配 mipmap 纹理所需的内存量。
keywords:
- ComputeMipMapSize 方法显示设备
- ComputeMipMapSize 方法显示设备，CPixel 接口
- CPixel 接口显示设备，ComputeMipMapSize 方法
topic_type:
- apiref
api_name:
- CPixel.ComputeMipMapSize
api_location:
- pixel.hpp
api_type:
- COM
ms.date: 01/05/2018
ms.localizationpriority: medium
ms.openlocfilehash: 25cd6bce1fcce4508c776dd808e252aee47b0c64
ms.sourcegitcommit: 418e6617e2a695c9cb4b37b5b60e264760858acd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/07/2020
ms.locfileid: "96834647"
---
# <a name="cpixelcomputemipmapsize-method"></a>CPixel：： ComputeMipMapSize 方法


**CPixel：： ComputeMipMapSize** 方法确定分配 mipmap 纹理所需的内存量。

<a name="syntax"></a>语法
------

```ManagedCPlusPlus
static UINT  ComputeMipMapSize(
   UINT      cpWidth,
   UINT      cpHeight,
   UINT      cLevels,
   D3DFORMAT Format
);
```

<a name="parameters"></a>参数
----------

*cpWidth* 指定 mipmap 纹理的宽度（以像素为单位）。

*cpHeight* 指定 mipmap 纹理的高度（以像素为单位）。

*cLevels* 指定 mipmap 纹理的级别数。

*格式* 使用 D3DFORMAT 枚举中的值指定表面格式。

<a name="return-value"></a>返回值
------------

返回 mipmap 纹理的大小（以字节为单位）。

<a name="remarks"></a>备注
-------

有关 D3DFORMAT 的详细信息，请参阅 Microsoft DirectX SDK 文档。

<a name="requirements"></a>要求
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>目标平台</p></td>
<td align="left">台式机</td>
</tr>
<tr class="even">
<td align="left"><p>标头</p></td>
<td align="left">Hpp (包含 hpp) </td>
</tr>
</tbody>
</table>

 

 





