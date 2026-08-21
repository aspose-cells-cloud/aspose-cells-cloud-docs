---
title: "Сбор данных для создания отчёта в Excel"
second_title: "Документ"
linktype: "Сбор данных"
type: docs
url: /ru/assembly-data-for-the-creation-of-an-excel-report/
aliases: [  /ru/assembly/ ]
keywords: "Aspose.Cells, отчёт Excel, сбор данных, облачный API, REST, SDK, cURL, PDF, ODS"
description: "Узнайте, как использовать API сборки Aspose.Cells Cloud для объединения данных в отчётах в форматах Excel (XLSX, PDF, ODS). Включает описание конечной точки, параметры, пример cURL, код SDK, руководство по аутентификации и обработку ошибок."
weight: 40
---

Этот REST API выполняет сбор данных **внутрь** файла Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/assembly
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса


| Имя параметра | Тип   | Местоположение            | Описание                                                     |
|---------------|-------|---------------------------|--------------------------------------------------------------|
| file          | файл  | formData (multipart body) | Загружаемый файл электронной таблицы.                         |
| DataSource    | строка | строка запроса            | Идентификатор источника данных, предоставляющего данные для сборки. |
| format        | строка | строка запроса            | Желаемый выходной формат (например, `xlsx`, `pdf`).          |

### **Ответ**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[имя файла 2]",
    "Filesize" : [размер файла],
    "FileContent" : "[Base64String]"
}
```

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                                      |
|-----|------------------------------|---------------------------------------------------------------|
| 200 | OK (ОК)                      | Фильтр успешно применён; ответ содержит детали операции.     |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недопустимый или отсутствующий JWT-токен.                    |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает допустимый размер.                |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                               |

## Как использовать API PostAssemble с SDK

### Спецификация API PostAssemble

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostAssemble) определяет публично доступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/assembly?DataSource=ds&format=pdf" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'template=@template.xlsx' \
  -F 'data=@data.json'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "report1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "report2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки с использованием API. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

В следующих примерах кода показано, как вызывать веб-сервисы Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAssemble.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAssemble.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAssemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAssemble.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAssemble.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAssemble.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAssemble.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAssemble.go" >}}

{{< /tab >}}

{{< /tabs >}}

---