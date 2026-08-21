---
title: "Удаление фигуры по индексу на листе Excel"
second_title: "Документ"
linktitle: "Удалить"
type: docs
url: /ru/shapes/delete/
aliases: [/ru/delete-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud, удаление фигуры, индекс фигуры, лист Excel, REST API, SDK"
description: "Используйте Aspose.Cells Cloud REST API для удаления фигуры по её индексу на листе Excel. API доступно через множество SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) и поддерживает различные варианты хранения."
weight: 50
---

Этот REST API удаляет фигуру на листе Excel.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### **Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                    |
| ------------- | ------ | ------------ | ------------------------------------------- |
| name          | string | path         | Имя файла рабочей книги.                    |
| sheetName     | string | path         | Имя листа.                                  |
| shapeindex    | integer| path         | Индекс фигуры в списке фигур листа.         |
| folder        | string | query        | Папка, в которой хранится рабочая книга.   |
| storageName   | string | query        | Имя хранилища.                              |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShape) определяет публично доступное программное интерфейсное решение и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать инструмент командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Приведённый ниже пример демонстрирует, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/1" \
-X DELETE \
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

Использование SDK — это самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода показывают, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}