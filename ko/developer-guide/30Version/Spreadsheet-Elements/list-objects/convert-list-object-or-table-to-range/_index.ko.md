---
title: "목록 개체를 범위로 변환 - Aspose.Cells Cloud API"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 목록 개체 또는 테이블을 범위로 변환"
second_title: "문서"
linktype: "변환"
type: docs
url: /ko/list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "Aspose Cells API, 목록 개체를 범위로 변환, Excel REST API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel ListObject(테이블)를 Range로 변환하는 방법을 알아보세요. 요청 구문, 매개변수, 샘플 cURL, 응답 스키마, 인증 세부 정보, 오류 코드 및 SDK 예제를 포함합니다."
weight: 30
---

이 REST API는 Excel 워크시트 내의 **ListObject**(테이블)를 **Range**로 변환합니다.

**필수 조건:**  
엔드포인트를 호출하기 전에 워크북이 Aspose Cloud 스토리지에 업로드되어 있고, 워크시트에 대상 ListObject가 존재하며, 지원되는 파일 형식(.xlsx, .xlsm 등)을 사용하고 있어야 합니다.

## REST API

**인증**  
이 작업을 호출하려면 `Authorization` 헤더에 유효한 JWT 토큰을 포함해야 합니다. 토큰은 클라이언트 ID와 클라이언트 비밀키를 사용하여 OAuth 2.0 토큰 엔드포인트에 POST 요청을 보내어 획득할 수 있습니다. 토큰에는 `Cells.ReadWrite` 범위가 포함되어야 하며, 토큰 서비스에서 반환된 기간 동안 유효합니다.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 이름                | 유형    | 위치   | 필수 여부 | 기본값 | 설명                                                       |
| ------------------- | ------- | ------ | -------- | ------ | ---------------------------------------------------------- |
| **name**            | string  | path   | Yes      | –      | Excel 파일의 이름입니다.                                   |
| **sheetName**       | string  | path   | Yes      | –      | ListObject가 포함된 워크시트의 이름입니다.                |
| **listObjectIndex** | integer | path   | Yes      | –      | 변환할 ListObject(테이블)의 0부터 시작하는 인덱스입니다.   |
| **folder**          | string  | query  | No       | –      | 파일이 저장된 폴더 경로입니다.                             |
| **storageName**     | string  | query  | No       | –      | 스토리지 서비스의 이름입니다.                              |

> **참고:** 이 작업은 **.xlsx**, **.xlsm** 등의 최신 Excel 형식에서만 작동합니다. ListObject는 보호되어 있어서는 안 됩니다. ListObject에 대한 자세한 내용은 [ListObjects 개요](/list-objects/)를 참조하세요. 범위 작업에 대한 자세한 내용은 [Ranges 문서](/ranges/)를 참조하세요.

### cURL 예제 (요청)

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

#### 응답 스키마

API는 새로 생성된 범위에 대한 세부 정보를 포함한 **200 OK** 응답을 반환합니다.

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| 필드            | 유형    | 설명                                            |
| --------------- | ------- | ----------------------------------------------- |
| **Code**        | integer | HTTP 유사 상태 코드(200은 성공을 나타냄).         |
| **Status**      | string  | 상태 메시지 텍스트입니다.                        |
| **RangeName**   | string  | 생성된 범위에 할당된 이름입니다.                 |
| **Address**     | string  | 워크시트 이름을 포함한 범위의 전체 주소입니다.   |
| **FirstRow**    | integer | 범위 내 첫 번째 행의 0부터 시작하는 인덱스입니다. |
| **FirstColumn** | integer | 범위 내 첫 번째 열의 0부터 시작하는 인덱스입니다. |
| **RowCount**    | integer | 범위의 행 수입니다.                              |
| **ColumnCount** | integer | 범위의 열 수입니다.                              |

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                             |
|------|------------------------------|--------------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                  | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                 | 유효하지 않거나 누락된 JWT 토큰입니다.             |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과했습니다.          |
| 500  | Internal Server Error        | 예기치 않은 서버 오류입니다.                       |

**오류 응답 스키마 (예시):**

```json
{
  "Code": 400,
  "Message": "Invalid listObjectIndex. Index must be between 0 and 5."
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 극대화할 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}