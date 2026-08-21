---
title: "Удаление проверки листа — Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Удаление"
type: docs
url: /validations/delete/
keywords: "Удаление, проверка листа, Aspose.Cells Cloud, Excel API"
description: "Узнайте, как удалить проверку листа из файла Excel с помощью REST API Aspose.Cells Cloud. Включает endpoint, параметры, данные для аутентификации, пример cURL, обработку ошибок и фрагменты кода SDK."
weight: 10
---

Этот REST API удаляет проверку листа по её нулевому индексу в листе Excel.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Параметры запроса**

| Имя параметра   | Тип     | Расположение | Описание                                          |
| ---------------- | ------- | ------------ | ------------------------------------------------- |
| name             | string  | path         | Имя файла Excel.                                  |
| sheetName        | string  | path         | Имя листа.                                        |
| validationIndex  | integer | path         | Нулевой индекс проверки, которую нужно удалить.  |
| folder           | string  | query        | Папка, содержащая документ.                       |
| storageName      | string  | query        | Имя сервиса хранилища.                            |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для вызова веб-сервиса Aspose.Cells. Пример ниже демонстрирует, как удалить проверку с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                           |
|------|-----------------------------|----------------------------------------------------|
| 200  | OK (ОК)                     | Фильтр успешно применён; ответ содержит детали операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован) | Неверный или отсутствующий JWT-токен.             |
| 413  | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает лимит размера.         |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                    |

## Семейство облачных SDK

Использование SDK — самый быстрый способ интеграции этой операции в ваше приложение. SDK обрабатывают низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют удаление проверки листа с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}