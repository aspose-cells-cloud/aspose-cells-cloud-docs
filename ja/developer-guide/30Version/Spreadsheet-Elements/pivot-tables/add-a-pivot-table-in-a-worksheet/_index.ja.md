---
title: "Excelワークシートにピボットテーブルを追加する"
second_title: "Document"
linktitle: Add
type: docs
url: /ja/pivot-tables/add/
aliases: [  /ja/add-a-pivot-table-in-a-worksheet/ ]
keywords: "ピボットテーブルの追加、Excelワークシート、Aspose.Cells Cloud、REST API、SDK、Excelピボットテーブル"
description: "Aspose.Cells Cloud REST APIを使用してExcelワークシートにピボットテーブルを追加します。C#、Java、PHP、Python、Node.js、Android、Swift、Perl、Go用のSDKで利用可能です。"
weight: 30
ArticleTitle: "Aspose.Cells Cloudを使用してExcelワークシートにピボットテーブルを追加する方法"
---

このREST APIは、ワークシートにピボットテーブルを追加します。

**前提条件:**  
- 有効なJWTアクセストークンを備えたAspose.Cells Cloudアカウント。  
- 対象のワークブックは、サポートされているストレージ場所（デフォルトストレージまたはユーザー指定のストレージ）に保存されていること。  
- `sheetName`で指定されたワークシートがワークブック内に存在すること。  

## PutWorksheetPivotTable API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を要求します。

### **リクエストパラメータ**

| パラメータ名 | 型      | 位置     | 説明                                                                                                                       |
| ------------ | ------- | -------- | -------------------------------------------------------------------------------------------------------------------------- |
| name         | string  | path     | Excelドキュメントの名前。                                                                                                  |
| sheetName    | string  | path     | ピボットテーブルを作成するワークシートの名前。                                                                             |
| request      | object  | body     | ピボットテーブル定義を含む`CreatePivotTableRequest` DTO。                                                                  |
| folder       | string  | query    | ドキュメントを含むフォルダ。                                                                                               |
| storageName  | string  | query    | ドキュメントが配置されているストレージの名前。                                                                             |
| sourceData   | string  | query    | 新しいピボットテーブルキャッシュのソースデータを提供する範囲（例: `A5:E10`）。                                             |
| destCellName | string  | query    | ピボットテーブルレポートの宛先範囲の左上セルのアドレス。                                                                   |
| tableName    | string  | query    | 新しいピボットテーブルに割り当てる名前。                                                                                   |
| useSameSource| boolean | query    | `true`の場合、新しいピボットテーブルは既存のデータソースを再利用し、他のピボットテーブルが既にこのソースを使用している場合にメモリを節約します。 |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接REST通信を実行できるようにします。

**cURL**コマンドラインツールを使用すると、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLを使用してクラウドAPIを呼び出す方法を示しています。

**セキュリティ注意事項:** APIを呼び出す際は常に`https://`を使用し、JWTトークンを機密に保つこと。平文HTTP経由でトークンを送信すると、トークンが傍受されるリスクがあります。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
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

**HTTPステータスコード**

| コード | 意味                       | 説明                                                       |
|------|---------------------------|------------------------------------------------------------|
| 200  | OK                        | フィルターが正常に適用されました。応答には操作の詳細が含まれます。 |
| 400  | Bad Request               | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized              | JWTトークンが無効または不足しています。                      |
| 413  | Payload Too Large         | アップロードされたファイルがサイズ制限を超えています。         |
| 500  | Internal Server Error     | 予期しないサーバーエラーが発生しました。                      |

## Cloud SDK Family

SDKを使用することが開発を高速化する最良の方法です。SDKは低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

その他の操作については、以下の関連APIページをご参照ください：**[ピボットテーブルの取得](https://docs.aspose.cloud/cells/pivot-tables/get/)**、**[ピボットテーブルの削除](https://docs.aspose.cloud/cells/pivot-tables/delete/)**、**[ピボットテーブルの更新](https://docs.aspose.cloud/cells/pivot-tables/update/)**。