---
title: Aspose.Cells Cloud Web API — Перемещение листа на новое место в электронной таблице
second_title: Documen
ArticleTitle: Move worksheet to new position in Spreadshee
linktitle: Переместить рабочий лист в электронную таблицу
type: docs
url: /ru/move-worksheet-in-spreadsheet/
keywords: Move Worksheet, Aspose.Cells Cloud Web API, Spreadsheet Management, Worksheet Positioning, Workbook Organization, Excel AP
description: MoveWorksheet API позволяет пользователям эффективно перемещать указанный рабочий лист в рабочей книге, тем самым улучшая организацию и доступность данных электронной таблицы.
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, Перемещение листа, Организация рабочей книги, PDF, CSV, JSON, Markdown
---
Переместить рабочий лист на новое место в электронной таблице.

## **Переместить рабочий лист из таблицы API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|Электронная таблица|Файл|FormData|Загрузите файл электронной таблицы.|
|рабочий лист|Нить|Запрос|Текущее имя перемещаемого листа.|
|позиция|Целое число|Запрос|Новое положение рабочего листа.|
|outPath|Нить|Запрос|(Необязательно) Путь к папке, где хранится книга. Значение по умолчанию — null.|
|outStorageName|Нить|Запрос|Имя хранилища выходного файла.|
|область|Нить|Запрос|Настройка региона электронной таблицы.|
|пароль|Нить|Запрос|Пароль для открытия файла электронной таблицы.|

### **Ответ**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Коды ошибок

- **400 Неверный запрос**: Неверный URI Apose.Cells Cloud API.
- **401 Неавторизованный**: Недействительный токен доступа. Или недействительный идентификатор клиента и секретный ключ.
- **404 Не найдено**: Файл электронной таблицы недоступен.
- **500 Ошибка сервера**: В электронной таблице обнаружена аномалия при получении расчетных данных.

## Где следует использовать функцию перемещения рабочего листа в электронной таблице API?

Если вам необходимо переместить рабочий лист на новое место в электронных таблицах, вы можете использовать этот код API.

## Почему вам следует использовать функцию перемещения рабочего листа в электронной таблице API?

- Быстро перемещайте рабочие листы из электронных таблиц.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать функцию перемещения рабочего листа в электронной таблице API с SDK

### Переместить рабочий лист в спецификацию API

 The[Переместить рабочий лист в спецификацию API](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) предоставляет общедоступный программный интерфейс для облегчения прямого взаимодействия REST из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет перемещать рабочие листы в электронной таблице с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.
В следующих примерах кода показано, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
