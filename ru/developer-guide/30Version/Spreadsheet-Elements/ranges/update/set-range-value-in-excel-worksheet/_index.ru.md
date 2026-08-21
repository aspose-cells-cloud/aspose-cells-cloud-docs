---
title: "Установка значения диапазона в рабочем листе Excel"
second_title: "Документ"
linktype: "Установка значений"
type: docs
url: /ranges/update/values/
aliases: [/set-range-value-in-excel-worksheet/]
keywords: "Aspose.Cells, Excel API, установка значения диапазона, REST API, облачное SDK, обновление рабочего листа"
description: "Узнайте, как установить значение ячейки или диапазона в книге Excel с использованием Aspose.Cells Cloud REST API (версия 3.0). Включает конечную точку, параметры, пример cURL, примеры кода SDK и обработку ошибок."
weight: 72
ArticleTitle: "Установка значения диапазона в рабочем листе Excel — Aspose.Cells Cloud API"
---

Используйте этот REST API для установки значения в указанный диапазон. При необходимости значение преобразуется в другой тип данных, а формат числа ячейки сбрасывается.

**Необходимые условия**  
- Действующая учетная запись Aspose Cloud.  
- JWT-токен, включающий область `Cells.ReadWrite`.  
- Книга уже должна быть загружена в целевое хранилище.

## API PostWorksheetCellsRangeValue

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

Параметры запроса:

| Имя параметра | Тип    | Расположение | Описание                                                 |
|---------------|--------|--------------|----------------------------------------------------------|
| name          | string | path         | Имя книги                                                |
| sheetName     | string | path         | Имя рабочего листа                                       |
| value         | string | query        | Входное значение                                         |
| range         | object | body         | Объект диапазона на рабочем листе                        |
| isConverted   | boolean| query        | Указывает, следует ли преобразовывать входное значение  |
| setStyle      | boolean| query        | Указывает, следует ли применять стиль к целевым ячейкам |
| folder        | string | query        | Папка книги                                              |
| storageName   | string | query        | Имя хранилища                                           |

**Пример объекта `range`**, который можно отправить в теле запроса:

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия прямо из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример показывает, как вызвать облачный API с помощью cURL. **Обязательно включите действующий JWT-токен в заголовке `Authorization`.**

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Схема ответа**

| Поле    | Тип     | Описание                                             |
|---------|---------|------------------------------------------------------|
| Code    | integer | Код HTTP-статуса операции.                          |
| Status  | string  | Краткое описание результата (например, "OK").       |
| Message | string  | Подробное сообщение об ошибке при неудачном запросе (необязательно). |
| Result  | object  | Дополнительные данные, возвращаемые при успешных вызовах (необязательно). |

**Возможные HTTP-коды состояния**

- **200 OK** – значение диапазона успешно установлено.  
- **400 Bad Request** – недопустимые параметры или некорректно сформированное тело запроса.  
- **401 Unauthorized** – отсутствует или недействителен JWT-токен.  
- **403 Forbidden** – недостаточно прав для выполнения запрошенной операции.  
- **404 Not Found** – указанная книга, рабочий лист или диапазон не существует.  
- **500 Internal Server Error** – непредвиденная ошибка сервера.

*Пример ответа об ошибке для кода 400 Bad Request:*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "В объекте 'range' отсутствуют обязательные поля."
}
```

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Посетите [репозиторий на GitHub](https://github.com/aspose-cells-cloud), чтобы ознакомиться со полным списком облачных SDK Aspose.Cells.

Следующие примеры кода демонстрируют, как выполнять вызовы к веб-сервисам Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}