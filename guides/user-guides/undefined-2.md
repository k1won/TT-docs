---
description: >-
  TestTracker를 구성하는 주요 기능 블록에 대한 전반적인 내용을 간략히 설명합니다. 세부적인 설명이 필요하신 경우 각 기능에 대한
  가이드 항목을 참고하시기 바랍니다.
---

# 주요 기능 및 화면 구성

## Workspace

Workspace는 테스트 타입(API/Ux/Performance)을 선택하거나 관련 리소스 상태확인 또는 설정 등 테스트 실행에 관한 기본 작업 공간이라 할 수 있습니다. 테스트 실행 또는 테스트 결과에 대한 확인 및 분석을 담당하는 다수의 팀원들이 멤버로서 Workspace를 공유하게 됩니다.

<figure><img src="../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption><p>Workspace 구성</p></figcaption></figure>

<mark style="color:blue;">**Entry**</mark> : TestTracker에서 지원하는 세 가지 테스트 타입을 실행하기 위한 각각의 페이지로 이동할 수 있는 선택 버튼들이 위치합니다.

<mark style="color:blue;">**Test Schedule**</mark> : 예약된 시각에 자동으로 테스트가 실행되도록 설정할 수 있는 기능으로, 예약된 작업, 테스트 종류, 등록자 및 테스트 옵션 등을 확인할 수 있습니다. Schedule job 설정 방법은 "[테스트 실행 (예약)](undefined-5.md)"을 참고해 주시기 바랍니다.

<mark style="color:blue;">**Resources**</mark> : Workspace는 다양한 형태의 리소스들의 조합으로 구성됩니다. 특정 기간 동안 테스트를 몇 회 실행 가능한지 나타내는 카운터, script 또는 data file 보관이 필요한 클라우드 서버 내 영구 저장소, 팀 멤버 등이 해당됩니다. 이러한 각각의 리소스에 대한 현황 확인이 가능하고, 우측의 Setup icon 클릭을 통해 일부 리소스에 대한 구성 변경 이 가능합니다.

<mark style="color:blue;">**Working Directory**</mark> : 테스트 실행에 필요한 script file 및 data file들을 관리할 수 있습니다. 권한이 있는 사용자에 의해 파일 삭제가 가능하고, data file에 한 해 업로드 기능을 지원합니다. Test script file에 대한 생성 또는 업로드는 각 테스트 실행 페이지에서 지원합니다.

{% hint style="warning" %}
UIUX, Performance test의 경우 현재 버전에서는 미 지원 상태입니다. (추후 지원 예정)
{% endhint %}



## API Test

API Test는 TestTracker에서 지원하는 세 가지 테스트 타입 가운데 하나이고, Back-end server를 대상으로 각각의 API Endpoint에 대한 테스트 요청을 전송하고 응답 메시지를 통해 Test Case를 검증하는 시험 방식입니다.

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption><p>API Test 실행 설정</p></figcaption></figure>

<mark style="color:blue;">**Test Script Selection**</mark> : 시험 대상 또는 목적에 따라 여러 test script 가운데 하나를 선택할 수 있고, 세부적으로는 관련 있는 TC 들의 묶음인 Test Suite(Item Group) 역시 선별해서 테스트를 실행할 수 있습니다. 그리고 test script 신규 추가 또는 기존 script modify를 위한 script file upload 기능이 제공됩니다.

<mark style="color:blue;">**Run Configuration**</mark> : Test script 실행 시 적용 가능한 몇 가지 옵션 설정 기능과 함께 테스트를 실행시키는 버튼이 위치합니다.

<mark style="color:blue;">**Script Information**</mark> : Script file 과 Environment file에 관한 메타 데이터를 제공합니다. 참고로 script file 은 test code 가 기술되어 있고, environment file 은 test code 가 참조하는 일부 변수값들이 설정되어 있어 테스트 대상 또는 조건에 따라 서로 다른 테스트 값으로 TC 검증이 가능합니다.



## API Test Result

테스트 실행 후 진행 상황 및 실행 결과를 확인할 수 있습니다. 테스트가 진행됨과 동시에 각각의 test item에 대한 테스트 결과가 화면에 반영되고, 모든 테스트 종료 시 오류 발생 여부 및 통계를 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption><p>Test Item 별 시험 현황 및 종합 결과</p></figcaption></figure>

테스트 과정에서 발생한 각종 메시지와 로그 등을 개별 test item 별로 확인 가능합니다. 즉, TestTracker 가 TC 검증을 위해 target entity 와 교환한 HTTP Transaction message(Request, Response)와 Console log, Error/Fail contents 등을 Side panel UI를 통해 자세히 확인 가능합니다.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption><p>테스트 결과에 대한 detail view</p></figcaption></figure>



## UX Test

서비스 준비 중입니다.



## Performance Test

서비스 준비 중입니다.



## Report

테스트 결과에 대해 요약된 정보를 제공합니다. 최근 365일간의 시험 결과를 바탕으로 Fail 발생 건수, Daily record, Item group 별 Fail 수 및 기타 부가정보 등을 확인할 수 있습니다. 이러한 정보들을 통해 테스트 대상에 대한 품질 현황 및 개선 추이 파악이 용이하도록 하는 것을 목적으로 합니다.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption><p>테스트 결과에 대한 summary report</p></figcaption></figure>

<mark style="color:blue;">**Test Fails**</mark> : Bug Curve 표현을 위해 사용자가 지정한 특정 기간의 Fail 발생 현황을 Bar chart 또는 Line chart로 나타냅니다.

<mark style="color:blue;">**Test Records**</mark> : 테스트에 대한 일별(daily) 요약 정보를 나타냅니다. Test Type, Title, Description, Tester, Date, Result, Total, Fail 등의 필드 정보를 포함하며, 특정 일 테스트가 2회 이상 실행되더라도 최초 실행된 테스트의 결과만 제공합니다(summary report 저장 옵션 활성화 조건).

<mark style="color:blue;">**ItemGroup Fails**</mark> : 위 Test Records에 종속된 데이터로써 서로 관련 있는 Test Item 들의 묶음인 Test Group 각각의 총 시험 항목 수(Total) 와 그중 결함 발생 수(Fail)를 나타냅니다. Radar chart 와 Bar chart 중 선택 가능합니다.

<mark style="color:blue;">**Response Time / Collection Stat / Test option**</mark> : 위 Test Records에 종속된 데이터로써 Test Item 별 요청에 대한 응답 시간 분포, 그중 worst case 5가지에 대한 정보, 통계, 테스트 실행 옵션 등의 정보를 제공합니다.

{% hint style="warning" %}
API Test에 한하며, UIUX, Performance Test의 경우 서비스 준비 중입니다.
{% endhint %}



## History (Test)

테스트 실행 이력을 제공합니다. 한 번에 20건씩 확인 가능하고, 하단의 "More" 버튼 클릭 시 추가로 20건씩 총 100건의 실행 이력을 확인할 수 있습니다. 또한 가장 최근 실행된 테스트 3건에 대해 테스트 결과를 다시 확인할 수 있는 기능을 제공합니다. 사후 테스트 결과 확인을 위해 "Review" 칼럼의 "open" 링크를 클릭하게 되면 해당 테스트의 저장된 시험 결과 데이터들을 로드하여 [API Test Result](undefined-2.md#api-test-result) page에서 테스트 결과 및 관련 로그 등을 다시 확인 가능합니다. 이를 통해 팀 멤버들 간의 테스트 결과 공유가 가능합니다.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption><p>테스트 실행 이력</p></figcaption></figure>

{% hint style="info" %}
위에서 설명한 "Review" 기능은 스토리지에 저장된 이전의 테스트 결과를 불러와서 출력해 주는 것입니다. 동일한 시험 조건(script, options)으로 신규 시험 결과 확인이 필요한 경우 [API Test Result](undefined-2.md#api-test-result) page에서 "Run Again" 버튼을 클릭하시거나 아니면 [API Test](undefined-2.md#api-test) page에서 테스트 조건 재 설정 후 "Run" 버튼 클릭하여 재 실행하시기 바랍니다.
{% endhint %}

{% hint style="warning" %}
Review를 위한 테스트 결과 데이터는 최대 3건만 제공합니다. 신규 테스트 결과 발생 시 가장 오래된 것을 지우고 신규 결과 포함 최근 3건만 유지한다는 것을 참고해 주시기 바랍니다.
{% endhint %}



## History (Operation)

서비스 준비 중입니다.

