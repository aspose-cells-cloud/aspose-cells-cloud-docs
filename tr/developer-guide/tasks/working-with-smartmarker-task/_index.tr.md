﻿---
title: SmartMarker Tas ile Çalışma
type: docs
url: /tr/tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: REST API, task, save result, spreadsheets, exce
description: "Cells.Cloud API, Excel'i çalıştırmak için: akıllı işaretleyiciye görevler desteği"
weight: 60
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, SmartMarker Göreviyle Çalışma
---
## DİNLENME API

|**API**|**Tip**|**Tanım**|**Kaynak Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/görev/çalıştırma görevi|POSTALAMAK|Görevi Çalıştır|[Çalıştırma SonrasıGörev](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

 Kullanabilirsiniz**cURL**Aspose.Cells web hizmetlerine kolayca erişmek için komut satırı aracı. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{<TaskData> <Tasks> <TaskDescription> <TaskType>SmartMarker</TaskType> <SmartMarkerTaskParameter> <SourceWorkbook> <FileSourceType>CloudFileSystem</FileSourceType> <FilePath>Designer.xlsx</FilePath> </SourceWorkbook> <DestinationWorkbook> <FileSourceType>InMemoryFiles</FileSourceType> <FilePath>Temp.xlsx</FilePath> </DestinationWorkbook> <xmlFile> <FileSourceType>CloudFileSystem</FileSourceType> <FilePath>DataSet.xml</FilePath> </xmlFile> </SmartMarkerTaskParameter> </TaskDescription> <TaskDescription> <TaskType>SaveResult</TaskType> <SaveResultTaskParameter> <ResultSource>InMemoryFiles</ResultSource> <ResultDestination> <DestinationType>OutputStream</DestinationType> <InputFile>Temp.xlsx</InputFile> <OutputFile>Output.xlsx</OutputFile> </ResultDestination> </SaveResultTaskParameter> </TaskDescription> </Tasks></TaskData>}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

HttpResponseMessage with the operation result.

```

{{< /tab >}}

{{< /tabs >}}

 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:

{{< tabs tabTotal="1" tabID="4" tabName1="C#" >}}

{{< tab tabNum="1" >}}
```csharp

var xml = @"<TaskData>

    <Tasks>

    <TaskDescription>

        <TaskType>SmartMarker</TaskType>

        <SmartMarkerTaskParameter>

        <SourceWorkbook>

            <FileSourceType>CloudFileSystem</FileSourceType>

            <FilePath>Designer.xlsx</FilePath>

        </SourceWorkbook>

        <DestinationWorkbook>

            <FileSourceType>InMemoryFiles</FileSourceType>

            <FilePath>Temp.xlsx</FilePath>

        </DestinationWorkbook>

        <xmlFile>

            <FileSourceType>CloudFileSystem</FileSourceType>

            <FilePath>DataSet.xml</FilePath>

        </xmlFile>

        </SmartMarkerTaskParameter>

    </TaskDescription>

    <TaskDescription>

        <TaskType>SaveResult</TaskType>

        <SaveResultTaskParameter>

        <ResultSource>InMemoryFiles</ResultSource>

        <ResultDestination>

            <DestinationType>OutputStream</DestinationType>

            <InputFile>Temp.xlsx</InputFile>

            <OutputFile>Output.xlsx</OutputFile>

        </ResultDestination>

        </SaveResultTaskParameter>

    </TaskDescription>

    </Tasks>

</TaskData>";

ServiceHelper helper = new ServiceHelper(sid, key);

using (HttpWebResponse response = helper.CallPost("http://api.aspose.com/v3.0/cells/task/runtask", xml, "application/xml"))

{

    if (response.StatusCode == HttpStatusCode.OK)

    {

        System.Console.WriteLine("OK");

        Stream st = response.GetResponseStream();

        FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate);

        st.CopyTo(fs);

    }

}

```
{{< /tab >}}

{{< /tabs >}}
