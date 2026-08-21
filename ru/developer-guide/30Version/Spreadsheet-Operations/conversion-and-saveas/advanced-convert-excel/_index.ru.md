---
title: "Расширенное преобразование файла Excel"
second_title: "Документ"
linktype: "Расширенное преобразование"
type: docs
url: /ru/advanced-convert-excel/
keywords: "Aspose.Cells, преобразование Excel, облачный API, SDK"
description: "Облачный REST API Aspose.Cells предоставляет мощные функции для преобразования рабочих книг Excel в широкий спектр форматов, настройки параметров страницы, параметров сохранения и параметров печати. SDK доступны для Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby и Swift, обеспечивая бесшовную интеграцию на различных платформах."
weight: 50
ArticleTitle: "Расширенное преобразование файла Excel – Руководство по API Aspose.Cells Cloud"
---

## Расширенный облачный API для преобразования Excel

Операция «Расширенное преобразование» позволяет преобразовать рабочую книгу Excel в различные выходные форматы (PDF, HTML, CSV и др.), предоставляя точный контроль над настройками страницы, параметрами сохранения и параметрами печати.

**Требования / Аутентификация**  
Для использования данного endpoint необходимо получить токен доступа в Aspose.Cells Cloud и включить его в заголовок `Authorization` как токен типа Bearer.

**Ссылка на API**  
- **Метод:** `PUT`  
- **Endpoint:** `/cells/convert`  
- **Параметры:**  
  - `format` (строка, обязательный) – Желаемый выходной формат (например, `pdf`, `html`).  
  - `outPath` (строка, необязательный) – Путь в облачном хранилище, куда будет сохранён преобразованный файл.  
  - `options` (объект, необязательный) – JSON-объект, содержащий расширенные параметры преобразования, такие как `pageSetup`, `saveOptions` и `printSettings`.  
- **Пример тела запроса:**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **Ответ:**  
  - `200 OK` – Преобразование успешно завершено; ответ содержит поток преобразованного файла или ссылку на сохранённый файл.  
  - `400 Bad Request` – Неверные параметры или некорректное тело запроса.  
  - `401 Unauthorized` – Ошибка аутентификации или отсутствие токена.  
  - `500 Internal Server Error` – Ошибка сервера во время преобразования.  

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK (OK)                     | Фильтр применён успешно; ответ содержит подробную информацию об операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен. |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

**Примечания**  
* Некоторые выходные форматы имеют специфические ограничения (например, преобразование в HTML не сохраняет макросы). Подробную информацию см. в документации по конкретным форматам.

### Возможность загрузки файлов электронных таблиц из нескольких источников данных

### Настройка параметров страницы и параметров сохранения

## Семейство облачных SDK

Использование SDK ускоряет разработку, скрывая низкоуровневые детали, что позволяет сосредоточиться на задачах проекта. Ознакомьтесь с полным списком SDK Aspose.Cells Cloud в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории на GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud — Расширенное преобразование",
  "description":"Преобразование рабочей книги Excel в PDF/HTML/CSV с расширенными настройками.",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"Желаемый выходной формат (pdf, html, csv, …)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>
---