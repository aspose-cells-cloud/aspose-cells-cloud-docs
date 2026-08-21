---
title: "Aspose.Cells Cloud – Преобразование диапазона Excel в HTML"
description: "Преобразуйте определённый диапазон файла Excel (например, A1:C10) в HTML-файл с помощью REST API Aspose.Cells Cloud. Включает аутентификацию, примеры запросов, обработку ответов, фрагменты кода SDK и коды ошибок."
keywords: "Aspose.Cells, Excel в HTML, преобразование диапазона, облачный API, электронная таблица"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

Преобразуйте выбранный диапазон локальной рабочей книги Excel в HTML-файл непосредственно через Aspose.Cells Cloud. Преобразование происходит полностью на облачном сервере, поэтому вам никогда не нужно загружать всю рабочую книгу или иметь установленный Excel локально.

## API преобразования диапазона в HTML

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

Тело запроса представляет собой `multipart/form-data`, содержащее файл электронной таблицы. Все остальные параметры передаются как параметры запроса.

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя                | Тип     | Местоположение | Обязательный | Описание                                                                 |
| ------------------ | ------- | -------------- | ------------ | ------------------------------------------------------------------------ |
| **Spreadsheet**    | Файл    | FormData       | Да           | Рабочая книга Excel для преобразования.                                 |
| **worksheet**      | Строка  | Query          | Да           | Имя листа, содержащего диапазон.                                        |
| **range**          | Строка  | Query          | Да           | Диапазон ячеек для преобразования, например `A1:C10`.                  |
| **outPath**        | Строка  | Query          | Нет          | Путь к папке, где должен быть сохранён результирующий HTML-файл (по умолчанию `null`). |
| **outStorageName** | Строка  | Query          | Нет          | Имя облачного хранилища для выходного файла.                            |
| **fontsLocation**  | Строка  | Query          | Нет          | Путь к пользовательской папке со шрифтами.                              |
| **AutoRowsFit**    | Булево  | Query          | Нет          | Автоматически подогнать все строки на листе.                            |
| **AutoColumnsFit** | Булево  | Query          | Нет          | Автоматически подогнать все столбцы на листе.                           |
| **region**         | Строка  | Query          | Нет          | Идентификатор языка и региона (например, `ru-RU`, `en-US`). Влияет на форматирование чисел и дат. |
| **password**       | Строка  | Query          | Нет          | Пароль для открытия защищённой рабочей книги.                           |
| **fontsLocation**  | Строка  | Query          | Нет          | Пользовательское расположение шрифтов.                                  |
| **region**         | Строка  | Query          | Нет          | Настройка региона/языка электронной таблицы.                            |
| **password**       | Строка  | Query          | Нет          | Пароль для открытия файла электронной таблицы.                          |

## Ответ

API возвращает преобразованный HTML-файл в виде **двоичного потока** (`application/octet-stream`).

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

### Пример успешного ответа (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Продукт</th><th>Цена</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

Сохраните тело ответа в файл (например, `report.html`), чтобы просмотреть отображаемую таблицу в браузере.

---

**Коды HTTP-статусов**

| Код  | Значение              | Описание                                                           |
| ---- | --------------------- | ------------------------------------------------------------------ |
| 200  | OK (ОК)               | Фильтр применён успешно; ответ содержит детали операции.          |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован) | Неверный или отсутствующий токен JWT.                              |
| 413  | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает ограничение по размеру. |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Как использовать API преобразования диапазона в HTML с помощью SDK?

### Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) описывает публично доступный API, позволяющий выполнять взаимодействие REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells Cloud. В следующем примере показано, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Продукт</th><th>Цена</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки, так как он абстрагирует низкоуровневые детали и позволяет преобразовать диапазон данных в HTML-файл с минимальным количеством кода.  
Полный список SDK Aspose.Cells Cloud вы найдёте в нашем [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода иллюстрируют вызов веб-сервисов Aspose.Cells Cloud с использованием различных SDK. Если загрузка из Gist заблокирована, вы можете загрузить примеры напрямую из репозитория.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}