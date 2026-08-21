---
title: "ワークシートのエクスポート – Aspose.Cells Cloud API v4（PDF、PNG、SVG、CSV）"
second_title: "ドキュメント"
ArticleTitle: "リモートスプレッドシートのワークシートを別の形式にエクスポートする方法：ステップ・バイ・ステップ・ガイド"
linktitle: "ワークシートのエクスポート"
type: docs
url: /export-worksheet-as-format/
keywords: "Aspose Cells, ワークシートのエクスポート, クラウドAPI, PDF, PNG, CSV, Excel変換"
description: "Aspose.Cells Cloudに保存されたワークシートを、単一のGETリクエストでPDF、PNG、SVG、CSV、その他の形式に変換します。C#、Java、Pythonなど向けのコードサンプルを含みます。"
weight: 100
---

Aspose.Cells Cloud Web API を使用して、クラウド上のスプレッドシート/Excelワークシートを別の形式のファイルにエクスポートします。

## **ワークシートを別の形式にエクスポートする API**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメーター**

| パラメーター名     | タイプ   | パス / クエリ文字列 / HTTP ボディ | 説明                                                                                                                                                        |
| :----------------- | :----- | :------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | 文字列 | パス                       | （必須）取得するワークブックファイルの名前。                                                                                                                |
| **worksheet**      | 文字列 | パス                       | （必須）変換する特定のワークシート。                                                                                                                        |
| **format**         | 文字列 | クエリ                     | （必須）出力形式（例: `png`, `pdf`, `svg`）。                                                                                                               |
| **folder**         | 文字列 | クエリ                     | （任意）ワークブックが保存されているフォルダーのパス。既定値は `null` です。                                                                                |
| **storageName**    | 文字列 | クエリ                     | （任意）カスタムクラウドストレージの名前。省略された場合、既定のストレージが使用されます。                                                                  |
| **outPath**        | 文字列 | クエリ                     | （任意）出力フォルダーのパス。既定値は `null` です。                                                                                                        |
| **outStorageName** | 文字列 | クエリ                     | （任意）出力ファイルのストレージ名。                                                                                                                        |
| **fontsLocation**  | 文字列 | クエリ                     | （任意）必要に応じてカスタムフォントを指定します。                                                                                                          |
| **region**         | 文字列 | クエリ                     | （任意）スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響を与えます。                            |
| **password**       | 文字列 | クエリ                     | （任意）スプレッドシートファイルにアクセスするためのパスワード。                                                                                           |

### **レスポンス**

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

**HTTP ステータスコード**

| コード | 意味                  | 説明                                                             |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request           | パラメーターが不足しているか、無効です（例: 未対応のファイル形式）。 |
| 401  | Unauthorized          | JWT トークンが無効または不足しています。                         |
| 413  | Payload Too Large     | アップロードされたファイルがサイズ制限を超えています。           |
| 500  | Internal Server Error | 予期せぬサーバーエラーが発生しました。                           |

## **ワークシートを別の形式にエクスポートする API の使用場所**

- **レガシーシステムの移行** – 数千のレガシー XLS ファイルをモダンなシステム用に XLSX に変換します。
- **アーカイブの標準化** – さまざまなスプレッドシート形式（XLS、XLSM、ODS、CSV）をアーカイブ用に単一の形式に正規化します。
- **オフィススイートの相互運用性** – Excel ファイルを、LibreOffice、Google スプレッドシート、Apple Numbers と互換性のある形式に変換します。
- **データソースの正規化** – 異なるスプレッドシート形式をデータベース取り込み用に CSV または JSON に変換します。
- **ウェブ公開** – 財務モデルを HTML に変換してウェブ上で表示します。

## なぜワークシートを別の形式にエクスポートする API を使用すべきなのか？

- **多言語 SDK サポート** – 複数のプログラミング言語向けのクライアントライブラリを提供し、開発者が好みの開発環境から直接 API を呼び出せるようにします。
- **中間アップロードを必要としない直接変換** – クラウドストレージに保存されたワークシートを、ファイルをダウンロード・再アップロードすることなく、要求された形式に変換できます。
- **データのみの抽出** – 視覚的な装飾を保持せず、選択された形式でワークシートの内容を返します。

## SDK を使用してスプレッドシートワークシートを形式としてエクスポートする API を使用する方法

### ワークシートを別の形式にエクスポートする API の仕様

[ワークシートを別の形式にエクスポートする API の仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) は、ウェブブラウザから直接 REST アクセスを行うための公開可能なプログラミングインターフェースを提供します。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速に行え、短いコードでスプレッドシートワークシートを形式ファイルにエクスポートできます。  
Aspose.Cells Cloud SDK の完全な一覧は、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを送信する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}