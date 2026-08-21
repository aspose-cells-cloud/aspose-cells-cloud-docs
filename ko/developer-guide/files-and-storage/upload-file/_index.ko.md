---
title: "Aspose.Cells Cloud 업로드 파일 API – 클라우드에서 파일을 빠르게 업로드하기 위한 인터페이스"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud 업로드 파일 API – 클라우드에서 파일을 빠르게 업로드하기 위한 인터페이스"
linktitle: "파일 업로드"
type: docs
url: /upload-file/
keywords: "Aspose.Cells, 파일 업로드, Excel API, 클라우드 저장소, REST API"
description: "Aspose.Cells Cloud API를 사용해 파일을 업로드하는 가이드로, 요청 매개변수, HTTP 상태 코드, 오류 처리 및 코드 예제를 포함합니다."
weight: 100
---

**uploadFile** API는 개발자가 파일을 클라우드 저장소로 직접 업로드하여 Aspose Cells로 처리할 수 있도록 합니다.

## **Aspose Cells API: 파일 업로드**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **uploadFile** API의 요청 매개변수는 다음과 같습니다:

| 매개변수 이름 | 타입   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                      |
| :------------ | :----- | :------------------------- | :---------------------------------------------------------------------------------------- |
| UploadFiles   | 파일   | FormData                   | 클라우드 저장소에 파일을 업로드합니다.                                                    |
| path          | 문자열 | 경로                       | 클라우드 저장소 내 대상 경로입니다. 파일을 업로드할 위치를 지정합니다.                     |
| storageName   | 문자열 | 쿼리                       | 파일이 업로드될 저장소의 이름입니다.                                                      |

### **응답**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["파일 업로드 결과"],
  "Type": "클래스",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["업로드된 파일 이름 목록"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": ["오류 목록"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

이 API는 다음과 같은 HTTP 상태 코드를 반환합니다:

| 상태 코드                     | 설명                                               |
| ----------------------------- | -------------------------------------------------- |
| **200 OK**                    | 파일이 성공적으로 업로드되었습니다.                |
| **400 Bad Request**           | 잘못된 매개변수 또는 요청 형식이 올바르지 않습니다.  |
| **401 Unauthorized**          | 인증 토큰이 누락되었거나 유효하지 않습니다.          |
| **403 Forbidden**             | 지정된 저장소에 대한 권한이 부족합니다.            |
| **500 Internal Server Error** | 예기치 않은 서버 오류가 발생했습니다.              |

## SDK를 사용하여 파일 업로드 API를 어떻게 활용할 수 있나요?

### OpenAPI 스펙

[OpenAPI 스펙](https://reference.aspose.cloud/cells/#/FileController/UploadFile)은 API에 대한 자세한 설명을 제공하며, 개발자가 웹 브라우저를 통해 직접 API와 상호작용할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청(Request)" tabName12="응답(Response)" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 활용하면 저수준 세부 사항을 관리해 주므로 개발자는 프로젝트 작업에 집중할 수 있어 개발 효율성이 향상됩니다. [GitHub 저장소](https://github.com/aspose-cells-cloud)에서 Aspose.Cells Cloud SDK의 전체 목록을 확인할 수 있습니다.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**참고**

- [다운로드 파일 API](/download-file/) – 클라우드 저장소에서 파일을 다운로드합니다.
- [복사 파일 API](/copy-file/) – 클라우드 저장소 내에서 파일을 복사합니다.
- [삭제 파일 API](/delete-file/) – 클라우드 저장소에서 파일을 삭제합니다.

---