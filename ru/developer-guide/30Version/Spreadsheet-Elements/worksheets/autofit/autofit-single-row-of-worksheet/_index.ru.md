---
title: "Автоматическая подгонка строки в рабочей книге Excel"
second_title: "Документ"
linktitle: "Строка"
type: docs
url: /ru/worksheets/autofit/row/
aliases: [  /ru/autofit-single-row-of-worksheet/ ]
description: "Узнайте, как использовать Aspose.Cells Cloud REST API для автоматической подгонки строки в рабочей книге Excel. Включает endpoint, параметры, аутентификацию, обработку ошибок, cURL-запрос и примеры SDK."
keywords: "автоматическая подгонка строки, Aspose.Cells Cloud, Excel API, REST, рабочий лист, SDK, электронная таблица, облачный API"
weight: 30
ArticleTitle: "Автоматическая подгонка строки в рабочей книге Excel с помощью Aspose.Cells Cloud API"
---

Этот REST API **автоматически подгоняет строку** в рабочей книге Excel.

## Безопасность и аутентификация
Aspose.Cells Cloud API защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **Параметры запроса**

| Имя параметра    | Тип    | Расположение | Описание                                                                                                                                                                                                  |
| ----------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| name              | string  | path     | Имя файла Excel.                                                                                                                                                                                  |
| sheetName         | string  | path     | Имя рабочего листа.                                                                                                                                                                                   |
| rowIndex          | integer | query    | Индекс строки (начиная с 0), которую необходимо подогнать.                                                                                                                                                                      |
| firstColumn       | integer | query    | Индекс первого столбца, включённого в операцию.                                                                                                                                                         |
| lastColumn        | integer | query    | Индекс последнего столбца, включённого в операцию.                                                                                                                                                          |
| autoFitterOptions | object  | body     | Объект, управляющий поведением подгонки (например, следует ли учитывать объединённые ячейки, перенос текста и т.д.). См. [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="Управляет поведением подгонки"}. |
| folder            | string  | query    | Папка, в которой хранится файл.                                                                                                                                                                             |
| storageName       | string  | query    | Имя хранилища.                                                                                                                                                                                         |

**Пример JSON-тела `autoFitterOptions`**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### Определения сущностей

| Сущность             | Описание                                                                              |
| ------------------- | ---------------------------------------------------------------------------------------- |
| `rowIndex`          | Индекс целевой строки (начиная с 0).                                                      |
| `firstColumn`       | Начальный столбец для операции автоматической подгонки.                                               |
| `lastColumn`        | Конечный столбец для операции автоматической подгонки.                                                 |
| `autoFitterOptions` | Необязательные настройки, влияющие на то, как выполняется подгонка строки (объединённые ячейки, перенос текста и т.д.). |

[OpenAPI Specification](/cells/#/Worksheets/PostAutofitWorksheetRow) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует вызов API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| Поле    | Описание                                |
| ------- | ------------------------------------------ |
| Code    | `200` — запрос выполнен успешно.                 |
| Status  | `"OK"` — строка успешно подогнана. |

{{< /tab >}}

{{< /tabs >}}

## Обработка ошибок

API возвращает стандартные HTTP-коды состояния. Типичные ответы об ошибках для этого endpoint:

| HTTP-код | Пример полезной нагрузки                                 | Значение                                                                           |
| -------- | --------------------------------------------------------- | --------------------------------------------------------------------------------- |
| 400      | `{ "Code": 400, "Message": "Row index out of range." }`   | Указанный `rowIndex` отсутствует в рабочем листе.                          |
| 401      | `{ "Code": 401, "Message": "Invalid or expired token." }` | Аутентификация не удалась — проверьте JWT-токен и убедитесь, что запрос передаётся по HTTPS. |
| 404      | `{ "Code": 404, "Message": "File not found." }`           | Указанный файл Excel или рабочий лист не найден.                          |
| 500      | `{ "Code": 500, "Message": "Internal server error." }`    | Возникла непредвиденная проблема на стороне сервера.                                       |

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"}.

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**См. также:** [Автоматическая подгонка столбца](/worksheets/autofit/column/), [Автоматическая подгонка строк](/worksheets/autofit/rows/), [AutoFitterOptions](/cells/auto-fitter-options).