---
title: "Excel в SQL"
second_title: "Документ"
linktitle: "Excel в SQL"
type: docs
url: /ru/convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel в SQL, облачный API, преобразование таблиц, REST"
description: "Используйте облачный REST API Aspose.Cells для преобразования Excel-таблиц в SQL-файлы. Поддерживает множество SDK и языков программирования для беспрепятственной интеграции в ваши приложения."
weight: 100
ArticleTitle: "Преобразование Excel в SQL — API Aspose.Cells Cloud"
---

Этот REST API преобразует файл таблицы в формат SQL.

**Необходимые условия**  
Для использования этого эндпоинта необходимо иметь действительный JWT-токен, сгенерированный в соответствии с инструкциями, описанными в руководстве по <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по JWT-токену</a>. API поддерживает Excel-файлы размером до предельных значений, указанных в документации сервиса, и может обрабатывать защищённые паролем книги при условии передачи параметра запроса `password`.

## API PostConvertWorkbookToSQL

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **Безопасность и аутентификация**

Облачные API Aspose.Cells защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по JWT-токену</a>.

### **Параметр запроса**

| Имя параметра       | Тип    | Описание                                                                 |
|---------------------|--------|--------------------------------------------------------------------------|
| password            | string | Пароль, необходимый для открытия Excel-файла.                           |
| storageName         | string | Имя хранилища, в котором сохранён файл.                                 |
| checkExcelRestriction | bool | Указывает, следует ли проверять ограничения Excel-файла при изменении объектов, связанных с ячейками. |

### **Параметр тела запроса**

| Имя параметра | Тип       | Описание                                                                  |
|---------------|-----------|---------------------------------------------------------------------------|
| datafile      | data file | Файл таблицы, подлежащий преобразованию; включается как первая часть запроса. |

### Ответ

API возвращает объект **FileInfo**, содержащий сгенерированный SQL-файл.

| Поле            | Тип    | Описание                                       |
|-----------------|--------|------------------------------------------------|
| **Filename**    | string | Имя SQL-файла (например, `example.sql`).      |
| **FileSize**    | int    | Размер файла в байтах.                         |
| **FileContent** | string | Содержимое SQL-файла в кодировке Base64.       |

[FileInfo](/ru/cells/file-info/)

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                                       |
|-----|------------------------------|----------------------------------------------------------------|
| 200 | OK (ОК)                      | Фильтр применён успешно; ответ содержит данные об операции.   |
| 400 | Bad Request (Неверный запрос)| Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Неверный или отсутствующий JWT-токен.                         |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает ограничение по размеру. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Как использовать API PostConvertWorkbookToSQL с SDK

### Спецификация API PostConvertWorkbookToSQL

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для простого доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки **cURL**. Пример ниже показывает, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.sql",
  "FileSize": 1024,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Другие API, реализующие эту функцию

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Сохраняет книгу в другом формате и сохраняет результат в указанном хранилище.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Преобразует книгу в другой формат с возможностью задать дополнительные настройки и возвращает результат в ответе.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Получает книгу с возможностью задать дополнительные настройки преобразования.

**Примечания**  
- При преобразовании защищённых паролем Excel-файлов обязательно передавайте параметр запроса `password`, иначе преобразование завершится с ошибкой 400.  
- Сервис возвращает содержимое SQL-файла в кодировке Base64; перед сохранением в файл `.sql` его необходимо декодировать.  

**Примеры файлов**  
Скачайте пример Excel-книги [здесь](https://example.com/sample.xlsx) и предварительно сгенерированный SQL-результат [здесь](https://example.com/sample.sql), чтобы быстро протестировать API.  
---