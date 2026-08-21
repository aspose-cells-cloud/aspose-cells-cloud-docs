---
title: "Вставка фильтра-среза в объект ListObject в Excel — API Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Вставить срез"
type: docs
keywords: "Aspose.Cells, срез Excel, ListObject, REST API, облачный SDK"
description: "Узнайте, как добавить срез в объект ListObject в Excel с помощью облачного REST API Aspose.Cells Cloud (v3.0). Включает эндпоинт, параметры, аутентификацию, пример запроса cURL и JSON-ответ."
weight: 20
ArticleTitle: "Вставка фильтра-среза в объект ListObject в Excel — API Aspose.Cells Cloud"
---

Этот REST API вставляет срез для объекта списка на листе Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### Параметры запроса

| Имя параметра  | Тип    | Расположение | Описание                                                                 |
| --------------- | ------ | ------------ | ------------------------------------------------------------------------ |
| name            | String | Path         | Имя файла Excel.                                                        |
| sheetName       | String | Path         | Имя листа, содержащего объект списка.                                   |
| listObjectIndex | Integer| Path         | Индекс объекта списка (начиная с нуля), к которому будет добавлен срез. |
| columnIndex     | Integer| Query        | Индекс столбца (начиная с нуля), по которому строится срез.             |
| destCellName    | String | Query        | Ссылка на ячейку (например, **A1**), где будет размещён срез.           |
| folder          | String | Query        | Папка в хранилище, где находится файл Excel.                            |
| storageName     | String | Query        | Имя облачного сервиса хранения Aspose.Cloud.                             |

Вы можете использовать утилиту командной строки cURL для вызова API:

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Примечание:** Запрос требует действительного JWT-токена, полученного из сервиса аутентификации Aspose.Cloud. Этот эндпоинт не требует тела запроса; отправьте пустой JSON-объект `{}`, если ваша клиентская библиотека требует наличие полезной нагрузки.

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **Заголовок ответа:** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                                     |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK (OK)                     | Фильтр успешно применён; ответ содержит детали операции.    |
| 400  | Bad Request (Неверный запрос)| Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано)| Неверный или отсутствующий JWT-токен.                        |
| 413  | Payload Too Large (Слишком большой объём полезной нагрузки)| Загруженный файл превышает лимит размера.                |
| 500  | Internal Server Error (Внутренняя ошибка сервера)| Непредвиденная ошибка сервера.                              |

### Обработка ошибок

При возникновении ошибки API возвращает JSON-объект с полем `ErrorMessage`, описывающим проблему. Проанализируйте код HTTP-статуса и поле `ErrorMessage`, чтобы определить необходимые действия по устранению ошибки.

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя работу с низкоуровневыми деталями и позволяет сосредоточиться на задачах проекта. Посетите репозиторий GitHub, чтобы ознакомиться с полным списком облачных SDK Aspose.Cells.

Следующие примеры кода демонстрируют вызов веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}