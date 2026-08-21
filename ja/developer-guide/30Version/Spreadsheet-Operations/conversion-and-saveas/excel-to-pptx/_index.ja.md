---
title: "Aspose.Cells Cloud API v3.0 を使用して Excel を PPTX に変換する"
second_title: "ドキュメント"
linktitle: "Excel から PPTX へ"
type: docs
url: /ja/convert-excel-file-to-pptx-file/
keywords: "Aspose, Cells, Excel, PPTX, 変換, REST API, クラウド"
description: "Aspose.Cells Cloud REST API v3.0 を使用して Excel ワークブックを PPTX プレゼンテーションに変換する方法を学びます。cURL リクエスト、SDK コードサンプル、認証、エラー処理を含みます。"
weight: 90
ArticleTitle: "Aspose.Cells Cloud API v3.0 を使用して Excel を PPTX に変換する"
---

この REST API は、スプレッドシートファイルを PPTX 形式に変換します。

## PostConvertWorkbookToPptx API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### クエリパラメータ

| パラメータ名            | 型     | 説明                                                                 |
| ----------------------- | ------ | -------------------------------------------------------------------- |
| `password`              | 文字列 | Excel ワークブックを開くために必要なパスワード。                     |
| `storageName`           | 文字列 | ソースファイルが配置されているストレージの名前。                     |
| `checkExcelRestriction` | 真偽値 | セル関連オブジェクトを変更する際に Excel ファイルの制限を強制するかどうかを示します。 |

### リクエストボディパラメータ

| パラメータ名 | 型       | 説明                                                     |
| ------------ | -------- | -------------------------------------------------------- |
| `datafile`   | データファイル | マルチパートリクエストボディの最初のパートに含まれる Excel ファイル。 |

**マルチパートリクエストボディの例（簡略化）：**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<input.xlsx のバイナリコンテンツ>
--boundary
Content-Disposition: form-data; name="password"

MyPwd
--boundary--
```

### レスポンス

API は、生成された pptx ファイルを含む **FileInfo** オブジェクトを返します。

| フィールド        | 型     | 説明                                   |
| ----------------- | ------ | -------------------------------------- |
| **Filename**     | 文字列 | pptx ファイルの名前（例：`example.pptx`）。 |
| **FileSize**     | 整数   | ファイルサイズ（バイト単位）。         |
| **FileContent**  | 文字列 | pptx ファイルの Base64 エンコードされたコンテンツ。 |

[FileInfo](/cells/file-info/)


**HTTP ステータスコード**

| コード | 意味                   | 説明                                               |
|------|------------------------|----------------------------------------------------|
| 200  | OK                     | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request            | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized           | JWT トークンが無効または不足しています。             |
| 413  | Payload Too Large      | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error  | 予期しないサーバーエラーが発生しました。             |

*注意:* エンドポイントは、一般的な Excel 形式（`.xlsx`、`.xls`、`.xlsm`）をサポートしています。最大ファイルサイズは 50 MB に制限されています。マクロまたは保護されたシートを含むワークブックの変換は、適切なパラメータが指定されない限り制限される場合があります。

## SDK を使用した PostConvertWorkbookToPptx API の利用方法

### PostConvertWorkbookToPptx API の仕様

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">OpenAPI 仕様</a>は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 操作を実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.pptx",
  "FileSize": 123456,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最速で行えます。SDK は低レベルの詳細を抽象化し、プロジェクトに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud" rel="noopener noreferrer") を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## この機能を実装するその他の API

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – Excel ファイルを PDF に変換します。
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – Excel ファイルを PNG 画像に変換します。
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – Excel ファイルを SVG 形式に変換します。