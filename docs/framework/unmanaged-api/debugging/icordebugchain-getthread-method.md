---
title: "ICorDebugChain::GetThread 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugChain.GetThread
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugChain::GetThread
helpviewer_keywords:
- GetThread method, ICorDebugChain interface [.NET Framework debugging]
- ICorDebugChain::GetThread method [.NET Framework debugging]
ms.assetid: b3390319-6366-418c-ba80-b552ac4dfc1e
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 1e8307134bc81041efe2a596131b5d309220a873
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugchaingetthread-method"></a><span data-ttu-id="85bf9-102">ICorDebugChain::GetThread 메서드</span><span class="sxs-lookup"><span data-stu-id="85bf9-102">ICorDebugChain::GetThread Method</span></span>
<span data-ttu-id="85bf9-103">호출 체인은 실제 스레드에서의 부분을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="85bf9-103">Gets the physical thread this call chain is part of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85bf9-104">구문</span><span class="sxs-lookup"><span data-stu-id="85bf9-104">Syntax</span></span>  
  
```  
HRESULT GetThread (  
    [out] ICorDebugThread    **ppThread  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="85bf9-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="85bf9-105">Parameters</span></span>  
 `ppThread`  
 <span data-ttu-id="85bf9-106">[out] 실제 스레드에 나타내는 ICorDebugThread 개체에 대 한 포인터가 호출 체인의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="85bf9-106">[out] A pointer to an ICorDebugThread object that represents the physical thread this call chain is part of.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="85bf9-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="85bf9-107">Requirements</span></span>  
 <span data-ttu-id="85bf9-108">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="85bf9-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="85bf9-109">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="85bf9-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="85bf9-110">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="85bf9-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="85bf9-111">**.NET framework 버전:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="85bf9-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>