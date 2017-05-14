---
title: "디지털 서명의 암호화 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "디지털 서명 [WCF]"
  - "디지털 서명 [WCF], 암호화"
  - "디지털 서명의 암호화 [WCF]"
ms.assetid: 0868866d-40b4-4341-8e42-eee3b7f15b69
caps.latest.revision: 9
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 9
---
# 디지털 서명의 암호화
기본적으로 메시지는 서명 및 암호화되며 서명은 디지털 방식으로 암호화됩니다.이 작업은 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement> 또는 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>의 인스턴스가 포함된 사용자 지정 바인딩을 만든 다음, 해당 클래스의 `MessageProtectionOrder` 속성을 <xref:System.ServiceModel.Security.MessageProtectionOrder> 열거형 값으로 설정하여 제어할 수 있습니다.기본값은 <xref:System.ServiceModel.Security.MessageProtectionOrder>입니다.이 프로세스는 단순한 서명 및 암호화보다 10%\-40%의 시간이 더 소모됩니다.하지만 서명 암호화를 사용하지 않으면 공격자가 메시지 내용을 추측할 수 있습니다.서명 요소에는 메시지의 서명된 모든 부분에 대한 일반 텍스트의 해시 코드가 들어 있기 때문입니다.예를 들어 메시지 본문이 기본적으로 암호화되어 있더라도 암호화되어 있지 않은 서명에는 메시지 본문에 대한 해시 코드가 포함되어 있습니다.따라서 메시지가 작을 경우 공격자는 그 내용을 추론할 수 있습니다.서명을 암호화하면 이러한 가능성을 줄이거나 없앨 수 있습니다.  
  
 따라서 보안에 영향을 주지 않는 큰 이진 파일을 보내는 경우와 같이, 내용 가치가 낮거나 성능이 크게 향상될 경우에만 서명 암호화를 사용하지 않도록 설정합니다.  
  
### 디지털 서명을 사용하지 않도록 설정하려면  
  
1.  <xref:System.ServiceModel.Channels.CustomBinding>을 만듭니다.[!INCLUDE[crdefault](../../../../includes/crdefault-md.md)][방법: SecurityBindingElement를 사용하여 사용자 지정 바인딩 만들기](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md).  
  
2.  <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement> 또는 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>를 바인딩 컬렉션에 추가합니다.  
  
3.  <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement.MessageProtectionOrder%2A?displayProperty=fullName> 속성을 <xref:System.ServiceModel.Security.MessageProtectionOrder>로 설정하거나 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement.MessageProtectionOrder%2A?displayProperty=fullName> 속성을 <xref:System.ServiceModel.Security.MessageProtectionOrder>로 설정합니다.  
  
 사용자 지정 바인딩 만들기[!INCLUDE[crabout](../../../../includes/crabout-md.md)][사용자 정의 바인딩 만들기](../../../../docs/framework/wcf/extending/creating-user-defined-bindings.md)를 참조하십시오.특정 인증 모드용 사용자 지정 바인딩 만들기[!INCLUDE[crabout](../../../../includes/crabout-md.md)][방법: 지정된 인증 모드에 대한 SecurityBindingElement 만들기](../../../../docs/framework/wcf/feature-details/how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md)를 참조하십시오.  
  
## 참고 항목  
 <xref:System.ServiceModel.Security.MessageProtectionOrder>   
 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>   
 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>   
 [방법: SecurityBindingElement를 사용하여 사용자 지정 바인딩 만들기](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)   
 [사용자 정의 바인딩 만들기](../../../../docs/framework/wcf/extending/creating-user-defined-bindings.md)   
 [방법: 지정된 인증 모드에 대한 SecurityBindingElement 만들기](../../../../docs/framework/wcf/feature-details/how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md)