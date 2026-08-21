---
title: "스마트 마커 템플릿을 사용하여 엑셀 리포트 구축하기"
second_title: "문서"
linktitle: "스마트마커"
type: docs
url: /build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "엑셀, 스마트 마커, Aspose.Cells Cloud, REST API, 워크북, SDK, API, 리포트 생성"
description: "Aspose.Cells Cloud REST API를 사용하여 스마트 마커 템플릿으로 엑셀 워크북을 생성하는 방법을 알아보세요. 요청/응답 세부 정보, cURL 예제, 사전 요구 사항, 참고 사항 및 SDK 코드 샘플을 포함합니다."
weight: 40
ArticleTitle: "스마트 마커 템플릿으로 엑셀 리포트 구축하기 – Aspose.Cells Cloud API 가이드"
---

이 REST API는 스마트 마커 템플릿을 사용하여 워크북을 생성합니다.

## 워크북 스마트마커 API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **스마트 마커란 무엇인가요?**

스마트 마커는 XML(또는 JSON) 파일의 데이터 필드를 엑셀 템플릿의 셀에 매핑하는 플레이스홀더 구문입니다. 런타임 시 Aspose.Cells는 마커를 해당 데이터로 대체하여 프로그래밍 방식으로 완전히 채워진 리포트를 생성할 수 있도록 합니다.

### **쿼리 매개변수**

| 매개변수 이름 | 유형   | 설명                                                  |
| -------------- | ------ | ------------------------------------------------------------ |
| outPath        | string | 생성된 워크북이 저장될 대상 경로입니다. |
| folder         | string | 원본 워크북이 포함된 폴더입니다.                     |
| storageName    | string | 사용할 스토리지 서비스의 이름입니다.                          |

### **요청 본문 매개변수**

| 매개변수 이름 | 유형 | 설명                                           |
| -------------- | ---- | ----------------------------------------------------- |
| xmlFile        | file | 요청과 함께 업로드된 스마트 마커 XML 데이터 파일입니다. |

### **응답**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**참고 / 제한 사항:**  
- 이 API는 최대 **50MB** 크기의 엑셀 파일을 지원합니다.  
- 허용되는 형식은 **.xlsx**, **.xlsm**, **.xlsb**만 있습니다.  
- 계정당 초당 **20개 요청**의 요청 제한이 적용됩니다.

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |
## 워크북 스마트마커 API 사용 방법

### 워크북 스마트마커 API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용하기

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

**간단한 1줄 예제**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **오류 처리**

| HTTP 상태 코드 | 설명           | 일반적인 원인                                           |
| ----------- | --------------------- | ------------------------------------------------------- |
| 400         | Bad Request           | 템플릿 누락, XML 형식 오류 또는 잘못된 매개변수. |
| 401         | Unauthorized          | 잘못되거나 누락된 인증 토큰.                |
| 404         | Not Found             | 지정된 워크북 또는 스토리지 위치가 존재하지 않음.  |
| 500         | Internal Server Error | 예기치 않은 서버 측 오류.                         |

**오류 응답 예시 (400)**

```json
{
  "Code": 400,
  "Message": "XML 데이터 파일이 누락되었거나 형식이 잘못되었습니다."
}
```

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}