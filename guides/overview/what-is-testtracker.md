# ✨ What is TestTracker

테스트 대상을 일반적인 웹 서비스로 한정할 경우, 테스트 방식은 크게 세 가지로 나눌 수 있습니다.\
첫째, 브라우저 상의 UI 요소를 이용한 테스트 방식,\
둘째, 클라이언트의 요청을 처리하고 응답하는 백엔드 서버를 대상으로 한 테스트 방식,\
셋째, 서비스를 구성하는 시스템 전반의 최대 성능과 안정성을 확인하는 테스트 방식이 있습니다.



<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>Web application을 대상으로 하는 다양한 테스트 방법</p></figcaption></figure>



이처럼 테스트 대상과 목적에 따라 다양한 테스트 방법이 존재하며, 각 방법은 그것을 구성하는 기반 기술, 실행 환경, 조작 방식이 모두 다를 수 있습니다.\
이러한 모든 테스트 방법을 충분히 이해하고 자동화를 적용할 수 있는 팀을 운영하는 일은, 소규모 IT 기업이나 스타트업에게는 결코 쉬운 일이 아닙니다.



<figure><img src="../.gitbook/assets/image (72).png" alt="" width="318"><figcaption></figcaption></figure>



그래서 우리는 고민했습니다.

> * 개발자에게 테스트 코드 작성을 요구하지 않고, 테스트 담당자에게 자동화 구현을 요구할 필요가 없도록 테스트 자동화를 위한 managed service를 제공하려면 무엇을 해야 할까
> * 웹 서비스 테스트를 위해 UIUx 관점, 개별 기능 관점, 성능/용량 관점에서의 테스트를 단일 조작성(interface)으로 실행하고 관리하는 것이 가능할까
> * _<mark style="color:purple;">프로그램 설치나 셋업 없이\[1]</mark>_ 누구나 손쉽게 이용할 수 있도록 접근성과 활용성을 높일 수 있는 방법은?
> * 필요한 서비스만 구독해서 특정 기간 또는 사용한 만큼 만 지불하는 비용 부과방식을 도입할 수 있을까
> * 테스트 실행, 결과 보고, 이슈 등록까지의 전 과정을 자동으로 처리할 수 있는 방법은 무엇일까



이와 같은 고민에 대한 해결책으로 자체 개발 솔루션을 구상하게 되었고 그 결과 Web app/service 테스트 자동화를 위한 클라우드 플랫폼인 "[TestTracker](https://testtracker.net)"를 선보이게 되었습니다. 아래는 "[<mark style="color:blue;">TestTracker</mark>](https://testtracker.net)"의 주요 특징 및 기능 요소를 나타냅니다. (일부 기능 추후 제공 예정)

<figure><img src="../.gitbook/assets/image.png" alt="" width="281"><figcaption></figcaption></figure>



**1) Test Automation**\
&#x20; \- 명시된 조건과 절차에 의해 테스트의 흐름이 결정되고 시험자의 수동 조작에 의지하지 않는 테스트 실행 지원\
&#x20; \- Schedule 등록에 의한 주기적인 반복 테스트 및 예약 실행 가능

**2) Test Report**\
&#x20; \- 테스트 완료 시 시험 결과와 요약 정보를 email로 전송\
&#x20; \- 최대 1년간의 defect 발생 이력 및 일일(daily) 요약정보 제공\
&#x20; \- 개별 시험 항목에 대한 자세한 테스트 로그 제공\
&#x20; \- Issue management/tracking system 연동(ex. Redmine, Trac 등) - <mark style="background-color:yellow;">(예정)</mark>

**3) Unified Platform**\
&#x20; \- API, UIUx, Performance 테스트를 단일 플랫폼에서 실행 <mark style="background-color:yellow;">(일부 예정)</mark>

_**4) Integrations**_ _<mark style="background-color:yellow;">(예정)</mark>_\
&#x20; _-_ CI 도구와 연동하여 모든 빌드 및 통합에서 Regression test 실행 지원\
&#x20; _-_ Metrics 및 시계열 데이터(Time series Test Data) 내보내기를 통해 모니터링 시스템과의 연동 지원

**5) Resource Sharing**\
&#x20; \- 테스트 환경, 리소스, 시험 결과 데이터를 팀 멤버들과 공유

**6) No code & Instant Test** <mark style="background-color:yellow;">(예정)</mark>\
&#x20; _- AI based test code generation & Execution_

**7) No Install & No setup**\
&#x20; \- Cloud 서비스(SaaS)로써 S/W 설치 및 셋업 과정 없이 웹에서 로그인을 통해 손쉽게 사용 가능

**8) Billing**\
&#x20; \- 구독(단기/연간), 테스트 실행 계획(횟수)별 과금



{% hint style="warning" %}
\[1] - Performance test의 경우 Nginx 와 같은 reverse proxy 이후의 upstream 구간부터 측정하도록 테스트를 설계한 경우 별도의 Agent module에 대한 셋업이 필요할 수 있음.
{% endhint %}

{% hint style="warning" %}
"예정" 표시 항목은 2025년 현재 기준 미 제공 기능입니다. (추후 기능 포함 예정)
{% endhint %}

{% hint style="info" %}
브라우저 호환 : TestTracker는 Chrome (v 126.0) 브라우저에 최적화되었기에 Google Chrome 브라우저 및 Chrome 호환 브라우저를통해 TestTracker를 이용하실 것을 권장합니다.
{% endhint %}



TestTracker를 통해 더욱 강력하고 효율적인 테스트 환경을 경험해보세요.\
직관적인 UI와 강력한 분석 기능을 갖춘 TestTracker는 자동화 커버리지를 극대화하여 품질 향상을 가속화하고,\
DevOps 파이프라인에 완벽히 통합될 수 있도록 설계되었습니다.

[https://testtracker.net](https://testtracker.net) 를 방문하여 직접 확인해 주세요.

