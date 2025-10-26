---
title: Aspose.Cells Cloud Web API — Снятие защиты электронной таблицы с помощью пароля
second_title: Documen
ArticleTitle: Unprotect the Spreadsheet with passwor
linktitle: Снять защиту электронной таблицы
type: docs
url: /ru/unprotect-spreadsheet/
keywords: Excel API, Unprotect Spreadsheet, Password Removal, Encryption, Office Cloud, REST API, Spreadsheet Security, Excel File Managemen
description: Эффективно удаляет двухслойную парольную защиту из электронных таблиц Excel, поддерживая как открытие, так и изменение паролей с помощью передовых методов шифрования.
weight: 100
kwords: Excel, Office Cloud, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, Сопоставление всех пустых ячеек на листе Excel
---
Применяется для снятия защиты электронных таблиц Excel с паролем, поддерживается как открытие, так и изменение паролей.

## **Снять защиту электронной таблицы API**

```http
PUT http://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|:- |:- |:- |:- |
|Электронная таблица|Файл|FormData|Загрузите файл электронной таблицы, с которого необходимо снять защиту.|
|пароль|Нить|Запрос|Пароль шифрования для файла электронной таблицы.|
|изменить пароль|Нить|Запрос|Пароль, необходимый для изменения защищенного файла.|
|outPath|Нить|Запрос|(Необязательно) Путь к папке, в которой будет сохранена незащищённая книга. Значение по умолчанию — null.|
|outStorageName|Нить|Запрос|Указывает имя хранилища выходного файла.|
|область|Нить|Запрос|Определяет настройки региона электронной таблицы.|

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

## Где следует использовать функцию «Удалить пустые столбцы электронной таблицы» API?

Если вам необходимо преобразовать данные, вы можете использовать этот код API.

## Почему следует использовать функцию удаления пустых столбцов электронной таблицы API?

- Быстро удалите все пустые столбцы, не содержащие данных или других объектов, из электронной таблицы Excel.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать функцию удаления пустых столбцов электронной таблицы API с SDK

### Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/ProtectionController/UnprotectSpreadsheet) определяет общедоступный программный интерфейс, позволяющий выполнять REST-взаимодействия непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя все базовые детали, позволяя вам легко реализовать удаление пустых столбцов в электронных таблицах с минимальным количеством кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода иллюстрируют, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
