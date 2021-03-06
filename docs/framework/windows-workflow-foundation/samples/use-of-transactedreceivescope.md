---
title: TransactedReceiveScope 사용
ms.date: 03/30/2017
ms.assetid: d455f1dc-bfc5-43d6-8ae9-bc3b3a3ea08a
ms.openlocfilehash: bc1c418f3fa116f5e1c1647af3543a38122842f5
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43501644"
---
# <a name="use-of-transactedreceivescope"></a>TransactedReceiveScope 사용
이 샘플에서는 <xref:System.Activities.Statements.TransactionScope>를 사용하여 클라이언트에 새 트랜잭션을 만들고 <xref:System.ServiceModel.Activities.TransactedReceiveScope>를 사용하여 이동된 트랜잭션과 함께 메시지를 받고 서버에 있는 트랜잭션의 수명 주기 범위를 지정하여 클라이언트에서 서버로 트랜잭션을 이동하는 방법을 보여 줍니다. 이 샘플은 클라이언트와 서버의 역할을 나타내는 두 개의 프로젝트로 구성되어 있습니다.  
  
## <a name="client-application"></a>클라이언트 응용 프로그램  
 클라이언트 응용 프로그램에서는 분산 트랜잭션 ID를 출력하고, 서버로 메시지를 보내고, 트랜잭션을 이동하고, 회신을 받고, 분산 트랜잭션 ID를 다시 출력한 후 완료되는 워크플로를 실행합니다. 분산 트랜잭션 ID를 처음 출력할 때는 트랜잭션이 아직 로컬인 상태이므로 빈 GUID가 출력됩니다.  
  
## <a name="server-application"></a>서버 응용 프로그램  
 서버 프로젝트도 클라이언트의 경우와 비슷하지만, 워크플로가 <xref:System.ServiceModel.Activities.WorkflowServiceHost>에 호스트된다는 점에서 차이가 있습니다. 서버의 경우 클라이언트의 메시지를 엔드포인트에서 수신해야 하기 때문입니다. 이 워크플로는 클라이언트에서 이동한 트랜잭션을 받고, 전달된 메시지를 출력하고, 분산 트랜잭션 ID를 출력하고, 클라이언트에 회신을 보내는 <xref:System.ServiceModel.Activities.TransactedReceiveScope>를 중심으로 합니다. 이번에는 분산 트랜잭션 ID가 빈 GUID가 아니며, 트랜잭션 인식 활동을 <xref:System.ServiceModel.Activities.TransactedReceiveScope>의 본문에 추가한 경우 이동한 트랜잭션 하에서 해당 활동이 실행됩니다.  
  
#### <a name="to-run-the-sample"></a>이 샘플을 실행하려면  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]에서 TransactedReceiveScope.sln 솔루션을 엽니다.  
  
2.  솔루션을 빌드하려면 CTRL + SHIFT + b 또는 선택 **솔루션 빌드** 에서 합니다 **빌드** 메뉴.  
  
3.  빌드가 성공 되 면 솔루션을 마우스 오른쪽 단추로 클릭 하 고 선택 **시작 프로젝트 설정**합니다. 대화 상자에서 선택 **여러 개의 시작 프로젝트** 두 프로젝트에 대 한 작업을 확인 하 고 **시작**합니다.  
  
4.  F5 키를 누르거나 **디버깅 시작** 에서 합니다 **디버그** 메뉴. 또는 CTRL + F5 키를 눌러 수도 있고 선택할 **디버깅 하지 않고 시작** 에서 **디버그** 메뉴 디버깅 하지 않고 실행 합니다.  
  
    > [!NOTE]
    >  클라이언트를 시작하기 전에 서버를 실행해야 합니다. 서비스를 호스트하는 콘솔 창의 출력을 통해 서비스가 시작되었음을 알 수 있습니다.  
  
> [!IMPORTANT]
>  컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다. 계속하기 전에 다음(기본) 디렉터리를 확인하세요.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플. 이 샘플은 다음 디렉터리에 있습니다.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Transactions\TransactedReceiveScope`