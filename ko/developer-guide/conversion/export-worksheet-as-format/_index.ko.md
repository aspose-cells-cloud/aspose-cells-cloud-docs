---
title: "워크시트 내보내기 – Aspose.Cells Cloud API v4(PDF, PNG, SVG, CSV)"
second_title: "문서"
ArticleTitle: "원격 스프레드시트 워크시트를 다른 형식으로 내보내는 방법: 단계별 가이드"
linktype: "워크시트 내보내기"
type: docs
url: /ko/export-worksheet-as-format/
keywords: "Aspose Cells, 워크시트 내보내기, 클라우드 API, PDF, PNG, CSV, 엑셀 변환"
description: "Aspose.Cells Cloud에 저장된 워크시트를 단일 GET 요청을 통해 PDF, PNG, SVG, CSV 또는 기타 형식으로 변환합니다. C#, Java, Python 등 다양한 언어의 코드 예제를 포함합니다."
weight: 100
---

Aspose.Cells Cloud 웹 API를 사용하여 클라우드 스프레드시트/엑셀 워크시트를 다른 형식의 파일로 내보냅니다.

## **워크시트를 다른 형식으로 내보내기 API**

### 웹 API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수**

| 매개변수 이름       | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                     |
| :----------------- | :----- | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Path                       | (필수) 가져올 워크북 파일의 이름입니다.                                                                                                  |
| **worksheet**      | String | Path                       | (필수) 변환할 특정 워크시트입니다.                                                                                                       |
| **format**         | String | Query                      | (필수) 원하는 출력 형식입니다(예: `png`, `pdf`, `svg`).                                                                                  |
| **folder**         | String | Query                      | (선택 사항) 워크북이 저장된 폴더 경로입니다. 기본값은 `null`입니다.                                                                     |
| **storageName**    | String | Query                      | (선택 사항) 사용자 정의 클라우드 스토리지의 이름입니다. 생략 시 기본 스토리지를 사용합니다.                                               |
| **outPath**        | String | Query                      | (선택 사항) 출력 폴더 경로입니다. 기본값은 `null`입니다.                                                                                 |
| **outStorageName** | String | Query                      | (선택 사항) 출력 파일을 저장할 스토리지 이름입니다.                                                                                      |
| **fontsLocation**  | String | Query                      | (선택 사항) 필요 시 사용자 정의 폰트를 지정합니다.                                                                                        |
| **region**         | String | Query                      | (선택 사항) 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`)입니다. 숫자 서식, 날짜 파싱 및 로케일별 동작에 영향을 미칩니다.            |
| **password**       | String | Query                      | (선택 사항) 스프레드시트 파일에 접근하기 위한 비밀번호입니다.                                                                            |

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

| 코드 | 의미                | 설명                                                           |
| ---- | ------------------- | -------------------------------------------------------------- |
| 200  | OK(성공)            | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request(잘못된 요청) | 매개변수 누락 또는 잘못된 매개변수(예: 지원되지 않는 파일 형식)입니다.    |
| 401  | Unauthorized(인증되지 않음) | 잘못되거나 누락된 JWT 토큰입니다.                                     |
| 413  | Payload Too Large(페이로드 너무 큼) | 업로드한 파일이 크기 제한을 초과했습니다.                               |
| 500  | Internal Server Error(내부 서버 오류) | 예기치 않은 서버 오류입니다.                                          |

## **워크시트를 다른 형식으로 내보내기 API를 어디에 사용해야 하나요?**

- **레거시 시스템 마이그레이션** – 수천 개의 레거시 XLS 파일을 현대적인 시스템용 XLSX로 변환합니다.
- **아카이브 표준화** – 다양한 스프레드시트 형식(XLS, XLSM, ODS, CSV)을 아카이빙 목적으로 단일 형식으로 정규화합니다.
- **오피스 스위트 상호 운용성** – LibreOffice, Google Sheets, Apple Numbers와 호환되는 형식으로 엑셀 파일을 변환합니다.
- **데이터 소스 정규화** – 다양한 스프레드시트 형식을 CSV 또는 JSON으로 변환하여 데이터베이스에 로드합니다.
- **웹 게시** – 금융 모델을 HTML로 변환하여 웹에 표시합니다.

## **왜 워크시트를 다른 형식으로 내보내기 API를 사용해야 하나요?**

- **다언어 SDK 지원** – 여러 프로그래밍 언어에 대한 클라이언트 라이브러리를 제공하여 개발자가 선호하는 환경에서 직접 API를 호출할 수 있습니다.
- **중간 업로드 없이 직접 변환** – 클라우드 스토리지에 저장된 워크시트를 요청한 형식으로 변환할 때 파일을 다운로드 후 다시 업로드할 필요 없이 바로 변환할 수 있습니다.
- **데이터 전용 추출** – 시각적 스타일을 유지하지 않고 선택한 형식으로 워크시트 콘텐츠를 반환합니다.

## **SDK를 사용하여 스프레드시트 워크시트를 다른 형식으로 내보내기 API를 어떻게 사용하나요?**

### 워크시트를 다른 형식으로 내보내기 API 사양

[워크시트를 다른 형식으로 내보내기 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
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

SDK를 사용하면 저수준 세부 사항을 추상화하여 짧은 코드로 스프레드시트 워크시트를 형식 파일로 내보낼 수 있으므로 개발 속도가 가장 빠릅니다.  
Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}