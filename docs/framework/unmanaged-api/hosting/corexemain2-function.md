---
title: _CorExeMain2 함수
ms.date: 03/30/2017
api_name:
- _CorExeMain2
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- _CorExeMain2
helpviewer_keywords:
- _CorExeMain2 function [.NET Framework hosting]
ms.assetid: 72ea68b4-689f-4733-9416-9664b75e8892
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 573336b32040f44ff1b59fcbb75b59aa00976b5c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33430181"
---
# <a name="corexemain2-function"></a>_CorExeMain2 함수
지정된 된 메모리 매핑된 코드에서 진입점을 실행합니다. 이 함수는 운영 체제 로더에 의해 호출 됩니다.  
  
## <a name="syntax"></a>구문  
  
```  
__int32 STDMETHODCALLTYPE _CorExeMain2 (  
   [in] PBYTE           pUnmappedPE,  
   [in] DWORD           cUnmappedPE,  
   [in] __in LPWSTR     pImageNameIn,  
   [in] __in LPWSTR     pLoadersFileName,  
   [in] __in LPWSTR     pCmdLine  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `pUnmappedPE`  
 [in] 메모리 매핑된 코드에 대 한 포인터입니다.  
  
 `cUnmappedPE`  
 [in] 요소 수가 `pUnmappedPE` 보유할 수 있습니다.  
  
 `pImageNameIn`  
 [in] 실행 가능 이미지의 이름에 대 한 포인터입니다.  
  
 `pLoadersFileName`  
 [in] 로더 파일의 이름입니다.  
  
 `pCmdLine`  
 [in] 명령줄 매개 변수가 있는 경우입니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.  
  
 **헤더:** Cor.h  
  
 **라이브러리:** MsCorEE.dll에 리소스로 포함  
  
 **.NET framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>참고 항목  
 [메타데이터 전역 정적 함수](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
