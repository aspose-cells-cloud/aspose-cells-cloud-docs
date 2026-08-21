---
title: "Объединение совпадающих таблиц в удалённой папке"
description: "Объединение файлов электронных таблиц, хранящихся в облачном хранилище Aspose Cloud, в один файл. Поддерживается более 30 выходных форматов: PDF, CSV, JSON, XLSX, ODS, XPS и другие."
keywords: "Aspose.Cells, объединение таблиц, удалённая папка, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /merge-spreadsheets-in-remote-folder/
---

Объединение нескольких файлов электронных таблиц, расположенных в удалённой папке облачного хранилища Aspose Cloud, в один выходной файл. Операция выполняется полностью в облаке, исключая необходимость загрузки исходных файлов локально. Поддерживается более 30 выходных форматов (PDF, CSV, JSON, XLSX, ODS, XPS и др.).

## API MergeSpreadsheetsInRemoteFolder

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются защищёнными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса <a id="request-parameters"></a>

| Имя                     | Тип     | Расположение | Обязательный | Описание                                                                                                      |
| ----------------------- | ------- | ------------ | ------------ | ------------------------------------------------------------------------------------------------------------- |
| **folder**              | string  | query        | **Да**       | Папка облачного хранилища, содержащая исходные таблицы.                                                      |
| **fileMatchExpression** | string  | query        | **Да**       | Шаблон для выбора файлов (например, `*отчёт*.xlsx`). Поддерживаются подстановочные знаки `*` и `?`.           |
| **outFormat**           | string  | query        | **Да**       | Желаемый выходной формат (`PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS` и др.).                                 |
| **mergeInOneSheet**     | boolean | query        | **Да**       | `true` — все данные объединяются в одну рабочую таблицу. `false` — каждый исходный файл получает свою таблицу. |
| **storageName**         | string  | query        | Нет          | Имя пользовательского хранилища; по умолчанию используется основное хранилище.                               |
| **outPath**             | string  | query        | Нет          | Папка назначения для объединённого файла. Если не указано, файл сохраняется в исходной папке.                 |
| **outStorageName**      | string  | query        | Нет          | Имя хранилища, в которое будет записан объединённый файл.                                                    |
| **fontsLocation**       | string  | query        | Нет          | Путь к папке с пользовательскими шрифтами (требуется для экспорта в PDF/изображения).                         |
| **region**              | string  | query        | Нет          | Локаль для форматирования чисел, дат и валют (например, `ru-RU`, `de-DE`).                                    |
| **password**            | string  | query        | Нет          | Пароль для открытия защищённых исходных таблиц.                                                              |

## Пример запроса (cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### **Ответ**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

Файл можно загрузить непосредственно по ссылке `FileUrl` или сохранить в папке, указанной в `outPath`.

**Детали успешного ответа**

| Код статуса | Content‑Type               | Описание                               |
| ----------- | -------------------------- | -------------------------------------- |
| 200 OK      | `application/octet-stream` | Бинарный поток объединённого файла.    |
| 202 Accepted| `application/json`         | JSON, содержащий `FileUrl`, `FileName` и др. |

**Коды HTTP-статусов**

| Код | Значение                | Описание                                               |
| --- | ----------------------- | ------------------------------------------------------ |
| 200 | OK                      | Фильтр применён успешно; ответ содержит детали операции. |
| 400 | Bad Request             | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized            | Недействительный или отсутствующий JWT-токен.         |
| 413 | Payload Too Large       | Размер загружаемого файла превышает предельно допустимый. |
| 500 | Internal Server Error   | Непредвиденная ошибка сервера.                         |

## Как использовать API объединения таблиц с помощью SDK

### Спецификация OpenAPI

Спецификация <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">OpenAPI</a> предоставляет машинно-читаемое описание API, позволяющее напрямую взаимодействовать через REST.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример показывает, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки, поскольку он абстрагирует низкоуровневые детали и позволяет сократить код для импорта данных в рабочую таблицу. Ознакомьтесь с полным списком SDK Aspose.Cells Cloud в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.
---