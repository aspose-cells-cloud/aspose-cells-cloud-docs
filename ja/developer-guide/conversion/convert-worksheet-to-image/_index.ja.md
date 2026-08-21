---
title: "ワークシート変換 – Aspose.Cells Cloud API ドキュメント"
second_title: "ドキュメント"
ArticleTitle: "ローカルのワークシートスプレッドシートデータを画像ファイルに変換する方法：ステップ・バイ・ステップ・ガイド"
linktitle: "ワークシートを画像に変換"
type: docs
url: /convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud, ワークシートを画像に変換, Excel を PNG に変換, Excel を SVG に変換, Excel を TIFF に変換, Excel を JPEG に変換, Excel を BMP に変換, 画像変換 API, REST API, スプレッドシートの画像エクスポート, SDK サンプル"
description: "Aspose.Cells Cloud API を使用して Excel ワークシートを画像形式 (PNG、SVG、TIFF、JPEG、BMP など) に変換するステップ・バイ・ステップ・ガイド。リクエストパラメータ、レスポンスの詳細、エラーコード、使用シナリオ、SDK コードサンプルを含みます。"
weight: 100
---

ローカルの Excel ファイル内のワークシートから [画像](https://docs.fileformat.com/image/) ファイルへデータをエクスポートするには、Aspose.Cells Cloud API を使用します。この操作は複数の画像形式をサポートしており、スプレッドシートデータのビジュアルなスナップショットを生成するのに最適です。

**サポートされる画像形式**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **ワークシートを画像に変換する API**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名      | 型     | Path / クエリ文字列 / HTTP ボディ | 説明                                                                 |
| :---------------- | :----- | :-------------------------------- | :------------------------------------------------------------------- |
| Spreadsheet       | ファイル | FormData                          | スプレッドシートファイルをアップロードします。                       |
| worksheet         | 文字列   | クエリ                            | 変換対象のワークシート名。                                           |
| format            | 文字列   | クエリ                            | 期望する画像形式（`svg`、`png`、`tiff`、`jpeg`、`bmp` など）。        |
| outPath           | 文字列   | クエリ                            | _(オプション)_ 出力画像の保存先フォルダパス。デフォルトは `null`。   |
| outStorageName    | 文字列   | クエリ                            | 出力ファイルの保存先ストレージ名。                                   |
| fontsLocation     | 文字列   | クエリ                            | サーバーにないフォントを使用する場合のカスタムフォントフォルダのパス。|
| region            | 文字列   | クエリ                            | スプレッドシートの地域設定（例: `en-US`）。                          |
| password          | 文字列   | クエリ                            | 保護されたスプレッドシートファイルを開くために必要なパスワード。     |

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

| コード | 意味               | 説明                                                      |
| ------ | ------------------ | --------------------------------------------------------- |
| 200    | OK                 | フィルター適用成功；レスポンスには操作の詳細が含まれます。|
| 400    | Bad Request        | パラメータ不足または不正（例: サポートされないファイル形式）。|
| 401    | Unauthorized       | JWT トークンが不正または不足しています。                  |
| 413    | Payload Too Large  | アップロードされたファイルがサイズ制限を超えています。    |
| 500    | Internal Server Error | サーバー内部エラーが発生しました。                        |

## **ワークシートを画像に変換する API の使用場面**

- **静的レポートスナップショット** – 財務表、計算式、その他のデータを画像に変換し、編集不要な PDF レポート、PowerPoint スライド、印刷ドキュメントに組み込みます。
- **プレゼンテーション用のデータ可視化** – 複雑なスプレッドシート表（条件付き書式や簡単なチャートを含む）を画像に変換し、プレゼンテーション（PPTX、Google スライド）に埋め込みます。
- **ドキュメント・トレーニング資料** – スプレッドシートの例、テンプレート、データ入力フォームを画像としてキャプチャし、ユーザーマニュアル、チュートリアル、ナレッジベース記事に使用します。
- **サムネイルプレビュー** – ファイルブラウザ、ドキュメントライブラリ、検索結果用に、スプレッドシートの重要なセクションの小さな画像プレビューを生成します。

## **なぜワークシートを画像に変換する API を使用すべきか**

- **開発者フレンドリー** – Aspose.Cells Cloud は複数の言語で SDK ライブラリを提供しており、迅速な開発を可能にし、包括的なドキュメントも整備されています。カスタムのチャート描画ソリューションを構築する場合と比べ、開発作業を大幅に削減できます。
- **コスト効率** – ワークブックを永続的に保存せずに表データを変換できるため、ストレージ容量を節約し、コストを削減できます。
- **ピクセルレベルでの正確な再現** – 出力画像には、セル書式、数式（表示値として）、罫線、色、条件付き書式など、Excel の外観を忠実に再現します。
- **汎用互換性** – 画像形式（PNG、JPEG、TIFF、BMP、SVG など）は、特殊なソフトウェアを必要とせず、あらゆるデバイスやプラットフォームで表示可能で、最大限のアクセシビリティを実現します。

## **SDK を使用してワークシートを画像に変換する API を利用する方法**

### ワークシートを画像に変換する API 仕様

[ワークシートを画像に変換する API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 通信を行うことができます。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
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

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速になります。最小限のコードでワークシートデータを画像に変換できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}