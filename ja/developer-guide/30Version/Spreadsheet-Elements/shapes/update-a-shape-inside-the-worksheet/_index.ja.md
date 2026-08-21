---
title: "Excelワークシート上の図形を更新する"
second_title: "ドキュメント"
linktitle: "更新"
type: docs
url: /shapes/update/
aliases: [/update-a-shape-inside-the-worksheet/]
keywords: "Excel API での図形の更新、Aspose.Cells Cloud、Excel 図形の更新、REST API、SDK、C#、Java、Python、Node.js、Go、Ruby、PHP、Perl、Swift"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシート内の図形を更新する方法を学びます。HTTPS エンドポイント、認証詳細、DTO スキーマ、使用手順、cURL の例、および複数言語向けの SDK コードサンプルを含みます。"
ArticleTitle: "Excelワークシート上の図形を更新する - Aspose.Cells Cloud API"
weight: 31
---

この REST API は、Excel ワークシート上の図形を更新します。

## セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### リクエストパラメータ

| パラメータ名  | 型      | 位置   | 説明                                                                                   |
| ------------- | ------- | ------ | --------------------------------------------------------------------------------------- |
| **name**      | 文字列  | パス   | ワークブックファイルの名前。                                                            |
| **sheetName** | 文字列  | パス   | 図形を含むワークシートの名前。                                                          |
| **shapeindex**| 整数    | パス   | ワークシート内の図形の 0 から始まるインデックス。                                       |
| **dto**       | オブジェクト | 本文 | 更新されたプロパティを含む図形のデータ転送オブジェクト（下記の _DTO スキーマ_ を参照）。 |
| **folder**    | 文字列  | クエリ | ワークブックが格納されているフォルダ。                                                  |
| **storageName**| 文字列 | クエリ | Aspose Cloud ストレージの名前。                                                         |

### DTO スキーマ

`dto` オブジェクトには更新可能なプロパティが含まれます。特に明記されていない限り、すべてのフィールドは任意です。

| フィールド           | 型      | 必須   | 説明                                                                                 |
| -------------------- | ------- | ------ | ------------------------------------------------------------------------------------- |
| **Name**             | 文字列  | いいえ | 図形の新しい名前。                                                                    |
| **UpperLeftRow**     | 整数    | いいえ | 図形の左上隅の行インデックス。                                                        |
| **UpperLeftColumn**  | 整数    | いいえ | 図形の左上隅の列インデックス。                                                        |
| **Width**            | 整数    | いいえ | 図形の幅（ポイント単位）。                                                            |
| **Height**           | 整数    | いいえ | 図形の高さ（ポイント単位）。                                                          |
| **RotationAngle**    | 整数    | いいえ | 回転角度（度単位）。                                                                  |
| **IsHidden**         | 真偽値  | いいえ | 図形を非表示にする場合は `true`。                                                     |
| **IsLocked**         | 真偽値  | いいえ | 図形をロックする場合は `true`。                                                       |
| **Font**             | オブジェクト | いいえ | フォント設定（サブプロパティについては OpenAPI 仕様を参照）。                         |
| **...**              | …       | いいえ | `HtmlText`、`AlternativeText`、`ZOrderPosition` などのその他のプロパティ。            |

> 完全なリストについては、公式 OpenAPI 仕様を参照してください：<https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>。

### リクエストヘッダー

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>` _（_認証_ステップで取得した JWT トークン）_

### リクエスト本文（例）

```json
{
  "Name": "MyShape",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## cURL を使用した例（コマンドラインツール）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "UpdatedShape",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### レスポンス

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**エラー処理** – API は以下のステータスコードを返す可能性があります：

| コード | 意味                 | 典型的な原因                                         |
| ------ | -------------------- | ---------------------------------------------------- |
| 400    | 不正リクエスト       | 無効な JSON、または必須フィールドが不足しています。  |
| 401    | 認証されていません   | JWT トークンが不足している、または無効です。         |
| 404    | 見つかりません       | ワークブック、ワークシート、または図形インデックスが存在しません。 |
| 500    | サーバーエラー       | サーバー側で予期しない問題が発生しました。           |

**エラー応答の例**

*400 – 不正リクエスト*

```json
{
  "Code": 400,
  "Message": "Invalid request payload. 'Name' field exceeds maximum length."
}
```

*401 – 認証されていません*

```json
{
  "Code": 401,
  "Message": "Authentication failed. Invalid or expired JWT token."
}
```

*404 – 見つかりません*

```json
{
  "Code": 404,
  "Message": "The specified workbook, worksheet, or shape index was not found."
}
```

*500 – サーバーエラー*

```json
{
  "Code": 500,
  "Message": "An unexpected error occurred on the server."
}
```

## Cloud SDK ファミリー

SDK を使用すると、開発を迅速化できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}