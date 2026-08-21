---
title: "Получение гиперссылки листа"
type: docs
url: /hyperlinks/get/
keywords: "Aspose.Cells Cloud, получение гиперссылки листа, API Excel для гиперссылок, REST, аутентификация JWT, лист Excel, конечная точка API"
description: "Получение конкретной гиперссылки из листа Excel с использованием API Aspose.Cells Cloud (v3.0). Включает конечную точку, параметры, пример cURL, данные об аутентификации, обработку ошибок и фрагменты SDK."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Получение гиперссылки листа"
---

Этот REST API позволяет получить **гиперссылку** листа с помощью **API Aspose.Cells Get Hyperlink**.

## Безопасность и аутентификация

API Aspose.Cells Cloud являются безопасными и требуют [аутентификации по токену JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
Перед вызовом конечной точки получите токен доступа JWT, используя ваш идентификатор клиента и секретный ключ, и включите его в заголовок `Authorization: Bearer <jwt token>`.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Параметры запроса

| Имя параметра  | Тип    | Расположение | Описание                                      |
| -------------- | ------ | ------------ | --------------------------------------------- |
| name           | string | path         | Имя файла Excel.                              |
| sheetName      | string | path         | Имя листа, содержащего гиперссылку.           |
| hyperlinkIndex | integer| path         | Индекс гиперссылки для получения (начиная с 0).|
| folder         | string | query        | Папка, в которой хранится документ.           |
| storageName    | string | query        | Имя сервиса хранения.                          |

### Ответы об ошибках

| HTTP-код | Причина                                                  | Пример тела ответа                                                  |
| -------- | -------------------------------------------------------- | ------------------------------------------------------------------- |
| **400**  | Неверный запрос – отсутствуют или некорректны параметры. | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**  | Неавторизован – отсутствует или некорректен токен JWT.  | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**  | Не найдено – рабочая книга или лист не существуют.      | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**  | Внутренняя ошибка сервера – непредвиденная ошибка сервера.| `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для удобного доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

В приведенных ниже примерах кода показано, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}