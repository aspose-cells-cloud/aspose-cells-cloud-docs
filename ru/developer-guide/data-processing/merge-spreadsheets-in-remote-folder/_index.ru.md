---
title: Aspose.Cells Cloud Web API — объединение соответствующих файлов электронных таблиц в файл в удаленной папке
second_title: Documen
ArticleTitle: Merge matching spreadsheet files into a file in a remote Folder
linktitle: Объединение таблиц в удаленной папке
type: docs
url: /ru/merge-spreadsheets-in-remote-folder/
keywords: Merge spreadsheets, cloud storage, Excel API, remote processing, spreadsheet formats, REST AP
description: Объедините файлы электронных таблиц, хранящиеся в облачном хранилище, в один файл, который поддерживает 30 форматов вывода, таких как PDF, CSV, Json и другие распространенные форматы.
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, Объединение электронных таблиц, Облачная обработка, Удалённая обработка файлов
---
Объединяет соответствующие файлы электронных таблиц в файлы в удаленной папке, выходной формат файла поддерживает более 30 форматов, таких как PDF, CSV, Json и другие распространенные форматы.


## **Объединение таблиц в удаленной папке API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
| папка| Нить| Запрос|Папка, в которой будут храниться объединенные файлы.|
| fileMatchExpression| Нить| Запрос| Выражение для сопоставления файлов для слияния.|
| outFormat| Нить| Запрос| Желаемый формат выходного файла.|
| mergeInOneSheet| Булевое значение| Запрос| Указывает, следует ли объединить все данные на одном листе.|
| имя_хранилища| Нить| Запрос| (Необязательно) Имя пользовательского облачного хранилища; если не указано иное, по умолчанию используется хранилище по умолчанию.|
| outPath| Нить| Запрос| (Необязательно) Путь к папке для сохранения рабочей книги; по умолчанию — null.|
|outStorageName| Нить| Запрос| Имя хранилища выходного файла.|
| шрифтыРасположение| Нить| Запрос| Задает пользовательские шрифты.|
| область| Нить| Запрос| Задает область электронной таблицы.|
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

## Где следует использовать функцию объединения таблиц в удаленной папке API?

Если вам необходимо объединить несколько файлов данных, вы можете использовать этот код API.

## Почему следует использовать функцию объединения таблиц в удаленной папке API?

- Файлы облачного хранилища не нужно загружать, их можно объединить непосредственно в облаке.
- Пакетное объединение нескольких файлов электронных таблиц, поддержка сопоставления выражений.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать объединенную электронную таблицу в удаленной папке API с SDK

### Объединение таблиц в удаленной папке API Спецификация

 The[Объединение таблиц в удаленной папке API Спецификация](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) предоставляет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет объединять соответствующие файлы электронных таблиц в файлы в удаленной папке с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода иллюстрируют, как взаимодействовать с веб-сервисами Aspose.Cells с использованием различных SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheetsInRemoteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheetsInRemoteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheetsInRemoteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheetsInRemoteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheetsInRemoteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheetsInRemoteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheetsInRemoteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheetsInRemoteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
