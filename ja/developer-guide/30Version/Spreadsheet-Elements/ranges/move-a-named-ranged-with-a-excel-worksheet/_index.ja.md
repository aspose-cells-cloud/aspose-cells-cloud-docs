---
title: "Excelワークシート内で名前付き範囲を移動する"
second_title: "Document"
linktitle: "移動"
type: docs
url: /ranges/move/
aliases: [/move-a-named-range-with-an-excel-worksheet/]
keywords: "Aspose.Cells Cloud, 名前付き範囲の移動, Excelワークシート, REST API, 範囲の移動, SDK サンプル"
description: "Aspose.Cells Cloud REST API v3.0 を使用して、Excelワークシート内で名前付き範囲を移動する方法を学びます。エンドポイントの詳細、認証、例、および SDK コードサンプルを含みます。"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API を使用して Excelワークシート内で名前付き範囲を移動する"
---

名前付き範囲を移動することは、データをプログラムで再編成する必要がある際に一般的なタスクです。このセクションでは、Aspose.Cells Cloud REST API を使用して、同じワークシート上の新しい位置に定義済みの範囲を移動する方法を説明します。

この REST API は、Excelワークシート上の指定された範囲を別の範囲の宛先に移動します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### 認証
API は、Aspose Cloud OAuth フローを通じて取得した **Bearer JWT トークン** を必要とします。このトークンは `Authorization` ヘッダーに含めてください：

```
Authorization: Bearer <jwt token>
```

トークンには **Cells** スコープが必要です。

### 前提条件
- ワークブックは Aspose Cloud ストレージ内に保存されている必要があります。  
- ファイルがルートディレクトリにない場合は、ストレージ名 (`storageName`) とフォルダーパス (`folder`) を指定してください。  
- API バージョン **v3.0** をサポートする最新の Aspose.Cells Cloud SDK を使用してください。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| 名前             | タイプ   | 位置   | 説明 |
|------------------|----------|--------|-------------|
| **name**         | 文字列   | パス   | ワークブックファイルの名前 |
| **sheetName**    | 文字列   | パス   | ワークシートの名前 |
| **destRow**      | 整数     | クエリ | 移動先範囲の開始行インデックス（0 から始まる） |
| **destColumn**   | 整数     | クエリ | 移動先範囲の開始列インデックス（0 から始まる） |
| **range**        | オブジェクト | ボディ | 移動する元の範囲の定義 |
| **folder**       | 文字列   | クエリ | ワークブックが保存されているフォルダーパス |
| **storageName**  | 文字列   | クエリ | Aspose Cloud ストレージの名前 |

### リクエストボディ

| フィールド         | タイプ   | 必須 | 説明 |
|-------------------|----------|--------|-------------|
| **ColumnCount**   | 整数     | いいえ | 元の範囲の列数 |
| **ColumnWidth**   | 整数     | いいえ | 各列の幅（ポイント単位） |
| **FirstColumn**   | 整数     | いいえ | 元の範囲の最初の列の 0 から始まるインデックス |
| **FirstRow**      | 整数     | いいえ | 元の範囲の最初の行の 0 から始まるインデックス |
| **Name**          | 文字列   | いいえ | 範囲の名前（名前付き範囲の場合） |
| **RefersTo**      | 文字列   | いいえ | 範囲を定義する A1 形式の参照 |
| **RowCount**      | 整数     | いいえ | 元の範囲の行数 |
| **RowHeight**     | 整数     | いいえ | 各行の高さ（ポイント単位） |
| **Worksheet**     | 文字列   | いいえ | 元の範囲を含むワークシート |

### ワークフロー

1. （まだ存在しない場合は）ワークブックを Aspose Cloud ストレージに **アップロード** します。  
2. OAuth エンドポイントを使用して JWT トークンを **生成** します。  
3. 移動元の範囲を記述する JSON ペイロードを **構築** します。  
4. 必要なパスパラメータ、クエリパラメータ、および JSON ボディとともに `moveto` エンドポイントを **呼び出します**。  
5. 応答を **確認** します。成功した呼び出しでは `200 OK` ステータスが返されます。

### 例：リクエスト／応答

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

エラーが発生した場合、応答にはオプションで `ErrorMessage` フィールドが含まれ、失敗の詳細が提供されます。

**HTTP ステータスコード**

| コード | 意味                     | 説明                                      |
|--------|--------------------------|--------------------------------------------------|
| 200    | OK                       | フィルターが正常に適用されました；応答には操作の詳細が含まれます。 |
| 400    | Bad Request              | パラメータが不足または無効（例：サポートされていないファイル形式） |
| 401    | Unauthorized             | JWT トークンが無効または不足しています。 |
| 413    | Payload Too Large        | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error    | 予期しないサーバーエラーが発生しました。 |

**応答スキーマ**

| フィールド          | タイプ   | 説明 |
|--------------------|----------|-------------|
| **Code**           | 整数     | API が返す HTTP 的なステータスコード（例：200） |
| **Status**         | 文字列   | 結果のテキストによる説明（例："OK"） |
| **ErrorMessage**   | 文字列（オプション） | 呼び出しが失敗した場合の、人間が読めるエラーの詳細 |

## Cloud SDK ファミリー

SDK を使用することは、開発を高速化する最良の方法です。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}