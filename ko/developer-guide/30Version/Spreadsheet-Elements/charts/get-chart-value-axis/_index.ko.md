---
title: "차트 값 축 가져오기"
type: docs
url: /ko/charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, 차트 값 축, REST API, Excel, 클라우드 SDK, 차트 값 축 가져오기
description: "Aspose.Cells Cloud REST API - 클라우드에 저장된 Excel 워크시트에서 차트의 값 축을 검색합니다."
ArticleTitle: "차트 값 축 가져오기 - Aspose.Cells Cloud REST API"
---

이 REST API는 차트의 값 축을 검색합니다. 이는 **Aspose.Cells Cloud REST API**의 일부이며, 클라우드에 저장된 Excel 워크시트와 상호 작용합니다.

관련 작업은 **[차트 범주 축 가져오기](/charts/category-axis/get/)** 엔드포인트를 참조하십시오.

## GetChartValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                                |
| ------------- | ------- | ---- | --------------------------------------------------- |
| name          | string  | path | Excel 파일 이름(확장자 포함).                       |
| sheetName     | string  | path | 차트가 포함된 워크시트 이름.                        |
| chartIndex    | integer | path | 워크시트 내 차트의 0부터 시작하는 인덱스.           |
| folder        | string  | query | 파일이 위치한 클라우드 스토리지 폴더.               |
| storageName   | string  | query | 스토리지 서비스 이름(예: Aspose Cloud).             |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
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
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "값",
    "Format": {
      "NumberFormat": "일반",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**가능한 HTTP 상태 코드**

| 코드 | 설명                                                     |
|------|----------------------------------------------------------|
| 200  | 성공 – 값 축 정보가 반환됩니다.                          |
| 400  | 잘못된 요청 – 필수 매개변수가 누락되었거나 유효하지 않습니다. |
| 401  | 인증되지 않음 – 인증 토큰이 누락되었거나 유효하지 않습니다.   |
| 404  | 찾을 수 없음 – 지정된 워크북, 워크시트 또는 차트가 존재하지 않습니다. |
| 500  | 내부 서버 오류 – 서버에서 예기치 않은 오류가 발생했습니다. |

응답에는 `Minimum`, `Maximum`, `MajorUnit`, `MinorUnit`, `Title`, `Format` 등과 같은 속성이 포함된 자세한 `ValueAxis` 객체가 포함됩니다. 전체 구현에서는 추가 서식 세부 정보가 제공될 수 있습니다.

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK가 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
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