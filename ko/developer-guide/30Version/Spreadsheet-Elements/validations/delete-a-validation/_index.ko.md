---
title: "워크시트 유효성 검사 삭제 – Aspose.Cells Cloud"
second_title: "문서"
linktitle: "삭제"
type: docs
url: /ko/validations/delete/
keywords: "삭제, 워크시트 유효성 검사, Aspose.Cells Cloud, Excel API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일에서 워크시트 유효성 검사를 삭제하는 방법을 알아보세요. 엔드포인트, 매개변수, 인증 세부 정보, cURL 예제, 오류 처리 및 SDK 코드 스니펫이 포함되어 있습니다."
weight: 10
---

이 REST API는 Excel 워크시트에서 0부터 시작하는 인덱스를 기준으로 워크시트 유효성 검사를 삭제합니다.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **요청 매개변수**

| 매개변수 이름     | 유형     | 위치   | 설명                                           |
| ----------------- | -------- | ------ | ---------------------------------------------- |
| name              | string   | path   | Excel 파일의 이름입니다.                       |
| sheetName         | string   | path   | 워크시트의 이름입니다.                         |
| validationIndex   | integer  | path   | 삭제할 유효성 검사의 0부터 시작하는 인덱스입니다. |
| folder            | string   | query  | 문서가 포함된 폴더입니다.                      |
| storageName       | string   | query  | 스토리지 서비스의 이름입니다.                  |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 아래 예제는 cURL을 사용하여 유효성 검사를 삭제하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                           |
|------|--------------------------|------------------------------------------------|
| 200  | OK                       | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request              | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형) |
| 401  | Unauthorized             | 잘못되거나 누락된 JWT 토큰                       |
| 413  | Payload Too Large        | 업로드된 파일이 크기 제한을 초과함               |
| 500  | Internal Server Error    | 예기치 않은 서버 오류                            |

## 클라우드 SDK 패밀리

SDK를 사용하면 이 작업을 애플리케이션에 통합하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 워크시트 유효성 검사를 삭제하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}