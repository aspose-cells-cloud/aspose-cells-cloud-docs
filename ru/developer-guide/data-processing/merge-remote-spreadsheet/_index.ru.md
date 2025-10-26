---
title: Aspose.Cells Cloud Web API — Объединение одной электронной таблицы в другую.
second_title: Aspose.Cells Cloud"
ArticleTitle: Merge one spreadsheet into anothe
linktitle: Объединение удаленных электронных таблиц
type: docs
url: /ru/merge-remote-spreadsheet/
keywords: Merge spreadsheets, cloud storage, Aspose.Cells Cloud Web API, spreadsheet merging, XLSX, CSV, PD
description: Объедините файл электронной таблицы, хранящийся в облачном хранилище, с другой электронной таблицей, и вы сможете указать формат и место вывода данных.
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, объединение пустых ячеек, облачная обработка
---
Объедините файл электронной таблицы, хранящийся в облачном хранилище, с другой электронной таблицей, и вы сможете указать формат и место вывода данных.

## **Объединение удаленной таблицы API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|имя|Нить|Путь|Имя файла рабочей книги, подлежащего объединению.|
|объединенная электронная таблица|Нить|Запрос|Список файлов электронных таблиц для объединения.|
|папка|Нить|Запрос|Путь к папке, в которой хранится рабочая книга.|
|outFormat|Нить|Запрос|Формат выходного файла (например, XLSX, PDF).|
|mergeInOneSheet|Булевое значение|Запрос|Следует ли объединить все данные на одном листе.|
|имя_хранилища|Нить|Запрос|(Необязательно) Имя хранилища, если используется пользовательское облачное хранилище. Если не указано, по умолчанию используется хранилище по умолчанию.|
|outPath|Нить|Запрос|(Необязательно) Путь к папке для объединённой книги. Значение по умолчанию — null.|
|outStorageName|Нить|Запрос|Имя хранилища выходного файла.|
|шрифтыРасположение|Нить|Запрос|Расположение шрифта по вашему выбору.|
|область|Нить|Запрос|Настройка региона электронной таблицы.|
|пароль|Нить|Запрос|Пароль для доступа к файлу электронной таблицы.|

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

## Где следует использовать Merge Remote Spreadsheet API?

- Когда вам необходимо объединить несколько файлов данных в облачном хранилище.


## Почему вам следует использовать Merge Remote Spreadsheet API?

- Файлы облачного хранилища не нужно загружать, их можно объединить непосредственно в облаке.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать объединенную удаленную электронную таблицу API с SDK

### Спецификация удаленной таблицы объединения API

 The[Спецификация удаленной таблицы объединения API](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) предоставляет общедоступный программный интерфейс для выполнения REST-взаимодействий непосредственно из веб-браузера.

## Excel API SDK

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет объединять одну электронную таблицу с другой с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.
В следующих примерах кода показано, как взаимодействовать с веб-сервисами Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
