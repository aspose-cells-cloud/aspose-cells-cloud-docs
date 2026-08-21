---
title: "Excelワークシートへの画像のインポート"
ArticleTitle: "Excelワークシートへの画像のインポート – Aspose.Cells Cloud APIガイド"
second_title: "ドキュメント"
linktitle: "画像のインポート"
type: docs
url: /import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "画像のインポート, Excel, Aspose.Cells Cloud, REST API, v3.0"
description: "Aspose.Cells Cloud REST API v3.0 を使用して、Excelワークシートに画像をインポートする方法を学びます。マルチパートリクエストの例、SDKコードサンプル、エラーハンドリングのガイドを含みます。明確な手順ですぐに始められます。"
weight: 19
---

Excelワークシートへの画像のインポートにより、ロゴ、チャート、図表などの視覚的コンテンツをスプレッドシートに追加できます。本ガイドでは、Aspose.Cells Cloudの**ImportPicture**操作、必要なリクエスト形式、およびレスポンスの処理方法を説明します。

**前提条件:** インポート操作を実行する前に、有効なJWT認証トークンと、Aspose Cloudストレージ内に保存されている既存のワークブックが必要です。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を要求します。

### **リクエストパラメータ**

リクエストは、HTTPの**POST**で、**multipart/related**形式のコンテンツです（[RFC 2046](https://tools.ietf.org/html/rfc2046#page-17)または[RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)を参照）。

- **最初のパート**には、画像の配置場所と方法を示す**ImportPictureOption**という名前のJSONオブジェクトが含まれます。
- **2番目のパート**には、画像ファイル（またはBase64エンコードされたデータ）が含まれます。

### ImportPictureOption – 定義

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert` は **boolean** 値です。`true` は新しい画像を挿入、`false` は既存の画像を置換します。_

### 重要なパラメータ

**ImportPictureOption**

| パラメータ名         | 型          | 説明                                                                                                                                                 |
|---------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| UpperLeftRow        | int         | 画像を配置する左上隅の行インデックス                                                                                                                  |
| UpperLeftColumn     | int         | 画像を配置する左上隅の列インデックス                                                                                                                  |
| LowerRightRow       | int         | 画像の範囲を定義する右下隅の行インデックス                                                                                                            |
| LowerRightColumn    | int         | 画像の範囲を定義する右下隅の列インデックス                                                                                                            |
| Filename            | string      | 画像ファイルの名前                                                                                                                                    |
| Data                | string      | 画像のBase64エンコードされたバイナリデータ（2番目のパートとしてファイルを送信する場合は省略可能）                                                      |
| DestinationWorksheet| string      | 画像を挿入するワークシートの名前                                                                                                                      |
| **IsInsert**        | **boolean** | `true` の場合は新しい画像を挿入、`false` の場合は既存の画像を置換します。                                                                             |
| ImportDataType      | string      | インポートするデータの種類（例: `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`） |
| Source              | FileSource  | `BatchData` パラメータが null の場合、データファイルの保存場所を示します。                                                                            |

### レスポンス

成功したリクエストは、以下のようなJSONペイロードを含む **HTTP 200** を返します。

```json
{
  "Code": 200,
  "Status": "OK"
}
```

可能なステータスコード:

| コード | 意味                           |
|------|-------------------------------|
| 200  | インポート成功                  |
| 400  | 不正なリクエスト — データ不足または無効 |
| 401  | 認証エラー — 無効または不足しているトークン |
| 500  | サーバー内部エラー               |

## SDK を使用した PostImportData API の利用方法

### PostImportData API の仕様

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)はパブリックに利用可能なプログラミングインターフェースを定義し、Webブラウザから直接REST APIとのやり取りを実行可能にします。

### Aspose.Cells Cloud SDK の利用

SDK を利用することで、開発を効率的に進められます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
---