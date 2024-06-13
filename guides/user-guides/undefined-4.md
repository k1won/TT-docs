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

{% hint style="warning" %}
User role 이 "Guest" 인 사용자는 테스트 예약 설정 또는 삭제 요청이 허용되지 않습니다.
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



## Schedule Job 확인

테스트 예약 상태 확인은 "Workspace > Test Schedule" 에서 확인 가능합니다. 아래 예시에서 총 3개의 schedule job 이 등록되었고, 그중 하나는 Non-periodic type 이, 나머지 두 개는 Periodic type 이 등록되었음을 확인할 수 있습니다.

각각의 schedule job 은 몇 가지 정보를 나타내는데 script title, test type, schedule job type, 예약자, 예약 시각 등을 포함합니다. 또한 각 schedule job 을 클릭하면 popup의 형태로 test option 과 실행할 item group에 대한 정보를 보여주는데 이를 통해 해당 schedule job에 대해 정확한 정보를 파악할 수 있도록 합니다.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption><p>등록된 schedule job 목록 확인</p></figcaption></figure>

## Schedule Job 삭제

등록된 schedule job 을 삭제하기 위한 방법은 다음과 같습니다. 삭제를 원하는 schedule job에 마우스 포인터를 위치시키면 해당 schedule job의 오른쪽 상단에 "x" 표시가 나타납니다. 해당 x를 클릭하세요.

<div align="left">

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption><p>특정 Schedule job 삭제 방법</p></figcaption></figure>

</div>

이후 삭제 확인을 위해 아래와 같이 팝업창이 실행되는데 삭제를 원할 경우 "OK" 버튼을 클릭하세요.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption><p>Schedule job 삭제 확인</p></figcaption></figure>

{% hint style="warning" %}
User role 이 "Tester" 인 경우 자신이 등록한 schedule job에 한 해 삭제 처리가 가능하고 "Manager" 이상인 경우 생성과 삭제가 모두 허용됩니다.
{% endhint %}

