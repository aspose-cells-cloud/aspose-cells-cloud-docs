---
title: "Удаление пустых столбцов из Excel с помощью Aspose.Cells Cloud API — быстрый пример REST"
second_title: "Документ"
ArticleTitle: "Как удалить пустые столбцы в Excel — автоматизация очистки столбцов"
linktitle: "Удаление пустых столбцов"
type: docs
url: /delete-spreadsheet-blank-columns/
keywords: "удаление пустых столбцов Excel API, Aspose.Cells Cloud, REST API, очистка Excel, автоматизация электронных таблиц"
description: "Узнайте, как удалять пустые столбцы из файлов Excel с помощью Aspose.Cells Cloud REST API. Включает endpoint, аутентификацию, примеры запросов и ответов, а также код SDK на C#, Java, Python и других языках."
weight: 100
---

Используйте Aspose.Cells Cloud API для автоматического удаления всех пустых столбцов из электронных таблиц Excel. Наш интеллектуальный API обнаруживает и удаляет столбцы, ячейки которых не содержат данных, формул, комментариев, диаграмм или объектов. API поддерживает пакетную обработку, облачную автоматизацию и бесшовную интеграцию REST для корпоративных сценариев очистки электронных таблиц.

**Контекст:**  
Пустые столбцы часто появляются после импорта данных, генерации шаблонов или миграции устаревших файлов. Удаление таких пустых столбцов уменьшает размер файла, улучшает производительность отображения и повышает точность дальнейшей обработки данных. API «Delete Spreadsheet Blank Columns» обеспечивает быстрое решение для очистки электронных таблиц на стороне сервера без ручного редактирования.

## **API DeleteSpreadsheetBlankColumns**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-columns
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Параметры запроса

| Имя параметра      | Тип    | Местоположение            | Описание                                                                                                                  |
| ------------------ | ------ | ------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | File   | Form‑Data (multipart)     | Рабочая книга Excel, подлежащая обработке.                                                                                 |
| **outPath**        | String | Query                     | Необязательно. Путь к папке в облачном хранилище, куда будет сохранён очищенный файл. Если параметр опущен, результат возвращается в теле ответа. |
| **outStorageName** | String | Query                     | Необязательно. Имя облачного хранилища, в котором будет сохранён результат.                                               |
| **region**         | String | Query                     | Необязательно. Идентификатор языка и региона (например, `ru-RU`, `de-DE`).                                                 |
| **password**       | String | Query                     | Необязательно. Пароль для открытия защищённой рабочей книги.                                                              |

### Ответ

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

### Коды ошибок

- **400 Bad Request** — недопустимые параметры запроса или некорректный URI.
- **401 Unauthorized** — отсутствует или недействителен токен доступа.
- **404 Not Found** — указанный файл электронной таблицы не найден.
- **500 Server Error** — непредвиденная ошибка, препятствующая обработке файла API.

## Когда использовать API «Delete Spreadsheet Blank Columns»

- **Потоки импорта и очистки данных** — немедленно удаляйте завершающие или структурные пустые столбцы после загрузки данных из CSV, баз данных или веб-API.
- **Генерация отчётов и дашбордов** — обеспечивайте чистую структуру финальных отчётов без лишних пустых столбцов.
- **Конвейеры ETL** — предварительно обрабатывайте файлы Excel перед загрузкой в хранилища данных, такие как Snowflake или BigQuery.
- **Системная интеграция** — приводите Excel-файлы, предоставленные партнёрами, к единому виду перед дальнейшей обработкой.
- **Пакетная автоматизация документов** — массово удаляйте столбцы-заглушки из сгенерированных шаблонов.
- **Пользовательский контент** — очищайте загружаемые пользователем файлы Excel из веб-порталов перед хранением или анализом.
- **Миграция устаревших данных** — упрощайте архивы старых электронных таблиц, удаляя исторически пустые столбцы.

## Почему использовать этот API?

- **Удобный для разработчиков** — SDK доступны для C#, Java, Python, PHP, Ruby, Node.js, Go и других языков, что снижает трудозатраты на разработку.
- **Экономически эффективно** — тарификация по факту использования исключает первоначальные затраты на инфраструктуру.
- **Нулевое обслуживание** — не нужно управлять серверами; сервис постоянно обновляется компанией Aspose.

## Как использовать API «Delete Spreadsheet Blank Columns» с SDK

### Спецификация API

[Спецификация API «Delete Spreadsheet Blank Columns»](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankColumns) содержит полное определение OpenAPI и примеры.

### Использование SDK Aspose.Cells Cloud

SDK скрывает детали низкоуровневого HTTP-взаимодействия, позволяя удалять пустые столбцы всего в несколько строк кода. Полный список поддерживаемых языков см. в официальном репозитории GitHub: <https://github.com/aspose-cells-cloud>.

Следующие примеры кода демонстрируют вызов API с помощью различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankColumns.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankColumns.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankColumns.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankColumns.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankColumns.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankColumns.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankColumns.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankColumns.go" >}}
{{</tab>}}
{{< /tabs >}}
---