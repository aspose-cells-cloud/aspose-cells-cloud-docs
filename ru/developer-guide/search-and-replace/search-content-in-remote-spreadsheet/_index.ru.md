---
title: Aspose.Cells Cloud Web API — Поиск контента в удаленной электронной таблице
second_title: Documen
ArticleTitle: Search Content in a Remote Spreadshee
linktitle: Поиск содержимого удаленной электронной таблицы
type: docs
url: /ru/search-content-in-remote-spreadsheet/
keywords: remote spreadsheet search, Excel API, search text in spreadsheet, cloud storage search, Aspose.Cells AP
description: Эффективный поиск текста в удаленной электронной таблице с помощью Aspose.Cells API
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, Сопоставление всех пустых ячеек на листе Excel, удаленный поиск в электронной таблице, поиск в облачном хранилище
---
Поиск указанного текста в удаленной электронной таблице.

### **Поиск содержимого в удаленной таблице API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|имя|Нить|Путь|Имя файла рабочей книги для поиска.|
|searchText|Нить|Запрос|Текст для поиска в электронной таблице.|
|игнорируяРегистр|Булевое значение|Запрос|Указывает, следует ли игнорировать регистр при поиске.|
|папка|Нить|Запрос|Путь к папке, в которой хранится рабочая книга.|
|имя_хранилища|Нить|Запрос|(Необязательно) Имя пользовательского облачного хранилища. Если не указано, будет использоваться хранилище по умолчанию.|
|область|Нить|Запрос|Настройка региона электронной таблицы.|
|пароль|Нить|Запрос|Пароль для открытия файла электронной таблицы.|

### **Ответ**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
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

## Где следует использовать содержимое поиска в таблице API?

Если вам необходимо выполнить поиск по содержимому электронной таблицы, вы можете использовать этот код API.

## Почему вам следует использовать поиск по содержимому таблицы API?

- С легкостью ищите контент в удаленной электронной таблице с помощью API.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать поиск неработающих ссылок в диапазоне электронной таблицы API с SDK

### Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteSpreadsheet) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя всю необходимую информацию, позволяя вам легко реализовывать поиск по содержимому ячеек в электронных таблицах с минимальным объёмом кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода иллюстрируют, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
