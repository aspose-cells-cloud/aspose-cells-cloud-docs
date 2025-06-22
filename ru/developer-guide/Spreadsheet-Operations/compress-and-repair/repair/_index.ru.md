---
title: Восстановить файл Excel
second_title: Aspose.Cells Cloud Documen
type: docs
linktitle: Восстановить файл Excel
url: /ru/repair-excel-files/
keywords: Repair Excel, ODS, WPS, and so on files
description: Восстановление файлов Excel с помощью Aspose.Cells Cloud REST API. API поддерживает несколько языков разработки, включая Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift для быстрой интеграции в ваши проекты.
weight: 39
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Восстановление
---
Этот REST API указывает на файлы `repair` Excel.

- Ремонт XLS, XLSX, XLSM, XLSB, ODS и т. д.
- Поддержка нескольких файлов.

Aspose.Cells Cloud Excel Repair восстанавливает данные из поврежденных файлов Excel онлайн без установки. Поврежденные файлы Excel могут быть проблемой, потому что вы не сможете их открыть. Вы можете попробовать приложение Aspose.Cells Cloud Excel Repair, чтобы восстановить данные из поврежденных файлов Excel.

## РЕТ API

```bash

POST https://api.aspose.cloud/v3.0/cells/repair

```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| файл| файл| formData| Файл для загрузки|
| формат| нить| запрос| Формат вывода. Значение по умолчанию — null, формат вывода соответствует формату входного файла.|

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать командную строку cURL для легкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/repair" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash

{
    "Files":
    [
        {
            "Filename":"xxxx1.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        {
            "Filename":"xxxx2.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}

```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}
