---
title: "Как работать с видимостью на листе Excel"
second_title: "Документ"
linktitle: "Видимость"
type: docs
url: /worksheets/panes/
keywords: "Aspose.Cells Cloud, API скрытия листа, API отображения скрытого листа, видимость листа Excel, REST API для Excel, Aspose.Cells v3.0"
description: "Узнайте, как программно скрывать или отображать листы Excel с помощью REST API Aspose.Cells Cloud. Включает URL-адреса запросов, примеры на cURL и .NET SDK, обработку ошибок и примечания, специфичные для версии."
weight: 20
---

## Работа с видимостью на листе Excel

*Видимость листа* определяет, отображается ли лист конечному пользователю. С помощью Aspose.Cells Cloud вы можете скрыть или отобразить лист с помощью простого REST-запроса. Используемые конечные точки API:

* **Скрыть лист** — `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **Отобразить лист** — `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **Поддерживаемая версия API:** **v3.0** (по состоянию на март 2026 г.)

### Предварительные требования
1. Активная учетная запись **Aspose.Cells Cloud**.  
2. Действующие **Client ID** и **Client Secret** (или токен доступа OAuth 2.0).  
3. Рабочая книга (`{fileName}`) должна уже быть загружена в облачное хранилище Aspose.  

---

## Скрытие листа

### Запрос
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### Ответ
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### Пример cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### Пример .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Лист скрыт: {response.Worksheet.Visible}");
```

### Типичные ошибки
| HTTP-код | Описание                                    | Способ устранения                                         |
|----------|---------------------------------------------|-----------------------------------------------------------|
| 400      | Неверный JSON-Body или отсутствует `Visible` | Убедитесь, что тело запроса — корректный JSON с указанным ключом. |
| 401      | Неавторизованный доступ — токен отсутствует или просрочен | Обновите токен OAuth и включите его в заголовок запроса. |
| 404      | Лист или файл не найден                     | Проверьте правильность `{fileName}` и `{sheetName}`.     |
| 409      | Лист уже скрыт                             | Проверьте текущую видимость перед отправкой запроса.     |

---

## Отображение скрытого листа

### Запрос
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### Ответ
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### Пример cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### Пример .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Лист отображается: {response.Worksheet.Visible}");
```

### Типичные ошибки
| HTTP-код | Описание                                    | Способ устранения                                         |
|----------|---------------------------------------------|-----------------------------------------------------------|
| 400      | Неверный JSON-Body или отсутствует `Visible` | Предоставьте корректный JSON с `"Visible": true`.       |
| 401      | Неавторизованный доступ — токен отсутствует или просрочен | Повторно сгенерируйте токен доступа и повторите запрос. |
| 404      | Лист или файл не найден                     | Убедитесь, что имя файла и листа существуют в хранилище. |
| 409      | Лист уже отображается                      | Действия не требуются — лист уже отображается.           |

---

## Связанные операции
> *Закрепление областей* | *Разделение областей* | *Масштаб* — см. соответствующие страницы для получения дополнительной информации о настройке макета листа.

---

## Часто задаваемые вопросы

<dl>
  <dt>Как скрыть лист с помощью API Aspose.Cells Cloud?</dt>
  <dd>Отправьте `PUT`-запрос к `/cells/{fileName}/worksheets/{sheetName}/visibility` с JSON-Body `{ "Visible": false }`. Не забудьте включить действующий токен OAuth 2.0. В ответ вы получите `200 OK` и обновлённый объект листа.</dd>

  <dt>Какой ответ возвращает API после отображения скрытого листа?</dt>
  <dd>API возвращает `200 OK` с JSON-телом, содержащим объект листа, где `"Visible": true`. Ответ включает свойства `Name`, `Index` и `Visible` листа.</dd>

  <dt>Могу ли я скрыть несколько листов за один вызов?</dt>
  <dd>Нет. Конечная точка видимости работает только с одним листом, идентифицируемым по `{sheetName}`. Чтобы скрыть несколько листов, переберите их имена в клиентском коде.</dd>
</dl>

---

*Написано командой Aspose Docs — более 15 лет опыта автоматизации рабочих процессов Excel.*