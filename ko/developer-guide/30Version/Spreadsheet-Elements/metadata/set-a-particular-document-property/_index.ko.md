---
title: "Aspose.Cells Cloud API – 문서 속성 업데이트(설정)"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북에 문서 속성을 설정하거나 새로 생성합니다."
keywords: "Aspose.Cells, 클라우드 API, 문서 속성 업데이트, Excel 메타데이터, REST API, SDK 예제"
api_version: "v3.0"
---

# 개요
**문서 속성 업데이트(설정)** 작업을 사용하면 Aspose Cloud 스토리지에 저장된 Excel 워크북에서 새로운 문서 속성을 생성하거나 기존 속성을 수정할 수 있습니다.

*엔드포인트*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

요청은 설정할 속성을 설명하는 JSON 페이로드를 수신합니다.

---

## 사전 요구 사항
- 유효한 **JWT 액세스 토큰** (참조: **인증** 섹션).  
- 대상 워크북(`{name}`)은 이미 Aspose Cloud 스토리지(또는 지정한 폴더)에 존재해야 합니다.  
- 스토리지 이름(`storageName`)은 선택 사항이며, 생략 시 기본 스토리지가 사용됩니다.

---

## 인증
Aspose.Cells Cloud는 **JWT 토큰 기반 인증**을 사용합니다. 토큰은 `Authorization` 헤더에 포함해야 합니다:

```http
Authorization: Bearer <jwt-token>
```

JWT 토큰 획득 방법에 대한 자세한 내용은 [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하세요.

---

## HTTP 요청

| 요소             | 값 |
|------------------|----|
| **메서드**       | `PUT` |
| **URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type**| `application/json` |
| **Accept**       | `application/json` |

### 경로 매개변수

| 이름            | 유형   | 필수 여부 | 설명 |
|-----------------|--------|-----------|------|
| `name`          | string | ✅ | Excel 파일 이름(확장자 포함). |
| `propertyName`  | string | ✅ | 설정하거나 생성할 문서 속성의 이름. |

### 쿼리 매개변수

| 이름            | 유형   | 필수 여부 | 설명 |
|-----------------|--------|-----------|------|
| `folder`        | string | ❌ | 워크북이 위치한 스토리지 내 폴더 경로. |
| `storageName`   | string | ❌ | 스토리지 서비스의 이름. 생략 시 기본 스토리지를 사용합니다. |

### 요청 본문 – 문서 속성 객체

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // 선택 사항, 예: "true" 또는 "false"
  "Link": {                     // 선택 사항
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| 필드      | 유형   | 필수 여부 | 설명 |
|-----------|--------|-----------|------|
| **Name**  | string | ✅ | 속성 이름(예: `author`). |
| **Value** | string | ✅ | 속성 값. |
| **BuiltIn**| string | ❌ | 내장 속성 여부를 나타냅니다. |
| **Link**  | object | ❌ | 하이퍼링크 정보(`Href`, `Rel`, `Title`, `Type`). |

---

## 예제 요청(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author?folder=Docs&storageName=MyStorage" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -d '{
        "Name": "author",
        "Value": "aspose",
        "BuiltIn": "false",
        "Link": {
          "Href": "https://example.com",
          "Rel": "self",
          "Title": "Author link",
          "Type": "text/html"
        }
      }'
```

### 예제 성공 응답

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**HTTP 상태 코드**

| 코드 | 의미                        | 설명 |
|------|-----------------------------|------|
| 200  | OK                          | 필터가 성공적으로 적용되었으며, 응답에는 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과합니다. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |

---

## SDK 예제
다음 코드 스니펫은 공식 Aspose.Cells Cloud SDK를 사용하여 해당 작업을 호출하는 방법을 보여줍니다.

| 언어 | 예제 |
|------|------|
| **C#** | <details><summary>C# 예제 표시</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: \"test.xlsx\",\n    propertyName: \"author\",\n    property: new CellsDocumentProperty {\n        Name = \"author\",\n        Value = \"aspose\",\n        BuiltIn = \"false\",\n        Link = new Link {\n            Href = \"https://example.com\",\n            Rel = \"self\",\n            Title = \"Author link\",\n            Type = \"text/html\"\n        }\n    },\n    folder: \"Docs\",\n    storageName: \"MyStorage\"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>Java 예제 표시</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName(\"author\");\nprop.setValue(\"aspose\");\nprop.setBuiltIn(\"false\");\nLink link = new Link();\nlink.setHref(\"https://example.com\");\nlink.setRel(\"self\");\nlink.setTitle(\"Author link\");\nlink.setType(\"text/html\");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest(\"test.xlsx\", \"author\", prop, \"Docs\", \"MyStorage\");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>Python 예제 표시</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name=\"author\", value=\"aspose\", built_in=\"false\")\nprop.link = Link(href=\"https://example.com\", rel=\"self\", title=\"Author link\", type=\"text/html\")\nresponse = api.put_document_property(name=\"test.xlsx\", property_name=\"author\", property=prop, folder=\"Docs\", storage_name=\"MyStorage\")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>Node.js 예제 표시</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>Go 예제 표시</summary>```go\nimport (\n    \"context\"\n    cells \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: \"author\", Value: \"aspose\", BuiltIn: \"false\"}\nprop.Link = &cells.Link{Href: \"https://example.com\", Rel: \"self\", Title: \"Author link\", Type: \"text/html\"}\nreq := cells.PutDocumentPropertyRequest{Name: \"test.xlsx\", PropertyName: \"author\", Property: &prop, Folder: \"Docs\", StorageName: \"MyStorage\"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>Ruby 예제 표시</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>PHP 예제 표시</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>Perl 예제 표시</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## 관련 링크
- **OpenAPI 사양**: <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty> (새 탭에서 열림, `rel="noopener noreferrer"`).  
- **인증 가이드**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/> (새 탭에서 열림, `rel="noopener noreferrer"`).  
- **Aspose.Cells Cloud SDK**: <https://github.com/aspose-cells-cloud> (새 탭에서 열림, `rel="noopener noreferrer"`).  

---