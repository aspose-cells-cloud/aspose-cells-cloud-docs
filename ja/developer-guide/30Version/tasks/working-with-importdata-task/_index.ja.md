---
title: "ImportData タスク – Aspose.Cells Cloud API リファレンスおよび cURL の例"
second_title: "ドキュメント"
type: docs
url: /ja/tasks/importdata/
aliases: [  /ja/working-with-importdata-task/ ]
keywords: "Aspose.Cells, ImportData タスク, Excel API, REST, cURL, SDK"
description: "Aspose.Cells Cloud の ImportData タスクを使用して、Excel ブックにバッチデータをインポートする方法を学習します。cURL の構文、リクエストスキーマ、SDK サンプル（C#, PHP, Ruby, Node.js）、およびエラー処理を含みます。"
weight: 40
---  

## REST API  

| **API** | **タイプ** | **説明** | **リソースリンク** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | タスクの実行 | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)は、ウェブブラウザから直接 REST 通信を可能にする公開可能なプログラミングインターフェースを定義しています。  

**cURL** コマンドラインツールを使用して、Aspose.Cells Cloud サービスを呼び出すことができます。以下の例では、適切にフォーマットされた JSON ペイロードを使用して **ImportData** タスクを実行する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
  "Tasks": [
    {
      "TaskDescription": {
        "TaskType": "ImportData",
        "ImportDataTaskParameter": {
          "Workbook": {
            "FileSourceType": "CloudFileSystem",
            "FilePath": "TaskBook.xlsx"
          },
          "ImportBatchDataOption": {
            "DestinationWorksheet": "Sheet1",
            "IsInsert": true,
            "Source": {
              "FileSourceType": "RequestFiles",
              "FilePath": "Batch_data_xml.txt"
            }
          }
        }
      }
    },
    {
      "TaskDescription": {
        "TaskType": "ImportData",
        "ImportDataTaskParameter": {
          "Workbook": {
            "FileSourceType": "InMemoryFiles",
            "FilePath": "TaskBook.xlsx"
          },
          "ImportBatchDataOption": {
            "DestinationWorksheet": "Sheet2",
            "IsInsert": true,
            "Source": {
              "FileSourceType": "RequestFiles",
              "FilePath": "Batch_data_xml_2.txt"
            }
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
            "DestinationType": "CloudFileSystem",
            "InputFile": "TaskBook.xlsx",
            "OutputFile": "ImpDataBook.xlsx"
          }
        }
      }
    }
  ]
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "OK",
  "TaskId": "12345678",
  "Result": {
    "FilePath": "ImpDataBook.xlsx",
    "DownloadUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

SDK を使用すると、これらの操作をアプリケーションに統合する最も効率的な方法となります。SDK は認証、リクエスト構築、レスポンス解析を処理するため、ビジネスロジックの開発に集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="5" tabID="8" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Tasks-ImportTaskData-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_run_task-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Tasks-ImportTaskData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ImportData-postImportDataMultipartContent-1.pl" >}}

{{< /tab >}}

{{< /tabs >}}
---