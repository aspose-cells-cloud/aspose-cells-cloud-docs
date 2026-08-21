---
title: "Получить все проверки рабочего листа из Excel-файла"
second_title: "Документ"
linktitle: "Получить все"
type: docs
url: /validations/get-all/
keywords: "Aspose.Cells Cloud, Excel, проверки рабочего листа, REST API, получить все проверки, SDK"
description: "Получить все проверки рабочего листа из Excel-файла с использованием REST API Aspose.Cells Cloud. Поддерживает множество SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) для быстрой интеграции."
weight: 10
---

Проверки рабочего листа позволяют задавать правила, ограничивающие тип или диапазон данных, которые могут быть введены в ячейки. Они обычно используются для обеспечения целостности данных, например, ограничения ввода списком допустимых значений, датами в определённом диапазоне или числовыми ограничениями.

Данный REST API возвращает все проверки рабочего листа в Excel-файле.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Параметры запроса**

| Имя параметра | Тип   | Местоположение | Описание                                 |
| ------------- | ----- | -------------- | ---------------------------------------- |
| name          | string | path          | Имя Excel-файла.                         |
| sheetName     | string | path          | Имя рабочего листа.                      |
| folder        | string | query         | Путь к папке, в которой хранится файл.   |
| storageName   | string | query         | Имя сервиса хранения данных.             |

**Коды статуса ответа**

| Код | Описание                                      |
|-----|-----------------------------------------------|
| 200 | Успешный запрос — список проверок             |
| 401 | Неавторизован — неверный или отсутствующий токен |
| 404 | Не найдено — файл или рабочий лист отсутствуют |
| 500 | Внутренняя ошибка сервера                     |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells Cloud. **Требуется:** в заголовке `Authorization` должен быть передан действительный JWT-токен.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "Значение должно быть между 1 и 100."
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Option1,Option2,Option3\"",
      "showErrorMessage": true,
      "errorMessage": "Выберите значение из списка."
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}