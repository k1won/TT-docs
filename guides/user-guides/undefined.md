---
description: 사용자 정보 확인, API Key 갱신 및 로그인 비밀번호 변경 등의 절차를 설명합니다.
---

# 사용자 프로필 관리

## 사용자 정보 확인 (User Info)

로그인 상태에서 브라우저 우상단의 user icon 을 클릭하고 이후 팝업 메뉴에서 "My Profile" 버튼을 클릭하세요.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1).png" alt=""><figcaption><p>사용자 정보 확인을 위한 메뉴</p></figcaption></figure>



Profile page에서 확인할 수 있는 사용자 정보는 다음과 같습니다.

<figure><img src="../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption><p>Profile page에서 확인 가능한 사용자 정보</p></figcaption></figure>

<table data-header-hidden><thead><tr><th width="194"></th><th></th></tr></thead><tbody><tr><td>User Name</td><td>사용자 이름</td></tr><tr><td>Email</td><td>사용자 계정의 로그인 식별자</td></tr><tr><td>Company</td><td>사용자 소속의 기관 또는 기업 이름</td></tr><tr><td>Role</td><td>TestTracker에서 사용자 그룹의 권한 분류 중 현재 사용자 자신에게 설정된 값.</td></tr><tr><td>Profile</td><td>업무 역할 등 부가정보</td></tr><tr><td>API Key</td><td>REST API를 통해 TestTracker 제어 시 사용자 식별 및 인증 수단</td></tr><tr><td>Key expiration</td><td>API Key 만료 일자</td></tr></tbody></table>



## API Key 갱신

API Key는 서비스 계약기간 동안만 유효합니다. 만료일은 Profile page 내 "User Info" 탭에서 확인 가능하고, 만료되기 15일 전부터 TestTracker 로그인 시 아래와 같이 알림 메시지를 통해 갱신 안내 문구가 출력됩니다.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>API Key 만료일 도래 시 갱신 요청을 위한 알림 메시지</p></figcaption></figure>



API Key 갱신을 위해 Profile page의 "User Info" 탭에서 "Request Renew" 버튼을 클릭하세요.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>API Key 갱신 요청을 위한 기능 버튼</p></figcaption></figure>



API Key 갱신 요청이 TT-Admin에게 정상적으로 전송이 되면 아래와 같이 "Renew requested already.." 메시지가 출력되어 요청 상태를 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>API Key 갱신 요청이 전송된 상태</p></figcaption></figure>



TT-Admin에 의해 사용자의 API Key 가 갱신되면 Notification icon을 통해 처리 결과를 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>API Key 갱신 요청이 승인된 상태</p></figcaption></figure>



{% hint style="info" %}
TT-Admin에게 API Key 갱신 요청이 접수된 이후 이를 승인하는 절차는 관리자에 의해 몇 가지 확인 절차를 거친 후 처리되기에 즉각적이지 않을 수 있습니다. 이점 참고하시어 가급적 만료 전 충분한 여유를 두고 갱신 요청해 주시기 바랍니다.
{% endhint %}

{% hint style="warning" %}
API Key 만료 시 TestTracker에 로그인할 수 없고, REST API를 통한 테스트 실행 역시 불가합니다. 또한 만료 이후 장기간 재설정 요구가 없을 시 미사용 계정으로 간주되어 데이터베이스에서 영구 삭제 처리될 수 있으니 참고해 주시기 바랍니다.
{% endhint %}



## 사용자 정보 변경 (Edit Profile)

(추후 업데이트 예정)



## 주요 설정값 변경 (Settings)

(추후 업데이트 예정)



## 비밀번호 변경 (Change Password)

로그인 비밀번호를 변경하고자 할 경우 Profile page에서 "Change Password" 탭을 클릭하세요.&#x20;

<figure><img src="../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption><p>비밀번호 변경을 위한 입력 폼</p></figcaption></figure>

위와 같은 비밀번호 변경을 위한 입력 폼에서 비밀번호 설정 조건에 따라 입력 후 "Change Password" 버튼을 클릭하세요.



<figure><img src="../.gitbook/assets/image (13) (1).png" alt=""><figcaption><p>비밀번호 변경 완료 예시</p></figcaption></figure>

비밀번호 변경이 정상적으로 처리된 경우 위와 같이 안내 메시지가 말풍선과 함께 나타나고 잠시 뒤 화면에서 사라집니다.

