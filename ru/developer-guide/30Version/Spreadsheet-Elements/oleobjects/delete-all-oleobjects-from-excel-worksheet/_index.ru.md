---
title: Удалить все OLE-объекты на листе Excel
description: Узнайте, как удалить все OLE-объекты с листа Excel с помощью REST API Aspose.Cells Cloud (v3.0). Включает адрес endpoint, параметры, примеры запросов и ответов, фрагменты кода SDK, аутентификацию, обработку ошибок и ЧАВО.
keywords: Aspose.Cells Cloud, удалить OLE-объекты, Excel API, REST API, очистка OLE на листе, облачный SDK
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# Удалить все OLE-объекты на листе Excel

Операция **OleObjects – Clear** удаляет **все** OLE-объекты (объекты со связыванием и встраиванием) с указанного листа, оставляя данные ячеек нетронутыми. Эта операция полезна для очистки устаревших электронных таблиц или подготовки рабочей книги к повторному распространению.

---

## Необходимые условия

- Действующий **JWT-токен доступа Aspose Cloud** (OAuth 2.0).  
- Целевая рабочая книга должна храниться в облачном хранилище Aspose Cloud (либо необходимо указать `folder`/`storageName`, где она расположена).  
- Версия API **v3.0** или выше.  

> **Примечание:** Операция является *идемпотентной* — её повторный вызов при отсутствии OLE-объектов возвращает успешный ответ `200 OK`.

---

## HTTP-запрос

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### Параметры пути

| Имя       | Тип    | Обязательный | Описание                     |
|-----------|--------|-------------|------------------------------|
| `name`    | string | ✔️           | Имя файла рабочей книги.     |
| `sheetName`| string | ✔️           | Имя листа.                   |

### Параметры запроса

| Имя           | Тип    | Обязательный | Описание                            |
|---------------|--------|-------------|-------------------------------------|
| `folder`      | string | нет         | Папка, содержащая рабочую книгу.    |
| `storageName` | string | нет         | Имя хранилища, где расположена рабочая книга. |

**Заголовки**

| Заголовок            | Значение                      |
|----------------------|-------------------------------|
| `Authorization`      | `Bearer <jwt token>`          |
| `Accept`             | `application/json`            |
| `Content-Type`       | `application/json`            |

---

## Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*Замените `<jwt token>` на действующий токен доступа и при необходимости скорректируйте значения `folder`/`storageName`.*

---

## Успешный ответ

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит подробную информацию об операции. |
| 400 | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Неверный или отсутствует JWT-токен.                                      |
| 413 | Payload Too Large           | Размер загружаемого файла превышает допустимый лимит.                   |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                                           |

---

## Примеры SDK

Следующие фрагменты кода демонстрируют вызов метода **DeleteWorksheetOleObjects** с использованием официальных SDK Aspose.Cells Cloud. Замените заглушки (`<YOUR_TOKEN>`, `<FILE_NAME>` и т.д.) на ваши реальные данные.

| Язык | Пример |
|------|--------|
| **C#** | <details><summary>Показать пример на C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = "<YOUR_TOKEN>", BasePath = "https://api.aspose.cloud" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: "Sample.xlsx", sheetName: "Sheet1", folder: "Samples", storageName: null);\n```</details> |
| **Java** | <details><summary>Показать пример на Java</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_TOKEN>");\nconfig.setBasePath("https://api.aspose.cloud");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);\n```</details> |
| **Python** | <details><summary>Показать пример на Python</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>Показать пример на Node.js</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('All OLE objects deleted'))\n  .catch(err => console.error(err));\n```</details> |
| **Go** | <details><summary>Показать пример на Go</summary>```go\npackage main\nimport (\n    "context"\n    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_TOKEN>"\n    cfg.Host = "https://api.aspose.cloud"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), "Sample.xlsx", "Sheet1", map[string]interface{}{ "folder": "Samples" })\n    if err != nil { panic(err) }\n    println("All OLE objects deleted")\n}\n```</details> |

*Полные исходные файлы для всех поддерживаемых языков доступны в [репозитории Aspose.Cells Cloud на GitHub](https://github.com/aspose-cells-cloud).*

---

## Ошибки и их обработка

- **Идемпотентность** – Удаление OLE-объектов с листа, где их уже нет, всё равно возвращает `200 OK`.  
- **Истечение срока действия токена** – При получении `401 Unauthorized` получите новый JWT-токен и повторите запрос.  
- **Некорректное имя листа** – Убедитесь, что имя листа точно совпадает с регистром, указанным в рабочей книге; иначе будет возвращён `400 Bad Request`.  

Для временных ошибок `500` реализуйте логику повторов с экспоненциальной задержкой.

---

## ЧАВО

**В1: Обязательно ли указывать параметры `folder` и `storageName`?**  
**О:** Нет. Если они не указаны, Aspose Cloud использует хранилище и корневую папку по умолчанию.

**В2: Можно ли удалить OLE-объекты только из определённой ячейки?**  
**О:** Данный endpoint удаляет **все** OLE-объекты на листе. Для удаления отдельного объекта используйте операцию *Удалить конкретный OLE-объект*.

**В3: Что произойдёт, если рабочая книга заблокирована для редактирования?**  
**О:** API вернёт `400 Bad Request` с сообщением о блокировке файла. Перед вызовом endpoint убедитесь, что файл не открыт в других приложениях.

**В4: Существует ли ограничение на размер рабочей книги?**  
**О:** Сервис следует общим ограничениям Aspose Cloud на размер файла (до 2 ГБ на файл). Более крупные файлы может потребоваться разбить или обрабатывать частями.

---

## Лучшие практики

- **Производительность** – Используйте атрибуты `async` или `defer` при подключении сторонних скриптов на вашем сайте документации для уменьшения начального времени загрузки страницы.  
- **Безопасность** – Добавляйте `rel="noopener noreferrer"` ко всем внешним ссылкам, открывающимся в новой вкладке.  
- **Доступность** – Декоративные иконки (например, стрелки «вниз» в боковых панелях) должны иметь `alt=""` и `role="presentation"` для соответствия стандартам WCAG AA.  
- **Единообразие** – Используйте формат даты ISO‑8601 (`ГГГГ‑ММ‑ДД`), чтобы избежать артефактов кодировки.  

---

## См. также

- **Добавить OLE-объект** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **Удалить конкретный OLE-объект** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

Используйте навигационные ссылки внизу страницы для перехода между связанными операциями API.

---
---