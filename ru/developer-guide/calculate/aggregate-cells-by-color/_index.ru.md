---
title: Aspose.Cells Cloud Web API — Сумма, количество, среднее значение и т. д. по цвету в электронных таблицах/Exce
second_title: Documen
ArticleTitle: Sum, Count, Average Value, etc by color in Spreadsheet/Exce
LinkTitle: Aggregate Cells by Colo
type: docs
url: /ru/aggregate-cells-by-color/
keywords: Sum, Count, Average Value, Max Value, Min Value, Excel REST API, Spreadsheet Operations, Aspose.Cells, Excel Cloud AP
description: Aspose.Cells Cloud Web API (Excel Cloud API) может выполнять вычисления данных, суммирование и усреднение, а также может находить максимальные и минимальные значения в электронной таблице Excel на основе цвета заливки или шрифта ячеек.
weight: 100
kwords: Сумма, Количество, Среднее значение, Максимальное значение, Минимальное значение, Excel REST API, Операции с электронными таблицами, Aspose.Cells, Excel Cloud API
---
API может выполнять вычисления данных, суммирование и усреднение, а также может находить максимальные и минимальные значения в электронной таблице Excel на основе цвета заливки или шрифта ячеек.

| Операция расчета| Описание|
|:- |:- |
| Считать| Определите количество ячеек одного цвета.|
| Сумма| Подсчитайте общее значение ячеек одного цвета.|
| Максимальное значение| Определите наибольшее значение среди ячеек одного цвета.|
| Мин. значение| Найдите наименьшее значение среди ячеек одинакового цвета.|
|Среднее значение| Вычислите среднее значение ячеек одинакового цвета.|

## **Агрегирование Cells по цвету API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
| Электронная таблица| Файл| FormData| Загрузите файл электронной таблицы.|
| Рабочий лист| Нить| Запрос| Указывает рабочий лист.|
| Диапазон| Нить| Запрос| Указывает диапазон.|
| Операция| Нить| Запрос| Укажите методы расчетных операций, включая сумму, количество, среднее, минимум и максимум.|
| ColorPosition| Нить| Запрос| Указывает содержимое, которое необходимо суммировать и подсчитывать на основе цвета фона и/или цвета шрифта.|
| Область| Нить| Запрос| Настройка региона электронной таблицы.|
| Пароль| Нить| Запрос| Пароль для открытия файла электронной таблицы.|

### **Ответ**

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
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Коды ошибок

- **400 Неверный запрос**: Неверный URI Apose.Cells Cloud API.
- **401 Неавторизованный**: Недействительный токен доступа. Или недействительный идентификатор клиента и секретный ключ.
- **404 Не найдено**: Файл электронной таблицы недоступен.
- **500 Ошибка сервера**: В электронной таблице обнаружена аномалия при получении расчетных данных.

## Где следует использовать Агрегат по цвету API?

В электронной таблице данные из разных категорий отображаются разными цветами, что позволяет выполнять такие операции, как суммирование, подсчет, вычисление средних значений и поиск максимальных и минимальных значений на основе цвета.

## Почему вам следует использовать Агрегат по цвету API?

- Предоставить методы анализа цветовых данных.
- Классифицируйте и рассчитывайте данные на основе цвета, чтобы получить основополагающие данные для анализа данных.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать агрегат по цвету API с SDK

### Агрегат по цвету API Спецификация

 The[Агрегат по цвету API Спецификация](https://reference.aspose.cloud/cells/#/CalculateController/AggregateCellsByColor) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет объединять вычисления по цвету ячеек с помощью всего лишь короткого фрагмента кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{< /tab >}}
{{< /tabs >}}
