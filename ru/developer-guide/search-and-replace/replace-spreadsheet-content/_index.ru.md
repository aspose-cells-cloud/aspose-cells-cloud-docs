---
title: Aspose.Cells Cloud Web API — Замена содержимого электронной таблицы
second_title: Documen
ArticleTitle: Replace Spreadsheet Conten
linktitle: Заменить содержимое электронной таблицы
type: docs
url: /ru/replace-spreadsheet-content/
keywords: Excel API, Spreadsheet manipulation, Replace text, Office Cloud integration, REST AP
description: Эффективная замена текста в локальных файлах электронных таблиц с помощью Aspose.Cells API
weight: 100
kwords: Excel, Office Cloud, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, Замена текста в Excel, Сопоставление пустых ячеек в рабочей таблице Excel
---
Эффективно заменяйте указанный текст в локальных файлах электронных таблиц.

## **Заменить содержимое электронной таблицы API**

```
PUT http://api.aspose.cloud/v4.0/cells/replace/content
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
| Электронная таблица| Файл| FormData| Загрузите файл электронной таблицы.|
| searchText| Нить| Запрос|Текст для поиска.|
| replaceText| Нить| Запрос| Текст, на который следует заменить.|
| рабочий лист| Нить| Запрос| Укажите рабочий лист для замены.|
| cellArea| Нить| Запрос| Укажите площадь ячейки для замены.|
| область| Нить| Запрос| Настройка региона электронной таблицы.|
| пароль| Нить| Запрос| Пароль для открытия файла электронной таблицы.|

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

## Где следует использовать замену содержимого в таблице API?

Если вам необходимо заменить содержимое электронной таблицы паролем, вы можете использовать этот код API.

## Почему следует использовать функцию «Заменить содержимое в таблице API»?

- Быстрая замена содержимого в электронных таблицах паролем.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать замену содержимого в таблице API с помощью SDK

### Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceSpreadsheetContent) определяет общедоступный программный интерфейс, позволяющий выполнять REST-взаимодействия непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя все основные детали, позволяя вам легко реализовать замену содержимого ячеек в электронных таблицах с минимальным количеством кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как взаимодействовать с веб-сервисами Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
