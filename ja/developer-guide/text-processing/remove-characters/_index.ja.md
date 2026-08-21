---
title: "Aspose.Cells Cloud Remove Characters Web API – Excel からカスタム文字と部分文字列を削除（オンライン・ショートコード）"
second_title: "ドキュメント"
ArticleTitle: "Excelテキストクリーナー – 選択範囲から文字と部分文字列を削除"
linktype: "docs"
url: /remove-characters/ja/
keywords: "Aspose.Cells, 文字削除, Excel API, テキストクリーニング, スプレッドシート"
description: "選択範囲内のExcelセルからカスタム文字、文字セット、および部分文字列を削除します。Aspose.Cells API を使用して、特定の位置のテキストを削除し、正確なデータクリーニングを実現します。"
weight: 100
---

選択したセル範囲からカスタム文字、文字セット、または部分文字列を削除して、Excelデータをクリーンアップします。Aspose.Cells API を使用して、正確なデータ整形のために特定の位置のテキストを削除します。

## はじめに

特定の不要な文字を削除して、Excelデータを簡単にクリーンアップ・標準化します。このアドインでは、セルのサニタイズ（クリーニング）を実行するための複数のターゲット指向手法が用意されています。

- **カスタム文字の削除**  
  定義した特定の記号を削除します。単純に各文字をフィールドに入力するだけで、アドインが選択したセル内にあるその文字のすべてのインスタンスを即座に削除します。固有の区切り文字、タイプミス、特殊マークの除去に最適です。

- **文字セットの削除（一括クリーニング）**
  - **非表示文字** – 分析や書式設定を妨げる不可視文字（改行、復帰、タブ、およびその他の制御文字：ASCII 0‑31、127、129、141、143、144、157）をデータから削除します。
  - **テキスト文字（すべての文字）** – 選択範囲からすべての文字（A‑Z、a‑z）を削除し、数字と記号だけを残します。
  - **数字文字（すべての数字）** – すべての数字（0‑9）を削除して純粋なテキストを抽出します。製品名やテキスト説明のクリーニングに最適です。
  - **記号** – 数学記号（±、√など）、幾何記号（∆、°など）、技術用記号、通貨記号（£、¢など）、および文字に似た記号（™、®、©など）を含む多様な記号類を削除します。
  - **句読点** – 句読点（ピリオド、コンマ、引用符、ハイフンなど）をすべて削除し、句読点のないクリーンなテキストを取得します。

- **特定の部分文字列の削除**  
  単一文字にとどまらず、単語全体や特定の文字列を削除します。データセットから共通の接頭辞、接尾辞、または冗長なテキストフレーズを簡単に削除できます。

**バージョン 4.0 – 更新日：2024‑11‑15**

## RemoveCharacters API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベース認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### リクエストパラメータ

| パラメータ名        | 型     | 位置                | 説明                                                                                                                                                                                                                      |
| ------------------- | ------ | ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet         | File   | FormData            | 処理対象のスプレッドシートファイル。対応フォーマット：XLSX、XLS、ODS、CSV など。                                                                                                                                         |
| removeTextMethod    | String | Query               | テキスト削除方法を指定します。オプション：`None`、`RemoveCustomCharacter`、`RemoveCharacterSets`、`RemoveSubString`。デフォルトは `None`。                                                                                 |
| characterSets       | String | Query               | `RemoveCharacterSets` を選択した場合に削除する事前定義された文字セット。オプション：`NonPrintingCharacters`、`TextCharacters`、`NumericCharacters`、`Symbols`、`PunctuationMarks`。複数設定可（カンマ区切り）。             |
| removeCustomValue   | String | Query               | `RemoveCustomCharacter` または `RemoveSubString` 使用時に削除するカスタム文字または部分文字列。                                                                                                                           |
| worksheet           | String | Query _(オプション)_ | テキスト削除を適用するワークシート名。**省略した場合、ワークブックの最初のワークシートが処理されます。**                                                                                                                   |
| range               | String | Query _(オプション)_ | テキスト削除を適用するセル範囲（例：`"A1:C10"`）。**省略した場合、指定されたワークシートのすべての使用セルに適用されます。**                                                                                               |
| outPath             | String | Query _(オプション)_ | 処理済みワークブックを保存するクラウドストレージのフォルダーパス。省略した場合、ファイルは元のフォルダーに保存されます。                                                                                                  |
| outStorageName      | String | Query _(オプション)_ | 出力ファイルを保存するクラウドストレージ名。                                                                                                                                                                              |
| region              | String | Query _(オプション)_ | 文字セット定義のロケールを設定します（例：`"en-US"`、`"ja-JP"`）。                                                                                                                                                         |
| password            | String | Query _(オプション)_ | 保護されたワークブックの場合に必要なパスワード。                                                                                                                                                                          |

### レスポンス

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
- **401 Unauthorized** – 無効なアクセス・トークン、または誤ったクライアントID・シークレット。
- **404 Not Found** – スプレッドシートファイルにアクセスできません。
- **500 Server Error** – スプレッドシートの計算データ取得中に異常が発生しました。

## Remove Characters API の使用例

- **データのインポート／エクスポート** – インポートしたCSV/データをクリーニングし、不可視文字や書式エラーを削除します。
- **データベース管理** – 不要な記号や句読点を削除して、製品コード、ID、名前を標準化します。
- **財務分析** – 通貨記号やテキスト文字を削除し、純粋な数値を抽出します。
- **テキスト処理** – 行区切りやタブを削除し、クリーンなテキスト分析とレポートを実現します。
- **在庫管理** – 冗長な接頭辞や接尾辞を削除して製品名をクリーニングします。

## Remove Characters API の利点

- **時間節約** – 手動クリーニングに代わって、複数の文字タイプを一括で瞬時に削除できます。
- **正確性の確保** – 分析エラーや書式問題の原因となる不可視文字を排除します。
- **データ標準化** – データセットやシステム全体で一貫した書式を実現します。
- **分析の改善** – 数値やテキストを必要な形で分離し、分析に適したクリーンなデータを取得します。
- **インポートエラーの修正** – データベースや数式を破壊する問題のある文字を削除します。
- **開発者向け** – Aspose.Cells Cloud は複数言語の SDK ライブラリを提供し、包括的なドキュメントにより迅速な開発を可能にします。カスタムソリューションの構築と比較し、開発工数を大幅に削減します。
- **コスト効率** – ワークブックを事前アップロードせずに文字削除が可能で、ストレージ容量を節約し、コストを削減します。

## OpenAPI スペック

[OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharacters) はパブリックに利用可能なプログラミング・インタフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

### Aspose.Cells Cloud SDK の使用

SDK を使用することで、開発スピードを最大化できます。SDK が下層の詳細を処理するため、**文字削除**機能をセルに実装する際に最小限のコードで済みます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells Web サービスを呼び出す方法を示しています：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}