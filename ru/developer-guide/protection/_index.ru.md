---
---
title: "Aspose.Cells Cloud Web API – Установка / изменение пароля открытия для файлов Excel"
second_title: "Всестороннее руководство разработчика"
ArticleTitle: "Защита электронных таблиц – Установка пароля открытия и пароля на редактирование"
linktitle: "Защита"
type: docs
url: /ru/protection/
keywords: "Aspose.Cells, Cloud, API, Электронная таблица, Защита, Пароль открытия, Пароль на редактирование, Excel"
description: "Узнайте, как защитить рабочую книгу Excel паролем открытия или паролем на редактирование с помощью Aspose.Cells Cloud REST API. Включает синтаксис запроса, примеры кода и обработку ошибок."
weight: 60
---

В этом руководстве вы узнаете, как устанавливать, изменять и удалять **пароль открытия** и **пароль на редактирование** для электронных таблиц с помощью Aspose.Cells Cloud Web API. Эти функции помогают защитить конфиденциальные данные в ваших рабочих книгах Excel.

**Необходимые условия**  
- Активная учетная запись Aspose.Cells Cloud с действующим API-ключом и SID.  
- Рабочая книга, которую вы хотите защитить, должна быть загружена в облачное хранилище Aspose Cloud или быть доступной по общедоступному URL-адресу.  

**Ссылка на API**  

| **HTTP-метод** | **Конечная точка** | **Параметры запроса / пути** | **Описание** |
|----------------|--------------------|------------------------------|--------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName` (путь) – имя рабочей книги<br>`openPassword` (запрос, необязательно) – пароль, необходимый для открытия файла<br>`readWritePassword` (запрос, необязательно) – пароль, необходимый для редактирования файла | Устанавливает или обновляет пароль открытия и/или пароль на редактирование для указанной рабочей книги. |
| `DELETE` | `/cells/{fileName}/protection` | `fileName` (путь) – имя рабочей книги | Удаляет все пароли, защищающие рабочую книгу. |

**Пример тела запроса (JSON)**  

```json
{
  "OpenPassword": "MyOpenPwd123",
  "ReadWritePassword": "MyEditPwd456"
}
```

**Пример ответа (JSON)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Защита рабочей книги успешно обновлена."
}
```

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK (ОК)                    | Фильтр успешно применен; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Недопустимый или отсутствующий JWT-токен. |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

**Примеры кода**

*C# (Aspose.Cells Cloud SDK)*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Sample.xlsx",
    openPassword: "MyOpenPwd123",
    readWritePassword: "MyEditPwd456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python (Aspose.Cells Cloud SDK)*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Sample.xlsx",
    open_password="MyOpenPwd123",
    read_write_password="MyEditPwd456"
)
api.set_workbook_protection(request)
```

**Обработка ошибок**  
При возникновении ошибки API возвращает JSON-payload, содержащий поля `Code`, `Message` и опционально `Description`. Проверьте код статуса и обработайте его соответствующим образом в логике вашего приложения.

**См. также**  

- **[Как защитить электронную таблицу паролем с помощью Aspose.Cells Cloud](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[Как снять защиту с электронной таблици паролем с помощью Aspose.Cells Cloud](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  
---