---
title: "Получение объединённых ячеек из рабочего листа Excel — Aspose.Cells Cloud API"
type: docs
url: /ru/get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud, объединённые ячейки, рабочий лист Excel, REST API, Aspose.Cells SDK, объединённые ячейки Excel"
description: "Узнайте, как получить диапазоны объединённых ячеек из рабочего листа Excel с помощью API Aspose.Cells Cloud (v3.0). Включает шаги аутентификации, полный запрос cURL, схему ответа, обработку ошибок и примеры SDK на C#, Java, Python и других языках."
---

Этот REST API возвращает информацию об **объединённых ячейках** в рабочем листе Excel.

> **Примечание** – объект API называется **MergedCell** (в единственном числе). В основном тексте мы ссылаемся на *концепцию* объединённых ячеек (во множественном числе).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

## Безопасность и аутентификация

API Aspose.Cells Cloud защищены и требуют [аутентификации с использованием JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Параметры запроса

| Имя параметра | Тип   | Расположение | Описание                         |
|---------------|-------|--------------|----------------------------------|
| **name**      | string | path        | Имя файла Excel.                 |
| **sheetName** | string | path        | Имя рабочего листа.              |
| **folder**    | string | query       | Папка, содержащая документ.      |
| **storageName**| string | query      | Имя используемого хранилища.     |

## **Ответ**

Возвращается объект MergedCellsResponse.

```json
{
  "Status":"OK",
  "Code":200,
  "MergedCells":{
    "Count": 0,
    "MergedCellList":[
      {
        "Link":{
          "Href":"",
          "Rel":"",
          "Type":"",
          "Title":""
        }
      }
    ]
  }
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK (OK)                     | Фильтр применён успешно; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен. |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает ограничение по размеру. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Как использовать API GetWorksheetMergedCells с SDK

### Спецификация API GetWorksheetMergedCells

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells) определяет общедоступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для лёгкого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MergedCells": {
    "Count": 1,
    "MergedCells": [
      {
      "link": {
            "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
            "Rel": "self"
          }
      }
    ]    
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки под API. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

{{< /tab >}}

{{< /tabs >}}
---