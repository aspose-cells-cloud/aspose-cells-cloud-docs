---
title: "Aspose.Cells Cloud Web API – AIを活用したテキストファイルの翻訳"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud AI 翻訳 API を使用してテキストファイルを翻訳する方法"
linktitle: "テキストファイルの翻訳"
type: docs
url: /ja/translate-text-file/
keywords: "Aspose.Cells, Cloud API, AI 翻訳, テキストファイルの翻訳, 多言語変換, REST PUT, 対象言語コード, ファイルアップロード翻訳, 生テキスト翻訳, スプレッドシート AI"
description: "Aspose.Cells Cloud AI の TranslateTextFile エンドポイントを使用して、テキストファイルをサポートされている任意の言語に変換する方法を学びましょう。multipart ファイルアップロードと生テキストペイロードの両方をサポートし、書式を保持したまま翻訳済みファイルをダウンロード可能に返却します。"
weight: 100
---

**TranslateTextFile** エンドポイントは、Aspose.Cells Cloud AI サービスを活用し、テキストファイルの内容を指定された対象言語に翻訳します。このエンドポイントは以下の2つの操作モードをサポートします：（1）**ファイルアップロードモード** – multipart/form-data 経由でテキストファイルを送信し、翻訳済みファイルを受信；（2）**直接コンテンツモード** – リクエストボディに生テキストを投稿し、翻訳済みテキストを直接取得。このサービスは元の改行や書式を保持し、ファイル名の末尾に自動的に "_translated" サフィックスを付加し、結果をダウンロード可能なストリームとして返却します。ドキュメントの一括翻訳、多言語ワークフローへの統合、ユーザー生成コンテンツのオンザフライ翻訳などに最適です。

## **テキストファイル翻訳 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/text-file
```

### **リクエストパラメータ:**

| パラメータ名   | 型     | 位置       | 必須/任意 | 説明                                                                                                                                                                                                 |
| :------------- | :----- | :--------- | :-------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | ファイル | 必須       | FormData  | 翻訳対象のソーステキストファイル。プレインテキスト (.txt) またはサポートされているスプレッドシート形式である必要があります。例: multipart/form-data の "file" フィールドに `document.txt` をアップロード。 |
| targetLanguage | 文字列 | 必須       | クエリ    | 目的の出力言語の ISO-639-1 言語コード（例: スペイン語 "es"、フランス語 "fr"、ドイツ語 "de"）。コードは大文字・小文字を区別しません。                                                                      |
| region         | 文字列 | 任意       | クエリ    | スプレッドシートの地域識別子で、日付・数値・通貨などのロケール固有の書式に影響します。一般的な値: "US", "EU", "CN"。省略された場合、ワークブックの元の地域設定が使用されます。                           |
| password       | 文字列 | 任意       | クエリ    | 暗号化されたスプレッドシートファイルを開くために必要なパスワード。プレインテキストファイルには不要です。                                                                                              |

### **レスポンス**

成功レスポンス (200 OK)
ヘッダー:
Content-Type: application/octet-stream // 翻訳済みファイルのバイナリストリーム
Content-Disposition: attachment; filename="<original_name>\_translated.txt"
Content-Length: <サイズ（バイト単位）>

ボディ: 生テキストの翻訳結果を含むバイナリストリーム（元の改行・書式を保持）。

**HTTP ステータスコード**

| コード | 意味             | 説明                                                 |
| ------ | ---------------- | ---------------------------------------------------- |
| 200    | OK               | 操作が正常に適用されました。レスポンスには詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足または不正です（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized     | JWT トークンが無効または不足しています。             |
| 413    | Payload Too Large| アップロードされたファイルがサイズ上限を超えています。 |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。             |

## どこでテキストファイル翻訳 API を使用すべきか？

- **多言語ドキュメントポータル** – ユーザーマニュアルやヘルプファイルをテキストドキュメントとしてアップロードし、オンデマンドでローカライズ版を提供。
- **コンテンツ管理システム (CMS)** – CMS のワークフローに統合し、国際向けに公開する前にブログ記事や記事を翻訳。
- **エンタープライズデータパイプライン** – 大量の CSV/TXT レポートをバッチ処理し、地域オフィスの言語に翻訳しながら元の書式を維持。
- **カスタマーサポートプラットフォーム** – 異なる言語のサポートエージェントを支援するため、受信したプレインテキストのチケットやチャットログをリアルタイムで翻訳。

## なぜテキストファイル翻訳 API を使用すべきか？

- **AI ドリブンの高精度** – 先進的なニューラル翻訳モデルを活用し、自然で文脈に応じた翻訳を実現。
- **双方向入力の柔軟性** – ファイルアップロードと生テキストペイロードの両方をサポートし、多様なクライアントアプリケーションへの統合を簡素化。
- **元のレイアウト保持** – 改行・インデント・特殊文字を保持し、翻訳後の手動修正を不要に。
- **シームレスなファイル取り扱い** – 自動生成された "_translated" サフィックス付きでダウンロード可能なファイルを返却し、クライアントサイドコードの複雑さを削減。

## SDK を使用したテキストファイル翻訳 API の利用方法

### テキストファイル翻訳 API 仕様

[テキストファイル翻訳 API 仕様](https://reference.aspose.cloud/cells/#/AIController/TranslateTextFile) は、Web ブラウザから直接 REST アクセスを実行するための公開可能なプログラミングインターフェースを提供します。

## Excel API SDK

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速になります。スプレッドシートを他のスプレッドシートに結合するコードも短く済みます。
Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。
以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスと連携する方法を示しています：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateTextFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateTextFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateTextFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateTextFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateTextFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateTextFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateTextFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateTextFile.go" >}}
{{</tab>}}
{{< /tabs >}}