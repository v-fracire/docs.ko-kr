---
title: "어셈블리를 사용한 프로그래밍 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-bcl"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "어셈블리[.NET Framework], 프로그래밍"
  - "어셈블리 프로그래밍"
ms.assetid: 25918b15-701d-42c7-95fc-c290d08648d6
caps.latest.revision: 18
author: "rpetrusha"
ms.author: "ronpet"
manager: "wpickett"
caps.handback.revision: 18
---
# 어셈블리를 사용한 프로그래밍
어셈블리는 .NET Framework를 구성하는 블록입니다. 어셈블리는 배포, 버전 제어, 다시 사용, 활성 범위 지정, 보안 권한 등의 기본적인 단위를 구성합니다.  어셈블리는 형식을 구현하는 데 필요한 정보를 공용 언어 런타임에 제공합니다.  어셈블리는 형식과 리소스의 컬렉션이며, 이 형식과 리소스가 통합되어 논리적 기능 단위를 구성합니다.  런타임에 있어서 형식은 어셈블리 컨텍스트 내에만 존재합니다.  
  
 이 단원에서는 모듈을 만들고 이 모듈에서 어셈블리를 만들고, 키 쌍을 만들고 강력한 이름을 사용하여 어셈블리를 서명하고, 전역 어셈블리 캐시에 어셈블리를 설치하는 방법에 대해 설명합니다.  이 단원에서는 또한 [MSIL 디스어셈블러\(Ildasm.exe\)](../../../docs/framework/tools/ildasm-exe-il-disassembler.md)를 사용하여 어셈블리 매니페스트 정보를 보는 방법에 대해 설명합니다.  
  
> [!NOTE]
>  .NET Framework 버전 2.0부터 현재 로드된 런타임보다 버전 번호가 높은 .NET Framework로 컴파일된 어셈블리는 런타임에서 로드되지 않습니다.  이는 주 버전 번호와 부 버전 번호의 조합에 해당됩니다.  
  
## 단원 내용  
 [어셈블리 만들기](../../../docs/framework/app-domains/create-assemblies.md)  
 단일 파일 어셈블리와 다중 파일 어셈블리에 대해 설명합니다.  
  
 [어셈블리 이름](../../../docs/framework/app-domains/assembly-names.md)  
 어셈블리 이름 지정 방법에 대해 설명합니다.  
  
 [방법: 어셈블리의 정규화된 이름 식별](../../../docs/framework/app-domains/how-to-determine-assembly-fully-qualified-name.md)  
 어셈블리의 정규화된 이름을 확인하는 방법에 대해 설명합니다.  
  
 [완전 신뢰 모드에서 인트라넷 응용 프로그램 실행](../../../docs/framework/app-domains/running-intranet-applications-in-full-trust.md)  
 인트라넷 공유에 있는 완전 신뢰 어셈블리에 대해 레거시 보안 정책을 지정하는 방법에 대해 설명합니다.  
  
 [어셈블리 위치](../../../docs/framework/app-domains/assembly-location.md)  
 어셈블리 검색 위치에 대해 설명합니다.  
  
 [방법: 단일 파일 어셈블리 만들기](../../../docs/framework/app-domains/how-to-build-a-single-file-assembly.md)  
 단일 파일 어셈블리를 만드는 방법에 대해 설명합니다.  
  
 [다중 파일 어셈블리](../../../docs/framework/app-domains/multifile-assemblies.md)  
 다중 파일 어셈블리를 만드는 이유에 대해 설명합니다.  
  
 [방법: 다중 파일 어셈블리 빌드](../../../docs/framework/app-domains/how-to-build-a-multifile-assembly.md)  
 다중 파일 어셈블리를 만드는 방법에 대해 설명합니다.  
  
 [어셈블리 특성 설정](../../../docs/framework/app-domains/set-assembly-attributes.md)  
 어셈블리 특성과 이 특성을 설정하는 방법에 대해 설명합니다.  
  
 [강력한 이름의 어셈블리 만들기 및 사용](../../../docs/framework/app-domains/create-and-use-strong-named-assemblies.md)  
 강력한 이름으로 어셈블리를 서명하는 방법과 그 이유에 대해 설명하고 방법 항목을 나열합니다.  
  
 [어셈블리 서명 연기](../../../docs/framework/app-domains/delay-sign-assembly.md)  
 어셈블리 서명을 연기하는 방법에 대해 설명합니다.  
  
 [어셈블리 및 전역 어셈블리 캐시 사용](../../../docs/framework/app-domains/working-with-assemblies-and-the-gac.md)  
 어셈블리를 전역 어셈블리 캐시에 추가하는 방법과 그 이유에 대해 설명하고 방법 항목을 나열합니다.  
  
 [방법: 어셈블리 내용 보기](../../../docs/framework/app-domains/how-to-view-assembly-contents.md)  
 MSIL 디스어셈블러\(Ildasm.exe\)를 사용하여 어셈블리 콘텐츠를 보는 방법에 대해 설명합니다.  
  
 [공용 언어 런타임의 형식 전달](../../../docs/framework/app-domains/type-forwarding-in-the-common-language-runtime.md)  
 형식 전달을 사용하여 기존 응용 프로그램을 중단하지 않고 형식을 다른 어셈블리로 이동하는 방법에 대해 설명합니다.  
  
## 참조  
 <xref:System.Reflection.Assembly>  
 어셈블리를 나타내는 .NET Framework 클래스입니다.  
  
## 관련 단원  
 [방법: 어셈블리에서 형식 및 멤버 정보 가져오기](../../../docs/framework/app-domains/how-to-obtain-type-and-member-information-from-an-assembly.md)  
 어셈블리에서 형식 및 기타 정보를 프로그래밍 방식으로 가져오는 방법에 대해 설명합니다.  
  
 [공용 언어 런타임의 어셈블리](../../../docs/framework/app-domains/assemblies-in-the-common-language-runtime.md)  
 공용 언어 런타임 어셈블리에 대해 개념적으로 설명합니다.  
  
 [어셈블리 버전 관리](../../../docs/framework/app-domains/assembly-versioning.md)  
 어셈블리 바인딩과 <xref:System.Reflection.AssemblyVersionAttribute> 및 <xref:System.Reflection.AssemblyInformationalVersionAttribute> 특성에 대해 간략하게 설명합니다.  
  
 [런타임에서 어셈블리를 찾는 방법](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)  
 런타임에서 바인딩 요청을 수행하는 데 필요한 어셈블리를 결정하는 방법에 대해 설명합니다.  
  
 [리플렉션](../../../docs/framework/reflection-and-codedom/reflection.md)  
 **Reflection** 클래스를 사용하여 어셈블리와 관련된 정보를 얻는 방법에 대해 설명합니다.