---
title: "차트 범주 축 가져오기"
type: docs
url: /charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, 차트 범주 축, Excel, REST API, 클라우드 스토리지, OAuth2, API 문서"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 차트 범주 축을 가져옵니다."
ArticleTitle: "차트 범주 축 가져오기 – Aspose.Cells Cloud API 문서"
---

이 REST API는 차트의 **범주 축**(Category Axis)을 가져옵니다.  
이 엔드포인트를 호출하려면 유효한 OAuth 2.0 액세스 토큰을 제공해야 하며, 워크북 파일은 Aspose Cloud 스토리지에 저장되어 있어야 합니다.

**사전 요구 사항**  
이 엔드포인트를 사용하기 전에 다음 사항을 확인하십시오:  

- OAuth 2.0 토큰이 발급되었으며, Aspose Cloud 서비스에 유효한 상태여야 합니다.  
- 워크북 파일이 Aspose Cloud 스토리지(기본 또는 지정된 폴더)에 업로드되어 있어야 합니다.  
- 요청 URL에 표시된 대로 API 버전 **v3.0**을 사용 중이어야 합니다.  
- 호출 애플리케이션이 워크북을 읽고 해당 워크시트에 액세스할 수 있는 권한이 있어야 합니다.

## GetChartCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**배경** – 워크시트에서 모든 차트를 제거하는 것은 시트의 시각적 레이아웃을 초기화하거나, 오래된 시각화를 교체하거나, 이전 차트 데이터를 유지하지 않고 워크북을 재사용할 준비를 할 때 유용합니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                             |
| ------------- | ------- | ---- | ------------------------------------------------ |
| name          | string  | path | 워크북 파일의 이름입니다.                        |
| sheetName     | string  | path | 차트가 포함된 워크시트의 이름입니다.            |
| chartIndex    | integer | path | 요청된 축을 가진 차트의 0부터 시작하는 인덱스입니다. |
| folder        | string  | query | 워크북이 저장된 스토리지 내 폴더 경로입니다.     |
| storageName   | string  | query | 스토리지 서비스의 이름(기본이 아닌 경우)입니다.  |

### **응답**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미                   | 설명                                           |
|------|------------------------|------------------------------------------------|
| 200  | OK                     | 필터가 성공적으로 적용됨; 응답에 작업 세부정보가 포함됨. |
| 400  | Bad Request            | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized           | 잘못되거나 누락된 JWT 토큰.                     |
| 413  | Payload Too Large      | 업로드된 파일이 크기 제한을 초과함.            |
| 500  | Internal Server Error  | 예기치 않은 서버 오류.                          |

## SDK를 사용한 GetChartCategoryAxis API 사용 방법

### GetChartCategoryAxis API 사양

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
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
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
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