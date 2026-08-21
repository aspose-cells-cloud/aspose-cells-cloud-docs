---
title: "Получение стиля ячейки из рабочего листа – Aspose.Cells Cloud API"
type: docs
url: /ru/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, REST API, стиль ячейки, электронная таблица, облачный SDK, документация API"
description: "Узнайте, как получить стиль конкретной ячейки в рабочем листе Excel с помощью Aspose.Cells Cloud REST API v3. Включает пример cURL, схему ответа, коды статусов и фрагменты кода SDK."
ArticleTitle: "Получение стиля ячейки из рабочего листа с помощью Aspose.Cells Cloud API – Подробное руководство"
---

Используйте этот REST API для получения **стиля** ячейки в рабочем листе Excel.

## GetWorksheetCellStyle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса


| Имя параметра | Тип    | Расположение | Описание                                   |
| ------------- | ------ | ----------- | ------------------------------------------ |
| name          | string | path        | Имя документа Excel.                       |
| sheetName     | string | path        | Имя рабочего листа.                        |
| cellName      | string | path        | Адрес ячейки (например, A1).               |
| folder        | string | query       | Папка, содержащая файл.                    |
| storageName   | string | query       | Имя хранилища, которое следует использовать.|


### **Ответ**

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**Коды HTTP-статуса**

| Код  | Значение                   | Описание                                                              |
|------|----------------------------|-----------------------------------------------------------------------|
| 200  | OK (ОК)                    | Фильтр успешно применён; ответ содержит сведения об операции.        |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.                        |
| 413  | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает предельный размер.                   |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                  |

**Ответы с ошибками**  
Типичные полезные нагрузки ошибок для этой конечной точки следуют стандартному формату ошибок Aspose.Cells. Например, при коде 400 (Bad Request) возвращается:

```json
{
  "Code": 400,
  "Message": "Недопустимый параметр 'cellName'.",
  "Description": "Указанное имя ячейки не соответствует допустимому формату A1."
}
```

Аналогично, при коде 401 (Unauthorized) возвращается:

```json
{
  "Code": 401,
  "Message": "Ошибка аутентификации.",
  "Description": "JWT-токен отсутствует или недействителен."
}
```

## Как использовать API GetWorksheetCellStyle с SDK

### Спецификация API GetWorksheetCellStyle


[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
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

## Схема ответа

| Поле                      | Тип     | Описание                                                                 |
| ------------------------- | ------- | ------------------------------------------------------------------------ |
| **Style**                 | object  | Контейнер всех свойств, относящихся к стилю ячейки.                      |
| Style.Font                | object  | Параметры шрифта (имя, размер, цвет, флаги стиля).                        |
| Style.Font.Color          | object  | RGBA-значения цвета шрифта.                                               |
| Style.Font.IsBold         | boolean | `true`, если шрифт жирный.                                                |
| Style.Font.IsItalic       | boolean | `true`, если шрифт курсивный.                                             |
| Style.Font.IsStrikeout    | boolean | `true`, если шрифт зачеркнут.                                             |
| Style.Font.IsSubscript    | boolean | `true`, если шрифт нижний индекс.                                         |
| Style.Font.IsSuperscript  | boolean | `true`, если шрифт верхний индекс.                                        |
| Style.Font.Name           | string  | Название семейства шрифтов (например, **Calibri**).                      |
| Style.Font.Size           | number  | Размер шрифта в пунктах.                                                  |
| Style.Font.Underline      | string  | Стиль подчёркивания (например, **Single**).                               |
| Style.IsLocked            | boolean | Указывает, защищена ли ячейка от редактирования.                          |
| Style.IsTextWrapped       | boolean | `true`, если включено перенос текста по строкам.                         |
| Style.IsGradient          | boolean | `true`, если применён градиентный залив.                                  |
| Style.Pattern             | string  | Название паттерна заливки (например, **None**).                          |
| Style.BorderCollection    | array   | Список объектов границ, определяющих стиль линии, цвет и тип границы.    |
| Style.BackgroundColor     | object  | RGBA-значения цвета фона ячейки.                                          |
| Style.ForegroundColor     | object  | RGBA-значения цвета переднего плана ячейки.                              |
| …                         | …       | _(Остальные поля следуют той же структуре, что указана в справке API.)_   |

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода показывают, как вызывать веб-сервисы Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**См. также**  
- [Установка стиля ячейки](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [Получение значения ячейки](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)
---