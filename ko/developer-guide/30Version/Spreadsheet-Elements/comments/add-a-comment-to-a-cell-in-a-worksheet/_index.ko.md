---
title: "워크시트 코멘트 추가"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 특정 셀에 코멘트를 추가합니다(PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName})."
keywords: "Aspose.Cells, 클라우드 API, 워크시트 코멘트 추가, Excel, 스프레드시트, 셀 코멘트"
weight: 20
api_version: "v3.0"
---

# 워크시트 코멘트 추가

Aspose.Cells Cloud REST API를 사용하여 Excel 워크북의 워크시트 내 특정 셀에 코멘트를 추가합니다.

---

## 사전 요구 사항 / 인증

* 모든 요청에는 **Bearer JWT 토큰**이 필요합니다.  
  *토큰 획득*: **/connect/token** 엔드포인트를 통해 토큰을 획득하세요([인증 가이드](/cells/authentication/) 참조).  
* 토큰은 `Authorization` 헤더에 포함해야 합니다:

```http
Authorization: Bearer <jwt token>
```

* 토큰과 데이터를 보호하기 위해 모든 호출은 **HTTPS**를 통해 이루어져야 합니다.

---

## HTTP 요청

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### 경로 매개변수

| 이름        | 타입     | 필수 여부 | 설명 |
|-------------|----------|------------|-------------|
| `name`      | 문자열   | ✔️ | 워크북 파일 이름(예: `test.xlsx`). |
| `sheetName` | 문자열   | ✔️ | 워크시트 이름(예: `Sheet1`). |
| `cellName`  | 문자열   | ✔️ | 대상 셀의 주소(예: `A1`). |

### 쿼리 매개변수

| 이름           | 타입     | 필수 여부 | 설명 |
|----------------|----------|------------|-------------|
| `folder`       | 문자열   | 선택 사항 | 워크북이 위치한 폴더. |
| `storageName`  | 문자열   | 선택 사항 | 파일이 위치한 스토리지 서비스 이름. |

### 요청 본문

본문은 JSON 형식의 **Comment** 객체를 포함해야 합니다.

```json
{
  "CellName": "A1",
  "Author": "string",
  "HtmlNote": "string",
  "Note": "string",
  "AutoSize": true,
  "IsVisible": true,
  "Width": 10,
  "Height": 10,
  "TextHorizontalAlignment": "Left",
  "TextOrientationType": "NoRotation",
  "TextVerticalAlignment": "Top"
}
```

**Comment 객체 필드**

| 필드                      | 타입      | 필수 여부 | 설명 |
|---------------------------|-----------|------------|-------------|
| `CellName`                | 문자열    | ✔️ | 셀 주소({`{cellName}` 경로 값과 일치해야 함). |
| `Author`                  | 문자열    | 선택 사항 | 코멘트 작성자 이름. |
| `HtmlNote`                | 문자열    | 선택 사항 | HTML 형식으로 서식화된 코멘트 텍스트. |
| `Note`                    | 문자열    | 선택 사항 | 일반 텍스트 코멘트. |
| `AutoSize`                | 불리언    | 선택 사항 | 코멘트 상자의 크기를 자동 조정. |
| `IsVisible`               | 불리언    | 선택 사항 | 기본적으로 코멘트 표시. |
| `Width` / `Height`        | 숫자      | 선택 사항 | 코멘트 상자의 크기(포인트 단위). |
| `TextHorizontalAlignment`| 문자열    | 선택 사항 | 가로 정렬(`Left`, `Center`, `Right`). |
| `TextOrientationType`     | 문자열    | 선택 사항 | 텍스트 회전(`NoRotation`, `Rotate90`, 등). |
| `TextVerticalAlignment`  | 문자열    | 선택 사항 | 세로 정렬(`Top`, `Center`, `Bottom`). |

---

## cURL 예제

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "A1",
        "Author": "test",
        "HtmlNote": "<font style=\"font-weight:bold;font-family:Tahoma;font-size:9pt;color:#000000;text-align:left;\">this is a comment</font>",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10,
        "TextHorizontalAlignment": "Left",
        "TextOrientationType": "NoRotation",
        "TextVerticalAlignment": "Top"
      }'
```

---

## 응답 스키마

| 필드      | 타입     | 설명 |
|-----------|----------|-------------|
| `Comment` | 객체     | 생성된 코멘트 객체(위의 **Comment 객체 필드** 참조, 링크 메타데이터 포함). |
| `Code`    | 정수     | API에서 반환된 HTTP 상태 코드(예: `200`). |
| `Status`  | 문자열   | 상태 메시지 텍스트(예: `"OK"`). |

`Comment` 객체는 **link** 하위 객체도 포함합니다:

| 하위 필드 | 타입     | 설명 |
|-----------|----------|-------------|
| `Href`    | 문자열   | 코멘트 리소스에 대한 자기 참조 URL. |
| `Rel`     | 문자열   | 관계 유형(`self`). |
| `Title`   | 문자열   | 선택적 제목(`null` 가능). |
| `Type`    | 문자열   | 선택적 MIME 유형(`null` 가능). |

---

## 성공 응답 예제

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "test",
    "HtmlNote": "<Font Style=\"FONT-WEIGHT: bold;FONT-FAMILY: Tahoma;FONT-SIZE: 9pt;COLOR: #000000;TEXT-ALIGN: left;\">this is a comment</Font>",
    "Note": "this is a comment",
    "AutoSize": true,
    "IsVisible": true,
    "Width": 10,
    "Height": 10,
    "TextHorizontalAlignment": "Left",
    "TextOrientationType": "NoRotation",
    "TextVerticalAlignment": "Top",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/comments/A1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## 오류 응답

| HTTP 코드 | 설명 | 예시 |
|-----------|-------------|---------|
| **400**   | 잘못된 요청 – 누락되거나 잘못된 매개변수. | `{ "Error": { "Code": "InvalidParameter", "Message": "The 'cellName' parameter is missing or malformed." }, "Code": 400, "Status": "Bad Request" }` |
| **401**   | 인증 실패 – 토큰 누락 또는 유효하지 않음. | `{ "Error": { "Code": "InvalidToken", "Message": "Authentication failed." }, "Code": 401, "Status": "Unauthorized" }` |
| **404**   | 없음 – 워크북, 워크시트 또는 셀이 존재하지 않음. | `{ "Error": { "Code": "FileNotFound", "Message": "Workbook 'test.xlsx' not found." }, "Code": 404, "Status": "Not Found" }` |
| **500**   | 내부 서버 오류 – 서버에서 예기치 않은 조건 발생. | `{ "Error": { "Code": "ServerError", "Message": "An unexpected error occurred." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## SDK 예제

다음 SDK는 이 작업을 위한 준비된 래퍼를 제공합니다. 자리 표시자 값(`<YOUR_TOKEN>`, `<FILE_NAME>` 등)을 실제 데이터로 바꾸세요.

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// API 클라이언트 구성
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// 코멘트 객체 준비
var comment = new Comment
{
    CellName = "A1",
    Author = "test",
    Note = "this is a comment",
    HtmlNote = "<font style=\"font-weight:bold;\">this is a comment</font>",
    AutoSize = true,
    IsVisible = true,
    Width = 10,
    Height = 10
};

try
{
    var response = apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, folder: null, storageName: null);
    Console.WriteLine(response);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.PutWorksheetComment: " + e.Message );
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.*;
import com.aspose.cells.cloud.model.*;

ApiClient client = new ApiClient();
client.setAppSid("<your_client_id>");
client.setAppKey("<your_client_secret>");

WorksheetsApi worksheetsApi = new WorksheetsApi(client);

Comment comment = new Comment()
        .cellName("A1")
        .author("test")
        .note("this is a comment")
        .htmlNote("<font style=\"font-weight:bold;\">this is a comment</font>")
        .autoSize(true)
        .isVisible(true)
        .width(10)
        .height(10);

try {
    CommentResponse resp = worksheetsApi.putWorksheetComment("test.xlsx", "Sheet1", "A1", comment, null, null);
    System.out.println(resp);
} catch (ApiException e) {
    e.printStackTrace();
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<your_client_id>');
$config->setAppKey('<your_client_secret>');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

$comment = new Aspose\Cells\Model\Comment([
    'CellName' => 'A1',
    'Author'   => 'test',
    'Note'     => 'this is a comment',
    'HtmlNote' => '<font style="font-weight:bold;">this is a comment</font>',
    'AutoSize' => true,
    'IsVisible'=> true,
    'Width'    => 10,
    'Height'   => 10
]);

try {
    $result = $apiInstance->putWorksheetComment('test.xlsx', 'Sheet1', 'A1', $comment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->putWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = AsposeCellsCloud::WorksheetsApi.new

comment = AsposeCellsCloud::Comment.new(
  cell_name: 'A1',
  author: 'test',
  note: 'this is a comment',
  html_note: '<font style="font-weight:bold;">this is a comment</font>',
  auto_size: true,
  is_visible: true,
  width: 10,
  height: 10
)

begin
  result = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
  puts result
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->put_worksheet_comment: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorksheetsApi, Configuration, Comment } = require('asposecellscloud');

let config = new Configuration();
config.clientId = '<your_client_id>';
config.clientSecret = '<your_client_secret>';

let api = new WorksheetsApi(config);

let comment = new Comment({
  CellName: 'A1',
  Author: 'test',
  Note: 'this is a comment',
  HtmlNote: '<font style="font-weight:bold;">this is a comment</font>',
  AutoSize: true,
  IsVisible: true,
  Width: 10,
  Height: 10
});

api.putWorksheetComment('test.xlsx', 'Sheet1', 'A1', comment)
  .then(response => console.log(response))
  .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.models import Comment

config = asposecellscloud.Configuration()
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = asposecellscloud.WorksheetsApi(asposecellscloud.ApiClient(config))

comment = Comment(
    CellName='A1',
    Author='test',
    Note='this is a comment',
    HtmlNote='<font style="font-weight:bold;">this is a comment</font>',
    AutoSize=True,
    IsVisible=True,
    Width=10,
    Height=10
)

try:
    api_response = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
    print(api_response)
except ApiException as e:
    print("Exception when calling WorksheetsApi->put_worksheet_comment: %s\\n" % e)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Object::Comment;

my $config = AsposeCellsCloud::Configuration->new(
    client_id     => '<your_client_id>',
    client_secret => '<your_client_secret>'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $comment = AsposeCellsCloud::Object::Comment->new(
    CellName => 'A1',
    Author   => 'test',
    Note     => 'this is a comment',
    HtmlNote => '<font style="font-weight:bold;">this is a comment</font>',
    AutoSize => 1,
    IsVisible=> 1,
    Width    => 10,
    Height   => 10
);

eval {
    my $result = $api_instance->put_worksheet_comment(
        name      => 'test.xlsx',
        sheet_name=> 'Sheet1',
        cell_name => 'A1',
        comment   => $comment
    );
    print $result;
};
if ($@) {
    warn "Exception when calling WorksheetsApi->put_worksheet_comment: $@";
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/model"
)

func main() {
    cfg := cellscloud.NewConfiguration()
    cfg.ClientId = "<your_client_id>"
    cfg.ClientSecret = "<your_client_secret>"

    apiInstance := api.NewWorksheetsApi(cfg)

    comment := model.Comment{
        CellName: "A1",
        Author:   "test",
        Note:     "this is a comment",
        HtmlNote: "<font style=\"font-weight:bold;\">this is a comment</font>",
        AutoSize: true,
        IsVisible: true,
        Width: 10,
        Height: 10,
    }

    resp, _, err := apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, nil, nil)
    if err != nil {
        fmt.Printf("Error: %v\\n", err)
    } else {
        fmt.Printf("Response: %+v\\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## 참조

* **워크시트 코멘트 조회** – `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **워크시트 코멘트 업데이트** – `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **워크시트 코멘트 삭제** – `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **모든 코멘트 지우기** – `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## 추가 참고 사항

* 엔드포인트 경로는 **v3.0**을 포함합니다. 최신 기능이 필요하다면 최신 버전(**v3.1**)을 사용해 기본 URL을 업데이트하세요.  
* 전체 OpenAPI 정의는 [Aspose.Cells Cloud API 참조](/cells/#/Worksheets/PutWorksheetComment)를 참조하세요.  
* API 가이드라인에 따라 속도 제한(HTTP 429)을 처리하고 재시도를 수행해야 합니다.  

---