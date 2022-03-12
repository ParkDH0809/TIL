SW를 개발하는 방법, 과정 등에 대해 알아보자.
=========  
**contents**
1. [SW 분류](#SW-분류)
2. [SW Process Model](#SW-Process-Model)
***
### SW 분류와 SW Process
분류 방법은 방법, 과정에 따라 매우 다양하다.    


**큰 범위의 SW 분류**
- 시스템 유형별 : Desktop SW, mobile SW, IoT SW, ...  
- 계약 유형별 : Custom SW, generic SW, embedded SW, ...  

**SW project 분류**
 - 신규 개발 프로젝트 : Greenfield, Poilt project, ...
 - 기능 개선(유지보수) 프로젝트 : Evolutionary project, 기존 legacy system 유지보수, ...
 - 프레임워크 프로젝트(재사용 가능한 system 개발) : framework를 이용한 project
 - 오픈 소스 프로젝트 : 집단 지성을 이요한 project  

**이에 따른 이해당사자(Stakeholder)**  
 - Sponsor or Client : 비용을 지불하는 사람
 - Software developer : 개발자
 - Project Manager(PM) : 개발 책임자
 - User, End user : 사용자, 최종 이용자  

**SW Process의 핵심적인 활동**  
SW Process : 소프트웨어 시스템을 개발하기 위한 활동들의 집합

1. SW 명세 : 무슨 SW인가? (제공해야 할 기능 및 제약조건 식별)
    - 요구사항 도출 및 분석, 확인 등을 진행한다.
2. SW 설계 및 구현 : 어떻게 기능을 제공할 것인가? 
3. SW 확인 : 제대로 작동하는가? (리뷰 및 테스트 진행)
    > 개발팀의 테스팅   
    >> Unit testing (단위 테스팅) : 한 class와 같이 작은 범위에 대한 테스트 진행  
    >> Integration testing (통합 테스팅) : SW를 통합해 테스트 진행  
    >> System testing (시스템 테스팅) : 운영 환경과 동일한 환경에서 테스트 진행   
    >> Regression testing (회귀 테스팅) :SW version을 올릴 때 이전 기능을 유지했는가에 대한 테스트
   
    > 사용자의 테스팅  
    >> Alpha testing (알파 테스팅) : 개발자의 입장에서 사용자를 대상으로 테스트 진행  
    >> Beta testing (베타 테스팅) : 사용자 입장에서 사용자를 대상으로 테스트 진행

    >발주자의 테스팅
    >> Acceptance testing (인수 테스팅) : 발주자의 바람을 충족했는지에 대한 테스트  
4. SW 진화 : SW 변경 및 유지보수
   - Adaptive maintenance (적응 유지보수) : OS, DB등의 발전에 따라 SW를 진화 및 적응시켜야 한다.
   - Corrective maintenance (수정 유지보수) : 버그를 고치는 등의 작업을 한다.
   - Perfective maintenance (개선 유지보수) : 사용자의 요구를 반영하여 새로운 기능을 만든다.
   - Preventive maintenance (예방 유지보수) : refectoring작업과 같이 SW 코드를 재구성한다. 가독성과 좋은 유지보수를 위함이다.


분류 기준 및 내용은 이외에도 다수 있다.  
***
### SW Process Model
SW 개발을 체계적으로 하기 위해 여러 Model이 등장했다.   
<img src="/assets/images/SE_PlanbasedVsAgile.PNG" width="550" height="300">  
큰 범위에서 Plan-based process model과 Agile process model로 구분된다.    
간단히
- Plan-based는 개발 계획부터 하나씩 해나가는 방식
- Agile은 짧은 주기로 개발을 끝내면서 피드백을 받는 방식  
이다.

대표적인 몇 가지 세부 process를 알아보자.  

#### Plan-based process  
Plan-based process model은 중간에 변경이 힘들다는 단점이 있다. 따라서 계획을 치밀하게 세워야 한다.   

- [폭포수 모델(Waterfall Model)](https://www.indeed.com/career-advice/career-development/waterfall-methodology)  
    순차적으로 진행하는 모습이 폭포수와 같다고 하여 붙여진 이름이다.  
    <img src="/assets/images/SE_Waterfallmodel.PNG" width="400" height="200">  
  - 순차적으로 개발 진행 ( 요구사항 정의 - 설계 - 구현 - 테스팅 - 운영 및 유지보수 )  
  - 장점 : 단순하다. 안정화 되어있다.
  - 단점 : 피드백이 늦다. 변경 사항이 생기면 많은 비용이 든다.
   - 설계 및 구현을 끝냈는데 사용자 혹은 발주자에게 요구사항이 생긴다면 손을 대기 힘들다.
   - 상위 단계가 끝나야 다음 단계를 진행하므로 유연성이 떨어진다.

- V 모델(V-Model)  
  <img src="/assets/images/SE_Vmodel.PNG" width="400" height="200">
  - 개발만큼 검증이 강조된 모델이다.
  - 국방, 자동차 등 안전이 필수인 시스템(Safety critical system) 개발에 사용된다.
  - 안전과 관련된 거의 모든 국제 규격에서 추천한다.(권고에 가깝다.)
  - 간단히 아래로 내려가는 쪽은 개발, 꼭짓점은 구현, 위로 올라오는 쪽은 테스팅이다.

이외에도 Incremental development model, Integration and configuration model 등이 있다.  

#### Agile process  
Iteration을 구분해 작업을 진행한다. 각 Interation마다 요구사항을 add, remove, modify할 수 있다.
짧은 주기로 개발해가면서 발주자 or 사용자의 의견을 수용한다.

**[애자일 선언문(Manifesto for Agile Software Development)](https://agilemanifesto.org/)**  
<img src="/assets/images/SE_AgileManifesto.PNG" width="300" height="300">  
다음은 애자일 방식의 기반이 되는 선언문이다.  
> 프로세스와 도구 보다 상호작용을  
> 광범위한 문서보다 작동하는 SW를  
> 계약 협상보다 고객과의 협력을  
> 계획을 따르기보다 변화 대응을 중요시하자.  
  
라는 내용으로 애자일이 추구하는 방향을 알 수 있다.

- Scrum  
  <img src="/assets/images/SE_ScrumProcess.PNG">
  - 대표적인 Agile 기법  
  - Product Owner, Scrum Master, Development team로 역할이 구분된다.  
 
    1. Product Owner가 원하는 SW에 대한 item들을 적어 Product Backlog를 만든다.  
    2. Product Backlog에서 이번 Sprint동안 만들 item들을 가져와 Sprint Backlog를 만든다.  
    3. Sprint를 진행하면서 SW를 개발한다.  
    4. 한 Sprint가 끝나면 Product Owner가 시연한다. 피드백을 통해 item을 추가, 변경 및 제거를 한다.  
    5. 위 과정을 반복하면서 Product Owner의 요구사항을 맞춘 SW를 개발한다.


  - 장점 
    - 스폰서가 원하는 SW에 가까이 갈 수 있도록 도와준다.
    - 프로덕트 오너가 산출물을 잘 이해도록 도와준다.
    - 실패 위험을 낮추도록 도와준다.

이외에도 XP, RUP 등 다양한 Agile process model이 있다.
