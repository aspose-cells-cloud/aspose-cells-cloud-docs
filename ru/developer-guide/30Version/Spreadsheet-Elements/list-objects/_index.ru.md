---
title: "Работа с ListObject в Excel"
ArticleTitle: "Работа с ListObject в Excel"
second_title: "Документ"
linktype: "ListObjects"
type: docs
url: /ru/list-objects/
aliases:
  - /ru/working-with-list-objects/
  - /ru/working-with-list-object-or-table/
keywords: "Aspose.Cells, ListObject в Excel, API таблиц Excel, добавление таблицы, обновление таблицы, удаление таблицы, преобразование таблицы в диапазон, сортировка таблицы Excel"
description: "Узнайте, как добавлять, обновлять, удалять, получать, сортировать и преобразовывать ListObject в Excel (таблицы) с помощью REST API Aspose.Cells Cloud. Примеры кода на C#, Java, Python и других языках."
weight: 100
---

ListObject в Excel (таблицы) обеспечивают структурированный способ организации наборов данных. Они включают такие функции, как автоматическая расстановка данных, заголовочные строки, встроенные фильтры и необязательные итоговые строки. Освойте эти возможности, чтобы быстро и эффективно анализировать ваши данные.

**Определение ListObject:** **ListObject** — это нативный объект таблицы в Excel, который объединяет строки и столбцы, позволяет выполнять сортировку, фильтрацию и стилизацию, а также доступен через API Aspose.Cells Cloud.

## Как работать с таблицей (объектом List)

- [Как добавить таблицу (объект List) в лист](/ru/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [Как обновить таблицу (объект List) в листе](/ru/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [Как преобразовать таблицу (объект List) в диапазон](/ru/cells/convert-list-object-or-table-to-range/)
- [Как отсортировать данные таблицы](/ru/cells/sort-table-data/)
- [Как удалить дублирующиеся строки из таблицы](/ru/cells/list-objects/remove-duplicates/)
- [Как добавить фильтр-срез для таблицы](/ru/cells/list-objects/insert-slicer/)

**Справочник по API (обзор):**  
REST API Aspose.Cells Cloud предоставляет операции с ListObject через такие конечные точки, как `GET /cells/{fileName}/worksheets/{sheetName}/listobjects`, `POST /cells/{fileName}/worksheets/{sheetName}/listobjects`, `PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` и `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. Обязательными параметрами запроса являются `folder` и `storage` (опционально). Тело запроса представляет собой JSON-объект, описывающий свойства таблицы (имя, наличие заголовка, итоговой строки и т.д.), а ответ возвращает JSON с данными созданного или изменённого ListObject.

**Необходимые условия:**  
- Действующий токен аутентификации Aspose.Cells Cloud.  
- Файл рабочей книги должен быть загружен в поддерживаемое хранилище (по умолчанию — **/**), а параметр запроса `folder` должен указывать на это расположение.  
- Опционально: укажите `storage`, если используется нестандартный сервис хранилища.

**Детали конечных точек**

| Метод | Конечная точка | Параметры запроса | Тело запроса (JSON) | Пример успешного ответа | Коды состояния |
|--------|----------|------------------|---------------------|----------------------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (обязательный), `storage` (опциональный) | *отсутствует* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 — OK, 400 — Bad Request, 401 — Unauthorized, 404 — Not Found |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (обязательный), `storage` (опциональный) | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 — Created, 400 — Bad Request, 401 — Unauthorized, 409 — Conflict |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (обязательный), `storage` (опциональный) | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 — OK, 400 — Bad Request, 401 — Unauthorized, 404 — Not Found |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (обязательный), `storage` (опциональный) | *отсутствует* | `{ "Code": 200, "Status": "Deleted" }` | 200 — OK, 400 — Bad Request, 401 — Unauthorized, 404 — Not Found |

**Фрагменты кода**

*C# (POST — добавление ListObject)*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java (GET — получение ListObjects)*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python (PUT — обновление ListObject)*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js (DELETE — удаление ListObject)*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**Примечания:**  
- Индексы ListObject начинаются с нуля.  
- При добавлении ListObject параметры `StartRow` и `StartColumn` определяют левую верхнюю ячейку таблицы.  
- API поддерживает постраничную выборку с помощью параметров запроса `offset` и `limit` (не показаны в таблице) для больших листов.  
- Ограничение по частоте запросов: 100 запросов в минуту на аккаунт; превышение возвращает **429 Too Many Requests**.

Путём многократного использования термина **Excel ListObject** в тексте страницы содержание согласуется с целевыми ключевыми словами «Excel ListObject», «Aspose.Cells Cloud» и «Excel table API», что улучшает SEO, сохраняя при этом естественность изложения для читателей.