---
title: "Удаление изображения из рабочего листа Excel – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Удаление"
type: docs
url: /ru/pictures/delete/
aliases: [  /ru/delete-a-specific-picture-from-excel-worksheet/ ]
keywords: "Aspose.Cells, облачный API, удаление изображения, рабочий лист Excel, REST"
description: "Удаление изображения из рабочего листа Excel с помощью облачного REST API Aspose.Cells. Изучите DELETE-эндпоинт, необходимые параметры, аутентификацию, коды ошибок и примеры кода."
weight: 50
ArticleTitle: "Удаление изображения из рабочего листа Excel – Aspose.Cells Cloud API"
---

Этот REST API удаляет изображение из рабочего листа Excel.

### **Безопасность и аутентификация**

Облачные API Aspose.Cells защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Параметры запроса

| Имя параметра | Тип    | Расположение | Обязательный | Описание                                                |
| ------------- | ------ | ------------ | ------------ | ------------------------------------------------------- |
| name          | string | path         | Да           | Имя файла книги.                                        |
| sheetName     | string | path         | Да           | Имя рабочего листа, содержащего изображение.           |
| pictureIndex  | integer| path         | Да           | Индекс удаляемого изображения (начинается с 0).         |
| folder        | string | query        | Нет          | Папка, в которой хранится книга.                       |
| storageName   | string | query        | Нет          | Имя службы хранилища (необязательно).                  |

Для простого доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки cURL. Ниже приведён пример вызова с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
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

**Пример заголовков ответа**

| Заголовок      | Значение                     |
|----------------|-----------------------------|
| Content-Type   | application/json            |
| Content-Length | (зависит от сервера)        |
| Date           | (дата сервера)              |

{{< /tab >}}

{{< /tabs >}}

### Обработка ошибок

| HTTP-код | Значение                                                   | Пример полезной нагрузки ошибки                                     |
| -------- | ---------------------------------------------------------- | ------------------------------------------------------------------- |
| 200      | Изображение успешно удалено.                               | `{ "Code": 200, "Status": "OK" }`                                   |
| 400      | Неверный запрос — некорректные параметры.                  | `{ "Code": 400, "Message": "Неверное значение pictureIndex." }`     |
| 401      | Неавторизованный доступ — отсутствует/некорректный токен. | `{ "Code": 401, "Message": "Токен доступа отсутствует или недействителен." }` |
| 404      | Не найдено — книга, рабочий лист или изображение не существует. | `{ "Code": 404, "Message": "Ресурс не найден." }`                 |
| 500      | Внутренняя ошибка сервера.                                 | `{ "Code": 500, "Message": "Непредвиденная ошибка сервера." }`      |

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на вашем проекте. Полный список облачных SDK Aspose.Cells доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}
---