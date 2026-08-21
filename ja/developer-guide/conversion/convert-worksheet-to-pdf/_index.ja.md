---
title: "Aspose.Cells Cloud Web API – ローカルのExcelワークシートをPDFファイルに変換する – 無料オンラインツール"
second_title: "ドキュメント"
ArticleTitle: "ローカルのスプレッドシートワークシートをPDFファイルに変換する方法：ステップ・バイ・ステップ・ガイド"
linktitle: "ワークシートをPDFに変換"
type: docs
url: /ja/convert-worksheet-to-pdf/
keywords: "Aspose.Cells, Excel to PDF, worksheet conversion, REST API, cloud conversion, spreadsheet PDF, API endpoint, PDF generation"
description: "Aspose.Cells Cloud APIを使用して、ローカルのExcelファイルのワークシートを迅速かつ安全にPDFドキュメントに変換します。"
weight: 100
---

Cloud APIを使用して、ローカルのExcelファイルからワークシートを[PDF](https://docs.fileformat.com/pdf/)ファイルにエクスポートします。

## **ワークシートをPDFに変換するAPI**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名 | 型     | パス/クエリ文字列/HTTPボディ | 説明                                                                 |
| ------------ | ------ | -------------------------- | ------------------------------------------------------------------- |
| Spreadsheet  | ファイル | FormData                   | スプレッドシートファイルをアップロードします。                         |
| worksheet    | 文字列   | クエリ                     | スプレッドシート内のワークシート名。                                   |
| outPath      | 文字列   | クエリ                     | (オプション) ワークブックを保存するフォルダーパス。デフォルトはnull。     |
| outStorageName | 文字列 | クエリ                     | 出力ファイルのストレージ名。                                           |
| fontsLocation | 文字列 | クエリ                     | PDFにカスタムフォントを使用します。                                    |
| region       | 文字列   | クエリ                     | スプレッドシートのリージョン設定を定義します。                          |
| password     | 文字列   | クエリ                     | スプレッドシートファイルを開くために必要なパスワード。                  |

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

| コード | 意味                 | 説明                                                             |
| ---- | -------------------- | ---------------------------------------------------------------- |
| 200  | OK                   | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。    |
| 400  | Bad Request          | パラメータが不足しているか無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized         | JWTトークンが無効または不足しています。                             |
| 413  | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。               |
| 500  | Internal Server Error | 予期しないサーバーエラーが発生しました。                             |

## **ワークシートをPDFに変換するAPIを使用すべき場所**

- **財務諸表**：貸借対照表、損益計算書（特定の表）を監査対応のドキュメントとしてPDFに変換します。
- **販売レポート**：販売ダッシュボードやコミッション計算を配布可能なPDFに変換します。
- **運用メトリクス**：KPI表やパフォーマンスメトリクスを正式なPDFレポートとしてエクスポートします。
- **契約データ**：価格表やサービスレベル合意（SLA）をスプレッドシートからPDF添付ファイルとしてエクスポートします。
- **監査トレール**：財務ワークシートを編集不可のPDF証拠として保存します。
- **ポートフォリオ概要**：投資パフォーマンス表をクライアント向けのPDFステートメントとしてエクスポートします。
- **品質管理レポート**：検査ワークシートをコンプライアンス記録用にPDFとしてエクスポートします。
- **在庫サマリー**：在庫ワークシートを管理チーム向けにPDFとして変換します。

## **なぜワークシートをPDFに変換するAPIを使用すべきか**

- **開発者フレンドリー**：Aspose.Cells Cloudは複数の言語でSDKライブラリを提供しており、迅速な開発が可能です。また、包括的なドキュメントも整備されています。独自のチャート描画ソリューションを構築する場合と比べ、開発負荷を大幅に削減できます。
- **コスト効率**：ワークブックをまずアップロードせずに表データを変換できるため、ストレージ容量を節約し、コストを削減できます。
- **フォーマットの維持**：複雑なExcelフォーマットを、汎用的にアクセス可能なPDF形式で維持します。

## **SDKを使用してワークシートをPDFに変換するAPIを活用する方法**

### Convert Worksheet to PDF API仕様

[Convert Worksheet to PDF API仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF)は、公開可能なプログラミングインターフェースを提供し、Webブラウザから直接REST通信を可能にします。

cURLコマンドラインツールを使用して、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例では、cURLを使用してCloud APIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

### Aspose.Cells Cloud SDKの使用

SDKを使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速に行えます。最小限のコードでスプレッドシートの表データをPDFファイルに変換できます。Aspose.Cells Cloud SDKの完全な一覧は、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}

---