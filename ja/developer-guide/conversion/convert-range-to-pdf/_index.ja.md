---
title: "Aspose.Cells Cloud API を使用して Excel の範囲を PDF に変換する"
second_title: "ドキュメント"
articleTitle: "ローカルスプレッドシートの範囲データを PDF ファイルに変換する方法：ステップ・バイ・ステップ・ガイド"
linktitle: "範囲を PDF に変換"
type: docs
url: /ja/convert-range-to-pdf/
keywords: "Aspose.Cells Cloud、Excel の範囲を PDF に変換、Excel to PDF、クラウド変換"
description: "Aspose.Cells Cloud の REST API を使用して、ローカル Excel スプレッドシートの特定の範囲を PDF に変換します。"
weight: 100
---

ローカルの Excel ファイルから範囲データを [PDF](https://docs.fileformat.com/pdf/) ファイルにエクスポートします。この操作はクラウド API を使用して行います。

**前提条件**: この API を使用するには、有効な Aspose.Cells Cloud アカウント、JWT アクセストークンが必要です。また、必要に応じて使用するプログラミング言語向けの Aspose.Cells Cloud SDK も用意してください。`outStorageName` パラメータを使用する場合は、対象のストレージ（デフォルトまたはカスタム）が事前に設定されていることを確認してください。

## **範囲を PDF に変換する API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名     | タイプ   | パス/クエリ文字列/HTTP ボディ | 説明                                                                 |
| ---------------- | -------- | ----------------------------- | -------------------------------------------------------------------- |
| Spreadsheet      | ファイル | FormData                      | スプレッドシートファイルをアップロードします。                       |
| worksheet        | 文字列   | クエリ                        | スプレッドシート内のワークシート名。                                 |
| range            | 文字列   | クエリ                        | 変換するセル範囲（例: A1:C10）。                                     |
| outPath          | 文字列   | クエリ                        | （任意）ワークブックが保存されているフォルダのパス。デフォルトは null。 |
| outStorageName   | 文字列   | クエリ                        | 出力ファイルのストレージ名。                                         |
| fontsLocation    | 文字列   | クエリ                        | ホーム利用向けのカスタムフォントを保存する場所。                     |
| region           | 文字列   | クエリ                        | スプレッドシートの地域設定。                                         |
| password         | 文字列   | クエリ                        | スプレッドシートファイルのオープンに必要なパスワード。               |

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

_通常のレスポンスは、PDF のバイナリストリームをファイルとしてダウンロードする形式です。_

**HTTP ステータスコード**

| コード | 意味             | 説明                                                             |
| ------ | ---------------- | ---------------------------------------------------------------- |
| 200    | OK               | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足または無効（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized     | JWT トークンが無効または不足しています。                         |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。           |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。                      |

## **「範囲を PDF に変換する API」の使用例**

- **財務諸表**: 貸借対照表や損益計算書（特定の範囲）を監査対応ドキュメントとして PDF に変換します。
- **販売レポート**: 売上ダッシュボードや手数料計算結果を配布可能な PDF 形式に変換します。
- **運用指標**: KPI 表やパフォーマンス指標を正式な PDF レポートとしてエクスポートします。
- **契約データ**: スプレッドシート内の価格表やサービスレベル合意（SLA）を PDF 添付ファイルとしてエクスポートします。
- **監査トレース**: 財務データの範囲を編集不可の PDF 証拠として保存します。
- **ポートフォリオ概要**: 投資パフォーマンスの範囲を顧客向け PDF 請求書としてエクスポートします。
- **品質管理レポート**: 検査データの範囲をコンプライアンス記録用に PDF としてエクスポートします。
- **在庫概要**: 在庫レベル表を管理層向けレビュー用に PDF に変換します。

## **「範囲を PDF に変換する API」を使用する理由**

- **開発者フレンドリー**: Aspose.Cells Cloud は複数のプログラミング言語向けの SDK ライブラリを提供しており、迅速な開発と包括的なドキュメントが可能です。カスタムのチャート描画ソリューションを構築する場合と比べ、開発負荷を大幅に削減します。
- **コスト効率**: 全ワークブックを先にアップロードせずに範囲データのみを変換できるため、ストレージ容量を節約し、コストを削減できます。
- **複雑な Excel 書式を保持**: 世界共通でアクセス可能な PDF 形式で、複雑な Excel 書式をそのまま保持します。

## **SDK を使用して「範囲を PDF に変換する API」を活用する方法**

### 範囲を PDF に変換する API の仕様

[範囲を PDF に変換する API の仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF) は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速です。短いコードで範囲データを PDF ファイルに変換できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを送信する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}