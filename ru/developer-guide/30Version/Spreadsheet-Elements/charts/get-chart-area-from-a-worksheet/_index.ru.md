---
title: "Получение области диаграммы из рабочего листа"
type: docs
url: /charts/area/get/
aliases: [/get-chart-area-from-a-worksheet/]
weight: 60
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "ChartArea"
  - "Worksheet"
  - "cURL"
  - "SDK"
  - "GetChartArea"
description: "Узнайте, как извлечь информацию об области диаграммы из рабочего листа с помощью REST API Aspose.Cells Cloud, приведены примеры для cURL и различных SDK."
ArticleTitle: "Получение области диаграммы из рабочего листа — Aspose.Cells Cloud API"
---

Этот REST API возвращает информацию об области диаграммы.

**Необходимые условия:** Для вызова этого эндпоинта необходим действующий JWT-токен доступа, целевая рабочая книга должна быть загружена в облачное хранилище Aspose, а формат файла должен поддерживаться Aspose.Cells.

**Введение:** Область диаграммы определяет внешний ограничивающий прямоугольник диаграммы Excel, включая заголовки, легенды и область построения. Получение её свойств позволяет программно настраивать макет и оформление.

## API GetChartArea

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                      |
| ------------- | ------ | ------------ | --------------------------------------------- |
| name          | string | path         | Имя файла рабочей книги.                      |
| sheetName     | string | path         | Имя рабочего листа, содержащего диаграмму.   |
| chartIndex    | integer| path         | Индекс диаграммы (начинается с нуля).         |
| folder        | string | query        | Папка, в которой хранится рабочая книга.     |
| storageName   | string | query        | Имя сервиса хранилища.                        |

### **Ответ**

```json
{
  "ChartArea": {
    "Area": {
      "BackgroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "FillFormat": { "Type": "Automatic" },
      "ForegroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": false,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "IsAuto": false,
      "IsAutomaticColor": false,
      "IsVisible": false,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": "255", "R": "0", "G": "0", "B": "0" },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": false,
    "IsInnerMode": false,
    "Shadow": false,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                              |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр применён успешно; ответ содержит данные о выполнении операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.        |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера.            |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                       |

## Как использовать API GetChartArea с SDK

### Спецификация API GetChartArea

<a href="https://apireference.aspose.cloud/cells/#/ChartArea/GetChartArea" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "ChartArea": {
    "Area": {
      "BackgroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "FillFormat": { "Type": "Automatic" },
      "ForegroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": false,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "IsAuto": false,
      "IsAutomaticColor": false,
      "IsVisible": false,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": "255", "R": "0", "G": "0", "B": "0" },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": false,
    "IsInnerMode": false,
    "Shadow": false,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории GitHub</a>.

Ниже приведены примеры кода, демонстрирующие вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartArea-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartArea-get-chart-area.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartArea-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_info-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartArea-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartArea-get-chart-area.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartArea-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "e00e3bbfdf94f400244f1974c3488036" >}}
{{< /tab >}}

{{< /tabs >}}

**Общий HTTP-запрос (например, с использованием fetch):**

```javascript
fetch('https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea', {
  method: 'GET',
  headers: {
    'Content-Type': 'application/json',
    'Accept': 'application/json',
    'Authorization': 'Bearer <jwt token>'
  }
})
  .then(response => response.json())
  .then(data => console.log(data));
```