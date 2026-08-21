---
title: "Как работать с удалением листов в книге Excel"
second_title: "Документ"
linktype: "Удалить"
type: docs
url: /ru/worksheets/delete/
keywords: "Aspose.Cells, Cloud, REST API, Удалить лист, Excel, C#, Java, Python"
description: "Узнайте, как удалить один или несколько листов из книги Excel с помощью Aspose.Cells Cloud REST API. Включает примеры для C#, Java и Python, требования к подготовке, советы по обработке ошибок и связанные операции."
weight: 20
ArticleTitle: "Удаление листа(ов) в книге Excel с помощью Aspose.Cells Cloud API"
---

## Работа с удалением листов в книге Excel

Когда приложение динамически генерирует или изменяет файлы Excel, может возникнуть необходимость удалить листы, которые больше не нужны — например, временные отчёты, заглушки или устаревшие данные. Aspose.Cells Cloud API упрощает удаление одного листа или нескольких листов за один запрос.

**Справочник по API**

| Элемент | Подробности |
|---------|-------------|
| **HTTP-метод** | `DELETE` |
| **Конечная точка** | `/cells/{fileName}/worksheets` |
| **Параметры пути** | `fileName` — имя файла Excel (обязательно) |
| **Параметры запроса** | `sheetName` — имя удаляемого листа (необязательно, для удаления одного листа) <br> `folder` — путь к папке в хранилище (необязательно) <br> `storage` — имя хранилища (необязательно) |
| **Тело запроса** | *Отсутствует* |
| **Успешный ответ** | `200 OK` — лист(ы) успешно удалены. Возвращает JSON-объект со статусом операции. |
| **Ответы об ошибках** | `400 Bad Request` — некорректные параметры <br> `401 Unauthorized` — сбой аутентификации <br> `404 Not Found` — файл или лист не найден <br> `500 Internal Server Error` — ошибка на стороне сервера |

**Запрос**

Для удаления одного или нескольких листов отправьте `DELETE`-запрос к указанной выше конечной точке, указав обязательный параметр `fileName`, а при необходимости — параметр запроса `sheetName` для удаления одного листа. Если параметр `sheetName` опущен, удаляются все листы в книге.

**Параметры**

- `fileName` (строка, обязательный): имя файла Excel, включая расширение.  
- `sheetName` (строка, необязательный): имя конкретного листа для удаления. Если не указан, API удаляет все листы.  
- `folder` (строка, необязательный): путь к папке, содержащей файл в хранилище.  
- `storage` (строка, необязательный): имя хранилища Aspose Cloud для использования.

**Ответы**

- **200 OK** — пример JSON:  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "Лист(ы) успешно удалены."
  }
  ```
- **400 Bad Request** — некорректные параметры запроса.  
- **401 Unauthorized** — отсутствует или недействителен токен аутентификации.  
- **404 Not Found** — указанный файл или лист не существует.  
- **500 Internal Server Error** — непредвиденная ошибка сервера.

**Примеры**

*Ниже приведены короткие фрагменты кода, демонстрирующие вызов конечной точки удаления на трёх популярных языках программирования.*

**Пример на C#**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"Статус: {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"Ошибка: {ex.Message}");
}
```

**Пример на Java**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("Статус: " + response.getStatus());
        } catch (Exception e) {
            System.err.println("Ошибка: " + e.getMessage());
        }
    }
}
```

**Пример на Python**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"Статус: {response.status}")
except ApiException as e:
    print(f"Ошибка: {e}")
```

**Обработка ошибок**

- Убедитесь, что токен аутентификации действителен, прежде чем отправлять запрос.  
- Проверьте код статуса ответа; обрабатывайте `400`, `401`, `404` и `500` соответствующим образом.  
- Используйте блоки try-catch (или аналогичные) для перехвата сетевых или SDK-исключений.

**Связанные операции**

- [Добавить лист](/ru/worksheets/add/) — создать новый лист в существующей книге.  
- [Копировать лист](/ru/worksheets/copy/) — дублировать существующий лист.  
- [Переименовать лист](/ru/worksheets/rename/) — изменить имя листа.  
- [Переместить лист](/ru/worksheets/move/) — изменить порядок листов в книге.  
---