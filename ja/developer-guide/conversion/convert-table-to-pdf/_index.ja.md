---
title: "Aspose.Cells Cloud Web API - ローカルのExcelテーブルデータをPDFファイルに変換する - 無料オンラインツール"
second_title: "ドキュメント"
ArticleTitle: "ローカルのスプレッドシートテーブルデータをPDFファイルに変換する方法：ステップ・バイ・ステップガイド"
linktitle: "テーブルをPDFに変換"
type: docs
url: /convert-table-to-pdf/
keywords: "Aspose.Cells, Excel to PDF, テーブル変換, Cloud API"
description: "Aspose.Cells Cloud REST API を使って、ローカルのExcelテーブルを迅速にPDFファイルに変換します。"
weight: 100
---

クラウドAPIを使用して、ローカルのExcelファイルからテーブルデータをPDFファイルにエクスポートします。

## **テーブルをPDFに変換するAPI**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメーター:**

| パラメーター名 | 型     | パス/クエリ文字列/HTTP本文 | 説明                                                                 |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------- |
| Spreadsheet    | ファイル | FormData                   | 変換するスプレッドシートファイルをアップロードします。               |
| worksheet      | 文字列  | クエリ                     | スプレッドシートのワークシート名。                                   |
| tableName      | 文字列  | クエリ                     | 変換するテーブル名。                                                 |
| outPath        | 文字列  | クエリ                     | (オプション) 変換されたPDFを保存するフォルダーパス。デフォルトは null。 |
| outStorageName | 文字列  | クエリ                     | 出力ファイルストレージの名前を指定します。                           |
| fontsLocation  | 文字列  | クエリ                     | PDFにカスタムフォントを使用します。                                  |
| region         | 文字列  | クエリ                     | スプレッドシートの地域設定を指定します。                             |
| password       | 文字列  | クエリ                     | スプレッドシートファイルにアクセスするためのパスワード。             |

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

**サンプルレスポンスヘッダー**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**HTTPステータスコード**

| コード | 意味               | 説明                                                       |
| ---- | ----------------- | --------------------------------------------------------- |
| 200  | OK                | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400  | Bad Request       | パラメーターが不足しているか無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized      | JWT トークンが無効または不足している。                         |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えた。               |
| 500  | Internal Server Error | 予期せぬサーバーエラーが発生しました。                          |

## **どこでConvert Table to PDF APIを使用すべきか？**

- **財務諸表**: 貸借対照表、損益計算書（特定のテーブル）を監査対応文書としてPDFに変換。
- **営業レポート**: 営業ダッシュボードや手数料計算を配布可能なPDFに変換。
- **運用指標**: KPIテーブルやパフォーマンスメトリクスを正式なPDFレポートとしてエクスポート。
- **契約データ**: 価格テーブルやサービスレベル合意（SLA）をスプレッドシートからPDF添付ファイルとしてエクスポート。
- **監査トレイル**: 金銭データテーブルを編集不可のPDF証拠として保持。
- **ポートフォリオ概要**: 投資パフォーマンステーブルをクライアント向けPDFステートメントとしてエクスポート。
- **品質管理レポート**: 検査データテーブルをコンプライアンス記録用にPDFエクスポート。
- **在庫概要**: 在庫レベルテーブルを管理層向けにPDFでエクスポート。

## **なぜConvert Table to PDF APIを使用すべきか？**

- **開発者フレンドリー**: Aspose.Cells Cloud は複数の言語で SDK ライブラリを提供しており、迅速な開発が可能で、包括的なドキュメントも整っています。独自のチャート描画ソリューションを構築する場合と比べ、開発作業を大幅に削減できます。
- **コスト効率**: ワークブックを先にアップロードせずにテーブルデータを変換できるため、ストレージ容量を節約し、コストを削減できます。
- **複雑なExcel書式を保持**: 世界中でアクセス可能なPDF形式で、複雑なExcel書式を維持します。

## **SDK を使って Convert Table to PDF API を使用する方法**

### Convert Table to PDF API スペック

[Convert Table to PDF API スペック](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF) は、Webブラウザから直接 REST 通信を実行できるパブリックアクセス可能なプログラミングインターフェースを提供します。
cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最速で行え、最小限のコードでスプレッドシートテーブルデータをPDFファイルに変換できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}