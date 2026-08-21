---
title: "Копирование диапазона в листе с параметрами вставки"
second_title: "Документ"
linktitle: "Копировать"
type: docs
url: /ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: "Aspose.Cells Cloud, REST API, Excel, копирование диапазона, лист, параметры вставки"
description: "Используйте Aspose.Cells Cloud REST API для копирования диапазона в пределах листа Excel с полной поддержкой параметров вставки. Включает примеры SDK для нескольких языков программирования."
weight: 20
ArticleTitle: "Копирование диапазона в листе с параметрами вставки – Aspose.Cells Cloud API"
---

Этот REST API копирует диапазон в листе книги Excel. Для смежных операций см. документацию **Получить диапазон** и **Обновить диапазон**.

**Необходимые условия:** Для использования этого конечного узла необходимо иметь действительный маркер OAuth 2.0 / JWT и убедиться, что версия API соответствует URL запроса.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **Параметры запроса**

| Название параметра | Тип    | Расположение | Описание                                                                 |
| ------------------ | ------ | ------------ | ------------------------------------------------------------------------ |
| name               | string | path         | Имя книги.                                                              |
| sheetName          | string | path         | Имя листа.                                                              |
| rangeOperate       | string | body         | Выполняемая операция: `copydata`, `copystyle`, `copyto` или `copyvalue`. |
| folder             | string | query        | Папка, содержащая книгу.                                                |
| storageName        | string | query        | Имя сервиса хранения.                                                   |

**Примечания:** Поле `rangeOperate` определяет, что именно копируется. Используйте `copydata` для копирования только значений ячеек, `copystyle` — для форматирования, `copyto` — для копирования и данных, и форматирования, и `copyvalue` — для копирования значений без формул. API поддерживает диапазоны до 1 миллиона ячеек; более крупные диапазоны могут привести к тайм-ауту.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopyCopy) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

При успешном выполнении возвращается статус `200 OK`. В случае ошибки API может вернуть payloads следующего вида:

```json
{
  "Code": 400,
  "Message": "Bad Request – недопустимые параметры."
}
```

или

```json
{
  "Code": 401,
  "Message": "Unauthorized – отсутствующий или недействительный маркер аутентификации."
}
```

Объекты ошибок содержат HTTP-код статуса и описательное сообщение для диагностики проблем.

{{< /tab >}}

{{< /tabs >}}

Вы можете загрузить образец книги для тестирования операции копирования [здесь](https://example.com/sample.xlsx).

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах проекта. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы увидеть полный список облачных SDK Aspose.Cells.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}