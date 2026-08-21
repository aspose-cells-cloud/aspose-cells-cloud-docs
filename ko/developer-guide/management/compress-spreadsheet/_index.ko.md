---
title: "Aspose.Cells Cloud Excel 압축 웹 API – 스프레드시트 파일 크기 프로그래밍 방식으로 줄이기"
second_title: "문서"
ArticleTitle: "Excel 파일 압축 방법 – 스프레드시트 크기 축소 및 성능 최적화"
linktitle: "스프레드시트 압축"
type: docs
url: /compress-spreadsheet/
keywords: "Excel 압축, Aspose.Cells Cloud, 스프레드시트 크기 축소, API, 워크북 최적화"
description: "Aspose.Cells Cloud API로 Excel 워크북을 압축하는 방법을 알아보세요. 단계별 예제, 매개변수, 인증 및 모범 사례를 확인하세요."
weight: 100
---

Aspose.Cells Cloud API를 사용하여 Excel 스프레드시트를 프로그래밍 방식으로 압축하고 파일 크기를 줄이세요. 사용하지 않는 데이터 제거, 포함된 개체 압축, 서식 정리를 통해 워크북 성능을 최적화하세요. 이 RESTful API는 Excel 파일 압축 및 최적화 워크플로우를 자동화할 수 있습니다.

## **스프레드시트 압축 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### 요청 매개변수

| 매개변수 이름 | 유형    | 경로/쿼리/문자열/HTTP 본문 | 설명                                                                                                                           |
| ------------- | ------- | -------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | 파일    | FormData                   | **필수.** 압축할 원본 Excel 워크북 파일( `.xlsx`, `.xls` 등)을 지정합니다.                                                     |
| level         | 정수    | 쿼리                       | **선택 사항.** 압축 강도(0 = 가장 빠름/최소, 9 = 가장 느림/최대). 생략 시 균형 잡힌 기본값(5)이 적용됩니다.         |
| outPath       | 문자열  | 쿼리                       | **선택 사항.** 클라우드 저장소 내 저장 대상 폴더 경로. 생략 시 원본 워크북과 동일한 폴더에 저장됩니다. |
| outStorageName| 문자열  | 쿼리                       | **필수.** 구성된 클라우드 저장소 서비스의 식별자(예: `CorporateDrive`).                                            |
| region        | 문자열  | 쿼리                       | **선택 사항.** 지역 설정(예: `de-DE`)으로, 지역별 데이터 처리 방식에 영향을 줄 수 있습니다.                                           |
| password      | 문자열  | 쿼리                       | **선택 사항.** 암호화된 스프레드시트를 복호화하기 위한 비밀번호. 파일이 암호화되어 있지 않으면 비워 둡니다.                              |

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

| 코드 | 의미                | 설명                                                      |
| ---- | ------------------- | --------------------------------------------------------- |
| 200  | OK (성공)           | 필터가 성공적으로 적용됨; 응답에는 작업 세부정보 포함     |
| 400  | Bad Request         | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형)   |
| 401  | Unauthorized        | 잘못되거나 누락된 JWT 토큰                                 |
| 413  | Payload Too Large   | 업로드된 파일이 크기 제한을 초과함                         |
| 500  | Internal Server Error | 예기치 않은 서버 오류                                     |

## 스프레드시트 압축 API를 어디에 사용해야 할까요?

- **자동 보고서 배포** – 이메일로 전송 전에 월간 재무 보고서를 압축해 전송 성공률을 높이고 수신자의 사용자 경험을 개선하세요.
- **사용자 파일 업로드 최적화** – 백그라운드에서 업로드된 Excel 파일을 압축해 클라우드 저장 공간을 절약하고 저장 비용을 줄이세요.
- **데이터 파이프라인 처리 및 마이그레이션** – ETL 프로세스 중 생성된 중간 Excel 파일을 압축해 네트워크 전송 속도를 높이고 임시 저장소 부하를 줄이세요.

## 왜 스프레드시트 압축 API를 사용해야 할까요?

- **개발자 친화적** – Aspose.Cells Cloud는 다양한 언어의 SDK 라이브러리를 제공하며, 체계적인 문서로 빠른 개발을 지원합니다.
- **인력 비용 절감** – 문서를 수동으로 통합할 필요 없이 전담 인력을 배치할 필요가 없습니다.
- **사용량 과금형 가격 정책** – 선불 투자가 필요 없으며, 실제로 수행한 API 호출에 대해서만 요금이 부과됩니다.
- **서버 유지보수 불필요** – 유지보수할 서버가 없고, 소프트웨어 업데이트 및 호환성 문제도 없습니다.

## SDK와 함께 스프레드시트 압축 API 사용하기

### 스프레드시트 압축 API 사양

[스프레드시트 압축 API 사양](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet)은 REST 상호작용을 위한 공개 인터페이스를 제공하며, 웹 브라우저에서 직접 API 호출이 가능합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청(Request)" tabName12="응답(Response)" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx"
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

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 저수준 세부 사항을 추상화해 몇 줄의 코드만으로 스프레드시트를 압축할 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}