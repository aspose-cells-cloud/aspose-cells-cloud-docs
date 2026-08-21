---
title: "엑셀 워크시트에서 차트 범례 숨기기 – Aspose.Cells Cloud API"
type: docs
url: /charts/legend/hide/
aliases: [/hide-chart-legend-in-a-worksheet/]
weight: 110
keywords: "Aspose.Cells, 엑셀, 차트 범례 숨기기, REST API, 클라우드 SDK, 차트 범례"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트에서 차트 범례를 숨기는 방법을 배웁니다. HTTPS 엔드포인트, 필요한 인증, 요청 구문, 응답 세부 정보, 오류 처리 및 SDK 예제를 포함합니다."
---

이 REST API는 차트의 범례를 숨깁니다. **차트 범례**는 차트에 표시된 데이터 시리즈를 식별하는 상자입니다.

이 API는 유효한 Aspose Cloud JWT 토큰이 필요하며, 워크북은 Aspose Cloud 저장소에 업로드되어 있어야 하며, 사용되는 API 버전은 **v3.0**입니다.

## 보안 및 인증
Aspose.Cells Cloud API는 보안을 위해 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### 요청 매개변수

| 매개변수 이름   | 유형    | 위치   | 설명                            |
| --------------- | ------- | ------ | ------------------------------- |
| **name**        | string  | 경로   | 워크북 이름.                    |
| **sheetName**   | string  | 경로   | 워크시트 이름.                  |
| **chartIndex**  | integer | 경로   | 차트의 인덱스.                  |
| **folder**      | string  | 쿼리   | 워크북 폴더 (선택 사항).        |
| **storageName** | string  | 쿼리   | 저장소 이름 (선택 사항).        |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend)은 이 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의합니다.

cURL 명령줄 도구를 사용하여 API를 쉽게 호출할 수 있습니다. 아래 예제는 _Sample_Test_Book.xls_ 파일의 차트 0번에 대한 범례를 숨기는 요청을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 응답

| HTTP 상태 코드                | 설명                                      | 예시 JSON                                                  |
| ----------------------------- | ----------------------------------------- | ---------------------------------------------------------- |
| **200 OK**                    | 범례가 성공적으로 숨겨졌습니다.            | `{ "Code": 200, "Status": "OK" }`                          |
| **401 Unauthorized**          | JWT 토큰이 누락되었거나 유효하지 않습니다.  | `{ "Code": 401, "Message": "Invalid access token." }`      |
| **404 Not Found**             | 워크북, 워크시트 또는 차트가 존재하지 않습니다. | `{ "Code": 404, "Message": "Chart not found." }`           |
| **500 Internal Server Error** | 예기치 않은 서버 오류입니다.               | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## FAQ

**Q:** _Aspose.Cells Cloud를 사용하여 차트 범례를 숨기는 방법은?_  
**A:** 유효한 JWT 토큰을 `Authorization` 헤더에 포함하여 `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` 엔드포인트에 `DELETE` 요청을 보내세요. `200 OK` 응답은 성공을 의미합니다.

**Q:** _차트 범례 숨기기 API에 필요한 인증은?_  
**A:** `Authorization: Bearer <jwt token>` 헤더를 포함해야 합니다. 이 토큰은 Aspose Cloud OAuth 흐름을 통해 획득할 수 있습니다.

**Q:** _차트 인덱스가 잘못되었을 경우 어떤 오류 응답을 받나요?_  
**A:** `404 Not Found` 상태 코드와 함께 `Code: 404` 및 누락된 차트에 대한 설명을 포함하는 JSON 본문이 반환됩니다.

**Q:** _HTTP를 사용할 수 있나요? (HTTPS가 아닌)_  
**A:** 아닙니다. 보안을 위해 모든 Aspose Cloud 엔드포인트는 HTTPS를 사용해야 합니다.

## 클라우드 SDK 패밀리

SDK를 사용하면 가장 빠르게 개발할 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**곧 제공 예정** – Swift SDK 예제가 곧 추가됩니다.  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "엑셀 워크시트에서 차트 범례 숨기기 – Aspose.Cells Cloud API",
  "description": "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트에서 차트 범례를 숨기는 단계별 가이드입니다. HTTPS 엔드포인트, 인증, 요청 구문, 응답 세부 정보, 오류 처리 및 SDK 예제를 포함합니다.",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "홈", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Charts", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "차트 범례 숨기기", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "Aspose.Cells Cloud API를 사용하여 차트 범례 숨기기"
}
</script>