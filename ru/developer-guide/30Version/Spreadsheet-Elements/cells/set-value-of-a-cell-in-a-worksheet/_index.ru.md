---
title: "Установка значения ячейки – Справочник по API Aspose.Cells Cloud (v3.0)"  
type: docs  
url: /set-value-of-a-cell-in-a-worksheet/  
weight: 70  
keywords: "Aspose Cells API установка значения ячейки, обновление ячейки Excel через REST, пример cURL для Aspose.Cells Cloud"  
description: "Узнайте, как установить значение конкретной ячейки в электронной таблице Excel с помощью REST API Aspose.Cells Cloud. Включает синтаксис запроса, параметры, пример HTTPS cURL и примеры кода SDK."  
---  

Этот REST API позволяет установить **значение ячейки** в файле Excel.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

## Безопасность и аутентификация

API Aspose.Cells Cloud защищены и требуют [аутентификации на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Параметры запроса**

| Имя           | Тип    | Местоположение | Описание                                            |
|---------------|--------|----------------|-----------------------------------------------------|
| name          | string | path           | Имя документа Excel (включая расширение).           |
| sheetName     | string | path           | Имя рабочего листа (с учетом регистра).             |
| cellName      | string | path           | Адрес целевой ячейки в формате A1 (например, `A1`). |
| value         | string | query          | Значение, присваиваемое ячейке.                     |
| type          | string | query          | Тип данных значения (`int`, `string`, `float` и т.д.). |
| formula       | string | query          | Формула, применяемая к ячейке (необязательно).      |
| folder        | string | query          | Папка, содержащая документ (необязательно).         |
| storageName   | string | query          | Имя хранилища, в котором находится файл (необязательно). |

## **Ответ**

Возвращает объект CellResponse.

- **Обзор полей ответа**

| Поле            | Тип     | Описание                                                  |
| --------------- | ------- | --------------------------------------------------------- |
| `Name`          | string  | Адрес ячейки (например, `F341`).                          |
| `Row`           | integer | Индекс строки (начиная с 0).                              |
| `Column`        | integer | Индекс столбца (начиная с 0).                             |
| `Value`         | string  | Отображаемое значение ячейки.                            |
| `Type`          | string  | Тип данных ячейки (например, `IsString`).                |
| `Formula`       | string  | Текст формулы, если ячейка содержит формулу.             |
| `IsFormula`     | bool    | Указывает, содержит ли ячейка формулу.                   |
| `IsMerged`      | bool    | Указывает, является ли ячейка частью объединённого диапазона. |
| `IsArrayHeader` | bool    | Указывает, является ли ячейка заголовком массива.        |
| `IsInArray`     | bool    | Указывает, принадлежит ли ячейка массиву.                |
| `IsErrorValue`  | bool    | Указывает, содержит ли ячейка ошибочное значение.       |
| `IsInTable`     | bool    | Указывает, находится ли ячейка внутри таблицы.          |
| `IsStyleSet`    | bool    | Указывает, применён ли к ячейке стиль.                   |
| `HtmlString`    | string  | HTML-представление значения ячейки.                      |
| `Style.link`    | object  | Ссылка на ресурс стиля.                                  |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                             |
|------|----------------------------|------------------------------------------------------|
| 200  | OK (ОК)                    | Фильтр успешно применён; ответ содержит детали операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован) | Недействительный или отсутствующий токен JWT.       |
| 413  | Payload Too Large (Слишком большой payload) | Загружаемый файл превышает допустимый размер. |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Как использовать API PostWorksheetCellSetValue с SDK

### Спецификация API PostWorksheetCellSetValue

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) определяет публично доступное программное интерфейсное описание, позволяющее разработчикам напрямую вызывать REST-эндпоинты из браузера или любого HTTP-клиента.

Вы можете использовать утилиту командной строки **cURL** для вызова веб-сервисов Aspose.Cells. Пример ниже демонстрирует, как установить значение ячейки с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK ускоряет разработку, скрывая низкоуровневые детали, что позволяет сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}