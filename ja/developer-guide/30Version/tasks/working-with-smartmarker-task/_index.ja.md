---
title: "Aspose.Cells Cloud API での SmartMarker タスクの使用方法"
type: docs
url: /tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: "SmartMarker タスク, Aspose.Cells Cloud, REST API, Excel, スプレッドシート自動化"
description: "Aspose.Cells Cloud API の SmartMarker タスクを cURL および SDK の使用例とともに学び、リクエスト スキーマやエラー処理についても理解しましょう。"
weight: 60
ArticleTitle: "Aspose.Cells Cloud API での SmartMarker タスクの使用方法"
---

## REST API

**SmartMarker** は、Aspose.Cells Cloud API の機能の一つであり、XML または JSON 形式のデータ ソースから取得したデータを Excel テンプレート内のプレースホルダーに統合し、完全にデータが埋め込まれたワークブックを生成します。主にレポート生成、メール マージ、データ駆動型スプレッドシート作成などに使用されます。

**前提条件**

- Aspose.Cells Cloud API バージョン 3.0 以降  
- 有効な OAuth2/JWT アクセストークン（`Authorization: Bearer <token>` ヘッダーで渡す）  
- ソースファイル（テンプレートワークブックおよびデータファイル）が Aspose Cloud ストレージにアップロード済み、または対応するファイル システム タイプからアクセス可能であること  
- HTTPS エンドポイント（すべてのリクエストは TLS を使用する必要がある）  

| **API** | **Type** | **Description** | **Resource Link** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | タスクの実行 | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) はパブリックにアクセス可能なプログラミング インターフェースを定義し、ウェブ ブラウザから直接 REST アクセスを実行できるようにします。

**cURL** コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、SmartMarker タスクを実行し、その後で結果のワークブックを保存する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <your_access_token>" \
     -d '{
  "TaskData": {
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "SmartMarker",
          "SmartMarkerTaskParameter": {
            "SourceWorkbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "Designer.xlsx"
            },
            "DestinationWorkbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "Temp.xlsx"
            },
            "xmlFile": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "DataSet.xml"
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "SaveResult",
          "SaveResultTaskParameter": {
            "ResultSource": "InMemoryFiles",
            "ResultDestination": {
              "DestinationType": "OutputStream",
              "InputFile": "Temp.xlsx",
              "OutputFile": "Output.xlsx"
            }
          }
        }
      }
    ]
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "FileLink": "https://api.aspose.cloud/v3.0/storage/file/Output.xlsx",
    "FileSize": 254321,
    "FileName": "Output.xlsx"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### リクエスト スキーマ（抜粋）

| 要素 | 型 | 必須 | 説明 |
| --- | --- | --- | --- |
| `TaskData` | オブジェクト | はい | 1 つ以上の `TaskDescription` オブジェクトを含むルート要素 |
| `Tasks` | オブジェクトの配列 | はい | 順番に実行されるタスクのコレクション |
| `TaskDescription.TaskType` | 文字列 | はい | タスクの種類（`SmartMarker`、`SaveResult` など） |
| `SmartMarkerTaskParameter.SourceWorkbook` | オブジェクト | はい | テンプレートワークブックの場所を指定 |
| `SmartMarkerTaskParameter.DestinationWorkbook` | オブジェクト | はい | 中間ワークブックの保存先を指定 |
| `SmartMarkerTaskParameter.xmlFile` | オブジェクト | はい | SmartMarker で使用されるデータ ソース（XML/JSON） |
| `SaveResultTaskParameter.ResultDestination` | オブジェクト | はい | 最終ワークブックの返し方（例: `OutputStream`）を定義 |

### エラー処理

API は以下の HTTP ステータス コードを返す場合があります。

- **400 Bad Request**：リクエスト本文の形式が不正、または必須フィールドが不足している  
- **401 Unauthorized**：無効または欠落している認証トークン  
- **404 Not Found**：指定されたソースファイルのいずれかが見つからない  
- **500 Internal Server Error**：予期しないサーバー側エラーが発生した  

レスポンス本文に含まれる `Error` オブジェクトには `Code` および説明的な `Message` が含まれるため、エラー内容の確認にご活用ください。

SDK を使用することで、開発を迅速に進めることができます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells ウェブサービスへの呼び出しを行う方法を示しています。

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
using (HttpWebResponse response = helper.CallPost(
       "https://api.aspose.cloud/v3.0/cells/task/runtask",
       xml,
       "application/xml"))
{
    if (response.StatusCode == HttpStatusCode.OK)
    {
        Console.WriteLine("OK");
        using (Stream st = response.GetResponseStream())
        using (FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate))
        {
            st.CopyTo(fs);
        }
    }
}
```
{{< /tab >}}

{{< /tabs >}}
---