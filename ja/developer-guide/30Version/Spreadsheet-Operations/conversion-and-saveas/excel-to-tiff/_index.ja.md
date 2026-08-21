---
title: "Excel から TIFF への変換"
second_title: "ドキュメント"
linketitle: "Excel から TIFF への変換"
type: docs
url: /convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/, /convert/excel-to-tiff/]
keywords: "Aspose.Cells Cloud, Excel から TIFF への変換, REST API, cURL, SDK, .NET, Java, Python, 画像エクスポート"
description: "Aspose.Cells Cloud API を使用して Excel ワークブックを高品質な TIFF 画像に変換する方法を学びます。詳細な cURL コマンド、SDK のサンプル (C#, Java, Python など)、認証手順、エラー処理を解説します。"
weight: 90
---

**Aspose.Cells Cloud** の **Convert**、**SaveAs**、および **Export** エンドポイントを使用すると、Excel ワークブックを TIFF 画像に変換できます。  
これらのエンドポイントは、**cURL** を直接呼び出すか、サポートされている SDK のいずれかを通じて呼び出すことができます。

## REST API

| **API**                | **メソッド** | **目的**                                                                                     | **Swagger リンク**                                                                          |
| ---------------------- | ---------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `/cells/convert`       | PUT        | リクエストボディに含まれるワークブックを指定された形式 (TIFF) に変換します。               | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`        | GET        | 指定された名前のワークブックを別の形式 (TIFF) にエクスポートし、結果をレスポンスとして返します。 | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs` | POST       | ワークブックを選択した形式 (TIFF) で保存し、結果をクラウドストレージに格納します。           | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

これらのエンドポイントは公開されており、Web ブラウザまたは任意の HTTP クライアントから直接呼び出すことができます。

### cURL の例

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<base64‑content>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< /tabs >}}

> **注意:**
>
> - **Convert** リクエストのボディには、ファイル (または保存済みファイルへの参照) と希望の `SaveFormat` を含める必要があります。
> - **Export** リクエストではリクエストボディは不要で、クエリ文字列 (`format=tiff`) で形式を指定します。

## エラー処理

| **ステータスコード** | **意味**             | **一般的な原因**                       |
| ------------------- | -------------------- | ------------------------------------- |
| 200                 | 成功                 | TIFF 画像が返されます (バイナリストリーム)。 |
| 400                 | 不正リクエスト       | パラメータが不足しているか、不正な形式です。   |
| 401                 | 認証エラー           | JWT トークンが無効または不足しています。     |
| 404                 | 見つかりません       | 指定されたワークブックが存在しません。      |
| 500                 | サーバー内部エラー   | サーバー側で予期しない状態が発生しました。    |

エラーが発生した場合、API は `Code`、`Message`、およびオプションで `Description` を含む JSON ペイロードを返します。

## クラウド SDK ファミリー

SDK を使用すると、開発を最も迅速に進めることができます。SDK が低レベルの詳細を処理するため、プロジェクトの本質的な部分に集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}