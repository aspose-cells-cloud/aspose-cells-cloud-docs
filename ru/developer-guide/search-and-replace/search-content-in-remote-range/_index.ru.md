---
title: Aspose.Cells Cloud Web API — Поиск содержимого диапазона в удаленной электронной таблице
second_title: Documen
ArticleTitle: Search Range Content in Remote Spreadshee
linktitle: Поиск содержимого в удаленном диапазоне
type: docs
url: /ru/search-content-in-remote-range/
keywords: Excel API, Remote Spreadsheet Search, Cloud Storage, Data Retrieval, Spreadsheet Search, Text Search AP
description: Эффективный поиск текста в указанном диапазоне удаленной электронной таблицы, хранящейся в облачном хранилище, с помощью Excel API
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, Текстовый поиск, JSON, CSV, PDF, Markdown, Сопоставление пустых значений Cells в Exce
---
Поиск указанного текста в диапазоне удаленной электронной таблицы.

## **Поиск контента в удаленном диапазоне API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|имя|Нить|Путь|Имя файла электронной таблицы.|
|рабочий лист|Нить|Путь|Название рабочего листа.|
|cellArea|Нить|Путь|Диапазон ячеек, в котором следует выполнить поиск.|
|searchText|Нить|Запрос|Текст для поиска.|
|игнорируяРегистр|Булевое значение|Запрос|Укажите, следует ли при поиске игнорировать регистр.|
|папка|Нить|Запрос|Папка, в которой хранится файл.|
|имя_хранилища|Нить|Запрос|(Необязательно) Имя хранилища, если используется пользовательское облачное хранилище. Если не указано, используйте хранилище по умолчанию.|
|regoin|Нить|Запрос|Настройка региона электронной таблицы.|
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

## Где следует использовать содержимое поиска в диапазоне электронной таблицы API?

Если вам необходимо выполнить поиск контента в диапазоне электронных таблиц, вы можете использовать этот код API.

## Почему вам следует использовать поисковый контент в диапазоне Spreadsheet API?

- С легкостью ищите контент в удаленных электронных таблицах с помощью API.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать поиск неработающих ссылок в диапазоне электронной таблицы API с SDK

### Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteRange) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя все базовые детали, позволяя вам легко реализовать поиск по содержимому ячеек в различных электронных таблицах с минимальным количеством кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
