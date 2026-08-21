---
title: "Aspose.Cells Cloud Web API — преобразование данных таблицы электронной таблицы в файл CSV — бесплатный онлайн-инструмент"
second_title: "Документ"
ArticleTitle: "Как преобразовать данные таблицы электронной таблицы в файл CSV: пошаговое руководство"
linktitle: "Преобразование таблицы в CSV"
type: docs
url: /convert-table-to-csv/
keywords: "Aspose.Cells Cloud, таблица в CSV, преобразование электронной таблицы, Excel в CSV, API, REST, экспорт данных"
description: "Быстро преобразуйте таблицу из электронной таблицы Excel в файл CSV с помощью API Aspose.Cells Cloud."
weight: 100
---

Экспортируйте данные таблицы из локального файла Excel в файл CSV с помощью облачного API.

## **API преобразования таблицы в CSV**

### Веб-API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Параметры запроса:**

| Имя параметра | Тип    | Путь/Строка запроса/Тело HTTP-запроса | Описание                                                                                                                                               |
|---------------|--------|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet   | Файл   | FormData                              | Загрузка файла электронной таблицы.                                                                                                                    |
| worksheet     | Строка | Параметр запроса                      | Имя рабочего листа в электронной таблице.                                                                                                              |
| tableName     | Строка | Параметр запроса                      | Имя таблицы, подлежащей преобразованию.                                                                                                                 |
| outPath       | Строка | Параметр запроса                      | (Необязательно) Путь к папке, где хранится рабочая книга; по умолчанию null.                                                                          |
| outStorageName| Строка | Параметр запроса                      | Имя хранилища для выходного файла.                                                                                                                     |
| fontsLocation | Строка | Параметр запроса                      | Путь для использования пользовательских шрифтов.                                                                                                       |
| region        | Строка | Параметр запроса                      | Настройка региона/языка электронной таблицы (например, `ru-RU`, `en-US`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от локали.|
| password      | Строка | Параметр запроса                      | Пароль для открытия файла электронной таблицы.                                                                                                         |

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

**Коды HTTP-статуса**

| Код | Значение                | Описание                                                                 |
|-----|-------------------------|--------------------------------------------------------------------------|
| 200 | OK (ОК)                 | Фильтр успешно применён; ответ содержит детали операции.                |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий токен JWT.                           |
| 413 | Payload Too Large (Слишком большой объём полезной нагрузки) | Загруженный файл превышает лимит размера.                          |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                        |

## **Где следует использовать API преобразования таблицы в CSV?**

- **Миграция базы данных**: Преобразуйте таблицы Excel в CSV для массового импорта в SQL-базы данных (MySQL, PostgreSQL, SQL Server).
- **Загрузка в хранилище данных**: Преобразуйте таблицы отчётов на основе Excel в CSV для загрузки в Snowflake, Redshift или BigQuery.
- **Пакетные запросы API**: Преобразуйте данные таблиц Excel в CSV для массовой загрузки через API REST-сервисов.
- **Взаимодействие между сервисами**: Используйте CSV как лёгкий формат обмена данными между микросервисами.
- **Подготовка данных для машинного обучения**: Преобразуйте таблицы признаков из Excel в CSV для использования в библиотеках машинного обучения на Python/R.
- **Статистический анализ**: Преобразуйте исследовательские таблицы данных в CSV для импорта в SPSS, SAS или Stata.
- **Миграция контента**: Перенесите структурированный контент из Excel в системы управления контентом (CMS) через CSV.

## Почему стоит использовать API преобразования таблицы в CSV?

- **Удобен для разработчиков**: Aspose.Cells Cloud предоставляет SDK на множестве языков программирования, что ускоряет разработку, и сопровождается подробной документацией. По сравнению с созданием собственных решений это существенно снижает объём работы.
- **Экономически эффективно**: Можно преобразовывать данные таблиц без предварительной загрузки рабочей книги, что экономит место в хранилище и снижает затраты.
- **Извлечение только данных без форматирования**.
- **CSV поддерживается практически всеми системами**:
  - Базы данных (все основные СУБД)
  - Языки программирования (встроенные парсеры во всех)
  - Средства бизнес-аналитики (Tableau, Power BI, Looker)
  - Табличные процессоры (Excel, Google Таблицы, LibreOffice)
  - Инструменты командной строки (awk, sed, grep)

## Как использовать API преобразования таблицы в CSV с SDK?

### Спецификация API преобразования таблицы в CSV

[Спецификация API преобразования таблицы в CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV) предоставляет открытый для использования программный интерфейс, позволяющий взаимодействовать с REST-интерфейсом напрямую из веб-браузера.
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки, так как он абстрагирует низкоуровневые детали, позволяя преобразовать данные таблицы электронной таблицы в файл CSV с минимальным объёмом кода. Полный список SDK Aspose.Cells Cloud доступен на [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода иллюстрируют, как делать вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}