---
title: "ワークシートを PDF、PNG、CSV などに変換 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "ワークシートの変換"
type: docs
url: /ja/worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells, ワークシート変換, REST API, cURL, SDK, PDF, PNG, CSV"
description: "Aspose.Cells Cloud REST API を使用して、Excel ブック内の単一ワークシートを PDF、PNG、CSV、および 15 种類以上のその他の形式に変換する方法を学びます。cURL の例、SDK のコードスニペット、および完全なパラメータ参照が含まれています。"
weight: 130
ArticleTitle: "ワークシートを PDF、PNG、CSV などに変換 – Aspose.Cells Cloud API"
---

**ワークシート変換 API** – `GET /cells/{name}/worksheets/{sheetName}` エンドポイントは、Excel ブック内の単一ワークシート（シート）を別のファイル形式に変換します。

> **前提条件:** このエンドポイントを呼び出す前に、有効な JWT トークンを取得し、ブックを Aspose Cloud のサポート対象ストレージに保存しておく必要があります。

サポートされる**インポート可能**形式（ワークシートの読み取り元）:

- XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT

サポートされる**エクスポート専用**形式（ワークシートの保存先）:

- PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS

## REST API

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) は、公開可能なインターフェースを定義しています。

### **リクエストパラメータ**

| パラメータ名                | 型      | 必須   | デフォルト | 許容値                                                                | 説明                                     |
| ------------------------ | ------- | ------ | -------- | --------------------------------------------------------------------- | ---------------------------------------- |
| **format**               | 文字列  | はい   | –        | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, …（サポート一覧参照） | 出力先のファイル形式。                   |
| **verticalResolution**   | 整数    | いいえ | 96       | 72‑600                                                                | 画像出力の垂直方向 DPI。                 |
| **horizontalResolution** | 整数    | いいえ | 96       | 72‑600                                                                | 画像出力の水平方向 DPI。                 |
| **password**             | 文字列  | いいえ | –        | –                                                                     | パスワードで保護されたブックを開くためのパスワード。 |
| **folder**               | 文字列  | いいえ | –        | –                                                                     | ソースブックが保存されているクラウドフォルダ。 |
| **storage**              | 文字列  | いいえ | –        | –                                                                     | ストレージ名（例: "Default"）。          |

### レスポンス

| ステータスコード | 説明                                                                   | 戻り値の型                 |
| ---------------- | ---------------------------------------------------------------------- | -------------------------- |
| **200**          | 変換成功；変換されたファイルのバイナリストリームが返されます。         | `application/octet-stream` |
| **400**          | 不正なリクエスト；パラメータが不足または無効です。                     | JSON エラーオブジェクト    |
| **401**          | 認証エラー；JWT トークンが無効または不足しています。                   | JSON エラーオブジェクト    |
| **404**          | 見つからない；ブックまたはワークシートが存在しません。                 | JSON エラーオブジェクト    |
| **500**          | サーバ内部エラー；予期しないエラーが発生しました。                     | JSON エラーオブジェクト    |

#### 例：リクエスト（cURL）

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### 例：レスポンス

```
変換された画像（バイナリストリーム）
```

## クラウド SDK ファミリー

SDK を使用すると、開発を最も迅速に行えます。SDK が低レベルの詳細を処理するため、プロジェクトの本質的な部分に集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---