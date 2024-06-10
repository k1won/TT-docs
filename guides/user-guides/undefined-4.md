---
description: 예약한 시각에 테스트가 자동으로 실행되도록 설정하는 방법 및 절차를 설명합니다.
---

# 테스트 실행 (예약)

테스트 예약을 설정하는 과정은 테스트 실행에 필요한 script와 관련 실행 옵션들 그리고 시간 설정값을 구성해서 예약 작업(schedule job)을 생성하고 시스템에 등록하는 절차로 진행됩니다. Schedule job에는 두 가지 종류가 있는데 Periodic 과 Non-periodic 이 그것입니다.

* <mark style="color:blue;">**Periodic**</mark> : 특정 시간을 주기로 반복해서 실행하거나(Hour Timer) 매일 또는 특정 요일 특정 시각에 반복(Week Timer)
* <mark style="color:blue;">**Non-periodic**</mark> : 특정 날짜의 시, 분에 한 번만 실행

{% hint style="info" %}
Schedule job 은 workspace 당 최대 3개까지 등록이 가능합니다. (단, Non-periodic type 은 최대 1개만 등록 가능)
{% endhint %}

## API Test

API Test 실행을 위한 예약 설정은 아래와 같은 절차로 진행합니다.

#### 1) API Test page로 이동 (Workspace > Entry > API Test 버튼 클릭)

#### 2) Test script 선택

"테스트 실행"의 [이곳](undefined-3.md#id-2-test-script)을 참조하세요.

#### 3) Test option 설정

테스트 예약 실행을 위해 "Run Option"에서 "Schedule Runs"를 선택하세요. 그 외 다른 옵션 항목들에 대한 설명은 [이곳](undefined-3.md#id-3-test-option)을 참조해 주세요.

*   Periodic schedule job 설정\
    &#x20; 아래 그림과 같이 "Periodic" 항목을 check 상태로 유지하고 Hour Timer 또는 Week Timer 에 해당하는 시간값을 설정하세요\
    &#x20;&#x20;

    <div align="left">

    <figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

    </div>
*   Non-periodic schedule job 설정\
    &#x20;  아래 그림과 같이 "Periodic" 항목을 uncheck 상태로 유지하고 날짜와 시, 분 값을 설정하세요.\
    &#x20;&#x20;

    <div align="left">

    <figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

    </div>

#### 4) Apply 버튼 클릭

아래의 Apply 버튼 클릭 시 테스트 예약이 등록됩니다.

<div align="left">

<figure><img src="../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

</div>



## UI Test

서비스 준비 중입니다.



## Performance Test

서비스 준비 중입니다.

