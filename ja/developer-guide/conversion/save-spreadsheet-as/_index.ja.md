---
title: "スプレッドシートを他の形式で保存 – Aspose.Cells Cloud API (v4.0)"
second_title: "ドキュメント"
ArticleTitle: "リモートストレージ上のスプレッドシートを他の形式ファイルとして保存する方法：ステップ・バイ・ステップ・ガイド"
linktype: "docs"
url: /ja/save-spreadsheet-as/
keywords: "Aspose Cells, スプレッドシート変換, 保存方法, API, XLSXからPDFへ, クラウドストレージ, ExcelからPDFへ, CSVエクスポート, クラウド変換"
description: "Aspose.Cells Cloud のスプレッドシート保存 API を使用して、Aspose Cloud に保存されたスプレッドシートを別の形式（XLSX、PDF、CSV など）で保存する方法を学びます。リクエスト構文、パラメータ、curl の例、SDK コードを含みます。"
weight: 100
---

クラウド上のスプレッドシートまたは Excel ファイルを、別の形式でクラウドストレージに保存します。

## **スプレッドシートを保存する API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名       | 型     | 位置     | 説明                                                                                                     |
| :----------------- | :----- | :------- | :------------------------------------------------------------------------------------------------------- |
| name               | 文字列 | パス     | **必須**。変換するワークブックファイルの名前。                                                           |
| format             | 文字列 | クエリ   | **必須**。希望の出力形式（例：`Xlsx`、`PDF`、`CSV`）。                                                   |
| saveOptionsData    | クラス | 本文     | オプションの保存オプションデータ。省略した場合、既定値は `null` です。                                   |
| folder             | 文字列 | クエリ   | オプション。ソースワークブックが保存されているフォルダのパス。省略した場合、既定値は `null` です。         |
| storageName        | 文字列 | クエリ   | オプション。カスタムストレージの名前。省略した場合、既定ストレージが使用されます。                        |
| outPath            | 文字列 | クエリ   | オプション。変換されたファイルの出力パス。省略した場合、既定値は `null` です。                            |
| outStorageName     | 文字列 | クエリ   | オプション。出力ファイル用のストレージ名。                                                                |
| fontsLocation      | 文字列 | クエリ   | オプション。カスタムフォントの場所。                                                                      |
| region             | 文字列 | クエリ   | オプション。スプレッドシートの地域設定。                                                                  |
| password           | 文字列 | クエリ   | オプション。スプレッドシートファイルを開くためのパスワード。                                              |

**サポートされる出力形式**

| 形式   | 拡張子                                           |
| :----- | :----------------------------------------------- |
| Xlsx   | .xlsx                                            |
| Pdf    | .pdf                                             |
| Csv    | .csv                                             |
| Html   | .html                                            |
| Ods    | .ods                                             |
| Xls    | .xls                                             |
| Txt    | .txt                                             |
| Mhtml  | .mhtml                                           |
| Tiff   | .tiff                                            |
| Pptx   | .pptx                                            |
| …（その他） | 完全なリストについては API 仕様を参照（20種類以上） |

### **レスポンス**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**エラー応答の例（400 Bad Request）**

```json
{
  "Code": 400,
  "Message": "無効なリクエストパラメータです。"
}
```

**HTTP ステータスコード**

| コード | 意味                 | 説明                                                              |
| ------ | -------------------- | ----------------------------------------------------------------- |
| 200    | OK                   | フィルターが正常に適用され、レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request          | パラメータが不足または無効（例：サポートされていないファイル形式）。|
| 401    | Unauthorized         | JWT トークンが無効または不足しています。                           |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。             |
| 500    | Internal Server Error| 想定外のサーバーエラーが発生しました。                             |

## どこでスプレッドシート保存 API を使用すべきか？

### エンタープライズ文書管理システム

- 財務レポートを PDF アーカイブとして自動保存。
- 売上データを定期的に CSV 形式でバックアップ。
- プロジェクト計画を読み取り専用ファイルとして保存し、誤って変更されないようにする。

### データ統合およびETL処理

- CRM システムのデータをエクスポートし、標準の Excel テンプレートとして保存。
- ERP データを CSV に変換して、他のシステムへインポート。
- 生データを JSON として保存し、API による送信に使用。

### 開発および自動化のシナリオ

- Web アプリケーションのバックエンド処理。
- 自動レポート生成システム。
- クラウドコラボレーションプラットフォーム。
- 承認プロセスとの統合。
- データバックアップおよび移行。

## なぜスプレッドシート保存 API を使用すべきか？

- **開発者フレンドリー** – 多言語向け SDK を提供し、詳細なドキュメントで統合を簡素化。
- **労働効率向上** – サーバー側で変換を処理し、カスタム変換コードの作成を不要に。
- **使用量ベースの課金** – 初期ライセンス料なしで、実行された API 呼び出しのみに課金。
- **サーバー保守不要** – サービスはクラウドで実行されるため、変換インフラの管理が不要。
- **幅広い形式サポート** – 20種類以上のスプレッドシート形式間の変換をサポート。
- **データ忠実性** – 変換中にレイアウト、数式、スタイルを保持。

## SDK を使用してスプレッドシート保存 API を使用する方法

### スプレッドシート保存 API 仕様

[スプレッドシート保存 API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/SaveSpreadsheetAs) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST 相互通信を実行可能にします。

**リクエスト本文と curl を使用した例**

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスへのアクセスが簡単になります。以下の例では、cURL を使用してクラウド API への呼び出しを行う方法を示します。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=pdf&outPath=output.pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{"SaveOptions":{"SaveFormat":"pdf"}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化し、最小限のコードでスプレッドシートを別の形式で保存できるため、開発が最も迅速になります。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示します：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{</tab>}}
{{< /tabs >}}