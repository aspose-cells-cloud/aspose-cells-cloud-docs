---
title: "セル数式の計算 – Aspose.Cells Cloud API"
type: docs
url: /calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, セル数式の計算, Excel API, REST API, SDK"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して Excel セルの数式を計算します。エンドポイント、パラメーター、cURL の例、および SDK スニペットを含みます。"
ArticleTitle: "セル数式の計算 – Aspose.Cells Cloud API ドキュメント"
---

## REST API

この REST API は、Excel ワークブック内の**セル数式**を計算します。

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

### リクエストパラメーター

| パラメーター名 | 型     | パラメーター位置 (パス/クエリ/ボディ) | 説明                                                  |
| -------------- | ------ | ------------------------------------ | ----------------------------------------------------- |
| name           | string | path                                 | Excel ファイル名 (例: `Book1.xlsx`)。                 |
| sheetName      | string | path                                 | セルを含むワークシート名。                            |
| cellName       | string | path                                 | 計算対象のセルアドレス (例: `A1`)。                   |
| options        | object | body                                 | 計算オプションを含む JSON オブジェクト (下記 **Options オブジェクト** 参照)。 |
| folder         | string | query                                | ファイルが配置されているストレージ内のフォルダー。    |
| storageName    | string | query                                | Aspose Cloud ストレージの名前。                       |

#### Options オブジェクト

| フィールド        | 型      | 説明                                                                  | デフォルト |
| ----------------- | ------- | --------------------------------------------------------------------- | ---------- |
| CalcStackSize     | string  | 最大計算スタックサイズ。                                              | `"1"`      |
| IgnoreError       | boolean | `true` の場合、計算エラーは無視され、セル値は `#N/A` に設定されます。 | `false`    |
| Recursive         | boolean | 依存セルの再帰的計算を有効にします。                                  | `false`    |
| Precision         | string  | 数値結果の小数点以下の桁数。                                          | `"15"`     |
| UseThreading      | boolean | スレッド並列計算を有効にします。                                      | `false`    |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                 | 説明                                               |
| ------ | -------------------- | -------------------------------------------------- |
| 200    | OK                   | フィルターが正常に適用された。レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request          | パラメーターが不足または無効 (例: 非対応のファイル形式)。 |
| 401    | Unauthorized         | JWT トークンが無効または不足している。             |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えている。 |
| 500    | Internal Server Error | サーバー内で予期せぬエラーが発生しました。          |

## SDK を使用した PostCellCalculate API の使い方

### PostCellCalculate API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API を呼び出す方法を示しています。**まず、`/connect/token` エンドポイントに対して認証して JWT トークンを取得し**、`<jwt token>` を実際のトークン値に置き換えてください。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速に進めることができます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}