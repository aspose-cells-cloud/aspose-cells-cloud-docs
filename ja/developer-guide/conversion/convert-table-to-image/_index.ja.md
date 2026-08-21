---
title: "Aspose.Cells Cloud Web API - ローカルのExcelテーブルデータを画像ファイルに変換する - 無料のオンラインツール"
second_title: "ドキュメント"
ArticleTitle: "ローカルのスプレッドシートテーブルデータを画像ファイルに変換する方法：ステップバイステップガイド"
linktitle: "テーブルを画像に変換"
type: docs
url: /ja/convert-table-to-image/
keywords: "Aspose.Cells, Cloud API, テーブルを画像に変換, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "Aspose.Cells Cloud API を使用して、ローカルの Excel スプレッドシートテーブルを画像ファイルに迅速に変換します。PNG、JPEG、TIFF、BMP、SVG およびその他の形式をサポートします。"
weight: 100
---

Cloud API を使用して、ローカルの Excel ファイルから[画像](https://docs.fileformat.com/image/)ファイルへテーブルデータをエクスポートします。

**サポートされている画像形式:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **テーブルを画像に変換する API**

このエンドポイントを使用する前に、以下の前提条件を確認してください。

- Aspose.Cells Cloud の認証を通じて取得した有効な JWT アクセストークン。
- `outPath` または `outStorageName` パラメータを使用する場合、アクセス可能なストレージアカウント。
- ソースワークブック（ローカルの Excel ファイル）が読み取り可能である必要があります。また、保護されている場合は正しいパスワードを指定する必要があります。

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### **リクエストパラメータ:**

| パラメータ名      | タイプ   | パス／クエリ文字列／HTTP ボディ | 説明                                                                                                                                                 |
| :---------------- | :------- | :---------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | ファイル | FormData                        | スプレッドシートファイルをアップロードします。                                                                                                        |
| worksheet         | 文字列   | クエリ                          | スプレッドシート／Excel のワークシート名。                                                                                                            |
| tableName         | 文字列   | クエリ                          | 変換するテーブルの名前。                                                                                                                              |
| format            | 文字列   | クエリ                          | 期望する画像ファイル形式（例: png, svg）。                                                                                                            |
| outPath           | 文字列   | クエリ                          | （オプション）変換された画像を保存するフォルダーパス。デフォルトは null です。                                                                        |
| outStorageName    | 文字列   | クエリ                          | 出力ファイルのストレージ名を指定します。                                                                                                              |
| fontsLocation     | 文字列   | クエリ                          | 必要に応じてカスタムフォントを使用します。                                                                                                            |
| region            | 文字列   | クエリ                          | スプレッドシートの地域／言語設定（例: `en-US`, `fr-FR`）。数値書式、日付解析、地域固有の動作に影響を与えます。                                           |
| password          | 文字列   | クエリ                          | スプレッドシートファイルにアクセスするために必要なパスワード。                                                                                       |

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

| コード | 意味             | 説明                                                       |
| ------ | ---------------- | ---------------------------------------------------------- |
| 200    | OK               | フィルターの適用に成功しました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足または無効です（例: 未対応のファイル形式）。     |
| 401    | Unauthorized     | JWT トークンが無効または不足しています。                         |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。           |
| 500    | Internal Server Error | サーバー内部で予期せぬエラーが発生しました。                     |

## **テーブルを画像に変換する API の使用例**

- **静的なレポートスナップショット**: 財務テーブル、計算結果、またはその他のフォーマット済みデータを画像に変換し、編集が不要な PDF レポート、PowerPoint スライド、印刷ドキュメントに組み込みます。
- **プレゼンテーションでのデータ可視化**: 条件付き書式やシンプルなビジュアライゼーションを含む複雑なスプレッドシートテーブルを画像に変換し、プレゼンテーション（PPTX、Google Slides）に埋め込みます。
- **ドキュメントおよびトレーニング資料**: スプレッドシートの例、テンプレート、データ入力フォームを画像としてキャプチャし、ユーザーマニュアル、チュートリアル、ナレッジベース記事に使用します。
- **サムネイルプレビュー**: 重要なスプレッドシートセクションの小さな画像プレビューを生成し、ファイルブラウザ、ドキュメントライブラリ、検索結果に表示します。

## **なぜテーブルを画像に変換する API を使用すべきか？**

- **開発者フレンドリー**: Aspose.Cells Cloud は複数の言語向け SDK ライブラリを提供し、迅速な開発を可能にします。また、包括的なドキュメントも整っています。カスタムレンダリングソリューションを構築する場合と比較して、開発作業を大幅に削減できます。
- **コスト効率的**: ワークブック全体を先にアップロードせずにテーブルデータを変換できるため、ストレージ容量を節約し、コストを削減できます。
- **ピクセル単位の正確な再現**: セル書式、数式（表示値として）、境界線、色、条件付き書式などを、出力画像に忠実に再現します。
- **汎用互換性**: 画像形式（PNG、JPEG、TIFF、BMP、SVG など）は、専用ソフトウェアを必要とせずにあらゆるデバイスやプラットフォームで表示可能で、最大限のアクセシビリティを実現します。

## **SDK を使用してテーブルを画像に変換する API を利用する方法**

### テーブルを画像に変換する API の仕様

[テーブルを画像に変換する API の仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage) は、Web ブラウザから直接 REST インタラクションを実行できる公開可能なプログラミングインターフェースを提供します。

cURL コマンドラインツールを使用することで、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
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

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速に行えます。最小限のコードでスプレッドシートテーブルデータを画像に変換できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}