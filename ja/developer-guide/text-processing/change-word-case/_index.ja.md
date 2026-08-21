---
title: "Aspose.Cells Cloud – 単語のケース変換（大文字、小文字、固有名詞、文頭大文字）"
ArticleTitle: "Excel ケースコンバーター – 大文字、小文字、固有名詞ケース、文頭大文字"
linktype: "Word Case"
type: docs
url: /ja/change-word-case/
keywords: "単語ケース変換 API、Aspose.Cells、Excel ケース変換、大文字、小文字、固有名詞ケース、文頭大文字、テキスト書式設定"
description: "Aspose.Cells Cloud API を使用して Excel ファイル内のテキストケースを簡単に変換します。大文字、小文字、固有名詞ケース、文頭大文字をサポート。C#、Java、Python などのコードサンプルを入手できます。"
weight: 100
---

## **単語のケース変換**

Aspose.Cells Cloud Web API を使用して、スプレッドシート内のテキストケースを即座に変換します。選択した範囲で、大文字、小文字、固有名詞ケース（各単語の先頭文字を大文字）、文頭大文字（各文の先頭文字を大文字）に切り替え可能です。文字列セルのみが影響を受け、数値、論理値、エラー、空白は無視されます。数式、書式、データ検証は変更されません。

- **UpperCase（大文字）** – すべての文字を大文字に変換します。
- **LowerCase（小文字）** – すべての文字を小文字に変換します。
- **ProperCase（固有名詞ケース）** – 各単語の先頭文字を大文字に、残りを小文字に変換します。
- **SentenceCase（文頭大文字）** – 各文の先頭文字を大文字に、残りを小文字に変換します。

<img src="images/result.png" alt="ケース変換前後のスクリーンショット" width="800" height="450" />

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/wordcase
```


### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```
### **UpdateWordCase** API のリクエストパラメータ

| パラメータ名      | 型     | 位置       | 説明                                                                                                                                                   |
| :---------------- | :----- | :--------- | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet       | File   | FormData   | 処理対象のスプレッドシートファイル。サポートされる形式には XLSX、XLS、ODS、CSV などがあります。                                                        |
| wordCaseType      | String | Query      | テキストケース変換のタイプを指定します。`UpperCase`、`LowerCase`、`ProperCase`、`SentenceCase` のいずれかを設定します。                               |
| worksheet         | String | Query      | _(オプション)_ ケース変換を適用するワークシートの名前。指定しない場合、ブックの最初のワークシートに処理が適用されます。                                |
| range             | String | Query      | _(オプション)_ ケース変換を適用するセル範囲（例：`"A1:C10"`）。指定しない場合、指定されたワークシートのすべての使用済みセルに処理が適用されます。        |
| outPath           | String | Query      | _(オプション)_ 処理済みのブックが保存されるクラウドストレージのフォルダーパス。指定しない場合、ファイルは元のフォルダーに保存されます。                |
| outStorageName    | String | Query      | 出力ファイルが保存されるクラウドストレージの名前。                                                                                                     |
| region            | String | Query      | _(オプション)_ テキストケース変換ルール用のロケールを設定します。言語固有の大文字変換規則（例：`"en-US"`、`"tr-TR"`）に特に関係します。                   |
| password          | String | Query      | _(オプション)_ アップロードされたスプレッドシートがパスワードで保護されている場合、ファイルを開いて処理するためのパスワードを指定します。               |

### レスポンス

成功した場合、サービスは **200 OK**（または **202 Accepted**）を返し、処理済みブックのバイナリストリームを含む JSON ペイロードを返します。

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

### エラーコード

- **400 Bad Request** – 無効な Aspose.Cells Cloud API URI。
- **401 Unauthorized** – 無効なアクセストークン、または誤ったクライアント認証情報。
- **404 Not Found** – スプレッドシートファイルにアクセスできません。
- **500 Server Error** – スプレッドシートの内部処理で異常が発生しました。

## 単語ケース変換 API を使用するべき場所はどこですか？

### データのクリーニングと標準化

- **顧客データ管理** – 顧客名や住所情報の大文字・小文字を標準化します（例：`john doe` → `John Doe`）。
- **製品カタログ処理** – 製品タイトルや説明テキストの大文字・小文字を標準化します（例：`IPHONE 15 PRO` → `iPhone 15 Pro`）。
- **財務レポート生成** – 財務諸表における項目名および説明フィールドを正規化します。

### 複数ソースデータの統合

- **データウェアハウス ETL** – 異なるシステムからデータをロードする際にテキスト形式を標準化します。
- **API データ受信** – 外部 API から返される、一貫性のない大文字・小文字を持つデータを処理します。
- **部署間データ統合** – 異なる部署からの Excel レポートのテキスト形式を標準化します。

### コンテンツ管理システム

- **自動ニュースリリース** – ニュース見出しとコンテンツ（見出しの大文字規則）を自動的に書式設定します。
- **製品ドキュメント生成** – 技術ドキュメント用語の書式を統一します。
- **ナレッジベース管理** – FAQ およびヘルプドキュメントのテキスト形式を標準化します。

### エンタープライズアプリケーション統合

- **CRM システム統合** – 顧客データのインポート/エクスポート時に名前や会社情報を自動的に書式設定します。
- **ERP データ処理** – 材料説明や仕入先名などの重要なフィールドを標準化します。
- **人事管理システム** – 従業員情報や職種を標準化します。

### バッチドキュメント処理

- **法的ドキュメント作成** – 契約や合意書の条項フォーマットをバッチ処理します。
- **マーケティング資料生成** – 広告コピーやメールテンプレートのテキスト形式を標準化します。
- **学術論文書式設定** – 参照およびタイトルの書式要件を標準化します。

### リアルタイムデータ処理

- **ユーザー入力検証** – ユーザーが送信したフォームデータをリアルタイムで書式設定します。
- **チャットボット応答** – 自動生成された応答のテキスト形式を標準化します。
- **インスタントレポート生成** – 一貫した書式のビジネスレポートを動的に生成します。

### 国際化とローカリゼーション

- **多言語データ処理** – 各言語のテキストにおける大文字規則の違いに対応します。
- **ローカライズコンテンツ準備** – 地域ごとのフォーマット済みローカルコンテンツを準備します。
- **翻訳プロジェクト管理** – 翻訳前後のテキスト形式を統一します。

## なぜ単語ケース変換 API を使用すべきですか？

- **開発者フレンドリー** – Aspose.Cells Cloud は複数言語の SDK ライブラリを提供しており、迅速な開発と包括的なドキュメントが可能です。カスタムソリューションを構築する場合と比較して、開発作業量を大幅に削減できます。
- **コスト効率** – ブックをアップロードせずに単語ケースを変更できるため、ストレージ容量を節約し、コストを削減できます。

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できます。

### Aspose.Cells Cloud SDK の使用

SDK を使用するのが開発を加速する最良の方法です。SDK は内部の詳細を処理し、最小限のコードでセルの **UpdateWordCase** を実装できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UpdateWordCase.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UpdateWordCase.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UpdateWordCase.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UpdateWordCase.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UpdateWordCase.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UpdateWordCase.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UpdateWordCase.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UpdateWordCase.go" >}}
{{</tab>}}
{{< /tabs >}}
---