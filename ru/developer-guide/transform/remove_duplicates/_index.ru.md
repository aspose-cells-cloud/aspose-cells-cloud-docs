---
title: "Удаление дубликатов"
ArticleTitle: "Удаление дубликатов – Aspose.Cells Cloud API"
second_title: "Документ"
linktype: "Удаление дубликатов"
type: docs
url: /ru/cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, Удаление дубликатов, API"
description: "Удаляет повторяющиеся значения в листе, диапазоне или таблице."
weight: 1000
---

## Удаление дубликатов в веб-сервисах Aspose.Cells Cloud

Удаляет повторяющиеся значения в листе, диапазоне или таблице. Данный метод сканирует целевой диапазон на предмет строк с одинаковыми значениями в указанных столбцах для проверки. Для каждой группы дубликатов удаляются все вхождения, кроме первого. Сравнение, как правило, чувствительно к регистру и производится по точному значению ячейки.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра | Тип   | Путь/Строка запроса/Тело HTTP-запроса | Описание |
|---------------|--------|----------------------------------------|----------|
| Spreadsheet   | Файл   | FormData                               | Загрузка файла электронной таблицы. |
| worksheet     | Строка | Параметр запроса                        | Имя листа. (необязательно) |
| range         | Строка | Параметр запроса                        | Имя диапазона, из которого нужно удалить дубликаты. (необязательно) |
| table         | Строка | Параметр запроса                        | Имя таблицы, из которой нужно удалить дубликаты. (необязательно) |
| outPath       | Строка | Параметр запроса                        | (Необязательно) Путь к папке, где сохраняется рабочая книга. По умолчанию — null. |
| outStorageName| Строка | Параметр запроса                        | Имя хранилища для выходного файла. |
| region        | Строка | Параметр запроса                        | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от региона. |
| password      | Строка | Параметр запроса                        | Пароль для открытия файла электронной таблицы. |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| ------------- | --- | -------- |
| [TBD]         | [TBD] | [TBD] |

### **Ответ**

```json
{
  "File": "двоичный поток результирующей электронной таблицы (например, .xlsx)"
}
```

**Коды состояния ответа**

| Код | Значение | Описание |
|-----|----------|----------|
| 200 | OK | Возвращается результирующая электронная таблица без дубликатов в виде потока файла. |
| 400 | Bad Request | Недопустимые параметры запроса или некорректный URL. |
| 401 | Unauthorized | Аутентификация не удалась или учетные данные не предоставлены. |
| 413 | Payload Too Large | Размер загруженного файла превышает допустимый лимит. |
| 500 | Internal Server Error | Произошла ошибка при получении данных из электронной таблицы или другая ошибка на стороне сервера. |

## Как использовать функцию удаления дубликатов с SDK

### Спецификация API удаления дубликатов

[Спецификация API удаления дубликатов](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Приведенный ниже пример демонстрирует, как выполнять вызовы Cloud API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}
{< tab tabNum="1" >}
```bash
# Используйте HTTPS для безопасного соединения
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Sheet1&range=A1:C10&table=MyTable&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "двоичный поток результирующей электронной таблицы (например, .xlsx)"
}
```
{< /tab >}
{< /tabs >}

### Использование SDK Aspose Cells Cloud

Использование SDK — самый быстрый способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Ознакомьтесь с полным списком SDK Aspose.Cells Cloud в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

Приведенные ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose Cells Cloud с использованием различных SDK:

```csharp
// Пример кода SDK для C#
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "en-US",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// Пример кода SDK для Java
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "en-US",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# Пример кода SDK для Python
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='en-US',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Исключение при вызове TransformApi->remove_duplicates: %s\\n" % e)
```

`[TBD]`
---