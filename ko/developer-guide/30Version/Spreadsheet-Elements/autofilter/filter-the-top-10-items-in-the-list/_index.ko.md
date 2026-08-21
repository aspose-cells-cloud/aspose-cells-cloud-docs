---
title: "Excel 워크시트에 상위 10개 필터 추가(Aspose.Cells Cloud)"
ArticleTitle: "Excel 워크시트에 상위 10개 필터 추가 – Aspose.Cells Cloud"
second_title: "문서"
linktitle: "상위 10개 필터 추가"
type: docs
url: /autofilter/add-top-10-filter/
aliases:
  [/filter-the-top-10-items-in-the-list/, /autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, AutoFilter, Top 10 필터, Excel API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 상위 10개 AutoFilter를 적용하는 방법을 알아보세요. 엔드포인트, 매개변수, HTTPS cURL 예제, 인증 세부 정보, 오류 처리, C#, Java, Python 등 다양한 언어의 SDK 스니펫이 포함되어 있습니다."
weight: 65
---

이 REST API는 목록에서 **상위 10개** 항목을 필터링합니다.

> **사전 조건**  
> • Aspose.Cells Cloud 인증을 사용하여 유효한 JWT 토큰을 획득하세요.  
> • Excel 워크북을 Aspose Cloud 스토리지에 업로드하세요(또는 워크북이 위치한 스토리지/폴더를 지정하세요).  
> • 필터를 적용하려는 워크시트 이름과 셀 범위를 알아두세요.

## PutWorksheetFilterTop10 API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름     | 유형      | 위치   | 필수 | 기본값 | 설명                                                                 |
| ----------------- | --------- | ------ | ---- | ------ | --------------------------------------------------------------------- |
| **name**          | string    | path   | 예   | —      | Excel 파일 이름.                                                      |
| **sheetName**     | string    | path   | 예   | —      | 데이터가 포함된 워크시트 이름.                                        |
| **range**         | string    | query  | 예   | —      | 필터를 적용할 셀 범위(예: `A1:B10`).                                  |
| **fieldIndex**    | integer   | query  | 예   | —      | 필터를 적용할 열의 0부터 시작하는 인덱스.                             |
| **isTop**         | boolean   | query  | 예   | `true` | `true`이면 상위 항목을 필터링하고, `false`이면 하위 항목을 필터링합니다. |
| **isPercent**     | boolean   | query  | 아니요 | `false` | `true`이면 `itemCount`를 백분율로 처리하고, `false`이면 절대 개수로 처리합니다. |
| **itemCount**     | integer   | query  | 아니요 | `10`   | 필터에 포함할 항목 수.                                                |
| **matchBlanks**   | boolean   | query  | 아니요 | `false` | 필터 결과에 빈 셀을 포함할지 여부.                                    |
| **refresh**       | boolean   | query  | 아니요 | `false` | 필터 적용 후 필터를 새로 고칠지 여부.                                 |
| **folder**        | string    | query  | 아니요 | —      | Excel 파일이 위치한 스토리지 내 폴더.                                 |
| **storageName**   | string    | query  | 아니요 | —      | Aspose Cloud 스토리지 이름.                                           |

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**일반적인 오류 응답**

```json
{
    "Code":400,
    "Message":"Bad Request – missing or invalid parameters."
}
```

```json
{
    "Code":401,
    "Message":"Unauthorized – invalid or missing JWT token."
}
```

```json
{
    "Code":413,
    "Message":"Payload Too Large – uploaded file exceeds the allowed size."
}
```

```json
{
    "Code":500,
    "Message":"Internal Server Error – unexpected server condition."
}
```

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                                  |
|------|-----------------------------|-------------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰.                            |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함.                   |
| 500  | Internal Server Error       | 예기치 않은 서버 오류.                                 |

## SDK를 사용하여 PutWorksheetFilterTop10 API 사용 방법

### PutWorksheetFilterTop10 API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
  -X PUT \
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

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}