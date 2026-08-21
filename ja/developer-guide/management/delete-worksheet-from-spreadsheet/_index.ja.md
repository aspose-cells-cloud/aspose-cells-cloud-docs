---
title: "Aspose.Cells Cloud Excel シート削除 Web API - ワークブックからシートをプログラムで削除する"
second_title: "ドキュメント"
ArticleTitle: "Excel からワークシートを削除する方法 - ワークブックからシートを削除する"
linktitle: "スプレッドシートからワークシートを削除"
type: docs
url: /ja/delete-worksheet-from-spreadsheet/
keywords: "Aspose Cells, delete worksheet API, Excel シート削除, クラウドスプレッドシート, REST API"
description: "Aspose.Cells Cloud API を使用して Excel ファイルからワークシートを削除する方法を学びます。エンドポイント、パラメーター、サンプル cURL、および SDK の例を含みます。"
weight: 100
---

Aspose.Cells Cloud API を使用して、Excel ワークブックからワークシートをプログラムで削除します。単一または複数のシートを安全に削除し、ワークブック構造をクリーンアップして、スプレッドシートの最適化を自動化します。エンタープライズグレードの Excel 管理およびドキュメント処理ワークフロー向けの RESTful API です。

## スプレッドシートからワークシートを削除する API

### Web API

```http
PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName={sheetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}"
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名 | 型     | 位置       | 説明                                                                                                                                                                                                 |
| :------------- | :----- | :--------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | ファイル | FormData   | **必須。** ワークシートを削除する元の Excel ワークブックファイル（.xlsx、.xls など）。                                                                                                               |
| sheetName      | 文字列 | クエリ     | **必須。** 削除するワークシートの正確な名前（例: `Sheet1`、`TemporaryData`）。                                                                                                                       |
| outPath        | 文字列 | クエリ     | **任意。** 変更されたワークブックを保存するクラウドストレージ内のターゲットフォルダーパス。省略または `null` の場合、ワークブックは元のファイルと同じ場所またはデフォルトパスに保存されます。         |
| outStorageName | 文字列 | クエリ     | **任意。** 出力ファイルを書き込むクラウドストレージサービスの識別子（例: `ProjectStorage`）。指定しない場合、デフォルトのストレージが使用されます。                                                   |
| region         | 文字列 | クエリ     | **任意。** 保存操作中に地域固有の数式やデータに影響を与える可能性があるロケール設定（例: `it-IT`）。                                                                                                  |
| password       | 文字列 | クエリ     | **任意。** パスワード保護されたスプレッドシートを開いて変更するために必要なパスワード。ファイルが暗号化されていない場合は省略してください。                                                           |

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

| コード | 意味                 | 説明                                                 |
| ---- | -------------------- | ---------------------------------------------------- |
| 200  | OK（成功）           | フィルターが正常に適用され、応答には操作の詳細が含まれます。 |
| 400  | 不正リクエスト       | パラメーターが不足または無効（例: サポートされていないファイル形式）。 |
| 401  | 認証されていません   | 無効または不足している JWT トークン。                 |
| 413  | ペイロードが大きすぎます | アップロードされたファイルがサイズ制限を超えています。       |
| 500  | サーバー内部エラー   | 予期しないサーバーエラー。                            |

## どこでスプレッドシートからワークシートを削除する API を使用すべきか？

- **自動レポートの後処理** – 最終的な財務レポートを生成した後、一時的な計算に使用された中間ワークシートを自動的に削除し、最終ファイルをクリーンでプロフェッショナルな状態に保ちます。
- **テンプレートファイルの動的クリーンアップ** – ユーザーがテンプレートからカスタマイズされたドキュメント（例: 見積もり）を生成する際、選択されなかったオプションページを削除します。
- **ワークフローのアーカイブ最適化** – プロジェクトまたは監査が完了した後、ドラフトまたは共同作業用ワークシートを削除し、アーカイブおよびコンプライアンス用に最終バージョンのみを保持します。

## なぜスプレッドシートからワークシートを削除する API を使用すべきか？

- **開発者フレンドリー** – Aspose.Cells Cloud は複数の言語向けの SDK ライブラリを提供し、迅速な開発を可能にし、包括的なドキュメントを提供します。
- **労務コストの削減** – ドキュメントを手動で統合するための専任人員の必要性を排除します。
- **従量課金制** – 初期投資不要。実際に使用した API コールのみに料金が発生します。
- **メンテナンスコストゼロ** – メンテナンスするサーバーが不要で、ソフトウェアの更新や互換性の問題もありません。

## SDK を使用してスプレッドシートからワークシートを削除する API を使用する方法

### スプレッドシートからワークシートを削除する API の仕様

<a href="https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet" rel="noopener noreferrer">スプレッドシートからワークシートを削除する API の仕様</a>は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード済み)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化し、最小限のコードでワークシートを削除できるため、開発が最も迅速に行えます。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリー</a>を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}