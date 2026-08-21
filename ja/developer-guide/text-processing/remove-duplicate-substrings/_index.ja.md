---
title: "Aspose.Cells Cloud 重複する部分文字列を削除する Web API — Excel の重複テキストを解消"
second_title: "ドキュメント"
ArticleTitle: "Excel 重複部分文字列削除ツール — セル内の重複テキストをクリーンアップ"
linktitle: "重複する部分文字列を削除"
type: docs
url: /ja/remove-duplicate-substrings/
keywords: "Aspose.Cells, 重複部分文字列, Excel API, テキストクリーニング, クラウド"
description: "Aspose.Cells Cloud API を使用して Excel セルから重複する部分文字列を削除し、書式設定や検証を維持します。"
weight: 100
---

Excel セル内の重複する部分文字列を、インテリジェントな検出で削除します。Aspose.Cells の重複排除 API を使用して、元の書式設定を維持したまま冗長なテキストを削除します。

## **はじめに**：不要な文字を正確に削除

重複部分文字列クリーナー API は、Excel 範囲内の各セル内にある重複する部分文字列を削除し、セルの書式設定、データ検証、その他のワークブック構造を維持します。各セルを独立して処理し、重複する部分文字列の最初の出現のみを残します。

### **データソースオプション**

| フィールド名   | タイプ | 必須 | 説明                                             |
| -------------- | ------ | ---- | ------------------------------------------------ |
| `workbook`     | ファイル | はい  | Excel ワークブックファイル (.xlsx, .xlsm)       |
| `range`        | 文字列 | はい  | 処理対象の範囲（例: "A1:D100"、"Sheet1!A:D"） |

### **区切り文字オプション**

| フィールド名                         | タイプ    | デフォルト値 | 説明                                                                                                                                                      |
| ------------------------------------ | --------- | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delimiters`                         | 文字列    | `"preset"`   | オプション: `preset`（事前設定）, `custom`（カスタム）, `comma`（コンマ）, `semicolon`（セミコロン）, `space`（スペース）, `tab`（タブ）, `line-break`（改行）、またはカスタム区切り文字文字列（複数文字は複合区切り文字として扱われる） |
| `treatConsecutiveDelimitersAsOne`   | 真偽値   | `false`      | 隣接する区切り文字を 1 つにまとめます                                                                                                                      |
| `caseSensitive`                     | 真偽値   | `false`      | 比較を大文字・小文字を区別するかどうかを指定します。`false` の場合、重複検出時に大文字・小文字が無視されます。                                              |

## **RemoveDuplicateSubstrings API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **RemoveDuplicateSubstrings API のリクエストパラメーター**

| パラメーター名                  | タイプ    | パス／クエリ文字列／HTTP ボディ | 説明                                                                                                                                                                       |
| :------------------------------ | :-------- | :------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet                     | ファイル   | FormData                        | 処理対象のスプレッドシートファイル。サポートされるフォーマットには、XLSX、XLS、ODS、CSV などがあります。                                                                    |
| delimiters                      | 文字列     | クエリ                          | セル内容を部分文字列に分割し、重複検出および削除するために使用する 1 つ以上の区切り文字を指定します。複数の区切り文字を指定可能（例: `",;"`）。                               |
| treatConsecutiveDelimitersAsOne | 真偽値    | クエリ                          | `true` の場合、連続する区切り文字は 1 つの区切りとして扱われます。`false` の場合、各区切り文字が個別に処理されます。                                                        |
| caseSensitive                   | 真偽値    | クエリ                          | `true` の場合、重複検出では大文字・小文字が考慮されます（例: "Text" ≠ "text"）。`false` の場合、重複比較時に大文字・小文字は無視されます。                                    |
| worksheet                       | 文字列     | クエリ                          | （オプション）重複部分文字列の削除を適用するワークシート名。省略した場合、操作は最初のワークシートに適用されます。                                                           |
| range                           | 文字列     | クエリ                          | （オプション）重複部分文字列の削除を適用するセル範囲（例: `"A1:C10"`）。省略した場合、操作は指定されたワークシート内のすべての使用済みセルに適用されます。                    |
| outPath                         | 文字列     | クエリ                          | （オプション）処理済みワークブックを保存するクラウドストレージフォルダーパス。省略した場合、ファイルはソースフォルダーに保存されます。                                     |
| outStorageName                  | 文字列     | クエリ                          | 出力ファイルを保存するクラウドストレージの名前。                                                                                                                           |
| region                          | 文字列     | クエリ                          | （オプション）テキスト処理用のロケールを設定します。これにより、言語によっては区切り文字の解釈や大文字・小文字の区別ルールに影響を与える可能性があります（例: `"en-US"`、`"tr-TR"`）。 |
| password                        | 文字列     | クエリ                          | （オプション）アップロードされたスプレッドシートがパスワードで保護されている場合、ファイルを開いて処理するためにパスワードを指定します。                                   |

**リクエスト例（cURL）**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&caseSensitive=false" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx" \
     -F "range=A1:D100"
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

### **ステータスコード**

| コード | 意味               | 説明                                                                                   |
|------|--------------------|----------------------------------------------------------------------------------------|
| 200  | OK                 | リクエストは成功し、処理済みのワークブックが返されます。                               |
| 202  | Accepted           | リクエストは非同期処理のために受理されました。                                         |
| 400  | Bad Request        | リクエストが不正な形式であるか、無効なパラメーターを含んでいます。                      |
| 401  | Unauthorized       | 認証に失敗したか、トークンが不足または無効です。                                        |
| 404  | Not Found          | 指定されたワークブックまたはリソースが見つかりません。                                 |
| 500  | Internal Server Error | サーバー側で予期せぬエラーが発生しました。                                              |

## 重複部分文字列削除 API の使用例

- **データクリーニング・標準化**: `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"` のようにタグをクリーンアップ
- **技術・運用データ**: 重複するエラーコードのクリーンアップ、重複する/bin/ラック識別子の削除など
- **コンテンツ・メディア管理**: スキルタグの重複排除、冗長な資格情報エントリの削除

## なぜ重複部分文字列削除 API を使用すべきなのか

- **手動タスクの自動化**: 面倒な編集を排除し、人的エラーを削減します。
- **データ整合性の維持**: セルの色、フォント、罫線、条件付き書式は変更されず、ドロップダウンリストや検証ルールも維持されます。
- **柔軟な処理**: 区切り文字に依存せず、オプションで大文字・小文字の区別制御やヘッダー保護が可能です。
- **開発者フレンドリー**: Aspose.Cells Cloud は複数の言語用の SDK ライブラリを提供し、包括的なドキュメントにより迅速な開発を実現します。
- **コスト効率**: 処理はクラウド上で実行されるため、中間ファイルをローカルに保存する必要がありません。

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings) はパブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できます。

### Aspose.Cells Cloud SDK を使用

SDK を使用すると、開発を最適化できます。SDK は内部の詳細を処理し、最小限のコードでセルの重複部分文字列削除機能を実装できます。Aspose.Cells Cloud SDK の完全な一覧は、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

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
---