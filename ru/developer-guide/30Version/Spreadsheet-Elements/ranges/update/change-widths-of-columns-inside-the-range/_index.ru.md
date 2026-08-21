---
title: "Изменение ширины столбцов внутри диапазона"
ArticleTitle: "Изменение ширины столбцов внутри диапазона – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Ширина столбца"
type: docs
url: /ranges/update/column-width/
aliases: [/change-widths-of-columns-inside-the-range/]
keywords: "Aspose.Cells, ширина столбца, REST API, Excel, SDK, диапазон, облако"
description: "Узнайте, как изменить ширину столбцов внутри диапазона с помощью Aspose.Cells Cloud REST API или SDK (C#, Java, Python и др.). Включает cURL, подробную информацию о запросе и ответе, а также шаги аутентификации."
weight: 74
---

Этот REST API устанавливает ширину столбцов для заданного диапазона.

## Безопасность и аутентификация
Aspose.Cells Cloud API защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**Необходимые условия** – Перед вызовом конечной точки необходимо:

1. Создать учётную запись Aspose Cloud и получить *client ID* и *client secret*.  
2. Получить JWT-токен, вызвав конечную точку OAuth (`/connect/token`). Токен возвращается в поле `access_token`.  
3. Загрузить целевую рабочую книгу в хранилище Aspose Cloud (или убедиться, что она уже существует в указанной папке).  

Параметры запроса:

| Имя параметра | Тип    | Расположение | Описание |
|---------------|--------|--------------|----------|
| name          | string | path         | Имя файла рабочей книги |
| sheetName     | string | path         | Имя рабочего листа |
| value         | number | query        | Желаемое значение ширины столбца |
| range         | object | body         | Объект диапазона, определяющий целевые ячейки |
| folder        | string | query        | Путь к папке, где хранится рабочая книга |
| storageName   | string | query        | Имя сервиса хранилища |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth) определяет общедоступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как вызывать Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

<h3 id="request">Запрос</h3>

```bash
# Вызов конечной точки column‑width для рабочей книги *test.xlsx*,
# рабочего листа *Sheet1*, установка ширины выбранных столбцов в 20 пунктов.
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">Ответ</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Возможные сообщения об ошибках*  

| Код HTTP | Описание                                     |
|----------|----------------------------------------------|
| 400      | Bad Request – неверный JSON или параметры   |
| 401      | Unauthorized – отсутствует или недействителен токен |
| 404      | Not Found – рабочая книга или рабочий лист отсутствуют |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Ознакомьтесь с [репозиторием GitHub](https://github.com/aspose-cells-cloud), где представлен полный список SDK Aspose.Cells Cloud.

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Часто задаваемые вопросы (FAQ)

**В:** *Какую конечную точку следует вызвать, чтобы установить ширину столбцов в диапазоне в файле Excel?*  
**О:** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth`, где `{name}` — имя файла рабочей книги, а `{sheetName}` — имя целевого рабочего листа.

**В:** *Как выполнить аутентификацию запроса при использовании API установки ширины столбца?*  
**О:** Добавьте заголовок `Authorization: Bearer <jwt token>`. Получите JWT-токен через OAuth-процесс Aspose Cloud (`/connect/token`), используя ваш *client ID* и *client secret*.

**В:** *Какой JSON-текст нужно отправить, чтобы изменить ширину столбцов A–C до 25 пунктов?*  
**О:**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

Добавьте параметр запроса `value=25` к URL запроса.