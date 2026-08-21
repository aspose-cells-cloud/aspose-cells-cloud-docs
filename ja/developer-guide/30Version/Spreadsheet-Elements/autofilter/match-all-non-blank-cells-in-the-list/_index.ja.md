---
title: "Excelワークシート内のすべての空白以外のセルを一致させる"
second_title: "ドキュメント"
linktitle: "すべての空白以外のセルを一致させる"
type: docs
url: /autofilter/match-all-non-blank/
aliases: [/match-all-non-blank-cells-in-the-list/]
keywords: "Aspose.Cells Cloud, 空白以外のセルを一致させる, AutoFilter, Excel API"
description: "Aspose.Cells Cloud REST API を使用して、ExcelワークシートのAutoFilterリスト内のすべての空白以外のセルを一致させる方法を学びます。エンドポイント、パラメータ、認証、レスポンススキーマ、エラーコード、SDKの例を含みます。"
ArticleTitle: "Aspose.Cells Cloud API を使用して Excelワークシート内のすべての空白以外のセルを一致させる"
weight: 100
---

**概要**  
*すべての空白以外のセルを一致させる* 操作は、ワークシートにAutoFilterを適用し、指定された列にデータが含まれている行のみを返し、空のセルは無視します。これは、データセットのクリーニング、レポートの生成、またはさらなる分析のためのデータの準備に役立ちます。

**前提条件**  
- Aspose.Cells Cloudの認証に使用できる有効なJWTトークン。  
- ワークブックはAspose Cloudストレージにアップロードされている必要があります。  
- フィルタを適用したいファイル名、ワークシート名、および0から始まる列インデックス（`fieldIndex`）が必要です。

このREST APIは、ExcelワークシートのAutoFilterリスト内のすべての空白以外のセルを一致させます。

## PostWorksheetMatchNonBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名 | 型      | 位置   | 説明                                                     |
| ------------ | ------- | ------ | --------------------------------------------------------- |
| name         | 文字列  | パス   | Excelファイルの名前。                                     |
| sheetName    | 文字列  | パス   | AutoFilterを含むワークシートの名前。                      |
| fieldIndex   | 整数    | クエリ | フィルタを適用する列の0から始まるインデックス。            |
| folder       | 文字列  | クエリ | _(オプション)_ ファイルが保存されているフォルダのパス。     |
| storageName  | 文字列  | クエリ | _(オプション)_ 使用するストレージサービスの名前。           |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTPステータスコード**

| コード | 意味                         | 説明                                             |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | フィルタが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | リクエストエラー            | 必須パラメータが不足しているか、無効なパラメータ（例：サポートされていないファイル形式）です。 |
| 401  | 認証エラー                  | JWTトークンが無効または不足しています。 |
| 413  | ペイロードが大きすぎます    | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | サーバ内部エラー            | 予期しないサーバエラーが発生しました。 |

*エラー応答の例（400）*  

```json
{
  "Code": 400,
  "Message": "無効なパラメータ: fieldIndexは0以上の整数である必要があります。"
}
```

## SDKを使用した PostWorksheetMatchNonBlanks API の使用方法

### PostWorksheetMatchNonBlanks API 仕様

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接RESTリクエストを実行できるようにします。

cURLコマンドラインツールを使用すると、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例では、cURLを使用してCloud APIに対して呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
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

### Aspose.Cells Cloud SDKの使用

SDKを使用すると、開発を迅速化できます。SDKは低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスに対して呼び出しを行う方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}
---