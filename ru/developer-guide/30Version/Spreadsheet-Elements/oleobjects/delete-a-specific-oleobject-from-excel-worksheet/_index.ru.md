---
title: "Удаление OLE-объекта из рабочего листа Excel"
second_title: "Документ"
linktitle: "Удаление"
type: docs
url: /ru/oleobjects/delete/
aliases: [/ru/delete-a-specific-oleobject-from-excel-worksheet/]
keywords: "Aspose.Cells, Cloud, Удаление, OLE, Объект, Excel, Рабочий лист, REST, API, SDK"
description: "Узнайте, как удалить OLE-объект из рабочего листа Excel с помощью REST API Aspose.Cells Cloud (v4.0). Включает HTTPS-Endpoint, шаги аутентификации, пример cURL, фрагменты SDK, рекомендации по обработке ошибок и ссылки на дальнейшие действия."
weight: 50
ArticleTitle: "Удаление OLE-объекта из рабочего листа Excel с помощью Aspose.Cells Cloud API"
---

На этой странице объясняется, как удалить конкретный OLE-объект из рабочего листа в файле Excel с использованием **Aspose.Cells Cloud**. OLE-объектом может быть связанное изображение, диаграмма или любой встроенный объект, который Excel хранит как отдельную сущность.

## Безопасность и аутентификация
Aspose.Cells Cloud API защищены и требуют [аутентификацию на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### Параметры запроса

| Имя параметра   | Тип    | Местоположение | Описание                                               |
|-----------------|--------|----------------|--------------------------------------------------------|
| name            | string | path           | Имя файла рабочей книги.                               |
| sheetName       | string | path           | Имя рабочего листа.                                    |
| oleObjectIndex  | integer| path           | Индекс OLE-объекта, подлежащего удалению.              |
| folder          | string | query          | Папка, содержащая рабочую книгу. (необязательно)       |
| storageName     | string | query          | Имя сервиса хранилища. (необязательно)                 |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для удобного доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует, как выполнить вызов с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Подробности ответа

| HTTP-статус          | Описание                                                                | Пример JSON                                                           |
|----------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **200 OK**           | OLE-объект успешно удалён.                                              | `{ "Code": 200, "Status": "OK" }`                                     |
| **401 Unauthorized** | Отсутствует или недействителен JWT-токен.                              | `{ "Code": 401, "Message": "Access token is missing or invalid." }`  |
| **404 Not Found**    | Указанная рабочая книга, рабочий лист или индекс OLE-объекта не существует. | `{ "Code": 404, "Message": "OLE object index out of range." }`      |
| **400 Bad Request**  | Обязательные параметры отсутствуют или имеют неверный формат.           | `{ "Code": 400, "Message": "Invalid request parameters." }`          |

Обрабатывайте эти ответы в своём приложении, проверяя код статуса и отображая сопровождающее сообщение.

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя низкоуровневые детали, позволяя вам сосредоточиться на задачах проекта. Посетите [репозиторий GitHub](https://github.com/aspose-cells-cloud), чтобы ознакомиться со полным списком SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}