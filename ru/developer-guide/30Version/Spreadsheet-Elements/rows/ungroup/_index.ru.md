---
title: "Отгруппировка строк на листе Excel"
second_title: "Документ"
linktitle: "Отгруппировка"
type: docs
url: /ru/rows/ungroup/
aliases: [  /ru/ungroup-rows-in-excel-worksheet/ ]
keywords: "отгруппировка строк, Excel, Aspose.Cells Cloud, REST API, SDK, электронная таблица"
description: "Узнайте, как отгруппировать строки на листе Excel с помощью REST API и SDK Aspose.Cells Cloud для различных языков программирования."
weight: 70
---

Этот REST API отгруппировывает строки на листе Excel.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/ungroup
```

### **Параметры запроса**

| Имя параметра | Тип    | Местоположение | Описание                                                                 |
| ------------- | ------ | -------------- | ------------------------------------------------------------------------ |
| name          | string | path           | Имя рабочей книги.                                                       |
| sheetName     | string | path           | Имя листа.                                                               |
| firstIndex    | integer | query         | Начальный индекс (отсчитываемый от нуля) первой строки для отгруппировки. |
| lastIndex     | integer | query         | Конечный индекс (отсчитываемый от нуля) последней строки для отгруппировки. |
| isAll         | boolean | query         | Если **true**, все строки в указанном диапазоне будут отгруппированы.    |
| folder        | string | query          | Папка, содержащая рабочую книгу.                                         |
| storageName   | string | query          | Имя хранилища, в котором расположена рабочая книга.                      |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetRows) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует, как выполнять вызовы к облачному API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/ungroup?firstIndex=1&lastIndex=5&isAll=true" \
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

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей и позволяет сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUngroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUngroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUngroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUngroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUngroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUngroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUngroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUngroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}