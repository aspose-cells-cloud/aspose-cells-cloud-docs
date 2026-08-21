---
title: "템플릿 파일을 사용하여 Excel 워크북 만들기"
second_title: "문서"
linktitle: "템플릿 파일"
type: docs
url: /create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, 템플릿, API, Aspose.Cells, 워크북, REST, 클라우드"
description: "Aspose.Cells Cloud REST API를 사용하여 템플릿 파일에서 Excel 워크북을 생성하는 방법을 알아보세요. 필수 조건, 인증 단계, cURL 예제, 오류 처리 세부 정보 및 SDK 코드 스니펫이 포함됩니다."
weight: 30
---

# 템플릿 파일을 사용하여 Excel 워크북 만들기

기존 템플릿 파일과 선택적으로 스마트 마커(Smart-Marker) 값을 제공하는 데이터 파일을 사용하여 새로운 Excel 워크북을 생성합니다. 이 작업은 Aspose.Cells Cloud의 **PUT** `/cells/{name}` 엔드포인트를 통해 수행됩니다.

---

## 필수 조건

| 요구 사항 | 설명 |
|-----------|------|
| **Aspose.Cells Cloud 계정** | https://dashboard.aspose.cloud/에서 가입 후 **Client Id** / **Client Secret**을 발급받으세요. |
| **JWT 액세스 토큰** | [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)에 설명된 대로 JWT 토큰을 생성합니다. |
| **템플릿 파일** | 템플릿 Excel 파일(예: `Calendar.xlsx`)을 선택한 스토리지에 **Upload File** API 또는 UI를 통해 업로드합니다. |
| **데이터 파일 (선택 사항)** | 스마트 마커(Smart-Marker) 값을 포함하는 JSON 또는 XML 파일(예: `Sample_Data.xml`). |
| **지원되는 스토리지** | 기본 스토리지(`Default`) 또는 Aspose 계정에서 구성한 사용자 정의 스토리지. |

---

## 인증

Aspose.Cells Cloud의 모든 요청은 `Authorization` 헤더에 **Bearer JWT 토큰**을 포함해야 합니다:

```http
Authorization: Bearer {access_token}
```

이 토큰은 요청 전에 미리 획득해야 하며, 기본적으로 유효 기간은 1시간입니다.

---

## 요청

### HTTP 요청

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| 구성 요소 | 값 |
|-----------|-----|
| **메서드** | `PUT` |
| **경로**   | `/cells/{name}` – `name`은 생성할 워크북의 이름(확장자 포함, 예: `newworkbook.xlsx`)입니다. |
| **Content‑Type** | `multipart/form-data` (본문에 데이터 파일을 전송하는 경우). |
| **Accept** | `application/json` |

### 경로 매개변수

| 이름 | 유형 | 필수 여부 | 설명 |
|------|------|-----------|------|
| `name` | string | **예** | 생성할 워크북의 이름(예: `newworkbook.xlsx`). |

### 쿼리 매개변수

| 매개변수 | 유형 | 필수 여부 | 기본값 | 설명 |
|----------|------|-----------|--------|------|
| `templateFile` | string | 아니요 | — | 클라우드에 저장된 템플릿 파일의 이름. |
| `dataFile` | string | 아니요 | — | 클라우드에 저장된 데이터 파일(XML 또는 JSON)의 이름. |
| `isWriteOver` | boolean | 아니요 | `false` | 대상 파일이 이미 존재할 경우 덮어씁니다. `true` 또는 `false`를 따옴표 없이 전달합니다. |
| `folder` | string | 아니요 | — | 템플릿(및 선택적 데이터 파일)이 위치한 폴더 경로. |
| `storageName` | string | 아니요 | — | 파일을 포함하는 스토리지 서비스의 이름. |
| `checkExcelRestriction` | boolean | 아니요 | `true` | 생성 전에 워크북을 Excel 제한 사항에 따라 유효성 검사합니다. |

### 요청 본문 (선택 사항)

스마트 마커(Smart-Marker) 플레이스홀더에 대한 데이터를 요청 본문에 직접 전송할 경우, **`data`**라는 이름의 멀티파트 파일 파트로 포함합니다.

| 파트 이름 | 유형 | 설명 |
|-----------|------|------|
| `data` | file | 스마트 마커(Smart-Marker) 값을 포함하는 XML 또는 JSON 파일. |

#### 요청 본문을 포함한 cURL 예제

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*멀티파트 본문 대신 `dataFile` 쿼리 매개변수를 사용할 경우, `-F` 플래그를 생략합니다.*

---

## 응답

성공적인 호출은 **`200 OK`** 또는 새로운 파일이 생성된 경우 **`201 Created`** 상태 코드와 생성된 워크북에 대한 설명을 담은 JSON 페이로드를 반환합니다.

```json
{
    "Code": 200,
    "Status": "OK",
    "File": {
        "Name": "newworkbook.xlsx",
        "Size": 18234,
        "Path": "output/newworkbook.xlsx",
        "Url": "https://api.aspose.cloud/v3.0/storage/file/output/newworkbook.xlsx"
    }
}
```

### 응답 데이터 유형

| 속성 | 유형 | 설명 |
|------|------|------|
| `Code` | integer | API에서 반환된 HTTP 유사 상태 코드. |
| `Status` | string | 상태에 대한 텍스트 설명. |
| `File` | object | 생성된 워크북의 세부 정보. |
| `File.Name` | string | 생성된 워크북의 파일 이름. |
| `File.Size` | integer | 크기(바이트 단위). |
| `File.Path` | string | 스토리지 내 상대 경로. |
| `File.Url` | string | 직접 다운로드 URL(JWT 토큰 동일하게 필요). |

---

**HTTP 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200  | OK | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨. |
| 400  | 잘못된 요청 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | 인증되지 않음 | 잘못되거나 누락된 JWT 토큰. |
| 413  | 페이로드가 너무 큼 | 업로드된 파일이 크기 제한을 초과함. |
| 500  | 내부 서버 오류 | 예기치 않은 서버 오류. |
---

## SDK 예제

다음 스니펫은 공식 Aspose.Cells Cloud SDK를 사용하여 **PutWorkbookCreate**를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | 새 문서 이름.
var templateFile = "Calendar.xlsx"; // string | 템플릿 파일 이름.
var dataFile = "Sample_Data.xml"; // string | 데이터 파일 이름 (선택 사항).
var isWriteOver = true; // bool? | 존재할 경우 덮어쓰기.
var folder = "templates"; // string | 파일이 위치한 폴더.
var storageName = "MyStorage"; // string | 스토리지 이름.

using (var dataStream = File.OpenRead("Sample_Data.xml"))
{
    var response = apiInstance.PutWorkbookCreate(
        name,
        templateFile: templateFile,
        dataFile: dataFile,
        isWriteOver: isWriteOver,
        folder: folder,
        storageName: storageName,
        data: dataStream);
    Console.WriteLine(response);
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cloud.cells.api.WorkbookApi;
import com.aspose.cloud.cells.model.*;

import java.io.File;
import java.io.FileInputStream;

WorkbookApi api = new WorkbookApi();
String name = "newworkbook.xlsx";
String templateFile = "Calendar.xlsx";
String dataFile = "Sample_Data.xml";
Boolean isWriteOver = true;
String folder = "templates";
String storageName = "MyStorage";

FileInputStream dataStream = new FileInputStream(new File("Sample_Data.xml"));
CellsCloudResponse response = api.putWorkbookCreate(
        name,
        templateFile,
        dataFile,
        isWriteOver,
        folder,
        storageName,
        dataStream);
System.out.println(response);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once('vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorkbookApi;
use Aspose\Cells\Cloud\Configuration;

$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new WorkbookApi(null, $config);
$name = "newworkbook.xlsx";
$templateFile = "Calendar.xlsx";
$dataFile = "Sample_Data.xml";
$isWriteOver = true;
$folder = "templates";
$storageName = "MyStorage";

$data = fopen("Sample_Data.xml", "r");
$result = $apiInstance->putWorkbookCreate($name, $templateFile, $dataFile, $isWriteOver, $folder, $storageName, $data);
print_r($result);
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::WorkbookApi.new
api.config.access_token = '{access_token}'

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = true
folder = 'templates'
storage_name = 'MyStorage'

File.open('Sample_Data.xml', 'rb') do |data|
  response = api.put_workbook_create(name,
                                     template_file: template_file,
                                     data_file: data_file,
                                     is_write_over: is_write_over,
                                     folder: folder,
                                     storage_name: storage_name,
                                     data: data)
  puts response
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorkbookApi, Configuration } = require('asposecellscloud');
const fs = require('fs');

let config = new Configuration();
config.accessToken = '{access_token}';
config.basePath = 'https://api.aspose.cloud';

let apiInstance = new WorkbookApi(config);

let name = 'newworkbook.xlsx';
let templateFile = 'Calendar.xlsx';
let dataFile = 'Sample_Data.xml';
let isWriteOver = true;
let folder = 'templates';
let storageName = 'MyStorage';

let data = fs.createReadStream('Sample_Data.xml');

apiInstance.putWorkbookCreate(name, templateFile, dataFile, isWriteOver, folder, storageName, data)
    .then(response => console.log(response))
    .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.apis import WorkbookApi
from asposecellscloud.models import CellsCloudResponse

config = asposecellscloud.Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api_instance = WorkbookApi(asposecellscloud.ApiClient(config))

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = True
folder = 'templates'
storage_name = 'MyStorage'

with open('Sample_Data.xml', 'rb') as data:
    response = api_instance.put_workbook_create(
        name,
        template_file=template_file,
        data_file=data_file,
        is_write_over=is_write_over,
        folder=folder,
        storage_name=storage_name,
        data=data)
    print(response)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorkbookApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '{access_token}';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::Api::WorkbookApi->new($config);

my $name = 'newworkbook.xlsx';
my $template_file = 'Calendar.xlsx';
my $data_file = 'Sample_Data.xml';
my $is_write_over = 1;
my $folder = 'templates';
my $storage_name = 'MyStorage';

open my $fh, '<:raw', 'Sample_Data.xml' or die $!;
my $response = $api_instance->put_workbook_create(
    name => $name,
    template_file => $template_file,
    data_file => $data_file,
    is_write_over => $is_write_over,
    folder => $folder,
    storage_name => $storage_name,
    data => $fh);
print $response;
close $fh;
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "os"

    asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorkbookApi(cfg)

    name := "newworkbook.xlsx"
    templateFile := "Calendar.xlsx"
    dataFile := "Sample_Data.xml"
    isWriteOver := true
    folder := "templates"
    storageName := "MyStorage"

    data, _ := os.Open("Sample_Data.xml")
    defer data.Close()

    result, _, err := apiInstance.PutWorkbookCreate(name, &templateFile, &dataFile, &isWriteOver, &folder, &storageName, data)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Printf("Response: %+v\n", result)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## 오류 처리

| 상태 코드 | 상황 | 권장 조치 |
|-----------|------|-----------|
| **400** | 필수 매개변수 누락 또는 잘못된 파일 유형. | 쿼리 매개변수를 확인하고, 템플릿 및 데이터 파일이 존재하고 지원되는 형식(`.xlsx`, `.xml`, `.json`)인지 확인하세요. |
| **401** | JWT 토큰이 누락, 만료되거나 잘못된 형식입니다. | Client Id/Secret을 사용하여 새 액세스 토큰을 재생성하세요. |
| **413** | 업로드된 파일이 서비스 크기 제한(기본값 50MB)을 초과합니다. | 파일 크기를 줄이거나 워크북을 더 작은 부분으로 분할하세요. |
| **500** | 예기치 않은 서버 오류. | 잠시 후 다시 시도하고, 문제가 지속되면 `Request‑Id` 헤더 값을 포함하여 Aspose 지원팀에 문의하세요. |

---

## 참조

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – 기존 워크북을 지정된 형식으로 저장합니다.  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – 워크북 정보를 조회하거나 파일을 다운로드합니다.  
- **[Upload File API](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – 템플릿 또는 데이터 파일을 클라우드 스토리지에 업로드합니다.  

---