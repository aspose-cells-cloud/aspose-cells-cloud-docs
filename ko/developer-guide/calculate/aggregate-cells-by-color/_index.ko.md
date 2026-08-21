---
title: "Aspose.Cells Cloud Web API – Excel에서 색상별 합계 및 개수 계산"
second_title: "문서"
ArticleTitle: "스프레드시트/Excel에서 색상별로 합계, 개수, 평균, 최대, 최소 값 계산"
LinkTitle: "색상별 셀 집계"
type: docs
url: /aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, aggregate, color, sum, count, average, min, max"
description: "Aspose.Cells Cloud API를 사용하여 Excel 셀을 배경색 또는 글꼴 색상별로 집계(합계, 개수, 평균, 최소, 최대)합니다. 엔드포인트, 매개변수, 인증 및 SDK 예제를 알아보세요."
weight: 100
---

## 개요

이 API는 셀의 **색상**을 기준으로 데이터를 계산할 수 있습니다. Excel 스프레드시트에서 셀의 채우기 색상 또는 글꼴 색상에 따라 합계, 개수, 평균, 최대값 및 최소값을 계산할 수 있습니다.

| 계산 작업 | 설명                                                     |
| :-------- | :------------------------------------------------------- |
| 개수      | 동일한 색상을 가진 셀의 개수를 구합니다.                  |
| 합계      | 동일한 색상을 가진 셀의 값 총합을 계산합니다.             |
| 최대값    | 동일한 색상을 가진 셀 중 가장 큰 값을 찾습니다.            |
| 최소값    | 동일한 색상을 가진 셀 중 가장 작은 값을 찾습니다.           |
| 평균값    | 동일한 색상을 가진 셀의 평균 값을 계산합니다.              |

## Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름   | 유형   | 위치     | 설명                                                         |
| :------------- | :----- | :------- | :----------------------------------------------------------- |
| Spreadsheet    | File   | FormData | 처리할 Excel 워크북 파일입니다.                              |
| Worksheet      | String | Query    | 범위가 포함된 워크시트 이름입니다.                           |
| Range          | String | Query    | A1 스타일 범위 (예: `A1:B10`)입니다.                         |
| Operation      | String | Query    | 계산 방법 – `Sum`, `Count`, `Average`, `Min`, `Max` 중 하나입니다. |
| ColorPosition  | String | Query    | 평가할 색상 유형 – `Background`, `Font` 중 하나입니다.      |
| Region         | String | Query    | 스프레드시트 지역 설정 (예: `us-east-1`)입니다.              |
| Password       | String | Query    | 보호된 워크북을 열기 위한 비밀번호 (선택 사항)입니다.         |

#### 열거형

- **ColorPosition**

  | 값         | 의미                       |
  | :--------- | :------------------------- |
  | Background | 셀의 채우기 색상을 사용합니다. |
  | Font       | 셀의 글꼴 색상을 사용합니다.   |

**예시 multipart/form-data 요청**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### 응답

아래 스키마는 응답 객체를 설명합니다. 스키마 뒤에 구체적인 예시가 있습니다.

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**예시 응답 (실제 값)**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                       |
| ---- | --------------------- | ---------------------------------------------------------- |
| 200  | OK                    | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함되어 있습니다. |
| 400  | Bad Request           | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 유형)입니다. |
| 401  | Unauthorized          | 잘못되었거나 누락된 JWT 토큰입니다.                          |
| 413  | Payload Too Large     | 업로드한 파일이 크기 제한을 초과했습니다.                    |
| 500  | Internal Server Error | 예기치 않은 서버 오류입니다.                                 |

## 색상별 집계 API는 어디에 사용해야 하나요?

스프레드시트에서 다양한 범주의 데이터는 일반적으로 색상으로 코드화됩니다. 이 API를 사용하면 각 색상 그룹에 대해 합계, 개수, 평균, 최소 및 최대 값을 계산하여 색상 기반 데이터 분석을 간소화할 수 있습니다.

## 왜 색상별 집계 API를 사용해야 하나요?

이 API는 사용자 정의 파싱 로직을 작성하지 않고도 색상 기반 계산을 빠르고 신뢰성 있게 수행할 수 있습니다. Aspose.Cells Cloud SDK와 원활하게 통합되므로 개발자는 몇 줄의 코드만으로 색상별 집계 기능을 구현할 수 있습니다.

## 색상별 집계 API를 SDK와 함께 사용하는 방법

### 색상별 집계 API 명세서

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">색상별 집계 API 명세서</a>는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 가장 빠르게 개발할 수 있는 방법입니다. SDK는 저수준 세부 사항을 추상화하여 단 몇 줄의 코드만으로 셀 색상별 집계 계산을 수행할 수 있습니다.  
Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 참조하세요.

아래 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**참고 사항:**

- 보호된 워크북을 사용하는 경우, 선택적 `Password` 쿼리 매개변수를 포함해야 하며, 그렇지 않으면 요청이 401 오류로 실패합니다.
- `Spreadsheet` 파일의 최대 요청 크기는 100MB입니다. 더 큰 파일을 처리해야 하는 경우, 워크북을 먼저 Aspose Cloud 스토리지에 업로드한 후 `Path` 매개변수를 통해 참조하는 방식을 고려해 보세요(여기서는 다루지 않음).