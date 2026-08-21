---
title: "Excel 워크시트 줌 설정 – Aspose.Cells Cloud API v3.0"
second_title: "문서"
linktitle: "줌"
type: docs
url: /ko/worksheets/zoom/
aliases: [  /ko/set-zoom-in-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel 줌, 워크시트 줌, REST API, 클라우드 SDK, Excel 자동화"
description: "Aspose.Cells Cloud API v3.0을 사용하여 워크시트 줌(10~400%)을 설정하는 방법을 배워보세요. cURL 및 SDK 예제, 오류 처리를 포함합니다."
weight: 20
ArticleTitle: "Excel 워크시트 줌 설정 – Aspose.Cells Cloud API v3.0"
---

이 REST API는 Excel 워크시트의 줌 값을 설정합니다. **인증**이 필요하며, 모든 요청의 `Authorization` 헤더에 유효한 Bearer JWT 토큰을 포함해야 합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 보안이 강화되어 있으며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
```

### **요청 파라미터**

| 파라미터      | 유형     | 위치   | 설명                                                         |
| ------------- | -------- | ------ | ------------------------------------------------------------ |
| name          | string   | path   | Excel 파일(워크북)의 이름입니다.                             |
| sheetName     | string   | path   | 수정할 워크시트의 이름입니다.                                |
| value         | integer  | query  | 줌 퍼센트(허용 범위는 **10~400**, 예: `40`은 40%를 의미)입니다. |
| folder        | string   | query  | 파일이 저장된 폴더 경로입니다.                               |
| storageName   | string   | query  | 스토리지 서비스의 이름입니다.                                |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
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

**오류 응답 정보**  
가능한 HTTP 상태 코드는 다음과 같습니다:

- `400 Bad Request` – 누락되거나 잘못된 파라미터.
- `401 Unauthorized` – 누락되거나 잘못된 JWT 토큰.
- `404 Not Found` – 지정된 파일 또는 워크시트가 존재하지 않음.
- `500 Internal Server Error` – 예기치 않은 서버 측 오류.

각 오류 응답은 `Code`와 설명적인 `Message`를 포함하는 JSON 본문을 반환합니다.

## 클라우드 SDK 패밀리
SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리해 주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}
---