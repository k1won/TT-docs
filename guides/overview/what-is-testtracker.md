# ✨ What is TestTracker

S/W 품질을 개선하고 지속적인 통합(Continuous Integration)과 배포를 위해서 테스트를 자동화하는 과정은 필수입니다. 시험 대상 즉 테스트 항목에서 자동화 커버리지를 확대할수록 운용 중 발생할 수 있는 Regression issue를 줄일 수 있고, 개발-검증-배포로 이어지는 일련의 과정에 소요되는 시간을 단축하여 적기에 신규 서비스를 적용할 수 있습니다.

테스트 대상을 일반적인 HTTP(S) Web Service로 한정할 때 크게는 브라우저 상에 표현되는 UI 요소를 이용한 테스트 방법과 클라이언트의 요청을 해석하고 처리 및 응답을 담당하는 Back-end 서버를 대상으로 하는 테스트 방법, 서비스를 구성하는 시스템 전반의 최대 성능 및 안정성 확인을 대상으로 하는 테스트 방법 등이 존재합니다.

이처럼 테스트 대상 및 목적에 따라 다양한 테스트 방법이 존재하고 이 각각의 방법들은 그것을 구성하는 기반 기술과 실행 환경 및 조작 방식이 모두 상이할 가능성이 높습니다. 이 모든 테스트 방법을 잘 이해하고 테스트 자동화에 적용할 수 있는 팀 조직을 운영하는 것은 소 규모의 IT 기업 및 스타트업에서는 여간 어려운 일이 아닐 수 없습니다.

그래서 우리는 고민했습니다.

* 개발자에게 테스트 코드 작성을 요구하지 않고, 테스트 담당자에게 자동화 구현을 요구할 필요가 없도록 테스트 자동화를 위한 managed service를 제공하려면 무엇을 해야 할까
* 웹 서비스 테스트를 위해 UIUX 관점, 서버 기능 관점, 성능/안정성 관점에서의 테스트를 단일 조작성(interface)으로 실행하고 관리하는 것이 가능할까
* 별도의 프로그램 설치나 셋업 없이 누구나손쉽게 이용할 수 있도록 접근성과 활용성을 높일 수 있는 서비스 형태는 무엇일까
* 필요한 서비스 항목을 구독이나 사용한 만큼 만 지불하는 비용 부과방식을 도입할 수 있을까
* 테스트 실행, 결과 보고, 이슈 등록까지의 전 과정을 자동화 처리할 수 있는 방법은 무엇일까

이와 같은 고민에 대한 해결책으로 자체 개발 설루션을 구상하게 되었고 그 결과 테스트 자동화를 위한 클라우드 서비스를 여기 선보이게 되었습니다.



아래는 고객 요구사항 만족을 위해 자체 개발한 테스트 자동화 플랫폼인 "[<mark style="color:blue;">TestTracker</mark>](https://testtracker.net)"의 주요 특징 및 기능 요소를 나타냅니다. (일부 기능 추후 제공 예정)



**1) Test Automation**\
&#x20; \- 명시된 조건과 절차에 의해 테스트의 흐름이 결정되고 시험자의 수동 조작에 의지하지 않는 테스트 실행 지원\
&#x20; \- Schedule 등록에 의한 주기적인 반복 테스트 및 예약 실행 가능

**2) Report & Results**\
&#x20; \- 테스트 완료 시 시험 결과와 관련 요약 정보를 email로 전송\
&#x20; \- 최대 1년간 결함(Defect) 발생 수 변화 및 일일(daily) 요약정보 제공\
&#x20; \- 개별 시험 항목에 대한 자세한 테스트 로그 확인 가능\
&#x20; <mark style="background-color:yellow;">- Issue management/tracking system 연동(ex. Redmine, Trac 등) - (예정)</mark>

**3) Unified Platform**\
&#x20; \- API, Web UI, Performance 자동화 테스트를 단일 플랫폼에서 실행 지원 <mark style="background-color:yellow;">(일부 예정)</mark>

_<mark style="background-color:yellow;">4) Integrations (예정)</mark>_\
&#x20; _<mark style="background-color:yellow;">- CI 도구와 연동하여 모든 빌드 및 통합에서 Regression test 실행 지원</mark>_

**5) Sharing**\
&#x20; \- 테스트 환경, 리소스, 시험 결과 데이터를 팀 멤버들과 공유

<mark style="background-color:yellow;">6) No code & Instant Test (예정)</mark>\
&#x20; _<mark style="background-color:yellow;">- AI based test code generation & Execution</mark>_

**7) No Install & No setup**\
&#x20; \- TestTracker는 Cloud에서 제공되는 서비스의 형태(TaaS)로써 별도의 설치 및 셋업 절차 없이 웹에서 로그인을 통해 손쉽게 사용 가능



[TestTracker](https://testtracker.net) 를 방문하여 직접 확인해주세요.

{% hint style="warning" %}
"예정" 표시 항목은 2024년 현재 기준 미 제공 기능입니다. (추후 오픈 예정)
{% endhint %}

{% hint style="info" %}
브라우저 호환 : TestTracker는 Chrome (v 126.0) 브라우저에 최적화되었기에 Google Chrome 브라우저를 통해 TestTracker를 이용하실 것을 권장합니다.
{% endhint %}

