---
title: "Установка масштаба для рабочего листа Excel – Aspose.Cells Cloud API v3.0"
second_title: "Документ"
linktitle: "Масштаб"
type: docs
url: /ru/worksheets/zoom/
aliases: [  /ru/set-zoom-in-excel-worksheet/ ]
keywords: "Aspose.Cells, масштаб Excel, масштаб рабочего листа, REST API, облачный SDK, автоматизация Excel"
description: "Узнайте, как установить масштаб рабочего листа (10–400 %) с помощью Aspose.Cells Cloud API v3.0. Примеры cURL и SDK, обработка ошибок."
weight: 20
ArticleTitle: "Установка масштаба для рабочего листа Excel – Aspose.Cells Cloud API v3.0"
---

Этот REST API устанавливает значение масштаба рабочего листа Excel. **Требуется аутентификация**; включайте действующий Bearer JWT-токен в заголовок `Authorization` каждого запроса.

## Безопасность и аутентификация
Aspose.Cells Cloud API защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
```

### **Параметры запроса**

| Параметр    | Тип    | Местоположение | Описание                                                         |
| ----------- | ------ | -------------- | ---------------------------------------------------------------- |
| name        | string | path           | Имя файла Excel (книги).                                         |
| sheetName   | string | path           | Имя рабочего листа, который нужно изменить.                     |
| value       | integer | query         | Процент масштаба (допустимый диапазон **10–400**, напр., `40` для 40 %). |
| folder      | string | query          | Путь к папке, где хранится файл.                                 |
| storageName | string | query          | Имя облачного хранилища.                                         |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для удобного доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки cURL. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
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

**Информация в ответе об ошибках**  
Возможные HTTP-коды состояния:

- `400 Bad Request` – отсутствуют или некорректны параметры запроса.
- `401 Unauthorized` – отсутствует или некорректен JWT-токен.
- `404 Not Found` – указанный файл или рабочий лист не существует.
- `500 Internal Server Error` – непредвиденная ошибка на стороне сервера.

В каждом ответе об ошибке возвращается JSON-тело, содержащее поле `Code` и описательное поле `Message`.

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}