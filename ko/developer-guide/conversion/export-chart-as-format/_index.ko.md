---
title: "엑셀 차트 내보내기 – Aspose.Cells Cloud API"
second_title: "문서"
description: "클라우드에 저장된 엑셀 워크북의 차트를 단일 REST 요청으로 PDF, PNG, SVG 등 다른 형식으로 변환합니다."
ArticleTitle: "로컬 스프레드시트 워크시트를 PDF 파일로 변환하는 방법: 단계별 가이드"
linktitle: "워크시트를 PDF로 변환"
type: docs
url: /ko/export-chart-as-format/
keywords: "Aspose.Cells Cloud, 차트 내보내기, API, PDF, PNG, SVG, 엑셀, REST, 클라우드 변환"
weight: 100
---

Aspose Cloud 스토리지에 저장된 워크북에 있는 차트를 다운로드 없이 다른 파일 형식(PDF, PNG, SVG 등)으로 변환합니다.

## ExportChartAsFormat API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 📦 요청 매개변수

| 이름               | 유형    | 위치   | 필수 여부 | 설명                                                      |
| ------------------ | ------- | ------ | --------- | --------------------------------------------------------- |
| **name**           | 문자열  | 경로   | 예        | 워크북 파일 이름.                                         |
| **worksheet**      | 문자열  | 경로   | 예        | 차트가 포함된 워크시트 이름.                              |
| **chartIndex**     | 정수    | 경로   | 예        | 내보낼 차트의 0부터 시작하는 인덱스.                      |
| **format**         | 문자열  | 쿼리   | 예        | 원하는 출력 형식(예: `png`, `pdf`, `svg`).               |
| **folder**         | 문자열  | 쿼리   | 아니요    | 워크북이 저장된 폴더 경로(기본값: 루트).                  |
| **storageName**    | 문자열  | 쿼리   | 아니요    | 사용자 지정 스토리지 이름; 생략 시 기본 스토리지 사용.    |
| **outPath**        | 문자열  | 쿼리   | 아니요    | 변환된 파일이 저장될 폴더 경로.                           |
| **outStorageName** | 문자열  | 쿼리   | 아니요    | 출력 파일을 저장할 스토리지 이름.                         |
| **fontsLocation**  | 문자열  | 쿼리   | 아니요    | 사용자 지정 폰트가 포함된 폴더 경로.                      |
| **region**         | 문자열  | 쿼리   | 아니요    | 로케일 설정(예: `en-US`, `fr-FR`).                        |
| **password**       | 문자열  | 쿼리   | 아니요    | 보호된 워크북을 열기 위한 비밀번호.                       |

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

| 코드 | 의미                  | 설명                                                           |
| ---- | --------------------- | -------------------------------------------------------------- |
| 200  | OK (성공)             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.         |
| 400  | 잘못된 요청           | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | 인증되지 않음         | 잘못되거나 누락된 JWT 토큰.                                    |
| 413  | 요청 본문이 너무 큼   | 업로드된 파일이 크기 제한을 초과함.                            |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류.                                         |

## SDK를 사용하여 Export Chart as Format API를 어떻게 활용하나요?

### Export Chart as Format API 사양

[Export Chart as Format API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 제공하며, 웹 브라우저에서 직접 REST 상호작용을 가능하게 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 아래 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
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

SDK를 사용하면 저수준 세부 정보를 추상화하여 최소한의 코드로 스프레드시트 테이블 데이터를 PDF 파일로 변환할 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

---