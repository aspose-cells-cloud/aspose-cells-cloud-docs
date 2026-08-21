---
title: "Task API でのサポート要求ファイル"
second_title: "ドキュメント"
type: docs
url: /ja/tasks/support-request-file/
aliases: [/support-request-file-in-task-api/]
keywords: "Aspose.Cells, REST API, Excel, クラウド"
description: "Aspose.Cells クラウド API は、Excel ワークブックのリクエストファイルをタスクベースで処理することを可能にします。"
weight: 10
ArticleTitle: "Aspose.Cells Task API でのサポート要求ファイル"
---

## REST API

| **API** | **タイプ** | **説明** | **リソースリンク** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | タスクの実行 | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) は公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

**リクエストパラメータ**

| パラメータ | タイプ | 必須 | 説明 |
|-----------|------|----------|-------------|
| TaskDescription | object | はい | 単一タスク定義のコンテナ。 |
| TaskType | string | はい | タスクのタイプ（例: `ImportData`、`SaveResult`）。 |
| Workbook.FileSourceType | string | はい | ワークブックファイルのソース（`CloudFileSystem`、`InMemoryFiles`）。 |
| Workbook.FilePath | string | はい | 選択されたソース内のワークブックファイルのパス。 |
| ImportBatchDataOption.DestinationWorksheet | string | はい | データをインポートする宛先ワークシート名。 |
| ImportBatchDataOption.IsInsert | boolean | はい | 行を挿入するかどうか（`true`：挿入、`false`：上書き）。 |
| ImportBatchDataOption.Source.FileSourceType | string | はい | リクエストファイルのソース（`RequestFiles`）。 |
| ImportBatchDataOption.Source.FilePath | string | はい | バッチデータを含むリクエストファイルのパス。 |
| SaveResultTaskParameter.ResultSource | string | はい | 結果ファイルのソース（`InMemoryFiles`）。 |
| SaveResultTaskParameter.ResultDestination.DestinationType | string | はい | 結果の宛先タイプ（`CloudFileSystem`）。 |
| SaveResultTaskParameter.ResultDestination.InputFile | string | はい | 入力ワークブックファイル名。 |
| SaveResultTaskParameter.ResultDestination.OutputFile | string | はい | 期望される出力ファイル名。 |

**レスポンス**

| フィールド | タイプ | 説明 |
|-------|------|-------------|
| Code | integer | HTTP ステータスコード（例: 成功時は 200）。 |
| Status | string | 操作のステータス（`OK` またはエラーメッセージ）。 |
| Result | object | タスク実行の詳細（生成されたファイルなど）。 |

**cURL** コマンドラインツールを使用すると、Aspose.Cells ウェブサービスへ簡単にアクセスできます。以下の例は、cURL を使ってクラウド API へリクエストを送る方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -H "x-aspose-client: Containerize.Swagger" \
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
  "Code": 200,
  "Status": "OK",
  "Result": {
    "GeneratedFiles": [
      {
        "FilePath": "ImpDataBook.xlsx",
        "FileUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

関連タスクの詳細については、[ImportData タスク](/cells/tasks/importdata/)および[SaveResult タスク](/cells/tasks/save-result/)のページをご参照ください。

## クラウド SDK ファミリー

SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells ウェブサービスへリクエストを送る方法を示しています。

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}