---
title: Aspose.Cells Cloud Web API — Разделение электронной таблицы на несколько файлов, по одному на каждый лист
second_title: Documen
ArticleTitle: Split a spreadsheet into multiple files, one for each worksheet
linktitle: Разделить удаленную таблицу в Clou
type: docs
url: /ru/split-remote-spreadsheet/
keywords: spreadsheet splitting, cloud spreadsheet API, split Excel file, multi-format outpu
description: Разделите электронную таблицу, хранящуюся в облачном хранилище, на несколько выходных форматов без загрузки
weight: 100
kwords: Excel, Office Облако, REST, Электронная таблица, PDF, CSV, JSON, Markdown, разделенная удаленная электронная таблица
---
Разделите электронную таблицу, хранящуюся в облаке, на отдельные файлы с 30 форматами выходных файлов.

## **Разделенная удаленная таблица API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|:- |:- |:- |:- |
| имя| Нить| Путь| Имя файла рабочей книги, который необходимо разделить.|
| папка| Нить| Запрос| Путь к папке, где хранится рабочая книга.|
| от| Целое число| Запрос| Начать оглавление рабочего листа.|
| к| Целое число| Запрос| Конец индекса рабочего листа.|
| outFormat| Нить| Запрос| Желаемый формат вывода (например, «Xlsx», «Pdf», «Csv»).|
| имя_хранилища| Нить| Запрос|(Необязательно) Укажите имя хранилища, если используется пользовательское облачное хранилище. Если не указано, используйте хранилище по умолчанию.|
| outPath| Нить| Запрос| (Необязательно) Путь к папке, где хранится книга. Значение по умолчанию — null.|
|outStorageName| Нить| Запрос| Имя хранилища выходного файла.|
| шрифтыРасположение| Нить| Запрос| Используйте пользовательские шрифты.|
| область| Нить| Запрос| Настройка региона электронной таблицы.|
| пароль| Нить| Запрос| Пароль для открытия файла электронной таблицы.|

## **Ответ**

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

## Где следует использовать таблицу Split Remote API?

Если вам необходимо объединить несколько файлов данных, вы можете использовать этот код API.

## Почему вам следует использовать Split Remote Spreadsheet API?

- Файлы облачного хранилища не нужно загружать, их можно разделить прямо в облаке.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать разделенную удаленную электронную таблицу API с SDK

### Спецификация для разделенной удаленной таблицы API

 The[Спецификация для разделенной удаленной таблицы API](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) определяет общедоступный программный интерфейс и обеспечивает взаимодействие REST непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет разделить электронную таблицу, хранящуюся в облаке, на отдельные файлы с коротким кодом.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.
В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{< /tab >}}
{{< /tabs >}}
