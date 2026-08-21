---
title: "엑셀 워크북 보호 해제 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "엑셀 파일 보호 해제"
type: docs
url: /ko/excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells, 엑셀 보호 해제 API, 워크북 보호 제거, REST API, 클라우드 스프레드시트"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크북의 보호를 해제하는 방법을 알아보세요. 요청 구문, 매개변수, cURL 예제 및 여러 언어로된 SDK 코드가 포함되어 있습니다."
weight: 60
ArticleTitle: "엑셀 워크북 보호 해제 – Aspose.Cells Cloud API"
---

이 REST API를 사용하여 엑셀 워크북의 보호를 해제하세요.

## DeleteUnProtectWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 확보되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 경로 매개변수

| 매개변수 | 유형   | 설명                                     | 필수 여부 |
| ------- | ------ | ---------------------------------------- | -------- |
| **name**  | string | 워크북 파일 이름(확장자 포함).              | 예       |

### 쿼리 매개변수

| 매개변수 이름 | 유형   | 설명                                          |
| ----------- | ------ | --------------------------------------------- |
| folder      | string | 원본 워크북이 포함된 폴더 경로.                 |
| storageName | string | 워크북이 저장된 스토리지 서비스 이름.            |

### 요청 본문 매개변수

| 매개변수 이름 | 유형                      | 설명                                    |
| ----------- | ------------------------- | --------------------------------------- |
| protection  | WorkbookProtectionRequest | 제거할 보호 설정을 지정하는 객체입니다.      |

#### WorkbookProtectionRequest

| 매개변수 이름   | 유형   | 설명                                                                 |
| ------------- | ------ | -------------------------------------------------------------------- |
| ProtectionType | string | 제거할 보호 유형(`ALL`, `CONTENTS`, `NONE`, `OBJECTS`, `SCENARIOS`, `STRUCTURE`, `WINDOWS`). |
| Password      | string | 보호를 해제하는 데 필요한 비밀번호(선택 사항).                                     |

#### cURL 예제

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### 응답 (성공)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### HTTPS 상태 오류 응답

| HTTP 상태 코드 | 코드                  | 설명                                          |
| -------------- | --------------------- | --------------------------------------------- |
| 400            | BadRequest            | 누락되거나 잘못된 매개변수.                     |
| 401            | Unauthorized          | 잘못되거나 누락된 액세스 토큰.                  |
| 404            | NotFound              | 지정된 폴더/스토리지에서 워크북을 찾을 수 없음. |
| 500            | InternalServerError   | 예기치 않은 서버 오류.                          |

## SDK를 사용한 DeleteUnProtectWorkbook API 사용 방법

### DeleteUnProtectWorkbook API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 통합이 간편해지고 보일러플레이트 코드를 줄일 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---