---
title: "엑셀 워크시트에서 수식 계산하기"
second_title: "문서"
linktype: "계산"
type: docs
url: /ko/worksheets/calculate-formula/
aliases: [/ko/calculate-formula-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, 수식 계산, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트에서 수식을 계산합니다. 다양한 SDK(C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift)를 지원하며, 즉시 활용 가능한 예제를 제공합니다."
weight: 20
ArticleTitle: "엑셀 워크시트에서 수식 계산하기 – Aspose.Cells Cloud 문서"
---

이 REST API는 워크시트 내 **수식의 계산 결과값**을 반환합니다. 이를 통해 애플리케이션에서 엑셀 수식을 직접 **평가**할 수 있습니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                                         |
| -------------- | ------ | -------- | --------------------------------------------- |
| name           | string | path     | 엑셀 파일 이름.                              |
| sheetName      | string | path     | 수식이 포함된 워크시트 이름.                |
| formula        | string | query    | 평가할 수식 (예: `SUM(A5:A10)`).           |
| folder         | string | query    | 문서가 저장된 폴더.                          |
| storageName    | string | query    | 스토리지 서비스 이름 (해당되는 경우).       |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### 인증

모든 요청은 `Authorization` 헤더에 유효한 **Bearer JWT 토큰**을 포함해야 합니다:

```
Authorization: Bearer <your_jwt_token>
```

토큰은 Aspose.Cells Cloud 인증 가이드에 설명된 OAuth 2.0 흐름에 따라 얻을 수 있습니다.

### 가능한 응답 상태 코드

| 코드 | 설명                                             |
|------|--------------------------------------------------|
| 200  | 요청 성공 — 수식 결과가 반환됩니다.               |
| 400  | 잘못된 요청 — 누락되었거나 잘못된 매개변수.       |
| 401  | 인증되지 않음 — 유효하지 않거나 누락된 JWT 토큰.  |
| 404  | 찾을 수 없음 — 지정된 파일 또는 워크시트가 존재하지 않음. |
| 500  | 내부 서버 오류 — 서버에서 예기치 않은 조건 발생.   |

**cURL** 명령줄 도구를 사용하면 Aspose.Cells Cloud 웹 서비스를 쉽게 호출할 수 있습니다. 아래 예제는 cURL로 수식 결과를 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 API를 통합하는 가장 빠른 방법입니다. SDK가 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**참고:**  
- [워크시트 조회](https://docs.aspose.cloud/cells/ko/worksheets/get-worksheet/)  
- [워크시트 업데이트](https://docs.aspose.cloud/cells/ko/worksheets/update-worksheet/)  
- [모든 수식 계산](https://docs.aspose.cloud/cells/ko/worksheets/calculate-all-formulas/)  
---