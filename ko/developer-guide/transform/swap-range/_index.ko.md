---
title: "Aspose.Cells Cloud – 열, 행 및 범위 교체 (v4.0)"
second_title: "문서"
ArticleTitle: "Excel에서 열, 행 및 셀 간 데이터 교체/교환"
linktype: "swap-range"
type: docs
url: /ko/swap-range/
keywords: "Aspose Cells, Excel API, 범위 교체, 클라우드 스프레드시트"
description: "Aspose.Cells Cloud API를 사용하여 Excel 파일에서 열, 행 또는 범위를 교체합니다. 단일 요청으로 포맷, 수식 및 셀 참조를 그대로 유지합니다."
weight: 100
---

Aspose.Cells Cloud API를 사용하여 Excel 파일 내에서 임의의 두 열, 행, 범위 또는 셀 간에 데이터를 자동으로 교환합니다. 범위 교체(Swap Range) API는 포맷, 수식 및 셀 참조를 모두 보존한 채로 정확한 데이터 교환을 가능하게 합니다. 복잡한 데이터 재구성, 일괄 처리 및 엔터프라이즈 워크플로우를 위한 원활한 클라우드 통합을 지원합니다.

## **범위 교체 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수**

| 매개변수 이름      | 유형   | 위치     | 설명                                                                                                                                   |
| ------------------ | ------ | -------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | 파일   | FormData | **필수.** 원본 Excel 워크북 파일(`.xlsx`, `.xls`).                                                                                     |
| **worksheet1**     | 문자열 | 쿼리     | **필수.** 첫 번째 데이터 영역을 포함하는 워크시트 이름.                                                                                |
| **range1**         | 문자열 | 쿼리     | **필수.** 교체할 `worksheet1` 내 셀 범위(예: `A1:D10`).                                                                               |
| **worksheet2**     | 문자열 | 쿼리     | **필수.** 두 번째 데이터 영역을 포함하는 워크시트 이름(`worksheet1`과 동일할 수 있음).                                                 |
| **range2**         | 문자열 | 쿼리     | **필수.** 교체할 `worksheet2` 내 셀 범위(예: `F1:I10`). **중요:** `range1`과 `range2`는 동일한 차원(크기)을 가져야 합니다.             |
| **outPath**        | 문자열 | 쿼리     | **선택 사항.** 수정된 워크북이 저장될 클라우드 스토리지 폴더.                                                                          |
| **outStorageName** | 문자열 | 쿼리     | **필수.** 설정된 클라우드 스토리지 서비스 이름(예: `MyCompanyStorage`).                                                                |
| **region**         | 문자열 | 쿼리     | **선택 사항.** 로케일 설정(예: `ko-KR`, `ja-JP`)으로, 포맷에 영향을 줄 수 있음.                                                        |
| **password**       | 문자열 | 쿼리     | **선택 사항.** 암호화된 스프레드시트를 해독하기 위한 비밀번호. 암호화되지 않은 경우 생략 가능.                                         |

**요청 예시(cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/swap/range?worksheet1=Sheet1&range1=A1:D10&worksheet2=Sheet2&range2=F1:I10&outStorageName=MyCompanyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### **응답**

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

**참고:**  
- API는 수정된 워크북을 파일 스트림 형태로 반환합니다. `outPath`가 지정된 경우, 파일은 지정된 클라우드 스토리지 위치에도 저장됩니다.  
- 범위 크기가 일치하지 않으면 **400 Bad Request** 오류가 발생합니다.

### 오류 코드

| 코드                 | 설명                                                         |
| -------------------- | ------------------------------------------------------------ |
| **400 Bad Request**  | 잘못된 요청 URI이거나 범위 크기가 일치하지 않습니다.           |
| **401 Unauthorized** | 잘못되거나 만료된 액세스 토큰; 클라이언트 ID 또는 비밀번호가 올바르지 않습니다. |
| **404 Not Found**    | 지정된 스프레드시트 파일에 접근할 수 없습니다.              |
| **500 Server Error** | 워크북 처리 중 내부 오류가 발생했습니다.                     |

## 범위 교체 API는 어디에 사용해야 하나요?

- **재무 모델 재구성** – 수식 및 조건부 서식을 보존한 채 데이터 블록을 재배열(예: 분기별 예측 데이터 이동).
- **데이터 파이프라인 및 ETL 프로세스** – 최종 출력 전에 원본 데이터 범위를 클린 데이터 범위로 스테이징 워크시트에서 교체.
- **오류 수정 및 데이터 복구** – 수동 복사·붙여넣기 없이 잘못 배치된 데이터를 빠르게 수정.

## 왜 범위 교체 API를 사용해야 하나요?

- **개발자 친화적** – 다양한 언어용 SDK가 제공되어 사용자 정의 솔루션 개발보다 개발 노력이 적습니다.
- **인건비 절감** – 수동 데이터 정리 작업을 자동화하여 집계 작업에 드는 수작업 필요성을 줄입니다.
- **사용량 과금** – 실제로 호출한 API 요청만 비용이 부과됩니다.
- **유지보수 없음** – 서버 관리, 소프트웨어 업데이트, 호환성 문제 등이 없습니다.

## SDK를 사용하여 범위 교체 API 사용하기

### 범위 교체 API 사양

[범위 교체 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/SwapRange)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 저수준 세부 사항을 추상화하여 간결한 코드로 범위를 교체할 수 있으므로 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}