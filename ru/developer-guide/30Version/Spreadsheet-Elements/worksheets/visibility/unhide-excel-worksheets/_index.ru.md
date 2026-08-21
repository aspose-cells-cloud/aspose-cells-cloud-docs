---
title: "Показать лист Excel"
second_title: "Документ"
linktitle: "Показать"
type: docs
url: /ru/worksheets/unhide/
aliases: [  /ru/unhide-excel-worksheets/ ]
keywords: "Aspose.Cells, показать лист, Excel API, облачная электронная таблица, REST, видимость листа, рабочая книга Excel"
description: "Узнайте, как с помощью Aspose.Cells Cloud REST API показать скрытый лист в рабочей книге Excel. Включает детали запроса, примеры cURL и фрагменты кода SDK для множества языков программирования."
weight: 60
---

Этот REST API предоставляет endpoint для **показа скрытого листа** в рабочей книге Excel.

**Необходимые условия**  
Перед вызовом этой операции необходимо:

* Действительный токен доступа Aspose Cloud (JWT), включённый в заголовок `Authorization`.  
* Рабочая книга, сохранённая в поддерживаемом хранилище, путь к которому указывается с помощью параметров запроса `folder` и `storageName`.  
* Рабочая книга должна быть в формате, поддерживаемом Aspose.Cells (например, `.xls`, `.xlsx`, `.xlsm`).  

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **Параметры запроса**

| Имя параметра  | Тип     | Расположение | Описание                                 |
| -------------- | ------- | ------------ | ---------------------------------------- |
| name           | string  | путь         | Имя документа.                           |
| sheetName      | string  | путь         | Имя листа.                               |
| isVisible      | boolean | запрос       | Новое значение видимости листа (`true`).|
| folder         | string  | запрос       | Папка документа.                         |
| storageName    | string  | запрос       | Имя хранилища.                           |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) определяет общедоступное программное интерфейсное описание, позволяющее выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого вызова веб-сервисов Aspose.Cells. В приведённом ниже примере показано, как выполнить запрос с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"   # замените <jwt token> на ваш токен доступа
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Возможные коды ответа**

| HTTP-код | Значение                                      | Пример тела ответа (при наличии)                             |
|----------|-----------------------------------------------|--------------------------------------------------------------|
| 200      | Видимость листа успешно обновлена             | `{ "Code": 200, "Status": "OK" }`                           |
| 400      | Неверный запрос – отсутствуют или некорректны параметры | `{ "Code": 400, "Message": "Invalid request parameters." }` |
| 401      | Ошибка аутентификации – отсутствует или некорректен JWT-токен | `{ "Code": 401, "Message": "Authentication failed." }`      |
| 404      | Не найдено – рабочая книга или лист не существуют | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| 500      | Внутренняя ошибка сервера                     | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK берёт на себя работу со всеми низкоуровневыми деталями, позволяя вам сосредоточиться на вашем проекте. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}