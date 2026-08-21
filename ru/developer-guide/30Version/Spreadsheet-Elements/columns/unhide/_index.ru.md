---
title: "Отмена скрытия столбцов на листе Excel"
ArticleTitle: "Отмена скрытия столбцов на листе Excel — Aspose.Cells Cloud API"
second_title: "Документ"
linktype: "docs"
url: /ru/columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells, облачный API, отмена скрытия столбцов, Excel, REST, SDK"
description: "Узнайте, как с помощью облачного REST API Aspose.Cells отменить скрытие столбцов на листе Excel. Включает сведения о запросе, пример cURL и примеры кода SDK для нескольких языков программирования."
weight: 50
---

Этот REST API отменяет скрытие столбцов листа.

**Необходимые условия** — все конечные точки облачных сервисов Aspose.Cells требуют HTTPS и действующего маркера доступа OAuth 2.0. Убедитесь, что вы получили маркер доступа и включили его в заголовок `Authorization` своих запросов.

## API PostUnhideWorksheetColumns

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **Безопасность и аутентификация**

Облачные API Aspose.Cells защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе маркера JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                       |
|---------------|--------|-------------|------------------------------------------------|
| name          | string | path        | Имя рабочей книги.                             |
| sheetName     | string | path        | Имя листа.                                     |
| startColumn   | integer | query      | Индекс первого обрабатываемого столбца.         |
| totalColumns  | integer | query      | Количество обрабатываемых столбцов.             |
| width         | number | query       | Желаемая ширина столбца (по умолчанию = 50,0).  |
| folder        | string | query       | Папка, содержащая документ.                    |
| storageName   | string | query       | Имя сервиса хранилища.                         |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Типичные HTTP-коды состояния**

| Код | Описание                                                 |
|-----|----------------------------------------------------------|
| 200 | OK — скрытие столбцов успешно отменено.                  |
| 400 | Bad Request — недопустимые параметры.                   |
| 401 | Unauthorized — отсутствующий или недействительный токен.|
| 404 | Not Found — рабочая книга или лист не найдены.          |
| 500 | Internal Server Error — непредвиденная ошибка.          |

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Ознакомьтесь со <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозиторием на GitHub</a> для получения полного списка SDK Aspose.Cells Cloud.

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}