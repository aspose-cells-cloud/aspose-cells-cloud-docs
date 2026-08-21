---
title: "Добавление рабочего листа Excel"
ArticleTitle: "Добавление рабочего листа Excel — Руководство по API Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Добавить"
type: docs
url: /worksheets/add/
aliases: [/add-a-new-excel-worksheet/]
keywords: "Добавление рабочего листа Excel, Aspose.Cells Cloud, REST API, PUT worksheet, рабочая тетрадь Excel, запрос API"
description: "Пошаговое руководство по добавлению нового рабочего листа в рабочую тетрадь Excel с помощью REST API Aspose.Cells Cloud, включая детали запроса, пример cURL и фрагменты кода SDK для нескольких языков."
weight: 20
---

Этот REST API добавляет новый рабочий лист в существующую рабочую тетрадь.

**Необходимые условия**: Для вызова этого конечного пункта необходимо иметь действительный маркер аутентификации Aspose Cloud, целевая рабочая тетрадь должна быть загружена в облачное хранилище Aspose Cloud, а также необходимо знать имя хранилища (если используется пользовательское хранилище).

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                           |
| ------------- | ------ | ------------ | -------------------------------------------------- |
| name          | string | path         | Имя файла рабочей тетради.                         |
| sheetName     | string | path         | Имя нового создаваемого рабочего листа.            |
| position      | integer | query       | Позиция вставки листа (индексация с нуля).         |
| sheettype     | string | query        | Тип нового листа (например, **Chart**, **Dialog**). |
| folder        | string | query        | Папка, содержащая рабочую тетрадь.                 |
| storageName   | string | query        | Имя облачного хранилища Aspose Cloud.              |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PutAddNewWorksheet) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks" \
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

**Возможные коды статуса ответа**

| Код статуса | Описание                                             |
|------------|------------------------------------------------------|
| 200        | Рабочий лист успешно добавлен.                       |
| 400        | Неверный запрос — недопустимые параметры.           |
| 401        | Неавторизован — отсутствует или недействителен маркер аутентификации. |
| 404        | Не найдено — рабочая тетрадь или папка не существуют. |
| 500        | Внутренняя ошибка сервера — непредвиденное состояние. |

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на вашем проекте. Ознакомьтесь со [списком репозиториев на GitHub](https://github.com/aspose-cells-cloud), где вы найдете полный список SDK для Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPutAddNewWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPutAddNewWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPutAddNewWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPutAddNewWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPutAddNewWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPutAddNewWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPutAddNewWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPutAddNewWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}