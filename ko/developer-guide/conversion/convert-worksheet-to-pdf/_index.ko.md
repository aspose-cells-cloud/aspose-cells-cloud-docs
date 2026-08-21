---
title: "Aspose.Cells Cloud Web API – 로컬 Excel 워크시트를 PDF 파일로 변환 – 무료 온라인 도구"
second_title: "문서"
ArticleTitle: "로컬 스프레드시트 워크시트를 PDF 파일로 변환하는 방법: 단계별 가이드"
linktitle: "워크시트를 PDF로 변환"
type: docs
url: /ko/convert-worksheet-to-pdf/
keywords: "Aspose.Cells, Excel to PDF, 워크시트 변환, REST API, 클라우드 변환, 스프레드시트 PDF, API 엔드포인트, PDF 생성"
description: "Aspose.Cells Cloud API를 사용하여 로컬 Excel 파일의 워크시트를 빠르고 안전하게 PDF 문서로 변환합니다."
weight: 100
---

클라우드 API를 사용하여 로컬 Excel 파일의 워크시트를 [PDF](https://docs.fileformat.com/pdf/) 파일로 내보냅니다.

## **워크시트를 PDF로 변환하는 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                 |
| ------------- | ------ | -------------------------- | ------------------------------------------------------------------- |
| Spreadsheet   | 파일   | FormData                   | 스프레드시트 파일을 업로드합니다.                                   |
| worksheet     | 문자열 | 쿼리                       | 스프레드시트 내 워크시트의 이름입니다.                              |
| outPath       | 문자열 | 쿼리                       | (선택 사항) 워크북을 저장할 폴더 경로; 기본값은 null입니다.         |
| outStorageName| 문자열 | 쿼리                       | 출력 파일의 저장소 이름입니다.                                      |
| fontsLocation | 문자열 | 쿼리                       | PDF 생성 시 사용자 정의 글꼴을 사용합니다.                          |
| region        | 문자열 | 쿼리                       | 스프레드시트의 지역 설정을 정의합니다.                              |
| password      | 문자열 | 쿼리                       | 스프레드시트 파일을 열기 위해 필요한 비밀번호입니다.                |

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

| 코드 | 의미                  | 설명                                                       |
| ---- | --------------------- | ---------------------------------------------------------- |
| 200  | OK (성공)             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.     |
| 400  | Bad Request (잘못된 요청) | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰.                                |
| 413  | Payload Too Large (과도한 페이로드 크기) | 업로드한 파일이 크기 제한을 초과함.                        |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류.                                      |

## **워크시트를 PDF로 변환하는 API를 어디에 사용해야 하나요?**

- **재무 제표**: 대차대조표, 손익계산서(특정 표)를 감사 준비 문서로 PDF로 변환합니다.
- **판매 보고서**: 판매 대시보드 또는 수수료 계산 결과를 배포 가능한 PDF로 변환합니다.
- **운영 지표**: 핵심 성과 지표(KPI) 테이블 및 성과 지표를 공식 PDF 보고서로 내보냅니다.
- **계약 데이터**: 스프레드시트에서 가격표 및 서비스 수준 계약(SLA)을 PDF 첨부 파일로 내보냅니다.
- **감사 추적 이력**: 재무 워크시트를 편집 불가능한 PDF 증거로 보존합니다.
- **포트폴리오 요약**: 투자 성과 테이블을 고객용 PDF 보고서로 내보냅니다.
- **품질 관리 보고서**: 검사 워크시트를 준수 기록을 위해 PDF로 내보냅니다.
- **재고 요약**: 재고 워크시트를 관리자 검토용 PDF로 변환합니다.

## **왜 워크시트를 PDF로 변환하는 API를 사용해야 하나요?**

- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하여 빠른 개발이 가능하며, 포괄적인 문서도 제공됩니다. 사용자 정의 차트 렌더링 솔루션을 구축하는 것에 비해 개발 작업량을 크게 줄여줍니다.
- **비용 효율적**: 워크북을 먼저 업로드하지 않고도 테이블 데이터를 변환할 수 있어 저장 공간을 절약하고 비용을 줄입니다.
- **서식 보존**: 복잡한 Excel 서식을 보존한 채 보편적으로 접근 가능한 PDF 형식으로 유지합니다.

## **SDK를 사용하여 워크시트를 PDF로 변환하는 API를 어떻게 사용하나요?**

### 워크시트를 PDF로 변환하는 API 사양

[워크시트를 PDF로 변환하는 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공하며, 웹 브라우저에서 직접 REST 상호작용을 가능하게 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용해 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

SDK를 사용하면 저수준 세부 사항을 추상화해 최소한의 코드로 스프레드시트 테이블 데이터를 PDF 파일로 변환할 수 있어 가장 빠른 개발 방식입니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}