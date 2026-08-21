---
title: "Aspose.Cells Cloud Web API - 스프레드시트 테이블 데이터를 CSV 파일로 변환 - 무료 온라인 도구"
second_title: "문서"
ArticleTitle: "스프레드시트 테이블 데이터를 CSV 파일로 변환하는 방법: 단계별 가이드"
linktype: "docs"
url: /ko/convert-table-to-csv/
keywords: "Aspose.Cells Cloud, 테이블을 CSV로, 스프레드시트 변환, Excel을 CSV로, API, REST, 데이터 내보내기"
description: "Aspose.Cells Cloud API를 사용하여 Excel 스프레드시트의 테이블을 빠르게 CSV 파일로 변환합니다."
weight: 100
---

Cloud API를 사용하여 로컬 Excel 파일에서 테이블 데이터를 CSV 파일로 내보냅니다.

## **테이블을 CSV로 변환 API**

### 웹 API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                             |
| ------------- | ------ | ------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | 파일   | FormData                  | 스프레드시트 파일을 업로드합니다.                                                                                               |
| worksheet     | 문자열 | 쿼리                      | 스프레드시트 내 워크시트의 이름입니다.                                                                                          |
| tableName     | 문자열 | 쿼리                      | 변환할 테이블의 이름입니다.                                                                                                     |
| outPath       | 문자열 | 쿼리                      | (선택 사항) 워크북이 저장된 폴더 경로이며, 기본값은 null입니다.                                                                |
| outStorageName| 문자열 | 쿼리                      | 출력 파일을 저장할 스토리지 이름입니다.                                                                                         |
| fontsLocation | 문자열 | 쿼리                      | 사용자 정의 글꼴을 사용할 경로입니다.                                                                                           |
| region        | 문자열 | 쿼리                      | 스프레드시트의 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱, 지역별 동작에 영향을 미칩니다.                       |
| password      | 문자열 | 쿼리                      | 스프레드시트 파일을 열기 위한 비밀번호입니다.                                                                                   |

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

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                             |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK(성공)              | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨.       |
| 400  | 잘못된 요청           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).         |
| 401  | 인증되지 않음         | 잘못되거나 누락된 JWT 토큰.                                       |
| 413  | 페이로드가 너무 큼    | 업로드된 파일이 크기 제한을 초과함.                               |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류.                                            |

## **테이블을 CSV로 변환 API를 어디에 사용해야 하나요?**

- **데이터베이스 마이그레이션**: Excel 테이블을 CSV로 변환하여 SQL 데이터베이스(MySQL, PostgreSQL, SQL Server)에 일괄 가져오기.
- **데이터 웨어하우스 로딩**: Excel 기반 보고서 테이블을 CSV로 변환하여 Snowflake, Redshift, BigQuery 등에 로딩.
- **일괄 API 페이로드**: Excel 테이블 데이터를 CSV로 변환하여 REST 서비스로 일괄 업로드.
- **서비스 간 통신**: 마이크로서비스 간에 가볍고 범용적인 데이터 교환 형식으로 CSV 사용.
- **머신러닝 데이터 준비**: Python/R 머신러닝 라이브러리에 사용하기 위해 Excel에서 기능 테이블을 CSV로 변환.
- **통계 분석**: SPSS, SAS, Stata 등에 가져오기 위해 연구 데이터 테이블을 CSV로 변환.
- **콘텐츠 마이그레이션**: 구조화된 콘텐츠를 CSV経由で Excel에서 CMS 시스템으로 이전.

## 왜 테이블을 CSV로 변환 API를 사용해야 하나요?

- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어의 SDK 라이브러리를 제공해 빠른 개발을 가능하게 하며, 체계적인 문서도 제공합니다. 자체 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **비용 효율적**: 워크북을 먼저 업로드하지 않고도 테이블 데이터를 변환할 수 있어 저장 공간을 절약하고 비용을 줄입니다.
- **서식 없이 순수 데이터 추출**.
- **CSV는 거의 모든 시스템에서 지원됩니다**:
  - 데이터베이스(모든 주요 RDBMS)
  - 프로그래밍 언어(모두 기본 파서 지원)
  - 비즈니스 인텔리전스 도구(Tableau, Power BI, Looker)
  - 스프레드시트 소프트웨어(Excel, Google Sheets, LibreOffice)
  - 명령줄 도구(awk, sed, grep)

## SDK를 사용해 테이블을 CSV로 변환 API를 어떻게 사용하나요?

### 테이블을 CSV로 변환 API 사양

[테이블을 CSV로 변환 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공해 웹 브라우저에서 직접 REST 상호작용이 가능합니다.
cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용해 Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
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

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 사항을 추상화해 최소한의 코드로 스프레드시트 테이블 데이터를 CSV 파일로 변환할 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예시는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}