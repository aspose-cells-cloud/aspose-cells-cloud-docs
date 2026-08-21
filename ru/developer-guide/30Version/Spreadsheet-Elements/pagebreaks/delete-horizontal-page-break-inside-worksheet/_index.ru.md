---
title: "Удалить горизонтальный разрыв страницы"
ArticleTitle: "Aspose.Cells Cloud – Удалить горизонтальный разрыв страницы (REST API)"
second_title: "Документ"
linktype: "Удалить горизонтальный разрыв страницы"
type: docs
url: /ru/page-breaks/delete-horizontal-page-break/
aliases: [  /ru/delete-horizontal-page-break-inside-worksheet/ ]
keywords: "Aspose.Cells Cloud, Удалить горизонтальный разрыв страницы, Электронная таблица Excel, REST API, SDK"
description: "Удалить горизонтальный разрыв страницы из электронной таблицы Excel с помощью Aspose.Cells Cloud REST API. Доступны SDK для C#, Java, PHP, Ruby, Node.js, Python, Perl, Go."
weight: 50
---

Этот REST API удаляет **горизонтальный** разрыв страницы.

**Необходимые условия**: Для вызова этого endpoints необходимо иметь действительный JWT-токен доступа Aspose Cloud. Получите его, следуя руководству по [аутентификации](https://docs.aspose.cloud/cells/authentication/).

## API DeleteHorizontalPageBreak

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*Все вызовы API должны выполняться по протоколу **HTTPS**.*

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                 |
|---------------|--------|--------------|----------------------------------------------------------|
| `name`        | string | path         | Имя файла Excel (книги).                                 |
| `sheetName`   | string | path         | Имя рабочего листа, содержащего разрыв страницы.        |
| `index`       | integer| path         | Индекс удаляемого горизонтального разрыва страницы (начиная с 0). |
| `folder`      | string | query        | Необязательный путь к папке в хранилище, где расположен файл. |
| `storageName` | string | query        | Необязательное имя службы хранилища.                     |

### Коды ошибок

| HTTP-код | Описание                                                                    |
|----------|-----------------------------------------------------------------------------|
| 401      | Unauthorized – отсутствует или недействителен токен.                       |
| 404      | Not Found – указанный файл, рабочий лист или индекс разрыва страницы не найден. |
| 400      | Bad Request – неверный синтаксис запроса или недопустимые параметры.       |
| 500      | Internal Server Error – возникло непредвиденное состояние.                 |

**См. также:**  
- [Добавить горизонтальный разрыв страницы](/page-breaks/add-horizontal-page-break/)  
- [Получить горизонтальные разрывы страницы](/page-breaks/get-horizontal-page-breaks/)  
- [Удалить вертикальный разрыв страницы](/page-breaks/delete-vertical-page-break/)

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки **cURL**. Пример ниже демонстрирует, как выполнить вызов с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
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

**Схема ответа**

| Поле    | Тип     | Описание                                     |
|---------|---------|----------------------------------------------|
| Code    | integer | HTTP-код статуса (например, 200).            |
| Status  | string  | Текстовое сообщение статуса (например, "OK").|
| Message | string  | Необязательное дополнительное сообщение в случае ошибок. |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже показывают, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*Если пример не загружается, просмотрите его на [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d).*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*Если пример не загружается, просмотрите его на [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f).*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*Если пример не загружается, просмотрите его на [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152).*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*Если пример не загружается, просмотрите его на [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca).*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*Если пример не загружается, просмотрите его на [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0).*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*Если пример не загружается, просмотрите его на [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1).*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*Если пример не загружается, просмотрите его на [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca).*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*Если пример не загружается, просмотрите его на [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185).*

{{< /tab >}}

{{< /tabs >}}