---
title: Экспорт OLE-объекта
second_title: Aspose.Cells Cloud Documen
linktitle: OLE-объект
type: docs
url: /ru/export/excel-ole-object/
keywords: Export Excel OLE object to kinds of format files
description: Aspose.Cells Cloud REST API поддерживает экспорт Excel объекта OLE в различные форматы файлов. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 20
kwords: Excel, Office Облако, REST API, электронная таблица, PDF, CSV, Json, Markdwon, экспорт OLE-объекта
---
- **ОТДЫХ API**

|**API**|**Тип**|**Описание**|**Сваггер Ссылка**|
|:- |:- |:- |:- |
|/ячейки/экспорт|ПОЧТА|Экспортировать Excel из содержимого запроса в какой-либо формат|[Постэкспорт](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)|


[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.

 Вы можете использовать**cURL**инструмент командной строки для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.



- **Запрос**

```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

- **Ответ**

```bash
{
    "Files": [{
        "Filename": "OLESlide.ppt",
        "FileSize": 390,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "OLEDoc.docx",
        "FileSize": 382,
        "FileContent": "-----Base64String--------"
    }]
}
```

- **Семейство облачных SDK**

 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:


{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export-shape-tiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Export-shape-tiff.php" >}}

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

{{< /tabs >}}
