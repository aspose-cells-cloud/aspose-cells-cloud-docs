---
title: "テキスト分割 API – Excel セルを列に分割する | Aspose.Cells Cloud"
second_title: "ドキュメント"
ArticleTitle: "Excel テキスト分割ツール – セルの内容を複数の列に分割する | Aspose.Cells Cloud"
linktitle: "テキスト分割"
type: docs
url: /split-text/
keywords: "Aspose, Cells, テキスト分割 API, Excel, 区切り文字, テキスト分割, クラウド API"
description: "Aspose.Cells Cloud を使って Excel セルのテキストを簡単に別々の列または行に分割します。カスタム区切り文字、マスク、改行、およびオプションで区切り文字を保持することをサポートしています。curl または SDK を使って数分で使い始めましょう。"
weight: 100
---

カスタムの分割ルールを使って Excel セルのテキストを複数の列に分割します。Aspose.Cells Cloud のテキスト分割 Web API を使って、指定された範囲に区切り文字でコンテンツを分割して出力します。

## **導入**: テキスト分割

テキスト分割 API は、指定された区切り文字、パターン、または改行に基づいてセルの内容を複数のセルに分割し、結果をターゲット範囲に出力します。柔軟な分割方法、出力方向（列または行）、および区切り文字を保持するオプションをサポートしており、連結されたデータ、CSV 形式のコンテンツ、または複数行のテキストを構造化された形式に解析するのに最適です。

- **特定の文字でセルを分割** – 任意の文字（コンマ、スペース、セミコロンなど）を区切り文字として選択し、セルの内容を複数のセルに分割します。
- **文字列でセルを分割** – 指定した任意の文字の組み合わせでセルを分割します。
- **マスクでテキストを分割** – ワイルドカードを使用して特定のパターンに基づいてテキストを分割し、より柔軟で強力なテキスト分割方法を提供します。
- **改行でセルの内容を分割** – 改行で分割して、より整理された表示を実現します。
- **列または行にセルを分割** – 分割結果を連続する列または行に書き込むかどうかを選択します。
- **区切り文字の削除または保持** – 結果のセルで区切り文字を削除するか、先頭または末尾に保持するかを決定します。

## **SplitText API**

**前提条件**: この API を使用するには、有効な Aspose Cloud アクセストークンが必要です。また、処理対象のワークブックは Aspose Cloud ストレージにアップロード済みであるか、リクエスト内で直接提供する必要があります。この API は、XLSX、XLS、ODS、CSV などの一般的なスプレッドシート形式をサポートしています。

### Web API

```http
POST https://api.aspose.cloud/v4.0/cells/content/split/text
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

```bash
-H "Authorization: Bearer {access_token}"
```

### **splitText** API のリクエストパラメータ

| パラメータ名                     | 型      | 位置       | 必須? | デフォルト       | 説明                                                                                                                                                   |
| ------------------------------ | ------- | -------- | --- | -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet                    | ファイル  | FormData   | はい  | —              | 処理対象のスプレッドシートファイル。サポートされる形式は XLSX、XLS、ODS、CSV などです。                                                                   |
| delimiters                     | 文字列   | クエリ      | いいえ | —              | セル内のテキストを分割するために使用する1つまたは複数の区切り文字（例：`","`、`";"`、`Space`、`LineBreak`、`Tab`、`Pipe`、`Custom`）。               |
| keepDelimitersInResultingCells | 真偽値   | クエリ      | いいえ | false          | `true` の場合、結果として得られる分割されたセルに区切り文字を保持します。                                                                             |
| keepDelimitersPosition         | 文字列   | クエリ      | いいえ | None           | `keepDelimitersInResultingCells` が `true` の場合に区切り文字を保持する位置。オプション: `None`、`AtTheBeginning`、`AtTheEnd`、`BeforeText`、`AfterText`。 |
| howToSplit                     | 文字列   | クエリ      | いいえ | SplitToColumns | テキスト分割方法。オプション: `None`、`SplitToColumns`、`SplitToRows`。                                                                               |
| outPositionRange               | 文字列   | クエリ      | はい  | —              | 分割結果を書き込むターゲット範囲（例：`"D1:F10"`）。                                                                                                   |
| worksheet                      | 文字列   | クエリ      | いいえ | —              | テキスト分割を適用するワークシートの名前。省略した場合、最初のワークシートが使用されます。                                                             |
| range                          | 文字列   | クエリ      | いいえ | —              | 分割操作を適用するソースセル範囲（例：`"A1:A10"`）。省略した場合、ワークシートのすべての使用済みセルが処理されます。                                    |
| outPath                        | 文字列   | クエリ      | いいえ | —              | 処理済みのワークブックを保存するクラウドストレージのフォルダーパス。省略した場合、ファイルはソースフォルダーに保存されます。                           |
| outStorageName                 | 文字列   | クエリ      | いいえ | —              | 出力ファイルを保存するクラウドストレージの名前。                                                                                                      |
| region                         | 文字列   | クエリ      | いいえ | —              | テキスト分割のロケール。区切り文字の解釈や文字エンコーディングに影響を与える可能性があります（例：`"en-US"`、`"ja-JP"`）。                              |
| password                       | 文字列   | クエリ      | いいえ | —              | パスワード保護されたスプレッドシートを開くためのパスワード。                                                                                          |

### **応答**

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

- **400 Bad Request（不正なリクエスト）** – 無効な Aspose.Cells Cloud API URI または不正な形式のパラメータ。
- **401 Unauthorized（未認証）** – アクセストークン（または client-id/secret）が不足しているか、無効です。
- **404 Not Found（見つかりません）** – 指定されたスプレッドシートファイルにアクセスできませんでした。
- **500 Server Error（サーバーエラー）** – スプレッドシートの内部処理中に異常が発生しました。

## Split Text API の使用例

### **CSV およびテキストファイルのインポートクリーンアップ**

外部システムからデータをインポートする際、フィールドが単一セルに連結されることがよくあります。

- **ERP/CRM データインポート** – `"John Doe;johndoe@email.com;555-1234"` を名前、メールアドレス、電話番号の別々の列に分割します。
- **データベースエクスポート** – `"ORD-2024-001|Premium|Express"` のような連結されたキーを注文 ID、ティア、配送方法に解析します。
- **ログファイル解析** – `"2024-01-15 10:30:00|ERROR|ConnectionTimeout"` のような半構造化ログを分割してフィルタリングします。

### **レガシーシステムの移行**

- 古いシステムでは複数値のフィールドが単一セルにダンプされるため、新しいデータベーススキーマに合わせて分割します。
- フラットファイルエクスポートを正規化された Excel テーブルに変換し、Power BI または Tableau で使用できるようにします。

### **データのクリーニングと標準化**

- **区切り文字の正規化** – 混在区切り文字（`"A,B;C|D"`）を複数の区切り文字分割で統一された形式に変換します。
- **空白のクリーニング** – スペースで分割して、単語間の余分なスペースを特定し、削除します。
- **財務データ** – `"DEP-CHK-3847"` のような連結された取引コードを取引タイプ、ソース、参照に分割します。
- **医療記録** – `"Smith,Jane_F_1985"` のような患者データを姓、名、性別、生年を解析します。

## Split Text API を使用すべき理由

- **特定の文字** – コンマ、セミコロン、タブ、スペースなど、任意の1文字で分割します。
- **文字列の組み合わせ** – `||`、`->`、またはカスタムセパレータなど、複数文字の区切り文字を使用します。
- **改行** – 複数行のセル（住所、コメント、説明など）を別々の行に即座に解析します。
- **カスタム区切り文字** – 独自のデータフォーマット用に任意の文字の組み合わせを区切り文字として定義します。
- **開発者フレンドリー** – Aspose.Cells Cloud は複数の言語で SDK ライブラリを提供しており、迅速な開発が可能です。また、包括的なドキュメントも用意されています。カスタムソリューションを構築する場合と比較して、開発作業を大幅に削減できます。
- **コスト効率** – ワークブックを事前にアップロードせずに重複する文字を削除できるため、ストレージ容量を節約し、コストを削減できます。

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/SplitText) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

### Aspose.Cells Cloud SDK の使用

SDK を使用するのは、開発を高速化する最良の方法です。SDK は底层の詳細を処理し、最小限のコードでセルのテキスト分割を実装できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitText.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitText.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitText.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitText.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitText.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitText.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitText.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitText.go" >}}  
{{</tab>}}  
{{< /tabs >}}