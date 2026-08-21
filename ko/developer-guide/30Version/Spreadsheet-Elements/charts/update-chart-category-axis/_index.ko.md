---
title: "차트 범주 축 업데이트"
type: docs
url: /charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, 차트, 범주 축, REST API, Excel, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 차트 범주 축을 업데이트합니다."
ArticleTitle: "차트 범주 축 업데이트 – Aspose.Cells Cloud API"
---

이 REST API는 차트의 범주 축을 업데이트합니다.

## PostChartCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 확보되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 타입    | 위치 | 설명 |
| -------------- | ------- | -------- | ----------- |
| name           | string  | path     | Excel 파일의 이름입니다. |
| sheetName      | string  | path     | 차트가 포함된 워크시트의 이름입니다. |
| chartIndex     | integer | path     | 업데이트할 차트의 0부터 시작하는 인덱스입니다. |
| axis           | object  | body     | 범주 축 속성을 정의하는 JSON 객체입니다. |
| folder         | string  | query    | 파일이 위치한 클라우드 스토리지의 폴더 경로 (선택 사항). |
| storageName    | string  | query    | 스토리지의 이름 (선택 사항). |

**요청 본문 스키마 – `axis` 객체**

| 속성 | 타입   | 설명 |
|----------|--------|-------------|
| IsAutomaticMajorUnit | boolean | 주간격 단위를 자동으로 계산할지 여부를 나타냅니다. |
| MajorUnit | number | `IsAutomaticMajorUnit`이 `false`일 때의 주간격 단위 값입니다. |
| IsAutomaticMinorUnit | boolean | 부간격 단위를 자동으로 계산할지 여부를 나타냅니다. |
| MinorUnit | number | `IsAutomaticMinorUnit`이 `false`일 때의 부간격 단위 값입니다. |
| Title | object | 축의 제목 설정 (예: `Text`, `Font`, `Visible`). |
| TickLabelPosition | string | 눈금 레이블의 위치 (예: `Low`, `High`, `NextToAxis`). |
| ... | ... | API 사양에서 정의한 추가 축 속성입니다. |

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (성공)                          | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request (잘못된 요청)                 | 누락되거나 잘못된 파라미터 (예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized (인증되지 않음)                | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large (ペイロードが大きすぎます) | 업로드된 파일이 크기 제한을 초과했습니다. |
| 500  | Internal Server Error (내부 서버 오류)       | 예기치 않은 서버 오류. |

**사전 요구 사항 / 인증**

이 엔드포인트를 호출하려면 Aspose.Cells Cloud 인증 서비스(`/connect/token`)에서 JWT 액세스 토큰을 획득해야 합니다. 아래 예시와 같이 토큰을 `Authorization` 헤더에 포함시킵니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Category Axis",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**응답 예시**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### 참고 사항

* 이 엔드포인트는 HTTPS를 요구하며, HTTP를 사용할 경우 브라우저에서 혼합 콘텐츠 경고가 발생할 수 있습니다.
* 모든 자리 표시자 값(`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`)은 실제 식별자로 대체되어야 합니다.
* 범주 축 업데이트를 지원하는 차트 유형은 API 레퍼런스에 나열되어 있습니다.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}