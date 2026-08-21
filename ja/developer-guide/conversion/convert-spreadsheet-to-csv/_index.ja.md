---
title: "Aspose.Cells Cloud Web API – スプレッドシートを CSV に変換"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud API を使用してスプレッドシートを CSV に変換する方法"
linktitle: "スプレッドシートを CSV に変換"
type: docs
url: /convert-spreadsheet-to-csv/
keywords: "Aspose Cells, CSV変換, Excel API, クラウド変換"
description: "Aspose.Cells Cloud API を使用して Excel ファイル（XLS、XLSX、XLSM など）を CSV に変換する方法を学びます。認証手順、cURL サンプル、SDK コードスニペット、エラー処理が含まれます。"
weight: 100
---

**ConvertSpreadsheetToCsv** エンドポイントは、ローカルドライブからアップロードされたスプレッドシートファイルを読み込み、その変換処理をすべて Aspose.Cells Cloud サーバー上で実行し、結果として得られた CSV ファイルをバイナリストリームとして返します。このクラウドネイティブな操作により、ソースファイルをクラウドストレージにアップロードする必要がなくなり、ストレージコストを削減し、迅速なスプレッドシートから CSV への変換が必要な開発者のワークフローを簡素化します。サポートされるフォーマットは、基盤となるライブラリに依存し、ソースファイルを読み込むには適切な権限が必要です。ファイルが見つからない、リクエストが無効、または変換に失敗したなどのエラーは、標準的な HTTP ステータスコードで返されます。

## **スプレッドシートを CSV に変換する API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/csv
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### **リクエストパラメーター**

| パラメーター名    | 型     | 位置       | 必須/任意 | 説明                                                                                                                                                              |
| :---------------- | :----- | :--------- | :-------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | ファイル | FormData   | 必須      | 変換するスプレッドシートファイル。.xls、.xlsx、.xlsm などの一般的なフォーマットを受け付けます。multipart/form-data として提供する必要があります。例: `myWorkbook.xlsx`      |
| outPath           | 文字列  | クエリ     | 任意      | 変換された CSV を保存する宛先フォルダーのパス。指定しない場合、CSV はレスポンス本体内に直接返されます。例: `/output/reports/`                                      |
| outStorageName    | 文字列  | クエリ     | 任意      | 出力ファイルを保存するクラウドストレージサービスの名前。指定されない場合、Aspose.Cells アカウントに設定されたデフォルトストレージが使用されます。                  |
| fontsLocation     | 文字列  | クエリ     | 任意      | スプレッドシートに必要なカスタムフォントを含むフォルダーのパス。非標準フォントを使用するセルの正しくレンダリングを可能にします。                                 |
| region            | 文字列  | クエリ     | 任意      | スプレッドシートの地域/言語設定（例: `en-US`、`fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響を与えます。                                           |
| password          | 文字列  | クエリ     | 任意      | パスワードで保護されたスプレッドシートを開くために使用するパスワード。ファイルが暗号化されていてパスワードが省略された、または不正な場合、400/401 エラーが返されます。 |

### **レスポンス**

成功した場合、API は **HTTP 200**（または非同期処理の場合は **202**）を返し、ヘッダー `Content-Type: application/octet-stream` を含みます。レスポンス本体には、生成された CSV ファイルがバイナリストリームとして含まれます。

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

| コード | 意味                     | 説明                                                     |
| ------ | ------------------------ | -------------------------------------------------------- |
| 200    | OK（成功）               | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request（不正なリクエスト） | パラメーターが不足している、または無効（例: サポートされていないファイル形式） |
| 401    | Unauthorized（未認証）       | JWT トークンが無効、または不足している。                     |
| 413    | Payload Too Large（ペイロードが大きすぎる） | アップロードされたファイルがサイズ制限を超えた。               |
| 500    | Internal Server Error（内部サーバーエラー） | 予期しないサーバーエラーが発生しました。                       |

## どこでスプレッドシートを CSV に変換する API を使用すべきか？

- **レポーティングシステムのためのデータエクスポート** – Excel ベースのレポートから CSV 抽出データを生成し、手動でのファイル処理なしに BI ツールやデータウェアハウスにデータを供給します。
- **自動バッチ処理** – サーバーサイドのジョブで多数のローカルに保存されたスプレッドシートを CSV に変換し、結果を直接下流のサービスへストリーミングします。
- **ファイルアップロードを伴う Web アプリケーション** – エンドユーザーが Excel ファイルをアップロードし、その後の分析や他のプラットフォームへのインポート用に CSV バージョンを即座に取得できるようにします。
- **レガシーシステムとの統合** – レガシーなスプレッドシートフォーマットを、プレーンテキストの区切り文字ファイルのみを受け入れるシステム用に CSV に変換します。

## なぜスプレッドシートを CSV に変換する API を使用すべきか？

- **アップロード不要アーキテクチャ** – ソースファイルをクラウドストレージに保存する必要がなく、直接アップロードされたストリームから変換が実行されるため、時間とストレージコストを節約できます。
- **高性能クラウド処理** – スケーラブルなクラウドサーバー上で Aspose.Cells の最適化された変換エンジンを活用し、大規模なワークブックでも高速に CSV 出力を提供します。
- **シンプルな統合** – オプションのクエリパラメーターを伴う単一の PUT リクエスト。CSV を即座にダウンロード可能なバイナリストリームとして返すため、追加の後処理ステップが不要です。
- **フル機能サポート** – パスワードで保護されたファイル、カスタムフォント、ロケール固有の設定を処理し、複雑なスプレッドシートでも正確な変換を保証します。

## SDK を使用してスプレッドシートを CSV に変換する API を利用する方法

### スプレッドシートを CSV に変換する API の仕様

[スプレッドシートを CSV に変換する API の仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToCsv) は、Web ブラウザーから直接 REST 操作を実行するための公開可能なプログラミングインターフェースを提供します。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

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

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最速になります。簡潔なコードでスプレッドシートを操作できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスとやり取りする方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToCsv.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToCsv.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToCsv.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToCsv.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToCsv.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToCsv.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToCsv.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToCsv.go" >}}
{{</tab>}}
{{< /tabs >}}