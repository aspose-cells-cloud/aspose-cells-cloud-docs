---
title: "Добавление правила валидации листа в рабочую книгу Excel"
second_title: "Документ"
linktitle: "Добавление"
type: docs
url: /validations/add/ru/
keywords: "Добавление правила валидации листа, Excel, Aspose.Cells Cloud, REST API, Таблица, Правило валидации"
description: "Используйте REST API Aspose.Cells Cloud для добавления правила валидации листа в файл Excel. Доступны SDK для C#, Java, PHP, Ruby, Node.js, Python, Perl, Go и Swift."
weight: 10
---

Этот REST API добавляет правило валидации листа в рабочий лист Excel.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Параметры запроса**

| Имя параметра | Тип   | Расположение | Описание                                                   |
| ------------- | ----- | ------------ | ---------------------------------------------------------- |
| name          | string | path        | Имя документа Excel.                                       |
| sheetName     | string | path        | Имя рабочего листа.                                        |
| range         | string | query       | Диапазон ячеек, к которому применяется валидация (например, A1:B10). |
| validation    | object | body        | Определение правила валидации.                             |
| folder        | string | query       | Папка, содержащая документ.                                |
| storageName   | string | query       | Имя службы хранения.                                       |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/PutWorksheetValidation) определяет общедоступное программное интерфейсное решение и позволяет выполнять взаимодействие по протоколу REST непосредственно из веб-браузера.

Для доступа к веб-сервисам Aspose.Cells можно легко использовать утилиту командной строки cURL. В следующем примере показано, как делать запросы к облачному API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X PUT \
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

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}