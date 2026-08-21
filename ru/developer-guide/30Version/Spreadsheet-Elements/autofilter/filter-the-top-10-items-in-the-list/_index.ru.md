---
title: "Добавление фильтра ТОП 10 в рабочий лист Excel (Aspose.Cells Cloud)"
ArticleTitle: "Добавление фильтра ТОП 10 в рабочий лист Excel – Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Добавление фильтра ТОП 10"
type: docs
url: /autofilter/add-top-10-filter/
aliases:
  [/filter-the-top-10-items-in-the-list/, /autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, AutoFilter, фильтр ТОП 10, Excel API"
description: "Узнайте, как применить фильтр AutoFilter ТОП 10 к рабочему листу Excel с помощью REST API Aspose.Cells Cloud. Включает endpoint, параметры, пример HTTPS cURL, данные о аутентификации, обработку ошибок и фрагменты кода SDK для C#, Java, Python и других языков."
weight: 65
---

Этот REST API фильтрует **ТОП 10** элементов в списке.

> **Необходимые условия**  
> • Получите действительный JWT-токен с помощью аутентификации Aspose.Cells Cloud.  
> • Загрузите рабочую книгу Excel в ваше облачное хранилище Aspose Cloud (или укажите хранилище/папку, где она расположена).  
> • Знайте имя рабочего листа и диапазон ячеек, который вы хотите отфильтровать.

## API PutWorksheetFilterTop10

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра  | Тип     | Расположение | Обязательный | Значение по умолчанию | Описание                                                                 |
| --------------- | ------- | ------------ | ----------- | --------------------- | -------------------------------------------------------------------------- |
| **name**        | string  | путь         | Да          | —                     | Имя файла Excel.                                                           |
| **sheetName**   | string  | путь         | Да          | —                     | Имя рабочего листа, содержащего данные.                                   |
| **range**       | string  | query        | Да          | —                     | Диапазон ячеек, к которому применяется фильтр (например, `A1:B10`).       |
| **fieldIndex**  | integer | query        | Да          | —                     | Индекс столбца (начиная с нуля), по которому применяется фильтр.          |
| **isTop**       | boolean | query        | Да          | `true`                | `true` — фильтровать верхние элементы; `false` — нижние элементы.         |
| **isPercent**   | boolean | query        | Нет         | `false`               | `true` — интерпретировать `itemCount` как процент; `false` — как абсолютное число. |
| **itemCount**   | integer | query        | Нет         | `10`                  | Количество элементов, включаемых в фильтр.                                 |
| **matchBlanks** | boolean | query        | Нет         | `false`               | `true` — включить пустые ячейки в результаты фильтрации.                  |
| **refresh**     | boolean | query        | Нет         | `false`               | `true` — обновить фильтр после его применения.                            |
| **folder**      | string  | query        | Нет         | —                     | Папка в хранилище, где расположен файл Excel.                             |
| **storageName** | string  | query        | Нет         | —                     | Имя облачного хранилища Aspose Cloud.                                     |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Типичные ошибочные ответы**

```json
{
    "Code":400,
    "Message":"Bad Request – отсутствуют или некорректны параметры."
}
```

```json
{
    "Code":401,
    "Message":"Unauthorized – недействительный или отсутствующий JWT-токен."
}
```

```json
{
    "Code":413,
    "Message":"Payload Too Large – загруженный файл превышает допустимый размер."
}
```

```json
{
    "Code":500,
    "Message":"Internal Server Error – непредвиденная ошибка сервера."
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                 |
|-----|-----------------------------|----------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий JWT-токен.           |
| 413 | Payload Too Large           | Загруженный файл превышает допустимый размер.            |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                           |

## Как использовать API PutWorksheetFilterTop10 с SDK

### Спецификация API PutWorksheetFilterTop10

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как вызвать API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
  -X PUT \
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

Использование SDK — самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на вашем проекте. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}