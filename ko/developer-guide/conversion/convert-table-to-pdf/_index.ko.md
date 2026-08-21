---
title: "Aspose.Cells Cloud 웹 API - 로컬 엑셀 테이블 데이터를 PDF 파일로 변환 - 무료 온라인 도구"
second_title: "문서"
ArticleTitle: "로컬 스프레드시트 테이블 데이터를 PDF 파일로 변환하는 방법: 단계별 가이드"
linktitle: "테이블을 PDF로 변환"
type: docs
url: /ko/convert-table-to-pdf/
keywords: "Aspose.Cells, 엑셀을 PDF로, 테이블 변환, 클라우드 API"
description: "Aspose.Cells Cloud REST API를 사용하여 로컬 엑셀 테이블을 빠르게 PDF 파일로 변환합니다."
weight: 100
---

클라우드 API를 사용하여 로컬 엑셀 파일의 테이블 데이터를 PDF 파일로 내보냅니다.

## **테이블을 PDF로 변환 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름   | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                   |
| :------------- | :----- | :------------------------- | :-------------------------------------------------------------------------------------- |
| Spreadsheet    | 파일   | FormData                   | 변환할 스프레드시트 파일을 업로드합니다.                                                 |
| worksheet      | 문자열 | 쿼리                       | 스프레드시트의 워크시트 이름입니다.                                                      |
| tableName      | 문자열 | 쿼리                       | 변환할 테이블의 이름입니다.                                                             |
| outPath        | 문자열 | 쿼리                       | (선택 사항) 변환된 PDF가 저장될 폴더 경로입니다. 기본값은 null입니다.                     |
| outStorageName | 문자열 | 쿼리                       | 출력 파일 저장소의 이름을 지정합니다.                                                   |
| fontsLocation  | 문자열 | 쿼리                       | PDF에 사용자 정의 글꼴을 사용합니다.                                                     |
| region         | 문자열 | 쿼리                       | 스프레드시트의 지역 설정을 지정합니다.                                                   |
| password       | 문자열 | 쿼리                       | 스프레드시트 파일에 액세스하기 위한 비밀번호입니다.                                       |

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

**샘플 응답 헤더**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                              |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | 성공 (OK)             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨.          |
| 400  | 잘못된 요청 (Bad Request) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형).           |
| 401  | 인증되지 않음 (Unauthorized) | 잘못되거나 누락된 JWT 토큰.                                        |
| 413  | 페이로드가 너무 큼 (Payload Too Large) | 업로드한 파일이 크기 제한을 초과함.                               |
| 500  | 내부 서버 오류 (Internal Server Error) | 예기치 않은 서버 오류.                                            |

## **어디에서 테이블을 PDF로 변환 API를 사용해야 하나요?**

- **재무 제표**: 재무상태표, 손익계산서(특정 테이블)를 감사 준비 문서로 PDF로 변환합니다.
- **판매 보고서**: 판매 대시보드 또는 수수료 계산을 배포 가능한 PDF로 변환합니다.
- **운영 지표**: KPI 테이블 및 성과 지표를 공식 PDF 보고서로 내보냅니다.
- **계약 데이터**: 스프레드시트에서 가격 테이블 및 서비스 수준 계약을 PDF 첨부 파일로 내보냅니다.
- **감사 추적 이력**: 재무 데이터 테이블을 수정 불가능한 PDF 증거로 보존합니다.
- **포트폴리오 요약**: 투자 성과 테이블을 고객용 PDF 보고서로 내보냅니다.
- **품질 관리 보고서**: 검사 데이터 테이블을 준수 기록용 PDF로 내보냅니다.
- **재고 요약**: 재고 수준 테이블을 경영진 검토용 PDF로 변환합니다.

## **왜 테이블을 PDF로 변환 API를 사용해야 하나요?**

- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 포괄적인 문서를 제공합니다. 사용자 정의 차트 렌더링 솔루션을 구축하는 것에 비해 개발 작업량을 크게 줄여줍니다.
- **비용 효율적**: 워크북을 먼저 업로드하지 않고도 테이블 데이터를 변환할 수 있어 저장 공간을 절약하고 비용을 줄입니다.
- **복잡한 엑셀 서식 보존**: 보편적으로 접근 가능한 PDF 형식으로 복잡한 엑셀 서식을 그대로 유지합니다.

## **SDK와 함께 테이블을 PDF로 변환 API를 사용하는 방법은?**

### 테이블을 PDF로 변환 API 사양

[테이블을 PDF로 변환 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF)은 웹 브라우저에서 직접 REST 상호 작용을 실행할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.
cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
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

SDK를 사용하면 저수준 세부 사항을 추상화하여 최소한의 코드로 스프레드시트 테이블 데이터를 PDF 파일로 변환할 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}