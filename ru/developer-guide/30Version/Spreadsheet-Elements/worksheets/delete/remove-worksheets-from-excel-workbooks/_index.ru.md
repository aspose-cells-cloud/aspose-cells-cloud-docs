---
title: "Удаление листа"
second_title: "Документ"
linktype: "Один лист"
type: docs
url: /worksheets/delete-worksheet/
aliases: [/remove-worksheets-from-excel-workbooks/]
keywords: "Aspose.Cells Cloud, удаление листа, Excel, электронная таблица, REST API"
description: "Удаление листа из рабочей книги Excel с помощью REST API Aspose.Cells Cloud. Поддерживаются SDK для C#, Java, PHP, Ruby, Node.js, Python, Perl, Go и cURL."
weight: 20
ArticleTitle: "Удаление листа – API Aspose.Cells Cloud"
---

Этот REST API удаляет лист.  
Необходимые условия: Для вызова этого API необходимо предоставить действительный токен аутентификации JWT в заголовке **Authorization**, а также иметь доступ к месту хранения, где находится рабочая книга.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*Примечание: API использует версию **v3.0**, которая является текущей стабильной версией. Все изменения версий в будущем будут объявляться в примечаниях к выпуску.*

### **Параметры запроса**

| Имя параметра | Тип   | Расположение | Описание              |
| ------------- | ----- | ------------ | --------------------- |
| name          | string | путь         | Имя документа.        |
| sheetName     | string | путь         | Имя листа.            |
| folder        | string | query        | Папка документа.      |
| storageName   | string | query        | Имя хранилища.        |

Возможные HTTP-ответы:

| Код состояния | Описание                                        |
| ------------- | ----------------------------------------------- |
| 200 OK        | Лист успешно удалён.                            |
| 400 Bad Request | Некорректные параметры запроса.               |
| 401 Unauthorized | Ошибка аутентификации или отсутствие токена.  |
| 404 Not Found   | Указанная рабочая книга или лист не существует. |
| 500 Internal Server Error | Непредвиденная ошибка сервера.            |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet) определяет публично доступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для простого доступа к веб-сервисам Aspose.Cells вы можете использовать утилиту командной строки cURL. В следующем примере показано, как выполнять вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Все запросы должны выполняться по протоколу HTTPS; API не поддерживает незащищённые TLS соединения.*

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

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на выполнении задач вашего проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

В следующих примерах кода показано, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}