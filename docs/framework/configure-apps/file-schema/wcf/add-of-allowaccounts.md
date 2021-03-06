---
title: '&lt;allowAccounts&gt;의 &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: 763c7b1f-e7b0-4d99-a42c-4506fcb8da00
ms.openlocfilehash: 2230b8d22a14c3df5eb3aa10872246febce015e9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33349693"
---
# <a name="ltaddgt-of-ltallowaccountsgt"></a>&lt;allowAccounts&gt;의 &lt;add&gt;
WCF 서비스를 호스팅하고 공유 서비스에 대 한 연결 액세스를 부여 하는 프로세스에 대 한 사용자 계정을 지정 합니다.  
  
 \<system.serviceModel.activation>  
  
## <a name="syntax"></a>구문  
  
```xml  
<allowAccounts>  
   <add securityIdentifier="String"/>  
</allowAccounts>  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
  
|특성|설명|  
|---------------|-----------------|  
|securityIdentifier|사용자 계정을 식별하는 데 사용하는 고유 식별자를 지정하는 문자열입니다. 반환되는 기본값은 LocalSystem, Administrators, NS, LS 및 IIS_USRS입니다.|  
  
### <a name="child-elements"></a>자식 요소  
 없음  
  
### <a name="parent-elements"></a>부모 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<allowAccounts>](../../../../../docs/framework/configure-apps/file-schema/wcf/allowaccounts.md)|포함 하는 구성 요소의 컬렉션을 `securityIdentifier` 는 WCF 서비스를 호스팅하고 공유 서비스에 대 한 연결 액세스가 부여 된 프로세스에 대 한 사용자 계정을 지정 하는 특성입니다.|  
  
## <a name="example"></a>예제  
 다음 구성 예제에서는 사용자 계정에 대한 다섯 가지 기본 식별자를 이 컬렉션에 추가합니다.  
  
```xml  
<allowAccounts>  
   // LocalSystem account  
   <add securityIdentifier="S-1-5-18"/>  
   // LocalService account  
   <add securityIdentifier="S-1-5-19"/>  
   // Administrators account  
   <add securityIdentifier="S-1-5-20"/>  
   // Network Service account  
   <add securityIdentifier="S-1-5-32-544" />  
   // IIS_IUSRS account (Vista only)  
   <add securityIdentifier="S-1-5-32-568"/>  
</allowAccounts>  
```  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
