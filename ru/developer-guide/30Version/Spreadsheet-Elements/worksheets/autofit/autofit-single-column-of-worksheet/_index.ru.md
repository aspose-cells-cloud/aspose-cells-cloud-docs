---
title: "Автоподбор ширины столбца в Excel с помощью Aspose.Cells Cloud API – Краткое руководство"
second_title: "Документ"
linktitle: "Столбец"
type: docs
url: /worksheets/autofit/column/
aliases: [/autofit-single-column-of-worksheet/]
keywords: "Aspose.Cells Cloud, автоподбор столбца, Excel API, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Узнайте, как автоматически изменить ширину одного столбца (или диапазона столбцов) на листе Excel с помощью Aspose.Cells Cloud REST API. Включает примеры cURL и SDK (C#, Java, Python и др.), а также полные данные о запросе и ответе."
weight: 10
---

Этот REST API автоматически настраивает ширину одного столбца или непрерывного диапазона столбцов на листе Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### Параметры запроса

| Имя параметра     | Тип     | Расположение | Описание                                                                                             |
| ----------------- | ------- | ------------ | ----------------------------------------------------------------------------------------------------- |
| name              | string  | path         | Имя файла Excel.                                                                                      |
| sheetName         | string  | path         | Имя листа.                                                                                            |
| firstColumn       | integer | query        | Нулевой индекс первого столбца, для которого выполняется автоподбор.                                  |
| lastColumn        | integer | query        | Нулевой индекс последнего столбца, для которого выполняется автоподбор.                               |
| autoFitterOptions | object  | body         | Параметры, управляющие поведением автоподбора (см. [AutoFitterOptions](/cells/auto-filter-options)). |
| firstRow          | integer | query        | Нулевой индекс первой строки, учитываемой при вычислении ширины столбца.                              |
| lastRow           | integer | query        | Нулевой индекс последней строки, учитываемой при вычислении ширины столбца.                           |
| folder            | string  | query        | Папка в хранилище, где расположен файл.                                                               |
| storageName       | string  | query        | Имя сервиса хранилища.                                                                                |

### Ответы об ошибках

| HTTP-статус | Значение                                      | Пример JSON-тела                                          |
| ----------- | --------------------------------------------- | --------------------------------------------------------- |
| 400         | Неверные параметры                            | `{"Code":400,"Message":"Неверный параметр 'firstColumn'."}` |
| 401         | Неавторизован — отсутствует или недействителен JWT-токен | `{"Code":401,"Message":"Ошибка авторизации."}`            |
| 404         | Файл или лист не найдены                      | `{"Code":404,"Message":"Лист 'Sheet1' не найден."}`    |
| 500         | Внутренняя ошибка сервера                     | `{"Code":500,"Message":"Произошла непредвиденная ошибка."}` |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для вызова сервисов Aspose.Cells Cloud. Пример ниже демонстрирует, как вызвать эндпоинт автоподбора столбца.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
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

Использование SDK — это самый быстрый способ интеграции API в ваше приложение. SDK обрабатывают низкоуровневые детали, позволяя вам сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов эндпоинта автоподбора столбца с использованием различных SDK:

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