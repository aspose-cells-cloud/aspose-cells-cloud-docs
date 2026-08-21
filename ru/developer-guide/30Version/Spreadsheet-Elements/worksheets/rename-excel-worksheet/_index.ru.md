---
title: "Переименование листа Excel"
second_title: "Документ"
linktitle: "Переименовать"
type: docs
url: /worksheets/rename/
aliases: [/rename-excel-worksheet/]
keywords: "Aspose.Cells Cloud, переименование листа Excel, REST API, SDK для электронных таблиц, переименование листа, облачное хранилище"
description: "Переименовать лист в книге Excel с использованием REST API Aspose.Cells Cloud. SDK доступны для Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby и Swift."
weight: 20
---

Этот REST API позволяет переименовать лист Excel.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rename
```

### **Параметры запроса**

| Имя параметра | Тип   | Расположение | Описание                                   |
| ------------- | ----- | ------------ | ------------------------------------------ |
| name          | string | path        | Имя файла Excel.                           |
| sheetName     | string | path        | Текущее имя листа, который требуется переименовать. |
| newname       | string | query       | Новое имя для листа.                       |
| folder        | string | query       | Путь к папке в хранилище (необязательно).  |
| storageName   | string | query       | Имя хранилища (необязательно).             |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostRenameWorksheet) определяет общедоступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для простого доступа к веб-сервисам Aspose.Cells вы можете использовать утилиту командной строки cURL. Пример ниже демонстрирует, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/rename?newname=newSheet" \
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

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя работу с низкоуровневыми деталями, позволяя вам сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют выполнение вызовов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostRenameWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-RenameWorksheet-rename-excel-worksheeet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostRenameWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-rename_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "RenameExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-RenameWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-RenameWorksheet-rename-excel-worksheeet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-RenameWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "accf2723cfaa2a328d3dea355156e4d9" >}}

{{< /tab >}}

{{< /tabs >}}