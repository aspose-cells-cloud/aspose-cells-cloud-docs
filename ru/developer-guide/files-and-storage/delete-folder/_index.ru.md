---
---
title: "Удаление папки – Aspose.Cells Cloud API | Удаление папок через REST"
description: "Узнайте, как удалить папку (опционально — рекурсивно) из облачного хранилища Aspose.Cells Cloud с помощью конечной точки DELETE /v4.0/cells/storage/folder/{path}. Включает синтаксис запроса, параметры, аутентификацию, примеры кода и обработку ошибок."
keywords: "Aspose.Cells, удаление папки, облачное хранилище, API, REST, Excel, управление файлами"
slug: delete-folder
date: 2026-07-30
---

# Удаление папки – Aspose.Cells Cloud API

Удаление папки (а при необходимости — всех её содержимых файлов и подпапок) из облачного хранилища Aspose.Cells Cloud.

---

## Обзор

Операция **Delete Folder** (Удалить папку) окончательно удаляет папку из учётной записи хранилища, используемой Aspose.Cells Cloud.  
Вы можете удалить пустую папку или, установив параметр `recursive` в значение `true`, удалить папку вместе со всеми содержащимися в ней файлами и подпапками. Эта конечная точка обычно используется в скриптах очистки, автоматизированных рабочих процессах или при необходимости удаления временных каталогов.

---

## HTTP-запрос

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* — полный путь к удаляемой папке (в URL-кодировке).

### Обязательные HTTP-заголовки

| Заголовок         | Значение                           | Описание                                       |
|-------------------|------------------------------------|------------------------------------------------|
| `Authorization`   | `Bearer {access_token}`            | JWT-токен, полученный из службы аутентификации. |
| `Accept`          | `application/json`                | Ожидаемый формат ответа.                      |
| `Content-Type`    | `application/json` *(необязательно)* | Не требуется для DELETE, но может быть отправлен. |

---

## Аутентификация

Aspose.Cells Cloud использует **аутентификацию на основе JWT-токенов**.  
Получите токен доступа через [конечную точку аутентификации](/authentication/) и включите его в заголовок `Authorization`, как показано выше.

```bash
-H "Authorization: Bearer {access_token}"
```

---

## Параметры

| Имя           | Тип     | Расположение | Обязательный | Описание                                                                 |
|---------------|---------|--------------|-------------|--------------------------------------------------------------------------|
| `path`        | строка  | Путь         | Да          | Путь к удаляемой папке (в URL-кодировке).                               |
| `storageName` | строка  | Параметр запроса | Нет      | Имя хранилища, содержащего папку. Если не указано, используется хранилище по умолчанию. |
| `recursive`   | логическое значение | Параметр запроса | Нет | `true` → удалить папку **вместе со всем её содержимым**. По умолчанию — `false`. |

**Пример строки запроса**

```
?storageName=MyStorage&recursive=true
```

---

## Пример запроса (cURL)

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Ответ

При успешном выполнении возвращается **HTTP 200 OK** с пустым JSON-объектом:

```json
{}
```

Дополнительные данные в теле ответа не возвращаются, так как результат операции бинарен — папка либо удалена, либо возвращена ошибка.

---

**Коды HTTP-статусов**

| Код  | Значение                    | Описание                                              |
|------|-----------------------------|-------------------------------------------------------|
| 200  | OK (ОК)                     | Фильтр применён успешно; ответ содержит данные об операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или неверны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.                |
| 413  | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает допустимый размер. |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

При возникновении ошибки в теле ответа содержится JSON-объект с полями `code` и `message`, описывающими проблему.

---

## Примеры кода SDK

В следующих примерах показано, как вызвать операцию **Delete Folder** с использованием официально поддерживаемых SDK. Замените `{access_token}` и значения параметров своими данными.

<details><summary>🟦 C# (dotnet)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Настройка клиента API
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// Удаление папки (рекурсивно)
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

// Инициализация клиента API
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

// Настройка
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// Удаление папки рекурсивно
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

## См. также

- **[Создать папку](/create-folder/)** – создать новую папку в облачном хранилище.  
- **[Копировать папку](/copy-folder/)** – дублировать папку и её содержимое.  
- **[Переместить папку](/move-folder/)** – переместить папку по другому пути.  
- **[Спецификация OpenAPI]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">DeleteFolder (операция удаления папки)</a> (интерактивный исследователь API).

---

## Контрольный список SEO и доступности (внутренний)

- **Заголовок и H1** используют правильное тире (`–`) и содержат основной ключевой запрос *Удаление папки*.  
- Все заголовки следуют логической иерархии (`H1 → H2 → H3`).  
- В тексте отсутствуют артефакты неправильной кодировки UTF-8.  
- Мета-ключевые слова объединены в один чёткий список (или опущены по желанию).  
- Внешние ссылки содержат `rel="noopener noreferrer"` для обеспечения безопасности.  
- Иконки интерфейса и языковые флаги (если отображаются на странице) должны иметь атрибуты `aria-label`/`alt` (например, `aria-label="English (US)"`).  
- В `<head>` страницы рекомендуется добавлять теги `<link rel="alternate" hreflang="xx" href="…">` для каждой языковой версии.