---
title: "Aspose.Cells Cloud – 클라우드에서 엑셀 파일 병합 | API를 통한 스프레드시트 통합"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "클라우드에서 엑셀 파일 병합 – Aspose.Cells Cloud API를 사용해 온라인으로 스프레드시트 통합"
linktitle: "원격 스프레드시트 병합"
type: docs
url: /ko/merge-remote-spreadsheet/
keywords: "Aspose.Cells, 엑셀 병합, 클라우드 API, 스프레드시트 통합"
description: "Aspose.Cells Cloud API를 사용해 클라우드 스토리지에 저장된 엑셀 워크북을 병합합니다. 단일 HTTPS 호출에서 출력 형식, 대상 폴더 및 병합 모드를 지정할 수 있습니다."
weight: 100
---

Aspose.Cells Cloud API를 사용해 클라우드에 저장된 엑셀 파일을 다른 스프레드시트와 빠르게 병합하고, 출력 데이터 형식 및 저장 위치를 지정합니다.

## 원격 스프레드시트 병합 API

이 작업을 호출하기 전에 다음 사항을 확인하십시오:

- 유효한 **JWT 액세스 토큰** (인증 가이드 참조).
- 병합할 소스 워크북과 모든 파일이 클라우드 스토리지에 업로드되어 있음.
- 소스 폴더에서 읽기 및 대상 폴더에 쓰기 위한 적절한 권한이 있음.

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구하는 보안 API입니다.

### 요청 파라미터:

| 파라미터 이름      | 유형      | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                       |
| :---------------- | :-------- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| name              | String    | Path                       | 병합할 소스 워크북 파일의 이름.                                                                                             |
| mergedSpreadsheet | String    | Query                      | 소스 워크북에 병합할 스프레드시트 파일 이름 목록(쉼표로 구분).                                                               |
| folder            | String    | Query                      | 소스 워크북이 위치한 클라우드 스토리지 내 폴더 경로.                                                                        |
| outFormat         | String    | Query                      | 병합된 출력 파일의 원하는 형식(예: `XLSX`, `PDF`, `CSV`).                                                                   |
| mergeInOneSheet   | Boolean   | Query                      | `true`로 설정 시 모든 소스 데이터를 단일 워크시트에 병합, `false`일 경우 각 파일별로 별도 워크시트 생성.                     |
| storageName       | String    | Query                      | _(선택 사항)_ 소스 워크북이 위치한 클라우드 스토리지의 이름. 생략 시 기본 스토리지가 사용됩니다.                            |
| outPath           | String    | Query                      | _(선택 사항)_ 병합된 파일을 저장할 클라우드 스토리지 내 대상 폴더 경로. 생략 시 소스 폴더에 저장됩니다.                      |
| outStorageName    | String    | Query                      | 출력 파일을 저장할 클라우드 스토리지의 이름.                                                                                |
| fontsLocation     | String    | Query                      | _(선택 사항)_ 이미지/PDF 형식으로 변환 시 사용할 글꼴 파일이 있는 사용자 정의 폴더 경로.                                   |
| region            | String    | Query                      | _(선택 사항)_ 출력 파일의 날짜, 숫자 및 통화 서식에 사용할 로케일/지역(예: `en-US`, `de-DE`).                              |
| password          | String    | Query                      | _(선택 사항)_ 소스 워크북이 보호되어 있는 경우 필요로 하는 비밀번호.                                                       |

### 응답

**상태:** `200 OK`

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

파일은 `outPath`로 지정된 위치에서 직접 다운로드하거나 저장할 수 있습니다.

**성공 응답 세부 정보**

| 상태 코드 | 콘텐츠 유형                  | 설명                               |
| --------- | ---------------------------- | ---------------------------------- |
| 200 OK    | `application/octet-stream`   | 병합된 워크북 파일의 바이너리 스트림. |

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                   |
| ---- | --------------------- | ------------------------------------------------------ |
| 200  | OK                    | 필터 적용 성공; 응답에 작업 세부 정보 포함.             |
| 400  | Bad Request           | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized          | 잘못되거나 누락된 JWT 토큰.                             |
| 413  | Payload Too Large     | 업로드된 파일이 크기 제한을 초과함.                     |
| 500  | Internal Server Error | 예기치 않은 서버 오류.                                  |

## 원격 스프레드시트 병합 API 사용처

### 엔터프라이즈 수준 데이터 통합

- **다 부서 보고서 통합** – 영업, 마케팅, 재무 등 여러 팀에서 제출한 별도 엑셀 보고서를 통합.
- **지사별 데이터 요약** – 전 세계 각 지사에서의 성과 데이터를 요약.
- **파트너 데이터 통합** – 여러 파트너로부터 제출된 데이터를 단일 워크북으로 병합.

### 클라우드 문서 처리 워크플로우

- 클라우드 스토리지 파일 처리: AWS S3, Azure Blob, Google Cloud Storage 등에 저장된 엑셀 파일을 직접 병합.
- **다중 소스 데이터 통합** – 여러 클라우드 위치의 파일을 하나의 워크북으로 통합.
- **자동화 데이터 파이프라인** – ETL 프로세스에 API를 통합해 파일 병합을 자동화.

### 문서 관리 자동화

- **버전 관리 통합** – 프로젝트 계획 또는 예산 워크북의 여러 버전을 병합.
- **템플릿 데이터 채우기** – 표준화된 보고서 템플릿에 데이터 파일을 삽입.
- **정기 보고서 생성** – 주간, 월간, 분기별 요약 보고서 자동 생성.

### 크로스 플랫폼 협업

- **원격 팀 협업** – 분산된 팀 구성원이 제출한 작업 내용을 통합.
- **고객 데이터 정리** – 여러 고객으로부터의 주문 또는 피드백 데이터를 병합.
- **공급업체 정보 요약** – 여러 공급업체로부터의 견적 또는 제품 정보를 통합.

## 왜 원격 스프레드시트 병합 API를 사용해야 하나요?

- **개발자 친화적** – Aspose.Cells Cloud는 다양한 언어의 SDK를 제공해 개발 시간을 단축하고, 포괄적인 문서를 제공합니다. 맞춤 솔루션 구축에 비해 작업량을 크게 줄여줍니다.
- **인력 비용 절감** – 수동 문서 통합을 담당하는 인력을 줄일 수 있습니다.
- **사용량 과금** – 사전 투자 없이 실제로 사용한 API 호출에만 요금이 부과됩니다.
- **유지보수 비용 제로** – 유지 관리할 서버가 없으며, 소프트웨어 업데이트 및 호환성 문제도 없습니다.

## SDK와 함께 원격 스프레드시트 병합 API 사용하기

### 원격 스프레드시트 병합 API 사양

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet" target="_blank" rel="noopener noreferrer">원격 스프레드시트 병합 API 사양</a>은 모든 HTTP 클라이언트에서 직접 호출할 수 있는 REST 인터페이스를 설명합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/merge/spreadsheet?mergedSpreadsheet=Report1.xlsx&outFormat=XLSX&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}"
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

SDK를 사용하면 저수준 세부 사항을 추상화해 짧은 코드 스니펫으로 스프레드시트를 다른 스프레드시트에 병합할 수 있어 가장 빠른 개발 방법입니다.  
Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---