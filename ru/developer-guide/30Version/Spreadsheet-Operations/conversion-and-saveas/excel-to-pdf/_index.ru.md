---
title: "Преобразование Excel в PDF — Aspose.Cells Cloud API"
ArticleTitle: "Преобразование Excel в PDF — Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Преобразование Excel в PDF"
type: docs
url: /ru/convert-excel-file-to-pdf-file/
aliases: [  /ru/convert-excel-file-to-pdf-in-cloud/ , /ru/convert/excel-to-pdf/ ]
keywords: "Aspose, Cells, Excel, PDF, преобразование, Cloud API"
description: "Узнайте, как преобразовать рабочие книги Excel в PDF с помощью REST API Aspose.Cells Cloud. Включает примеры cURL, SDK (C#, Java, Python) и руководство по аутентификации."
weight: 80
---

Этот REST API преобразует файл электронной таблицы в файл формата PDF. **Необходимые условия:** получите действительный JWT-токен доступа, убедитесь, что исходный файл Excel хранится в поддерживаемом хранилище, и обладайте соответствующими правами для вызова конечной точки преобразования.

## API PostConvertWorkbookToPDF

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### **Параметр запроса (query parameter)**

| Имя параметра         | Тип    | Описание                                                                 |
| :-------------------- | :----- | :------------------------------------------------------------------------ |
| password              | string | Пароль для открытия файла Excel.                                         |
| storageName           | string | Имя хранилища, в котором находится файл.                                 |
| checkExcelRestriction | bool   | Следует ли применять ограничения файлов Excel при изменении объектов, связанных с ячейками. |

Если параметр `checkExcelRestriction` опущен, по умолчанию он принимает значение `false`.

### **Параметр тела запроса**

| Имя параметра | Тип  | Описание                                                    |
| :------------ | :--- | :----------------------------------------------------------- |
| datafile      | file | Файл данных, сохраняемый в качестве первой части мультитекстового содержимого. |

### **Ответ**

[FileInfo](/cells/file-info/)

В ответе возвращается объект JSON с метаданными файла. Сам файл PDF можно загрузить, используя предоставленное поле `FileContent` (base64) или по ссылке из `FileInfo`. API возвращает объект JSON типа **FileInfo**:

- **FileInfo** — объект, содержащий имя, размер и содержимое сгенерированного файла **PDF** в кодировке base64.

```json
{
  "Filename": "example.pdf",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                  |
|------|-----------------------------|-----------------------------------------------------------|
| 200  | OK                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400  | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Недействительный или отсутствующий JWT-токен.            |
| 413  | Payload Too Large           | Загруженный файл превышает лимит размера.                 |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера.                            |

## Как использовать API PostConvertWorkbookToPDF с SDK

### Спецификация API PostConvertWorkbookToPDF

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

**Заголовки запроса**

| Заголовок      | Тип    | Описание                                                |
| :------------- | :----- | :------------------------------------------------------- |
| Authorization  | string | Bearer-токен, полученный при аутентификации через JWT.  |
| Content-Type   | string | Должен быть `multipart/form-data` для загрузки файла.  |
| Accept         | string | `application/json` для получения метаданных ответа.     |

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Включите токен доступа в заголовок `Authorization`, затем выполните запрос ниже.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}


### Использование SDK Aspose.Cells Cloud

Использование SDK упрощает разработку, скрывая низкоуровневые детали. Полный список SDK Aspose.Cells Cloud представлен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызовы веб-сервисов Aspose.Cells с использованием различных SDK:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Другие API, реализующие эту функцию

| **API**        | **Тип** | **Описание**                                                     | **Ссылка Swagger**                                                                          |
| :------------- | :------ | :--------------------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| /cells/convert | PUT     | Преобразует рабочую книгу из содержимого запроса в указанный формат. | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

API [POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) позволяет сохранить файл MS Excel в формате PDF с дополнительными настройками и сохранить результат в хранилище.

Этот REST API преобразует файл Excel в PDF.

API [PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) позволяет преобразовать файл MS Excel в PDF с дополнительными настройками и вернуть результат в ответе.

API [GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) позволяет преобразовать файл MS Excel в PDF с дополнительными настройками и вернуть результат в ответе.

Эти API — [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) и [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) — определяют публично доступный программный интерфейс и позволяют выполнять REST-взаимодействия непосредственно из веб-браузера.

Дополнительные варианты преобразования доступны на странице [Параметры сохранения](/cells/save-options/).