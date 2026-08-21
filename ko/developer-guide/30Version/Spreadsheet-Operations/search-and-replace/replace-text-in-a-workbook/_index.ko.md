---
title: "Excel 워크북에서 텍스트 바꾸기"
second_title: "문서"
linktitle: "워크북에서 바꾸기"
type: docs
url: /ko/workbook/replace-text/
aliases: [  /ko/replace-text-in-a-workbook/ ]
weight: 60
keywords: "Aspose.Cells Cloud, 텍스트 바꾸기, Excel 워크북, XLSX, ODS, REST API, 스프레드시트, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel(XLS, XLSX, XLSM, XLSB) 및 OpenDocument 스프레드시트(ODS) 워크북에서 텍스트를 바꿉니다. cURL 및 다양한 SDK(C#, Java, PHP, Ruby, Node.js, Python, Perl, Go 등)를 통해 사용할 수 있습니다."
---

이 REST API는 Excel 워크북에서 텍스트를 바꿉니다.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
```
### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 설명                                             |
| -------------- | ------ | -------- | ------------------------------------------------------- |
| name           | string | path     | 워크북 파일 이름.                              |
| sheetName      | string | path     | 바꾸기 작업이 수행되는 워크시트 이름.     |
| oldValue       | string | query    | 바뀔 텍스트.                           |
| newValue       | string | query    | 기존 값을 대체할 텍스트.                   |
| folder         | string | query    | 워크북이 위치한 폴더 경로.                    |
| storageName    | string | query    | 워크북이 저장된 스토리지 서비스 이름. |

### **응답**

```json
{
    "Status":"OK",
    "Code":200,
      "Workbook": {
    "FileName": "test.xlsx",
    "Links": [
      {
        "Href": "/test.xlsx",
        "Rel": "self",
        "Title": null,
        "Type": null
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "CSV로 다운로드",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "HTML로 다운로드",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ODS로 다운로드",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "PDF로 다운로드",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "테이블 구분 텍스트 형식으로 다운로드",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "TIFF로 다운로드",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Microsoft Excel 2003으로 다운로드",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Microsoft Excel 2007으로 다운로드",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "XPS로 다운로드",
        "Type": "application/vnd.ms-xpsdocument"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "/worksheets",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "/defaultstyle",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "/documentproperties",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Names": {
      "link": {
        "Href": "/names",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Settings": {
      "link": {
        "Href": "/settings",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "IsWriteProtected": "False",
    "IsProtected": "False",
    "IsEncryption": "false",
    "Password": null
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용되었으며, 응답에는 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized                | 유효하지 않거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과합니다. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |
## SDK를 사용하여 PostReplace API 사용하는 방법

### PostReplace API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextReplace)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 쉽게 호출할 수 있습니다. 아래 예제는 cURL을 사용하여 요청을 만드는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/replaceText?oldValue=a&newValue=a12" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Matches": 26,
  "Workbook": {
    "link": {
      "Href": "/test.xlsx",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 이 기능을 통합하는 데 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookTextReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookTextReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookTextReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookTextReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookTextReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookTextReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookTextReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookTextReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}