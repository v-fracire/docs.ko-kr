---
title: IMetaDataImport::GetRVA 메서드
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetRVA
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetRVA
helpviewer_keywords:
- GetRVA method [.NET Framework metadata]
- IMetaDataImport::GetRVA method [.NET Framework metadata]
ms.assetid: ea422217-988b-4acd-b2db-c55357938275
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1232e8c574f263f709a9b66c7b1b3d06cca5e4da
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447213"
---
# <a name="imetadataimportgetrva-method"></a>IMetaDataImport::GetRVA 메서드
상대 가상 주소 (RVA)와 메서드 또는 지정한 토큰이 나타내는 필드의 구현 플래그를 가져옵니다.  
  
## <a name="syntax"></a>구문  
  
```  
HRESULT GetRVA (  
   [in]  mdToken     tk,   
   [out] ULONG       *pulCodeRVA,   
   [out]  DWORD      *pdwImplFlags  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `tk`  
 [in] MethodDef 또는 FieldDef 메타 데이터를 나타내는 토큰에 대 한 RVA를 반환할 코드 개체입니다. 한 FieldDef 토큰을 사용 하는 경우 필드에는 전역 변수 여야 합니다.  
  
 `pulCodeRVA`  
 [out] 토큰이 나타내는 코드 개체의 상대 가상 주소에 대 한 포인터입니다.  
  
 `pdwImplFlags`  
 [out] 메서드에 대 한 구현 플래그에 대 한 포인터입니다. 이 값은의 비트 마스크는 [CorMethodImpl](../../../../docs/framework/unmanaged-api/metadata/cormethodimpl-enumeration.md) 열거 합니다. 값 `pdwImplFlags` 유효한 경우에만 `tk` MethodDef 토큰입니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.  
  
 **헤더:** Cor.h  
  
 **라이브러리:** MsCorEE.dll에 리소스로 포함  
  
 **.NET framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>참고 항목  
 [IMetaDataImport 인터페이스](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [IMetaDataImport2 인터페이스](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
