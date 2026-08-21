---
title: "Получение проверки листа по индексу из рабочей книги Excel"
second_title: "Документ"
linktitle: "Получить"
type: docs
url: /ru/validations/get/
aliases: [  /ru/get-validation-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, API проверки листов, получить проверку по индексу, Excel REST API, Aspose.Cells SDK"
description: "Получение проверки листа по её нулевому индексу из рабочей книги Excel с использованием API Aspose.Cells Cloud (v3.0). Включает пример cURL, схему ответа, коды ошибок и фрагменты кода SDK для C#, Java, Python и других языков."
weight: 10
---

Этот REST API позволяет получить проверку листа по её индексу в рабочей книге Excel.  
Перед вызовом конечной точки получите токен JWT через конечную точку `/connect/token` и включите его в заголовок `Authorization` как `Bearer <jwt token>`.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Параметры запроса**

| Имя параметра    | Тип     | Расположение | Описание                                                |
| ---------------- | ------- | ------------ | ------------------------------------------------------- |
| name             | string  | path         | Имя файла рабочей книги.                                |
| sheetName        | string  | path         | Имя рабочего листа.                                     |
| validationIndex  | integer | path         | Нулевой индекс проверки, которую необходимо получить.  |
| folder           | string  | query        | Папка, содержащая рабочую книгу.                        |
| storageName      | string  | query        | Имя службы хранения.                                    |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует вызов API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Схема ответа**

| Поле           | Тип     | Описание                                                               |
| -------------- | ------- | ---------------------------------------------------------------------- |
| AlertStyle     | string  | Стиль предупреждения, отображаемого пользователю (Stop, Warning, Information). |
| AreaList       | array   | Коллекция диапазонов ячеек, к которым применяется проверка.            |
| IgnoreBlank    | boolean | Если `true`, пустые ячейки игнорируются при проверке.                  |
| InCellDropDown | boolean | Если `true`, в ячейке отображается раскрывающийся список.              |
| Operator       | string  | Оператор сравнения, используемый для проверки (например, `None`, `Between`). |
| ShowError      | boolean | Определяет, отображается ли сообщение об ошибке при неудачной проверке. |
| ShowInput      | boolean | Определяет, отображается ли сообщение при выборе ячейки.               |
| Type           | string  | Тип проверки (например, `AnyValue`, `WholeNumber`, `Decimal` и т.д.). |
| link.Href      | string  | Самоуказывающий URL-адрес ресурса проверки.                            |
| link.Rel       | string  | Тип связи (всегда `self`).                                             |

**Возможные коды ошибок**

| HTTP-статус | Значение                                                              |
| ----------- | -------------------------------------------------------------------- |
| 200         | Проверка успешно получена.                                           |
| 400         | Неверный запрос — отсутствуют или недопустимы параметры.             |
| 401         | Неавторизовано — недопустимый или отсутствующий токен JWT.           |
| 404         | Не найдено — рабочая книга, лист или индекс проверки не существуют.  |
| 500         | Внутренняя ошибка сервера — непредвиденное состояние.                |

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки под Aspose.Cells Cloud. SDK скрывает детали низкоуровневой реализации, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}