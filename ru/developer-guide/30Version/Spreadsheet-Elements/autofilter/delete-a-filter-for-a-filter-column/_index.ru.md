---
title: "Удаление фильтра из рабочей книги Excel — Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Удалить фильтр"
type: docs
url: /ru/delete-filter/
aliases: [/ru/delete-a-filter-for-a-filter-column/, /ru/delete-auto-filter/]
keywords: "Aspose.Cells Cloud удаление фильтра, Excel, REST API, SDK"
description: "Узнайте, как удалить Автофильтр из рабочего листа Excel с помощью Aspose.Cells Cloud REST API, cURL и SDK (C#, Java, Python и др.). Включает адрес конечной точки, параметры, аутентификацию и примеры кода."
weight: 100
---

## REST API

Этот REST API удаляет **Автофильтр** с рабочего листа Excel.

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра          | Тип    | Расположение | Обязательный? | Описание                                                                                   |
| ---------------------- | ------ | ------------ | ------------- | ------------------------------------------------------------------------------------------ |
| **name**               | string | Path         | Да            | Имя рабочей книги.                                                                         |
| **sheetName**          | string | Path         | Да            | Имя рабочего листа.                                                                        |
| **range**              | string | Query        | Нет           | Диапазон ячеек, к которому применяется фильтр (например, `A1:C10`).                       |
| **fieldIndex**         | integer| Query        | Да            | Нулевой индекс столбца, к которому применяется фильтр.                                     |
| **dateTimeGroupingType**| string| Query        | Нет           | Способ группировки значений даты и времени: `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`. |
| **year**               | integer| Query        | Нет           | Компонент года для группировки дат.                                                        |
| **month**              | integer| Query        | Нет           | Компонент месяца для группировки дат.                                                      |
| **day**                | integer| Query        | Нет           | Компонент дня для группировки дат.                                                         |
| **hour**               | integer| Query        | Нет           | Компонент часа для группировки дат.                                                        |
| **minute**             | integer| Query        | Нет           | Компонент минуты для группировки дат.                                                      |
| **second**             | integer| Query        | Нет           | Компонент секунды для группировки дат.                                                     |
| **matchBlanks**        | boolean| Query        | Нет           | `true` / `false` — включать ли пустые ячейки в фильтр.                                     |
| **refresh**            | boolean| Query        | Нет           | `true` / `false` — обновлять ли рабочий лист после удаления.                               |
| **folder**             | string | Query        | Нет           | Папка исходной рабочей книги.                                                              |
| **storageName**        | string | Query        | Нет           | Имя хранилища.                                                                             |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK (OK)                     | Фильтр успешно применён; ответ содержит подробности операции.            |
| 400 | Bad Request (Неверный запрос)| Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано)| Неверный или отсутствующий токен JWT.                                     |
| 413 | Payload Too Large (Слишком большой payload)| Загруженный файл превышает лимит размера.                     |
| 500 | Internal Server Error (Внутренняя ошибка сервера)| Непредвиденная ошибка сервера.                                  |

## Как использовать API DeleteWorksheetFilter с SDK

### Спецификация API DeleteWorksheetFilter

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) определяет общедоступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
  -X DELETE \
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

Использование SDK — наиболее эффективный способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже показывают, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}