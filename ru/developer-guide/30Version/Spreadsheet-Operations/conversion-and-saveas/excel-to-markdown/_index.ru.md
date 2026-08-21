---
title: "Конвертация Excel в Markdown"
second_title: "Документ"
linktype: "docs"
url: /convert-excel-file-to-markdown-file/
keywords: "Excel, Markdown, конвертация, Aspose.Cells Cloud, REST API, конвертация Excel в Markdown, Aspose Cells Markdown API, экспорт Excel в Markdown"
description: "Конвертируйте рабочие листы Excel в Markdown с помощью Aspose.Cells Cloud REST API — включает пример cURL, фрагменты кода SDK, необходимые параметры и данные аутентификации."
weight: 100
ArticleTitle: "Конвертация Excel в Markdown — Документация Aspose.Cells Cloud API"
---

Этот REST API преобразует файл электронной таблицы в файл формата Markdown.

## Безопасность и аутентификация
Aspose.Cells Cloud API защищены и требуют [аутентификации на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют [аутентификации на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Параметры запроса


| Имя параметра         | Тип    | Расположение | Описание                                                                                                |
| --------------------- | ------ | ------------ | ------------------------------------------------------------------------------------------------------- |
| password              | string | query        | Пароль, необходимый для открытия файла Excel.                                                          |
| storageName           | string | query        | Имя хранилища, в котором расположен файл.                                                              |
| checkExcelRestriction | bool   | query        | Указывает, следует ли применять ограничения, специфичные для Excel, при изменении ячеек или связанных объектов. |
| datafile              | file   | body         | Файл Excel, который необходимо загрузить в качестве первой части многокомпонентного содержимого.       |

### Ответ

API возвращает объект JSON типа **FileInfo**:

- **FileInfo** — объект, содержащий имя, размер и содержимое сгенерированного файла Markdown, закодированное в base64.

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

### Ответы об ошибках

| HTTP-код | Описание                                                         | Пример тела JSON                                |
| -------- | ---------------------------------------------------------------- | ----------------------------------------------- |
| 401      | Неавторизован — отсутствует или недействителен токен.           | `{"error":"Invalid access token."}`             |
| 400      | Неверный запрос — отсутствуют обязательные параметры или неверный формат файла. | `{"error":"The 'datafile' field is required."}` |
| 500      | Внутренняя ошибка сервера — непредвиденная проблема на сервере.  | `{"error":"An unexpected error occurred."}`     |



## Как использовать API PostConvertWorkbookToMarkdown с SDK

### Спецификация API PostConvertWorkbookToMarkdown

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) определяет публично доступное программное интерфейсное решение и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@your_excel_file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Другие API, реализующие эту функцию

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** — сохраняет файл Excel как HTML с дополнительными настройками и сохраняет результат.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** — конвертирует файл Excel в HTML с дополнительными параметрами и возвращает результат в ответе.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** — извлекает файл Excel и может конвертировать его в HTML с дополнительными настройками.
---