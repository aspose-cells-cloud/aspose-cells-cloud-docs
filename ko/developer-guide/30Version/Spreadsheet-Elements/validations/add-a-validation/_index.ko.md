---
title: "Excel 워크시트에 유효성 검사 규칙 추가"
second_title: "문서"
linktitle: "추가"
type: docs
url: /ko/validations/add/
keywords: "워크시트 유효성 검사 추가, Excel, Aspose.Cells Cloud, REST API, 스프레드시트, 유효성 검사 규칙"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일에 워크시트 유효성 검사 규칙을 추가합니다. C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift용 SDK가 제공됩니다."
weight: 10
---

이 REST API는 Excel 워크시트에 유효성 검사 규칙을 추가합니다.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **요청 파라미터**

| 파라미터 이름 | 유형   | 위치 | 설명                                                      |
| ------------- | ------ | ---- | --------------------------------------------------------- |
| name          | string | path | Excel 문서의 이름입니다.                                 |
| sheetName     | string | path | 워크시트의 이름입니다.                                   |
| range         | string | query | 유효성 검사가 적용될 셀 범위 (예: A1:B10)               |
| validation    | object | body | 유효성 검사 규칙 정의입니다.                             |
| folder        | string | query | 문서가 위치한 폴더입니다.                                |
| storageName   | string | query | 스토리지 서비스의 이름입니다.                            |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/WorksheetValidations/PutWorksheetValidation)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 Cloud API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

## Cloud SDK Family

SDK를 사용하는 것이 개발 속도를 높이는 최고의 방법입니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트의 핵심 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)에서 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}