---
title: "끝점 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: fe63370d-81a1-40f3-97c2-59cb357c78d2
caps.latest.revision: 9
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 9
---
# 끝점
끝점  
  
## 구문  
  
```  
class Endpoint  
{  
  string Address;  
  string AddressHeaders[];  
  string AddressIdentity;  
  sint32 AppDomainId;  
  Behavior Behaviors[];  
  Binding Binding;  
  string ContractName;  
  string CounterInstanceName;  
  string ListenUri;  
  string Name;  
  sint32 ProcessId;  
  Contract ref;  
};  
```  
  
## 메서드  
 Endpoint 클래스는 다음과 같은 메서드를 정의합니다.  
  
|메서드|설명|  
|---------|--------|  
|[GetOperationCounterInstanceName](../../../../../docs/framework/wcf/diagnostics/wmi/getoperationcounterinstancename.md)|작업 성능 카운터 인스턴스 이름을 검색합니다.|  
  
## 속성  
 Endpoint 클래스에는 다음 속성이 있습니다.  
  
### Address  
 데이터 형식: string  
  
 액세스 형식: 읽기 전용  
  
 끝점의 주소를 포함하는 URI입니다.  
  
### AddressHeaders  
 데이터 형식: string array  
  
 액세스 형식: 읽기 전용  
  
 이 끝점에 연결된 주소 헤더의 컬렉션입니다.  
  
### AddressIdentity  
 데이터 형식: string  
  
 액세스 형식: 읽기 전용  
  
 끝점의 ID입니다.  
  
### AppDomainId  
 데이터 형식: sint32  
  
 액세스 형식: 읽기 전용  
  
 끝점을 호스트하는 appdomain의 appdomain ID입니다.  
  
### 동작  
 데이터 형식: Behavior array  
  
 액세스 형식: 읽기 전용  
  
 이 끝점에서 구현된 동작의 컬렉션입니다.  
  
### 바인딩  
 데이터 형식: Binding  
  
 액세스 형식: 읽기 전용  
  
 이 끝점에서 사용하는 바인딩입니다.  
  
### ContractName  
 데이터 형식: string  
  
 액세스 형식: 읽기 전용  
  
 이 끝점이 공개하는 계약을 지정하는 문자열입니다.  
  
### CounterInstanceName  
 데이터 형식: string  
  
 액세스 형식: 읽기 전용  
  
 끝점의 성능 카운터 인스턴스 이름입니다.  
  
### ListenUri  
 데이터 형식: string  
  
 액세스 형식: 읽기 전용  
  
 끝점이 수신하는 URI입니다.  
  
### 이름  
 데이터 형식: string  
  
 액세스 형식: 읽기 전용  
  
 이 끝점의 고유한 이름입니다.  
  
### ProcessId  
 데이터 형식: sint32  
  
 액세스 형식: 읽기 전용  
  
 끝점을 호스트하는 프로세스의 프로세스 ID입니다.  
  
### ref  
 데이터 형식: Contract  
  
 액세스 형식: 읽기 전용  
  
 이 끝점이 공개하는 계약입니다.  
  
## 요구 사항  
  
|MOF|Servicemodel.mof에 선언되어 있습니다.|  
|---------|----------------------------------|  
|네임스페이스|root\\ServiceModel에 정의되어 있습니다.|