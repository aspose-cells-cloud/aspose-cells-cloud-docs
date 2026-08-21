---
title: "ワークシートをCSVに変換 – Aspose.Cells Cloud API ドキュメント"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud API を使用してスプレッドシートのワークシートをCSVに変換する方法"
linktitle: "ワークシートをCSVに変換"
type: docs
url: /convert-worksheet-to-csv/
keywords: "Aspose.Cells, CSV変換, ワークシートをCSVへ, REST API, クラウドスプレッドシート, ExcelをCSVへ"
description: "Aspose.Cells Cloud API (v4.0) を使用してExcelファイルから特定のワークシートをCSVに変換する方法を学びます。エンドポイント、パラメータ、サンプルcURL、SDKコード、エラーハンドリングを含みます。"
weight: 100
---

**ConvertWorksheetToCsv** エンドポイントは、ローカルのスプレッドシートファイルから単一のワークシートを取得し、Aspose.Cells Cloud サーバー上で完全にCSVドキュメントに変換します。ソースファイルをアップロードし、対象ワークシートを指定するだけで、開発者はクラウドストレージにファイルを保存することなく、バイナリ形式のCSVストリームを受け取ることができます。このAPIは、データ抽出の自動化、スプレッドシートデータを後続システムへ統合する、ストレージオーバーヘッドの削減などに最適です。

## ワークシートをCSVに変換する API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/csv
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベース認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### リクエストパラメータ

| パラメータ名     | 型     | 位置       | 必須/任意   | 説明                                                                                                                               |
| :--------------- | :----- | :--------- | :---------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | ファイル | FormData   | **必須**    | ソーススプレッドシートのバイナリファイル（例: `.xlsx`、`.xls`）。例: `myWorkbook.xlsx`。                                           |
| worksheet        | 文字列  | クエリ     | **必須**    | 変換対象のワークシート名（大文字・小文字を区別）。指定しない場合、最初のワークシートが使用されます。例: `Sheet1`。                 |
| outPath          | 文字列  | クエリ     | 任意        | 変換されたCSVを保存するクラウドストレージ内の宛先フォルダーパス。指定しない場合、CSVはレスポンスストリームとして直接返されます。 |
| outStorageName   | 文字列  | クエリ     | 任意        | 出力ファイルを配置するストレージサービス（例: Azure、AWS S3）の名前。`outPath` を使用する場合にのみ必要です。                     |
| fontsLocation    | 文字列  | クエリ     | 任意        | サーバー上のカスタムフォントフォルダーのパス。変換エンジンが非標準フォントを使用できるようにします。                             |
| region           | 文字列  | クエリ     | 任意        | CSV内の数値・日付の書式に影響を与えるロケール識別子（例: `en-US`、`fr-FR`）。                                                     |
| password         | 文字列  | クエリ     | 任意        | 保護されたスプレッドシートを開くためのパスワード。ソースファイルの暗号化パスワードと一致している必要があります。                   |

### レスポンス

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP ステータスコード**

| コード | 意味               | 説明                                                   |
| :----- | :----------------- | :----------------------------------------------------- |
| 200    | OK                 | フィルターが正常に適用された；レスポンスに操作詳細が含まれる。 |
| 400    | Bad Request        | パラメータが不足または無効（例: 未対応のファイル形式）。     |
| 401    | Unauthorized       | 無効または不足しているJWTトークン。                      |
| 413    | Payload Too Large  | アップロードされたファイルがサイズ制限を超えた。         |
| 500    | Internal Server Error | 予期しないサーバーエラー。                             |

## ワークシートをCSVに変換する API を使用するタイミング

- **BI パイプライン用データ抽出** – Excelレポートから特定のワークシートを取得し、中間ファイル処理なしに、結果のCSVを Power BI または Tableau に直接取り込みます。
- **請求書処理の自動化** – 請求書行を含むワークシートをCSVに変換し、会計システムへ高速にインポートします。
- **レガシーシステムとの統合** – ワークシートデータをCSV形式でエクスポートし、区切りテキストファイルのみを受け入れる古いアプリケーションで利用します。
- **オンデマンドレポート生成** – ウェブサービス内でライブスプレッドシートデータのCSVスナップショットを生成し、クライアントブラウザへ即座にファイルを返します。

## ワークシートをCSVに変換する API の利点

- **永続的なクラウドストレージが不要** – ファイルは直接変換エンジンにストリームされ、変換後に破棄されるため、帯域幅とストレージコストを削減します。
- **高性能クラウド実行** – Aspose の最適化されたサーバー上で変換が実行され、通常100MB以下のファイルは2秒以内に完了します。
- **細かな制御が可能** – 単一ワークシートの選択、カスタムフォント、地域フォーマット、パスワード保護を1回のリクエストで適用できます。
- **クロスプラットフォームでの一貫性のある出力** – 同じRESTエンドポイントを使用する.NET、Java、PythonなどすべてのSDKで、同一のCSV出力を保証します。

## SDK を使用してワークシートをCSVに変換する API の使用方法

### ワークシートをCSVに変換する API の仕様

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToCsv" target="_blank" rel="noopener noreferrer">ワークシートをCSVに変換する API の仕様</a> は、ウェブブラウザから直接RESTインタラクションを実行するための公開可能なプログラミングインターフェースを提供します。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスへ簡単にアクセスできます。以下の例は、cURL を使用してクラウド API へリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化し、スプレッドシートを別のスプレッドシートにマージするなどの処理を簡潔なコードで実現できます。Aspose.Cells Cloud SDK の完全な一覧は <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスと連携する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToCsv.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToCsv.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToCsv.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToCsv.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToCsv.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToCsv.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToCsv.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToCsv.go" >}}  
{{</tab>}}  
{{< /tabs >}}