---
title: "엑셀 파일을 여러 파일로 분할"
second_title: "Document"
linktype: "분할 다중 엑셀 파일"
type: docs
url: /ko/split-an-excel-file-to-multi-files/
aliases: [  /ko/split-excel-workbooks/ , /ko/workbook/split/ ]
keywords: "Aspose.Cells, 클라우드, 엑셀, 분할, API, PDF, CSV, JSON"
description: "Aspose.Cells Cloud REST API를 사용하여 다중 시트 엑셀 워크북을 개별 파일로 분할합니다. PDF, CSV, JSON 등의 출력 형식을 지원하며, 안드로이드, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift용 SDK를 통해 제공됩니다."
weight: 32
ArticleTitle: "엑셀 파일을 여러 파일로 분할 - Aspose.Cells Cloud 문서"
---

Aspose.Cells Cloud REST API는 다중 시트 엑셀 워크북을 개별 파일로 분할합니다.

**사전 요구 사항**  
API를 호출하기 전에 유효한 JWT 토큰을 획득하여 각 요청의 `Authorization` 헤더에 포함해야 합니다. 자세한 내용은 [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하세요.

## PostSplit API

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.


### 요청 매개변수

| 매개변수 이름 | 유형   | 위치      | 설명                                                        |
|--------------|--------|-----------|-------------------------------------------------------------|
| file         | file   | formData  | 업로드할 엑셀 워크북 파일입니다.                             |
| format       | string | query     | 원하는 출력 형식 (예: `pdf`, `csv`, `json`).                 |
| password     | string | query     | 암호화된 워크북의 비밀번호 (선택 사항).                      |
| from         | integer| query     | 포함할 첫 번째 시트의 인덱스 (1부터 시작).                   |
| to           | integer| query     | 포함할 마지막 시트의 인덱스 (포함).                          |

### **응답**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[file1 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[file2 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[file3 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                                  |
|------|-----------------------------|-------------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용되었고, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수 (예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰.                              |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과했습니다.               |
| 500  | Internal Server Error       | 예기치 않은 서버 오류입니다.                             |
## SDK를 사용하여 PostSplit API 사용하는 방법

### PostSplit API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**HTTP 상태 코드**

| 코드 | 의미                          | 설명                                                     |
|------|-------------------------------|----------------------------------------------------------|
| 200  | OK                            | 워크북이 성공적으로 분할되었고, 응답에 파일 목록이 포함됩니다. |
| 400  | Bad Request                   | 누락되거나 잘못된 매개변수 (예: 지원되지 않는 형식).      |
| 401  | Unauthorized                  | 잘못되거나 누락된 JWT 토큰.                               |
| 500  | Internal Server Error         | 서버 측에서 예기치 않은 오류가 발생했습니다.              |

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# xxxxx1.xlsx 및 xxxxx2.xlsx를 실제 엑셀 파일 경로로 바꾸세요
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_sheet1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        },
        {
            "Filename": "xxxxx_sheet2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트의 핵심 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스로 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
---