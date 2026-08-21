---
title: "Обновление свойств диаграммы"
type: docs
url: /charts/properties/update/
aliases: [/update-chart-properties/]
weight: 160
keywords: "Aspose.Cells, диаграмма, обновление, Excel, REST API, SDK"
description: "Узнайте, как обновлять свойства диаграммы (тип, заголовок, легенда и т.д.) в книге Excel с помощью Aspose.Cells Cloud REST API (v3.0). Включает endpoint, параметры, пример cURL и фрагменты кода SDK для C#, Java, PHP, Ruby, Node.js, Perl и Go."
ArticleTitle: "Обновление свойств диаграммы – Aspose.Cells Cloud REST API"
---

Этот REST API обновляет свойства диаграммы.

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию по токену JWT</a>.

## API PostWorksheetChart

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Параметры запроса

| Имя параметра | Тип    | Путь/Строка запроса/HTTP-тело | Описание                                                   |
|---------------|--------|-------------------------------|-------------------------------------------------------------|
| name          | string | path                          | Имя файла Excel.                                            |
| sheetName     | string | path                          | Имя листа, содержащего диаграмму.                           |
| chartIndex    | integer| path                          | Индекс диаграммы (отсчитывается от нуля), подлежащей обновлению. |
| chart         | object | body                          | JSON-объект, определяющий обновляемые свойства диаграммы.  |
| folder        | string | query                         | Папка в хранилище, где расположен файл.                     |
| storageName   | string | query                         | Имя сервиса хранилища.                                      |

### Схема тела запроса

Объект **`chart`** содержит свойства, которые можно изменить. Ниже приведён типичный пример JSON, включающий несколько часто используемых полей:

```json
{
  "Title": {
    "Text": "Квартальные продажи"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **Примечание:** Необходимо передавать только те поля, которые требуется изменить. Неуказанные свойства сохранят свои текущие значения.

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для простого доступа к веб-сервисам Aspose.Cells вы можете использовать утилиту командной строки cURL. В следующем примере показано, как выполнять вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
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

{{< /tab >}}

{{< /tabs >}}

## Ответ

API возвращает JSON-объект, указывающий результат операции. При успешном обновлении возвращается:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Коды успешного состояния**

| HTTP-статус | Описание |
|-------------|----------|
| 200         | OK — свойства диаграммы успешно обновлены. |

**Заголовки ответа**

| Заголовок | Описание |
|----------|----------|
| `Content-Type` | `application/json` — указывает, что тело ответа имеет формат JSON. |
| `X-RequestId` | Уникальный идентификатор запроса (полезно для устранения неполадок). |

Возможные ответы об ошибках:

| HTTP-статус | Описание |
|-------------|----------|
| 400         | Bad Request — неверные параметры или тело запроса |
| 401         | Unauthorized — отсутствует или неверен токен |
| 404         | Not Found — файл, лист или диаграмма не найдены |
| 500         | Internal Server Error — внутренняя ошибка сервера |

Для других операций, связанных с диаграммами, см. смежные разделы, например [Обновление заголовка диаграммы](/charts/title/update/) и [Обновление легенды диаграммы](/charts/legend/update/).

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории GitHub</a>.

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}