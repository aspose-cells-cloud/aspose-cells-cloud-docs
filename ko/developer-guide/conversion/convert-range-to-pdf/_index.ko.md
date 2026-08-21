---
title: "Aspose.Cells Cloud API를 사용하여 Excel 범위를 PDF로 변환"
second_title: "문서"
ArticleTitle: "로컬 스프레드시트 범위 데이터를 PDF 파일로 변환하는 방법: 단계별 가이드"
linktitle: "범위를 PDF로 변환"
type: docs
url: /ko/convert-range-to-pdf/
keywords: "Aspose.Cells Cloud, Excel 범위를 PDF로 변환, Excel을 PDF로, 클라우드 변환"
description: "로컬 Excel 스프레드시트에서 특정 범위를 Aspose.Cells Cloud의 REST API를 사용하여 PDF로 변환합니다."
weight: 100
---

Cloud API를 사용하여 로컬 Excel 파일의 데이터 범위를 [PDF](https://docs.fileformat.com/pdf/) 파일로 내보냅니다.

**필수 조건**: 이 API를 사용하려면 유효한 Aspose.Cells Cloud 계정, JWT 액세스 토큰, 그리고 필요에 따라 사용 중인 프로그래밍 언어에 맞는 Aspose.Cells Cloud SDK가 필요합니다. `outStorageName` 매개변수를 사용하려는 경우, 대상 저장소(기본 또는 사용자 정의)가 구성되어 있어야 합니다.

## **범위를 PDF로 변환 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                      |
| ------------- | ------ | -------------------------- | ------------------------------------------------------------------------- |
| Spreadsheet   | 파일   | FormData                   | 스프레드시트 파일을 업로드합니다.                                         |
| worksheet     | 문자열 | 쿼리                       | 스프레드시트 내 워크시트 이름입니다.                                      |
| range         | 문자열 | 쿼리                       | 변환할 셀 영역(예: A1:C10)입니다.                                        |
| outPath       | 문자열 | 쿼리                       | (선택 사항) 워크북이 저장된 폴더 경로입니다. 기본값은 null입니다.       |
| outStorageName| 문자열 | 쿼리                       | 출력 파일을 저장할 저장소 이름입니다.                                     |
| fontsLocation | 문자열 | 쿼리                       | 사용자 정의 글꼴을 저장할 위치(홈 사용용)입니다.                         |
| region        | 문자열 | 쿼리                       | 스프레드시트 지역 설정입니다.                                              |
| password      | 문자열 | 쿼리                       | 스프레드시트 파일을 열기 위한 암호입니다.                                 |

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

_일반적인 응답은 다운로드 파일로 반환되는 이진 PDF 스트림입니다._

**HTTP 상태 코드**

| 코드 | 의미                | 설명                                                          |
| ---- | ------------------- | ------------------------------------------------------------- |
| 200  | 성공(OK)            | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청(Bad Request) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)입니다.     |
| 401  | 인증되지 않음(Unauthorized) | 잘못되거나 누락된 JWT 토큰입니다.                               |
| 413  | 페이로드가 너무 큼(Payload Too Large) | 업로드된 파일이 크기 제한을 초과합니다.                         |
| 500  | 내부 서버 오류(Internal Server Error) | 예기치 않은 서버 오류입니다.                                     |

## **어디에서 Convert Range to PDF API를 사용해야 하나요?**

- **재무 제표**: 대차대조표, 손계산서(특정 범위)를 감사 준비 문서로 PDF로 변환합니다.
- **판매 보고서**: 대시보드 또는 수수료 계산 결과를 배포 가능한 PDF로 변환합니다.
- **운영 지표**: 핵심 성과 지표(KPI) 테이블 및 성과 지표를 공식 PDF 보고서로 내보냅니다.
- **계약 데이터**: 스프레드시트에서 가격 테이블 및 서비스 수준 계약(SLA)을 PDF 첨부 파일로 내보냅니다.
- **감사 추적 기록**: 재무 데이터 범위를 수정 불가능한 PDF 증거로 보존합니다.
- **포트폴리오 요약**: 투자 성과 범위를 고객용 PDF 보고서로 내보냅니다.
- **품질 관리 보고서**: 검사 데이터 범위를 준수 기록용 PDF로 내보냅니다.
- **재고 요약**: 재고 수준 테이블을 경영진 검토용 PDF로 변환합니다.

## **왜 Convert Range to PDF API를 사용해야 하나요?**

- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하여 빠른 개발과 포괄적인 문서화를 지원합니다. 사용자 정의 차트 렌더링 솔루션을 구축하는 것에 비해 개발 작업량을 크게 줄여줍니다.
- **비용 효율적**: 전체 워크북을 먼저 업로드하지 않고도 범위 데이터만 변환할 수 있어 저장 공간을 절약하고 비용을 줄입니다.
- **복잡한 Excel 서식 보존**: 범용적으로 접근 가능한 PDF 형식으로 복잡한 Excel 서식을 그대로 유지합니다.

## **SDK와 함께 Convert Range to PDF API를 사용하는 방법**

### Convert Range to PDF API 사양

[Convert Range to PDF API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 사항을 추상화하여 간결한 코드로 데이터 범위를 PDF 파일로 변환할 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}