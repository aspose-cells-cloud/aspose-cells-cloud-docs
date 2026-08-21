---
title: "Aspose.Cells Cloud Excel 해제 웹 API – 프로그래밍 방식으로 열기 및 수정 비밀번호 제거"
second_title: "문서"
ArticleTitle: "Excel 보호 해제 – 열기 및 수정 비밀번호 즉시 해제"
linktitle: "스프레드시트 보호 해제"
type: docs
url: /ko/unprotect-spreadsheet/
keywords: "보호 해제, 스프레드시트, Aspose.Cells, API, Excel, 비밀번호 제거"
description: "Aspose.Cells Cloud 스프레드시트 보호 해제 API를 사용해 Excel 파일의 열기 및 수정 비밀번호를 프로그래밍 방식으로 제거합니다. .xlsx/.xls 지원, OAuth2 인증, 일괄 처리 기능을 제공합니다."
weight: 100
---

스프레드시트 보호 해제 API는 단일 요청으로 Excel 파일의 열기 및 수정 비밀번호 보호를 제거합니다. 데이터 파이프라인, 문서 관리 시스템, 마이그레이션 워크플로우에 적합합니다.

## **스프레드시트 보호 해제 API**

### **웹 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치     | 설명                                                                 |
| ------------- | ------ | -------- | -------------------------------------------------------------------- |
| Spreadsheet   | 파일   | FormData | 보호를 해제할 Excel 파일.                                            |
| password      | 문자열 | 쿼리     | 파일을 열 때 보호하는 비밀번호.                                      |
| modifyPassword| 문자열 | 쿼리     | 파일을 수정할 때 필요한 비밀번호(열기 비밀번호만 설정된 경우 선택 사항). |
| outPath       | 문자열 | 쿼리     | (선택 사항) 보호가 해제된 워크북이 저장될 폴더 경로.                |
| outStorageName| 문자열 | 쿼리     | (선택 사항) 출력 파일이 저장될 저장소 이름.                          |
| region        | 문자열 | 쿼리     | (선택 사항) 스프레드시트 지역 설정.                                  |

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

성공 응답은 보호가 해제된 파일을 스트림으로 반환합니다. 파일은 `outPath`/`outStorageName`으로 지정된 위치에 저장하거나 응답 페이로드에서 직접 가져올 수 있습니다.

**HTTP 상태 코드**

| 코드 | 의미                 | 설명                                                       |
| ---- | -------------------- | ---------------------------------------------------------- |
| 200  | 성공(OK)             | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함.       |
| 400  | 잘못된 요청(Bad Request) | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | 인증되지 않음(Unauthorized) | 유효하지 않거나 누락된 JWT 토큰.                            |
| 413  | 페이로드 너무 큼(Payload Too Large) | 업로드된 파일이 크기 제한을 초과함.                         |
| 500  | 내부 서버 오류(Internal Server Error) | 예기치 않은 서버 오류.                                      |

## 언제 스프레드시트 보호 해제 API를 사용해야 하나요?

- **잠긴 워크북에 대한 접근 복구** – 수동 개입 없이 잊어버린 열기 또는 수정 비밀번호를 빠르게 제거합니다.
- **대량 해제 자동화** – 데이터 마이그레이션 또는 아카이빙 프로젝트에서 수많은 파일을 처리합니다.
- **기존 워크플로우와 통합** – 저장소 또는 변환 API와 결합하여 엔드 투 엔드 파이프라인(예: 업로드 → 보호 해제 → PDF로 변환)을 구성합니다.
- **데이터 보안 유지** – 작업은 서버 측에서 수행되므로 원본 파일은 안전하게 유지되고, 보호가 해제된 버전은 클라우드 저장소에 저장됩니다.

## SDK를 사용하여 스프레드시트 보호 해제 API 사용하기

### OpenAPI 사양

[스프레드시트 보호 해제 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet)은 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스를 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
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

SDK를 사용하면 인증, 요청 구성, 응답 파싱을 자동으로 처리하므로 API 호출이 간편해집니다. 다양한 언어에서 사용 가능한 SDK가 제공되며, 스프레드시트 보호 해제를 위한 준비된 메서드를 포함하고 있습니다.

다음 코드 예제는 다양한 SDK를 사용해 스프레드시트 보호 해제 API를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}