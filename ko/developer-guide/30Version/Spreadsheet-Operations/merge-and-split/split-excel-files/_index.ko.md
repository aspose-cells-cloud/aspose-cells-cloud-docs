---
title: "엑셀 워크북을 여러 파일로 분할"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 엑셀 워크북을 여러 파일로 분할하는 방법"
second_title: "문서"
linktype: "분할"
type: docs
url: /split-multi-excel-files/
aliases: [/split/multi-files/]
keywords: "엑셀, Aspose.Cells Cloud, REST API, 워크북 분할, 여러 파일, JPEG, PNG, PDF, CSV, JSON"
description: "Aspose.Cells Cloud REST API를 사용하면 엑셀 워크북을 다양한 형식의 여러 파일로 분할할 수 있습니다. 이 문서에는 C#, Java, PHP, Ruby, Node.js, Python, Perl, Go 등의 언어에 대한 요청 매개변수, cURL 예제 및 SDK 코드 예시가 포함되어 있습니다."
weight: 130
---

이 REST API는 엑셀 **워크북**을 다양한 형식의 여러 파일로 분할합니다.

> **사전 조건** – 이 API를 사용하려면 유효한 JWT 토큰을 획득해야 하며, 지원되는 SDK 버전을 사용하고 있으며 워크북이 지원되는 저장소 위치에 저장되어 있어야 합니다. 또한 API는 플랫폼 가이드라인에 명시된 대로 파일 크기 제한을 적용합니다.

## PostWorkbookSplit API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름         | 유형    | 위치       | 설명                                                                                     | 필수 여부 |
| -------------------- | ------- | ---------- | ---------------------------------------------------------------------------------------- | -------- |
| files[]              | 파일    | formData   | **분할**할 하나 이상의 엑셀 워크북. 요청 시 `file1`, `file2`, … 을 사용합니다.          | 예       |
| format               | 문자열  | 쿼리       | 분할된 파일의 원하는 출력 형식.                                                          | 아니요    |
| from                 | 정수    | 쿼리       | 시작 워크시트 인덱스.                                                                    | 아니요    |
| to                   | 정수    | 쿼리       | 끝 워크시트 인덱스.                                                                      | 아니요    |
| horizontalResolution | 정수    | 쿼리       | 이미지 가로 해상도.                                                                      | 아니요    |
| verticalResolution   | 정수    | 쿼리       | 이미지 세로 해상도.                                                                      | 아니요    |
| outFolder            | 문자열  | 쿼리       | 분할된 파일의 출력 폴더.                                                                 | 아니요    |
| splitNameRule        | 문자열  | 쿼리       | 분할된 파일에 적용할 이름 규칙.                                                          | 아니요    |
| folder               | 문자열  | 쿼리       | 원본 워크북이 위치한 폴더.                                                               | 아니요    |
| storageName          | 문자열  | 쿼리       | 사용할 저장소 이름.                                                                      | 아니요    |

### **응답**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[file1 이름]",
        "Filesize" : [파일 크기],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[file2 이름]",
        "Filesize" : [파일 크기],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[file3 이름]",
        "Filesize" : [파일 크기],
        "FileContent" : "[Base64String]"
      }
    ]
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                                     |
|------|-----------------------------|----------------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청                  | 누락되거나 잘못된 매개변수 (예: 지원되지 않는 파일 형식) |
| 401  | 인증되지 않음                | 잘못되거나 누락된 JWT 토큰                              |
| 413  | 페이로드가 너무 큼           | 업로드된 파일이 크기 제한을 초과했습니다.               |
| 500  | 내부 서버 오류               | 예기치 않은 서버 오류                                    |

## SDK를 사용하여 PostWorkbookSplit API 사용하기

### PostWorkbookSplit API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
---