---
title: "Удаление области ячеек — Документация API Aspose.Cells Cloud"
type: docs
url: /conditional-formattings/delete-cell-area/
aliases: [/remove-cell-area-from-conditional-formatting/]
keywords: "Aspose.Cells Cloud, Удаление области ячеек, API условного форматирования, Excel REST API"
description: "Используйте REST API Aspose.Cells Cloud для удаления конкретной области ячеек из условного форматирования в листе Excel. Примеры на ASP.NET, Java и Python."
ArticleTitle: "Удаление области ячеек — Документация API Aspose.Cells Cloud"
weight: 70
---

Этот REST API удаляет область ячеек из правила условного форматирования.

## Безопасность и аутентификация
API Aspose.Cells Cloud защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                                   |
|---------------|--------|--------------|----------------------------------------------------------------------------|
| `name`        | string | path         | Имя файла Excel.                                                           |
| `sheetName`   | string | path         | Имя листа, содержащего условное форматирование.                           |
| `startRow`    | integer | query       | Индекс первой строки удаляемой области (начинается с 0).                   |
| `startColumn` | integer | query       | Индекс первого столбца удаляемой области (начинается с 0).                |
| `totalRows`   | integer | query       | Количество строк в удаляемой области.                                      |
| `totalColumns`| integer | query       | Количество столбцов в удаляемой области.                                  |
| `folder`      | string | query       | Папка в облачном хранилище, где расположен файл (необязательно).          |
| `storageName` | string | query       | Имя службы хранилища (необязательно).                                     |

### Ответы об ошибках

| HTTP-статус | Код             | Описание                                                       | Пример JSON                                                   |
|-------------|-----------------|----------------------------------------------------------------|---------------------------------------------------------------|
| 400         | `BadRequest`    | Отсутствуют или недопустимы параметры запроса.                | `{ "Code": "400", "Message": "Invalid request parameters." }` |
| 401         | `Unauthorized`  | Отсутствует или недопустим JWT-токен.                         | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404         | `NotFound`      | Файл, лист или условное форматирование не найдены.            | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500         | `InternalError` | Непредвиденная ошибка сервера.                                 | `{ "Code": "500", "Message": "Internal server error." }`      |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к сервисам Aspose.Cells Cloud. В следующем примере показано, как вызвать конечную точку **Удаление области ячеек** с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"}, чтобы получить полный список SDK Aspose.Cells Cloud.

Приведённые ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}
---