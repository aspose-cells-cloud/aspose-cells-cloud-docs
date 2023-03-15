---
title: Компрессы
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/compress/
keywords: Compress excel files
description: Aspose.Cells Cloud REST API поддерживает сжатие файлов Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 39
---
Этот REST API указывает на данные `compress` в файле Excel.

- Сжатие XLS, XLSX, XLSM, XLSB, ODS
- Быстрый способ сжатия нескольких файлов электронных таблиц Excel
- Выберите уровень сжатия
- Поддержка нескольких файлов

## РСЕТ API

```bash

POST https://api.aspose.cloud/v3.0/cells/compress

```

 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| файл| файл| formData| Файл для загрузки|
| Уровень сжатия| целое число| запрос||
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LiteCells/PostCompress) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
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
            "Filename":"xxxx1",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxx2",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}

```
 
{{< /tab >}}
 
{{< /tabs >}}
 


## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "" >}}


{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "" >}}
{{< /tab >}}

{{< /tabs >}}
