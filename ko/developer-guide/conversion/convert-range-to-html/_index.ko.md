---
title: "Aspose.Cells Cloud – Excel 범위를 HTML로 변환"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일의 특정 범위(예: A1:C10)를 HTML 파일로 변환합니다. 인증, 요청 예시, 응답 처리, SDK 스니펫 및 오류 코드가 포함됩니다."
keywords: "Aspose.Cells, Excel을 HTML로, 범위 변환, 클라우드 API, 스프레드시트"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

로컬 Excel 워크북의 선택한 범위를 Aspose.Cells Cloud를 통해 직접 HTML 파일로 변환합니다. 이 변환은 클라우드 서버에서 완전히 처리되므로 전체 워크북을 업로드하거나 로컬에 Excel을 설치할 필요가 없습니다.

## 범위를 HTML로 변환 API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

요청 본문은 `multipart/form-data` 형식이며 스프레드시트 파일을 포함합니다. 기타 모든 옵션은 쿼리 파라미터로 제공됩니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구하는 안전한 API입니다.

### 요청 파라미터

| 이름               | 타입    | 위치     | 필수 여부 | 설명                                                                 |
| ------------------ | ------- | -------- | --------- | -------------------------------------------------------------------- |
| **Spreadsheet**    | 파일    | FormData | 예        | 변환할 Excel 워크북.                                                |
| **worksheet**      | 문자열  | 쿼리     | 예        | 범위가 포함된 워크시트 이름.                                         |
| **range**          | 문자열  | 쿼리     | 예        | 변환할 셀 영역(예: `A1:C10`).                                        |
| **outPath**        | 문자열  | 쿼리     | 아니요    | 생성된 HTML 파일을 저장할 폴더 경로(기본값 `null`).                 |
| **outStorageName** | 문자열  | 쿼리     | 아니요    | 출력 파일을 저장할 저장소 서비스 이름.                              |
| **fontsLocation**  | 문자열  | 쿼리     | 아니요    | 사용자 정의 글꼴 폴더 경로.                                         |
| **AutoRowsFit**    | 불리언  | 쿼리     | 아니요    | 워크시트의 모든 행을 자동으로 맞춤.                                 |
| **AutoColumnsFit** | 불리언  | 쿼리     | 아니요    | 워크시트의 모든 열을 자동으로 맞춤.                                 |
| **region**         | 문자열  | 쿼리     | 아니요    | 로케일 식별자(예: `en-US`, `fr-FR`). 숫자/날짜 포맷에 영향을 줌.    |
| **password**       | 문자열  | 쿼리     | 아니요    | 보호된 워크북을 열기 위한 비밀번호.                                 |
| **fontsLocation**  | 문자열  | 쿼리     | 아니요    | 사용자 정의 글꼴 위치.                                              |
| **region**         | 문자열  | 쿼리     | 아니요    | 스프레드시트 지역/언어 설정.                                        |
| **password**       | 문자열  | 쿼리     | 아니요    | 스프레드시트 파일을 열기 위한 비밀번호.                             |

## 응답

API는 변환된 HTML 파일을 **이진 스트림**(`application/octet-stream`)으로 반환합니다.

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### 성공 응답 예시 (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>제품</th><th>가격</th></tr>
  <tr><td>위젯 A</td><td>$10</td></tr>
  <tr><td>위젯 B</td><td>$15</td></tr>
</table>
```

응답 본문을 파일(예: `report.html`)로 저장하여 브라우저에서 렌더링된 표를 확인합니다.

---

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                            |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | 필터 적용 성공; 응답에 작업 세부 정보 포함.                     |
| 400  | Bad Request           | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식).        |
| 401  | Unauthorized          | 잘못되거나 누락된 JWT 토큰.                                      |
| 413  | Payload Too Large     | 업로드한 파일이 크기 제한을 초과함.                             |
| 500  | Internal Server Error | 예기치 않은 서버 오류.                                          |

## SDK와 함께 범위를 HTML로 변환 API 사용하기

### OpenAPI 명세서

[OpenAPI 명세서](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML)는 웹 브라우저에서 직접 REST 인터랙션을 수행할 수 있는 공개적으로 접근 가능한 API를 정의합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>제품</th><th>가격</th></tr>
  <tr><td>위젯 A</td><td>$10</td></tr>
  <tr><td>위젯 B</td><td>$15</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 저수준 세부 사항을 추상화하여 최소한의 코드로 데이터 범위를 HTML 파일로 빠르게 변환할 수 있어 개발 속도가 가장 빠릅니다.  
Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)에서 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 설명합니다. Gist에서 로딩가 차단될 경우 저장소에서 직접 예시를 다운로드할 수 있습니다.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}

---