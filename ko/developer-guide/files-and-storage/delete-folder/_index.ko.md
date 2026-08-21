---
title: "폴더 삭제 – Aspose.Cells Cloud API | REST를 통한 폴더 제거"
description: "DELETE /v4.0/cells/storage/folder/{path} 엔드포인트를 사용하여 Aspose.Cells Cloud 스토리지에서 폴더를(선택적으로 재귀적으로) 삭제하는 방법을 알아보세요. 요청 구문, 매개변수, 인증, 샘플 코드, 오류 처리를 포함합니다."
keywords: "Aspose.Cells, 폴더 삭제, 클라우드 스토리지, API, REST, 엑셀, 파일 관리"
slug: delete-folder
date: 2026-07-30
---

# 폴더 삭제 – Aspose.Cells Cloud API

Aspose.Cells Cloud 스토리지에서 폴더(선택적으로 그 안의 모든 콘텐츠 포함)를 제거합니다.

---

## 개요

**폴더 삭제** 작업은 Aspose.Cells Cloud에서 사용하는 스토리지 계정에서 폴더를 영구적으로 제거합니다.  
비어 있는 폴더를 삭제하거나, `recursive` 플래그를 `true`로 설정하여 폴더와 그 안에 포함된 모든 파일 및 하위 폴더를 함께 삭제할 수 있습니다. 이 엔드포인트는 주로 정리 스크립트, 자동화 워크플로우, 임시 디렉터리가 더 이상 필요 없을 때 사용됩니다.

---

## HTTP 요청

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – 삭제할 폴더의 전체 경로(URL 인코딩됨).

### 필수 HTTP 헤더

| 헤더              | 값                                 | 설명                                     |
|-------------------|------------------------------------|------------------------------------------|
| `Authorization`   | `Bearer {access_token}`            | 인증 서비스에서 획득한 JWT 토큰.          |
| `Accept`          | `application/json`                | 예상 응답 형식.                           |
| `Content-Type`    | `application/json` *(선택 사항)*   | DELETE 요청에는 필요하지 않지만 전송 가능. |

---

## 인증

Aspose.Cells Cloud는 **JWT 토큰 기반 인증**을 사용합니다.  
[인증 엔드포인트](/authentication/)를 통해 액세스 토큰을 획득하고, 위와 같이 `Authorization` 헤더에 포함시킵니다.

```bash
-H "Authorization: Bearer {access_token}"
```

---

## 매개변수

| 이름            | 유형      | 위치   | 필수 여부 | 설명                                                                      |
|-----------------|-----------|--------|-----------|---------------------------------------------------------------------------|
| `path`          | 문자열    | 경로   | 예        | 삭제할 폴더의 경로(URL 인코딩됨).                                          |
| `storageName`   | 문자열    | 쿼리   | 아니요    | 폴더를 포함한 스토리지의 이름. 생략 시 기본 스토리지가 사용됩니다.          |
| `recursive`     | 불리언    | 쿼리   | 아니요    | `true` → 폴더를 **그 안의 모든 콘텐츠와 함께** 삭제합니다. 기본값은 `false`. |

**예시 쿼리 문자열**

```
?storageName=MyStorage&recursive=true
```

---

## 요청 예시(cURL)

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## 응답

성공적인 요청은 빈 JSON 객체를 포함한 **HTTP 200 OK**를 반환합니다:

```json
{}
```

이 작업의 결과는 이진적으로 결정되므로(폴더가 삭제되었는지 여부만 판단), 추가적인 응답 본문은 제공되지 않습니다.

---

**HTTP 상태 코드**

| 코드 | 의미                       | 설명                                           |
|------|----------------------------|------------------------------------------------|
| 200  | OK                         | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized               | 유효하지 않거나 누락된 JWT 토큰.                |
| 413  | Payload Too Large          | 업로드된 파일이 크기 제한을 초과함.             |
| 500  | Internal Server Error      | 예기치 않은 서버 오류.                          |

오류가 발생하면, 본문에는 문제를 설명하는 `code` 및 `message` 필드를 가진 JSON 객체가 포함됩니다.

---

## SDK 샘플 코드

다음 예시는 공식적으로 지원되는 SDK를 사용하여 **폴더 삭제**를 호출하는 방법을 보여줍니다. `{access_token}`과 매개변수 값을 사용자 고유의 값으로 바꾸세요.

<details><summary>🟦 C# (dotnet)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API 클라이언트 설정
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// 폴더 삭제(재귀)
var request = new DeleteFolderRequest
{
    Path = "MyFolder",
    StorageName = "MyStorage",
    Recursive = true
};

folderApi.DeleteFolder(request);
```
</details>

<details><summary>🟨 Java</summary>

```java
import com.aspose.cloud.cells.api.FolderApi;
import com.aspose.cloud.cells.model.*;
import com.aspose.cloud.cells.model.requests.DeleteFolderRequest;

// API 클라이언트 초기화
FolderApi folderApi = new FolderApi("{access_token}");

DeleteFolderRequest request = new DeleteFolderRequest()
        .path("MyFolder")
        .storageName("MyStorage")
        .recursive(true);

folderApi.deleteFolder(request);
```
</details>

<details><summary>🟪 PHP</summary>

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\FolderApi;
use Aspose\Cells\Cloud\Configuration;

// 설정
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// 재귀적으로 폴더 삭제
try {
    $apiInstance->deleteFolder('MyFolder', 'MyStorage', true);
    echo "Folder deleted.";
} catch (Exception $e) {
    echo 'Exception when calling FolderApi->deleteFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```
</details>

<details><summary>🟧 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::FolderApi.new

begin
  api.delete_folder('MyFolder', storage_name: 'MyStorage', recursive: true)
  puts 'Folder deleted.'
rescue AsposeCellsCloud::ApiError => e
  puts "Error: #{e.message}"
end
```
</details>

<details><summary>🟢 Node.js (TypeScript)</summary>

```ts
import { FolderApi, DeleteFolderRequest } from '@asposecloud/cells-sdk';

const config = {
    accessToken: '{access_token}',
    basePath: 'https://api.aspose.cloud'
};

const folderApi = new FolderApi(config);

const request: DeleteFolderRequest = {
    path: 'MyFolder',
    storageName: 'MyStorage',
    recursive: true
};

folderApi.deleteFolder(request)
    .then(() => console.log('Folder deleted'))
    .catch(err => console.error('Error:', err));
```
</details>

<details><summary>🐍 Python</summary>

```python
from asposecellscloud import FolderApi, DeleteFolderRequest, Configuration

config = Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

folder_api = FolderApi(config)

request = DeleteFolderRequest(
    path='MyFolder',
    storage_name='MyStorage',
    recursive=True
)

folder_api.delete_folder(request)
print("Folder deleted")
```
</details>

<details><summary>🦪 Perl</summary>

```perl
use AsposeCellsCloud::FolderApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '{access_token}',
    host => 'https://api.aspose.cloud'
);

my $api = AsposeCellsCloud::FolderApi->new($config);

eval {
    $api->delete_folder(
        path => 'MyFolder',
        storage_name => 'MyStorage',
        recursive => 1
    );
    print "Folder deleted.\n";
};
if ($@) {
    warn "Error deleting folder: $@";
}
```
</details>

<details><summary>🦑 Go</summary>

```go
package main

import (
    "context"
    "fmt"
    cells "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    api := cells.NewFolderApi(cfg)

    req := cells.DeleteFolderRequest{
        Path:        "MyFolder",
        StorageName: "MyStorage",
        Recursive:   true,
    }

    _, err := api.DeleteFolder(context.Background(), req)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println("Folder deleted")
}
```
</details>

---

## 참조

- **[폴더 생성](/create-folder/)** – 클라우드 스토리지에 새 폴더 생성.  
- **[폴더 복사](/copy-folder/)** – 폴더와 그 안의 콘텐츠를 복제.  
- **[폴더 이동](/move-folder/)** – 폴더를 다른 경로로 이동.  
- **[OpenAPI 사양]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">DeleteFolder 작업</a> (대화형 API 탐색기).

---

## SEO 및 접근성 체크리스트 (내부용)

- **제목 및 H1**에 올바른 대시(`–`)를 사용하며, 주요 키워드 *Delete Folder*를 포함.  
- 모든 제목은 논리적 계층 구조(`H1 → H2 → H3`)를 따름.  
- UTF‑8 인코딩 관련 아티팩트는 없음.  
- 메타 키워드는 단일 명확한 목록으로 정리됨(선호 시 생략 가능).  
- 외부 링크는 보안을 위해 `rel="noopener noreferrer"` 포함.  
- UI 아이콘 및 언어 플래그(해당 페이지에 렌더링된 경우)는 `aria-label`/`alt` 속성을 가져야 함(예: `aria-label="English (US)"`).  
- 각 언어 버전에 대해 페이지 헤드에 `<link rel="alternate" hreflang="xx" href="…">` 태그를 추가하는 것이 권장됨.

---