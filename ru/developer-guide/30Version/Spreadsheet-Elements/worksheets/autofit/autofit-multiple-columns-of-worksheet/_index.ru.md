---
title: "Автоподбор нескольких столбцов на листе Excel"
second_title: "Документ"
linktitle: "Столбцы"
type: docs
url: /ru/worksheets/autofit/columns/
aliases: [  /ru/autofit-multiple-columns-of-worksheet/ ]
keywords: "Aspose.Cells, автоподбор столбцов, Excel API, облачная таблица, REST"
description: "Узнайте, как выполнить автоподбор нескольких столбцов на листе Excel с помощью Aspose.Cells Cloud REST API (версия 3.0). Включает endpoint, параметры, пример cURL, обработку ошибок и фрагменты кода SDK для C#, Java, Python и других языков."
weight: 20
---

Этот REST API выполняет **автоподбор нескольких столбцов** на листе Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **Параметры запроса**

| Имя параметра      | Тип    | Расположение | Описание                                                                                                                                     |
| ------------------- | ------ | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| name                | string | path         | Имя файла.                                                                                                                                   |
| sheetName           | string | path         | Имя листа.                                                                                                                                   |
| firstColumn         | integer | query       | Индекс начального столбца.                                                                                                                   |
| lastColumn          | integer | query       | Индекс конечного столбца.                                                                                                                    |
| autoFitterOptions\* | object  | body        | Параметры автоподбора (см. [Параметры автоподбора](/ru/cells/auto-fitter-options/)). Включает `AutoFitMergedCells`, `IgnoreHidden` и `OnlyAuto`. |
| firstRow            | integer | query       | Индекс начальной строки для автоподбора (**необязательно**).                                                                                 |
| lastRow             | integer | query       | Индекс конечной строки для автоподбора (**необязательно**).                                                                                  |
| folder              | string  | query       | Путь к папке в хранилище (**необязательно**).                                                                                                |
| storageName         | string  | query       | Имя хранилища (**необязательно**).                                                                                                           |

\*Имя параметра отображается как ссылка на соответствующую документацию.

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
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

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}