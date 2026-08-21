---
title: "Aspose.Cells Cloud Add Text API – 複数のExcelセルに一度にテキストを追加 – 接頭辞、接尾辞、ラベルの挿入"
second_title: "Document"
ArticleTitle: "Excel 用の一括テキスト挿入 – セルに接頭辞、接尾辞、カスタムテキストを追加 – ステップ・バイ・ステップガイド"
linktype: "AddText"
type: docs
url: /ja/add-text/
keywords: "Aspose Cells API, Excel にテキスト追加, 一括テキスト挿入, Excel の接頭辞・接尾辞, スプレッドシートのテキスト置換, Excel 自動化, クラウドスプレッドシート API"
description: "Aspose.Cells Cloud を使用して、一度の呼び出しで多数の Excel セルに接頭辞、接尾辞、またはカスタムラベルを挿入します。テキストの任意の位置（先頭、末尾、特定テキストの前または後）に挿入可能です。範囲、ワークシート、空セルの処理もサポートしています。"
weight: 100
---

一度の操作で複数の Excel セルにテキストを挿入します。Aspose.Cells API を使用して、セルの先頭、末尾、または特定のテキストの前後へ接頭辞、接尾辞、ラベル、またはカスタム文字を追加できます。

## 概要

対象範囲内のすべてのセルに対して、一度の呼び出しで接頭辞、接尾辞、または固定位置の文字列を一括挿入します。数式や補助列は不要です。

- 各セル内の**任意の位置**にカスタムテキストを挿入可能

| 値               | 説明                                                                 |
| ---------------- | -------------------------------------------------------------------- |
| `None`           | 元の内容を置き換えます                                               |
| `AtTheBeginning` | 先頭に挿入（接頭辞）                                                 |
| `AtTheEnd`       | 末尾に挿入（接尾辞）                                                 |
| `BeforeText`     | `selectText` の**最初の出現箇所の前**に挿入。見つからない場合はスキップ |
| `AfterText`      | `selectText` の**最初の出現箇所の後**に挿入。見つからない場合はスキップ |

- 4つの挿入モード：接頭辞、接尾辞、部分文字列の前または後
- 空白セルをスキップして不要な混雑を回避
- API は**文字列型の値のみ**を操作します。数値、ブール値、数式は事前にテキストに変換されます。
- **空セルの処理**
  - `skipEmptyCells = true` → 空白セルはスキップされます。
  - `skipEmptyCells = false` → 空白セルには挿入テキストが追加され、セルは文字列型になります。

- **アンカーが見つからない場合**：`position = BeforeText | AfterText` かつ `selectText` が**存在しない**場合、セルの値は変更されません。

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/add/text
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **AddText API のリクエストパラメータ**

| パラメータ名      | 型      | パス/クエリ文字列/HTTPボディ | 説明                                                                                                                                              | 必須 |
| :---------------- | :------ | :--------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ | :--- |
| Spreadsheet       | File    | FormData                     | 処理するスプレッドシートファイル。サポートされる形式は XLSX、XLS、ODS、CSV などです。                                                            | はい |
| text              | String  | Query                        | スプレッドシート内の指定されたセルに追加するテキスト内容。                                                                                       | はい |
| position          | String  | Query                        | 既存のセル内容に対してテキストを挿入する位置を指定します。オプション: `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`, `None`.         | はい |
| selectText        | String  | Query                        | _(オプション)_ 指定された場合、この部分文字列を含むセルにのみテキストが追加されます。`position` パラメータと併用します。                         | いいえ |
| skipEmptyCells    | Boolean | Query                        | `true` の場合、空のセルはスキップされます。`false` の場合、空のセルにもテキストが追加されます。                                                   | いいえ |
| worksheet         | String  | Query                        | _(オプション)_ テキストを追加するワークシート名。省略した場合、デフォルトで最初のワークシートが対象になります。                                  | いいえ |
| range             | String  | Query                        | _(オプション)_ テキストを追加するセル範囲（例: `"A1:C10"`）。省略した場合、指定されたワークシート内のすべての使用済みセルが対象になります。      | いいえ |
| outPath           | String  | Query                        | _(オプション)_ 処理済みワークブックを保存するクラウドストレージのフォルダーパス。省略した場合、ファイルは元のフォルダーに保存されます。         | いいえ |
| outStorageName    | String  | Query                        | 出力ファイルを保存するクラウドストレージの名前。                                                                                                 | いいえ |
| region            | String  | Query                        | _(オプション)_ 出力ファイルの数値、日付、通貨のロケールを設定します（例: `"en-US"`, `"zh-CN"`, `"de-DE"`）。                                      | いいえ |
| password          | String  | Query                        | _(オプション)_ アップロードしたスプレッドシートがパスワード保護されている場合、ファイルを開いて処理するためにパスワードを指定します。          | いいえ |

**cURL の例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/add/text?text=Report&position=AtTheBeginning&skipEmptyCells=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/workbook.xlsx" \
  -F "outPath=output/workbook_modified.xlsx"
```

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

### エラーコード

| コード | 説明 |
| ---- | ----------- |
| **400** Bad Request | 無効な Aspose.Cells Cloud API URI、または必須パラメータが不足しています。 |
| **401** Unauthorized | 無効なアクセストークン、または無効なクライアント ID およびシークレット。 |
| **404** Not Found | スプレッドシートファイルにアクセスできません。 |
| **500** Server Error | スプレッドシートの計算データ取得中に異常が発生しました。 |

## Add Text for Spreadsheet API の使用例

- **動的レポートラベル付け**: 自動生成された財務諸表や営業レポートに、動的なタイトル、日付タグ、メモを追加します。
- **バッチファイルへの透かし挿入**: 一括で Excel ファイルに会社ロゴ、機密性透かし、バージョン情報を追加します。
- **テンプレートデータ入力**: 契約書や請求書テンプレート内の指定された位置に、顧客名、金額その他のテキストを自動入力します。
- **データ分類タグ付け**: 分析結果に基づき、データ行に分類タグやステータスラベル（例: 「審査中」「承認済み」）を自動追加します。
- **データ品質注釈**: データクリーニング中に問題のあるデータにメモを追加します。
- **一括テキスト整形**: 製品名や顧客名に一貫して接頭辞や接尾辞を追加します。

## Add Text for Spreadsheet API を使用すべき理由

- **一括テキスト追加**: 数百のセルやファイルに一度にテキストを追加でき、手作業と比較して最大95％の時間を節約できます。
- **精密な位置制御**: セルの先頭、末尾、または特定テキストの前後など、6つの位置に正確にテキストを挿入可能。
- **インテリジェントな条件付き処理**: セルが空であるか、特定のテキストを含んでいるかに基づいてテキスト追加の有無を判断可能。
- **複数位置戦略サポート**:
  - `AtTheBeginning`: 選択したすべてのセルの内容の前に同じテキストを追加。
  - `AtTheEnd`: 選択したすべてのセルの内容の後にテキストを追加。
  - `BeforeText` / `AfterText`: 特定のテキストを含むセルのみの前または後にテキストを追加。
  - `None`: 元の内容を置き換えます。
- **精密な範囲制御**: 操作対象のワークシートやセル範囲を指定可能。
- **条件付きスキップ機能**: 空白セルをスキップして不要なテキスト追加を回避可能。
- **開発者向け設計**: Aspose.Cells Cloud は複数の言語向け SDK ライブラリを提供し、迅速な開発が可能です。また、包括的なドキュメントも整備されています。独自のチャート描画ソリューションを構築する場合と比較して、開発負荷を大幅に削減できます。
- **コスト効率**: ワークブックをアップロードせずにセル内にテキストを追加可能で、ストレージ領域を節約し、コストを削減できます。

## OpenAPI 仕様

[OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/AddText) はパブリックに利用可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

### Aspose.Cells Cloud SDK の使用

SDK を使用するのが開発を最速で進める方法です。SDK が下層の詳細を処理するため、最小限のコードでセルへのテキスト追加を実装できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddText.go" >}}
{{</tab>}}
{{< /tabs >}}
---