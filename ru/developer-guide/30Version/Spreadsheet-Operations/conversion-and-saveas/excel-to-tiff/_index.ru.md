---
title: "Excel в TIFF"
second_title: "Документ"
linketitle: "Excel в TIFF"
type: docs
url: /ru/convert-excel-file-to-tiff-file/
aliases: [  /ru/convert-excel-file-to-tiff-in-cloud/ , /ru/convert/excel-to-tiff/ ]
keywords: "Aspose.Cells Cloud, конвертация Excel в TIFF, REST API, cURL, SDK, .NET, Java, Python, экспорт изображений"
description: "Узнайте, как с помощью API Aspose.Cells Cloud конвертировать рабочие книги Excel в высококачественные изображения TIFF. Подробные команды cURL, примеры SDK (C#, Java, Python и др.), шаги аутентификации и обработка ошибок."
weight: 90
---

Конечные точки **Convert**, **SaveAs** и **Export** Aspose.Cells Cloud позволяют преобразовать рабочую книгу Excel в изображение TIFF.  
Вы можете вызывать эти конечные точки напрямую с помощью **cURL** или через один из поддерживаемых SDK.

## REST API

| **API**                | **Метод** | **Назначение**                                                                                     | **Ссылка Swagger**                                                                          |
| ---------------------- | --------- | -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `/cells/convert`       | PUT       | Преобразует рабочую книгу, переданную в теле запроса, в указанный формат (TIFF).                  | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`        | GET       | Экспортирует указанную рабочую книгу в другой формат (TIFF) и возвращает результат в ответе.      | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs` | POST      | Сохраняет рабочую книгу в выбранном формате (TIFF) и сохраняет результат в облачном хранилище.     | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

Эти конечные точки общедоступны и могут быть вызваны напрямую из веб-браузера или любого HTTP-клиента.

### Примеры cURL

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<base64‑content>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< /tabs >}}

> **Примечание:**
>
> - В теле запроса **Convert** должен содержаться файл (или ссылка на сохранённый файл) и желаемый `SaveFormat`.
> - Запрос **Export** не требует тела запроса; формат указывается в строке запроса (`format=tiff`).

## Обработка ошибок

| **Код состояния** | **Значение**          | **Типичная причина**                         |
| ------------------- | --------------------- | -------------------------------------------- |
| 200                 | Успех                 | Возвращается изображение TIFF (бинарный поток). |
| 400                 | Неверный запрос       | Отсутствуют или некорректны параметры.       |
| 401                 | Неавторизован         | Неверный или отсутствующий JWT-токен.        |
| 404                 | Не найдено            | Указанная рабочая книга не существует.       |
| 500                 | Внутренняя ошибка сервера | Непредвиденное состояние на стороне сервера. |

При возникновении ошибки API возвращает JSON-полезную нагрузку с полями `Code`, `Message` и, при необходимости, `Description`.

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK берёт на себя работу с низкоуровневыми деталями, позволяя сосредоточиться на проекте. Полный список SDK Aspose.Cells Cloud доступен на [GitHub-репозитории](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}