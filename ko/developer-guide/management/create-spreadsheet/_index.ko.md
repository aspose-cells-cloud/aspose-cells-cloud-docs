---
title: "스프레드시트 API 생성 – Aspose.Cells Cloud(v5.0) | Excel 파일 생성"
second_title: "문서"
ArticleTitle: "새 Excel 스프레드시트 생성 방법 – 빈 파일 또는 템플릿 기반 파일 생성"
linktype: "스프레드시트 생성"
type: docs
url: /ko/create-spreadsheet/
keywords: "Aspose.Cells, 스프레드시트 API, Excel 생성, 클라우드, XLSX, ODS, CSV, 템플릿, SDK, 자동화"
description: "Aspose.Cells Cloud API(v5.0)를 사용해 빈 Excel 워크북 또는 템플릿 기반 파일을 생성하는 방법을 알아보세요. 엔드포인트, 매개변수, 오류 코드, 인증 단계, SDK 예제를 포함합니다."
weight: 100
---

Aspose.Cells Cloud API를 사용해 프로그래밍 방식으로 새 Excel 스프레드시트를 생성합니다. 빈 워크북을 생성하거나 사용자 정의 템플릿에서 파일을 인스턴스화할 수 있습니다. 이 RESTful API는 자동화된 Excel 파일 생성을 지원하며, 보고서 생성, 문서 자동화, 데이터 처리 워크플로우에 이상적입니다.

## **스프레드시트 API 생성**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름       | 유형   | 위치   | 설명                                                                                                                                            |
| ------------------- | ------ | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**          | String | Query  | **필수**. 새 스프레드시트의 파일 형식(예: `XLSX`, `XLS`, `ODS`, `CSV`).                                                                         |
| **template**        | String | Query  | **선택 사항**. 클라우드 저장소에 저장된 템플릿 파일 이름(예: `invoice_template.xlsx`). 생략 시 빈 워크북이 생성됩니다.                           |
| **outPath**         | String | Query  | **선택 사항**. 생성된 파일을 저장할 클라우드 저장소의 대상 폴더 경로. `null` 또는 생략 시 기본 위치에 스프레드시트가 저장됩니다.                 |
| **outStorageName**  | String | Query  | **필수**. 구성된 클라우드 저장소의 식별자(예: `MyDrive`).                                                                                       |
| **region**          | String | Query  | **선택 사항**. 기본 날짜, 숫자 및 통화 형식을 결정하는 로케일 설정(예: `fr-FR`).                                                               |
| **password**        | String | Query  | **선택 사항**. 암호화된 템플릿 파일의 비밀번호. 템플릿이 보호되지 않은 경우 비워 둡니다.                                                         |

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

| 코드 | 의미                 | 설명                                                            |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK(성공)             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.           |
| 400  | Bad Request(잘못된 요청) | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식).   |
| 401  | Unauthorized(인증되지 않음) | 유효하지 않거나 누락된 JWT 토큰.                               |
| 413  | Payload Too Large(ペイロードが大きすぎます) | 업로드된 파일이 크기 제한을 초과함.                             |
| 500  | Internal Server Error(내부 서버 오류) | 예기치 않은 서버 오류.                                          |

## 스프레드시트 생성 API는 어디에 사용해야 하나요?

- **자동 보고 시스템 초기화** – 매일/매주 자동화 사이클 시작 시 표준 템플릿에서 보고서 파일을 생성하거나 빈 워크북을 만듭니다.
- **사용자 자체 서비스 포털** – 고객이 템플릿(견적서, 프로젝트 일정 등)을 선택하고 즉시 맞춤형 Excel 파일을 다운로드할 수 있도록 합니다.
- **일괄 데이터 내보내기 및 배포** – 내보낸 각 데이터 세트에 대해 동일한 형식의 별도 워크북을 생성하여 후속 배포 및 처리를 간소화합니다.

워크시트 추가 또는 셀 채우기 등 후속 작업은 **워크시트 추가 API**, **셀 업데이트 API**, **워크북 내보내기 API**를 참조하세요.

## 왜 스프레드시트 생성 API를 사용해야 하나요?

- **개발자 친화적** – 다양한 언어용 SDK 라이브러리와 광범위한 문서를 제공하여 맞춤형 솔루션 구축보다 통합이 간편합니다.
- **노력 효율성 향상** – 문서 통합 작업을 자동화하여 수동 작업을 줄입니다.
- **사용량 기준 요금제** – 선불 라이선스 비용 없이 API 사용량에 따라 요금이 부과됩니다.
- **관리형 서비스** – API는 완전히 호스팅되며, 온프레미스 서버 유지보수 또는 소프트웨어 업데이트가 필요 없습니다.

## SDK를 사용한 스프레드시트 생성 API 사용 방법

### 스프레드시트 생성 API 사양

[스프레드시트 생성 API 사양](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 가능하게 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API에 호출을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MyStorage" \
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

SDK를 사용하면 저수준 세부 사항을 추상화하여 간결한 코드로 스프레드시트를 빌드할 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}