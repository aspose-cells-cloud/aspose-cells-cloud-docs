---
title: "Aspose.Cells Cloud Web API – ワークシートを HTML に変換"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud API を使用してワークシートを HTML に変換する方法"
linktype: "Convert Worksheet To Html"
type: docs
url: /ja/convert-worksheet-to-html/
description: "Aspose.Cells Cloud API を使用して Excel ワークシートを HTML に変換する方法を学習します。アップロード不要、カスタムフォント対応、地域設定対応、エラーハンドリング機能を備えています。"
keywords: "Aspose.Cells, Excel to HTML, worksheet conversion, cloud API"
weight: 100
---

**ConvertWorksheetToHtml** エンドポイントは、ローカルファイルシステムから Excel ワークブックを読み取り、指定されたワークシートを抽出し、その内容を HTML ファイルとして返します。変換は Aspose のクラウドサーバー上で完全に実行されるため、中間的なアップロードやストレージの利用は不要です。スプレッドシートデータをウェブで表示可能な形式で生成するのに最適で、この API ではオプションの出力パス、カスタムフォント、地域設定、パスワードで保護されたワークブックのサポートが提供されています。

## ワークシートを HTML に変換する API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名     | 型     | 位置     | 必須／オプション | 説明                                                                                                                                                                |
| :---------------- | :----- | :------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | File   | 必須     | FormData         | 処理対象のバイナリ Excel ファイル。有効な .xlsx、.xls、.xlsb などの形式である必要があります。例: `myWorkbook.xlsx`。Excel ファイルはリクエストボディから直接読み込まれ、事前のクラウドストレージへのアップロードは不要です。 |
| worksheet         | String | 必須     | クエリ           | 変換するワークシート名（大文字・小文字を区別）。指定されたワークブック内に存在する必要があります。例: `Sheet1`。                                                      |
| outPath           | String | オプション | クエリ           | 生成された HTML ファイルを保存するクラウドストレージ内のターゲットフォルダーパス。省略した場合、ファイルはレスポンス内で直接返されます。例: `/output/html/`。         |
| outStorageName    | String | オプション | クエリ           | `outPath` で使用するクラウドストレージサービスの名前。`outPath` がデフォルト以外のストレージを指す場合にのみ必要です。                                             |
| fontsLocation     | String | オプション | クエリ           | 変換中に使用するカスタム TrueType/OpenType フォントが格納されたフォルダーへの絶対パス。非標準文字の正しくレンダリングを可能にします。                             |
| region            | String | オプション | クエリ           | 数値・日付の書式設定に影響を与えるロケール識別子（例: `en-US`、`fr-FR`）。デフォルトではワークブック内の内部地域設定が使用されます。                                 |
| password          | String | オプション | クエリ           | 保護されたワークブックを開くために必要なパスワード。保護されていないファイルの場合は指定不要です。                                                                   |

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

| コード | 意味                   | 説明                                           |
| ------ | ---------------------- | ---------------------------------------------- |
| 200    | OK                     | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request            | パラメーターが不足または無効（例: 非対応のファイル形式）。     |
| 401    | Unauthorized           | JWT トークンが無効または不足しています。                      |
| 413    | Payload Too Large      | アップロードされたファイルがサイズ制限を超えています。         |
| 500    | Internal Server Error  | サーバー側で予期しないエラーが発生しました。                   |

## Convert worksheet to HTML API の使用例

- ウェブポータルにライブスプレッドシートデータを埋め込む – 財務レポートのワークシートを HTML に変換し、Excel プラグインなしでブラウザ上で直接表示可能にします。
- Excel テンプレートから印刷用 HTML 請求書を生成 – 事前に定義されたワークシートから、ウェブ表示可能な請求書ページを自動生成します。
- ドキュメントスニペットの作成 – 設計仕様シートを HTML フラグメントに変換し、技術マニュアルや wiki に挿入可能にします。
- ローコード BI ダッシュボードの開発 – ワークシートデータを取得し、それを HTML に変換してカスタムダッシュボードウィジェット内に表示します。

## Convert worksheet to HTML API の利点

- **アップロード不要のワークフロー** – クラウド上でローカルファイルを直接変換し、まず大きなワークブックをストレージに転送する必要を排除します。
- **高性能なレンダリング** – サーバー側での変換により Aspose の最適化されたエンジンが活用され、高速かつ正確な HTML 出力を実現します。
- **出力の完全な制御** – オプションパラメーター（カスタムフォント、地域設定、パスワード）により、ロケールやブランド要件に合わせた HTML をカスタマイズ可能です。
- **シームレスな統合** – multipart/form‑data を使用したシンプルな PUT リクエストは、CI/CD パイプライン、マイクロサービス、サーバーレス関数へ自然に統合可能です。

## SDK を使用して Convert worksheet to HTML API を活用する方法

### Convert worksheet to HTML API の仕様

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtml" target="_blank" rel="noopener noreferrer">Convert Worksheet to HTML API の仕様</a> は、ウェブブラウザから直接 REST アクセスを実行可能なパブリックなプログラミングインターフェースを提供しています。

cURL コマンドラインツールを使用することで、Aspose.Cells のウェブサービスへ簡単にアクセスできます。以下の例では、cURL を使用してクラウド API へリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速に行え、ワークシートを短いコードでマージできます。  
Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud/aspnet-sdk" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud SDK GitHub リポジトリ</a>をご確認ください。  
以下のコード例では、さまざまな SDK を使用して Aspose.Cells ウェブサービスとやり取りする方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}