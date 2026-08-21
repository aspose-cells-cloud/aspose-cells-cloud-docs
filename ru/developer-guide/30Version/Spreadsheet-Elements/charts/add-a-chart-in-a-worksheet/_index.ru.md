---
title: "Добавление диаграммы в рабочий лист"
type: docs
url: /charts/add/
aliases: [/add-a-chart-in-a-worksheet/]
weight: 20
description: "Узнайте, как добавить диаграмму в рабочий лист Excel с использованием Aspose.Cells Cloud API v3.0. Включает endpoint, параметры, пример cURL и фрагменты кода SDK."
keywords:
  - "добавить диаграмму Aspose.Cells"
  - "Aspose.Cells add chart API"
  - "REST API диаграмм"
  - "примеры SDK Aspose.Cells"
ArticleTitle: "Добавление диаграммы в рабочий лист — руководство по Aspose.Cells Cloud API"
---

Этот REST API добавляет новую диаграмму в рабочий лист.

**Необходимые условия**  
Перед вызовом данной операции получите действительный JWT-токен доступа и убедитесь, что целевая рабочая книга хранится в указанной папке или месте хранения.

## API PutWorksheetAddChart

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра         | Тип     | Расположение | Описание                                                                                                                                                                           |
| --------------------- | ------- | ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**              | string  | path         | Имя рабочей книги.                                                                                                                                                                 |
| **sheetName**         | string  | path         | Имя рабочего листа.                                                                                                                                                                |
| **chartType**         | string  | query        | Тип диаграммы (см. свойство **Type** ресурса диаграммы). Поддерживаемые типы диаграмм включают **Bar**, **Column**, **Line**, **Pie**, **Scatter**, **Area**, **Doughnut**, **Radar** и др. |
| **upperLeftRow**      | integer | query        | Индекс верхней левой строки области диаграммы (начинается с 0).                                                                                                                   |
| **upperLeftColumn**   | integer | query        | Индекс верхнего левого столбца области диаграммы (начинается с 0).                                                                                                                |
| **lowerRightRow**     | integer | query        | Индекс нижней правой строки области диаграммы (начинается с 0).                                                                                                                   |
| **lowerRightColumn**  | integer | query        | Индекс нижнего правого столбца области диаграммы (начинается с 0).                                                                                                                |
| **area**              | string  | query        | Диапазон, содержащий значения для построения диаграммы (например, `A1:B5`).                                                                                                       |
| **isVertical**        | boolean | query        | Указывает, является ли ориентация диаграммы вертикальной.                                                                                                                         |
| **categoryData**      | string  | query        | Диапазон значений оси категорий (например, `D1:E10`).                                                                                                                             |
| **isAutoGetSerialName** | boolean | query      | Если **true**, имена серий генерируются автоматически.                                                                                                                             |
| **title**             | string  | query        | Заголовок диаграммы.                                                                                                                                                               |
| **folder**            | string  | query        | Папка, содержащая рабочую книгу.                                                                                                                                                   |
| **storageName**       | string  | query        | Имя хранилища.                                                                                                                                                                     |
| **dataLabels**        | boolean | query        | Отображать метки данных, если **true**.                                                                                                                                            |
| **dataLabelsPosition**| string  | query        | Положение меток данных (например, `Above`).                                                                                                                                        |
| **pivotTableSheet**   | string  | query        | Имя листа, содержащего сводную таблицу.                                                                                                                                            |
| **pivotTableName**    | string  | query        | Имя сводной таблицы.                                                                                                                                                               |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                      | Описание                                                                 |
|-----|-------------------------------|--------------------------------------------------------------------------|
| 200 | OK                            | Фильтр успешно применён; ответ содержит подробную информацию об операции. |
| 400 | Bad Request                   | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                  | Недействительный или отсутствующий JWT-токен.                            |
| 413 | Payload Too Large             | Загружаемый файл превышает предельный размер.                            |
| 500 | Internal Server Error         | Непредвиденная ошибка сервера.                                           |

## Как использовать API PutWorksheetAddChart с SDK

### Спецификация API PutWorksheetAddChart

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) определяет общедоступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки cURL. Пример ниже демонстрирует вызов Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# Тело запроса для этой операции не требуется
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK абстрагирует низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud приведён в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}