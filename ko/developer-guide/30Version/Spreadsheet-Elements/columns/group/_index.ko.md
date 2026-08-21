---
title: "열 그룹화 – Aspise.Cells 클라우드 API 문서"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에서 워크시트 열을 그룹화합니다. 요청 구문, 매개변수, cURL 및 SDK 예제, 응답 세부 정보가 포함됩니다."
keywords: "Aspose.Cells, 열 그룹화, Excel API, REST, 클라우드 SDK"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# Excel 워크시트에서 열 그룹화

**API 버전:** v3.0  
**작업:** `PostGroupWorksheetColumns` – 워크시트의 열을 그룹화합니다.

---

## 개요

이 REST API를 사용하면 워크시트에서 열 범위를 그룹화할 수 있습니다. 그룹화된 열은 표시하거나 숨길 수 있어 Microsoft Excel의 접기 기능과 유사한 섹션을 만들 수 있습니다.

---

## 사전 요구 사항

- Aspose Cloud 인증 서비스에서 가져온 유효한 **JWT 액세스 토큰**  
- 워크북은 Aspose.Cells Cloud에서 접근 가능한 위치(기본 스토리지 또는 사용자 정의 스토리지 이름)에 저장되어 있어야 합니다.  
- 사용하는 SDK의 요구 버전(SDK 사용 시): API 버전 **v3.0**을 지원하는 최신 릴리스  

---

## 인증

모든 요청은 **Bearer 토큰** 인증이 필요합니다.

```http
Authorization: Bearer <access_token>
```

토큰 획득 방법에 대한 자세한 내용은 [JWT 인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하세요.

---

## HTTP 요청

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| 매개변수 | 위치 | 필수 여부 | 설명 |
|---------|------|----------|------|
| `name` | 경로(Path) | 예 | 워크북 파일 이름(예: `test.xlsx`) |
| `sheetName` | 경로(Path) | 예 | 그룹화할 열을 포함하는 워크시트 이름 |
| `firstIndex` | 쿼리(Query) | 예 | 그룹에 포함할 첫 번째 열의 0부터 시작하는 인덱스 |
| `lastIndex` | 쿼리(Query) | 예 | 그룹에 포함할 마지막 열의 0부터 시작하는 인덱스 |
| `hide` | 쿼리(Query) | 아니요 | `true`인 경우 그룹화된 열이 숨겨지고, 그렇지 않으면 표시됩니다. |
| `folder` | 쿼리(Query) | 아니요 | 워크북이 포함된 폴더의 경로 |
| `storageName` | 쿼리(Query) | 아니요 | 파일이 위치한 스토리지 서비스 이름 |

---

## 요청 예제(cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **참고:** 요청은 암호화된 통신을 위해 **HTTPS**를 사용합니다.

---

## 응답

### 성공 (200)

| 필드 | 유형 | 설명 |
|------|------|------|
| `Code` | 정수 | HTTP 상태 코드(`200`) |
| `Status` | 문자열 | 작업의 텍스트 상태(`OK`) |

**예시**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### 오류(예: 400 Bad Request)

| 필드 | 유형 | 설명 |
|------|------|------|
| `Code` | 정수 | HTTP 상태 코드(`400`, `401`, `404`, `500` 등) |
| `Status` | 문자열 | 텍스트 상태(`Error`) |
| `ErrorMessage` | 문자열 | 문제에 대한 사람이 읽을 수 있는 설명 |
| `ErrorCode` | 문자열 | 오류의 프로그래밍 식별자 |

**예시 – 잘못된 요청(Bad Request)**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "잘못된 열 인덱스입니다.",
  "ErrorCode": "InvalidParameter"
}
```

---

## SDK 예제

다음 코드 스니펫은 지원되는 SDK를 사용하여 **워크시트 열 그룹화** 작업을 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## 참고 사항

- **그룹화 동작:** API는 Excel에서 확장 및 축소 가능한 열 그룹을 생성합니다. `hide=true`를 설정하면 그룹이 즉시 축소됩니다.  
- **0부터 시작하는 인덱스:** `firstIndex` 및 `lastIndex` 모두 **0**부터 시작하며, 워크시트의 첫 번째 열은 인덱스 0입니다.  
- **스토리지 고려 사항:** 워크북이 기본 스토리지가 아닌 곳에 있는 경우, `folder` 및 `storageName` 쿼리 매개변수를 모두 제공해야 합니다.  

---

## 참고 자료

- [인증 – JWT 토큰 기반](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [워크시트 열 그룹화를 위한 OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [Aspose.Cells Cloud SDK (GitHub)](https://github.com/aspose-cells-cloud)  
- [Excel 워크시트에서 행 그룹화](/rows/group/)  

---

> *일러스트레이션:* ![Excel 워크시트에서 그룹화된 열을 보여주는 스크린샷](./images/group-columns.png){: .img-fluid alt="Excel 워크시트에서 그룹화된 열을 보여주는 스크린샷" }

*위의 플레이스홀더 이미지는 열 그룹화의 시각적 결과를 보여주는 실제 스크린샷으로 교체되어야 합니다.*