---
title: "Excel 파일에서 텍스트 찾기 – Aspose.Cells Cloud API"
description: "Aspose.Cells Cloud API를 사용하여 Excel(XLS, XLSX, XLSM, XLSB) 및 ODS 파일에서 특정 텍스트를 검색합니다. 요청 세부 정보, cURL 및 SDK 예제, 오류 처리가 포함됩니다."
keywords: "Aspose.Cells, Excel, 검색, API, REST"
type: docs
url: /ko/cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# Excel 파일에서 텍스트 찾기 – Aspose.Cells Cloud API

## 개요
Aspose.Cells Cloud는 Excel 워크북(XLS, XLSX, XLSM, XLSB) 및 OpenDocumentSpreadsheet(ODS) 파일 내에서 주어진 텍스트 문자열을 검색하는 **POST** 엔드포인트를 제공합니다. API는 요청된 텍스트를 포함하는 모든 셀과 일치하는 셀이 포함된 워크시트로 연결되는 링크를 반환합니다.

> **사용 사례**  
> - 추가 처리를 수행하기 전에 보고서에 특정 값이 존재하는지 검증합니다.  
> - 먼저 모든 발생 위치를 나열하는 빠른 “찾기 및 바꾸기” 도구를 구축합니다.  
> - 대량의 스프레드시트에서 주요 용어의 색인을 생성합니다.

---

## 사전 요구 사항
| 요구 사항 | 세부 정보 |
|-----------|-----------|
| **인증** | Aspose Cloud OAuth 흐름을 통해 획득한 JWT 토큰. 토큰에는 **Cells** 범위가 포함되어야 합니다. |
| **지원되는 형식** | XLS, XLSX, XLSM, XLSB, ODS |
| **최대 파일 크기** | 150 MB(압축 기준). 더 큰 파일은 **413 Payload Too Large**를 반환합니다. |
| **필수 헤더** | `Authorization: Bearer <jwt-token>`  <br> `Accept: application/json` |
| **권한** | 토큰은 대상 스토리지(원격 스토리지 사용 시)에 대한 *읽기* 권한이 있어야 합니다. `multipart/form-data`로 파일을 업로드하는 경우는 필요하지 않습니다. |

*팁:* JWT 토큰을 생성하려면 **/connect/token** 엔드포인트를 사용하세요. 자세한 내용은 [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하세요.

---

## 엔드포인트

| 항목 | 값 |
|------|-----|
| **HTTP 메서드** | `POST` |
| **URL** | `https://api.aspose.cloud/v3.0/cells/search` |
| **목적** | 업로드된 Excel 워크북 내에서 지정된 텍스트를 검색합니다. |
| **보안** | JWT 토큰(Bearer) – 위의 *사전 요구 사항* 참조. |

---

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 확보되어 있으며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

## 요청 매개 변수

| 이름 | 유형 | 위치 | 필수 여부 | 설명 |
|------|------|------|-----------|------|
| `file` | **file** | `formData`(multipart) | **필수** | 업로드할 스프레드시트 파일입니다. |
| `text` | **string** | 쿼리 문자열 | **필수** | 검색할 텍스트 문자열입니다. |
| `password` | **string** | 쿼리 문자열 | 없음 | 보호된 워크북을 열기 위한 암호(필요한 경우)입니다. |
| `sheetname` | **string** | 쿼리 문자열 | 없음 | 검색 범위를 제한할 워크시트 이름입니다. 생략 시 모든 워크시트를 검색합니다. |
| `checkExcelRestriction` | **boolean** | 쿼리 문자열 | 없음(기본값: `true`) | `true`인 경우 API는 검색 전에 Excel 관련 제한(예: 읽기 전용 셀)을 검증합니다. |

---

## 요청 예제(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

*`<jwt-token>`을 유효한 토큰으로 대체하고 필요에 따라 쿼리 매개 변수를 조정하세요.*

---

## 성공적인 응답

**HTTP 200 – 검색 성공; 응답에는 검색된 텍스트 항목이 포함됩니다.**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Invoice #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      },
      {
        "Text": "Invoice #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### 응답 필드

| 필드 | 유형 | 설명 |
|------|------|------|
| `Status` | string | 요청 전체 상태(`OK`는 성공을 의미) |
| `Code` | integer | HTTP 상태 코드(200) |
| `TextItems.link` | object | 컬렉션 리소스에 대한 하이퍼미디어 링크 |
| `TextItems.TextItemList` | array | 일치 항목 목록. 각 항목은 다음을 포함합니다: |
| `Text` | string | 검색 텍스트와 일치하는 셀 값 |
| `link` | object | 일치 항목이 있는 워크시트로 연결되는 하이퍼링크(`Href`는 `Workbook/worksheets/SheetName`을 가리킴) |

---

## 오류 응답

| HTTP 코드 | 의미 | 일반적인 원인 | 예제 본문 |
|-----------|------|---------------|--------------|
| **400** | 잘못된 요청 | 필수 매개 변수 누락, 지원되지 않는 파일 형식 또는 잘못된 쿼리 값 | `{ "Status":"Error","Code":400,"Message":"The 'text' query parameter is required." }` |
| **401** | 인증되지 않음 | 누락되거나 유효하지 않은 JWT 토큰 | `{ "Status":"Error","Code":401,"Message":"Invalid or expired access token." }` |
| **413** | 페이로드가 너무 큼 | 업로드된 파일이 150 MB 제한을 초과함 | `{ "Status":"Error","Code":413,"Message":"File size exceeds the allowed limit." }` |
| **500** | 내부 서버 오류 | 예상치 못한 서버 측 문제 | `{ "Status":"Error","Code":500,"Message":"An unexpected error occurred." }` |

---

## SDK 예제

아래는 공식 Aspose.Cells Cloud SDK를 사용한 **PostSearch** 작업을 위한 최소 코드 스니펫입니다. `YOUR_JWT_TOKEN`과 파일 경로를 귀하의 값으로 대체하세요.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Invoice",
            sheetname: "Sheet1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Invoice",
                null,          // password
                "Sheet1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Invoice",
        password=None,
        sheetname="Sheet1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "YOUR_JWT_TOKEN",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Invoice",
    sheetname: "Sheet1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*(PHP, Ruby, Go, Perl용 SDK는 [Aspose.Cells Cloud GitHub 저장소](https://github.com/aspose-cells-cloud)에서 제공됩니다.)*

---

## 추가 참고 사항

- **`checkExcelRestriction`**은 기본값이 `true`입니다. 워크북에 검색에 방해가 될 수 있는 보호된 셀이 포함되어 있지 않다는 것이 확실한 경우에만 `false`로 설정하세요.
- API는 **하이퍼미디어 링크**(`Href`)를 반환하며, 이를 사용하여 다른 Aspose.Cells 엔드포인트(예: 워크시트 다운로드 또는 셀 서식 검색)와 함께 사용할 수 있습니다.
- 큰 워크북을 검색할 때는 응답 시간을 개선하기 위해 `sheetname` 매개 변수로 범위를 좁히는 것을 고려하세요.

---

## 관련 링크

- **인증 가이드** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **PostSearch에 대한 OpenAPI 사양** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **Aspose.Cells Cloud SDK** – <https://github.com/aspose-cells-cloud>
- **요청 제한 및 할당량** – <https://docs.aspose.cloud/total/getting-started/limits/>