---
title: "Aspose.Cells Cloud 웹 API - 원격 엑셀 워크시트를 다른 형식으로 내보내는 무료 온라인 도구"
second_title: "문서"
ArticleTitle: "원격 스프레드시트 워크시트를 다른 형식으로 내보내는 방법: 단계별 가이드"
linktype: "Export Spreadsheet as Format"
type: docs
url: /export-spreadsheet-as-format/
keywords: "Aspose.Cells, 스프레드시트 변환, API, 내보내기, PDF, CSV, JSON, XLSX"
description: "Aspose Cloud에 저장된 엑셀 워크북을 단일 REST 엔드포인트를 통해 PDF, XLSX, CSV, JSON 또는 HTML로 변환하세요. 요청 구문, 매개변수를 배우고 C#, Java, Python 등 여러 언어의 SDK 예제를 확인하세요."
weight: 100
---

클라우드 스프레드시트(Excel)를 다른 파일 형식으로 내보내기.

## **스프레드시트를 다른 형식으로 내보내기 API**

### 웹 API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름   | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                               |
| :------------- | :----- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                        | (필수) 가져올 워크북 파일의 이름.                                                                                                                  |
| format         | String | Query                       | (필수) 원하는 출력 형식(예: "Xlsx", "PDF", "CSV").                                                                                                 |
| folder         | String | Query                       | (선택 사항) 워크북이 저장된 폴더 경로. 기본값은 null입니다.                                                                                        |
| storageName    | String | Query                       | (선택 사항) 사용자 정의 클라우드 스토리지를 사용할 경우 스토리지 이름. 생략 시 기본 스토리지를 사용합니다.                                            |
| outPath        | String | Query                       | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다.                                                                                         |
| outStorageName | String | Query                       | (선택 사항) 출력 파일의 스토리지 이름.                                                                                                             |
| fontsLocation  | String | Query                       | (선택 사항) 사용자 정의 글꼴 위치.                                                                                                                 |
| region         | String | Query                       | (선택 사항) 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 지역별 동작에 영향을 미칩니다.                               |
| password       | String | Query                       | (선택 사항) 스프레드시트 파일을 열기 위한 비밀번호.                                                                                                |

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

응답은 변환된 파일 스트림을 나타내는 단일 객체를 포함합니다.

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                              |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.             |
| 400  | Bad Request           | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).         |
| 401  | Unauthorized          | 잘못되었거나 누락된 JWT 토큰.                                      |
| 413  | Payload Too Large     | 업로드된 파일이 크기 제한을 초과함.                                |
| 500  | Internal Server Error | 예기치 않은 서버 오류.                                             |

## 스프레드시트를 다른 형식으로 내보내기 API는 어디에 사용해야 하나요?

- **레거시 시스템 마이그레이션**: 수천 개의 레거시 XLS 파일을 최신 시스템용 XLSX로 변환.
- **아카이브 표준화**: XLS, XLSM, ODS, CSV 등 다양한 스프레드시트 형식을 단일 형식으로 정규화하여 보관.
- **오피스 스위트 상호 운용성**: 엑셀 파일을 LibreOffice, 구글 시트, 애플 넘버스와 호환되는 형식으로 변환.
- **데이터 소스 정규화**: 데이터베이스 인GEST를 위해 다양한 스프레드시트 형식을 CSV 또는 JSON으로 변환.
- **웹 게시**: 금융 모델을 웹 표시용 HTML로 변환.

## 왜 스프레드시트를 다른 형식으로 내보내기 API를 사용해야 하나요?

- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 포괄적인 문서도 제공합니다. 사용자 정의 차트 렌더링 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **인건비 절감**: 문서 통합을 위한 전담 인력을 배치할 필요가 줄어듭니다.
- **사용량 과금**: 초기 투자가 필요 없으며, 실제로 사용한 API 호출만 요금이 부과됩니다.
- **서버 측 유지보수 불필요**: 서버 유지보수, 소프트웨어 업데이트, 호환성 문제 해결이 필요 없습니다.
- **포괄적인 형식 지원**: 20개 이상의 스프레드시트 형식 간 변환 가능.
- **데이터 무결성 및 서식 유지**: 변환 시 원래 레이아웃, 수식 및 스타일을 유지합니다.

## SDK를 사용하여 스프레드시트를 다른 형식으로 내보내기 API를 어떻게 사용하나요?

### 스프레드시트를 다른 형식으로 내보내기 API 사양

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat" rel="noopener noreferrer">스프레드시트를 다른 형식으로 내보내기 API 사양</a>은 REST 상호 작용을 원활하게 수행할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

SDK를 사용하면 저수준 세부 정보를 추상화하여 짧은 코드로 스프레드시트를 형식 파일로 내보낼 수 있으므로 개발 속도가 가장 빠릅니다.  
API를 호출하기 전에 OAuth 2.0 액세스 토큰을 받아 `Authorization: Bearer <token>` 헤더에 포함시켜야 합니다.

Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 통해 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
---