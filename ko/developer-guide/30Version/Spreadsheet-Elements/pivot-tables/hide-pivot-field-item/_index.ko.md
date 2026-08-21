---
title: "피벗 테이블에서 피벗 필드 항목 숨기기"
second_title: "문서"
linktitle: 숨기기
type: docs
url: /ko/pivot-tables/hide-pivot-field-item/
aliases: [  /ko/hide-pivot-field-item/ ]
keywords: "Aspose.Cells, 피벗 필드 항목 숨기기, 피벗 테이블 API, REST API, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 피벗 테이블에서 피벗 필드 항목을 숨기는 방법을 알아보세요. 요청 세부 정보, cURL 예제 및 여러 언어의 SDK 코드 스니펫을 포함합니다."
weight: 110
ArticleTitle: "피벗 테이블에서 피벗 필드 항목 숨기기 – Aspose.Cells Cloud API 가이드"
---

API를 호출하기 전에 다음 사항을 확인하십시오:

* 유효한 **JWT 액세스 토큰** (Aspose Cloud 인증 흐름을 통해 획득 가능).  
* 대상 워크북이 Aspose Cloud 스토리지에 업로드되어 있어야 합니다.  
* 워크시트와 피벗 테이블이 이미 생성되어 있어야 합니다.

이러한 사전 조건은 인증 오류 및 "리소스를 찾을 수 없음" 오류 응답을 방지합니다. 아래 단계에서는 API를 호출하기 전에 수행해야 하는 설정을 설명합니다.

이 REST API는 피벗 테이블의 피벗 필드 항목을 숨깁니다.

## PostPivotTableFieldHideItem API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름   | 유형    | 위치 | 설명                                                                                      |
| --------------- | ------- | ------ | ------------------------------------------------------------------------------------------- |
| name            | string  | path   | Excel 파일 이름.                                                                            |
| sheetName       | string  | path   | 피벗 테이블이 포함된 워크시트.                                                               |
| pivotTableIndex | integer | path   | 워크시트 내 피벗 테이블의 인덱스.                                                             |
| pivotFieldType  | string  | query  | 피벗 필드 유형(Row, Column, Page, Data 등).                                                  |
| fieldIndex      | integer | query  | 수정할 피벗 필드의 0부터 시작하는 인덱스.                                                    |
| itemIndex       | integer | query  | 숨길 특정 항목의 필드 내 인덱스.                                                              |
| isHide          | boolean | query  | 항목을 숨길 경우 **true**, 표시할 경우 **false**로 설정합니다.                               |
| needReCalculate | boolean | query  | 변경 후 피벗 테이블을 재계산할지 여부를 나타냅니다. 기본값은 **false**입니다.                |
| folder          | string  | query  | 워크북이 저장된 폴더 경로.                                                                   |
| storageName     | string  | query  | 스토리지 서비스 이름.                                                                        |

**필수 쿼리 매개변수 빠른 참고**

- **pivotFieldType** – 필드 유형(예: `Row`).  
- **fieldIndex** – 수정할 필드의 0부터 시작하는 인덱스.  
- **itemIndex** – 숨기거나 표시할 항목의 0부터 시작하는 인덱스.  
- **isHide** – 숨길 경우 `true`, 표시할 경우 `false`.  
- **needReCalculate** – 선택적, 기본값은 `false`.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**응답 세부 정보**

| 상태 코드 | 설명                                                              |
| --------- | ------------------------------------------------------------------- |
| 200       | 항목이 성공적으로 숨겨졌습니다.                                   |
| 400       | 잘못된 요청 – 누락되거나 잘못된 매개변수.                        |
| 401       | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰.                        |
| 500       | 서버 오류 – 작업을 완료할 수 없습니다.                |

**참고:** 제공된 `fieldIndex` 또는 `itemIndex`가 범위를 벗어나면 API는 **400 잘못된 요청** 응답을 반환합니다.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 API에 가장 빠르게 개발하는 방법입니다. SDK는 저수준 세부 정보를 처리하므로 비즈니스 로직에 집중할 수 있습니다. 완전한 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 피벗 필드 항목을 숨기는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // 워크북 및 워크시트 준비
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // 워크북 업로드
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // 피벗 테이블을 포함할 워크시트 생성
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // 샘플 데이터가 포함된 두 번째 워크시트 생성
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Sheet2에 샘플 데이터 가져오기
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // 간결함을 위해 축약
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // PivotSheet에 피벗 테이블 추가
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // 특정 행 필드 항목 숨기기
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**참고:** SDK 예제는 인증(JWT 토큰)이 이미 구성되어 있으며, 워크북이 지정된 스토리지 폴더에 있다고 가정합니다. 환경에 맞게 `folder` 및 `storageName` 매개변수를 적절히 조정하십시오.