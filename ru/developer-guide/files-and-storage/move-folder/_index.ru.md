---
title: "Aspose.Cells Cloud API перемещения папок — быстрое перемещение папок в облаке"
second_title: "Документ"
ArticleTitle: "Управление файлами Excel в облаке — быстрое перемещение папок в облаке"
linktitle: "Перемещение папки"
type: docs
url: /ru/move-folder/
keywords: "Aspose.Cells, перемещение папки, облачное хранилище, Excel API"
description: "Узнайте, как перемещать папки в облачном хранилище Aspose.Cells Cloud с помощью RESTful API перемещения папок. Включает конечную точку, параметры, пример cURL, коды ошибок и примеры SDK для C#, Java, Python и других языков."
weight: 100
---

Этот API перемещает папку из одного места в другое внутри облачного хранилища Aspose.Cells Cloud. Он помогает организовать файлы и эффективно управлять облачным хранилищем.

## **Excel API: Перемещение папки**

### Веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**Пример запроса cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса API **moveFolder**

| Имя параметра   | Тип    | Местоположение | Описание                                                           |
| ---------------- | ------ | -------------- | ------------------------------------------------------------------ |
| srcPath          | string | Path           | Полный путь к перемещаемой папке, например, `FolderA/`.           |
| destPath         | string | Query          | Целевой путь, куда будет перемещена папка, например, `FolderB/`.   |
| srcStorageName   | string | Query          | (Необязательно) Имя исходного хранилища.                           |
| destStorageName  | string | Query          | (Необязательно) Имя целевого хранилища.                            |

**Описание параметров**

- **srcPath** — обязательный. Путь к исходной папке.
- **destPath** — обязательный. Путь к целевой папке.
- **srcStorageName** — необязательный. Идентификатор исходного хранилища.
- **destStorageName** — необязательный. Идентификатор целевого хранилища.

### **Ответ**

При успешном выполнении API возвращает пустое тело ответа с HTTP-статусом **200 OK**. Ошибки возвращаются в виде JSON-объектов, содержащих поле `error`.

**Коды HTTP-статусов**

| Код HTTP | HTTP-статус           | Описание                                                           |
| -------- | --------------------- | ------------------------------------------------------------------ |
| 200      | OK                    | Веб-API вызван успешно; ответ содержит детали операции.           |
| 400      | Bad Request           | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401      | Unauthorized          | Недействительный или отсутствующий JWT-токен.                     |
| 413      | Payload Too Large     | Загружаемый файл превышает ограничение по размеру.                 |
| 500      | Internal Server Error | Непредвиденная ошибка сервера.                                     |

## Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

Использование SDK — это лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как выполнять вызовы к веб-сервисам Aspose.Cells с использованием различных SDK:

---