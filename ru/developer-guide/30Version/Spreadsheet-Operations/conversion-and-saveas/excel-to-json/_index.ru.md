---
title: "Excel в JSON"
second_title: "Документ"
linktitle: "Excel в JSON"
type: docs
url: /ru/convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel в JSON, облачный API, конвертация электронных таблиц, REST API"
description: "Узнайте, как конвертировать электронные таблицы Excel в файлы JSON с помощью облачного REST API Aspose.Cells. Включает пример cURL, фрагменты кода SDK (C#, Java, Python), необходимые параметры, аутентификацию и формат ответа."
weight: 100
ArticleTitle: "Преобразование Excel в JSON с помощью Aspose.Cells Cloud API — Краткое руководство"
---


## REST API

Этот REST API преобразует файл электронной таблицы в файл формата JSON.  


```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### Безопасность и аутентификация

API облачной платформы Aspose.Cells являются безопасными и требуют [аутентификации на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Запрос

**Параметры запроса (query parameters)**

| Имя параметра          | Тип   | Описание                                                                |
| ---------------------- | ----- | ----------------------------------------------------------------------- |
| `password`             | string | Пароль, необходимый для открытия файла Excel (необязательный).          |
| `storageName`          | string | Имя хранилища, в котором расположен файл (необязательный).              |
| `checkExcelRestriction`| bool   | Включает ограничения, специфичные для Excel, при изменении ячеек (необязательный). |

**Параметр тела запроса**

| Имя параметра | Тип | Описание                                                                                        |
| ------------- | --- | ----------------------------------------------------------------------------------------------- |
| `datafile`    | file | Файл Excel, который необходимо загрузить. Должен быть отправлен как первая часть запроса `multipart/form-data`. |

#### Пример вызова с помощью cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### Ответ

Сервис возвращает объект **FileInfo**. Основные поля описаны ниже:

| Поле          | Тип    | Описание                                                                   |
| ------------- | ------ | -------------------------------------------------------------------------- |
| `Filename`    | string | Имя созданного JSON-файла (например, `myWorkbook.json`).                   |
| `FileSize`    | integer| Размер созданного файла в байтах.                                          |
| `FileContent` | string | Содержимое JSON-файла, закодированное в Base64. Раскодируйте, чтобы получить исходный JSON. |

**Пример ответа**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (base64 строка) ..."
}
```

#### Обработка ошибок

В случае ошибки API возвращает объект ошибки со следующей структурой:

| Поле      | Тип   | Описание                                  |
| --------- | ----- | ----------------------------------------- |
| `Code`    | string| Машинно-читаемый идентификатор ошибки.    |
| `Message` | string| Человеко-читаемое описание ошибки.        |

Типичные HTTP-коды статуса:

- **400** – Неверный запрос (например, отсутствует файл, неверные параметры).
- **401** – Неавторизованный доступ (недействительный или отсутствующий токен доступа).
- **500** – Внутренняя ошибка сервера.

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                               |
|------|-----------------------------|--------------------------------------------------------|
| 200  | OK                          | Фильтр успешно применён; ответ содержит данные о операции. |
| 400  | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Недействительный или отсутствующий JWT-токен.         |
| 413  | Payload Too Large           | Загруженный файл превышает допустимый размер.          |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера.                         |
## Как использовать API PostConvertWorkbookToJson с SDK

### Спецификация API PostConvertWorkbookToJson

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson" rel="noopener noreferrer" title="Спецификация Aspose.Cells OpenAPI – Преобразование рабочей книги в JSON">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия прямо из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (base64 строка)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK облачной платформы Aspose.Cells

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах вашего проекта. Ознакомьтесь с полным списком SDK облачной платформы Aspose.Cells в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="SDK облачной платформы Aspose.Cells на GitHub">репозитории на GitHub</a>.

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Другие API, реализующие аналогичный функционал

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Сохраняет файл Excel как файл HTML с дополнительными настройками и сохраняет результат в указанном хранилище.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Преобразует файл Excel в файл HTML с дополнительными настройками и возвращает результат в ответе.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Получает файл Excel; может использоваться с параметрами запроса для получения файла в формате HTML.
---