---
title: "Aspose.Cells Cloud Web API — Конвертация электронной таблицы в другой формат — Бесплатный онлайн-инструмент"
second_title: "Документ"
ArticleTitle: "Как конвертировать электронную таблицу в другой формат: Пошаговое руководство"
linktitle: "Конвертация электронной таблицы"
type: docs
url: /convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, конвертация электронных таблиц, Excel в PDF, Excel API, облачная конвертация файлов"
description: "Конвертируйте файл электронной таблицы в другой формат с помощью Aspose.Cells Cloud API."
weight: 100
---

Конвертируйте локальный файл электронной таблицы/Excel в другой формат с помощью Aspose.Cells Cloud Web API.

## **API конвертации электронной таблицы**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API безопасны и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса:**

| Имя параметра | Тип    | Путь/Строка запроса/HTTPBody | Описание                                                                                     |
| :------------ | :----- | :-------------------------- | :------------------------------------------------------------------------------------------- |
| Spreadsheet   | Файл   | FormData                    | Загрузите файл электронной таблицы, который необходимо конвертировать.                       |
| format        | Строка | Query                       | (Обязательно) Желаемый выходной формат (например, «XLSX», «PDF», «CSV»).                     |
| outPath       | Строка | Query                       | (Необязательно) Путь к папке, в которой будет сохранена конвертированная рабочая книга. По умолчанию — null. |
| outStorageName| Строка | Query                       | Укажите имя хранилища для выходного файла.                                                   |
| fontsLocation | Строка | Query                       | Использовать пользовательские шрифты для электронной таблицы.                                |
| region        | Строка | Query                       | Указать региональные настройки электронной таблицы.                                          |
| password      | Строка | Query                       | Пароль для открытия защищенного файла электронной таблицы.                                   |

### **Ответ**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Успешный статус**

- **200 OK** — Конвертация выполнена успешно; тело ответа содержит поток конвертированного файла.
- Заголовок `Content-Type` отражает MIME-тип запрошенного выходного формата (например, `application/pdf` для PDF).

**Коды HTTP-статусов**

| Код | Значение                | Описание                                                        |
| --- | ----------------------- | --------------------------------------------------------------- |
| 200 | OK                      | Фильтр успешно применён; ответ содержит детали операции.        |
| 400 | Bad Request             | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized            | Недействительный или отсутствующий JWT-токен.                  |
| 413 | Payload Too Large       | Размер загруженного файла превышает допустимый лимит.           |
| 500 | Internal Server Error   | Непредвиденная ошибка сервера.                                  |

## Форматы вывода

| **Выходной формат**                                                                                    | **Описание**                                                                                                               |
| :----------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>               | Рабочая книга Excel 95/5.0 – 2003.                                                                                         |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>             | Формат файла Excel в формате Office Open XML SpreadsheetML.                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>             | Двоичная рабочая книга Excel.                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>             | Рабочая книга Excel с поддержкой макросов.                                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>               | Шаблон Excel 97 – Excel 2003.                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>             | Шаблон Excel.                                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>             | Шаблон Excel с поддержкой макросов.                                                                                        |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>             | Файл надстройки Excel с поддержкой макросов, используемый для добавления новых функций в Excel.                            |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>               | Файл CSV (значения, разделённые запятыми).                                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>               | Файл TSV (значения, разделённые символами табуляции).                                                                      |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>           | Текстовый файл с разделителями.                                                                                            |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                     | Формат HTML.                                                                                                               |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                   | Файл MHTML.                                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>               | Электронная таблица OpenDocument (ODS).                                                                                    |
| SpreadsheetML                                                                                          | Файл Excel 2003 XML.                                                                                                       |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>       | Документ, созданный в приложении Apple «Numbers», входящем в состав пакета iWork для macOS и iOS.                          |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                     | JavaScript Object Notation.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>               | Формат обмена данными (DIF).                                                                                               |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                  | Файл с расширением .dbf — файл базы данных, используемый в СУБД dBASE.                                                     |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                           | Adobe Portable Document Format.                                                                                            |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | Формат спецификации XML-страницы (XPS).                                                                                    |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | Формат масштабируемой векторной графики (SVG).                                                                             |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                   | Формат TIFF (Tagged Image File Format).                                                                                    |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                     | Формат PNG (Portable Network Graphics).                                                                                    |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                     | Растровый формат изображения (BMP).                                                                                        |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                     | Улучшенный метафайл (EMF).                                                                                                 |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                   | JPEG — формат изображения с потерями.                                                                                      |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                     | Формат GIF (Graphics Interchange Format).                                                                                  |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>       | Представляет документ Markdown.                                                                                            |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>               | XML-основанный формат, используемый в OpenOffice и StarOffice.                                                             |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>             | Формат Open Document, сохраняемый как плоский XML.                                                                         |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>         | Хорошо известный формат документов Microsoft Word, сочетающий XML и двоичные данные.                                      |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>            | Формат PPTX основан на формате презентаций Open XML Microsoft PowerPoint.                                                 |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>            | Язык структурированных запросов (SQL).                                                                                     |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                   | XHTML — текстовый формат на основе XML с разметкой, представляющий собой переформулировку HTML 4.0.                        |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                   | Файлы с расширением .epub — формат электронных книг, обеспечивающий стандартную цифровую публикацию для издателей и пользователей. |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                       | XML (Extensible Markup Language) — язык разметки, похожий на HTML, но использующий теги для определения объектов.           |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>               | Шаблон электронной таблицы OpenDocument (OTS).                                                                             |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                   | AZW — цифровой формат электронных книг, разработанный Amazon для устройств Kindle. AZW3 также известен как Kindle Format 8 (KF8). |

## Где следует использовать API конвертации электронной таблицы?

- **Миграция устаревших систем**: конвертация тысяч устаревших файлов XLS в XLSX для современных систем.
- **Стандартизация архивов**: приведение различных форматов электронных таблиц (XLS, XLSM, ODS, CSV) к единому формату для архивирования.
- **Совместимость с офисными пакетами**: конвертация файлов Excel в форматы, совместимые с LibreOffice, Google Таблицами или Apple Numbers.
- **Нормализация источников данных**: конвертация различных форматов электронных таблиц в CSV или JSON для последующей загрузки в базу данных.
- **Публикация в вебе**: конвертация финансовых моделей в HTML для отображения в вебе.

## Почему следует использовать API конвертации электронной таблицы?

- **Удобен для разработчиков**: Aspose.Cells Cloud предоставляет SDK на множестве языков программирования, что ускоряет разработку, и сопровождается подробной документацией. По сравнению с созданием собственных решений для отрисовки графиков, это значительно снижает трудозатраты.
- **Экономически эффективно**: можно конвертировать табличные данные без предварительной загрузки рабочей книги, что экономит место в хранилище и снижает затраты.
- **Широкая поддержка форматов**: конвертация между более чем 20 форматами электронных таблиц.
- **Сохранение точности данных и форматирования**.

## Как использовать API конвертации электронной таблицы с SDK?

Следующие примеры кода демонстрируют использование API конвертации электронной таблицы с различными SDK.

### Спецификация API конвертации электронной таблицы

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">Спецификация API конвертации электронной таблицы</a> предоставляет публично доступное программное интерфейсное описание, позволяющее выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Ниже приведён пример вызова облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки, так как он абстрагирует низкоуровневые детали и позволяет конвертировать файл электронной таблицы в другой формат с помощью компактного кода. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Convert Spreadsheet",
  "description": "Конвертируйте файл электронной таблицы в другой формат с помощью Aspose.Cells Cloud.",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "Конвертирует электронную таблицу в указанный формат."
    }
  ]
}
</script>

---