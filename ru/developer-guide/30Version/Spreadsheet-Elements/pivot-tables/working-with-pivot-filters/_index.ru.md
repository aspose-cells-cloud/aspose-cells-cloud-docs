---
title: "Работа с фильтрами сводных таблиц"
second_title: "Документ"
linktype: "Фильтры"
type: docs
url: /ru/pivot-tables/add-filters/
aliases: [  /ru/working-with-pivot-filters/ ]
keywords: "Aspose.Cells, сводная таблица, фильтр, REST API, облако"
description: "Узнайте, как добавлять, получать и удалять фильтры сводных таблиц с помощью REST API Aspose.Cells Cloud. Включает синтаксис запроса, обязательные параметры, пример cURL и фрагменты кода SDK для C# и Go."
weight: 50
ArticleTitle: "Работа с фильтрами сводных таблиц — документация Aspose.Cells Cloud"
---

Этот REST API добавляет **фильтр сводной таблицы** к сводной таблице, расположенной по указанному индексу.

**Необходимые условия**  
Перед вызовом этого конечного узла вы должны:

- Сгенерировать действительный токен доступа OAuth/JWT и включить его в заголовок `Authorization`.  
- Убедиться, что целевая рабочая книга хранится в облачной папке, к которой у вас есть доступ (указать `folder` и необязательно `storageName`).  
- Использовать версию API Aspose.Cells Cloud не ниже 3.0.

## API PutWorksheetPivotTableFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра       | Тип     | Расположение | Описание                                                                                       |
| ------------------- | ------- | ------------ | ---------------------------------------------------------------------------------------------- |
| **name**            | string  | путь         | Имя файла Excel.                                                                               |
| **sheetName**       | string  | путь         | Рабочий лист, содержащий сводную таблицу.                                                      |
| **pivotTableIndex** | integer | путь         | Индекс сводной таблицы (начиная с 0), к которой будет применён фильтр.                         |
| **filter**          | object  | тело         | Объект JSON, определяющий настройки фильтра. См. таблицу **схемы filter** ниже.               |
| **needReCalculate** | boolean | query        | Если **true**, принудительно пересчитывает рабочую книгу после добавления фильтра. По умолчанию **false**. |
| **folder**          | string  | query        | Папка в облачном хранилище, где расположен файл.                                               |
| **storageName**     | string  | query        | Имя облачного хранилища.                                                                       |

**Схема filter**

| Свойство                     | Тип     | Описание                                                                                     |
| ---------------------------- | ------- | -------------------------------------------------------------------------------------------- |
| **AutoFilter**               | object  | Настройки автофильтра; можно опустить, если не используется.                                |
| **EvaluationOrder**          | integer | Порядок, в котором применяется фильтр.                                                       |
| **FieldIndex**               | integer | Индекс поля (начиная с 0), к которому применяется фильтр.                                    |
| **FilterType**               | string  | Тип фильтра (например, `Value`, `Count`, `Label`).                                          |
| **MeasureFldIndex**          | integer | Индекс поля измерения, если применимо.                                                       |
| **MemberPropertyFieldIndex** | integer | Индекс поля свойства элемента, если применимо.                                              |
| **Name**                     | string  | Необязательное имя фильтра.                                                                  |
| **Value1**                   | string  | Первое значение, используемое фильтром (например, нижняя граница диапазона).                |
| **Value2**                   | string  | Второе значение, используемое фильтром (например, верхняя граница диапазона).               |
| **CustomFilters**            | array   | Коллекция пользовательских объектов фильтра (каждый содержит `FilterOperatorType`, `Value1`, `Value2`). |
| **DynamicFilter**            | object  | Настройки динамического фильтра (например, Top10, Bottom10).                                 |
| **IconFilter**               | object  | Настройки фильтра по иконкам.                                                                |
| **Top10Filter**              | object  | Настройки фильтра Top10/Bottom10.                                                            |
| **ColorFilter**              | object  | Настройки фильтра по цвету.                                                                  |
| **Visibledropdown**          | boolean | Указывает, отображается ли раскрывающийся список фильтра.                                   |

> **Примечание:** Все параметры, перечисленные выше, являются обязательными, если в описании API явно не указано иное.

### Коды ответа

| Код | Значение                                         |
| --- | ------------------------------------------------ |
| 200 | Фильтр успешно добавлен.                         |
| 400 | Неверный запрос — недопустимые параметры.        |
| 401 | Неавторизовано — отсутствует или недействителен токен. |
| 404 | Не найдено — рабочая книга или сводная таблица отсутствует. |
| 500 | Внутренняя ошибка сервера.                       |

**Рекомендации по использованию**  
- Минимизируйте размер объектов фильтров: большие определения могут увеличить задержку ответа.  
- Вызовы являются идемпотентными: повторное добавление одного и того же фильтра не создаёт дубликатов.  
- Учитывайте лимит API — 100 запросов в минуту на аккаунт.  

*Дополнительные примечания:*  
- Максимальный размер определения фильтра — 1 МБ; более крупные нагрузки будут отклонены с кодом 400.  
- При использовании `needReCalculate=true` время ответа может увеличиться для больших рабочих книг.  

Вы можете ознакомиться с полным описанием OpenAPI здесь:  
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### Пример запроса cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
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

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки под Aspose.Cells Cloud. SDK обрабатывают низкоуровневые детали, позволяя вам сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud см. в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Ниже приведены примеры кода, демонстрирующие вызов веб-сервисов Aspose.Cells с помощью различных SDK.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // Инициализация клиента API (замените на ваши учётные данные)
        var config = new Configuration
        {
            ClientId = "YOUR_CLIENT_ID",
            ClientSecret = "YOUR_CLIENT_SECRET"
        };
        var apiInstance = new CellsApi(config);

        // Создание объекта фильтра
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // Подготовка запроса
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // Выполнение запроса
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Статус: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

Дополнительные операции, связанные со сводными таблицами, описаны в документации по **добавлению**, **удалению** и **очистке** фильтров.