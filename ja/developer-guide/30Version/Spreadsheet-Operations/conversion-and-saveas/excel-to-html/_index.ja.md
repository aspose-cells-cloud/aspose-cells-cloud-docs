---
title: Excel を HTML に変換する  
description: Aspose.Cells Cloud API v3.0 を使用して Excel ワークブックを HTML ファイルに変換します。  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# Excel を HTML に変換する  

Aspose.Cells Cloud は、Excel ワークブック（XLS、XLSX、CSV など）を HTML ドキュメントに変換する堅牢な REST エンドポイントを提供します。この操作は、生成された HTML ファイル（ファイル名、サイズ、Base64 エンコードされた内容）を含む **FileInfo** オブジェクトを返します。

---

## 前提条件

| 必要条件 | 対応方法 |
|----------|----------|
| **Aspose Cloud アカウント** | [aspose.cloud](https://www.aspose.cloud) でアカウント登録を行ってください。 |
| **JWT アクセストークン** | OAuth 2.0 の `POST /connect/token` エンドポイントを通じてベアラートークンを取得してください。 |
| **ストレージ（オプション）** | API が特定のストレージからファイルを読み書きする場合、事前にストレージ（例：Amazon S3、Azure Blob、Aspose Cloud ストレージなど）を作成してください。 |
| **cURL / SDK** | multipart/form-data を処理可能な任意の HTTP クライアント（cURL、Postman、または Aspose.Cells SDK のいずれか）。 |

---

## 認証

Aspose.Cells Cloud のすべてのリクエストは **JWT トークンベース認証** が必要です。

```http
Authorization: Bearer <access-token>
```

このトークンは、すべてのリクエストの `Authorization` ヘッダーに含める必要があります。

---

## エンドポイント

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **注** – リクエストは `multipart/form-data` として送信する必要があります。Excel ファイルはマルチパート本文の最初のパートとして提供する必要があります。

---

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベース認証</a>が必須です。

## リクエストパラメータ  

### クエリパラメータ  

| 名前                     | 型      | 必須 | デフォルト | 説明 |
|--------------------------|---------|------|------------|------|
| `password`               | 文字列  | いいえ | – | 保護されたワークブックを開くためのパスワード。 |
| `storageName`            | 文字列  | いいえ | – | ソースファイルが存在するストレージの名前。 |
| `checkExcelRestriction` | 真偽値 | いいえ | `true` | `true` の場合、サービスは Excel 固有の制限（例：シート保護）を検証します。 |
| `region`                 | 文字列  | いいえ | – | ワークブックの地域設定（例：`ja-JP`）。 |
| `FontsLocation`          | 文字列  | いいえ | – | 描画に必要なカスタムフォントが格納されているフォルダの URL またはパス。 |

### フォームデータ（マルチパート）  

| 名前 | 型 | 必須 | 説明 |
|------|----|------|------|
| **File** | ファイル | **はい** | 変換対象の Excel ワークブック。マルチパートリクエストの最初のパートとして提供する必要があります。 |

---

## リクエスト例（cURL）

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/your_workbook.xlsx"
```

---

## 成功時の応答  

**ステータスコード:** `200 OK`

| フィールド     | 型     | 説明 |
|----------------|--------|------|
| `Filename`     | 文字列 | 生成された HTML ファイルの名前（例：`example.html`）。 |
| `FileSize`     | 整数  | HTML ファイルのサイズ（バイト単位）。 |
| `FileContent`  | 文字列 | Base64 エンコードされた HTML コンテンツ。 |

```json
{
  "Filename": "example.html",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

応答スキーマは **FileInfo** モデルによって定義されます：[/cells/file-info](/cells/file-info/)。

---

## エラーレスポンス  

| コード | 意味                   | 例のペイロード |
|--------|------------------------|----------------|
| `400` | 不正なリクエスト – パラメータが不足または無効 | ```json { "Code": "BadRequest", "Message": "The 'File' part is required." } ``` |
| `401` | 認証エラー – 無効または未指定の JWT トークン | ```json { "Code": "InvalidToken", "Message": "Access token is missing or expired." } ``` |
| `404` | 見つからない – 指定されたストレージ内にソースファイルが存在しない | ```json { "Code": "FileNotFound", "Message": "File 'my.xlsx' does not exist in storage 'MyStorage'." } ``` |
| `413` | ペイロードが大きすぎます – アップロードされたファイルが許容サイズを超える | ```json { "Code": "RequestEntityTooLarge", "Message": "Uploaded file exceeds the 100 MB limit." } ``` |
| `429` | リクエストが多すぎます – レート制限を超過 | ```json { "Code": "TooManyRequests", "Message": "Rate limit of 60 calls per minute exceeded." } ``` |
| `500` | サーバー内部エラー – 予期しないサーバー状態 | ```json { "Code": "InternalError", "Message": "An unexpected error occurred. Please try again later." } ``` |

---

## レート制限  

| 制限 | 説明 |
|------|------|
| **アカウントあたり 60 リクエスト/分**（デフォルト） | この制限を超過すると `429 Too Many Requests` が返されます。クライアントのロジックを調整するか、Aspose Cloud ポータルからクォータの引き上げをリクエストしてください。 |

---

## SDK サポート  

Aspose は、このエンドポイントをラップした複数のプログラミング言語向けの公式 SDK を提供しています。以下の例では、公式 SDK を使用した同じ変換処理を示しています。

| 言語   | サンプル |
|--------|----------|
| C#     | <details><summary>例を表示</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("your.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java   | <details><summary>例を表示</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("your.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python | <details><summary>例を表示</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js| <details><summary>例を表示</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('your.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go     | <details><summary>例を表示</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("your.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP    | <details><summary>例を表示</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby   | <details><summary>例を表示</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl   | <details><summary>例を表示</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

サポートされている SDK の全リストおよびインストール手順については、**Aspose.Cells Cloud SDKs** リポジトリをご覧ください：<https://github.com/aspose-cells-cloud>。

---

## 関連エンドポイント  

| エンドポイント | 説明 |
|----------------|------|
| `POST /cells/{name}/saveAs` | 既存の Excel ファイルを HTML（またはその他の形式）としてストレージに直接保存します。 |
| `PUT /cells/convert` | 追加の変換オプションを使用してワークブックを HTML に変換し、結果を応答ボディで返します。 |
| `GET /cells/{name}` | すでに HTML（またはその他の形式）として保存されているワークブックを、オプションのクエリパラメータ付きで取得します。 |

---

## よくある質問  

**Q:** *Excel から HTML への変換 API を呼び出す際の認証方法は？*  
**A:** OAuth 2.0 の `/connect/token` エンドポイントから取得した `Authorization: Bearer <access-token>` ヘッダーを含めてください。

**Q:** *`FileInfo` 応答にはどのようなフィールドが含まれますか？*  
**A:** 3 つのフィールド – `Filename`（文字列）、`FileSize`（整数、バイト単位）、`FileContent`（Base64 エンコードされた HTML コンテンツ）。

**Q:** *どのようなエラーコードが発生する可能性がありますか？*  
**A:** `400`（不正なリクエスト）、`401`（認証エラー）、`404`（ファイルが見つかりません）、`413`（ペイロードが大きすぎます）、`429`（リクエストが多すぎます）、`500`（サーバー内部エラー）。いずれも `Code` と `Message` を含む JSON ペイロードを返します。

**Q:** *カスタムフォントの場所を指定できますか？*  
**A:** はい。`FontsLocation` クエリパラメータを使用して、必要なフォントが含まれるフォルダまたは URL を指定できます。

**Q:** *この操作にはレート制限がありますか？*  
**A:** デフォルトでは**アカウントあたり 60 回/分**です。これを超過すると `429 Too Many Requests` が返されます。

---

## JSON‑LD パンくずリスト（構造化データ）

このブロックを追加すると、検索結果のリッチスニペットにパンくずリストが表示され、SEO が改善されます。

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "Developer Center", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "Conversion", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel to HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## 変更履歴  

| バージョン | 日付 | 変更内容 |
|------------|------|----------|
| **v3.0** | 2024‑10‑01 | `PostConvertWorkbookToHtml` の初回パブリックリリース。 |
| **v3.1** | 2025‑04‑15 | `region` および `FontsLocation` クエリパラメータを追加。エラーペイロードの形式を更新。 |
| **v3.2** | 2026‑03‑20 | レート制限のドキュメントとサンプルエラーレスポンスを追加。 |

--- 

*その他のサポートが必要な場合は、Aspose サポートにお問い合わせいただくか、公式 API リファレンスをご覧ください：* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---