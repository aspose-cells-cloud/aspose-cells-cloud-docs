---
title: "Excel 워크시트에서 텍스트 교체하기 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "워크시트 내 텍스트 교체"
type: docs
url: /ko/worksheets/replace-text/
aliases: [  /ko/replace-text-in-a-workbook/ ]
keywords: "Aspose.Cells, 텍스트 교체, Excel, REST API, 스프레드시트, 워크시트"
description: "Aspose.Cells Cloud API(v3.0)를 사용하여 Excel 워크시트에서 텍스트를 교체하는 방법을 알아보세요. 필요한 사전 조건, 인증, 요청 구문, cURL 예제, SDK 코드 샘플, 응답 세부 정보 및 오류 처리를 포함합니다."
ArticleTitle: "Excel 워크시트에서 텍스트 교체하기 – Aspose.Cells Cloud API"
weight: 70
---

이 REST API는 **Aspose.Cells 텍스트 교체 API**를 사용하여 Excel 워크시트의 텍스트를 교체합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 보안을 위해 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
```

### 요청 파라미터

| 파라미터 이름   | 유형   | 위치   | 설명                              |
| --------------- | ------ | ------ | --------------------------------- |
| **name**        | string | path   | Excel 워크북의 이름입니다.        |
| **sheetName**   | string | path   | 워크시트의 이름입니다.            |
| **oldValue**    | string | query  | 교체할 텍스트입니다.              |
| **newValue**    | string | query  | 교체될 새로운 텍스트입니다.       |
| **folder**      | string | query  | 파일이 포함된 폴더입니다.         |
| **storageName** | string | query  | 스토리지 서비스 이름입니다.       |

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

| 코드 | 의미                      | 설명                                              |
|------|---------------------------|---------------------------------------------------|
| 200  | OK                        | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request               | 누락되었거나 잘못된 파라미터(예: 지원되지 않는 파일 형식)입니다. |
| 401  | Unauthorized              | 유효하지 않거나 누락된 JWT 토큰입니다.             |
| 413  | Payload Too Large         | 업로드된 파일이 크기 제한을 초과했습니다.          |
| 500  | Internal Server Error     | 예기치 않은 서버 오류입니다.                       |

## SDK를 사용하여 PostWorksheetTextReplace API 사용하는 방법

### PostWorksheetTextReplace API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextReplace)은 이 공개적으로 접근 가능한 인터페이스를 정의합니다.

cURL 명령줄 도구를 사용하여 서비스를 호출할 수 있습니다:

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/replaceText?oldValue=b&newValue=b11" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Matches": 0,
  "Worksheet": {
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1",
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


### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetTextReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetTextReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetTextReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetTextReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetTextReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetTextReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetTextReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetTextReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}