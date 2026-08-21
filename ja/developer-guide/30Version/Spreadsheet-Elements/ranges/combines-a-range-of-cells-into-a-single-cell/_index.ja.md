---
title: "Aspose.Cells Cloud API – セル範囲の結合"
second_title: "ドキュメント"
linktitle: "結合"
type: docs
url: /ja/ranges/merge/
aliases: [  /ja/combines-a-range-of-cells-into-a-single-cell/ ]
keywords: "Aspose.Cells, セル結合, Excel API, REST, クラウドSDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシート上のセル範囲を 1 つのセルに結合します。C#、Java、Python などのリクエスト形式、パラメータ、SDK サンプルについて学びます。"
weight: 20
---

この REST API は、Excel ワークシート上のセル範囲を 1 つのセルに結合します。

**概要** – 範囲の結合は、選択したセルを 1 つのセルにまとめ、左上セルの値を保持し、他のセルの値を破棄します。複数の列や行にまたがるヘッダーを作成する場合や、ワークシートのレイアウトを簡略化したい場合にこの操作を使用します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **リクエストパラメータ**

| パラメータ名    | 型     | 位置   | 説明                                  |
| --------------- | ------ | ------ | ------------------------------------- |
| **name**        | 文字列 | パス   | ワークブック名。                      |
| **sheetName**   | 文字列 | パス   | ワークシート名。                      |
| **range**       | オブジェクト | 本文 | 結合するセルを指定する範囲オブジェクト。 |
| **folder**      | 文字列 | クエリ | ワークブックが保存されているフォルダ。 |
| **storageName** | 文字列 | クエリ | ストレージ名。                        |

#### リクエストボディのスキーマ

**Range** オブジェクトには、以下のフィールドを含める必要があります（その他のフィールドは任意です）：

| プロパティ名    | 型      | 必須 | 説明                                      |
| --------------- | ------- | ---- | ----------------------------------------- |
| **FirstRow**    | 整数    | はい | 範囲内の最初の行の 0 から始まるインデックス。 |
| **FirstColumn** | 整数    | はい | 範囲内の最初の列の 0 から始まるインデックス。 |
| **RowCount**    | 整数    | はい | 範囲に含める行数。                        |
| **ColumnCount** | 整数    | はい | 範囲に含める列数。                        |
| **Name**        | 文字列  | いいえ | 範囲の任意の名前。                        |
| **RefersTo**    | 文字列  | いいえ | 範囲が参照する数式。                      |
| **Worksheet**   | 文字列  | いいえ | ワークシート名（パスパラメータと異なる場合）。 |
| **RowHeight**   | 数値    | いいえ | 範囲内の行の高さ（ピクセル単位）。        |
| **ColumnWidth** | 数値    | いいえ | 範囲内の列の幅（ピクセル単位）。          |

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
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

#### レスポンス詳細

| HTTP ステータス               | 説明                                          | サンプル JSON                                          |
| ----------------------------- | --------------------------------------------- | ------------------------------------------------------ |
| **200 OK**                    | 範囲が正常に結合されました。                  | `{ "Code": 200, "Status": "OK" }`                      |
| **400 Bad Request**           | 無効な範囲パラメータ（例：インデックスが範囲外）。 | `{ "Code": 400, "Message": "Invalid range." }`         |
| **401 Unauthorized**          | JWT トークンが不足しているか、無効です。      | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404 Not Found**             | ワークブックまたはワークシートが見つかりません。 | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500 Internal Server Error** | 予期しないサーバーエラー。                    | `{ "Code": 500, "Message": "Internal server error." }` |

## クラウド SDK ファミリー

SDK を使用すると、開発を迅速に進めることができます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}