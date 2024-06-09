---
description: 테스트 진행을 위해 필요한 사전 준비 절차(script 생성 및 test data upload)를 설명합니다.
---

# 테스트 구성

{% hint style="info" %}
Member role 이 "Manager" 이상인 사용자에게만 허용되는 기능입니다.
{% endhint %}

{% hint style="info" %}
Working directory의 허용된 저장 공간을 초과할 경우 script 또는 data file 생성 절차가 거부될 수 있습니다.
{% endhint %}

## API Test

TestTracker 의 API Test 기능은 [Postman](https://www.postman.com/)의 script format과 호환성을 유지합니다. 때문에 Postman에서 작성된 test code(collection, environment)를 TestTracker에서 어떠한 변경 없이 그대로 적용 후 사용할 수 있습니다. 단, TestTracker에서 collection이나 environment에 대한 직접적인 생성 또는 내용 수정을 지원하지는 않고, Postman에서 작성 후 script file export 후 해당 파일을 TestTracker에 업로드하는 방식으로 적용 가능합니다. (collection의 경우 추가적으로 URL fetch를 통한 적용도 가능)

#### collection 적용 (파일 업로드)

1. Postman에서 collection 작성 후 export ([참조](https://learning.postman.com/docs/getting-started/importing-and-exporting/exporting-data/#export-collections))
2.  TestTracker > Workspace > API Test > Collection Choose File 클릭\


    <div align="left">

    <figure><img src="../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

    </div>
3. 위 1. 에서 저장한 collection file 선택 후 열기(또는  OK) 버튼 클릭&#x20;
4. Upload 버튼 클릭

#### collection 적용 (URL)

1. Postman에서 collection 작성 후 우측 "참조" 내용을 바탕으로 access\_key 가 포함된 collection url 확인   ([참조](https://learning.postman.com/docs/collaborating-in-postman/sharing/#sharing-using-the-postman-api))
2.  TestTracker > Workspace > API Test > Collection URL 입력란에 위 1. 에서 확인한 주소 입력\


    <div align="left">

    <figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

    </div>
3. Fetch 버튼 클릭

#### environment 적용 (파일 업로드)

1. Postman에서 environment 작성 후 export ([참조](https://learning.postman.com/docs/getting-started/importing-and-exporting/exporting-data/#export-environments))
2.  TestTracker > Workspace > API Test > Environment Choose File 클릭\


    <div align="left">

    <figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

    </div>
3. 위 1. 에서 저장한 collection file 선택 후 열기(또는  OK) 버튼 클릭
4. Upload 버튼 클릭

#### 테스트 데이터  업로드

1.  TestTracker > Workspace > Test Data Choose File 클릭\


    <div align="left">

    <figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

    </div>
2. Data file 선택 후 열기(또는  OK)버튼 클릭
3. Upload 버튼 클릭

## UIUX Test

서비스 준비 중입니다.



## Performance Test

서비스 준비 중입니다.

