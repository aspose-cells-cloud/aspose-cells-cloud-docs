---
title: "Группировка строк в рабочей тетради Excel"
second_title: "Документ"
linktype: "Группировка"
type: docs
url: /ru/rows/group/
aliases: [  /ru/group-rows-in-excel-worksheet/ ]
keywords: "группировка строк, Excel, Aspose.Cells Cloud, REST API, SDK, рабочий лист, Excel API"
description: "Группировка строк в рабочем листе Excel с использованием REST API Aspose.Cells Cloud. Поддерживает множество SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) для простой интеграции."
weight: 60
ArticleTitle: "Группировка строк в рабочем листе Excel с помощью API Aspose.Cells Cloud"
---

Этот REST API позволяет выполнить группировку строк в рабочем листе Excel.

**Необходимые условия:**  
- В заголовке `Authorization` должен быть предоставлен действительный токен доступа OAuth 2.0 (Bearer JWT).  
- Рабочая книга должна уже существовать в указанной `папке` выбранного `storageName` (или в хранилище по умолчанию) до отправки запроса.

## API PostGroupWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию по токену JWT</a>.

### **Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                                                     |
|---------------|--------|-------------|------------------------------------------------------------------------------|
| name          | string | path        | Имя файла рабочей книги.                                                     |
| sheetName     | string | path        | Имя рабочего листа.                                                          |
| firstIndex    | integer| query       | Нулевой индекс первой строки, включаемой в группу.                           |
| lastIndex     | integer| query       | Нулевой индекс последней строки, включаемой в группу.                        |
| hide          | boolean| query       | Указывает, должны ли быть скрыты сгруппированные строки (`true` или `false`).|
| folder        | string | query       | Путь к папке, содержащей рабочую книгу.                                     |
| storageName   | string | query       | Имя хранилища, в котором находится рабочая книга.                           |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
-X POST \
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

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | OK (ОК)                     | Фильтр успешно применён; в ответе содержатся подробности операции.      |
| 400  | Bad Request (Неверный запрос)| Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован)| Недействительный или отсутствующий JWT-токен.                           |
| 413  | Payload Too Large (Слишком большой payload)| Загружаемый файл превышает лимит размера.                          |
| 500  | Internal Server Error (Внутренняя ошибка сервера)| Непредвиденная ошибка сервера.                                    |

Типичные сообщения об ошибках:

- **400 Bad Request** – убедитесь, что `firstIndex` и `lastIndex` являются допустимыми целыми числами и что `firstIndex` ≤ `lastIndex`.  
- **401 Unauthorized** – проверьте, содержит ли заголовок `Authorization` актуальный JWT-токен.  
- **404 Not Found** – убедитесь, что рабочая книга (`name`) и рабочий лист (`sheetName`) существуют в указанной `папке`/`storageName`.

{{< /tab >}}

{{< /tabs >}}

**Смотрите также:** [Разгруппировка строк в рабочем листе Excel](../rows/ungroup/ "Разгруппировка строк в рабочем листе Excel"), [Скрытие строк в рабочем листе Excel](../rows/hide/ "Скрытие строк в рабочем листе Excel"), [Показ строк в рабочем листе Excel](../rows/unhide/ "Показ строк в рабочем листе Excel").

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}