---
title: "Преобразование файла Excel в различные форматы"
ArticleTitle: "Преобразование файла Excel в различные форматы"
second_title: "Документ"
linktype: "Преобразование Excel"
type: docs
url: /ru/convert-an-excel-file-to-different-formats/
aliases:
  [
    /convert-excel-workbook-to-different-file-formats/,
    /convert/excel-to-different-formats/,
  ]
keywords: "Aspose.Cells Cloud, преобразование Excel, преобразование форматов файлов, REST API, SDK, CSV, PDF, HTML, JSON, Markdown"
description: "Преобразуйте рабочие книги Excel в такие форматы, как CSV, PDF, HTML, JSON, Markdown и другие, с использованием REST API Aspose.Cells Cloud."
weight: 10
---

Перед вызовом этого конечного ponto убедитесь, что вы получили действительный токен JWT и что исходная рабочая книга находится в поддерживаемом хранилище (например, Aspose Cloud Storage). Включите токен в заголовок `Authorization`, а при необходимости укажите параметр запроса `storageName`.

Этот REST API преобразует файл Excel в различные выходные форматы.

## API PutConvertWorkBook

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

Запрос представляет собой HTTP **PUT** с многочастным содержимым (см. [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) или [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Первая часть многочастного тела содержит **файл данных**, а вторая часть — **параметры сохранения**.

### Безопасность и аутентификация

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра           | Тип    | Описание                                                                                                                  |
| ----------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------- |
| `format`                | string | Целевой формат файла (например, CSV, XLS, HTML, PDF, XML, TXT, TIFF, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG и др.). |
| `password`              | string | Пароль, необходимый для открытия исходного файла Excel.                                                                  |
| `outPath`               | string | Полный путь (включая имя файла и расширение) для одного выходного файла или путь к папке при генерации нескольких файлов. |
| `storageName`           | string | Имя хранилища, в котором находится исходный файл.                                                                         |
| `checkExcelRestriction` | bool   | Если **true**, проверяет ограничения Excel перед изменением ячеек или связанных объектов.                                |
| `streamFormat`          | string | Формат входного потока файла.                                                                                             |
| `region`                | string | Региональные настройки, применяемые к рабочей книге.                                                                     |
| `pageWideFitOnPerSheet` | bool   | Регулирует ширину страницы под размер каждого листа при преобразовании в PDF.                                             |
| `pageTallFitOnPerSheet` | bool   | Регулирует высоту страницы под размер каждого листа при преобразовании в PDF.                                             |
| `sheetName`             | string | Имя листа для преобразования.                                                                                             |
| `pageIndex`             | string | Индекс страницы для преобразования (требуется `sheetName`).                                                               |
| `onePagePerSheet`       | bool   | Если **true**, генерирует по одной странице PDF на каждый лист.                                                           |
| `AutoRowsFit`           | bool   | Автоматически подгоняет все строки в рабочей книге.                                                                       |
| `AutoColumnsFit`        | bool   | Автоматически подгоняет ширину столбцов в рабочей книге.                                                                  |

### Параметры тела запроса

| Имя параметра | Тип       | Описание                                                   |
| ------------- | --------- | ---------------------------------------------------------- |
| `datafile`    | data file | Файл Excel, размещенный в первой части многочастного тела. |
| `SaveOptions` | object    | Параметры сохранения, размещенные во второй части тела.    |

### Ответ

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                                   |
|-----|-----------------------------|----------------------------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит сведения о выполненной операции.   |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий токен JWT.                             |
| 413 | Payload Too Large           | Загруженный файл превышает лимит размера.                                  |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                                             |

## Как использовать API PutConvertWorkBook с SDK

### Спецификация API PutConvertWorkBook

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) определяет открытый интерфейс, позволяющий выполнять прямые REST-взаимодействия из веб-браузера.

### Пример cURL

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Использование SDK Aspose.Cells Cloud

Использование SDK ускоряет разработку, позволяя сосредоточиться на бизнес-логике, поскольку низкоуровневые детали обрабатываются SDK. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}