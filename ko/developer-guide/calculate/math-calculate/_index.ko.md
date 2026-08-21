---
title: "Aspose.Cells Cloud – 수학 계산 API(더하기, 빼기, 곱하기, 나누기, 백분율)"
second_title: "문서"
ArticleTitle: "스프레드시트/Excel에서 더하기, 빼기, 곱하기, 나누기 및 백분율 계산"
linktitle: "수학 계산"
type: docs
url: /ko/math-calculate/
keywords: "수학 계산 API, Aspose.Cells Cloud, Excel 계산, 더하기, 빼기, 곱하기, 나누기, 백분율, 대량 Excel 처리, REST API"
description: "Aspose.Cells Cloud 수학 계산 API를 사용하여 Excel 범위에 대해 더하기, 빼기, 곱하기, 나누기 또는 백분율 연산을 일괄 적용하는 방법을 알아보세요. 요청 형식, 샘플 코드 및 오류 처리 포함."
weight: 100
---

## **소개**: 스프레드시트 빠른 계산 – 한 번의 API 호출로 더하기, 곱하기, 빼기, 나누기 및 백분율 수식 처리

_수식을 직접 작성하지 않고도 전체 열, 행 또는 테이블에 대해 대량 계산을 수행하세요._

- **기본 수학 연산**: 범위 내 모든 셀을 임의의 숫자로 더하기, 빼기, 곱하기, 나누기
- **백분율 계산**: 백분율로 증가/감소 또는 숫자의 백분율 계산(예: +15%, -8%, 20% of…)
- **대량 처리**: 수천 개의 셀을 즉시 처리—셀 채우기 드래그, 배열 수식, VBA 불필요

| **계산 연산** | 설명 |
| :---------------------- | :---------- |
| **더하기**(Add)                 | +           |
| **빼기**(Subtract)            | -           |
| **곱하기**(Multiply)            | \*          |
| **나누기**(Divide)              | /           |
| **백분율**(Percentage)          | %           |

## **수학 계산 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 파라미터**

| 파라미터 이름 | 타입   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                              |
| :------------- | :----- | :-------------------------- | :--------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                    | 처리할 스프레드시트 파일을 업로드합니다.                                              |
| operation      | String | Query                       | 수행할 수학 연산(Add, Subtract, Multiply, Divide, Percentage)을 지정합니다. |
| value          | String | Query                       | 계산에 사용할 값(해당하는 경우)입니다.                                        |
| worksheet      | String | Query                       | 작업을 수행할 워크시트 이름입니다.                                                 |
| range          | String | Query                       | 계산에 포함할 셀 범위입니다.                                        |
| region         | String | Query                       | 스프레드시트 지역 설정입니다.                                                          |
| password       | String | Query                       | 보호된 스프레드시트 파일을 열기 위한 비밀번호입니다.                             |

### **응답**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**HTTP 상태 코드**

| 코드 | 의미               | 설명                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK (성공)                    | 필터가 성공적으로 적용됨; 응답에 연산 세부 정보 포함. |
| 400  | Bad Request (잘못된 요청)           | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식).      |
| 401  | Unauthorized (인증되지 않음)          | 잘못되거나 누락된 JWT 토큰.                                     |
| 413  | Payload Too Large (ペイロードが大きすぎます) | 업로드된 파일이 크기 제한을 초과함.                                 |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류.                                          |

## 수학 계산 API는 어디에 사용해야 하나요?

- **금융**: 전체 구매 가격 열에 13% 부가가치세(VAT)를 추가합니다.
- **재고**: kg 열을 2.2046배 곱하여 일괄 파운드로 변환합니다.
- **급여**: 모든 직원의 보너스 열에 고정 보너스 1,000을 추가합니다.
- **환율 변환**: 매출 열을 실시간 환율로 나누어 USD 금액을 계산합니다.
- **성적 부여**: 출석 패널티로 모든 학생 점수에서 5점을 뺍니다.
- **전자상거래**: 15% 프로모션 할인을 한 번의 클릭으로 제품 가격에 적용합니다.

## 수학 계산 API를 사용해야 하는 이유

- **빠른 Excel 계산** – 월말 리포트를 몇 초 만에 완료하세요.
- **Excel에서 대량 백분율 증가** – 가격, 예측, 수수료를 한 번의 클릭으로 업데이트하세요.
- **동일한 숫자를 전체 열에 추가** – 재고, 통화 변환, 단위 변환.
- **수식 없이 Excel 사용** – 비전문 사용자도 간편하게 사용 가능.
- 기존 SDK를 통해 개발을 빠르게 완료할 수 있습니다.

**참고**  
지원되는 최대 파일 크기는 200MB입니다. `range` 파라미터는 유효한 Excel 주소(A1:B10 등)여야 합니다. 매우 큰 워크시트의 경우 추가 처리 시간이 소요될 수 있습니다.

## SDK를 사용하여 수학 계산 API 사용하는 방법

### 수학 계산 API 사양

[Math Calculate Specification](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate)은 개발자가 웹 브라우저에서 직접 API와 상호 작용할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 사항을 추상화하여 간단한 코드만으로 셀 단위 수학 계산을 수행할 수 있어 개발 속도가 가장 빠릅니다.  
Aspose.Cells Cloud SDK 전체 목록은 [GitHub의 Aspose.Cells Cloud SDKs](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{</tab>}}
{{< /tabs >}}

---