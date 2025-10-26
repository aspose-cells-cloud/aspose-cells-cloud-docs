---
title: Aspose.Cells Cloud Web API — сложение, вычитание, умножение, деление и процент в диапазоне электронных таблиц/Exce
second_title: Documen
ArticleTitle: Add, Minus, Multiply, Divide and Percentage in Spreadsheet/Exce
linktitle: Математический расчет
type: docs
url: /ru/math-calculate/
keywords: Math calculation,Cloud REST API, Add, Minus, Multiply, Divide, Percentage, Office Cloud, Aspose.Cell
description: Полное руководство по использованию Math Calculate API для выполнения вычислений в электронных таблицах Excel
weight: 100
kwords: Математические вычисления, Cloud REST API, Сложение, Вычитание, Умножение, Деление, Процент, Office Cloud, Aspose.Cells
---
Разработчики могут использовать API для выполнения сложения, вычитания, умножения, деления и процентных вычислений в указанных диапазонах электронных таблиц/Excel.

|**Операция расчета** | Описание|
|:- |:- |
|**Добавлять** |+ |
|**Минус** |-  |
|**Умножить** |*  |
|**Разделять** |/ |
|**Процент** |% |

## **Математический расчет API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|:- |:- |:- |:- |
| Электронная таблица| Файл| FormData| Загрузите файл электронной таблицы для обработки.|
| операция| Нить| Запрос| Математическая операция, которую необходимо выполнить (сложение, вычитание, умножение, деление и процент).|
| ценить| Нить| Запрос| Значение, которое следует использовать в расчетах, если применимо.|
| рабочий лист| Нить| Запрос| Имя рабочего листа, над которым будет выполняться операция.|
| диапазон| Нить| Запрос| Диапазон ячеек, включаемых в расчет.|
| область| Нить| Запрос|Определяет конкретную область электронной таблицы.|
| пароль| Нить| Запрос| Пароль для открытия файла электронной таблицы, если он защищен.|

### **Ответ**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Коды ошибок

- **400 Неверный запрос**: Неверный URI Apose.Cells Cloud API.
- **401 Неавторизованный**: Недействительный токен доступа. Или недействительный идентификатор клиента и секретный ключ.
- **404 Не найдено**: Файл электронной таблицы недоступен.
- **500 Ошибка сервера**: В электронной таблице обнаружена аномалия при получении расчетных данных.

## Где следует использовать Math Calculate API?

Математическое вычисление API подходит для пакетных вычислений в электронных таблицах.

## Почему вам следует использовать Math Calculate API?

- Выполнение пакетных математических расчетов.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать математический калькулятор API с SDK

### Математический расчет API Спецификация

 The[Математические вычисления Спецификация](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) определяет общедоступный программный интерфейс, позволяющий разработчикам взаимодействовать с API непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет выполнять математические вычисления по ячейкам с помощью всего лишь короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{< /tab >}}
{{< /tabs >}}
