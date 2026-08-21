---
title: Конвертирование Excel в HTML  
description: Конвертирование рабочей книги Excel в файл HTML с использованием Aspose.Cells Cloud API v3.0.  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# Конвертирование Excel в HTML  

Aspose.Cells Cloud предоставляет надёжный REST-интерфейс для преобразования рабочей книги Excel (XLS, XLSX, CSV и др.) в HTML-документ. В результате операции возвращается объект **FileInfo**, содержащий сгенерированный HTML-файл (имя, размер и содержимое в формате Base64).

---

## Необходимые условия

| Требование | Как выполнить |
|------------|---------------|
| **Аккаунт Aspose Cloud** | Зарегистрируйтесь на [aspose.cloud](https://www.aspose.cloud). |
| **JWT-токен доступа** | Получите токен типа «bearer» через OAuth 2.0 endpoint `POST /connect/token`. |
| **Хранилище (необязательно)** | Если вы хотите, чтобы API читал/записывал файлы в конкретном хранилище, создайте его заранее (например, Amazon S3, Azure Blob или хранилище Aspose Cloud). |
| **cURL / SDK** | Любой HTTP-клиент, поддерживающий формат multipart/form-data (cURL, Postman или одно из SDK Aspose.Cells). |

---

## Аутентификация

Все запросы к Aspose.Cells Cloud требуют **аутентификации по JWT-токену**.

```http
Authorization: Bearer <access-token>
```

Токен должен быть указан в заголовке `Authorization` каждого запроса.

---

## Конечная точка

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **Примечание** — Запрос должен быть отправлен как `multipart/form-data`. Файл Excel должен быть первым элементом multipart-тела запроса.

---

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по JWT-токену</a>.

## Параметры запроса  

### Параметры строки запроса  

| Имя                      | Тип     | Обязательный | Значение по умолчанию | Описание |
|--------------------------|---------|--------------|------------------------|----------|
| `password`               | string  | Нет          | —                      | Пароль для открытия защищённой рабочей книги. |
| `storageName`            | string  | Нет          | —                      | Имя хранилища, в котором находится исходный файл. |
| `checkExcelRestriction` | boolean | Нет          | `true`                 | Если `true`, сервис проверяет ограничения, специфичные для Excel (например, защищённые листы). |
| `region`                 | string  | Нет          | —                      | Региональные настройки рабочей книги (например, `ru-RU`). |
| `FontsLocation`          | string  | Нет          | —                      | URL-адрес или путь к папке, содержащей пользовательские шрифты, необходимые для рендеринга. |

### Форм-данные (multipart)  

| Имя  | Тип  | Обязательный | Описание |
|------|------|--------------|----------|
| **File** | file | **Да** | Рабочая книга Excel, подлежащая преобразованию. Должна быть передана как первый элемент multipart-запроса. |

---

## Пример запроса (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/your_workbook.xlsx"
```

---

## Успешный ответ  

**Код состояния:** `200 OK`

| Поле         | Тип    | Описание |
|--------------|--------|----------|
| `Filename`   | string | Имя сгенерированного HTML-файла (например, `example.html`). |
| `FileSize`   | int    | Размер HTML-файла в байтах. |
| `FileContent`| string | Содержимое HTML в кодировке Base64. |

```json
{
  "Filename": "example.html",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

Схема ответа определяется моделью **FileInfo**: [/cells/file-info](/cells/file-info/).

---

## Ответы об ошибках  

| Код | Описание ошибки | Пример полезной нагрузки |
|-----|------------------|---------------------------|
| `400` | Неверный запрос — отсутствуют/некорректные параметры | ```json { "Code": "BadRequest", "Message": "Часть 'File' является обязательной." } ``` |
| `401` | Неавторизован — неверный или отсутствующий JWT-токен | ```json { "Code": "InvalidToken", "Message": "Токен доступа отсутствует или просрочен." } ``` |
| `404` | Не найдено — исходный файл не найден в указанном хранилище | ```json { "Code": "FileNotFound", "Message": "Файл 'my.xlsx' не существует в хранилище 'MyStorage'." } ``` |
| `413` | Перегрузка полезной нагрузки — размер загруженного файла превышает допустимый лимит | ```json { "Code": "RequestEntityTooLarge", "Message": "Размер загруженного файла превышает лимит в 100 МБ." } ``` |
| `429` | Слишком много запросов — превышен лимит частоты запросов | ```json { "Code": "TooManyRequests", "Message": "Лимит частоты — 60 вызовов в минуту — превышен." } ``` |
| `500` | Внутренняя ошибка сервера — непредвиденное состояние сервера | ```json { "Code": "InternalError", "Message": "Произошла непредвиденная ошибка. Повторите попытку позже." } ``` |

---

## Ограничения частоты запросов  

| Ограничение | Описание |
|-------------|----------|
| **60 запросов в минуту** на аккаунт (по умолчанию) | Превышение лимита возвращает `429 Too Many Requests`. Измените логику клиента или запросите более высокий лимит через портал Aspose Cloud. |

---

## Поддержка SDK  

Aspose предоставляет официальные SDK для нескольких языков программирования, оборачивающих данный endpoint. Ниже приведены примеры, иллюстрирующие ту же операцию конвертации с использованием официальных SDK.

| Язык | Пример |
|------|--------|
| C#   | <details><summary>Показать пример</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("your.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java | <details><summary>Показать пример</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("your.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python | <details><summary>Показать пример</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js | <details><summary>Показать пример</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('your.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go | <details><summary>Показать пример</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("your.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP | <details><summary>Показать пример</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby | <details><summary>Показать пример</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl | <details><summary>Показать пример</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

Полный список поддерживаемых SDK и инструкции по установке см. в репозитории **Aspose.Cells Cloud SDKs**: <https://github.com/aspose-cells-cloud>.

---

## См. также: другие endpoint’ы  

| Endpoint | Описание |
|----------|----------|
| `POST /cells/{name}/saveAs` | Сохранить существующий файл Excel как HTML (или другой формат) непосредственно в хранилище. |
| `PUT /cells/convert` | Конвертировать рабочую книгу в HTML с дополнительными опциями конвертации; результат возвращается в теле ответа. |
| `GET /cells/{name}` | Получить уже сохранённую в хранилище рабочую книгу в формате HTML (или другом формате), с возможностью указания дополнительных параметров запроса. |

---

## Часто задаваемые вопросы  

**В:** *Как выполнить аутентификацию при вызове API конвертации Excel в HTML?*  
**О:** Укажите заголовок `Authorization: Bearer <access-token>`, полученный с OAuth 2.0 endpoint `/connect/token`.

**В:** *Что содержит ответ `FileInfo`?*  
**О:** Три поля: `Filename` (строка), `FileSize` (целое число, байты), и `FileContent` (HTML-содержимое в кодировке Base64).

**В:** *Какие коды ошибок могут возникнуть?*  
**О:** `400` (Неверный запрос), `401` (Неавторизован), `404` (Файл не найден), `413` (Перегрузка полезной нагрузки), `429` (Слишком много запросов), `500` (Внутренняя ошибка сервера). Каждый ответ содержит JSON-объект с полями `Code` и `Message`.

**В:** *Могу ли я указать собственное расположение шрифтов?*  
**О:** Да. Используйте параметр строки запроса `FontsLocation`, чтобы указать путь к папке или URL-адрес, где находятся требуемые шрифты.

**В:** *Есть ли ограничение частоты вызовов для этой операции?*  
**О:** По умолчанию — **60 вызовов в минуту** на аккаунт. Превышение лимита возвращает `429 Too Many Requests`.

---

## JSON‑LD навигационная цепочка (структурированные данные)

Добавление этого блока улучшит SEO, позволяя поисковым системам отображать расширенные навигационные цепочки (rich snippets).

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Главная", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "Разработчикам", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "Конвертация", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel в HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## Журнал изменений  

| Версия | Дата | Изменения |
|--------|------|-----------|
| **v3.0** | 2024‑10‑01 | Первый публичный выпуск `PostConvertWorkbookToHtml`. |
| **v3.1** | 2025‑04‑15 | Добавлены параметры строки запроса `region` и `FontsLocation`; обновлён формат полезной нагрузки ошибок. |
| **v3.2** | 2026‑03‑20 | Добавлена документация по ограничению частоты запросов и примеры ответов об ошибках. |

--- 

*Для получения дополнительной помощи обращайтесь в службу поддержки Aspose или посетите официальную справку по API:* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---