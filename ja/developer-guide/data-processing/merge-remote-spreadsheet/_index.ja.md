---
title: "Aspose.Cells Cloud – クラウドで Excel ファイルをマージ | API 経由でスプレッドシートを結合"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "クラウドで Excel ファイルをマージ | Aspose.Cells Cloud API を使用してオンラインでスプレッドシートを結合"
linktype: "Merge Remote Spreadsheet"
type: docs
url: /merge-remote-spreadsheet/
keywords: "Aspose.Cells, Excel マージ, クラウド API, スプレッドシート結合"
description: "Aspose.Cells Cloud API を使用してクラウドストレージに保存されている Excel ワークブックをマージします。出力形式、出力フォルダ、マージモードを 1 回の HTTPS 呼び出しで指定できます。"
weight: 100
---

クラウドに保存された Excel ファイルを Aspose.Cells Cloud API を使用して他のスプレッドシートにすばやくマージし、出力データの形式および保存先を指定できます。

## リモートスプレッドシートのマージ API

この操作を呼び出す前に、以下の条件を満たしていることを確認してください。

- 有効な **JWT アクセストークン** を取得していること（認証ガイドを参照）。
- 結合元のワークブックおよびマージ対象のすべてのファイルがクラウドストレージにアップロードされていること。
- 結合元フォルダからの読み取り権限と、出力先フォルダへの書き込み権限を所有していること。

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名        | 型      | パス / クエリ文字列 / HTTP ボディ | 説明                                                                                                                                      |
| :---------------- | :------ | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------- |
| name              | 文字列  | パス                       | マージ対象のソースワークブックファイル名。                                                                                                 |
| mergedSpreadsheet | 文字列  | クエリ                     | ソースワークブックにマージするスプレッドシートファイル名のコンマ区切りリスト。                                                              |
| folder            | 文字列  | クエリ                     | ソースワークブックを含むクラウドストレージ上のフォルダパス。                                                                                |
| outFormat         | 文字列  | クエリ                     | マージ後の出力ファイルの希望フォーマット（例：`XLSX`、`PDF`、`CSV`）。                                                                       |
| mergeInOneSheet   | 真偽値  | クエリ                     | `true` を設定するとすべてのソースデータを 1 つのワークシートにマージします。`false` の場合は各ファイルごとに別々のワークシートを作成します。     |
| storageName       | 文字列  | クエリ                     | （省略可）ソースワークブックが格納されているクラウドストレージの名前。省略した場合、デフォルトストレージが使用されます。                      |
| outPath           | 文字列  | クエリ                     | （省略可）マージされたファイルを保存するクラウドストレージ上の出力先フォルダパス。省略した場合、ファイルはソースフォルダに保存されます。         |
| outStorageName    | 文字列  | クエリ                     | 出力ファイルを保存するクラウドストレージの名前。                                                                                            |
| fontsLocation     | 文字列  | クエリ                     | （省略可）画像/PDF 形式への変換時に使用されるフォントファイル用のカスタムフォルダパス。                                                       |
| region            | 文字列  | クエリ                     | （省略可）出力ファイルの日付・数値・通貨の書式設定に使用するロケール／地域（例：`en-US`、`de-DE`）。                                             |
| password          | 文字列  | クエリ                     | （省略可）ソースワークブックがパスワード保護されている場合に必要なパスワード。                                                                |

### レスポンス

**ステータス:** `200 OK`

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

ファイルは `outPath` で指定された場所から直接ダウンロードまたは保存できます。

**成功レスポンスの詳細**

| ステータスコード | コンテンツタイプ           | 説明                             |
| -------------- | ------------------------ | -------------------------------- |
| 200 OK         | `application/octet-stream` | マージされたワークブックファイルのバイナリストリーム。 |

**HTTP ステータスコード**

| コード | 意味              | 説明                                           |
| ---- | --------------- | --------------------------------------------- |
| 200  | OK              | フィルター適用成功。レスポンスには操作の詳細が含まれます。     |
| 400  | Bad Request     | パラメータ不足または不正（例：サポートされていないファイルタイプ）。 |
| 401  | Unauthorized    | 無効または不足している JWT トークン。             |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。           |
| 500  | Internal Server Error | サーバー内部で予期せぬエラーが発生しました。                    |

## どこでリモートスプレッドシートのマージ API を使用すべきか？

### エンタープライズグレードのデータ統合

- **複数部門のレポート集計** – 営業、マーケティング、財務などの各チームが提出した個別の Excel レポートを統合します。
- **支店ごとのデータ要約** – 世界中の各支店からの業績データを要約します。
- **パートナーからのデータ統合** – 複数のパートナーから提出されたデータを単一ワークブックにマージします。

### クラウドドキュメント処理ワークフロー

- クラウドストレージのファイル処理：AWS S3、Azure Blob、Google Cloud Storage に保存された Excel ファイルを直接マージします。
- **複数ソースからのデータ統合** – 異なるクラウドの場所にあるファイルを単一ワークブックに結合します。
- **自動データパイプライン** – ETL プロセスに API を統合し、ファイルマージを自動化します。

### ドキュメント管理の自動化

- **バージョン管理の統合** – プロジェクト計画や予算ワークブックの異なるバージョンをマージします。
- **テンプレートへのデータ挿入** – 標準化されたレポートテンプレートにデータファイルを挿入します。
- **定期レポートの生成** – 週次・月次・四半期報告書の生成を自動化します。

### クロスプラットフォーム共同作業

- **リモートチームの共同作業** – 離れた場所にいるチームメンバーが提出した作業内容を統合します。
- **顧客データの整理** – 複数の顧客から得た注文データやフィードバックデータをマージします。
- **サプライヤー情報の要約** – 複数のサプライヤーから得た見積りや製品情報を統合します。

## なぜリモートスプレッドシートのマージ API を使用すべきか？

- **開発者に優しい** – Aspose.Cells Cloud は多言語向け SDK を提供しており、開発時間を短縮し、包括的なドキュメントを提供します。カスタムソリューションの構築と比較すると、作業負荷を大幅に削減します。
- **人件費の削減** – 手動でのドキュメント統合に専任のスタッフを配置する必要性を軽減します。
- **ペイ・パー・ユース** – 初期投資不要。実際に使用した API 呼び出し分のみ料金が発生します。
- **メンテナンスコストゼロ** – サーバーの管理やソフトウェアの更新、互換性の懸念がありません。

## SDK を使用してリモートスプレッドシートのマージ API を使用する方法

### リモートスプレッドシートのマージ API 仕様

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet" target="_blank" rel="noopener noreferrer">リモートスプレッドシートのマージ API 仕様</a> は、任意の HTTP クライアントから直接呼び出すことができる REST インターフェースを記述しています。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/merge/spreadsheet?mergedSpreadsheet=Report1.xlsx&outFormat=XLSX&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}"
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

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化し、短いコードスニペットでスプレッドシートを別のスプレッドシートにマージできるため、開発が最も速く行えます。  
Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスと対話する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}