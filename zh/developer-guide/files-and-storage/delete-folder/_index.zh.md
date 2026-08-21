---
title: "删除文件夹 – Aspose.Cells Cloud API | 通过 REST 删除文件夹"
description: "了解如何使用 DELETE /v4.0/cells/storage/folder/{path} 端点从 Aspose.Cells Cloud 存储中删除文件夹（可选地递归删除）。包含请求语法、参数、身份验证、示例代码和错误处理。"
keywords: "Aspose.Cells, 删除文件夹, 云存储, API, REST, Excel, 文件管理"
slug: delete-folder
date: 2026-07-30
---

# 删除文件夹 – Aspose.Cells Cloud API

从 Aspose.Cells Cloud 存储中删除一个文件夹（可选地连同其全部内容）。

---

## 概述

**删除文件夹** 操作会永久性地从 Aspose.Cells Cloud 使用的存储账户中移除一个文件夹。  
您可以删除空文件夹，或通过将 `recursive` 标志设为 `true` 来删除该文件夹及其包含的所有文件和子文件夹。此端点常用于清理脚本、自动化工作流，或在临时目录不再需要时进行清理。

---

## HTTP 请求

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – 要删除的文件夹的完整路径（需 URL 编码）。

### 必需的 HTTP 请求头

| 请求头            | 值                                 | 描述                                  |
|-------------------|------------------------------------|---------------------------------------|
| `Authorization`   | `Bearer {access_token}`            | 从身份验证服务获取的 JWT 令牌。        |
| `Accept`          | `application/json`                | 期望的响应格式。                      |
| `Content-Type`    | `application/json` *（可选）*     | DELETE 请求不需要，但可发送。         |

---

## 身份验证

Aspose.Cells Cloud 使用 **基于 JWT 令牌的身份验证**。  
请通过 [身份验证端点](/authentication/) 获取访问令牌，并按上述方式将其包含在 `Authorization` 请求头中。

```bash
-H "Authorization: Bearer {access_token}"
```

---

## 参数

| 名称            | 类型      | 位置   | 是否必需 | 描述                                                                 |
|-----------------|-----------|--------|----------|----------------------------------------------------------------------|
| `path`          | 字符串    | 路径   | 是       | 要删除的文件夹路径（需 URL 编码）。                                   |
| `storageName`   | 字符串    | 查询参数 | 否       | 包含该文件夹的存储名称；若省略，则使用默认存储。                     |
| `recursive`     | 布尔值    | 查询参数 | 否       | `true` → 删除该文件夹 **及其中所有内容**；默认为 `false`。           |

**示例查询字符串**

```
?storageName=MyStorage&recursive=true
```

---

## 请求示例（cURL）

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## 响应

成功请求将返回 **HTTP 200 OK**，响应体为一个空的 JSON 对象：

```json
{}
```

由于该操作结果是二元的（文件夹被成功删除或返回错误），因此不提供额外的响应体。

---

**HTTP 状态码**

| 状态码 | 含义           | 描述                                     |
|--------|----------------|------------------------------------------|
| 200    | OK（成功）     | 操作已成功执行；响应包含操作详情。        |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | 无效或缺失 JWT 令牌。                    |
| 413    | Payload Too Large（请求体过大） | 上传文件超出大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                  |

发生错误时，响应体将包含一个带有 `code` 和 `message` 字段的 JSON 对象，用于描述问题详情。

---

## SDK 代码示例

以下示例展示了如何使用官方支持的 SDK 调用 **删除文件夹** 功能。请将 `{access_token}` 和参数值替换为您自己的。

<details><summary>🟦 C# (.NET)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// 配置 API 客户端
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// 递归删除文件夹
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

// 初始化 API 客户端
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

// 配置
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// 递归删除文件夹
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

## 参考链接

- **[创建文件夹](/create-folder/)** – 在云存储中新建一个文件夹。  
- **[复制文件夹](/copy-folder/)** – 复制一个文件夹及其全部内容。  
- **[移动文件夹](/move-folder/)** – 将文件夹移动至另一路径。  
- **[OpenAPI 规范]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">DeleteFolder 操作</a>（交互式 API 浏览器）。

---

## SEO 与可访问性检查清单（内部使用）

- **标题与 H1** 使用正确的短破折号（`–`）并包含核心关键词 *删除文件夹*。  
- 所有标题均遵循合理的层级结构（`H1 → H2 → H3`）。  
- 无 UTF‑8 编码残留错误。  
- 元关键词已整合为单一、简洁的列表（或按需省略）。  
- 外部链接均包含 `rel="noopener noreferrer"` 以增强安全性。  
- 页面中如出现 UI 图标或语言标志，应添加 `aria-label`/`alt` 属性（例如：`aria-label="English (US)"`）。  
- 建议在各语言版本页面的 `<head>` 中添加 `<link rel="alternate" hreflang="xx" href="…">` 标签。  

---