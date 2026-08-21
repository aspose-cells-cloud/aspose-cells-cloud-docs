---
title: "Перемещение сводной таблицы в файле Excel"
second_title: "Документ"
linktype: "Move"
type: docs
url: "/pivot-tables/move/"
aliases: [/move-pivot-table/]
keywords: "Aspose.Cells Cloud, перемещение сводной таблицы, Excel, REST API, SDK, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Узнайте, как с помощью REST API Aspose.Cells Cloud переместить сводную таблицу внутри рабочей книги Excel. SDK доступны для Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby и Swift."
weight: 120
---

Этот REST API позволяет перемещать сводную таблицу внутри рабочей книги Excel.

**Необходимые условия:** Перед вызовом данной операции у вас должен быть действующий JWT-токен доступа, а рабочая книга должна храниться в облачном хранилище Aspose Cloud. В зависимости от необходимости укажите параметры `folder` (папка) и `storageName` (имя хранилища).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Move
```

### **Параметры запроса**

| Имя параметра  | Тип    | Расположение | Описание                                                  |
| --------------- | ------ | ------------ | --------------------------------------------------------- |
| name            | string | path         | Имя файла Excel.                                          |
| sheetName       | string | path         | Имя рабочего листа, содержащего сводную таблицу.         |
| pivotTableIndex | integer| path         | Индекс (начиная с нуля) перемещаемой сводной таблицы.     |
| fieldIndex      | integer| query        | Индекс поля сводной таблицы, которое нужно переместить.   |
| from            | string | query        | Исходная область поля (например, `Row` или `Column`).    |
| to              | string | query        | Целевая область поля (например, `Row` или `Column`).      |
| folder          | string | query        | Папка в хранилище, где расположен файл.                   |
| storageName     | string | query        | Имя облачного хранилища.                                  |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldMoveTo) определяет публично доступное программное API и позволяет выполнять взаимодействие по протоколу REST непосредственно из веб-браузера.

Для доступа к веб-сервисам Aspose.Cells вы можете использовать утилиту командной строки cURL. Приведённый ниже пример демонстрирует, как выполнять вызовы к облачному API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Move?fieldIndex=0&from=C1&to=C10" \
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

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// В продакшене используйте HTTPS-эндпоинты.
public void Run_PivotTable_Move()
{
    url = @"https://api.aspose.com/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null}, ... ],\"DestinationWorksheet\":\"Sheet2\",\"IsInsert\":false}";
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/Move?row=10&column=10&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Move?fieldIndex=1&from=Row&to=Column&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "60360c7d035abd1b2c9e36c68c9f00fb" >}}

{{< /tab >}}

{{< /tabs >}}