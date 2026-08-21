---
title: "Excel 워크시트의 암호 보호 설정 수정하기"
second_title: "문서"
linktitle: "Excel 파일 암호 수정하기"
type: docs
url: /workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "Excel 암호, Aspose.Cells Cloud, 쓰기 보호, REST API, 워크시트 암호 수정"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용해 Excel 워크시트의 쓰기 보호 암호를 변경합니다. cURL 및 SDK 예제 포함."
weight: 100
ArticleTitle: "Excel 워크시트의 암호 보호 설정 수정하기 – Aspose.Cells Cloud"
---

이 REST API는 기존 Excel 워크시트의 **쓰기 보호 암호를 변경**합니다.

프로그래밍 방식으로 쓰기 보호 암호를 업데이트하면 파일을 다운로드하지 않고도 암호를 교체하거나 갱신할 수 있습니다. 특히 Aspose.Cells Cloud 스토리지에 저장된 보안 워크시트를 관리할 때 유용합니다.


## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### 보안 및 인증

Aspose.Cells Cloud API는 보안이 강화되었으며 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.


### 요청 매개변수

| 매개변수 이름   | 유형   | 위치    | 설명                                             |
| --------------- | ------ | ------- | ------------------------------------------------ |
| **name**        | string | path    | Excel 워크시트 이름(필수).                        |
| **password**    | string | body (JSON) | 설정할 새 쓰기 보호 암호(필수).                 |
| **folder**      | string | query   | 워크시트가 저장된 선택적 폴더.                    |
| **storageName** | string | query   | 선택적 스토리지 서비스 이름.                      |

### 응답

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                               |
|------|-----------------------------|----------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에는 작업 세부정보 포함. |
| 400  | 잘못된 요청                  | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | 인증되지 않음                | 잘못되거나 누락된 JWT 토큰.                         |
| 413  | 요청 본문이 너무 큼          | 업로드된 파일이 크기 제한을 초과함.                 |
| 500  | 내부 서버 오류               | 예기치 않은 서버 오류.                              |

## SDK를 사용하여 PutDocumentProtectFromChanges API를 사용하는 방법

### PutDocumentProtectFromChanges API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges)은 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스를 쉽게 접근할 수 있습니다. 아래의 cURL 명령은 Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ "Password": "aspose" }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 가장 빠르게 개발할 수 있습니다. SDK는 저수준 세부사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}
---