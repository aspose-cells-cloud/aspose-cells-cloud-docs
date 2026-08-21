---
title: "SaveResult タスクの使用方法"
second_title: "Document"
type: docs
url: /tasks/save-result/
aliases: [/working-with-saveresult-task/]
keywords: "SaveResult タスク, Aspose.Cells Cloud API, 結果のエクスポート, ワークブックのダウンロード, クラウドストレージ, REST API, スプレッドシート, Excel"
description: "Aspose.Cells Cloud API で SaveResult タスクを使用して、処理済みのワークブックデータをクラウドストレージにエクスポートする方法、または直接ダウンロードする方法を学習します。cURL、Java、.NET のコード例と、パラメータの完全なリファレンスを含みます。"
weight: 50
---

## REST API

| **API** | **Type** | **Description** | **Resource Link** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | タスクの実行 | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) は公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

**cURL** コマンドラインツールを使用することで、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使って Cloud API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/xml" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d "<?xml version=\"1.0\" encoding=\"UTF-8\"?>
<TaskData>
  <Tasks>
    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>CloudFileSystem</FileSourceType>
          <FilePath>TaskBook.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet1</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <Source>
            <FileSourceType>RequestFiles</FileSourceType>
            <FilePath>Batch_data_xml.txt</FilePath>
          </Source>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>InMemoryFiles</FileSourceType>
          <FilePath>TaskBook.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet2</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <Source>
            <FileSourceType>RequestFiles</FileSourceType>
            <FilePath>Batch_data_xml_2.txt</FilePath>
          </Source>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>SaveResult</TaskType>
      <SaveResultTaskParameter>
        <ResultSource>InMemoryFiles</ResultSource>
        <ResultDestination>
          <DestinationType>CloudFileSystem</DestinationType>
          <InputFile>TaskBook.xlsx</InputFile>
          <OutputFile>ImpDataBook.xlsx</OutputFile>
        </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
操作結果を含む HttpResponse オブジェクト。
```

{{< /tab >}}

{{< /tabs >}}

SDK を使用すると、開発速度を最大限に高めることができます。SDK は低レベルの詳細を処理してくれるため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="1" tabID="4" tabName1="Java" >}}

{{< tab tabNum="1" >}}
```java
var xml = @"
<TaskData>
  <Tasks>
    <TaskDescription>
      <TaskType>Convert</TaskType>
      <ConvertTaskParameter>
        <Workbook>
          <FileSourceType>CloudFileSystem</FileSourceType>
          <FilePath>Source.xlsx</FilePath>
        </Workbook>
        <DestinationFile>Temp.tiff</DestinationFile>
        <ImageSaveOptions>
          <HorizontalResolution>200</HorizontalResolution>
          <OnePagePerSheet>true</OnePagePerSheet>
          <VerticalResolution>100</VerticalResolution>
        </ImageSaveOptions>
      </ConvertTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>SaveResult</TaskType>
      <SaveResultTaskParameter>
        <ResultSource>InMemoryFiles</ResultSource>
        <ResultDestination>
          <DestinationType>OutputStream</DestinationType>
          <InputFile>Temp.tiff</InputFile>
          <OutputFile>Output.tiff</OutputFile>
        </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>
";

ServiceHelper helper = new ServiceHelper(sid, key);
using (HttpWebResponse response = helper.CallPost("http://api.aspose.com/v3.0/cells/task/runtask", xml, "application/xml"))
{
    if (response.StatusCode == HttpStatusCode.OK)
    {
        System.Console.WriteLine("OK");
        Stream st = response.GetResponseStream();
        FileStream fs = new FileStream("Output.tiff", FileMode.OpenOrCreate);
        st.CopyTo(fs);
    }
}
```
{{< /tab >}}

{{< /tabs >}}
---