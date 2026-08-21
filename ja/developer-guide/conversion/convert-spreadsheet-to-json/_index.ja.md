---
title: "Aspose.Cells Cloud Web API – スプレッドシートを JSON に変換"
second_title: "ドキュメント"
ArticleTitle: "ローカルのスプレッドシートを Aspose.Cells Cloud API を使用して JSON に変換する方法"
linktitle: "スプレッドシートを JSON に変換"
type: docs
url: /ja/convert-spreadsheet-to-json/
keywords: "Aspose Cells Cloud, スプレッドシートを JSON に変換, Excel to JSON API, Aspose.Cells Cloud API, REST API, スプレッドシート変換"
description: "Aspose.Cells Cloud API を使用してローカルの Excel ファイルを JSON に変換する方法を学びます。エンドポイント、パラメーター、サンプルコード、エラー処理を含み、シームレスな統合を実現します。"
weight: 100
---

**ConvertSpreadsheetToJson** エンドポイントは、ローカルドライブに保存されたスプレッドシートを、Aspose.Cells Cloud サーバー上で完全に JSON ファイルに変換します。スプレッドシートを `multipart/form-data` として送信することで、サービスはダウンロードや追加処理が可能な JSON ストリームを返却します。このクラウドネイティブな変換により、事前にファイルをストレージにアップロードする必要がなくなり、ストレージコストを削減し、分析、レポート、データ交換などの目的でスプレッドシートデータを JSON 形式で必要とするアプリケーションのワークフローを簡素化します。

**前提条件**: Aspose Cloud アカウント、有効な JWT アクセストークン、および Aspose.Cells Cloud SDK または API キーが設定されている必要があります。

**背景**: スプレッドシートを JSON に変換することは、Excel データを Web サービス、NoSQL データベース、またはクライアント側 JavaScript アプリケーションと統合する際の一般的な手順です。スプレッドシートを JSON に変換する API は、元のファイルを保存する必要なく、高速なサーバーサイド変換を実現します。

## スプレッドシートを JSON に変換する API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名 | 型                         | 位置       | 必須/任意 | 説明                                                                                                                                                             |
| :------------- | :------------------------- | :--------- | :-------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | ファイル (multipart/form-data) | FormData   | 必須      | 変換元のスプレッドシートファイル（例: `.xls`、`.xlsx`、`.xlsm`）。例: `curl -F "Spreadsheet=@myfile.xlsx"`                                                          |
| outPath        | 文字列                       | クエリ     | 任意      | 変換後の JSON ファイルを保存するクラウドストレージ上のフォルダーパス。省略した場合、JSON はレスポンスストリームに直接返されます。例: `outPath=/output/`             |
| outStorageName | 文字列                       | クエリ     | 任意      | 出力ファイルを書き込むクラウドストレージ（例: Amazon S3、Azure Blob）の名前。`outPath` をデフォルト以外のストレージで使用する場合にのみ必要です。               |
| fontsLocation  | 文字列                       | クエリ     | 任意      | サーバー上のカスタムフォントフォルダーへのパス。スプレッドシートでデフォルトライブラリにないフォントが参照されている場合に使用します。                            |
| region         | 文字列                       | クエリ     | 任意      | スプレッドシートの地域/言語設定（例: `en-US`、`fr-FR`）。変換時の数値、日付、通貨の書式に影響を与えます。                                                        |
| password       | 文字列                       | クエリ     | 任意      | パスワードで保護されたスプレッドシートを開くためのパスワード。保護されていないファイルの場合は省略してください。                                                   |

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

| コード | 意味               | 説明                                                             |
| ---- | ----------------- | --------------------------------------------------------------- |
| 200  | OK                | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request       | パラメーターが不足しているか、無効です（例: サポートされていないファイル形式）。 |
| 401  | Unauthorized      | JWT トークンが無効または不足しています。                          |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。             |
| 500  | Internal Server Error | サーバーで予期しないエラーが発生しました。                         |

## Convert Spreadsheet to JSON API の使用例

- **データ移行パイプライン** – 従来の Excel レポートを JSON に変換し、モダンな NoSQL データベースやデータレイクに取り込みます。
- **モバイル・ウェブアプリケーション** – ユーザーがアップロードしたスプレッドシートを、クラウドに元のファイルを保存することなく、クライアント側で描画可能な JSON に迅速に変換します。
- **自動レポート生成** – スプレッドシート入力から直接、下流の分析サービス（例: Power BI、Tableau）用の JSON ペイロードを生成します。
- **サーバーレス関数** – AWS Lambda や Azure Functions などのサーバーレス環境で API を使用し、一時ストレージの管理なしにリアルタイムで変換を実行します。

## Convert Spreadsheet to JSON API の使用メリット

- クラウドネイティブな変換により、処理前に大容量ファイルをストレージにアップロードする必要がなくなり、遅延とストレージコストを削減します。
- 単一リクエストのワークフロー: スプレッドシートをアップロードし、同じ HTTP 呼び出しで JSON を受信し、統合ロジックを簡素化します。
- パスワード保護されたスプレッドシートや地域固有の設定にも対応し、ロケールごとに正確なデータ表現を保証します。
- Aspose のインフラストラクチャ上でスケーラブル：大規模なワークブックや複雑な数式も処理でき、自社サーバーのリソースに影響を与えません。

## SDK を使用して Convert Spreadsheet to JSON API を活用する方法

### Convert Spreadsheet to JSON API の仕様

[Convert Spreadsheet to JSON API の仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToJson) は、Web ブラウザーから直接 REST 呼び出しを実行するための公開可能なプログラミングインターフェースを提供します。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速になります。数行のコードでスプレッドシートを JSON に変換できます。  
Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。  
以下のコード例では、さまざまな SDK を使用して Aspose.Cells Web サービスと対話する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}