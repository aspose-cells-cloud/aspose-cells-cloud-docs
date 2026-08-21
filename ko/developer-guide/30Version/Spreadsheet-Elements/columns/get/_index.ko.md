---
title: 열 세부 정보 가져오기 – Aspose.Cells Cloud API 참조 (v4.0)
description: Aspose.Cells Cloud REST API를 사용하여 워크시트 열(인덱스, 너비, 스타일, 숨김 상태)에 대한 세부 정보를 검색합니다.
keywords: Aspose.Cells, 클라우드 API, 엑셀 열, 열 가져오기, REST API, JWT, 워크시트
date: 2026-07-30
---

# 열 세부 정보 가져오기  

Aspose Cloud 스토리지에 저장된 엑셀 워크북에서 특정 워크시트 열(인덱스, 너비, 스타일, 숨김 상태)에 대한 세부 정보를 검색합니다.

## 목차
1. [사전 요구 사항](#prerequisites)  
2. [인증](#authentication)  
3. [엔드포인트](#endpoint)  
4. [요청 매개변수](#request-parameters)  
5. [cURL 예제](#curl-example)  
6. [응답 예제](#response-example)  
7. [응답 스키마](#response-schema)  
8. [발생 가능한 오류](#possible-errors)  
9. [SDK 예제](#sdk-examples)  
10. [추가 자료](#additional-resources)  

---

## 사전 요구 사항
- Aspose Cloud 인증을 통해 얻은 유효한 **JWT 액세스 토큰**.  
- 워크북 파일은 Aspose Cloud 스토리지(또는 다른 지원되는 스토리지)에 저장되어 있어야 하며, 폴더 경로(해당되는 경우)를 알고 있어야 합니다.  

---

## 인증
모든 Aspose.Cells Cloud API는 **JWT 토큰 기반 인증**을 사용합니다. `Authorization` 헤더에 토큰을 포함하세요:

```http
Authorization: Bearer <access_token>
```

토큰 획득 방법에 대한 자세한 내용은 [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하세요.

---

## 엔드포인트
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – 워크북 파일 이름(예: `test.xlsx`).  
- **{sheetName}** – 워크시트 이름(예: `Sheet1`).  
- **{columnIndex}** – 검색할 열의 0부터 시작하는 인덱스입니다.

---

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되었으며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

## 요청 매개변수

| 이름            | 위치   | 유형     | 필수 여부 | 설명 |
|-----------------|--------|----------|-----------|------|
| **name**        | path   | string   | 예        | 워크북 파일 이름입니다. |
| **sheetName**   | path   | string   | 예        | 열이 포함된 워크시트입니다. |
| **columnIndex** | path   | integer  | 예        | 검색할 열의 0부터 시작하는 인덱스입니다. |
| **folder**      | query  | string   | 아니요    | 워크북이 위치한 스토리지 폴더입니다. |
| **storageName** | query  | string   | 아니요    | 스토리지 서비스 이름(예: Aspose Cloud Storage)입니다. |

---

## cURL 예제
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## 응답 예제
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## 응답 스키마
| 필드                 | 유형    | 설명 |
|----------------------|---------|------|
| `Column.GroupLevel`  | integer | 열의 개요 수준(그룹화에 사용됨)입니다. |
| `Column.Index`       | integer | 열의 0부터 시작하는 인덱스입니다. |
| `Column.IsHidden`    | boolean | 열이 숨겨진 경우 `true`, 그렇지 않으면 `false`입니다. |
| `Column.Width`       | number  | 열 너비(문자 단위)입니다. |
| `Column.Style`       | object  | 열의 스타일 리소스에 대한 `link`를 포함합니다. |
| `Column.link`        | object  | 열 리소스에 대한 자기 링크입니다. |
| `Code`               | integer | 응답의 HTTP 상태 코드입니다. |
| `Status`             | string  | 상태의 텍스트 설명(예: **OK**)입니다. |

---

## 발생 가능한 오류
| HTTP 상태 코드 | 코드 | 메시지                    | 발생 조건 |
|----------------|------|---------------------------|-----------|
| 400            | 400  | Bad Request               | 필수 매개변수 누락 또는 잘못된 형식. |
| 401            | 401  | Unauthorized              | `Authorization` 헤더 누락 또는 유효하지 않음. |
| 404            | 404  | Not Found                 | 워크북, 워크시트 또는 열이 존재하지 않음. |
| 500            | 500  | Internal Server Error     | 예기치 않은 서버 측 오류 발생. |

### 예제 – 404 Not Found
```json
{
  "Code": 404,
  "Message": "Column index out of range."
}
```

### 예제 – 401 Unauthorized
```json
{
  "Code": 401,
  "Message": "Invalid or missing authentication token."
}
```

---

## SDK 예제
다음 코드 스니펫은 공식 Aspose.Cells Cloud SDK를 사용하여 **Get Worksheet Columns** 작업을 호출하는 방법을 보여줍니다. Gist가 사용 불가능할 경우 예제 코드가 내장되어 제공됩니다.

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// API 클라이언트 설정
var apiInstance = new CellsApi("client_id", "client_secret");

// 필수 매개변수 설정
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // 선택 사항
string storageName = "MyStorage";    // 선택 사항

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Column Index: " + response.Column.Index);
    Console.WriteLine("Width: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.GetWorksheetColumns: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // 선택 사항
        String storageName = "MyStorage";    // 선택 사항

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Column index: " + result.getColumn().getIndex());
            System.out.println("Width: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Exception while calling CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # 선택 사항
storage_name = "MyStorage"  # 선택 사항

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Column index:", response.column.index)
    print("Width:", response.column.width)
except Exception as e:
    print("Exception when calling CellsApi->get_worksheet_columns:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // 선택 사항
const storageName = "MyStorage"; // 선택 사항

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Column index:", result.column?.index);
        console.log("Width:", result.column?.width);
    })
    .catch((error) => {
        console.error("Error calling getWorksheetColumns:", error);
    });
```

</details>

> **참고:** SDK는 `client_id` 및 `client_secret`을 제공한 후 자동으로 `Authorization` 헤더를 처리합니다.

---

## 추가 자료
- **OpenAPI 사양:** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **인증 가이드:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **GitHub 저장소 (SDK 및 샘플):** <https://github.com/aspose-cells-cloud>  

--- 

*문서 최종 업데이트일: 2026-07-30.*