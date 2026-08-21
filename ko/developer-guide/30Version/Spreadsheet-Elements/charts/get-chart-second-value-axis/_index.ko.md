---
title: "차트 두 번째 값 축 가져오기"
type: docs
url: /ko/charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, 차트 두 번째 값 축, Excel, REST API, 클라우드, API, Excel 차트 축
description: Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 특정 차트에서 두 번째 값 축을 검색합니다.
ArticleTitle: "차트 두 번째 값 축 가져오기 – Aspose.Cells Cloud API"
---

이 REST API는 차트의 두 번째 값 축을 검색합니다.

## GetChartSecondValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 확보되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                      |
| ------------- | ------- | ---- | ----------------------------------------- |
| name          | string  | path | Excel 파일의 이름입니다.                  |
| sheetName     | string  | path | 차트가 포함된 워크시트 이름입니다.        |
| chartIndex    | integer | path | 차트의 0부터 시작하는 인덱스입니다.       |
| folder        | string  | query| 파일이 저장된 폴더입니다.                 |
| storageName   | string  | query| Aspose Cloud 스토리지의 이름입니다.       |

**필수 조건**: 각 요청의 `Authorization` 헤더에는 Aspose Cloud OAuth2 흐름을 통해 획득한 유효한 JWT 액세스 토큰이 포함되어야 합니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다. 모든 Aspose Cloud 엔드포인트는 HTTPS를 사용해야 합니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "두 번째 값 축"
  }
}
```

**응답 필드**

- **Code** – 작업의 HTTP 상태 코드입니다(예: 성공 시 `200`).  
- **Status** – 상태의 텍스트 설명입니다(성공 시 `"OK"`).  
- **Axis** – 두 번째 값 축의 세부 정보가 포함된 객체입니다:  
  - **AxisId** – 축의 식별자입니다.  
  - **IsVisible** – 축이 표시되는지 여부를 나타내는 부울 값입니다.  
  - **MinimumScale** – 축에 표시되는 최소 값입니다.  
  - **MaximumScale** – 축에 표시되는 최대 값입니다.  
  - **MajorUnit** – 눈금선 주 단위 간격입니다.  
  - **MinorUnit** – 눈금선 부 단위 간격입니다.  
  - **Title** – 축의 제목 텍스트입니다.

**오류 응답**(200이 아닌 경우)

- `400 Bad Request` – 잘못된 매개변수 또는 잘못된 형식의 요청입니다.  
- `401 Unauthorized` – 누락되거나 유효하지 않은 JWT 토큰입니다.  
- `404 Not Found` – 지정된 파일, 워크시트 또는 차트가 존재하지 않습니다.  
- `500 Internal Server Error` – 예기치 않은 서버 오류입니다.

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 가장 좋은 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# 예제 플레이스홀더 -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java 예제 플레이스홀더 -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP 예제 플레이스홀더 -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby 예제 플레이스홀더 -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python 예제 플레이스홀더 -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android 예제 플레이스홀더 -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift 예제 플레이스홀더 -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl 예제 플레이스홀더 -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go 예제 플레이스홀더 -->

{{< /tab >}}

{{< /tabs >}}
---