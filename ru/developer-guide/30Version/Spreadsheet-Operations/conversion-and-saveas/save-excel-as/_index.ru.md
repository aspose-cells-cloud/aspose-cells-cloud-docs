---
title: "Сохранение рабочей книги Excel – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Сохранить как"
type: docs
url: /save-an-excel-file-as-other-formats-files/
aliases:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, Сохранить как, PDF, CSV, JSON, Markdown, REST API"
description: "Сохраняйте рабочие книги Excel в форматы PDF, CSV, JSON, Markdown и другие с помощью Aspose.Cells Cloud REST API."
weight: 30
---

Этот REST API позволяет **сохранить** файл Excel в различных форматах.  
Перед вызовом этого конечного пункта убедитесь, что у вас есть действительный токен доступа OAuth 2.0 и что исходная рабочая книга хранится в вашем облачном хранилище Aspose.

**Необходимые условия**  
1. Получите JWT-токен доступа и включите его в заголовок `Authorization: Bearer <token>` каждого запроса.  
2. Загрузите исходную рабочую книгу в облачное хранилище Aspose (или подтвердите её существование).  
3. Знайте имя хранилища и путь к папке, в которой находится рабочая книга.

## API PostWorkbookSaveAs

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### **Параметр пути**

| Имя параметра | Тип   | Описание                     |
| ------------- | ----- | ---------------------------- |
| name          | string | Имя файла Excel.             |

### **Параметр запроса**

| Имя параметра         | Тип    | Описание                                                                              |
| --------------------- | ------ | ------------------------------------------------------------------------------------- |
| newfilename           | string | Новое имя файла сохраняемого документа.                                               |
| isAutoFitRows         | string | Если `true`, автоматически подстраивает высоту всех строк в рабочей книге. По умолчанию — `false`. |
| isAutoFitColumns      | string | Если `true`, автоматически подстраивает ширину столбцов в рабочей книге. По умолчанию — `false`. |
| folder                | string | Папка, содержащая исходную рабочую книгу.                                             |
| storageName           | string | Имя хранилища, в котором находится исходный файл.                                      |
| outStorageName        | string | Имя хранилища, в котором будет сохранён выходной файл.                                |
| checkExcelRestriction | bool   | Указывает, следует ли применять ограничения Excel при изменении ячеек или связанных объектов. |
| region                | string | Региональные настройки, применяемые к рабочей книге.                                  |
| pageWideFitOnPerSheet | bool   | Подгонять ширину страницы под каждую рабочую лист при преобразовании.                  |
| pageTallFitOnPerSheet | bool   | Подгонять высоту страницы под каждую рабочую лист при преобразовании.                  |
| sheetName             | string | Имя рабочего листа для преобразования.                                                 |
| pageIndex             | string | Индекс страницы для преобразования в указанном рабочем листе (требуется `sheetName`).  |
| onePagePerSheet       | bool   | При преобразовании в PDF генерировать по одной странице на рабочий лист.              |

### **Параметр тела запроса**

| Имя параметра | Тип    | Описание                                                   |
| ------------- | ------ | ---------------------------------------------------------- |
| SaveOptions   | Object | Параметры сохранения, передаваемые во второй части multipart-запроса. |

**Пример тела запроса (JSON-часть multipart-запроса)**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### Ответ

API возвращает объект `SaveResponse`.

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK                          | Фильтр применён успешно; ответ содержит детали операции.                |
| 400 | Bad Request                 | Отсутствуют или неверны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Неверный или отсутствующий JWT-токен.                                   |
| 413 | Payload Too Large           | Загруженный файл превышает лимит размера.                               |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                                           |

## Как использовать API PostWorkbookSaveAs с SDK

### Спецификация API PostWorkbookSaveAs

[OpenAPI-спецификация](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать **cURL** для простого доступа к веб-сервисам Aspose.Cells. В приведённом ниже примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <ваш_jwt_токен>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах проекта. Ознакомьтесь со списком всех SDK Aspose.Cells Cloud в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории GitHub</a>.

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

Для других сценариев преобразования см. руководства [Преобразование Excel в PDF](/convert-excel-to-pdf/) и [Экспорт Excel в CSV](/export-excel-to-csv/).