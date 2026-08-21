---
title: "Excelから文字を削除する – Aspose.Cells Cloud API（POST /cells/removecharacters）"
second_title: "ドキュメント"
linktitle: "文字の削除"
type: docs
url: /excel-remove-characters/
keywords: "文字削除, Aspose.Cells, Excel API, テキスト処理, クラウド"
description: "Aspose.Cells Cloud APIを使用してExcelワークシートから文字、文字セット、または部分文字列を削除する方法を学びます。リクエストスキーマ、cURLの例、SDKコード、エラーハンドリングを含みます。"
weight: 100
ArticleTitle: "Excelから文字を削除する – Aspose.Cells Cloud API（POST /cells/removecharacters）"
---

## Excel Web APIから文字を削除する

選択したセル内のテキストコンテンツをクリーニングするための包括的なツールセットです。このAPIは、特定の文字、事前定義された文字セット、または部分文字列を削除し、ワークシートのテキストを標準化し、不要な記号を排除します。

**前提条件**

- アクティブなAspose Cloudアカウント。  
- 認証ガイドに記載されている方法で取得した有効なJWTアクセストークン。  
- このエンドポイントを呼び出す前に、Excelファイルをストレージにアップロードしておく必要があります。  
- サポートされているファイル形式は `.xlsx`、 `.xls`、 `.xlsm`、およびその他の一般的なExcel形式です。

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### 機能の説明

- **カスタム文字の削除** – 削除したい任意の文字を指定します。_カスタム文字の削除_フィールドに各文字を入力すると、APIは選択されたセル内のその文字の出現回数をすべて削除します。  
- **文字セットの削除** – 事前定義されたセットから選択します：  
  - **非表示文字** – 改行と最初の32個の非表示ASCII文字（0～31）、および追加のコード（127、129、141、143、144、157）を削除します。  
  - **文字文字** – すべての文字を削除します。  
  - **数値文字** – すべての数字を削除します。  
  - **記号** – 数学的、幾何学的、技術的、通貨記号、および“?”、“1”、“™”などの字形に似た記号を削除します。  
  - **句読点記号** – すべての句読点を削除します。  
- **部分文字列の削除** – 選択されたセルから指定された部分文字列（例：単語）を削除します。

### リクエストパラメータ

| パラメータ名            | 型    | 位置   | 説明                                                                 |
| ----------------------- | ----- | ------ | -------------------------------------------------------------------- |
| removeCharactersOptions | クラス | 本文   | 削除する文字、文字セット、または部分文字列を定義するオプション。     |

**`removeCharactersOptions`のスキーマ**

| プロパティ         | 型      | 必須 | 説明                                                                                     |
| ------------------ | ------- | ---- | ---------------------------------------------------------------------------------------- |
| Range（範囲）      | 文字列  | はい | 処理するセルを識別するA1表記または名前付き範囲（例：`"A1:C10"`）。                      |
| CustomCharacters（カスタム文字） | 文字列 | いいえ | 削除する各カスタム文字を含む文字列（例：`"@#$"`）。                                      |
| CharacterSet（文字セット） | 文字列 | いいえ | 事前定義されたセットを指定する列挙値（`"NonPrinting"`、`"Text"`、`"Numeric"`、`"Symbols"`、`"Punctuation"`）。 |
| Substring（部分文字列） | 文字列 | いいえ | 削除する正確な部分文字列（例：`"USD"`）。                                                |
| IgnoreCase（大文字小文字を区別しない） | 真偽値 | いいえ | `true`の場合、文字削除は大文字小文字を区別しません。                                     |

**JSONリクエストボディの例**

```json
{
  "Range": "A1:B20",
  "CustomCharacters": "@#$",
  "CharacterSet": "NonPrinting",
  "Substring": "USD",
  "IgnoreCase": true
}
```

**cURLリクエストの例**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "Range": "A1:B20",
           "CustomCharacters": "@#$",
           "CharacterSet": "NonPrinting",
           "Substring": "USD",
           "IgnoreCase": true
         }'
```

### **レスポンス**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[merged filename]",
    "Filesize" : [file size],
    "FileContent" : "[Base64String]"
}
```

**HTTPステータスコード**

| コード | 意味                   | 説明                                                   |
| ------ | ---------------------- | ------------------------------------------------------ |
| 200    | OK                     | フィルターが正常に適用されました；レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request（不正なリクエスト） | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized（認証されていません） | JWTトークンが無効または不足しています。                    |
| 413    | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルがサイズ制限を超えています。     |
| 500    | Internal Server Error（内部サーバーエラー） | 予期しないサーバーエラーが発生しました。                  |

## SDKを使用してPostRemoveCharacters APIを利用する方法

### PostRemoveCharacters API仕様

<a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters" rel="noopener noreferrer">PostRemoveCharactersエンドポイントの完全なOpenAPI仕様</a>は、公開可能なプログラミングインターフェースを定義し、Webブラウザから直接RESTインタラクションを実行できるようにします。

### Aspose.Cells Cloud SDKの使用

SDKを使用することは、開発を高速化する最良の方法です。SDKは低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHubリポジトリ</a>をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています：
---