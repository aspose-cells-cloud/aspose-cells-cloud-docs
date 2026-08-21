---
title: "Excelワークシートから行を削除する"
second_title: "Document"
linktitle: "Row"
type: docs
url: /ja/rows/delete/row/
aliases: [  /ja/delete-row-from-a-worksheet/ ]
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシートから特定の行を削除するには、DELETE /worksheets/{sheetName}/cells/rows/{rowIndex} エンドポイントを使用します。cURL コマンド、SDK サンプル、および完全なパラメーターリファレンスを含みます。"
keywords: "Aspose.Cells, 行の削除, Excel, API, REST, Cloud, SDK"
weight: 80
ArticleTitle: "Excelワークシートから行を削除する – Aspose.Cells Cloud API ガイド"
---

この REST API は、Excelワークシートから1行を削除します。

**前提条件**  
- 有効な JWT **Authorization** トークン。  
- ワークブックは、サポートされている Aspose Cloud ストレージ（デフォルトまたはカスタム）に保存されていること。  
- 対象フォルダ（指定されている場合）が、選択されたストレージ内に存在すること。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **リクエストパラメーター**

| パラメーター名      | 型      | パス / クエリ | 必須 | 説明                                                                                       |
| ------------------- | ------- | ------------- | ---- | ------------------------------------------------------------------------------------------- |
| **name**            | 文字列  | path          | はい  | ワークブック名。                                                                            |
| **sheetName**       | 文字列  | path          | はい  | ワークシート名。                                                                            |
| **rowIndex**        | 整数    | path          | はい  | 削除する行の 0 から始まるインデックス。                                                     |
| **startrow**        | 整数    | query         | いいえ | 削除する最初の行のインデックス（通常は `rowIndex` と同じ）。                                 |
| **totalRows**       | 整数    | query         | いいえ | 削除する連続する行数。                                                                      |
| **updateReference** | 真偽値  | query         | いいえ | `true`（デフォルト）の場合、削除後に数式、名前付き範囲、その他の参照が更新されます。         |
| **folder**          | 文字列  | query         | いいえ | ワークブックを含むフォルダ。                                                                |
| **storageName**     | 文字列  | query         | いいえ | ストレージサービスの名前。                                                                  |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接REST通信を実行できるようにします。

cURLコマンドラインツールを使用すると、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例は、完全で実行可能な呼び出しを示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

**可能なHTTPレスポンスコード**

| コード | 意味                                 | 説明                                                                           |
|------|--------------------------------------|--------------------------------------------------------------------------------|
| 200  | OK                                   | 行が正常に削除されました。                                                     |
| 400  | Bad Request                          | パラメーターが不足している、または無効です（例：`rowIndex` が数値でない）。   |
| 401  | Unauthorized                         | JWT トークンが無効または不足しています。                                       |
| 404  | Not Found                            | 指定されたワークブック、ワークシート、または行が存在しません。                |
| 500  | Internal Server Error                | サーバーで予期しないエラーが発生しました。詳細はエラーレスポンスを参照してください。 |

**エラーレスポンスの例**

```json
{
  "Code": 400,
  "Message": "Invalid row index supplied."
}
```

## Cloud SDK ファミリー

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を抽象化するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

**関連する操作**  
- [行を追加する](/cells/rows/add/row/)  
- [複数の行を削除する](/cells/rows/delete/rows/)  
- [行の詳細を取得する](/cells/rows/get/row/)  
---