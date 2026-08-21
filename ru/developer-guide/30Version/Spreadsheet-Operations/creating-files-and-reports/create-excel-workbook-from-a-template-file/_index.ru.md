---
title: "Как создать рабочую книгу Excel с использованием файла шаблона"
second_title: "Документ"
linktitle: "Файл шаблона"
type: docs
url: /create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, шаблон, API, Aspose.Cells, рабочая книга, REST, облако"
description: "Узнайте, как создавать рабочие книги Excel из файлов шаблонов с помощью Aspose.Cells Cloud REST API. Включает предварительные требования, шаги аутентификации, примеры cURL, информацию об обработке ошибок и фрагменты кода SDK."
weight: 30
---

# Как создать рабочую книгу Excel с использованием файла шаблона

Создайте новую рабочую книгу Excel, используя существующий файл шаблона и, при необходимости, файл данных, содержащий значения маркеров умной подстановки. Операция выполняется через конечную точку **PUT** `/cells/{name}` Aspose.Cells Cloud.

---

## Предварительные требования

| Требование | Описание |
|-------------|-------------|
| **Аккаунт Aspose.Cells Cloud** | Зарегистрируйтесь на https://dashboard.aspose.cloud/ и получите **Client Id** / **Client Secret**. |
| **JWT-токен доступа** | Сгенерируйте JWT-токен, как описано в [руководстве по аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Файл шаблона** | Загрузите шаблонный файл Excel (например, `Calendar.xlsx`) в выбранное вами хранилище с помощью API **Upload File** или через интерфейс. |
| **Файл данных (необязательно)** | Файл JSON или XML, содержащий значения маркеров умной подстановки (например, `Sample_Data.xml`). |
| **Поддерживаемое хранилище** | Хранилище по умолчанию (`Default`) или настраиваемое хранилище, настроенное в вашем аккаунте Aspose. |

---

## Аутентификация

Все запросы Aspose.Cells Cloud требуют передачи **Bearer JWT-токена** в заголовке `Authorization`:

```http
Authorization: Bearer {access_token}
```

Токен должен быть получен заранее и по умолчанию действителен в течение 1 часа.

---

## Запрос

### HTTP-запрос

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| Компонент | Значение |
|-----------|-------|
| **Метод** | `PUT` |
| **Путь**   | `/cells/{name}` — `name` — желаемое имя создаваемой рабочей книги (включая расширение, например `newworkbook.xlsx`). |
| **Content‑Type** | `multipart/form-data` (при отправке файла данных в теле запроса). |
| **Accept** | `application/json` |

### Параметр пути

| Имя | Тип | Обязательный | Описание |
|------|------|----------|-------------|
| `name` | строка | **Да** | Имя создаваемой рабочей книги (например, `newworkbook.xlsx`). |

### Параметры запроса

| Параметр | Тип | Обязательный | По умолчанию | Описание |
|-----------|------|----------|---------|-------------|
| `templateFile` | строка | Нет | — | Имя файла шаблона, хранящегося в облаке. |
| `dataFile` | строка | Нет | — | Имя файла данных (XML или JSON), хранящегося в облаке. |
| `isWriteOver` | логическое значение | Нет | `false` | Перезаписать целевой файл, если он уже существует. Передавайте `true` или `false` **без** кавычек. |
| `folder` | строка | Нет | — | Путь к папке, где находится шаблон (и необязательный файл данных). |
| `storageName` | строка | Нет | — | Имя сервиса хранилища, содержащего файлы. |
| `checkExcelRestriction` | логическое значение | Нет | `true` | Проверить соответствие рабочей книги ограничениям Excel перед созданием. |

### Тело запроса (необязательно)

Если данные для заполнителей маркеров умной подстановки отправляются непосредственно в запросе, включите их как часть multipart-файла с именем **`data`**.

| Имя части | Тип | Описание |
|-----------|------|-------------|
| `data` | файл | Файл XML или JSON, содержащий значения маркеров умной подстановки. |

#### Пример cURL с телом запроса

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*Если используется параметр запроса `dataFile` вместо multipart-тела, опустите флаг `-F`.*

---

## Ответ

Успешный вызов возвращает **`200 OK`** (или **`201 Created`**, когда создаётся новый файл) с JSON-полезной нагрузкой, описывающей созданную рабочую книгу.

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

### Типы данных ответа

| Свойство | Тип | Описание |
|----------|------|-------------|
| `Code` | целое число | HTTP-подобный код статуса, возвращаемый API. |
| `Status` | строка | Текстовое описание статуса. |
| `File` | объект | Детали сгенерированной рабочей книги. |
| `File.Name` | строка | Имя файла созданной рабочей книги. |
| `File.Size` | целое число | Размер в байтах. |
| `File.Path` | строка | Относительный путь в хранилище. |
| `File.Url` | строка | Прямая ссылка для скачивания (требует тот же JWT-токен). |

---

**Коды HTTP-статусов**

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400  | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Неверный или отсутствующий JWT-токен. |
| 413  | Payload Too Large           | Загруженный файл превышает лимит размера. |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера. |
---

## Примеры SDK

Следующие фрагменты кода демонстрируют вызов **PutWorkbookCreate** с использованием официальных SDK Aspose.Cells Cloud.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | Имя нового документа.
var templateFile = "Calendar.xlsx"; // string | Имя файла шаблона.
var dataFile = "Sample_Data.xml"; // string | Имя файла данных (необязательно).
var isWriteOver = true; // bool? | Перезаписать, если существует.
var folder = "templates"; // string | Папка, в которой находятся файлы.
var storageName = "MyStorage"; // string | Имя хранилища.

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

## Обработка ошибок

| Код статуса | Ситуация | Рекомендуемое действие |
|-------------|-----------|--------------------|
| **400** | Отсутствуют обязательные параметры или указан недопустимый тип файла. | Проверьте параметры запроса, убедитесь, что файлы шаблона и данных существуют и поддерживаются (`.xlsx`, `.xml`, `.json`). |
| **401** | JWT-токен отсутствует, истёк или некорректен. | Сгенерируйте новый токен доступа с использованием Client Id/Secret. |
| **413** | Загруженный файл превышает лимит размера сервиса (по умолчанию 50 МБ). | Уменьшите размер файла или разделите рабочую книгу на более мелкие части. |
| **500** | Непредвиденная ошибка сервера. | Повторите запрос через короткий промежуток времени; если проблема сохраняется, свяжитесь с поддержкой Aspose, указав значение заголовка `Request‑Id`. |

---

## См. также

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – Сохранить существующую рабочую книгу в заданном формате.  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – Получить информацию о рабочей книге или скачать файл.  
- **[API Upload File](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – Загрузить файлы шаблона или данных в облачное хранилище.  

---