---
title: "Удаление диаграммы из рабочего листа"
type: docs
url: /charts/delete/
aliases: [/delete-a-chart-from-a-worksheet/]
weight: 40
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "Удаление диаграммы"
  - "Рабочий лист"
  - "Excel"
  - "Облачный SDK"
  - "Удаление диаграммы"
  - "Справка по API"
description: "Удаляет диаграмму из рабочего листа по её индексу (начиная с нуля), используя Aspose.Cells Cloud REST API."
ArticleTitle: "Удаление диаграммы из рабочего листа с помощью Aspose.Cells Cloud REST API"
---

Этот REST API удаляет диаграмму с рабочего листа по её индексу.

Для связанных операций см. страницы **[Добавление диаграммы](#)** и **[Получение диаграммы](#)**.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Безопасность и аутентификация

Aspose.Cells Cloud API защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                             |
|---------------|--------|-------------|------------------------------------------------------|
| name          | string | path        | Имя рабочей книги.                                   |
| sheetName     | string | path        | Имя рабочего листа.                                  |
| chartIndex    | integer | path       | Индекс удаляемой диаграммы (начиная с нуля).         |
| folder        | string | query       | Папка, содержащая рабочую книгу.                     |
| storageName   | string | query       | Имя используемого хранилища.                         |


### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр успешно применён; ответ содержит подробности операции.           |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.                                   |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает допустимый размер.                   |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                      |

## Как использовать API PutWorksheetAddChart с SDK

### Спецификация API PutWorksheetAddChart

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart) определяет общедоступное программное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для удобного доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
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

API возвращает следующие коды состояния:

| Код | Описание                                              |
|-----|-------------------------------------------------------|
| 200 | Диаграмма успешно удалена                             |
| 400 | Неверный запрос (например, некорректный индекс)       |
| 401 | Неавторизован (отсутствует или недействителен JWT)   |
| 404 | Рабочая книга, рабочий лист или диаграмма не найдены  |
| 500 | Ошибка сервера                                        |

**Обработка ошибок:** Подробную информацию об ошибках см. в общем описании модели ошибок в спецификации OpenAPI.

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}