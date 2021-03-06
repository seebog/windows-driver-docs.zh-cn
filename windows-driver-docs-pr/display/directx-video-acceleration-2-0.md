---
title: DirectX 视频加速 2.0
description: DirectX 视频加速 2.0
keywords:
- 用户模式显示驱动程序 WDK Windows Vista，DirectX 视频加速
- DirectX 视频加速 WDK 显示，版本2
- 视频加速 WDK DirectX，版本2
- VA WDK DirectX，版本2
- DirectX 视频加速 WDK 显示
ms.date: 04/20/2017
ms.localizationpriority: medium
ms.openlocfilehash: 9af1bd3e7294faefd0bad23ef87d52506befcbdc
ms.sourcegitcommit: 418e6617e2a695c9cb4b37b5b60e264760858acd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/07/2020
ms.locfileid: "96809317"
---
# <a name="directx-video-acceleration-20"></a>DirectX 视频加速 2.0

以下主题讨论 Microsoft DirectX 视频加速 (VA) 版本2.0：

[DirectX VA 2.0 的视频解码加速](video-decode-acceleration-for-directx-va-2-0.md)

[DirectX VA 2.0 的视频处理](video-processing-for-directx-va-2-0.md)

[DirectX VA 2.0 的扩展支持](extended-support-for-directx-va-2-0.md)

## <a name="directx-video-acceleration-20-structures-and-enumerations"></a>DirectX 视频加速2.0 结构和枚举

DirectX 视频加速 (VA) 2.0 用户模式显示驱动程序函数使用以下结构和枚举类型。

* DXVADDI_AYUVSAMPLE16
* DXVADDI_AYUVSAMPLE8
* DXVADDI_CONFIGPICTUREDECODE
* DXVADDI_DECODEBUFFERDESC
* DXVADDI_DECODEBUFFERINFO
* DXVADDI_DECODEINPUT
* DXVADDI_EXTENDEDFORMAT
* DXVADDI_FILTERVALUES
* DXVADDI_FIXED32
* DXVADDI_FREQUENCY
* DXVADDI_NOMINALRANGE
* DXVADDI_PRIVATEBUFFER
* DXVADDI_PRIVATEDATA
* DXVADDI_PROCAMPVALUES
* DXVADDI_PVP_HW_IV
* DXVADDI_PVP_KEY128
* DXVADDI_PVP_SETKEY
* DXVADDI_QUERYEXTENSIONCAPSINPUT
* DXVADDI_QUERYFILTERPROPERTYRANGEINPUT
* DXVADDI_QUERYPROCAMPINPUT
* DXVADDI_SAMPLEFORMAT
* DXVADDI_VALUERANGE
* DXVADDI_VIDEOCHROMASUBSAMPLING
* DXVADDI_VIDEODESC
* DXVADDI_VIDEOLIGHTING
* DXVADDI_VIDEOPRIMARIES
* DXVADDI_VIDEOPROCESSBLTFLAGS
* DXVADDI_VIDEOPROCESSORCAPS
* DXVADDI_VIDEOPROCESSORINPUT
* DXVADDI_VIDEOSAMPLE
* DXVADDI_VIDEOSAMPLEFLAGS
* DXVADDI_VIDEOTRANSFERFUNCTION
* DXVADDI_VIDEOTRANSFERMATRIX
* DXVAHDDDI_ALPHA_FILL_MODE
* DXVAHDDDI_BLT_STATE
* DXVAHDDDI_BLT_STATE_ALPHA_FILL_DATA
* DXVAHDDDI_BLT_STATE_BACKGROUND_COLOR_DATA
* DXVAHDDDI_BLT_STATE_CONSTRICTION_DATA
* DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
* DXVAHDDDI_BLT_STATE_PRIVATE_DATA
* DXVAHDDDI_BLT_STATE_TARGET_RECT_DATA
* DXVAHDDDI_COLOR
* DXVAHDDDI_COLOR_RGBA
* DXVAHDDDI_COLOR_YCbCrA
* DXVAHDDDI_CONTENT_DESC
* DXVAHDDDI_CUSTOM_RATE_DATA
* DXVAHDDDI_DEVICE_DESC
* DXVAHDDDI_DEVICE_USAGE
* DXVAHDDDI_FILTER
* DXVAHDDDI_FILTER_RANGE_DATA
* DXVAHDDDI_FRAME_FORMAT
* DXVAHDDDI_NOMINAL_RANGE
* DXVAHDDDI_OUTPUT_RATE
* DXVAHDDDI_RATIONAL
* DXVAHDDDI_ROTATION
* DXVAHDDDI_STREAM_DATA
* DXVAHDDDI_STREAM_STATE
* DXVAHDDDI_STREAM_STATE_ALPHA_DATA
* DXVAHDDDI_STREAM_STATE_ASPECT_RATIO_DATA
* DXVAHDDDI_STREAM_STATE_DESTINATION_RECT_DATA
* DXVAHDDDI_STREAM_STATE_FILTER_DATA
* DXVAHDDDI_STREAM_STATE_FRAME_FORMAT_DATA
* DXVAHDDDI_STREAM_STATE_INPUT_COLOR_SPACE_DATA
* DXVAHDDDI_STREAM_STATE_LUMA_KEY_DATA
* DXVAHDDDI_STREAM_STATE_OUTPUT_RATE_DATA
* DXVAHDDDI_STREAM_STATE_PALETTE_DATA
* DXVAHDDDI_STREAM_STATE_PRIVATE_DATA
* DXVAHDDDI_STREAM_STATE_PRIVATE_IVTC_DATA
* DXVAHDDDI_STREAM_STATE_ROTATION_DATA
* DXVAHDDDI_STREAM_STATE_SOURCE_RECT_DATA
* DXVAHDDDI_SURFACE
* DXVAHDDDI_VPCAPS
* DXVAHDDDI_VPDEVCAPS
