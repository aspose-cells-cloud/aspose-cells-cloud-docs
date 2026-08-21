---
title: "Экспорт диаграммы Excel"
second_title: "Документ"
linktype: docs
url: /ru/export-excel-chart-to-different-formats/
aliases: [  /ru/export/excel-chart-to-different-formats/ ]
description: "Экспортируйте объекты диаграмм Excel в популярные форматы, такие как PNG, JPEG, PDF, SVG, TIFF, EMF, WMF и другие, с использованием REST API или SDK Aspose.Cells Cloud. Включает аутентификацию, пример cURL и примеры кода на различных языках."
keywords: "Aspose.Cells, экспорт диаграммы, экспорт диаграммы Excel, REST API, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, форматы диаграмм, Aspose Cells Cloud"
weight: 20
ArticleTitle: "Экспорт диаграммы Excel – Документ"
---

Экспорт объектов диаграмм из рабочей книги Excel в различные форматы изображений и документов — распространённая задача при создании отчётов и публикации контента. Aspose.Cells Cloud предоставляет простой REST-эндпоинт для прямого преобразования диаграмм в популярные форматы, такие как PNG, JPEG, PDF, SVG, TIFF, EMF, WMF и другие.

Вы можете экспортировать диаграммы в следующие форматы: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/), и [PDF](https://docs.fileformat.com/pdf/).

**Необходимые условия:**  
- Действующая учётная запись Aspose.Cells Cloud с активной подпиской.  
- OAuth 2.0 Bearer-токен (JWT), полученный в процессе аутентификации.  
- Файл рабочей книги для загрузки (максимальный размер — менее 50 МБ).  

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Название параметра | Тип   | Путь / строка запроса / тело HTTP-запроса | Обязательный | Описание                                                                                                                     |
|-------------------|--------|--------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------|
| file              | файл   | formData                                   | Да          | Файл для загрузки                                                                                                            |
| objectType        | строка | query                                      | Да          | Тип экспортируемого объекта. Для экспорта диаграмм используйте `chart`. Другие возможные значения: `worksheet`, `picture` и т.д. |
| format            | строка | query                                      | Да          | Желаемый выходной формат. Поддерживаемые значения: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`.           |

### **Ответ**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK (OK)                     | Фильтр успешно применён; ответ содержит детали операции.                |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.                           |
| 413 | Payload Too Large (Слишком большой payload) | Загружаемый файл превышает лимит размера.                              |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                          |

## Как использовать API PostExport с SDK

### Спецификация API PostExport

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Все запросы должны содержать действующий OAuth 2.0 Bearer-токен в заголовке `Authorization`. Пример ниже демонстрирует вызов API с помощью **cURL** и загрузку рабочей книги с использованием multipart/form‑data.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}