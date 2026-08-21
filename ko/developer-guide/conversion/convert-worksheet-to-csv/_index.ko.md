---
title: "워크시트를 CSV로 변환 – Aspose.Cells Cloud API 문서"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 스프레드시트 워크시트를 CSV로 변환하는 방법"
linktitle: "워크시트를 CSV로 변환"
type: docs
url: /convert-worksheet-to-csv/
keywords: "Aspose.Cells, CSV 변환, 워크시트를 CSV로, REST API, 클라우드 스프레드시트, 엑셀을 CSV로"
description: "Aspose.Cells Cloud API(v4.0)를 사용하여 엑셀 파일에서 특정 워크시트를 CSV로 변환하는 방법을 알아보세요. 엔드포인트, 매개변수, 샘플 cURL, SDK 코드 및 오류 처리가 포함됩니다."
weight: 100
---

**ConvertWorksheetToCsv** 엔드포인트는 로컬 스프레드시트 파일의 단일 워크시트를 Aspose.Cells Cloud 서버 내에서 완전히 CSV 문서로 변환합니다. 소스 파일을 업로드하고 대상 워크시트를 지정하면, 클라우드 스토리지에 파일을 저장할 필요 없이 이진 CSV 스트림을 받을 수 있습니다. 이 API는 데이터 추출 자동화, 스프레드시트 데이터를 하위 시스템에 통합, 및 스토리지 오버헤드 감소에 이상적입니다.

## 워크시트를 CSV로 변환 API

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/csv
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치     | 필수/선택 사항 | 설명                                                                                                                                           |
| :------------ | :----- | :------- | :-------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | 파일   | FormData | **필수**        | 소스 스프레드시트의 이진 파일(예: `.xlsx`, `.xls`). 예: `myWorkbook.xlsx`.                                                                      |
| worksheet     | 문자열 | Query    | **필수**        | 변환할 워크시트 이름(대소문자 구분). 생략 시 첫 번째 워크시트가 사용됩니다. 예: `Sheet1`.                                                       |
| outPath       | 문자열 | Query    | 선택 사항       | 생성된 CSV가 저장될 클라우드 스토리지의 대상 폴더 경로. 생략 시 CSV는 응답 스트림에 직접 반환됩니다.                                              |
| outStorageName| 문자열 | Query    | 선택 사항       | 출력 파일을 저장할 스토리지 서비스(예: Azure, AWS S3)의 이름. `outPath`를 사용하는 경우에만 필요합니다.                                         |
| fontsLocation | 문자열 | Query    | 선택 사항       | 서버의 사용자 정의 글꼴 폴더 경로로, 변환 엔진이 비표준 글꼴을 사용할 수 있도록 합니다.                                                         |
| region        | 문자열 | Query    | 선택 사항       | CSV의 숫자/날짜 서식에 영향을 주는 로케일 식별자(예: `en-US`, `fr-FR`).                                                                         |
| password      | 문자열 | Query    | 선택 사항       | 보호된 스프레드시트를 열기 위한 비밀번호. 소스 파일의 암호화 비밀번호와 일치해야 합니다.                                                       |

### 응답

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

**HTTP 상태 코드**

| 코드 | 의미                 | 설명                                                           |
| ---- | -------------------- | -------------------------------------------------------------- |
| 200  | OK                   | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨.     |
| 400  | Bad Request          | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).       |
| 401  | Unauthorized         | 잘못되거나 누락된 JWT 토큰.                                     |
| 413  | Payload Too Large    | 업로드된 파일이 크기 제한을 초과함.                             |
| 500  | Internal Server Error| 예기치 않은 서버 오류.                                          |

## 워크시트를 CSV로 변환 API를 언제 사용하나요?

- **BI 파이프라인을 위한 데이터 추출** – 엑셀 보고서에서 특정 워크시트를 추출하여 중간 파일 처리 없이 Power BI 또는 Tableau로 CSV를 직접 전달합니다.
- **자동 송장 처리** – 송장 행이 포함된 워크시트를 CSV로 변환하여 회계 시스템에 빠르게 가져옵니다.
- **레거시 시스템 통합** – 구형 애플리케이션에서만 사용 가능한 구분 기호가 있는 텍스트 파일로 워크시트 데이터를 내보냅니다.
- **실시간 보고** – 웹 서비스에서 실시간 스프레드시트 데이터의 CSV 스냅샷을 생성하여 클라이언트 브라우저에 즉시 파일을 반환합니다.

## 왜 워크시트를 CSV로 변환 API를 사용해야 하나요?

- **영구 클라우드 스토리지가 필요 없음** – 파일은 변환 엔진으로 직접 스트리밍되고 변환 후 폐기되어 대역폭 및 스토리지 비용을 절약합니다.
- **고성능 클라우드 실행** – Aspose의 최적화된 서버에서 변환이 실행되며, 일반적으로 100MB 이하의 파일은 2초 이내에 완료됩니다.
- **세밀한 제어** – 단일 워크시트 선택, 사용자 정의 글꼴, 지역 포맷, 비밀번호 보호를 하나의 요청으로 적용합니다.
- **일관된 크로스 플랫폼 출력** – 동일한 REST 엔드포인트를 사용하는 .NET, Java, Python 등 다양한 SDK에서 동일한 CSV 출력을 보장합니다.

## SDK를 사용하여 워크시트를 CSV로 변환 API 사용하기

### 워크시트를 CSV로 변환 API 사양

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToCsv" target="_blank" rel="noopener noreferrer">워크시트를 CSV로 변환 API 사양</a>은 웹 브라우저에서 직접 REST 상호작용을 실행할 수 있는 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 인코딩됨)",
  "contentType": "MIME 유형",
  "fileDownloadName": "선택적 파일 이름"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 저수준 세부 사항을 추상화하여 개발을 간소화하고, 스프레드시트를 다른 스프레드시트로 병합하는 간결한 코드를 작성할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToCsv.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToCsv.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToCsv.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToCsv.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToCsv.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToCsv.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToCsv.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToCsv.go" >}}  
{{</tab>}}  
{{< /tabs >}}