---
title: "표 내보내기 – Aspose.Cells Cloud API | Excel을 PDF, PNG, CSV로 변환"
second_title: "문서"
ArticleTitle: "원격 스프레드시트 표를 다른 형식으로 내보내는 방법: 단계별 가이드"
linktitle: "표를 지정된 형식으로 내보내기"
type: docs
url: /ko/export-table-as-format/
keywords: "Aspose.Cells, 표 내보내기, Excel을 PDF로, 클라우드 API, REST"
description: "Aspose.Cells Cloud API를 사용하여 원격 Excel 표를 PDF, PNG, CSV, JSON 또는 기타 형식으로 내보냅니다. JWT 인증이 필요한 안전한 HTTPS 엔드포인트 및 SDK 예제 제공."
weight: 100
---

클라우드에 저장된 스프레드시트(Excel) 표를 다른 형식의 파일로 내보냅니다.

## **표를 다른 형식으로 내보내기 API**

### 웹 API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                             |
| :------------ | :----- | :------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | String | Path                       | **필수.** 가져올 워크북 파일의 이름입니다.                                                                                                        |
| worksheet     | String | Path                       | 워크시트 이름입니다.                                                                                                                              |
| tableName     | String | Path                       | 표의 이름입니다.                                                                                                                                  |
| format        | String | Query                      | **필수.** 원하는 출력 형식입니다(예: “png”, “pdf”, “svg”).                                                                                         |
| folder        | String | Query                      | 선택 사항. 워크북이 저장된 폴더 경로입니다. 기본값은 `null`입니다.                                                                                 |
| storageName   | String | Query                      | 선택 사항. 사용자 정의 클라우드 스토리지를 사용할 경우 스토리지 이름입니다. 생략 시 기본 스토리지를 사용합니다.                                          |
| outPath       | String | Query                      | 선택 사항. 출력 파일을 저장할 폴더 경로입니다. 기본값은 `null`입니다.                                                                              |
| outStorageName| String | Query                      | 선택 사항. 출력 파일을 저장할 스토리지 이름입니다.                                                                                                |
| fontsLocation | String | Query                      | 선택 사항. 사용자 정의 글꼴이 위치한 경로입니다.                                                                                                   |
| region        | String | Query                      | 선택 사항. 스프레드시트의 지역/언어 설정(예: `en-US`, `fr-FR`)입니다. 숫자 서식, 날짜 파싱 및 지역별 동작에 영향을 미칩니다.                           |
| password      | String | Query                      | 선택 사항. 스프레드시트 파일을 열기 위한 비밀번호입니다.                                                                                           |

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

| 코드 | 의미                  | 설명                                                                |
| ---- | --------------------- | ------------------------------------------------------------------- |
| 200  | OK                    | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함되어 있습니다. |
| 400  | Bad Request           | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)입니다.         |
| 401  | Unauthorized          | 잘못되었거나 누락된 JWT 토큰입니다.                                   |
| 413  | Payload Too Large     | 업로드된 파일이 크기 제한을 초과했습니다.                             |
| 500  | Internal Server Error | 예기치 않은 서버 오류입니다.                                          |

## **표를 다른 형식으로 내보내기 API는 어디에 사용해야 하나요?**

- **레거시 시스템 마이그레이션**: 최신 시스템을 위해 수천 개의 레거시 XLS 파일을 XLSX로 변환합니다.
- **아카이브 표준화**: XLS, XLSM, ODS, CSV 등 다양한 스프레드시트 형식을 아카이빙을 위해 단일 형식으로 정규화합니다.
- **오피스 스위트 상호 운용성**: LibreOffice, Google 시트, Apple Numbers와 호환되는 형식으로 Excel 파일을 변환합니다.
- **데이터 소스 정규화**: 데이터베이스 인서트를 위해 다양한 스프레드시트 형식을 CSV 또는 JSON으로 변환합니다.
- **웹 게시**: 재무 모델을 HTML로 변환하여 웹에 표시합니다.

## **왜 표를 다른 형식으로 내보내기 API를 사용해야 하나까요?**

- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어의 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 포괄적인 문서도 함께 제공됩니다. 사용자 정의 차트 렌더링 솔루션을 구축하는 것에 비해 개발 작업량을 크게 줄여줍니다.
- **인건비 절감**: 문서 통합을 위한 전용 인력을 배치할 필요가 줄어듭니다.
- **사용량 과금**: 초기 투자가 필요 없으며, 실제로 사용한 API 호출에 대해서만 비용을 지불합니다.
- **유지보수 비용 없음**: 서버 유지보수, 소프트웨어 업데이트, 호환성 문제 해결이 필요 없습니다.
- **API는 워크북 서식 없이 순수한 표 데이터만 반환합니다.**

## **SDK를 사용하여 스프레드시트 표를 다른 형식으로 내보내기 API를 사용하는 방법은?**

### 표를 다른 형식으로 내보내기 API 사양

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">표를 다른 형식으로 내보내기 API 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API로 요청을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
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

SDK를 사용하면 저수준 세부 사항을 추상화해 짧은 코드로 스프레드시트 표를 지정된 형식 파일로 내보낼 수 있으므로, 개발 속도가 가장 빠릅니다. 전체 Aspose.Cells Cloud SDK 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스로 요청을 수행하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}