---
title: "Excelチャートのエクスポート – Aspose.Cells Cloud API"
second_title: "ドキュメント"
description: "クラウド上に保存されたExcelワークブック内のチャートを、単一のREST呼び出しでPDF、PNG、SVGなどの形式に変換します。"
ArticleTitle: "ローカルのスプレッドシートワークシートをPDFファイルに変換する方法：ステップ・バイ・ステップ・ガイド"
linktype: "ワークシートをPDFに変換"
type: docs
url: /export-chart-as-format/ja/
keywords: "Aspose.Cells Cloud, チャートエクスポート, API, PDF, PNG, SVG, Excel, REST, クラウド変換"
weight: 100
---

Aspose Cloudストレージに保存されたワークブック内のチャートを、ソースファイルをダウンロードせずに別のファイル形式（PDF、PNG、SVGなど）にエクスポートします。

## ExportChartAsFormat API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### 📦 リクエストパラメータ

| 名前               | 型      | 位置   | 必須 | 説明                                                        |
| ------------------ | ------- | ------ | ---- | ------------------------------------------------------------ |
| **name**           | 文字列  | パス   | はい  | ワークブックのファイル名。                                   |
| **worksheet**      | 文字列  | パス   | はい  | チャートを含むワークシート名。                               |
| **chartIndex**     | 整数    | パス   | はい  | エクスポートするチャートの0から始まるインデックス。           |
| **format**         | 文字列  | クエリ | はい  | 出力形式（例: `png`, `pdf`, `svg`）。                        |
| **folder**         | 文字列  | クエリ | いいえ | ワークブックが保存されているフォルダのパス（デフォルト: ルート）。 |
| **storageName**    | 文字列  | クエリ | いいえ | カスタムストレージ名；省略するとデフォルトストレージを使用します。 |
| **outPath**        | 文字列  | クエリ | いいえ | 変換されたファイルを保存するフォルダのパス。                 |
| **outStorageName** | 文字列  | クエリ | いいえ | 出力ファイル用のストレージ名。                               |
| **fontsLocation**  | 文字列  | クエリ | いいえ | カスタムフォントが格納されたフォルダのパス。                 |
| **region**         | 文字列  | クエリ | いいえ | ロケール設定（例: `en-US`, `fr-FR`）。                       |
| **password**       | 文字列  | クエリ | いいえ | 保護されたワークブックを開くためのパスワード。               |

### **レスポンス**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**HTTPステータスコード**

| コード | 意味           | 説明                                                  |
| ------ | -------------- | ----------------------------------------------------- |
| 200    | OK             | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | 不正リクエスト | パラメータが不足しているか無効です（例：サポートされていないファイル形式）。 |
| 401    | 認証不可       | JWTトークンが無効または不足しています。               |
| 413    | ペイロードが大きすぎます | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | サーバーエラー | 予期しないサーバーエラーが発生しました。               |

## Export Chart as Format API を SDK とともに使用する方法

### Export Chart as Format API の仕様

[Export Chart as Format API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat) は、パブリックに利用可能なプログラミングインターフェースを提供し、Webブラウザから直接RESTリクエストを実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例では、cURL を使ってクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64エンコード)",
  "contentType": "MIMEタイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細が抽象化されるため、開発が最も迅速に行えます。最小限のコードでスプレッドシートのデータをPDFファイルに変換できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。