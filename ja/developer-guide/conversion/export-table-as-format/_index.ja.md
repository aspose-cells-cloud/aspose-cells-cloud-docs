---
title: "表のエクスポート – Aspose.Cells Cloud API | Excel を PDF、PNG、CSV に変換"
second_title: "ドキュメント"
ArticleTitle: "リモートスプレッドシートの表を他の形式にエクスポートする方法：ステップ・バイ・ステップガイド"
linktype: "表のエクスポート – 指定した形式"
type: docs
url: /export-table-as-format/
keywords: "Aspose.Cells, 表のエクスポート, Excel から PDF への変換, クラウド API, REST"
description: "Aspose.Cells Cloud API を使用して、クラウドに保存された Excel 表を PDF、PNG、CSV、JSON などの他の形式にエクスポートします。JWT 認証を備えた安全な HTTPS エンドポイントと SDK のコード例を提供します。"
weight: 100
---

クラウドに保存されたスプレッドシート（Excel）の表を、他の形式のファイルとしてエクスポートします。

## **表を指定した形式でエクスポートする API**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必須とします。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメーター:**

| パラメーター名 | 型     | パス/クエリ文字列/HTTP ボディ | 説明                                                                                                                                                     |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | 文字列 | パス                       | **必須。** 取得対象のワークブックファイル名。                                                                                                            |
| worksheet      | 文字列 | パス                       | シート名。                                                                                                                                               |
| tableName      | 文字列 | パス                       | 表の名前。                                                                                                                                               |
| format         | 文字列 | クエリ                     | **必須。** 出力形式（例: "png"、"pdf"、"svg"）。                                                                                                          |
| folder         | 文字列 | クエリ                     | オプション。ワークブックが保存されているフォルダーのパス。既定値は `null`。                                                                              |
| storageName    | 文字列 | クエリ                     | オプション。カスタムクラウドストレージを使用する場合のストレージ名。省略した場合は既定のストレージを使用します。                                         |
| outPath        | 文字列 | クエリ                     | オプション。出力ファイルを保存するフォルダーのパス。既定値は `null`。                                                                                    |
| outStorageName | 文字列 | クエリ                     | オプション。出力ファイルを保存するストレージの名前。                                                                                                      |
| fontsLocation  | 文字列 | クエリ                     | オプション。カスタムフォントの場所。                                                                                                                      |
| region         | 文字列 | クエリ                     | オプション。スプレッドシートの地域/言語設定（例: `en-US`、`fr-FR`）。数値の書式、日付の解析、ロケール固有の動作に影響します。                             |
| password       | 文字列 | クエリ                     | オプション。スプレッドシートファイルを開く際のパスワード。                                                                                                |

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

**HTTP ステータスコード**

| コード | 意味                   | 説明                                                                   |
| ---- | --------------------- | --------------------------------------------------------------------- |
| 200  | OK                    | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。         |
| 400  | リクエストエラー       | パラメーターが不足しているか、無効です（例: 未対応のファイル形式）。     |
| 401  | 認証エラー             | JWT トークンが無効または不足しています。                                               |
| 413  | ペイロードが大きすぎます | アップロードされたファイルがサイズ制限を超えています。                                |
| 500  | サーバーエラー         | 予期せぬサーバーエラーが発生しました。                                                |

## **表を他の形式にエクスポートする API を使用すべきケース**

- **レガシーシステムの移行**: 数千のレガシー XLS ファイルを XLSX に変換し、モダンなシステムに対応させます。
- **アーカイブの標準化**: さまざまなスプレッドシート形式（XLS、XLSM、ODS、CSV）をアーカイブ用に単一の形式に統一します。
- **オフィススイート間の相互運用性**: Excel ファイルを LibreOffice、Google スプレッドシート、Apple Numbers と互換性のある形式に変換します。
- **データソースの正規化**: さまざまなスプレッドシート形式を CSV または JSON に変換し、データベースへの取り込みを容易にします。
- **ウェブ公開**: 財務モデルを HTML に変換し、ウェブで表示します。

## **表を他の形式にエクスポートする API を使用すべき理由**

- **開発者向け**: Aspose.Cells Cloud は複数の言語向けの SDK ライブラリを提供しており、迅速な開発が可能です。また、包括的なドキュメントも整備されています。カスタムのチャート描画ソリューションを構築する場合と比べ、開発工数を大幅に削減できます。
- **人件費の削減**: ドキュメントの統合作業に専任の人員を割り当てる必要がなくなります。
- **従量課金制**: 初期投資は不要で、実際に使用した API 呼び出し分のみ課金されます。
- **メンテナンスコストゼロ**: サーバーの運用、ソフトウェアの更新、互換性問題への対応が不要です。
- **API はワークブックのスタイル情報を除き、表データのみを返します。**

## **SDK を使用してスプレッドシート表を指定した形式でエクスポートする方法**

### 表を指定した形式でエクスポートする API の仕様

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">表を指定した形式でエクスポートする API の仕様</a> は、パブリックに公開されたプログラミングインタフェースを定義し、ウェブブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード済み)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化して、短いコードでスプレッドシート表を指定した形式のファイルにエクスポートできるため、開発が最も迅速に行えます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにアクセスする方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}