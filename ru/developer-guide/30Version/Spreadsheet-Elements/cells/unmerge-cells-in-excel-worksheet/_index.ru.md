---
title: "Разъединение ячеек в рабочем листе Excel"
type: docs
url: /ru/unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, разъединение ячеек, REST API, облачный SDK"
description: "Узнайте, как использовать Aspose.Cells Cloud REST API для разъединения ячеек в рабочем листе Excel, включая примеры запросов, формат ответа и примеры кода SDK для различных языков программирования."
ArticleTitle: "Разъединение ячеек в рабочем листе Excel"
---

Этот REST API разъединяет ячейки в файле Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## Безопасность и аутентификация

Облачные API Aspose.Cells защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                             |
|----------------|---------|----------|---------------------------------------------------------|
| name           | string  | path     | Имя файла рабочей книги.                              |
| sheetName      | string  | path     | Имя рабочего листа.                                  |
| startRow       | integer | query    | Нулевой индекс первой строки, подлежащей разъединению.           |
| startColumn    | integer | query    | Нулевой индекс первого столбца, подлежащего разъединению.        |
| totalRows      | integer | query    | Количество строк, включаемых в операцию разъединения.    |
| totalColumns   | integer | query    | Количество столбцов, включаемых в операцию разъединения. |
| folder         | string  | query    | Путь к папке, где хранится рабочая книга.               |
| storageName    | string  | query    | Имя сервиса хранилища.                            |

## **Ответ**

Возвращает объект `CellCloudResponse`.

- **Обзор полей ответа**

| Поле           | Тип    | Описание                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  | Статус выполнения операции.          |
| `Code`           | integer | 200, 400, 401, 500 и т.д.                                 |


```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статусов**

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Фильтр успешно применён; ответ содержит данные об операции. |
| 400  | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Недействительный или отсутствующий JWT-токен. |
| 413  | Payload Too Large           | Загруженный файл превышает допустимый размер. |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера. |
## Как использовать API PostWorksheetUnmerge с SDK

### Спецификация API PostWorksheetUnmerge

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge) определяет публично доступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для удобного доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки cURL. Ниже приведён пример вызова облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

### Использование облачных SDK Aspose.Cells

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
---