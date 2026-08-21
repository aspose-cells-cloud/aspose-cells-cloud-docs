---
title: "Aspose.Cells Cloud API – ExcelチャートをPDFに変換"
second_title: "ドキュメント"
ArticleTitle: "ローカルスプレッドシートのチャートをPDFファイルに変換する方法：ステップ・バイ・ステップガイド"
linktitle: "チャートをPDFに変換"
type: docs
url: /convert-chart-to-pdf/
keywords: "Aspose Cells, チャート, PDF, Excel, 変換, クラウドAPI"
description: "Aspose.Cells Cloud REST API を使用して、ローカルExcelファイルのチャートをPDF形式にエクスポートします。XLSXおよびXLSファイルをサポートします。"
weight: 100
---

クラウドAPIを使用して、ローカルのExcelファイルからチャートを[PDF](https://docs.fileformat.com/pdf/)形式にエクスポートします。

## **チャートをPDFに変換するWeb API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を必要とします。

### **リクエストパラメータ**

| パラメータ名      | タイプ    | パス/クエリ文字列/HTTPボディ | 説明                                                                 |
| ----------------- | --------- | ---------------------------- | -------------------------------------------------------------------- |
| Spreadsheet       | ファイル  | FormData                     | スプレッドシートファイルをアップロードします。                      |
| worksheet         | 文字列    | クエリ                       | チャートを含むワークシートの名前。                                  |
| chartIndex        | 整数      | クエリ                       | 変換するチャートのインデックス。                                    |
| outPath           | 文字列    | クエリ                       | （オプション）変換されたファイルを保存するフォルダパス。デフォルトはnullです。 |
| outStorageName    | 文字列    | クエリ                       | 出力ファイルのストレージ名。                                        |
| fontsLocation     | 文字列    | クエリ                       | 必要に応じてカスタムフォントを使用します。                          |
| region            | 文字列    | クエリ                       | スプレッドシートの地域設定。                                        |
| password          | 文字列    | クエリ                       | スプレッドシートファイルを開くためのパスワード。                    |

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

**HTTPステータスコード**

| コード | 意味             | 説明                                                     |
| ------ | ---------------- | -------------------------------------------------------- |
| 200    | OK               | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized     | JWTトークンが無効または不足しています。                  |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。  |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。              |

## いつConvert Chart to PDF APIを使用すべきか？

### **1. ビジネスレポートと自動化**

- **財務部門**：月次財務レポートのチャート → PDFアーカイブ
- **営業チーム**：業績トレンドチャート → PDFクライアントレポート
- **マーケティング分析**：キャンペーン業績チャート → PDF経営陣向け簡報
- **運用管理**：生産モニタリングチャート → PDFコンプライアンスドキュメント

### **2. ソフトウェア開発と統合**

- **SaaSアプリケーション**：ユーザー生成チャートデータ → ダウンロード可能なPDFレポート
- **エンタープライズシステム**：ERP/CRMシステムのチャート → PDF監査ドキュメント
- **モバイルアプリケーション**：アプリ内分析チャート → 共有可能なPDFファイル
- **Webアプリケーション**：ダッシュボードチャート → PDFエクスポート機能

### **3. ドキュメント処理ワークフロー**

- **バッチ処理**：複数のExcelファイルのチャートを同時にPDFに変換
- **スケジュールタスク**：自動的な日次／週次チャートレポート生成
- **テンプレートベースの出力**：標準チャート形式 → PDFドキュメント
- **ドキュメント構成**：PDF形式でチャートを他のコンテンツと組み合わせる

### **4. 業界固有のアプリケーション**

- **研究機関**：実験データチャート → PDF研究論文図版
- **教育分野**：教育資料のチャート → PDFカリキュラム教材
- **コンサルティングファーム**：分析チャート → PDFクライアント成果物
- **製造業**：品質管理チャート → PDF検査レポート
- **医療分野**：患者データチャート → PDF医療記録
- **公共機関**：統計チャート → PDF公式出版物

### **5. コンテンツ管理と配信**

- **デジタルアセット管理**：標準化されたPDF形式でのチャートアーカイブ
- **ナレッジベース**：埋め込みチャートPDFを含む技術ドキュメント
- **クライアントポータル**：ステークホルダーへの安全なPDFレポート配信
- **規制コンプライアンス**：監査対応のPDFドキュメント生成

## なぜConvert Chart to PDF APIを使用すべきか？

- ワークブックを先にアップロードすることなくチャートを変換できるため、ストレージ容量を節約し、コストを削減できます。
- 既存のAspose.Cells Cloud SDKを通じて、開発を迅速に完了できます。
- **簡単な統合**：明確なドキュメントを備えたREST API。
- **スケーラブルなアーキテクチャ**：小規模からエンタープライズ規模のワークロードまで処理可能です。

## SDKを使用してConvert Chart to PDF APIをどのように活用するか？

### Convert Chart to PDF API仕様

[Convert Chart to PDF API仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPDF) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Webブラウザから直接RESTインタラクションを実行できるようにします。

## Aspose.Cells Cloud SDKの使用

SDKを使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速です。最小限のコードでチャートをPDFファイルに変換できます。  
以下のコード例では、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}