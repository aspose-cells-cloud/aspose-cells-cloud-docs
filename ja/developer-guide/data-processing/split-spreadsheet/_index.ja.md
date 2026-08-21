---
title: "Aspose.Cells Cloud Split Excel Web API – Excel ファイルをローカルで複数のファイルに分割し、30 以上の形式にエクスポート"
second_title: "ドキュメント"
ArticleTitle: "Excel 分割ツール – ローカルのスプレッドシートを 30 以上の形式でファイルに分割"
linktype: "スプレッドシートの分割"
type: docs
url: /ja/split-spreadsheet/
keywords: "分割, Excel, Aspose.Cells, スプレッドシート API, PDF エクスポート, CSV, JSON"
description: "Aspose.Cells Cloud API を使用して、Excel ワークブックをローカルで別々のファイルに分割します。クラウドへのアップロードは不要で、PDF、CSV、JSON、XLSX、HTML など 30 以上の形式にエクスポートできます。"
weight: 100
---

クラウドストレージを一切使用せずに、ローカルの Excel ワークブックを別々のファイルに完全に分割します。出力は PDF、CSV、JSON、ODS、XPS など 30 以上のファイル形式をサポートしています。

## **スプレッドシート分割 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメータ**

| パラメータ名   | 型     | パス / クエリ文字列 / HTTP ボディ | 説明                                                                                                                                                                    |
| :------------- | :------ | :------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | ファイル | FormData                         | 分割するローカルのスプレッドシートファイル。対応形式には XLSX、XLS、ODS、CSV などがあります。ファイルはクラウドストレージを必要とせず、サーバー側で完全に処理されます。     |
| from           | 整数   | クエリ                           | 分割するワークシート範囲の開始インデックス（0 から始まる）。例: 最初のワークシートを指定する場合は `0`。                                                                  |
| to             | 整数   | クエリ                           | 分割するワークシート範囲の終了インデックス（0 から始まる）。例: `2` を指定すると、ワークシート 0、1、2 を分割します。                                                     |
| outFormat      | 文字列 | クエリ                           | 分割後のファイルの出力形式。`PDF`、`CSV`、`JSON`、`XLSX`、`HTML` など 30 以上の形式をサポートします。                                                                  |
| outPath        | 文字列 | クエリ                           | _(任意)_ 分割された出力ファイルを保存するローカルフォルダパス。指定しない場合は、デフォルトの一時的な場所に保存されます。                                               |
| outStorageName | 文字列 | クエリ                           | 出力ファイルを整理するためのストレージ識別子。ローカル処理モードでは、通常、セッションベースまたはユーザー定義のストレージラベルを指します。                            |
| fontsLocation  | 文字列 | クエリ                           | _(任意)_ PDF または画像形式へのエクスポート時にテキストのレンダリングを正確に行うための、ローカルまたはカスタムフォントディレクトリを指定します。                        |
| region         | 文字列 | クエリ                           | _(任意)_ 出力ファイルにおける数値、日付、通貨の書式設定に使用するロケールを設定します（例: `"en-US"`、`"de-DE"`）。                                                     |
| password       | 文字列 | クエリ                           | _(任意)_ アップロードされたスプレッドシートがパスワードで保護されている場合、ファイルを開いて処理するためにパスワードを指定します。                                   |

## **レスポンス**

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

ファイルは、`outPath` で指定された場所から直接ダウンロードするか、その場所に保存できます。

**正常応答の詳細**

| ステータスコード | コンテンツタイプ           | 説明                         |
| ---------------- | -------------------------- | ---------------------------- |
| 200 OK           | `application/octet-stream` | 結合されたワークブックファイルのバイナリストリーム。 |

**HTTP ステータスコード**

| コード | 意味             | 説明                                                       |
| ------ | ---------------- | ---------------------------------------------------------- |
| 200    | OK               | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足または無効（例: 非対応のファイル形式）。     |
| 401    | Unauthorized     | 無効または不足している JWT トークン。                        |
| 413    | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。       |
| 500    | Internal Server Error | サーバーで予期しないエラーが発生しました。                   |

## スプレッドシート分割 API の使用例

- **部署別データ配布**: 複数の部署のデータを含む統合ワークブックを、部署別のファイルに分割。
- **地域別レポート配布**: 国全体の売上報告書を、地域別のレポートファイルに分割。
- **顧客データマスキング配布**: 機密情報を含むワークブックを、顧客ビュー用に簡略化されたファイルに分割。
- **定期レポートの分割**: 月次で、サマリーレポートを自動的に週次または日次レポートに分割。
- **マルチフォーマット配布**: 単一の Excel ファイルを、PDF、CSV、JSON など複数の形式で同時に分割。
- **テンプレートベースの分割**: 事前定義されたテンプレートに基づき、データファイルを標準化された出力ファイルに分割。
- **データソースの前処理**: Excel ファイルを標準化された CSV ファイルに分割し、データベースへのロード前に準備。
- **API 用データ準備**: 大規模なデータセットを、API での転送に適した小さなチャンクに分割。

## なぜスプレッドシート分割 API を使用すべきか？

- **開発者フレンドリー**: Aspose.Cells Cloud は複数の言語向け SDK ライブラリを提供しており、迅速な開発が可能で、包括的なドキュメントも整備されています。独自のチャート描画ソリューションを構築する場合と比べ、開発工数を大幅に削減できます。
- **人件費削減**: 文書統合に特化した職位の削減が可能。
- **ペイ-per-use（使用量課金）**: 初期投資不要で、実際に使用した API 呼び出し分のみに料金が発生。
- **メンテナンスコストゼロ**: サーバーの維持、ソフトウェアの更新、互換性の問題への対応が不要。
- **複雑な Excel 書式を PDF 形式で維持**: 汎用的にアクセス可能な PDF 形式で、複雑な Excel 書式を保持。

## SDK を使用したスプレッドシート分割 API の利用方法

### スプレッドシート分割 API の仕様

[スプレッドシート分割 API の仕様](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) は、Web ブラウザから直接 REST 通信を行うための公開プログラミングインターフェースを提供します。
cURL コマンドラインツールを使用して、Aspose.Cells Web サービスを簡単に利用できます。以下の例は、cURL を使用して Cloud API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/spreadsheet?outFormat=PDF" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o split-spreadsheet.zip
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

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速に行え、短いコードでスプレッドシートを別々のファイルに分割できます。  
Aspose.Cells Cloud SDK の完全な一覧は、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご覧ください。

以下のコード例は、異なる SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}