---
title: "リスト オブジェクトを範囲に変換する – Aspose.Cells Cloud API"
ArticleTitle: "Aspose.Cells Cloud API を使用してリスト オブジェクトを範囲に変換する"
second_title: "ドキュメント"
linktitle: "変換"
type: docs
url: /ja/list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "Aspose Cells API, リスト オブジェクトを範囲に変換, Excel REST API"
description: "Aspose.Cells Cloud REST API を使用して Excel の ListObject（テーブル）を範囲に変換する方法を学習します。リクエスト構文、パラメーター、サンプル cURL、レスポンス スキーマ、認証の詳細、エラー コード、SDK の使用例を含みます。"
weight: 30
---

この REST API は、Excelワークシート内の**リスト オブジェクト（テーブル）**を**範囲**に変換します。

**前提条件:**  
エンドポイントを呼び出す前に、ワークブックが Aspose Cloud ストレージにアップロードされていること、ワークシートに変換対象のリスト オブジェクトが存在すること、およびサポートされているファイル形式（例: .xlsx、.xlsm）を使用していることを確認してください。

## REST API

**認証**  
この操作を呼び出すには、`Authorization` ヘッダーに有効な JWT トークンを含める必要があります。トークンは、クライアント ID とクライアント シークレットを使用して OAuth 2.0 トークン エンドポイントに POST リクエストを送信することで取得します。トークンには `Cells.ReadWrite` スコープが含まれており、トークン サービスが返す期間有効です。

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエスト パラメーター

| 名前                | 型      | 位置   | 必須 | デフォルト | 説明                                                  |
| ------------------- | ------- | ------ | ---- | --------- | ----------------------------------------------------- |
| **name**            | 文字列  | パス   | はい  | –         | Excel ファイルの名前。                               |
| **sheetName**       | 文字列  | パス   | はい  | –         | リスト オブジェクトを含むワークシートの名前。        |
| **listObjectIndex** | 整数    | パス   | はい  | –         | 変換するリスト オブジェクト（テーブル）の 0 から始まるインデックス。 |
| **folder**          | 文字列  | クエリ | いいえ | –         | ファイルが保存されているフォルダーのパス。           |
| **storageName**     | 文字列  | クエリ | いいえ | –         | ストレージ サービスの名前。                          |

> **注意:** この操作は、**.xlsx** や **.xlsm** などの最新の Excel 形式でのみ動作します。リスト オブジェクトは保護されていない必要があります。リスト オブジェクトの詳細については、[リスト オブジェクトの概要](/list-objects/) を参照してください。範囲の操作方法の詳細については、[範囲のドキュメント](/ranges/) を参照してください。

### cURL の例（リクエスト）

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

#### レスポンス スキーマ

API は、新しく作成された範囲の詳細を含む **200 OK** レスポンスを返します。

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| フィールド         | 型      | 説明                                           |
| ----------------- | ------- | ---------------------------------------------- |
| **Code**          | 整数    | HTTP に類似したステータス コード（200 は成功を示します）。 |
| **Status**        | 文字列  | ステータスのテキスト メッセージ。               |
| **RangeName**     | 文字列  | 作成された範囲に割り当てられた名前。            |
| **Address**       | 文字列  | シート名を含む範囲の完全なアドレス。            |
| **FirstRow**      | 整数    | 範囲内の最初の行の 0 から始まるインデックス。    |
| **FirstColumn**   | 整数    | 範囲内の最初の列の 0 から始まるインデックス。    |
| **RowCount**      | 整数    | 範囲内の行数。                                 |
| **ColumnCount**   | 整数    | 範囲内の列数。                                 |

**HTTP ステータス コード**

| コード | 意味                   | 説明                                             |
|------|------------------------|-------------------------------------------------|
| 200  | OK                     | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request            | パラメーターが不足または無効です（例: サポートされていないファイル形式）。 |
| 401  | Unauthorized           | 無効または不足している JWT トークン。             |
| 413  | Payload Too Large      | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error  | 予期しないサーバーエラー。                        |

**エラー レスポンス スキーマ（例）:**

```json
{
  "Code": 400,
  "Message": "Invalid listObjectIndex. Index must be between 0 and 5."
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK を使用すると、開発を最速で進めることができます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}
---