---
title: "Aspose.Cells Cloud Web API - リモート Excel ワークシートを他の形式へエクスポートする - 無料オンラインツール"
second_title: "ドキュメント"
ArticleTitle: "リモートスプレッドシートのワークシートを他の形式へエクスポートする方法：ステップ・バイ・ステップガイド"
linktype: "Export Spreadsheet as Format"
type: docs
url: /ja/export-spreadsheet-as-format/
keywords: "Aspose.Cells, スプレッドシート変換, API, エクスポート, PDF, CSV, JSON, XLSX"
description: "Aspose Cloud に保存された Excel ワークブックを、単一の REST エンドポイントで PDF、XLSX、CSV、JSON、または HTML に変換します。リクエスト構文やパラメータの説明、C#、Java、Python などの SDK サンプルを確認できます。"
weight: 100
---

クラウド上のスプレッドシート（Excel）を他のファイル形式へエクスポートします。

## **スプレッドシートを他の形式へエクスポートする API**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必須とします。

### **リクエストパラメータ**

| パラメータ名     | タイプ   | パス／クエリ文字列／HTTP ボディ | 説明                                                                                                                                                 |
| :--------------- | :------- | :---------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | 文字列   | パス                          | （必須）取得するワークブックファイルの名前。                                                                                                         |
| format           | 文字列   | クエリ                        | （必須）出力形式（例："Xlsx"、"PDF"、"CSV"）。                                                                                                       |
| folder           | 文字列   | クエリ                        | （オプション）ワークブックが保存されているフォルダのパス。デフォルトは null。                                                                        |
| storageName      | 文字列   | クエリ                        | （オプション）カスタムクラウドストレージを使用する場合のストレージ名。省略時はデフォルトストレージが使用されます。                                   |
| outPath          | 文字列   | クエリ                        | （オプション）変換後のワークブックを保存するフォルダのパス。デフォルトは null。                                                                      |
| outStorageName   | 文字列   | クエリ                        | （オプション）出力ファイルの保存先ストレージ名。                                                                                                     |
| fontsLocation    | 文字列   | クエリ                        | （オプション）カスタムフォントの場所。                                                                                                               |
| region           | 文字列   | クエリ                        | （オプション）スプレッドシートの地域／言語設定（例：`en-US`、`fr-FR`）。数値書式や日付解析、ロケール固有の動作に影響を与えます。                      |
| password         | 文字列   | クエリ                        | （オプション）スプレッドシートファイルを開くためのパスワード。                                                                                       |

### **レスポンス**

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

レスポンスには、変換されたファイルストリームを表す単一のオブジェクトが含まれます。

**HTTP ステータスコード**

| コード | 意味                   | 説明                                                        |
| ------ | ---------------------- | ----------------------------------------------------------- |
| 200    | OK（成功）             | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request（不正なリクエスト） | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized（未認証） | JWT トークンが無効または不足しています。                         |
| 413    | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルがサイズ制限を超えています。           |
| 500    | Internal Server Error（内部サーバーエラー） | 予期しないサーバーエラーが発生しました。                         |

## スプレッドシートを他の形式へエクスポートする API を使用すべき場面

- **レガシーシステムの移行**：数千のレガシー XLS ファイルを、モダンなシステム向けに XLSX へ変換します。
- **アーカイブの標準化**：さまざまなスプレッドシート形式（XLS、XLSM、ODS、CSV）を、アーカイブ用に単一の形式に統一します。
- **オフィススイートの相互運用性**：Excel ファイルを、LibreOffice、Google スプレッドシート、Apple Numbers と互換性のある形式へ変換します。
- **データソースの正規化**：さまざまなスプレッドシート形式を CSV または JSON へ変換し、データベースへの取り込みを容易にします。
- **ウェブ公開**：財務モデルを HTML へ変換し、ウェブでの表示を実現します。

## なぜスプレッドシートを他の形式へエクスポートする API を使用すべきか

- **開発者フレンドリー**：Aspose.Cells Cloud は、複数の言語向けの SDK ライブラリを提供しており、迅速な開発が可能です。また、包括的なドキュメントも整っています。独自のチャート描画ソリューションを構築する場合と比べ、開発負荷を大幅に削減できます。
- **人的コストの削減**：ドキュメント統合のための専任体制を設ける必要がなくなります。
- **ペイ・パー・ユース**：初期投資不要。実際に使用した API コール分のみの課金です。
- **サーバーサイドのメンテナンス不要**：サーバーの維持管理、ソフトウェアの更新、互換性の問題に対応する必要がありません。
- **幅広い形式サポート**：20種類以上のスプレッドシート形式間での変換が可能です。
- **データと書式の忠実な再現**：変換時に元のレイアウト、数式、スタイルを保持します。

## SDK を使用してスプレッドシートを他の形式へエクスポートする API を利用する方法

### スプレッドシートを他の形式へエクスポートする API の仕様

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat" rel="noopener noreferrer">スプレッドシートを他の形式へエクスポートする API の仕様</a> は、REST インタラクションをシームレスに実行するための公開可能なプログラミングインターフェースを提供します。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード済み)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "オプション：ファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化できるため、最も迅速に開発できます。短いコードでスプレッドシートを目的の形式のファイルへエクスポートできます。  
API を呼び出す前に、OAuth 2.0 アクセストークンを取得し、`Authorization: Bearer <token>` ヘッダーに含めてください。

Aspose.Cells Cloud SDK の完全な一覧は、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を介して Aspose.Cells Web サービスとやりとりする方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
---