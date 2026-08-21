---
title: "Сопоставление всех пустых ячеек в рабочем листе Excel"
ArticleTitle: "Сопоставление всех пустых ячеек в рабочем листе Excel – Руководство по API Aspose.Cells Cloud"
second_title: "Документ"
linktype: docs
url: /autofilter/match-all-blank/
aliases: [/match-all-blank-cells-in-the-list/]
keywords: "Aspose.Cells, пустые ячейки, автофильтр, REST API, Excel"
description: "Узнайте, как с помощью Aspose.Cells Cloud REST API фильтровать и сопоставлять все пустые ячейки в рабочем листе Excel. Включает endpoint, параметры, шаги аутентификации, пример cURL и фрагменты кода SDK для C#, Java, Python и других языков."
weight: 100
---

Этот REST API выполняет сопоставление всех **пустых ячеек** в списке фильтра на рабочем листе Excel.

**Необходимые условия:** Перед вызовом этого endpoint убедитесь, что у вас есть действующий JWT-токен доступа, рабочая книга загружена в облачное хранилище Aspose и вы знаете путь к папке хранилища (если применимо). Укажите параметры `folder` и `storageName`, если файл находится не в корневой папке по умолчанию.

## API PostWorksheetMatchBlanks

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.


### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                     |
|---------------|--------|-------------|--------------------------------------------------------------|
| name          | string | path        | Имя файла рабочей книги.                                     |
| sheetName     | string | path        | Имя рабочего листа, содержащего фильтр.                     |
| fieldIndex    | integer| query       | Индекс столбца (отсчитываемый от нуля), к которому применяется фильтр. |
| folder        | string | query       | Путь к папке в хранилище, где расположена рабочая книга.    |
| storageName   | string | query       | Имя облачного хранилища Aspose.                             |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                     |
|-----|-----------------------------|--------------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит сведения о выполнении операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недопустимый или отсутствующий JWT-токен.                   |
| 413 | Payload Too Large           | Загруженный файл превышает ограничение по размеру.          |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                               |

## Как использовать API PostWorksheetMatchBlanks с SDK

### Спецификация API PostWorksheetMatchBlanks

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks) определяет общедоступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
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

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK абстрагирует низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), где представлен полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}
{{< /tab >}}

{{< /tabs >}}
---