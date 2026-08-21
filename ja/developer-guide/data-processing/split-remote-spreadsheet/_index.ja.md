---
title: "Aspose.Cells Cloud スプレッドシート分割 Web API - Excel ワークブックを 30 以上の形式で複数のファイルに分割"
second_title: "ドキュメント"
ArticleTitle: "クラウドで Excel ファイルを分割して個別のファイルに分離し、30 以上の形式にエクスポート"
linktype: "クラウド上のスプレッドシートを分割"
type: docs
url: /ja/split-remote-spreadsheet/
keywords: "Aspose.Cells Cloud、Excel ワークブックの分割、スプレッドシート分割ツール、クラウド API、PDF へのエクスポート、CSV へのエクスポート、JSON へのエクスポート、複数形式エクスポート、クラウドスプレッドシート処理"
description: "Aspose.Cells Cloud API を使用して、クラウドストレージに保存された Excel ワークブックを個々のワークシートに分割し、各パートを PDF、CSV、JSON、XLSX、HTML、ODS、XPS など 30 以上の形式でエクスポートします。"
weight: 100
---

クラウドに保存された大規模な Excel ワークブックをワークシート単位で個別のファイルに分割し、各ファイルを PDF、CSV、JSON、ODS、XPS など 30 以上の出力形式でエクスポートします。これには Aspose.Cells Cloud を使用します。

## **クラウド上のスプレッドシートを分割する API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### **リクエストパラメーター**

| パラメーター名 | 型     | パス／クエリ文字列／HTTP ボディ | 説明                                                                                                                     |
| :------------- | :----- | :---------------------------- | :----------------------------------------------------------------------------------------------------------------------- |
| name           | 文字列 | パス                          | 分割対象のワークブックファイル名（例：`data.xlsx`）。指定されたクラウドストレージフォルダー内に存在します。             |
| folder         | 文字列 | クエリ                        | 元のワークブックが保存されているクラウドストレージフォルダーのパス。                                                    |
| from           | 整数   | クエリ                        | 分割操作の開始ワークシートインデックス（0 から始まる）。例：`0` は最初のワークシートを示します。                          |
| to             | 整数   | クエリ                        | 分割操作の終了ワークシートインデックス（0 から始まる）。例：`2` はワークシート 0、1、2 を分割します。                      |
| outFormat      | 文字列 | クエリ                        | 分割されたファイルの出力形式。サポートされる形式には `XLSX`、`PDF`、`CSV`、`JSON`、`HTML` など 30 以上があります。         |
| storageName    | 文字列 | クエリ                        | （オプション）元のワークブックが存在するクラウドストレージの名前。省略した場合、デフォルトのクラウドストレージが使用されます。 |
| outPath        | 文字列 | クエリ                        | （オプション）分割されたファイルを保存するクラウドフォルダーのパス。省略した場合、ファイルは元のフォルダーに保存されます。   |
| outStorageName | 文字列 | クエリ                        | 出力された分割ファイルを保存するクラウドストレージの名前。                                                               |
| fontsLocation  | 文字列 | クエリ                        | （オプション）PDF や画像出力での適切なテキスト描画用にフォントファイルを含むカスタムクラウドフォルダーのパスを指定します。   |
| region         | 文字列 | クエリ                        | （オプション）出力ファイルにおける数値・日付・通貨のロケール設定（例：`"en-US"`、`"zh-CN"`、`"de-DE"`）。                 |
| password       | 文字列 | クエリ                        | （オプション）元のワークブックがパスワード保護されている場合は、ファイルを開くためのパスワードを指定します。               |

## **レスポンス**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

ファイルは `outPath` で指定された場所から直接ダウンロードするか、その場所に保存できます。

**成功レスポンスの詳細**

| ステータスコード | コンテンツタイプ           | 説明                                         |
| ---------------- | -------------------------- | -------------------------------------------- |
| 200 OK           | `application/octet-stream` | 合成されたワークブックファイルのバイナリストリーム。 |

**HTTP ステータスコード**

| コード | 意味             | 説明                                                             |
| ------ | ---------------- | ---------------------------------------------------------------- |
| 200    | OK               | フィルターが正常に適用され、レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request      | パラメーターが不足または不正（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized     | JWT トークンが不正または不足しています。                         |
| 413    | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。           |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。                        |

## クラウド上のスプレッドシートを分割する API の使用例

- **部門別データ配布**：複数部門のデータを含む統合ワークブックを、部門別に個別のファイルに分割。
- **地域別レポート配布**：全国の売上報告書を地域ごとに個別のレポートファイルに分割。
- **顧客データマスキング配布**：機密情報を含むワークブックを、顧客向け専用のファイルに分割。
- **定期レポートの分割**：月次でサマリーレポートを自動的に週次または日次レポートに分割。
- **多形式配布**：1 つの Excel ファイルを PDF、CSV、JSON などの複数形式で同時に分割。
- **テンプレート分割**：事前定義されたテンプレートに基づき、データファイルを標準化された出力ファイルに分割。
- **データソース前処理**：Excel ファイルを標準化された CSV ファイルに分割し、データベースへのロード前に処理。
- **API 用データ準備**：大規模なデータセットを API 送信に適した小さなチャンクに分割。
- **マイクロサービス向けデータ配布**：中央データファイルを、各マイクロサービスが必要とする個別のデータファイルに分割。

## なぜクラウド上のスプレッドシートを分割する API を使用すべきか？

- **開発者フレンドリー**：Aspose.Cells Cloud は複数言語の SDK ライブラリを提供しており、迅速な開発が可能で、豊富なドキュメントも整備されています。カスタムのチャート描画ソリューションを構築する場合と比べ、開発作業量を大幅に削減できます。
- **人件費削減**：ドキュメント統合専任の職員を減らすことができます。
- **従量課金制**：初期投資不要。実際に使用した API コールのみに課金されます。
- **メンテナンスコストゼロ**：サーバーの保守、ソフトウェアの更新、互換性の問題に対処する必要がありません。
- **複雑な Excel 書式を PDF 形式で保持**：汎用的にアクセス可能な PDF 形式で、複雑な Excel 書式を保持します。

## SDK を使用したクラウド上のスプレッドシート分割 API の使い方

### クラウド上のスプレッドシート分割 API の仕様

[クラウド上のスプレッドシート分割 API の仕様](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを可能にします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Report.xlsx/split/spreadsheet?folder=Input&outFormat=PDF&from=0&to=2" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
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

SDK を使用すると、低レベルの詳細が抽象化されるため、クラウドに保存されたスプレッドシートを短いコードで個別のファイルに分割して開発を最速で行えます。  
Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。  
以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{</tab>}}
{{< /tabs >}}