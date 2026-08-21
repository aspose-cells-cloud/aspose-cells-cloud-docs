---
title: "워크시트에 배경 이미지 추가"
second_title: "문서"
linktitle: "추가"
type: docs
url: /add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, 배경 이미지 추가, Excel API, REST, 클라우드 SDK, cURL, 워크시트 배경"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 배경 이미지를 추가하는 방법을 알아보세요. 필요한 매개변수, 인증 세부 정보, 전체 cURL 예제 및 오류 처리 정보를 포함합니다."
weight: 160
---

## REST API

이 REST API는 Excel 워크시트에 **배경 이미지**를 추가합니다.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.


### 쿼리 매개변수

| 매개변수 이름 | 유형   | 설명                                               |
| ------------- | ------ | -------------------------------------------------- |
| `picPath`     | string | 배경으로 사용할 이미지 파일의 경로입니다.         |
| `folder`      | string | 원본 워크시트가 포함된 폴더입니다.                |
| `storageName` | string | 파일이 위치한 스토리지 이름입니다.                |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명                                                   |
| ------------- | ---- | ------------------------------------------------------ |
| `datafile`    | file | 배경을 적용할 워크시트 파일입니다.                     |

**경로 매개변수** – URL의 `{name}`은 **워크시트 파일 이름**(예: `Book1.xlsx`)을 나타냅니다.


### **응답**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                |
| ---- | --------------------- | --------------------------------------------------- |
| 200  | OK (성공)             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request (잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식) |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰                         |
| 413  | Payload Too Large (페이로드가 너무 큼) | 업로드된 파일이 크기 제한을 초과함          |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류 발생                   |

## SDK를 사용하여 PutWorkbookBackground API 사용 방법

### PutWorkbookBackground API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 아래 예제는 multipart 파일 업로드 플래그와 필요한 인증 헤더를 포함한 전체 요청을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
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


### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 가장 빠른 개발 방법입니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}