---
title: "Excelの範囲を画像に変換 – Aspose.Cells Cloud API"
description: "ローカルのExcelファイルから特定の範囲をPNG、JPEG、SVG、TIFF、BMP形式に変換します。Aspose.Cells Cloud REST APIを使用し、ワークブック全体をアップロードする必要はありません。"
keywords: "Aspose.Cells Cloud、範囲を画像に変換、Excel API、画像形式、PNG、JPEG、SVG、TIFF、BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

このAPIはローカルのスプレッドシートファイルを読み取り、指定された範囲を変換し、画像をバイナリストリームとして返します。

## 範囲を画像に変換するメソッド

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **セキュリティと認証**

Aspose.Cells Cloud APIはセキュアであり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を必要とします。

## リクエストパラメータ

| 名前               | 位置                              | 型      | 必須   | 説明                                                                   |
| ------------------ | --------------------------------- | ------- | ------ | ---------------------------------------------------------------------- |
| **Spreadsheet**    | Form‑Data (`multipart/form-data`) | ファイル | **はい**  | 処理対象のExcelファイル。                                              |
| **worksheet**      | クエリ                            | 文字列  | **はい**  | 範囲を含むワークシート名（例: `Sheet1`）。                             |
| **range**          | クエリ                            | 文字列  | **はい**  | 変換するセル範囲（例: `A1:C10`）。                                     |
| **format**         | クエリ                            | 文字列  | **はい**  | 出力画像形式（`png`、`jpeg`、`svg`、`tiff`、`bmp`）。                   |
| **printHeadings**  | クエリ                            | 真偽値  | いいえ  | 画像に行/列の見出しを含める場合は `true`。                             |
| **outPath**        | クエリ                            | 文字列  | いいえ  | クラウドストレージに生成されたファイルを保存する場合のフォルダパス。   |
| **outStorageName** | クエリ                            | 文字列  | いいえ  | ストレージサービスの名前（例: `MyStorage`）。                          |
| **fontsLocation**  | クエリ                            | 文字列  | いいえ  | 変換中に使用されるカスタムフォントのURLまたはパス。                    |
| **region**         | クエリ                            | 文字列  | いいえ  | ロケール識別子（例: `en-US`、`fr-FR`）。数値および日付の書式に影響します。 |
| **password**       | クエリ                            | 文字列  | いいえ  | 暗号化されたワークブックのパスワード。                                |
| **AutoRowsFit**    | クエリ                            | 真偽値  | いいえ  | レンダリング前に行を自動調整します。                                   |
| **AutoColumnsFit** | クエリ                            | 真偽値  | いいえ  | レンダリング前に列を自動調整します。                                   |

## レスポンス

APIは変換された画像ファイルを**バイナリストリーム**（`application/octet-stream`）として返します。

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### サンプル成功レスポンス（HTTP）

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

レスポンスボディをファイル（例: `report.png`）として保存し、ブラウザでレンダリングされた画像を表示してください。

---

**HTTPステータスコード**

| コード | 意味                  | 説明                                                               |
| ------ | --------------------- | ------------------------------------------------------------------ |
| 200    | OK                    | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。   |
| 400    | Bad Request           | パラメータが不足または無効（例: 未対応のファイル形式）。           |
| 401    | Unauthorized          | JWTトークンが無効または不足しています。                            |
| 413    | Payload Too Large     | アップロードされたファイルがサイズ制限を超えています。             |
| 500    | Internal Server Error | 想定外のサーバーエラーが発生しました。                             |

## SDKを使用して範囲を画像に変換するAPIを利用するには？

### OpenAPI仕様

[OpenAPI仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage)は、パブリックにアクセス可能なAPIを定義しており、Webブラウザから直接REST APIを操作できます。

cURLコマンドラインツールを使用すると、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例では、cURLを使用してCloud APIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## Aspose.Cells Cloud SDKを使用する

SDKを使用すると、低レベルの詳細を抽象化できるため、開発が最速で行えます。最小限のコードでデータ範囲を画像ファイルに変換できます。  
Aspose.Cells Cloud SDKの完全なリストは、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)でご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています。Gistからの読み込みがブロックされる場合は、リポジトリから直接例をダウンロードできます。

---