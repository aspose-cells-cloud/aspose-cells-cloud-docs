---
title: "Aspose.Cells Cloud Web API – スプレッドシートを目的の言語に翻訳する"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud AI 翻訳 API を使用してスプレッドシート全体を翻訳する方法"
linktype: "翻訳スプレッドシート"
type: docs
url: /translate-spreadsheet/
keywords: "Aspose.Cells Cloud, スプレッドシート翻訳 API, AI 翻訳, スプレッドシート翻訳, targetLanguage, マルチシート翻訳, クラウドスプレッドシート処理, Aspose.Cells Cloud 翻訳"
description: "Aspose.Cells Cloud AI を使用して Excel ブック全体を翻訳します。テキストをサポートされる任意の言語に変換しながら、数式、チャート、書式を保持します。エンドポイント、パラメータ、SDK の使用例、制限事項、エラー処理について学習します。"
weight: 100
---

**TranslateSpreadsheet** エンドポイントは **Translate Spreadsheet API** の一部であり、ブック内のすべてのテキスト要素を読み取り、その内容を AI 搭載の翻訳サービスに送信し、指定された **targetLanguage** ですべてのテキストデータが表示された新しいスプレッドシートファイルを返します。この操作は、元のレイアウト、セルのスタイル、数式、および**マルチシート構造**をそのまま維持するため、グローバル向けのレポート、ダッシュボード、データ駆動型ドキュメントの多言語化に最適です。サポートされるファイル形式は、XLS、XLSX、XLSM、CSV、ODS です。無効な言語コード、認証失敗、翻訳サービスの障害などの場合はエラーが返されます。

## **Translate Spreadsheet API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/spreadsheet
```

### **リクエストパラメータ**

| パラメータ名 | タイプ   | 位置     | 必須/任意 | 説明                                                                                                                                                                                                 |
| :----------- | :------- | :------- | :-------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet  | ファイル | 必須     | FormData  | 翻訳対象の Excel ブック。許可される拡張子: .xls、.xlsx、.xlsm、.csv、.ods。最大ファイルサイズ: 50 MB。例: `budget.xlsx`。                                                                            |
| targetLanguage | 文字列 | 必須     | クエリ    | 目的の出力言語の ISO 639-1 言語コード（例: "es"（スペイン語）、"fr"（フランス語）、"de"（ドイツ語））。底层の AI サービスでサポートされている言語である必要があります。                             |
| region       | 文字列   | 任意     | クエリ    | スプレッドシートの地域識別子で、日付、数値、通貨などのロケール固有の書式に影響を与えます。一般的な値: "US"、"EU"、"CN"。省略された場合、ブックの元の地域設定が使用されます。                              |
| password     | 文字列   | 任意     | クエリ    | パスワードで保護されたブックを開くためのパスワード。ファイルがパスワード保護されていない場合は空白のままにしてください。                                                                             |

### **レスポンス**

成功レスポンス（200 OK）  
ヘッダー:  
Content-Type: application/octet-stream // CSV 出力が要求された場合は text/csv  
Content-Disposition: attachment; filename="translated.xlsx"  
Content-Length: <バイト単位のサイズ>

ボディ:  
<翻訳済みスプレッドシートファイルを含むバイナリストリーム>

エラーレスポンスは、`code`、`message`、およびオプションの `details` フィールドを持つ標準的な Aspose.Cells Cloud エラーモデル（application/json）に従います。

**HTTP ステータスコード**

| コード | 意味                   | 説明                                          |
| ------ | ---------------------- | --------------------------------------------- |
| 200    | OK                     | フィルターが正常に適用されました。            |
| 400    | Bad Request            | パラメータが不足または無効（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized           | JWT トークンが無効または不足しています。      |
| 413    | Payload Too Large      | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error  | サーバーで予期しないエラーが発生しました。    |

## Translate Spreadsheet API の使用例

- **国際財務報告** – 四半期ごとの Excel レポートを、数式やチャートのレイアウトを維持したまま複数の言語に変換し、地域事務所向けに提供します。
- **多言語マーケティングダッシュボード** – グローバルチーム向けに、売上パフォーマンスダッシュボードのローカライズ版を自動生成します。
- **教育コンテンツの配布** – 異なる国の学生向けに、成績表、課題シート、カリキュラムスプレッドシートを翻訳し、手動でのコピー＆ペーストを省略します。
- **規制コンプライアンス** – 検証ルールとデータ検証リストを保持したまま、言語別コンプライアンススプレッドシートを生成します。

## なぜ Translate Spreadsheet API を使用すべきなのか？

- **AI による高精度** – 文脈を理解した高品質な言語変換のため、最先端のニューラル翻訳モデルを活用します。
- **レイアウトの変更なし** – セルの数式、条件付き書式、チャート、ワークシートの順序を、元のファイルと完全に一致させます。
- **1回の呼び出しでマルチシート処理** – シートごとのループ処理を必要とせず、リクエスト1回で全ワークシートを翻訳します。
- **クラウドとのシームレスな統合** – Aspose.Cells Cloud 認証と連携し、CI/CD、サーバーレス関数、エンタープライズバックエンドでの自動化パイプラインを実現します。

## SDK を使用した Translate Spreadsheet API の利用方法

### Translate Spreadsheet API の仕様

[Translate Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/TranslateSpreadsheet) は、Web ブラウザから REST 通信を直接実行するための公開可能なプログラミングインターフェースを提供します。

## Excel API SDK

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速に行え、短いコードでスプレッドシートを他のスプレッドシートにマージできます。  
Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。  
以下のコード例では、さまざまな SDK を使用して Aspose.Cells Web サービスと連携する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}