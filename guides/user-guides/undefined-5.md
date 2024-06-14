---
description: 테스트 결과를 확인하는 방법과 리포트 화면을 구성하는 각각의 영역에 대해 설명합니다.
---

# 테스트 결과 확인

## API Test Result

Schedule 이 아닌 manual run 을 통해 테스트를 실행한 경우 아래의 화면으로 이동하고 리포트를 위한 준비 단계를 거쳐 test item 별 시험 결과가 실시간으로 화면에 업데이트됩니다.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (2).png" alt=""><figcaption><p>테스트 실행 준비 상태</p></figcaption></figure>

테스트 종료 시 시험 결과와 관련 통계가 업데이트되고, test item의 개별 실행 결과가 테이블의 형식으로 보고됩니다.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (2).png" alt=""><figcaption><p>테스트 종료 상태</p></figcaption></figure>

### Summary

Summary 영역은 테스트에 대한 몇 가지 정보를 나타내는데 script의 title 과 test state, 실행 시각 그리고 시험자 이메일 등이 포함됩니다. Test state에 표시될 수 있는 내용과 의미는 아래 테이블을 참고해 주시기 바랍니다.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (2).png" alt=""><figcaption><p>Test Summary</p></figcaption></figure>

<table><thead><tr><th width="154" align="center">State</th><th>Description</th></tr></thead><tbody><tr><td align="center">Running</td><td>테스트가 실행되어 진행 중인 상태</td></tr><tr><td align="center">Standby</td><td>다른 사용자에 의해 테스트가 이미 진행 중인 상태. 먼저 실행 중인 테스트가 종료되면 곧바로 Running 상태가 된다.</td></tr><tr><td align="center">Success</td><td>모든 test case 가 Pass 처리되고 테스트가 종료된 상태</td></tr><tr><td align="center">Failed</td><td>Pass 되지 못하고 결함/오류(Fail) 처리된 test case 가 한 건 이상 발생한 채 테스트 종료된 상태</td></tr><tr><td align="center">Error</td><td>Script error 발생한 채 테스트 종료된 상태</td></tr><tr><td align="center">Aborted</td><td>테스트 진행(Running) 중 Stop 버튼을 클릭하여 테스트 종료된 상태</td></tr><tr><td align="center">TimedOut</td><td>Test option 중 timeout으로 설정한 시간을 초과하여 테스트 실행이 강제 종료된 상태</td></tr><tr><td align="center">Cancelled</td><td>테스트 예약 후 실행 시점에 가용 리소스 소진으로 인해 실행되지 못하고 종료된 상태</td></tr><tr><td align="center">UnknownERR</td><td>비정상 종료</td></tr></tbody></table>

### Control

테스트 제어를 위한 기능으로 Running 상태에서는 테스트 종료를, 완료 상태에서는 재실행을 수행합니다.

<figure><img src="../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>

Control 버튼 우측의 역삼각형 버튼은 test option 과 item group 설정값을 팝업창의 형태로 나타냅니다. 테스트 종료 후 "Run Again" 버튼을 클릭하면 동일한 조건으로 테스트를 재실행 하게 됩니다.

<figure><img src="../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

### Filter

[Result table](undefined-5.md#result-table)의 첫 번째 칼럼(Result) 값들을 통해 필터링 기능을 제공합니다.

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

* 예시) All Items

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

* 예시) Passed

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

### Statistics

테스트 종료 시 아래와 같이 통계 데이터가 업데이트됩니다. 각 항목에 대한 설명은 아래 테이블을 참고해 주세요.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

<table data-header-hidden><thead><tr><th width="158" align="center"></th><th></th></tr></thead><tbody><tr><td align="center">Iterations</td><td>Test script 총 반복 횟수</td></tr><tr><td align="center">Duration</td><td>테스트 실행에 소요된 시간</td></tr><tr><td align="center">All Items</td><td>Test item의 총합</td></tr><tr><td align="center">All Requests</td><td>Target system으로 전송한 HTTP Request message의 총합</td></tr><tr><td align="center">All Tests</td><td>Test case의 총합. Postman에서 assertion code 즉, pm.test() 실행 횟수를 의미. <a href="undefined-5.md#result-table">Result table</a>의 "TotalAssertions" 칼럼 값의 총합</td></tr><tr><td align="center">Test Fail</td><td>Assertion code에서 fail 발생 횟수. <a href="undefined-5.md#result-table">Result table</a>에서 "FailedCount" 칼럼 값의 총합</td></tr><tr><td align="center">Error</td><td>Script error 발생 총합</td></tr><tr><td align="center">Avg.Rsp.Time</td><td>모든 HTTP Request에 대한 평균 응답(response) 시간</td></tr></tbody></table>

### Result table

Test item 별 테스트 결과와 테스트 정보 등을 나타냅니다. 구성 정보는 크게 다섯 종류로 구분되는데 test result, request info, response info, test case info, view control 등이고, 각각에 대한 설명은 아래 테이블을 참고해 주세요.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="158" align="center"></th><th></th></tr></thead><tbody><tr><td align="center">Test result</td><td>해당 test item에서 실행된 test case 들의 시험 결과(Pass/Fail/Error)</td></tr><tr><td align="center">Request info</td><td>테스트를 위해 target system으로 전송한 HTTP Request message의 요약 정보</td></tr><tr><td align="center">Response info</td><td>Request 전송 후 target으로부터 수신한 HTTP Response message의 요약 정보</td></tr><tr><td align="center">Test case info</td><td>Pass 처리된 test case와 fail 처리된 test case 그리고 각각에 대한 통계를 나타냄</td></tr><tr><td align="center">View control</td><td>보다 자세한 HTTP message 및 로그 등을 확인할 수 있는 detail-view side panel 을 열기 위한 버튼</td></tr></tbody></table>

### Detail view

[Result table](undefined-5.md#result-table) 이 테스트를 위해 실행된 모든 test item 들에 대한 요약 정보를 나타낸 것이라면 detail-view에서는 특정 test item에 대한 상세 시험정보를 확인할 수 있습니다. 기본적으로 "Fail" 또는 "Error"의 테스트 결과를 갖는 test item 들에 한 해 detail-view side panel 을 열 수 있는 링크("open")가 생성됩니다.

{% hint style="info" %}
테스트 결과 상관없이 모든 test item 에 대해 "open" 링크 생성을 원할 경우 "[테스트 실행](undefined-3.md)"을 참고하여 "API Test > Run Configuration > Advanced Settings"에서 "Persist transaction data for all test results" 항목을 체크하시기 바랍니다.
{% endhint %}

Result table 의 DetailView 칼럼에서 상세정보 확인을 원하는 test item의 "open" 링크를 클릭해 보세요. 아래와 같이 브라우저 화면 좌측에서 side panel 이 나타나고 다양한 테스트 관련 정보들을 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (6) (1).png" alt=""><figcaption><p>특정 test item의 테스트 관련 상세 정보 보기</p></figcaption></figure>

Detail view는 네 개의 탭(tab)으로 구성되는데 각각 HTTP Request 와 Response message, 콘솔 로그 그리고 테스트 결과에 따라 오류 관련 정보 등을 담습니다. 탭 이름은 순서대로 "Request", "Response", "Console", "Failure"이고 각각에 대한 추가 설명은 아래 내용 참고하시기 바랍니다.

#### Detail  view 화면 구성 (Request, Response tab)

Detail view에서 제공하는 4가지 정보 유형 중 HTTP Request 와 Response에 대한 공통된 내용은 다음과 같습니다.

<figure><img src="../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

#### Detail  view 화면 구성 (Console, Failure tab)

Console tab에서는 script 실행 중 console 객체의 메시지 출력 메서드(log(), error() 등)에 의한 내용들을 확인할 수 있고, Failure tab에서는 test result 가 "Fail" 또는 "Error"일 경우 해당 오류에 대한 정보를 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>



***

## UI Test Result

서비스 준비 중입니다.

***

## Performance Test Result

서비스 준비 중입니다.

