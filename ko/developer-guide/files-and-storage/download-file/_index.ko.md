---
title: "Aspose.Cells Cloud 다운로드 파일 API – 클라우드에서 빠른 파일 다운로드를 위한 인터페이스"
second_title: "문서"
articleTitle: "Aspose.Cells Cloud 다운로드 파일 API – 클라우드에서 빠른 파일 다운로드를 위한 인터페이스"
linkTitle: "다운로드 파일 API"
type: docs
url: /download-file/
keywords: "Aspose.Cells, 다운로드 파일 API, 엑셀 클라우드 저장소, REST API, 파일 다운로드, PDF, CSV, SDK"
description: "Aspose.Cells Cloud 저장소에서 엑셀, PDF, CSV 및 기타 파일을 Download File API(v4.0)를 통해 다운로드합니다. 엔드포인트, 매개변수, 인증 세부 정보 및 코드 예제가 포함됩니다."
weight: 100
---

**DownloadFile** API는 Aspose.Cells Cloud 저장소에 저장된 파일을 검색할 수 있도록 해줍니다. 다운로드 파일 API는 클라우드에서 엑셀 스프레드시트, PDF, CSV 및 기타 지원 포맷을 직접 접근하는 데 필수적입니다.

## **엑셀 API: 파일 다운로드**

### 웹 API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **DownloadFile** API의 요청 매개변수는 다음과 같습니다.

| 매개변수 이름 | 유형   | 위치 (경로 / 쿼리) | 설명                                                             |
| ------------- | ------ | ------------------ | ---------------------------------------------------------------- |
| path          | String | Path               | 다운로드하려는 파일의 가상 경로입니다.                            |
| storageName   | String | Query              | 파일을 검색할 저장소의 이름입니다.                               |
| versionId     | String | Query              | 다운로드할 파일의 버전 식별자입니다(해당되는 경우).               |

### **응답**

API는 **이진 파일 스트림**을 반환합니다. `Content-Type` 헤더는 파일 형식과 일치합니다(예: XLSX는 `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet`). JSON 페이로드는 반환되지 않습니다.

**HTTP 상태 코드**

| 코드 | 의미                 | 설명                                                                 |
| ---- | ------------------- | ------------------------------------------------------------------- |
| 200  | OK (성공)           | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함되어 있습니다. |
| 400  | Bad Request         | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형)가 있습니다.     |
| 401  | Unauthorized        | 잘못되었거나 누락된 JWT 토큰입니다.                                  |
| 413  | Payload Too Large   | 업로드된 파일이 크기 제한을 초과합니다.                              |
| 500  | Internal Server Error | 예기치 않은 서버 오류입니다.                                         |

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/FileController/DownloadFile)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 REST 상호작용을 직접 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해 주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}