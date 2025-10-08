---
title: Aspose.Cells Cloud Web API — Сохранение электронной таблицы как файла формата
second_title: Documen
ArticleTitle: Save Spreadsheet as a Format fil
linktitle: Сохранить электронную таблицу
type: docs
url: /ru/save-spreadsheet-as/
keywords: spreadsheet conversion, Save as, Excel to PDF, Excel to CSV, RES
description: Легко конвертируйте электронные таблицы, хранящиеся в облаке, в различные форматы, включая XLSX, PDF и CSV, используя наш надежный инструмент API.
weight: 100
kwords: Excel API, Office Облако, REST, Электронная таблица, PDF, CSV, JSON, Markdown, преобразование файлов Excel, сохранение электронной таблицы как, Aspose.Cells Cloud Web AP
---
Сохраните файл облачной таблицы/Excel как файл формата в облачном хранилище.

## **Сохранить таблицу как API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|:- |:- |:- |:- |
| имя| Нить| Путь| (Обязательно) Имя файла рабочей книги, который необходимо преобразовать.|
| формат| Нить| Запрос| (Обязательно) Желаемый формат вывода (например, «Xlsx», «Pdf», «Csv»).|
| сохранитьПараметрыДанные| Сорт| Тело| (Необязательно) Сохраните данные параметров. Значение по умолчанию — null.|
| папка| Нить| Запрос| (Необязательно) Путь к папке, где хранится книга. Значение по умолчанию — null.|
| имя_хранилища| Нить| Запрос|(Необязательно) Укажите имя хранилища, если используется пользовательское облачное хранилище. Если не указано, используйте хранилище по умолчанию.|
| outPath| Нить| Запрос| (Необязательно) Путь к папке, где хранится книга. Значение по умолчанию — null.|
|outStorageName| Нить| Запрос| Имя хранилища выходного файла.|
| шрифтыРасположение| Нить| Запрос| Используйте пользовательские шрифты.|
| область| Нить| Запрос| Настройка региона электронной таблицы.|
| пароль| Нить| Запрос| Пароль для открытия файла электронной таблицы.|

### **Ответ**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
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

## Почему вам следует использовать расклад «Экономия» API?

- Вы можете конвертировать облачные файлы в различные форматы в любое время и в любом месте.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать таблицу преобразования в Json API с SDK?

### Сохранить таблицу как API Спецификация

 The[Сохранить таблицу как API Спецификация](https://reference.aspose.cloud/cells/#/ConversionController/SaveSpreadsheetAs) определяет общедоступный программный интерфейс, позволяющий осуществлять REST-взаимодействие непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет сохранять электронную таблицу как файл формата с коротким кодом.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{< /tab >}}
{{< /tabs >}}
