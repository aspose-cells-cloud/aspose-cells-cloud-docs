---
title: "複数の Excelワークシートを削除する"
second_title: "Document"
linktitle: "複数のワークシート"
type: docs
url: /worksheets/delete-multiple/
aliases: [/delete-excel-worksheets/]
keywords: "Aspose.Cells Cloud, 複数のワークシートを削除, Excel API, REST API, v3.0, ワークシートの削除"
description: "Aspose.Cells Cloud REST API（v3.0）を使用して、Excelワークブックから複数のワークシートを削除する方法を学びます。HTTPSエンドポイントのセキュリティ、必要なパラメータ、修正済みcURLの例、および複数のプログラミング言語向けのSDKスニペットを含みます。"
weight: 20
ArticleTitle: "Aspose.Cells Cloud REST API を使用して複数の Excel ワークシートを削除する"
---

この REST API は、ワークブックから複数のワークシートを削除します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **リクエストパラメータ**

| パラメータ名      | 型     | 位置   | 説明                                                        |
| ----------------- | ------ | ------ | ------------------------------------------------------------- |
| name              | string | path   | Excel ファイルの名前。                                        |
| matchCondition    | object | body   | 削除するワークシートを指定する `MatchConditionRequest` オブジェクト。 |
| folder            | string | query  | ファイルが配置されているストレージ内のフォルダパス。          |
| storageName       | string | query  | ストレージサービスの名前。                                    |

**MatchConditionRequest プロパティ**

| 名前                | 型       | 説明                              | 備考     |
| ------------------- | -------- | ----------------------------------- | -------- |
| RegexPattern        | string   | ワークシート名に一致させる正規表現。 | オプション |
| FullMatchConditions | string[] | 削除する完全なワークシート名。      | オプション |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 相互作用を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API にリクエストを送信する方法を示しています。**`Authorization` ヘッダーには有効な JWT トークンが必要です。**

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

リクエストは、以下のような一般的なエラーレスポンスも返す場合があります：

| HTTP ステータス | 意味                           | サンプルペイロード                                         |
| --------------- | ------------------------------ | ---------------------------------------------------------- |
| 400             | 不正なリクエスト – 無効な JSON またはパラメータ | `{"Code":400,"Message":"Invalid request payload."}`      |
| 401             | 認証失敗 – JWT トークンが欠落または無効          | `{"Code":401,"Message":"Authentication failed."}`        |
| 403             | 権限不足                         | `{"Code":403,"Message":"Access denied."}`                |
| 404             | 見つかりません – ファイルまたはワークシートが存在しない | `{"Code":404,"Message":"Resource not found."}`           |
| 500             | サーバー内部エラー                 | `{"Code":500,"Message":"An unexpected error occurred."}` |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK ファミリー

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを送信する方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**関連項目:**  
- [単一のワークシートを削除する](https://docs.aspose.cloud/cells/worksheets/delete/)  
- [ワークシートをコピーする](https://docs.aspose.cloud/cells/worksheets/copy/)  
- [ワークシートを移動する](https://docs.aspose.cloud/cells/worksheets/move/)  
---