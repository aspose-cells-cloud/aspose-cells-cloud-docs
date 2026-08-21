---
title: "Экспорт рабочей книги"
second_title: "Документ"
linktitle: "Рабочая книга"
type: docs
url: /ru/export-excel-to-different-formats/
aliases: [  /ru/export/excel-to-different-formats/ ]
keywords: "Aspose.Cells Cloud, экспорт Excel, конвертация рабочей книги, PDF, CSV, JSON, форматы изображений, API электронных таблиц, XLSX, ODS, PNG"
description: "Пошаговое руководство по экспорту рабочих книг Excel в различные форматы — включая PDF, CSV, JSON и различные типы изображений — с использованием REST API и SDK Aspose.Cells Cloud."
weight: 20
---

Вы можете экспортировать рабочие книги в следующие форматы: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.


### Параметры запроса

| Имя параметра | Тип    | Путь/Строка запроса/HTTP-тело | Обязательный | Описание |
|---------------|--------|-------------------------------|-------------|----------|
| file          | file   | formData                      | Да          | Файл для загрузки |
| objectType    | string | query                         | Да          | Тип экспортируемого объекта. Для экспорта диаграммы используйте `chart`. Другие возможные значения: `worksheet`, `picture` и т.д. |
| format        | string | query                         | Да          | Желаемый выходной формат. Поддерживаемые значения: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |


### **Ответ**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx.tif",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx.tif",
      "FileSize": 348126,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**Коды HTTP-статуса**

| Код | Значение                | Описание |
|-----|-------------------------|----------|
| 200 | OK (OK)                 | Элементы успешно экспортированы; в ответе содержится список файлов. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры. |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий токен доступа. |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |


## Как использовать API PostExport с SDK

### Спецификация API PostExport


[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) определяет публично доступный программный интерфейс, позволяющий выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать инструмент командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как вызвать облачный API с помощью cURL.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=workbook&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Использование SDK Aspose.Cells Cloud

Использование SDK ускоряет разработку, позволяя сосредоточиться на бизнес-логике, поскольку низкоуровневые детали обрабатываются автоматически. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервиса Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExport.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExport.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExport.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExport.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExport.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExport.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExport.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExport.go" >}}

{{< /tab >}}

{{< /tabs >}}