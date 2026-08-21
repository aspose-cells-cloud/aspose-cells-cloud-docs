---
title: "Aspose.Cells Cloud Web API - Excel チャートを画像に変換 - 無料オンラインツール"
second_title: "ドキュメント"
ArticleTitle: "スプレッドシートのチャートを画像に変換する方法：ステップ・バイ・ステップガイド"
linktitle: "チャートを画像に変換"
type: docs
url: /convert-chart-to-image/
keywords: "チャートを画像に変換, Aspose.Cells, Excel チャートのエクスポート, PNG, SVG, JPEG, BMP, TIFF"
description: "Aspose.Cells Cloud Web API を使用して、スプレッドシートファイルから Excel チャートを PNG、SVG、TIFF、JPEG、BMP 画像に直接変換します。"
weight: 100
---

Excel チャートは、ワークシート内に埋め込まれるデータの視覚的表現です。これらのチャートを画像形式に変換することで、Excel を使用せずにドキュメント、ウェブページ、レポートなど across multiple contexts に簡単に再利用できます。

ローカルのスプレッドシートまたは Excel ファイル内のチャートを画像ファイルに変換します。サポートされている**画像形式**は以下の通りです：<a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>、<a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>、<a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>、<a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>、<a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>

## **チャートを画像に変換する API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/image
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/chart/image?format=png&chartIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@MyWorkbook.xlsx" \
     -o chart.png
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名      | タイプ   | パス / クエリ文字列 / HTTP ボディ | 説明                                                                 | 必須 |
| :---------------- | :------- | :-------------------------------- | :------------------------------------------------------------------- | :--- |
| Spreadsheet       | ファイル | FormData                          | チャートを含むスプレッドシートファイルをアップロードします。         | はい |
| worksheet         | 文字列   | クエリ                            | 該当する場合はワークシート名を指定します。                           | いいえ |
| chartIndex        | 整数     | クエリ                            | 変換するチャートのインデックスです。                                 | はい |
| format            | 文字列   | クエリ                            | （必須）希望する画像形式（例：svg、png、jpg）。                      | はい |
| outPath           | 文字列   | クエリ                            | （任意）出力ファイルを保存するフォルダのパス。デフォルトは null です。 | いいえ |
| outStorageName    | 文字列   | クエリ                            | 出力ファイルのストレージ名です。                                     | いいえ |
| fontsLocation     | 文字列   | クエリ                            | 必要に応じてカスタムフォントを指定します。                           | いいえ |
| region            | 文字列   | クエリ                            | スプレッドシートのリージョンを設定します。                           | いいえ |
| password          | 文字列   | クエリ                            | スプレッドシートファイルのパスワードです。                           | いいえ |

## **レスポンス**

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

| コード | 意味                 | 説明                                                |
| ------ | -------------------- | --------------------------------------------------- |
| 200    | OK                   | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request          | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized         | JWT トークンが無効または不足しています。            |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error| サーバー内で予期せぬエラーが発生しました。           |

## Convert Chart to Image API を使用する適切なシーンは？

- **レポート生成とダッシュボード**：Excel データからチャートを自動的に画像（PNG、JPEG など）に変換し、PDF レポート、ウェブダッシュボード、PowerPoint プレゼンテーションに埋め込みます。
- **ウェブ／メールアプリケーション**：ユーザーが Excel ファイルをダウンロードまたは開くことなく、ウェブページやメールでチャート画像を直接提供します。動的レポーティングツール、ニュースレター、自動通知に役立ちます。
- **ドキュメント処理ワークフロー**：Excel のチャートを他の形式（Word、PDF、HTML）に挿入する必要がある自動化パイプライン（例：請求書、分析）に統合します。
- **モバイル／デスクトップアプリケーション**：スプレッドシート全体をレンダリングする必要がない、または非現実的なアプリケーションで Excel チャートを表示します。
- **アーカイブと可視化**：Excel 依存なしで、長期保存用やサムネイル、クイックプレビュー用としてチャートをスタンドアロン画像として保存します。

## Convert Chart to Image API を使用する理由は？

- **視覚的な正確性を維持**：Excel 上での色、ラベル、スケーリングなどのチャート書式を正確に保持し、プロフェッショナルな品質の出力を保証します。
- **プラットフォーム非依存**：Excel のインストールは不要です。REST API 経由でクロスプラットフォーム（Windows、Linux、macOS）で動作し、クラウドベースまたはサーバーサイドアプリケーションに最適です。
- **自動化とスケーラビリティ**：複数のチャートやファイルを一括でプログラム的に変換でき、手動エクスポートに比べて時間を大幅に節約できます。クラウド上で大規模な処理も効率的に実行可能です。
- **柔軟な出力形式**：人気のある画像形式（PNG、JPG、BMP、SVG など）をサポートし、多様なシステムやメディアとの統合が可能です。
- **セキュアで信頼性が高い**：クライアント側ツールに機密データをさらすことなく、Aspose のクラウド環境でファイル処理を行います。高可用性と安定したパフォーマンスを提供します。
- **開発者向けに最適化**：Aspose.Cells Cloud は複数の言語向け SDK ライブラリを提供しており、迅速な開発が可能です。また、包括的なドキュメントも用意されています。カスタムチャートレンダリングソリューションの構築と比較すると、開発作業を大幅に削減できます。
- **コスト効率的**：ワークブックを先にアップロードせずにチャートを変換できるため、ストレージ容量を節約し、コストを削減できます。

## SDK を使用して Convert Chart to Image API をどのように活用するか？

### Convert Chart to Image API の仕様

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage" rel="noopener noreferrer">Convert Chart to Image API の仕様</a>は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 呼び出しを実行できるようにします。

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も速く、短いコードでチャートを画像に変換できます。  
Aspose.Cells Cloud SDK の完全な一覧は <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}