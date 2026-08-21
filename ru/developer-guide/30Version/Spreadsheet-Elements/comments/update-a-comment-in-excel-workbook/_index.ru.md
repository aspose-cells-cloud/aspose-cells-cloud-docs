---
title: "Обновить комментарий ячейки рабочего листа"
type: docs
url: /comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: "Aspose.Cells Cloud, REST API, Excel, рабочий лист, комментарий ячейки, обновить комментарий рабочего листа, объект комментария"
description: "Используйте REST API Aspose.Cells Cloud для обновления комментария ячейки в рабочем листе книги Excel, включая сведения о запросе, коды ответов и примеры SDK."
weight: 30
ArticleTitle: "Обновить комментарий ячейки рабочего листа – Aspose.Cells Cloud API"
---

Этот REST API обновляет комментарий ячейки рабочего листа. Используйте этот конечный пункт для **обновления комментария рабочего листа** в файле Excel.

**Необходимые условия:**  
- В заголовке `Authorization` должен присутствовать действительный токен OAuth/JWT.  
- Книга должна быть сохранена в поддерживаемом облачном хранилище (укажите `folder` и, при необходимости, `storageName`).

## API PostWorksheetComment

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются защищенными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Местоположение | Описание                                                             |
| ------------- | ------ | -------------- | -------------------------------------------------------------------- |
| name          | string | path           | Имя документа Excel.                                                 |
| sheetName     | string | path           | Имя рабочего листа, содержащего ячейку.                              |
| cellName      | string | path           | Адрес ячейки (например, **A1**).                                     |
| comment       | object | body           | Объект **Comment**, определяющий комментарий для добавления или обновления. |
| folder        | string | query          | Папка, в которой хранится документ.                                  |
| storageName   | string | query          | Имя сервиса хранилища.                                               |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Возможные коды состояния ответа:

| Код  | Описание                                                     |
|------|--------------------------------------------------------------|
| 200  | Комментарий успешно обновлён.                                |
| 400  | Неверный запрос — отсутствуют или некорректны параметры.     |
| 401  | Неавторизован — аутентификация не удалась.                   |
| 404  | Не найдено — книга, рабочий лист или комментарий не существуют. |
| 500  | Внутренняя ошибка сервера.                                   |

**Примечания / советы:**  
- Максимальная длина комментария — 1024 символа.  
- Поддерживаются символы UTF‑8; избегайте управляющих символов.

## Семейство облачных SDK

Использование SDK — это самый быстрый способ разработки с Aspose.Cells Cloud. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на вашем проекте. Ознакомьтесь со <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозиторием на GitHub</a> для получения полного списка SDK Aspose.Cells Cloud.

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

См. также:  
- [Получить комментарий рабочего листа](/comments/get/)  
- [Добавить комментарий рабочего листа](/comments/add/)  
- [Удалить комментарий рабочего листа](/comments/delete/)