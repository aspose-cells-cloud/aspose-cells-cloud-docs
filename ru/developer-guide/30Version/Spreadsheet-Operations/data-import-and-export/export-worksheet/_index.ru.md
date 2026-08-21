---
title: "Экспорт рабочего листа – Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Рабочий лист"
type: docs
url: /export-excel-worksheet-to-different-formats/
aliases: [/export/excel-worksheet-to-different-formats/]
keywords: "Aspose.Cells, экспорт рабочего листа, Excel API, PDF, CSV, TIFF, ODS, форматы изображений"
description: "Узнайте, как экспортировать рабочий лист Excel в форматы PDF, CSV, TIFF и другие с помощью REST API Aspose.Cells Cloud. Пример cURL, необходимая аутентификация, детали параметров и обработка ответов."
weight: 20
ArticleTitle: "Экспорт рабочего листа Excel в различные форматы – Aspose.Cells Cloud"
---

Вы можете экспортировать рабочий лист в следующие форматы:

- **XLS** – [Сведения о формате XLS](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [Сведения о формате XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [Сведения о формате XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [Сведения о формате CSV](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [Сведения о формате TSV](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [Сведения о формате XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [Сведения о формате ODS](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [Сведения о формате TXT](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [Сведения о формате PDF](https://docs.fileformat.com/pdf/)
- **OTS** – [Сведения о формате OTS](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [Сведения о формате XPS](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [Сведения о формате DIF](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [Сведения о формате PNG](https://docs.fileformat.com/Image/png/)
- **JPEG** – [Сведения о формате JPEG](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [Сведения о формате BMP](https://docs.fileformat.com/image/bmp/)
- **SVG** – [Сведения о формате SVG](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [Сведения о формате TIFF](https://docs.fileformat.com/image/tiff/)
- **EMF** – [Сведения о формате EMF](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [Сведения о формате Numbers](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [Сведения о формате FODS](https://docs.fileformat.com/spreadsheet/fods/)

[Ознакомьтесь с другими операциями экспорта, например, экспортом всей книги или диаграммы.](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## API PostExport

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип    | Путь/Строка запроса/HTTP-тело | Обязательный | Описание                                                                 |
|---------------|--------|-------------------------------|-------------|--------------------------------------------------------------------------|
| file          | file   | formData                      | Да          | Файл для загрузки                                                        |
| objectType    | string | query                         | Да          | Тип объекта для экспорта. Для экспорта диаграммы используйте `chart`. Другие возможные значения: `worksheet`, `picture` и т.д. |
| format        | string | query                         | Да          | Желаемый выходной формат. Поддерживаемые значения: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### Ответ

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet3.tif",
      "FileSize": 2824,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4.tif",
      "FileSize": 1350,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet5.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet7.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet4.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### **Обработка ошибок**

В случае ошибки запроса API возвращает объект JSON с ошибкой, содержащий поля, такие как `Code` и `Message`. Типичные HTTP-коды состояния включают **401 Unauthorized** (отсутствующий или недействительный токен) и **400 Bad Request** (некорректные параметры).

**HTTP-коды состояния**

| Код | Значение                    | Описание                                                  |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | OK (OK)                     | Фильтр успешно применён; ответ содержит данные операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствующие или некорректные параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.                     |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает ограничение по размеру.        |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                            |

**Примечания**

- Максимальный размер файла для загрузки: 50 МБ.  
- API поддерживает экспорт нескольких рабочих листов в одном запросе; каждый рабочий лист возвращается как отдельный файл в массиве `Files`.  
- Для больших книг доступна асинхронная обработка; используйте ответ `202 Accepted` для опроса статуса операции.

## Как использовать API PostExport с SDK

### Предварительные требования

Перед вызовом API получите действительный JWT-токен доступа, используя процесс аутентификации Aspose.Cells Cloud. Убедитесь, что токен включён в заголовок `Authorization` каждого запроса. SDK автоматически обрабатывают получение токена при настройке с вашими учётными данными клиента.

### Спецификация API PostExport

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия напрямую из веб-браузера.

Вы можете использовать инструмент командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует вызов Cloud API с помощью cURL.

```bash
# Экспорт рабочего листа в формат TIFF
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки под Aspose.Cells Cloud. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список поддерживаемых SDK доступен на [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}