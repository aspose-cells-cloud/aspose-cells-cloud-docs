---
title: "모든 문서 속성 가져오기"
second_title: "문서"
linktitle: "모두 가져오기"
type: docs
url: /ko/document-properties/get-all/
aliases: [  /ko/get-all-document-properties/ ]
keywords: "모든 문서 속성 가져오기, Aspose.Cells Cloud, Excel 문서 속성, REST API, SDK, Excel 메타데이터"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일에서 모든 문서 속성을 검색합니다. 이 엔드포인트는 지원되는 모든 SDK 및 프로그래밍 언어와 함께 작동합니다."
ArticleTitle: "모든 문서 속성 가져오기 – Aspose.Cells Cloud API"
weight: 25
---

이 REST API는 문서 속성을 읽습니다.

## GetDocumentProperties API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 설명                          |
| -------------- | ------ | -------- | ---------------------------- |
| name           | string | path     | Excel 파일 이름.              |
| folder         | string | query    | 파일이 포함된 폴더.           |
| storageName    | string | query    | 저장소 서비스 이름.           |

[OpenAPI 스펙](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperties)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperties": {
    "DocumentPropertyList": [
      {
        "Name": "제목",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Title",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "주제",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Subject",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "작성자",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Author",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "키워드",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Keywords",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "주석",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Comments",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "최종 저장자",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/LastSavedBy",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "생성 시간",
        "Value": "6/5/2015 6:17:20 PM",
        "BuiltIn": "True",
        "link": {
          "Href": "/CreateTime",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "최종 저장 시간",
        "Value": "9/27/2019 9:09:43 PM",
        "BuiltIn": "True",
        "link": {
          "Href": "/LastSavedTime",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "카테고리",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Category",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "응용 프로그램 이름",
        "Value": "Microsoft Excel",
        "BuiltIn": "True",
        "link": {
          "Href": "/NameOfApplication",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "버전",
        "Value": "16.0300",
        "BuiltIn": "True",
        "link": {
          "Href": "/Version",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "보안",
        "Value": "0",
        "BuiltIn": "True",
        "link": {
          "Href": "/Security",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "축소하여 맞춤",
        "Value": "False",
        "BuiltIn": "True",
        "link": {
          "Href": "/ScaleCrop",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "템플릿",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Template",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "관리자",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Manager",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "회사",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Company",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "링크 최신 상태",
        "Value": "False",
        "BuiltIn": "True",
        "link": {
          "Href": "/LinksUpToDate",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/documentproperties",
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

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                             |
|------|------------------------------|--------------------------------------------------|
| 200  | OK (성공)                    | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함. |
| 400  | 잘못된 요청                  | 누락되었거나 유효하지 않은 매개변수 (예: 지원되지 않는 파일 유형). |
| 401  | 인증되지 않음                | 유효하지 않거나 누락된 JWT 토큰. |
| 413  | 페이로드가 너무 큼           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | 내부 서버 오류               | 예기치 않은 서버 오류 발생. |

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperties.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperties.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperties.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperties.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperties.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperties.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperties.go" >}}

{{< /tab >}}

{{< /tabs >}}