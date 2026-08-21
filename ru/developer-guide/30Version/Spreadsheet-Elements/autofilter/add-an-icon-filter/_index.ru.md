---
title: "Добавление фильтра по значку в рабочий лист Excel"
second_title: "Документ"
linktype: "Добавление фильтра по значку"
type: docs
url: /autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/,/autofilter/add-an-icon-filter/]
keywords: "Aspose.Cells Cloud, Excel, фильтр по значку, автофильтр, REST API"
description: "Узнайте, как добавить фильтр по значку в рабочий лист Excel с помощью REST API Aspose.Cells Cloud, включая детали запроса, пример cURL, примеры кода SDK и обработку ошибок."
weight: 65
ArticleTitle: "Добавление фильтра по значку в рабочий лист Excel — документация Aspose.Cells Cloud"
---

## REST API

Этот REST API добавляет **фильтр по значку** в рабочий лист Excel с использованием **Aspose.Cells Cloud REST API**.

**Фон:** Фильтр по значку применяет визуальный набор значков к ячейкам на основе их значений, позволяя быстро анализировать тренды данных визуально. Типичные сценарии использования включают подсветку показателей эффективности, индикаторов статуса или категоризацию значений с помощью значков в форме дорожных светофоров непосредственно в рабочих листах Excel.


```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud безопасны и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе токена JWT</a>.


### Параметры запроса:

| Имя параметра | Тип    | Расположение | Описание |
|---------------|--------|-------------|----------|
| name          | string | Path        | Имя рабочей книги. |
| sheetName     | string | Path        | Имя рабочего листа. |
| range         | string | Query       | Диапазон ячеек (например, `A1:B1`), к которому будет применён фильтр. |
| fieldIndex    | integer| Query       | Индекс столбца (начиная с нуля), к которому применяется фильтр. |
| iconSetType   | string | Query       | Набор значков для использования. Допустимые значения: `Arrows3`, `ArrowsGray3`, `Flags3`, `Signs3`, `Symbols3`, `Symbols32`, `TrafficLights31`, `TrafficLights32`, `Arrows4`, `ArrowsGray4`, `Rating4`, `RedToBlack4`, `TrafficLights4`, `Arrows5`, `ArrowsGray5`, `Quarters5`, `Rating5`, `Stars3`, `Boxes5`, `Triangles3`, `None`, `CustomSet`, `Smilies3`, `ColorSmilies3`. |
| iconId        | integer| Query       | Идентификатор конкретного значка в выбранном наборе значков. |
| matchBlanks   | boolean| Query       | Определяет, включать ли пустые ячейки (`true` или `false`). |
| refresh       | boolean| Query       | Указывает, следует ли обновить фильтр после применения (`true` или `false`). |
| folder        | string | Query       | Папка, содержащая исходную рабочую книгу. |
| storageName   | string | Query       | Имя хранилища, в котором находится рабочая книга. |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание |
|-----|-----------------------------|----------|
| 200 | OK (ОК)                    | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий токен JWT. |
| 413 | Payload Too Large (Слишком большой объём полезной нагрузки) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Как использовать API PutWorksheetIconFilter с SDK

### Спецификация API PutWorksheetIconFilter

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать инструмент командной строки cURL для лёгкого доступа к веб-сервисам Aspose.Cells. Следующий пример показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Возможные коды статуса ответа:

| Код | Описание |
|-----|----------|
| 200 | Фильтр успешно применён. |
| 400 | Неверный запрос — отсутствуют или недопустимы параметры. |
| 401 | Неавторизовано — недействительный или отсутствующий токен аутентификации. |
| 404 | Рабочая книга, рабочий лист или указанный диапазон не найдены. |
| 500 | Внутренняя ошибка сервера. |
{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud) для получения полного списка SDK Aspose.Cells Cloud.

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Дополнительные возможности автофильтра см. в документации по **[добавлению цветового фильтра](/autofilter/add-color-filter/)**, **[добавлению фильтра по дате](/autofilter/add-date-filter/)** и **[очистке автофильтра](/autofilter/clear-autofilter/)**.