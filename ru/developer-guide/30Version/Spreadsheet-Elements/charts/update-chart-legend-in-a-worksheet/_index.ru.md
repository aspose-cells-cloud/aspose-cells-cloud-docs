---
title: "Обновление легенды диаграммы в рабочем листе"
type: docs
url: /ru/charts/legend/update/
aliases: [  /ru/update-chart-legend-in-a-worksheet/ ]
weight: 160
keywords: "Aspose.Cells, облако, Excel, диаграмма, легенда, REST API, обновление, рабочий лист, cURL, SDK"
description: "Как обновить легенду диаграммы в рабочем листе Excel с помощью Aspose.Cells Cloud REST API, включая примеры запросов cURL и фрагменты кода SDK для различных языков программирования."
ArticleTitle: "Обновление легенды диаграммы в рабочем листе – руководство по API Aspose.Cells Cloud"
---

Этот REST API обновляет легенду диаграммы.

**Необходимые условия:** Для использования этого endpoint’а необходимо иметь действительный JWT-токен Aspose Cloud, а целевая рабочая книга должна быть размещена в поддерживаемом хранилище (по умолчанию — хранилище Aspose Cloud). Убедитесь, что имя рабочей книги, имя рабочего листа и индекс диаграммы указаны корректно.

Легенда диаграммы отображает названия и символы рядов данных диаграммы. Обновление легенды позволяет настроить её внешний вид, например, изменить начертание шрифта, цвет и тень.

## API PostWorksheetChartLegend

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип    | Местоположение | Описание                                      |
|---------------|--------|----------------|-----------------------------------------------|
| name          | string | path           | Имя рабочей книги.                            |
| sheetName     | string | path           | Имя рабочего листа.                           |
| chartIndex    | integer| path           | Индекс диаграммы, подлежащей изменению.       |
| legend        | object | body           | JSON-объект, определяющий параметры легенды. |
| folder        | string | query          | Папка, содержащая рабочую книгу.             |
| storageName   | string | query          | Имя хранилища.                                |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartLegend) определяет публично доступное программное интерфейсное решение и позволяет выполнять взаимодействие по REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-d '{"Font":{"Color":{"A":"1","R":"255","G":"0","B":"0"},"DoubleSize":10.0,"IsBold":true,"IsItalic":false,"IsStrikeout":false,"IsSubscript":false,"IsSuperscript":false,"Name":"Arial","Size":15,"Underline":"None"},"Shadow":true}' \
-X POST \
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

Использование SDK ускоряет разработку: SDK берёт на себя работу с низкоуровневыми деталями, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartLegendInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "74fffa317bc5ba65dc6536005e5bb683" >}}

{{< /tab >}}

{{< /tabs >}}
---