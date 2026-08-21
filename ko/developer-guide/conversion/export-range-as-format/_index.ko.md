---
title: "Excel 범위를 PDF, PNG, CSV로 내보내기 – Aspose.Cells Cloud API"
second_title: "문서"
ArticleTitle: "원격 스프레드시트 범위를 다른 형식으로 내보내는 방법: 단계별 가이드"
linktype: "Export Range as Format"
type: docs
url: /export-range-as-format/
keywords: "Aspose Cells, Excel 범위 내보내기, PDF, PNG, CSV, 클라우드 API, 스프레드시트 변환"
description: "Aspose.Cells Cloud에 저장된 특정 Excel 범위를 PDF, PNG, CSV 또는 다른 형식으로 변환하는 방법을 알아보세요. 엔드포인트 세부 정보, 매개변수, 샘플 요청, 응답 처리 및 오류 정보가 포함됩니다."
weight: 100
---

클라우드 스프레드시트/Excel 범위를 다른 형식의 파일로 내보냅니다. 이 형식 파일은 클라우드에 저장하거나 로컬 저장소로 내보낼 수 있습니다.

## 범위를 다른 형식으로 내보내기 API

### 웹 API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름       | 유형   | 위치 | 설명                                                                                                                                              |
| :----------------- | :----- | :--- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| **name**           | 문자열 | 경로 | (필수) 가져올 워크북 파일의 이름입니다.                                                                                                             |
| **worksheet**      | 문자열 | 경로 | 스프레드시트의 워크시트 이름입니다.                                                                                                                 |
| **range**          | 문자열 | 경로 | 변환할 범위 (예: `A1:C12`)                                                                                                                          |
| **format**         | 문자열 | 쿼리 | (필수) 원하는 출력 형식 (예: `pdf`, `png`, `svg`)                                                                                                   |
| **folder**         | 문자열 | 쿼리 | (선택사항) 워크북이 저장된 폴더 경로입니다.                                                                                                          |
| **storageName**    | 문자열 | 쿼리 | (선택사항) 사용자 정의 클라우드 저장소를 사용할 경우 저장소 이름입니다.                                                                               |
| **outPath**        | 문자열 | 쿼리 | (선택사항) 클라우드 저장소에 출력 파일을 저장할 경로입니다.                                                                                           |
| **outStorageName** | 문자열 | 쿼리 | (선택사항) 출력 파일을 저장할 저장소 이름입니다.                                                                                                     |
| **fontsLocation**  | 문자열 | 쿼리 | (선택사항) 사용자 정의 글꼴 위치입니다.                                                                                                             |
| **region**         | 문자열 | 쿼리 | (선택사항) 스프레드시트 지역/언어 설정 (예: `en-US`, `fr-FR`). 숫자 포맷, 날짜 파싱 및 로케일 관련 동작에 영향을 미칩니다.                              |
| **password**       | 문자열 | 쿼리 | (선택사항) 스프레드시트 파일을 열기 위해 필요한 비밀번호입니다.                                                                                      |

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

| 코드 | 의미                  | 설명                                                           |
| ---- | --------------------- | -------------------------------------------------------------- |
| 200  | OK (성공)             | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request (잘못된 요청) | 누락되거나 유효하지 않은 매개변수 (예: 지원되지 않는 파일 형식)         |
| 401  | Unauthorized (인증 실패) | 유효하지 않거나 누락된 JWT 토큰                                           |
| 413  | Payload Too Large (페이로드 크기 초과) | 업로드된 파일이 크기 제한을 초과했습니다.                              |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류가 발생했습니다.                                      |

## 범위를 다른 형식으로 내보내기 API를 어디에 사용해야 하나요?

### 데이터 내보내기 및 이전 시나리오

- **데이터베이스 통합** – 특정 Excel 범위를 데이터베이스 시스템으로 직접 내보냅니다.
- **애플리케이션 통합** – 선택한 스프레드시트 데이터를 SaaS 애플리케이션에 공급합니다.
- **시스템 이전** – 구식 시스템과 최신 시스템 간에 특정 데이터 범위를 전송합니다.
- **크로스플랫폼 공유** – 다양한 플랫폼 간에 집중적인 데이터 하위 집합을 공유합니다.

### 리포팅 및 분석

- **타겟 리포팅** – 집중적인 분석을 위해 특정 리포트 섹션을 다른 형식으로 내보냅니다.
- **대시보드 데이터 피드** – BI 대시보드 도구에 특정 데이터 범위를 제공합니다.
- **성과 측정 지표** – 성과 추적 시스템에 KPI 범위를 추출합니다.
- **재무 보고** – 외부 감사를 위해 재무 제표 섹션을 내보냅니다.

### 개발 및 테스트

- **테스트 데이터 관리** – 테스트 목적을 위해 특정 데이터 범위를 내보냅니다.
- **개발 환경** – 개발 팀에 샘플 데이터 범위를 공유합니다.
- **API 테스트** – 특정 스프레드시트 섹션에서 CSV 테스트 데이터를 생성합니다.
- **프로토타입 개발** – 애플리케이션 프로토타입에 집중적인 데이터 세트를 제공합니다.

### 비즈니스 운영

- **선택적 데이터 공유** – 외부 파트너와 특정 데이터 범위를 공유합니다.
- **부분 데이터 백업** – 선택한 형식으로 중요한 데이터 범위를 백업합니다.
- **부서 간 데이터 전송** – 부서 간에 특정 데이터를 공유합니다.
- **규정 준수 보고** – 규정 준수 제출을 위해 규제 데이터 범위를 내보냅니다.

### 자동화 워크플로우

- **예약 범위 내보내기** – 특정 범위를 예약된 일정에 따라 자동으로 내보냅니다.
- **트리거 기반 추출** – 비즈니스 이벤트나 트리거에 따라 범위를 내보냅니다.
- **워크플로우 통합** – 범위 내보내기를 비즈니스 프로세스 워크플로우에 통합합니다.
- **배치 범위 처리** – 여러 특정 범위를 배치 작업으로 처리합니다.

## 왜 범위를 다른 형식으로 내보내기 API를 사용해야 하나요?

- **개발자 친화적** – Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하며, 포괄적인 문서를 통해 빠른 개발을 지원합니다. 사용자 정의 차트 렌더링 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **인건비 절감** – 문서 통합에 전담 인력이 덜 필요합니다.
- **사용량 과금** – 사전 투자가 필요 없으며, 실제로 사용한 API 호출에 대해서만 비용이 부과됩니다.
- **서버 유지보수 불필요** – 유지보수할 서버가 없고, 소프트웨어 업데이트 및 호환성 문제도 없습니다.
- **복잡한 Excel 포맷 보존** – 출력 파일은 원본 스프레드시트의 포맷을 그대로 유지합니다.

## SDK를 사용하여 스프레드시트 범위를 다른 형식으로 내보내기 API를 어떻게 사용하나요?

### 범위를 다른 형식으로 내보내기 API 사양

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat" rel="noopener noreferrer">범위를 다른 형식으로 내보내기 API 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공하여, 웹 브라우저에서 직접 REST 상호 작용을 가능하게 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf" \
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

SDK를 사용하면 저수준 세부 사항을 추상화하여 단순한 코드로 스프레드시트 범위를 형식 파일로 내보낼 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}