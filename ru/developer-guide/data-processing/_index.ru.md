---
title: "Aspose.Cells Cloud – Объединение, разделение и импорт табличных данных"
second_title: "Документ"
ArticleTitle: "Обработка табличных данных – Объединение, разделение и импорт"
linktitle: "Обработка данных"
type: docs
url: /ru/data-processing/
keywords: "Aspose.Cells Cloud, обработка табличных данных, объединение Excel, разделение Excel, импорт CSV, импорт JSON, API"
description: "Подробное руководство по импорту данных в форматах CSV/JSON, объединению удалённых рабочих книг Excel и разделению больших табличных файлов с использованием REST API Aspose.Cells Cloud, включая примеры запросов и ответов."
weight: 30
---

**Aspose.Cells Cloud** – REST-сервис, позволяющий программно управлять файлами Excel в облаке. Он поддерживает импорт данных из различных форматов, объединение рабочих книг и разделение больших табличных файлов.

Раздел **Обработка данных** API Aspose.Cells Cloud позволяет программно импортировать, объединять и разделять табличные данные. Используйте указанные ниже конечные точки для обработки импорта CSV/JSON, объединения рабочих книг или разделения больших файлов на более мелкие части.

## Импорт и управление данными

- **[Импорт данных CSV, JSON, XML в файлы Excel](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

Операция импорта принимает данные в формате CSV, JSON или XML и создаёт новый рабочий лист (или обновляет существующий) в целевой рабочей книге.

**Детали конечной точки**

| HTTP-метод | Конечная точка | Тело запроса | Успешный ответ |
|------------|----------------|--------------|----------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` или `text/csv` (в зависимости от формата) | `200 OK` с JSON, содержащим метаданные обновлённой рабочей книги |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *отсутствует* | Возвращает обработанный файл рабочей книги |

**Пример запроса cURL (импорт CSV)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**Пример JSON-ответа**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **Необходимые условия**: Требуется OAuth2-токен доступа. Исходный файл должен находиться в облачном хранилище Aspose Cloud или быть загружен через multipart-загрузку.

## Операция объединения файлов

- **[Объединение удалённых файлов Excel в указанную рабочую книгу](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[Объединение нескольких файлов Excel в одну рабочую книгу](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Объединение файлов Excel, соответствующих шаблону в удалённой папке](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

Объединение — это процесс объединения двух или более рабочих книг в одну целевую. API поддерживает как явный перечень файлов, так и объединение по шаблону в папке хранилища.

**Детали конечной точки**

| HTTP-метод | Конечная точка | Параметры | Успешный ответ |
|------------|----------------|-----------|----------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files` (массив имён файлов), `target` (опционально — имя целевой рабочей книги) | `200 OK` с JSON, описывающим объединённую рабочую книгу |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`, `pattern`, `target` | `200 OK` с метаданными объединённой рабочей книги |

**Пример запроса cURL (объединение явного списка)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**Пример JSON-ответа**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **Необходимые условия**: Все исходные рабочие книги должны находиться в одном и том же расположении облачного хранилища, а вызывающий пользователь должен иметь права на чтение/запись.

## Операция разделения файлов

- **[Разделение файла Excel на несколько файлов по рабочим листам](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[Разделение файла Excel по пользовательским правилам](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

Разделение извлекает отдельные рабочие листы или группы строк/столбцов в отдельные файлы рабочих книг.

**Детали конечной точки**

| HTTP-метод | Конечная точка | Параметры | Успешный ответ |
|------------|----------------|-----------|----------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy` (например, `worksheet`), `outputFolder` | `200 OK` со списком URL-адресов созданных файлов |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | JSON-описание пользовательского правила (размер страницы, диапазон строк и т.д.) | `200 OK` с деталями разделённых файлов |

**Пример запроса cURL (разделение по рабочим листам)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**Пример JSON-ответа**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **Необходимые условия**: Исходная рабочая книга должна быть доступна в облачном хранилище Aspose Cloud, а вызывающий пользователь должен иметь права на запись в целевую папку.