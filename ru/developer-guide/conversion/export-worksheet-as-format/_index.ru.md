---
title: "Экспорт рабочего листа — Aspose.Cells Cloud API v4 (PDF, PNG, SVG, CSV)"
second_title: "Документ"
ArticleTitle: "Как экспортировать удалённый рабочий лист электронной таблицы в другой формат: пошаговое руководство"
linktitle: "Экспорт рабочего листа"
type: docs
url: /ru/export-worksheet-as-format/
keywords: "Aspose Cells, экспорт рабочего листа, облачный API, PDF, PNG, CSV, конвертация Excel"
description: "Преобразуйте рабочий лист, хранящийся в Aspose.Cells Cloud, в форматы PDF, PNG, SVG, CSV и другие с помощью одного GET-запроса. Включает примеры кода для C#, Java, Python и других языков."
weight: 100
---

Экспортируйте рабочий лист облачной электронной таблицы/Excel в файл другого формата с помощью веб-API Aspose.Cells Cloud.

## **API экспорта рабочего листа в другой формат**

### Веб-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Параметры запроса**

| Имя параметра      | Тип    | Путь/Строка запроса/HTTPBody | Описание                                                                                                                                           |
| :----------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Path                       | (Обязательный) Имя файла книги, который необходимо получить.                                                                                      |
| **worksheet**      | String | Path                       | (Обязательный) Имя конкретного рабочего листа, подлежащего преобразованию.                                                                        |
| **format**         | String | Query                      | (Обязательный) Желаемый выходной формат (например, `png`, `pdf`, `svg`).                                                                          |
| **folder**         | String | Query                      | (Необязательный) Путь к папке, в которой хранится книга. По умолчанию `null`.                                                                     |
| **storageName**    | String | Query                      | (Необязательный) Имя пользовательского облачного хранилища. Если не указано, используется хранилище по умолчанию.                                  |
| **outPath**        | String | Query                      | (Необязательный) Путь к папке для выходного файла. По умолчанию `null`.                                                                           |
| **outStorageName** | String | Query                      | (Необязательный) Имя хранилища для выходного файла.                                                                                               |
| **fontsLocation**  | String | Query                      | (Необязательный) Укажите пользовательские шрифты при необходимости.                                                                               |
| **region**         | String | Query                      | (Необязательный) Настройка региона/языка электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и региональное поведение. |
| **password**       | String | Query                      | (Необязательный) Пароль для доступа к файлу электронной таблицы.                                                                                  |

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

**Коды HTTP-статуса**

| Код | Значение               | Описание                                                         |
|-----|-----------------------|------------------------------------------------------------------|
| 200 | OK (ОК)               | Фильтр применён успешно; ответ содержит данные об операции.     |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Неверный или отсутствующий JWT-токен.                           |
| 413 | Payload Too Large (Слишком большой полезный нагрузка) | Размер загружаемого файла превышает допустимый предел. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                  |

## **Где следует использовать API экспорта рабочего листа в другой формат?**

- **Миграция устаревших систем** – Преобразуйте тысячи устаревших файлов XLS в формат XLSX для современных систем.
- **Стандартизация архивов** – Приведите различные форматы электронных таблиц (XLS, XLSM, ODS, CSV) к единому формату для архивирования.
- **Взаимодействие с офисными пакетами** – Преобразуйте файлы Excel в форматы, совместимые с LibreOffice, Google Таблицами или Apple Numbers.
- **Нормализация источников данных** – Преобразуйте различные форматы электронных таблиц в CSV или JSON для последующей загрузки в базу данных.
- **Публикация в вебе** – Преобразуйте финансовые модели в HTML для отображения в вебе.

## Почему использовать API экспорта рабочего листа в другой формат?

- **Поддержка SDK на нескольких языках** – Предоставляет клиентские библиотеки для различных языков программирования, позволяя разработчикам вызывать API непосредственно из предпочитаемой ими среды.
- **Прямое преобразование без промежуточной загрузки** – Позволяет преобразовать рабочий лист, хранящийся в облачном хранилище, в требуемый формат без необходимости скачивания и повторной загрузки файла.
- **Извлечение только данных** – Возвращает содержимое рабочего листа в выбранном формате без сохранения визуального оформления.

## Как использовать API экспорта рабочего листа электронной таблицы в другой формат с помощью SDK?

### Спецификация API экспорта рабочего листа в другой формат

[Спецификация API экспорта рабочего листа в другой формат](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) предоставляет общедоступный программный интерфейс для выполнения REST-взаимодействий непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки, поскольку он скрывает детали низкоуровневой реализации и позволяет экспортировать рабочий лист электронной таблицы в файл нужного формата с помощью короткого кода.  
Полный список SDK Aspose.Cells Cloud доступен на [GitHub-репозитории](https://github.com/aspose-cells-cloud).

В следующих примерах кода показано, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}