---
title: "Excelワークシート内のOLEオブジェクトを更新する"
second_title: "Document"
linktitle: "Update"
type: docs
url: /oleobjects/update/
aliases: [/update-a-specific-oleobject-from-excel-worksheet/]
keywords: "OLEオブジェクトの更新、Excel、Aspose.Cells Cloud、REST API、SDK"
description: "Aspose.Cells Cloud REST API を使って Excel ワークシート内の OLE オブジェクト（画像、チャートなど）を更新する方法を学びます。cURL や SDK の例、認証手順、エラー処理も含まれます。"
weight: 30
author: "Aspose Cloud Documentation Team"
lastmod: "2024-03-01"
ArticleTitle: "Excelワークシート内のOLEオブジェクトを更新する – Aspose.Cells Cloud API ガイド"
---

この REST API は、Excel ワークシート内の **OLE オブジェクト** を更新します。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が要求されます。

## PostUpdateWorksheetOleObject API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

リクエストパラメータは以下の通りです：

| パラメータ名        | 型     | パラメータ位置 | 説明                                      |
| ------------------- | ------ | -------------- | ----------------------------------------- |
| name                | string | path           | ワークブック名。                          |
| sheetName           | string | path           | ワークシート名。                          |
| oleObjectIndex      | integer| path           | ワークシート内の OLE オブジェクトのインデックス。|
| ole                 | object | body           | 更新対象の OLE オブジェクトの JSON 表現。 |
| folder              | string | query          | ワークブックを含むフォルダ。              |
| storageName         | string | query          | ストレージサービスの名前。                |

### リクエストボディのフィールド

| フィールド              | 型      | 必須   | 説明                                               |
| ----------------------- | ------- | ------ | -------------------------------------------------- |
| ImageSourceFullName     | string  | オプション | OLE オブジェクトに使用される画像ファイルのパス。   |
| IsAutoSize              | boolean | オプション | OLE オブジェクトを自動サイズ調整するかどうか。     |
| SourceFullName          | string  | 必須   | OLE オブジェクトのソースファイル（画像やチャートなど）。|
| UpperLeftRow            | integer | 必須   | 左上隅の行インデックス（0 から始まる）。           |
| UpperLeftColumn         | integer | 必須   | 左上隅の列インデックス（0 から始まる）。           |
| Left                    | integer | オプション | 左上隅からの水平オフセット（単位：ポイント）。     |
| Top                     | integer | オプション | 左上隅からの垂直オフセット（単位：ポイント）。     |
| Width                   | integer | 必須   | OLE オブジェクトの幅（単位：ポイント）。           |
| Height                  | integer | 必須   | OLE オブジェクトの高さ（単位：ポイント）。         |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 操作を実行できるようにします。

**cURL** コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## エラーレスポンス

| HTTP ステータス | コード | メッセージ                                           |
| --------------- | ---- | ---------------------------------------------------- |
| 400             | 4000 | 不正リクエスト – パラメータが不足または無効です。     |
| 401             | 4010 | 認証エラー – JWT トークンが無効または不足しています。 |
| 404             | 4040 | 見つかりません – ワークブック、ワークシート、または OLE オブジェクトが存在しません。 |
| 500             | 5000 | サーバー内部エラー – サーバー側で予期しないエラーが発生しました。 |

API はレスポンスボディ内にカスタムの **Code** フィールドも返し、HTTP ステータスコードに対応します（例：200 → 2000、400 → 4000 など）。

## 何时この API を使用すべきか？

このエンドポイントは、ワークシート全体を再アップロードせずに、既存の OLE オブジェクト（埋め込み画像、チャート、ドキュメントなど）を変更する必要がある場合に使用します。典型的なユースケースには、画像ソースの更新、オブジェクトのサイズ変更、ワークブック生成後の位置変更が含まれます。関連する操作については、[OLE オブジェクトを追加する](/oleobjects/add/)および[OLE オブジェクトを削除する](/oleobjects/delete/)を参照してください。

## Cloud SDK ファミリー

SDK を使用すると、開発を最も迅速に進めることができます。SDK は低レベルの詳細を抽象化し、プロジェクトの本質的な作業に集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下は、Aspose.Cells Cloud SDK を使って OLE オブジェクトを更新する C# の短い例です：

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<your-app-sid>",
    AppKey = "<your-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"Status: {response.Status}");
```

以下のコード例は、さまざまな SDK を使って Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}