---
title: "Сортировка данных ListObject в рабочем листе Excel"
second_title: "Документ"
linktitle: "Сортировка"
type: docs
url: /ru/list-objects/sort-data/
aliases: [  /ru/get-a-list-object-or-table-inside-the-worksheet/ , /ru/tables/sort-data/ ]
keywords: "Aspose.Cells Cloud, Excel, ListObject, Сортировка данных, REST API, Рабочий лист"
description: "Узнайте, как сортировать данные ListObject (таблицы) в рабочем листе Excel с помощью REST API Aspose.Cells Cloud (версия 3.0). Приведены конечная точка, параметры, пример запроса cURL и примеры SDK."
weight: 40
ArticleTitle: "Сортировка данных ListObject в рабочем листе Excel – API Aspose.Cells Cloud"
---

**Необходимые условия**  
Для вызова этого API требуется действительный JWT-токен доступа Aspose Cloud, а также загруженная рабочая книга в облачное хранилище Aspose Cloud. В каждый запрос необходимо добавлять заголовок `Authorization: Bearer <jwt token>`.

Этот REST API выполняет сортировку данных таблицы в рабочем листе Excel.  
Для использования этой операции укажите имя рабочей книги, имя рабочего листа и индекс целевого ListObject, а также JSON-тело `dataSorter`, определяющее критерии сортировки.

## API PostWorksheetListObjectSortTable

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются безопасными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Параметры запроса**

| Имя параметра  | Тип    | Путь / Строка запроса / HTTP-тело | Описание                                                                                                     |
| --------------- | ------- | -------------------------- | --------------------------------------------------------------------------------------------------------------- |
| name            | string  | path                       | Имя файла Excel, хранящегося в облачном хранилище Aspose Cloud.                                                      |
| sheetName       | string  | path                       | Имя рабочего листа, содержащего ListObject.                                                         |
| listObjectIndex | integer | path                       | Индекс ListObject (таблицы) в рабочем листе (начиная с нуля).                                                |
| dataSorter      | object  | body                       | JSON-объект, определяющий параметры сортировки (например, `CaseSensitive`, `HasHeaders`, `KeyList`, `SortLeftToRight`). |
| folder          | string  | query                      | Путь к папке в хранилище, где расположен файл Excel.                                                         |
| storageName     | string  | query                      | Имя облачного хранилища Aspose Cloud.                                                                               |

**Примечания**  
Тело запроса должно быть допустимым JSON-объектом, соответствующим схеме `dataSorter`. Убедитесь, что рабочая книга, рабочий лист и ListObject существуют перед вызовом операции сортировки.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable) определяет публично доступное программное интерфейсное API и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
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

**Коды HTTP-статуса**

| Код статуса | Описание                              |
|------------|------------------------------------------|
| 200        | OK – сортировка успешно завершена.    |
| 400        | Bad Request – недопустимые параметры.       |
| 401        | Unauthorized – ошибка аутентификации.    |
| 404        | Not Found – рабочая книга, рабочий лист или ListObject не найдены. |
| 500        | Internal Server Error – внутренняя проблема сервера.|

**Параметры ответа**

| Параметр | Тип    | Описание                                 |
|-----------|---------|---------------------------------------------|
| Code      | integer | HTTP-код статуса, возвращаемый API.       |
| Status    | string  | Текстовое описание результата (например, "OK"). |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[Вернуться к обзору ListObjects](/ru/list-objects/)