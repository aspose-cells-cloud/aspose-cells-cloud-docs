---
title: Aspose.Cells Cloud Web API — импорт данных CSV, JSON или XML в файл электронной таблицы
second_title: Documen
ArticleTitle: Import Csv, JSON, or XML Data into a Spreadsheet file
linktitle: Импорт данных в электронную таблицу
type: docs
url: /ru/import-data-into-spreadsheet/
keywords: Import data, Aspose.Cells Cloud Web API, spreadsheet integration, CSV, JSON, XML, data handling, Aspose.Cell
description: Эффективно импортируйте данные в электронную таблицу из поддерживаемых форматов, таких как CSV, JSON и XML, с помощью Cloud Web Aspose.Cells API
weight: 100
kwords: Aspose.Cells Cloud Web API, Импорт данных, Office Cloud, REST, Электронная таблица, CSV, JSON, XM
---
 Импорт данных в электронную таблицу. Поддерживаемый формат файла импортируемых данных:[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) или[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## **Импорт данных в электронную таблицу API**

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
| файл данных| Файл| FormData| Загрузите файл данных для импорта.|
| Электронная таблица| Файл| FormData| Загрузите целевой файл электронной таблицы.|
| рабочий лист| Нить| Запрос| Укажите рабочий лист для импорта данных.|
| стартселл| Нить| Запрос|Укажите начальную позицию для импорта данных.|
| вставлять| Булевое значение| Запрос| Указывает, следует ли вставлять или перезаписывать указанные импортируемые данные.|
| convertNumericData| Булевое значение| Запрос| Укажите, следует ли преобразовывать числовые данные при импорте.|
| разветвитель| Нить| Запрос| Укажите разделитель для формата CSV.|
| outPath| Нить| Запрос| (Необязательно) Путь к папке, где хранится книга. Значение по умолчанию — null.|
|outStorageName| Нить| Запрос| Укажите имя хранилища выходного файла.|
| шрифтыРасположение| Нить| Запрос| Определите пользовательские шрифты, которые будут использоваться.|
| regoin| Нить| Запрос| Настройте конфигурацию региона электронной таблицы.|
| пароль| Нить| Запрос| Пароль для открытия файла электронной таблицы.|

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

## Где следует использовать импорт данных в электронную таблицу API?

- Импорт больших объемов данных в электронную таблицу.
-  Формат файла импортированных данных:[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) и[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## Почему вам следует использовать импорт данных в электронную таблицу API?

- Импорт больших объемов данных в электронные таблицы.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать импорт данных в электронную таблицу API с SDK

### Импорт данных в электронную таблицу API Спецификация

 The[Импорт данных в электронную таблицу API Спецификация](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) предоставляет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из вашего веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет импортировать данные в электронную таблицу с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода иллюстрируют, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ImportDataIntoSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ImportDataIntoSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ImportDataIntoSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ImportDataIntoSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ImportDataIntoSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ImportDataIntoSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ImportDataIntoSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ImportDataIntoSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
