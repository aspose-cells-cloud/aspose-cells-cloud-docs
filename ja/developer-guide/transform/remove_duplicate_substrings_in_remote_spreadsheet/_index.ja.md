---
title: "リモートスプレッドシート内の重複する部分文字列を削除する"
ArticleTitle: "リモートスプレッドシート内の重複する部分文字列を削除する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktype: "Remove Duplicate Substrings In Remote Spreadsheet"
type: docs
url: /ja/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
aliases: []
keywords: "Aspose.Cells, 重複する部分文字列の削除, API"
description: "ワークブック内の指定された範囲のセル内にある繰り返し部分文字列を検出し、削除するためのAPIです。"
weight: 1
---

## Aspose.Cells Cloud Web サービスによるリモートスプレッドシート内の重複する部分文字列の削除

選択された範囲内の各セルにある繰り返し部分文字列を、ユーザー定義または事前設定された区切り文字を使って検出し、削除します。この処理では、数式、書式設定、データ検証は保持されます。

**重複の検出方法**  
1. 各セルの値は、選択された区切り文字で部分文字列に分割されます。  
2. 本ツールは、**同じセル内**の部分文字列を比較し、重複する文字列のうち**最初の出現のみ**を保持します。  
3. クリーンされた部分文字列を同じ区切り文字で再結合し、セルに書き戻します。  

**区切り文字のオプション**  
- 事前設定リスト：コンマ、セミコロン、スペース、タブ、改行  
- `Custom`（カスタム）– 任意の文字（複数可）を入力可能；複数文字は1つの複合区切り文字として扱われます  
- `TreatConsecutiveDelimitersAsOne`（連続する区切り文字を1つとして扱う）– 隣接する区切り文字を1つの区切り文字として圧縮します  

文字列型のセルのみ処理されます。数値、ブール値、数式は文字列に変換された上で分割処理されます（数式は削除されます）。処理結果として、クリーンされたセル数と更新されたワークブックストリームを返します。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | タイプ | Path/Query String/HTTP Body | 説明 |
|----------------|---------|-----------------------------|-------------|
| name | string | Path | （必須）取得するワークブックファイルの名前。 |
| worksheet | string | Path | スプレッドシートのワークシートを指定します。 |
| range | string | Path | スプレッドシートのワークシート範囲を指定します。 |
| delimiters | string | Query | セル値を分割するために使用する区切り文字（例：コンマ、セミコロン、スペース、タブ、改行）。必須。 |
| treatConsecutiveDelimitersAsOne | boolean | Query | 隣接する区切り文字を1つの区切り文字として圧縮するかどうか。既定値：true。オプション。 |
| caseSensitive | boolean | Query | 重複検出時に大文字・小文字を区別して比較するかどうか。オプション。 |
| folder | string | Query | （オプション）ワークブックが保存されているフォルダのパス。既定値：null。 |
| storageName | string | Query | （オプション）カスタムクラウドストレージを使用する場合のストレージ名。 |
| region | string | Query | スプレッドシートの地域/言語設定（例：`en-US`, `fr-FR`）。オプション。 |
| password | string | Query | スプレッドシートファイルを開くためのパスワード。オプション。 |

### リクエストボディパラメータ

| パラメータ名 | タイプ | 説明 |
| -------------- | ---- | ----------- |
| - | - | この操作にはリクエストボディは不要です。 |

### **レスポンス**

```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-encoded workbook stream"
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|------|---------|-------------|
| 200 | OK | 処理が成功し、クリーンされたセル数と更新されたワークブックストリームが返されます。 |
| 400 | Bad Request | 1つ以上のリクエストパラメータが不足しているか、無効です。 |
| 401 | Unauthorized | 認証に失敗したか、JWT トークンが不足しているか無効です。 |
| 413 | Payload Too Large | リクエストが許容サイズ制限を超過しています。 |
| 500 | Internal Server Error | サーバー上で予期しないエラーが発生しました。 |

## SDK を使用したリモートスプレッドシート内の重複する部分文字列の削除の使い方

### リモートスプレッドシート内の重複する部分文字列の削除の仕様

[リモートスプレッドシート内の重複する部分文字列の削除 API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstringsInRemoteSpreadsheet)は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST による操作を実行可能にします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使って Cloud API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# セキュアな接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/range/A1:C10/content/remove/duplicate-substrings?delimiters=comma%2Csemicolon&treatConsecutiveDelimitersAsOne=true&caseSensitive=false" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-encoded workbook stream"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---