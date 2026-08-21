---
title: "Aspose.Cells Cloud – Excel の範囲を HTML に変換"
description: "Aspose.Cells Cloud REST API を使用して、Excel ファイルの特定の範囲 (例: A1:C10) を HTML ファイルに変換します。認証、リクエストの例、レスポンス処理、SDK スニペット、エラーコードを含みます。"
keywords: "Aspose.Cells, Excel to HTML, 範囲変換, クラウド API, スプレッドシート"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

ローカルの Excel ワークブックから選択した範囲を、Aspose.Cells Cloud を通じて直接 HTML ファイルに変換します。この変換はすべてクラウドサーバー上で実行されるため、ワークブック全体をアップロードする必要はなく、またローカルに Excel をインストールする必要もありません。

## 範囲を HTML に変換する API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

リクエストボディは `multipart/form-data` で、スプレッドシートファイルを含みます。その他のオプションはすべてクエリパラメータとして指定します。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| 名前               | 型      | 位置       | 必須   | 説明                                                                 |
| ------------------ | ------- | ---------- | ------ | -------------------------------------------------------------------- |
| **Spreadsheet**    | ファイル | FormData   | はい    | 変換する Excel ワークブック。                                        |
| **worksheet**      | 文字列   | クエリ     | はい    | 範囲を含むワークシートの名前。                                        |
| **range**          | 文字列   | クエリ     | はい    | 変換するセル範囲 (例: `A1:C10`)。                                    |
| **outPath**        | 文字列   | クエリ     | いいえ  | 生成された HTML ファイルを保存するフォルダーパス (デフォルト `null`)。|
| **outStorageName** | 文字列   | クエリ     | いいえ  | 出力ファイルを保存するストレージサービスの名前。                     |
| **fontsLocation**  | 文字列   | クエリ     | いいえ  | カスタムフォントフォルダーのパス。                                   |
| **AutoRowsFit**    | 真偽値   | クエリ     | いいえ  | ワークシート内のすべての行を自動的に最适合します。                   |
| **AutoColumnsFit** | 真偽値   | クエリ     | いいえ  | ワークシート内のすべての列を自動的に最适合します。                   |
| **region**         | 文字列   | クエリ     | いいえ  | ロケール識別子 (例: `en-US`, `fr-FR`)。数値・日付の書式に影響します。|
| **password**       | 文字列   | クエリ     | いいえ  | パスワードで保護されたワークブックを開くためのパスワード。           |
| **fontsLocation**  | 文字列   | クエリ     | いいえ  | カスタムフォントの場所。                                             |
| **region**         | 文字列   | クエリ     | いいえ  | スプレッドシートの地域/言語設定。                                    |
| **password**       | 文字列   | クエリ     | いいえ  | スプレッドシートファイルを開くためのパスワード。                     |

## レスポンス

API は変換された HTML ファイルを **バイナリストリーム** (`application/octet-stream`) として返します。

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

### 成功レスポンスの例 (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

レスポンスボディをファイル (例: `report.html`) として保存すると、ブラウザで描画された表を表示できます。

---

**HTTP ステータスコード**

| コード | 意味           | 説明                                       |
| ------ | -------------- | ------------------------------------------ |
| 200    | OK             | フィルターが正常に適用された。             |
| 400    | Bad Request    | パラメータが不足または不正 (例: 非対応のファイル形式)。 |
| 401    | Unauthorized   | JWT トークンが無効または不足している。     |
| 413    | Payload Too Large | アップロードされたファイルがサイズ制限を超えた。 |
| 500    | Internal Server Error | サーバー側で予期せぬエラーが発生した。   |

## SDK を使用して範囲を HTML に変換する API を利用する方法

### OpenAPI スペック

[OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) はパブリックにアクセス可能な API を定義しており、Web ブラウザから直接 REST API を利用できます。

cURL コマンドラインツールを使用して、Aspose.Cells クラウドサービスに簡単にアクセスできます。以下の例では、cURL を使ってクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化して、少ないコードでデータ範囲を HTML ファイルに変換できるため、開発が最も迅速になります。  
Aspose.Cells Cloud SDK の完全なリストは、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)でご確認ください。

以下のコード例では、さまざまな SDK を使って Aspose.Cells クラウドサービスを呼び出す方法を示しています。Gist からの読み込みがブロックされた場合は、リポジトリから直接サンプルをダウンロードできます。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}