---
title: "Отображение легенды диаграммы в рабочем листе"
type: docs
url: /charts/legend/show/
aliases: [/show-chart-legend-in-a-worksheet/]
weight: 100
keywords: "Aspose.Cells Cloud, API легенды диаграммы, легенда диаграммы Excel, REST PUT для легенды диаграммы, Aspose API v3.0"
description: "Узнайте, как отобразить легенду диаграммы в рабочем листе Excel с помощью REST API Aspose.Cells Cloud (v3.0). Включает детали конечной точки, параметры, пример cURL и фрагменты кода SDK."
---

Этот REST API позволяет отобразить **легенду** — поясняющий блок, идентифицирующий ряды данных — в диаграмме, расположенной в рабочем листе книги Excel.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                    |
| ------------- | ------ | ------------ | ------------------------------------------- |
| name          | string | path         | Имя файла книги.                            |
| sheetName     | string | path         | Имя рабочего листа, содержащего диаграмму. |
| chartIndex    | integer| path         | Индекс диаграммы (начинается с нуля).       |
| folder        | string | query        | Папка, содержащая книгу.                    |
| storageName   | string | query        | Имя сервиса хранилища.                      |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend) определяет общедоступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Аутентификация выполняется с помощью токена Bearer JWT, передаваемого в заголовке **Authorization**.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

API может возвращать следующие HTTP-коды состояния:

- **200 OK** — Легенда успешно отображена.
- **400 Bad Request** — Недопустимые параметры.
- **401 Unauthorized** — Ошибка аутентификации.
- **404 Not Found** — Указанная книга, рабочий лист или диаграмма не существует.
- **500 Internal Server Error** — Произошла непредвиденная ошибка сервера.

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах вашего проекта. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы получить полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}