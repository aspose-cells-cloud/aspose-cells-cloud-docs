---
title: "Aspose.Cells Cloud Web API — Суммирование и подсчет по цвету в Excel"
second_title: "Документ"
ArticleTitle: "Сумма, подсчет, среднее, максимум и минимум значений по цвету в электронной таблице/Excel"
LinkTitle: "Агрегирование ячеек по цвету"
type: docs
url: /ru/aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, агрегирование, цвет, сумма, подсчет, среднее, минимум, максимум"
description: "Агрегация ячеек Excel по цвету фона или шрифта (сумма, подсчет, среднее, минимум, максимум) с помощью Aspose.Cells Cloud API. Изучите конечную точку, параметры, аутентификацию и примеры SDK."
weight: 100
---

## Обзор

API может выполнять вычисления данных на основе **цвета** ячейки. Он позволяет суммировать, подсчитывать, вычислять среднее, а также находить максимальное и минимальное значения в электронной таблице Excel в соответствии с цветом заливки или шрифта ячеек.

| Операция вычисления | Описание                                                           |
| :------------------ | :----------------------------------------------------------------- |
| Подсчет             | Определение количества ячеек одинакового цвета.                    |
| Сумма               | Вычисление общей суммы значений ячеек одинакового цвета.           |
| Максимальное значение | Определение наибольшего значения среди ячеек одинакового цвета.    |
| Минимальное значение | Определение наименьшего значения среди ячеек одинакового цвета.    |
| Среднее значение    | Вычисление среднего значения ячеек одинакового цвета.              |

## Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                                 |
| :------------ | :----- | :--------- | :----------------------------------------------------------------------- |
| Spreadsheet   | File   | FormData    | Рабочая книга Excel для обработки.                                        |
| Worksheet     | String | Query       | Имя листа, содержащего диапазон.                                         |
| Range         | String | Query       | Диапазон в стиле A1 (например, `A1:B10`).                                |
| Operation     | String | Query       | Метод вычисления — `Sum`, `Count`, `Average`, `Min` или `Max`.           |
| ColorPosition | String | Query       | Определяет, какой цвет использовать — `Background` (фон) или `Font` (шрифт). |
| Region        | String | Query       | Параметр региона электронной таблицы (например, `us-east-1`).            |
| Password      | String | Query       | Пароль для открытия защищённой рабочей книги (необязательный).           |

#### Перечисления

- **ColorPosition**

  | Значение   | Смысл                              |
  | :--------- | :---------------------------------- |
  | Background | Использовать цвет заливки ячейки.   |
  | Font       | Использовать цвет шрифта ячейки.     |

**Пример запроса multipart/form‑data**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### Ответ

Схема ниже описывает объект ответа. Ниже приведён конкретный пример.

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**Пример ответа (реальные значения)**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**Коды HTTP-статуса**

| Код | Значение                | Описание                                                              |
| --- | ----------------------- | --------------------------------------------------------------------- |
| 200 | OK (ОК)                 | Фильтр успешно применён; ответ содержит подробности операции.        |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или неверны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.                                 |
| 413 | Payload Too Large (Слишком большой полезный груз) | Размер загружаемого файла превышает лимит.                             |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                        |

## Где следует использовать API агрегирования по цвету?

В электронной таблице данные из различных категорий часто кодируются цветом. Этот API позволяет суммировать, подсчитывать, вычислять среднее или находить минимальное и максимальное значения для каждой цветовой группы, упрощая анализ данных по цвету.

## Почему стоит использовать API агрегирования по цвету?

API обеспечивает быстрый и надёжный способ выполнения расчётов по цвету без необходимости писать собственную логику разбора. Он легко интегрируется с SDK Aspose.Cells Cloud, позволяя разработчикам реализовать агрегирование по цвету всего в несколько строк кода.

## Как использовать API агрегирования по цвету с SDK

### Спецификация API агрегирования по цвету

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">Спецификация API агрегирования по цвету</a> определяет публично доступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки, поскольку он скрывает низкоуровневые детали, позволяя агрегировать вычисления по цвету ячейки всего в несколько строк кода.  
Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**Примечания:**

- При работе с защищёнными рабочими книгами укажите необязательный параметр запроса `Password`; в противном случае запрос завершится с ошибкой 401.
- Максимальный размер запроса для файла `Spreadsheet` составляет 100 МБ. Если необходимо обрабатывать более крупные файлы, сначала загрузите рабочую книгу в облачное хранилище Aspose Cloud и укажите её через параметр `Path` (здесь не показано).