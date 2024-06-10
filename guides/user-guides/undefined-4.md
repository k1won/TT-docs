---
description: 테스트 실행을 위한 절차 및 방법을 설명합니다.
---

# 테스트 실행

{% hint style="info" %}
테스트 코드가 작성된 script file 이 테스트 실행 전 working directory의 해당 위치에 미리 존재해야 합니다. 테스트 목적에 맞는 script file 이 TestTracker에 존재하지 않는 경우 "[테스트 구성](undefined-3.md)"에서 설명하는 절차를 먼저 진행하시기 바랍니다.
{% endhint %}

{% hint style="info" %}
테스트를 실행할 수 있는 Resource 조건은 다음과 같습니다.

* Locked : False
* Remains : 1 이상
{% endhint %}

{% hint style="info" %}
User role 이 "Tester" 이상이면 테스트 실행이 가능하고, "Guest" 인 경우 테스트 실행이 허용되지 않습니다.
{% endhint %}

## API Test

API Test는 아래와 같은 절차로 진행합니다.

#### 1) API Test page로 이동 (Workspace > Entry > API Test 버튼 클릭)

#### 2) Test script 선택

<div align="center">

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

</div>

위 예시는 3개의 script 중 "API testing basics"를 선택했을 때 보이는 화면입니다. Script는 하나 이상의 Item Group으로 이루어질 수 있고 시험 목적에 따라 선별적으로 실행될 수 있습니다. 예시에서는 두 개의 Item Group 중 "Basic test syntax" 만 선택된 모습입니다. 각각의 Item Group 을 클릭해서 선택 또는 해제가 가능하고, "Select All", "Deselect All" 버튼을 통해 일괄 선택 또는 일괄 해제도 가능합니다.

{% hint style="info" %}
Item Group 은 Postman collection에서의 "folder" 와 동일한 역할을 합니다. Postman에서는 비슷한 성격의 Request 들 또는 동일한 endpoint를 대상으로 하는 Request 들을 함께 특정 폴더에 위치시키고 테스트 실행 시 folder 단위로 실행하는 것이 가능합니다. TestTracker 역시 그와 같은 script 구성 방법을 따르되 다만 folder 내에 또 다른 folder 가 존재하는 중첩 구조는 지원하지 않고 single level의 grouping(Item Group)으로 처리합니다.
{% endhint %}

{% hint style="info" %}
Script title 우측의 열쇠 모양의 아이콘이 의미하는 것은 해당 script는 테스트 실행이 허용되지 않는다는 것을 나타냅니다. TT-Admin에 의해 설정 또는 해제될 수 있습니다.
{% endhint %}

#### 3) Test option 설정

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

각 항목에 대한 설명은 아래 내용을 참고해 주시기 바랍니다.

<table data-header-hidden><thead><tr><th width="167" align="center"></th><th></th></tr></thead><tbody><tr><td align="center">Collection</td><td>Script 선택 시 script title 이 자동으로 설정됨</td></tr><tr><td align="center">Environment</td><td>Script에서 참조하는 variable set이 environment에 위치할 경우 그에 해당하는 적절한 environment를 선택하고 그렇지 않은 경우 "None" 선택</td></tr><tr><td align="center">Description</td><td>테스트 목적 또는 s/w version 등 임의의 문자열 입력 가능. (기본값은 script title)</td></tr><tr><td align="center">Iteration Count</td><td>Script 실행 반복 횟수 (최대 3회 가능)</td></tr><tr><td align="center">Timeout</td><td>Script 가 실행될 수 있는 최대 시간. 테스트 진행이 설정값을 초과하여 실행되는 경우 강제 종료되고 test result 값은 "TimedOut"으로 처리.</td></tr><tr><td align="center">Delay Request</td><td>Test target으로 전송하는 request 들 간의 interval 시간을 의미</td></tr><tr><td align="center">Stop Option</td><td><p>Script 실행을 종료시킬 수 있는 조건을 의미. </p><p>"<strong>Script Error"</strong> : test code의 문법적 오류 즉, exception 등의 오류 발생 케이스</p><p>"<strong>Test Fail</strong>" : test case 실행 결과가 Pass 가 아닌 Fail인 경우<br>"<strong>None</strong>" : Script error 또는 test fail 발생하더라도 모든 test case 실행 후 종료</p></td></tr><tr><td align="center">Run Option</td><td>즉시 실행 또는 예약한 시각에 실행. Schedule runs 설정 방법은 "<a href="undefined-5.md">테스트 실행 (예약)</a>" 참조</td></tr></tbody></table>



Advanced Settings 에 대한 설명은 아래 내용을 참고해 주시기 바랍니다.

* <mark style="color:blue;">Save daily summary report</mark> : 테스트 종료 시 summary report 저장 여부 선택
* <mark style="color:blue;">Persist transaction data for all test results</mark> : 테스트 종료 시 기본적으로는 test fail 항목에 대해서만 detail view 패널 확인이 가능하지만 본 옵션 체크 시 모든 테스트 항목에 대해 detail view 제공
* <mark style="color:blue;">Send report mail</mark> : 테스트 종료 시 report mail 전송 여부 선택

#### 4) Run 버튼 클릭

아래의 Run 버튼 클릭 시 테스트가 실행되면서 "API Test Result" page로 전환됩니다.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>



## UI Test

서비스 준비 중입니다.



## Performance Test

서비스 준비 중입니다.

