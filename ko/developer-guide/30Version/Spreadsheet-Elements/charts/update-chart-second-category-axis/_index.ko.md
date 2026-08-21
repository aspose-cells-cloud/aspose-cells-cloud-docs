---
title: "차트 두 번째 범주 축 업데이트"
type: docs
url: /ko/charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, 차트, 두 번째 범주 축, REST API, 차트 업데이트, 엑셀, 클라우드 API"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트의 차트 두 번째 범주 축을 업데이트하는 방법을 알아보세요."
ArticleTitle: "차트 두 번째 범주 축 업데이트 – Aspose.Cells Cloud API"
---

이 REST API는 차트의 두 번째 범주 축을 업데이트합니다.

## PostChartSecondCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                                  |
| ------------- | ------- | ---- | ----------------------------------------------------- |
| name          | string  | path | 엑셀 파일의 이름입니다.                              |
| sheetName     | string  | path | 차트가 포함된 워크시트 이름입니다.                   |
| chartIndex    | integer | path | 업데이트할 차트의 0부터 시작하는 인덱스입니다.        |
| axis          | object  | body | 새 설정이 포함된 두 번째 범주 축 객체입니다.         |
| folder        | string  | query | 파일이 저장된 폴더 경로입니다.                       |
| storageName   | string  | query | 스토리지 서비스의 이름입니다.                        |

**인증** – 이 API는 유효한 OAuth 2.0 액세스 토큰이 필요합니다. [인증 가이드](https://docs.aspose.cloud/cells/authentication/)에 따라 JWT 토큰을 생성한 후 아래 cURL 예제와 같이 `Authorization` 헤더에 토큰을 포함시킵니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* 축 설정 예: "Title": "새 축 제목", "IsVisible": true */
        }
      }'
```

*`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`을 실제 값으로 바꾸세요. 요청 본문에는 원하는 설정이 포함된 `axis` 객체가 포함되어야 합니다.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**성공 응답 (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "새 축 제목",
      "IsVisible": true,
      /* 추가 축 속성 */
    }
  }
}
```

**오류 응답**  

| 상태 코드 | 설명                                              |
|-----------|---------------------------------------------------|
| 400       | 잘못된 요청 – 누락되었거나 잘못된 매개변수입니다.     |
| 401       | 인증되지 않음 – 잘못되었거나 누락된 JWT 토큰입니다. |
| 404       | 찾을 수 없음 – 지정된 파일, 워크시트 또는 차트가 존재하지 않습니다. |
| 500       | 내부 서버 오류 – 서버에서 예기치 않은 조건이 발생했습니다. |

```json
{
  "Code": 400,
  "Message": "잘못된 요청 페이로드입니다."
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK는 저수준 세부 사항을 처리하여 개발을 간소화하고 비즈니스 로직에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
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

**참고 및 모범 사례**

* `chartIndex` 매개변수는 0부터 시작하며, 워크시트의 첫 번째 차트는 인덱스 0입니다.  
* 이 API는 `.xlsx` 및 `.xls` 워크북 형식을 모두 지원합니다.  
* `axis` 객체에는 필요한 속성만 포함하고, 지정하지 않은 속성은 기존 값이 유지됩니다.  
* 제한 초과를 방지하기 위해 속도 제한 가이드라인(일반적으로 계정당 분당 100회 요청)을 준수하세요.