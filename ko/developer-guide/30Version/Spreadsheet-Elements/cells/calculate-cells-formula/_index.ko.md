---
title: "셀 수식 계산 – Aspose.Cells Cloud API"
type: docs
url: /ko/calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, 셀 수식 계산, Excel API, REST API, SDK"
description: "Aspose.Cells Cloud REST API(v3.0)를 통해 Excel 셀 수식을 계산합니다. 엔드포인트, 매개변수, cURL 예제, SDK 스니펫이 포함됩니다."
ArticleTitle: "셀 수식 계산 – Aspose.Cells Cloud API 문서"
---

## REST API

이 REST API는 Excel 워크북 내 **셀 수식**을 계산합니다.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## 보안 및 인증

Aspose.Cells Cloud API는 보안이며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 매개변수 위치(경로/쿼리/본문) | 설명                                                            |
| ------------- | ------ | ----------------------------- | --------------------------------------------------------------- |
| name          | string | path                          | Excel 파일 이름(예: `Book1.xlsx`).                              |
| sheetName     | string | path                          | 셀이 포함된 워크시트 이름.                                       |
| cellName      | string | path                          | 계산할 셀의 주소(예: `A1`).                                      |
| options       | object | body                          | 계산 옵션이 포함된 JSON 객체(아래 **Options 객체** 표 참조).    |
| folder        | string | query                         | 파일이 위치한 저장소 폴더.                                      |
| storageName   | string | query                         | Aspose Cloud 저장소 이름.                                       |

#### Options 객체

| 필드            | 유형    | 설명                                                                       | 기본값  |
| --------------- | ------- | -------------------------------------------------------------------------- | ------- |
| CalcStackSize   | string  | 최대 계산 스택 크기.                                                       | `"1"`   |
| IgnoreError     | boolean | `true`인 경우 계산 오류는 무시되고 셀 값은 `#N/A`로 설정됩니다.            | `false` |
| Recursive       | boolean | 종속 셀에 대한 재귀 계산을 활성화합니다.                                    | `false` |
| Precision       | string  | 숫자 결과의 소수 자릿수.                                                   | `"15"`  |
| UseThreading    | boolean | 다중 스레드 계산을 활성화합니다.                                            | `false` |


### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                    | 설명                                              |
|------|-------------------------|---------------------------------------------------|
| 200  | OK                      | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함. |
| 400  | Bad Request             | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized            | 잘못되거나 누락된 JWT 토큰.                         |
| 413  | Payload Too Large       | 업로드된 파일이 크기 제한을 초과함.                 |
| 500  | Internal Server Error   | 예기치 않은 서버 오류.                              |

## SDK를 사용한 PostCellCalculate API 사용 방법

### PostCellCalculate API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API를 호출하는 방법을 보여줍니다. **먼저 `/connect/token` 엔드포인트에 인증하여 JWT 토큰을 획득**하고, `<jwt token>`을 실제 토큰 값으로 대체하세요.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
  -X POST \
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

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}
---