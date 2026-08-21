---
title: "Aspose.Cells Cloud – Преобразование рабочей книги Excel в PDF, CSV, HTML и другие форматы (GET /cells/{name})"
second_title: "Документ"
linktitle: "Преобразование Excel"
type: docs
url: /ru/get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, преобразование Excel, преобразовать Excel, PDF, CSV, HTML, ODS, JSON, форматы изображений, экспорт таблиц, API, REST"
description: "Узнайте, как получить рабочую книгу Excel в любом формате (PDF, CSV, HTML, PNG и др.) с помощью REST API Aspose.Cells Cloud. Приведены примеры cURL и SDK, информация об аутентификации и ответах."
weight: 10
ArticleTitle: "Aspose.Cells Cloud – Преобразование рабочей книги Excel в PDF, CSV, HTML и другие форматы (GET /cells/{name})"
---

Этот REST API позволяет получить рабочую книгу Excel в другом формате.

## API GetWorkBook

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Параметры запроса**

| Имя параметра         | Тип    | Описание                                                                                                                                                   | Значение по умолчанию |
| --------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------- |
| format                | string | Целевой формат файла (например, CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG и др.). | –                     |
| password              | string | Пароль, необходимый для открытия файла Excel.                                                                                                             | –                     |
| isAutoFit             | bool   | Автоматически подгоняет ширину строк и столбцов.                                                                                                          | false                 |
| onlySaveTable         | bool   | Если **true**, сохраняются только данные таблицы. Принимает значения `true` или `false`.                                                                  | false                 |
| outPath               | string | Путь для сохранения результата. Для одного файла укажите имя файла и расширение; для нескольких файлов — только папку.                                     | –                     |
| outStorageName        | string | Имя хранилища, в котором будет сохранен выходной файл.                                                                                                   | –                     |
| checkExcelRestriction | bool   | Проверка ограничений Excel при изменении ячеек или связанных объектов.                                                                                    | false                 |
| region                | string | Региональные настройки, применяемые к рабочей книге.                                                                                                      | –                     |
| pageWideFitOnPerSheet | bool   | Подгоняет ширину страницы под ширину каждого листа при преобразовании в PDF.                                                                               | false                 |
| pageTallFitOnPerSheet | bool   | Подгоняет высоту страницы под высоту каждого листа при преобразовании в PDF.                                                                              | false                 |
| onePagePerSheet       | bool   | Генерирует по одной странице PDF для каждого листа.                                                                                                       | false                 |
| folder                | string | Путь к папке с исходной рабочей книгой.                                                                                                                   | –                     |
| storageName           | string | Имя хранилища, в котором находится исходный файл.                                                                                                         | –                     |

### Ответ

**Успех (200)**

- Если параметр запроса `format` не указан, API возвращает объект **[Workbook](/cells/workbook/)**, содержащий информацию о структуре рабочей книги.

- Если параметр запроса `format` указывает тип файла, API возвращает преобразованный файл в запрошенном формате.

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(двоичные данные PDF)
```

**Коды HTTP-статусов**

| Код  | Значение                    | Описание                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | OK (Успех)                  | Фильтр применён успешно; ответ содержит детали операции.                |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый формат файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий токен JWT.                           |
| 413  | Payload Too Large (Слишком большой payload) | Загруженный файл превышает предельный размер.                          |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                         |

> **Примечания:**  
> - Преобразование больших рабочих книг может занять больше времени; рекомендуется увеличить таймаут запроса.  
> - Некоторые форматы (например, `ODS`) не поддерживают определённые функции Excel, такие как макросы.

## Как использовать API GetWorkBook с SDK

> **Требования:**  
> - Действующий **JWT-токен доступа**, полученный в процессе аутентификации Aspose.Cells.  
> - Исходная рабочая книга должна быть размещена в поддерживаемом хранилище Aspose или передана непосредственно в запросе.  
> - Убедитесь, что версия API (`v3.0`) соответствует последней выпущенной версии.

### Спецификация API GetWorkBook

<a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступный программный интерфейс и позволяет выполнять REST-взаимодействия прямо из веб-браузера.

### Пример запроса

Вы можете использовать инструмент командной строки **cURL** для доступа к веб-сервисам Aspose.Cells. Следующий пример показывает корректный GET-запрос с обязательным заголовком авторизации.

{{< tabs tabTotal="1" tabID="11" tabName11="Запрос" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

Следующие примеры кода показывают, как вызывать веб-сервисы Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**См. также**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">Преобразование рабочей книги (POST)</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">Сохранить как (GET)</a>

---

_Последнее обновление: 2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – Преобразование рабочей книги Excel в PDF, CSV, HTML и другие форматы (GET /cells/{name})",
  "description": "Документация по конечной точке Aspose.Cells Cloud GET /cells/{name}, которая преобразует рабочие книги Excel в различные форматы, такие как PDF, CSV, HTML и другие.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, преобразование Excel, PDF, CSV, HTML, API, REST, облако",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>