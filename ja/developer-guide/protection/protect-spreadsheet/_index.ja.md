---
title: "Aspose.Cells Cloud Excelパスワード保護 Web API – 開くパスワードと変更パスワードの暗号化を自動化"
second_title: "Excel保護開発者ガイド"
ArticleTitle: "Excelパスワード保護ツール – 開くパスワードと変更パスワードを設定 – スプレッドシートを安全に保護"
linktitle: "スプレッドシートの保護"
type: docs
url: /ja/protect-spreadsheet/
keywords: "Aspose.Cells, Excelパスワード保護, API, 開くパスワード, 変更パスワード, クラウドストレージ, スプレッドシートセキュリティ"
description: "Aspose.Cells Cloud を使用して Excel ファイルをプログラムで安全に保護します。1回の API コールで開くパスワードと変更パスワードの両方を設定できます。.xlsx、.xls、およびクラウドストレージをサポートしています。無料で試してみてください。"
weight: 100
---

開発者向け API を使用して、大規模な Excel パスワード保護を自動化します。開くパスワードと変更パスワードの両方をプログラムで適用でき、エンタープライズワークフローに最適で、.xlsx およびレガシ形式に対応しています。ドキュメントを確認して、今日から無料で統合を開始してください。

## **スプレッドシートの保護 API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメータ**

| パラメータ名     | タイプ   | パス／クエリ文字列／HTTPボディ | 説明                                                                                                                                                         |
| :--------------- | :------- | :---------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | ファイル | FormData                      | パスワード暗号化で保護する Excel スプレッドシートファイルをアップロードします。                                                                            |
| openPassword     | 文字列   | クエリ                        | 保護されたスプレッドシートを開く（復号化）する際に必要なパスワード。                                                                                         |
| modifyPassword   | 文字列   | クエリ                        | スプレッドシートの内容を編集または変更できるようにするためのパスワード。                                                                                      |
| outPath          | 文字列   | クエリ                        | （オプション）保護されたワークブックを保存する出力フォルダーのパスを指定します。指定しない場合、ファイルはレスポンスとして返されます。                        |
| outStorageName   | 文字列   | クエリ                        | 出力として保護されたファイルを保存するために使用するクラウドストレージの名前。                                                                               |
| region           | 文字列   | クエリ                        | 処理中にスプレッドシートに適用される地域・文化設定（日付形式、数値書式など）を指定します。                                                                    |

**認証**  
スプレッドシートの保護 API へのすべての呼び出しには、有効な OAuth 2.0 アクセストークンが必要です。トークンは `Authorization` ヘッダーに含めてください。

```http
Authorization: Bearer {access_token}
```

トークンは Aspose Cloud の認証エンドポイントから取得し、**Cells** スコープを含める必要があります。

## **レスポンス**

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

| コード | 意味                   | 説明                                                       |
| ------ | ---------------------- | ---------------------------------------------------------- |
| 200    | OK（成功）             | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | 不正リクエスト         | パラメータが不足しているか、無効です（例：サポートされていないファイル形式）。 |
| 401    | 認証エラー             | JWT トークンが無効または不足しています。                   |
| 413    | ペイロードが大きすぎます | アップロードされたファイルがサイズ制限を超えています。     |
| 500    | サーバーエラー         | 予期しないサーバーエラーが発生しました。                   |

## スプレッドシートの保護 API の使用例

- **機密性の高い財務データの保護** – バジェット、請求書、給与情報などを含む Excel ファイルを、開くパスワードと変更パスワードで保護し、不正アクセスや編集を防ぎます。
- **機密レポートの安全な共有** – 社内・社外問わず、ビジネスレポート、監査レポート、コンプライアンスレポートを配布する際、認可された受信者のみが閲覧・変更できるようにします。
- **ワークフロー内のドキュメントセキュリティの自動化** – API をエンタープライズシステム（例：ERP、CRM）に統合し、生成されたスプレッドシートを保存またはメール送信前に自動的にパスワード保護します。
- **読み取り専用アクセスの強制** – 別途設定した変更パスワードで、ユーザーにレポートの閲覧のみを許可し、変更を制限できます。テンプレートや最終確定データセットに最適です。
- **規制コンプライアンスの遵守** – GDPR、HIPAA、SOX などの要件を満たすために、自動保護を通じて、静止時および転送中の機密スプレッドシートデータを暗号化します。

## なぜスプレッドシートの保護 API を使用すべきか？

- **開発者フレンドリー** – Aspose.Cells Cloud は複数の言語向け SDK ライブラリを提供しており、迅速な開発が可能です。また、包括的なドキュメントも整っています。独自ソリューションを構築する場合と比較して、開発負荷を大幅に削減できます。
- **人的リソースの削減** – ドキュメントの統合とセキュリティ処理を自動化し、専任担当者の必要性を低減します。
- **従量課金制** – 初期投資不要。実際に使用した API 呼び出し分のみ課金されます。
- **メンテナンスコストゼロ** – サーバーの管理が不要で、ソフトウェアの更新や互換性の懸念もありません。
- **元の Excel 書式を完全に保持** – パスワード保護を適用しても、保護されたワークブックの書式はソースファイルと完全に一致します。

## SDK を使用したスプレッドシートの保護 API の利用方法

### OpenAPI スペック

[スプレッドシートの保護 API スペック](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) は、Web ブラウザから直接 REST API を呼び出せるパブリックアクセス可能なプログラミングインターフェースを提供します。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?openPassword=MyOpenPwd&modifyPassword=MyModifyPwd" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
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

SDK を使用すると、開発を最も効率的に進められます。SDK が内部処理をすべて処理するため、最小限のコードでスプレッドシートの保護機能を実装できます。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスとやり合う方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}