---
title: "Удаление нескольких строк из рабочего листа Excel"
second_title: "Документ"
linktitle: "Строки"
type: docs
url: /ru/rows/delete/rows/
keywords: "Aspose.Cells Cloud, удаление строк, удаление нескольких строк, рабочий лист Excel, REST API, SDK"
description: "Узнайте, как удалить одну или несколько строк из рабочего листа Excel с помощью REST API Aspose.Cells Cloud. Включает сведения об конечной точке, параметрах, пример cURL и примеры кода SDK для различных языков."
weight: 80
ArticleTitle: "Удаление нескольких строк из рабочего листа Excel с помощью API Aspose.Cells Cloud"
---

Этот REST API удаляет несколько строк **из** рабочего листа Excel.

**Необходимые условия:** Для вызова этой конечной точки требуется действительный JWT-токен доступа, полученный из аутентификации Aspose Cloud, а также соответствующие разрешения на хранилище для данной книги.

## API DeleteWorksheetRows

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра  | Тип    | Путь / Строка запроса / HTTP-тело | Описание                                                                 |
| --------------- | ------- | --------------------------------- | ------------------------------------------------------------------------ |
| name            | string  | path                              | Имя книги.                                                               |
| sheetName       | string  | path                              | Имя рабочего листа.                                                      |
| startrow        | integer | query                             | Индекс первой удаляемой строки (начинается с нуля), например, `0` — первая строка. |
| totalRows       | integer | query                             | Количество удаляемых строк.                                              |
| updateReference | boolean | query                             | Нужно ли обновлять ссылки после удаления (`true`/`false`).              |
| folder          | string  | query                             | Папка документа.                                                         |
| storageName     | string  | query                             | Имя хранилища.                                                           |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует, как выполнять вызовы в облачный API с помощью cURL. **Все конечные точки требуют HTTPS; HTTP устарел.**

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
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

**Возможные коды ответа**

| HTTP-статус | Описание                                      |
|-------------|-----------------------------------------------|
| 200         | Строки успешно удалены.                       |
| 400         | Неверный запрос — некорректные параметры.     |
| 401         | Неавторизовано — отсутствует или недействителен JWT-токен. |
| 404         | Не найдено — книга или рабочий лист не существуют. |
| 500         | Внутренняя ошибка сервера — непредвиденное условие. |

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}