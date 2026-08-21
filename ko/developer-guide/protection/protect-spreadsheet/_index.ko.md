---
title: "Aspose.Cells Cloud Excel 암호 보호 웹 API – 열기 및 수정 암호 암호화 자동화"
second_title: "Excel 보호 개발자 가이드"
ArticleTitle: "Excel 암호 보호 도구 – 열기 및 수정 암호 설정 – 스프레드시트 보안 강화"
linktype: "protect-spreadsheet"
type: docs
url: /ko/protect-spreadsheet/
keywords: "Aspose.Cells, Excel 암호 보호, API, 열기 암호, 수정 암호, 클라우드 스토리지, 스프레드시트 보안"
description: "Aspose.Cells Cloud을 사용하여 프로그래밍 방식으로 Excel 파일을 보호하세요. 단일 API 호출로 열기 및 수정 암호를 모두 설정합니다. .xlsx, .xls 및 클라우드 스토리지를 지원합니다. 무료로 체험해 보세요."
weight: 100
---

개발자 API를 통해 대규모로 Excel 암호 보호를 자동화하세요. 열기 및 수정 암호를 프로그래밍 방식으로 적용할 수 있으며, 엔터프라이즈 워크플로우에 이상적이며 .xlsx 및 레거시 형식을 지원합니다. 문서를 확인하고 오늘 바로 무료 통합을 시작하세요.

## **스프레드시트 보호 API**

### **웹 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요하며, 안전하게 설계되었습니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                 |
| :------------ | :----- | :------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | 파일   | FormData                   | 업로드하여 암호 암호화로 보호할 Excel 스프레드시트 파일입니다.                                                                                      |
| openPassword  | 문자열 | 쿼리                       | 보호된 스프레드시트를 열기(복호화)하기 위해 필요한 암호입니다.                                                                                      |
| modifyPassword| 문자열 | 쿼리                       | 스프레드시트 콘텐츠의 편집 또는 수정을 활성화하기 위해 필요한 암호입니다.                                                                           |
| outPath       | 문자열 | 쿼리                       | (선택 사항) 보호된 워크북을 저장할 출력 폴더 경로를 지정합니다. 지정하지 않으면 파일이 응답에 포함됩니다.                                            |
| outStorageName| 문자열 | 쿼리                       | 보호된 출력 파일을 저장하는 데 사용할 클라우드 스토리지 이름입니다.                                                                                 |
| region        | 문자열 | 쿼리                       | 처리 중 스프레드시트에 적용할 지역/문화 설정(예: 날짜 형식, 숫자 서식)을 지정합니다.                                                                 |

**인증**  
스프레드시트 보호 API에 대한 모든 호출에는 유효한 OAuth 2.0 액세스 토큰이 필요합니다. 토큰은 `Authorization` 헤더에 포함해야 합니다:

```http
Authorization: Bearer {access_token}
```

이 토큰은 Aspose Cloud의 인증 엔드포인트에서 가져와야 하며, **Cells** 범위를 포함해야 합니다.

## **응답**

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

| 코드 | 의미                 | 설명                                                     |
| ---- | --------------------- | ---------------------------------------------------------- |
| 200  | OK (성공)             | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)가 있습니다. |
| 401  | 인증되지 않음         | 잘못되거나 누락된 JWT 토큰입니다.                           |
| 413  | 페이로드가 너무 큼    | 업로드된 파일이 크기 제한을 초과합니다.                      |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류가 발생했습니다.                         |

## 보호 스프레드시트 API는 어디에 사용해야 하나요?

- **민감한 금융 데이터 보호** – 예산, 송장, 급여 정보가 포함된 Excel 파일을 열기 및 수정 암호로 보호하여 무단 접근이나 편집을 방지하세요.
- **기밀 보고서 안전 공유** – 내부 및 외부 배포 시 승인된 수신자만 비즈니스, 감사 또는 준수 보고서를 열거나 수정할 수 있도록 보장하세요.
- **워크플로우에서 문서 보안 자동화** – ERP, CRM 등 엔터프라이즈 시스템에 API를 통합하여 생성된 스프레드시트를 저장 또는 이메일 전송 전에 자동으로 암호로 보호하세요.
- **읽기 전용 액세스 적용** – 별도의 수정 암호를 사용하여 사용자가 보고서를 열어 볼 수는 있지만 수정은 제한하세요. 템플릿 또는 최종 데이터셋에 이상적입니다.
- **규정 준수 보장** – 자동 보호를 통해 데이터 저장 시 및 전송 중에 민감한 스프레드시트 데이터를 암호화하여 GDPR, HIPAA, SOX 요건을 충족할 수 있도록 도와줍니다.

## 왜 보호 스프레드시트 API를 사용해야 하나요?

- **개발자 친화적** – Aspose.Cells Cloud는 다양한 언어로 SDK 라이브러리를 제공하여 빠른 개발을 지원하며, 포괄적인 문서도 제공됩니다. 사용자 정의 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **인력 필요 감소** – 문서 통합 및 보안을 자동화하여 전담 인력을 줄일 수 있습니다.
- **사용량 과금** – 사전 투자 불필요하며, 실제로 사용한 API 호출 수에 대해서만 비용이 부과됩니다.
- **유지보수 비용 없음** – 유지보수할 서버가 없고, 소프트웨어 업데이트나 호환성 문제도 없습니다.
- **원본 Excel 서식 보존** – 암호 보호를 적용하더라도 보호된 워크북이 원본 파일과 동일하게 표시되도록 보장합니다.

## SDK를 사용하여 보호 스프레드시트 API 사용 방법

### OpenAPI 사양

[Protect Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 공개적으로 액세스 가능한 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?openPassword=MyOpenPwd&modifyPassword=MyModifyPwd" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 인코딩)",
  "contentType": "MIME 유형",
  "fileDownloadName": "선택적 파일 이름"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 기본 세부 정보를 처리하므로 최소한의 코드로 스프레드시트 보호 기능만 구현하면 됩니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 설명합니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}