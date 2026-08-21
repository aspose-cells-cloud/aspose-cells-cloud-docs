---
title: "Aspose.Cells Cloud Web API –ワークシートをJSONに変換"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud API を使用してスプレッドシートのワークシートをJSONに変換する方法"
linktitle: "ワークシートをJSONに変換"
type: docs
url: /convert-worksheet-to-json/
keywords: "Aspose.Cells, ワークシートからJSONへ, Excel変換, クラウドAPI, API v4, データエクスポート"
description: "Aspose.Cells Cloud API を使用してExcelワークシートをJSONに変換するステップバイステップガイド。リクエストパラメータ、レスポンス処理、エラーコード、SDKサンプルを含みます。"
weight: 100
---

**ConvertWorksheetToJson** エンドポイントは、ローカルファイルシステムからスプレッドシートファイルを読み取り、指定されたワークシートを抽出し、その内容をJSONファイルとして返します。変換はすべてAspose.Cells Cloudサーバー上で実行されるため、中継用のアップロードやストレージの使用は不要です。この機能は、パスワードで保護されたワークブック、カスタムフォントの場所、地域設定をサポートし、ワークシートデータをJSON形式でエクスポートして後続処理に使用するための高速なクラウドネイティブソリューションを提供します。

## **ワークシートをJSONに変換するAPI**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名      | 型     | 位置         | 必須／任意 | 説明                                                                                                                                                                                                 |
| :---------------- | :----- | :----------- | :--------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | file   | FormData     | 必須       | 処理対象のExcelワークブック。対応フォーマット（xls、xlsx、csvなど）である必要があります。multipart/form-data形式で送信します。例: `Spreadsheet=@C:\Docs\Sample.xlsx`                                   |
| worksheet         | string | Query        | 必須       | 変換するワークシートの正確な名前（大文字・小文字を区別）。指定がない、または見つからない場合、APIはエラーを返します。例: `worksheet=Sheet1`                                                              |
| outPath           | string | Query        | 任意       | 設定されたクラウドストレージ内の、生成されたJSONファイルを保存する宛先フォルダ。指定がない場合、JSONはレスポンスストリーム内で直接返されます。例: `outPath=/converted/`                             |
| outStorageName    | string | Query        | 任意       | `outPath` を含むターゲットストレージの名前（例: "MyStorage"）。省略時はデフォルトストレージが使用されます。                                                                                             |
| fontsLocation     | string | Query        | 任意       | ワークシート内のテキストを正確にレンダリングするために必要なカスタムフォントを格納するサーバーサイドフォルダ。例: `fontsLocation=/fonts/custom/`                                                       |
| region            | string | Query        | 任意       | 生成されたJSONにおける数値・日付・通貨のフォーマットに影響を与える文化・地域識別子（例: `en-US`, `fr-FR`）。                                                                                           |
| password          | string | Query        | 任意       | 暗号化されたワークブックを開くためのパスワード。ワークブックがパスワード保護されていない場合はこのパラメータを省略してください。                                                                      |

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

**HTTPステータスコード**

| コード | 意味               | 説明                                                   |
| ------ | ------------------ | ------------------------------------------------------ |
| 200    | OK                 | フィルターが正常に適用された。レスポンスには操作詳細が含まれます。 |
| 400    | Bad Request        | パラメータが不足している、または無効（例: 非対応のファイル形式）。 |
| 401    | Unauthorized       | 無効な、または不足しているJWTトークン。                |
| 413    | Payload Too Large  | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | 予期しないサーバーエラー。                             |

## どこでワークシートをJSONに変換するAPIを使用すべきか？

- **Webダッシュボード** – ワークシートデータをJSON形式でエクスポートし、クライアントサイドのチャートライブラリ（Chart.js、D3.jsなど）に提供します。
- **データ移行** – 従来のExcelデータを、JSONを消費するNoSQLデータベースやRESTサービスへ移行します。
- **モバイル／オフラインアプリ** – サーバーサイドでワークシート内容をJSONに変換し、軽量ペイロードをモバイルデバイスと同期します。
- **レポートパイプライン** – 中間にCSV処理を挟まず、ワークシートデータを直接JSON入力を許容する分析エンジンにフィードします。

## なぜワークシートをJSONに変換するAPIを使用すべきか？

- **アップロード不要のワークフロー** – ストレージへ事前アップロードすることなく、ローカルファイルをクラウドで処理できるため、帯域幅とストレージコストを節約できます。
- **フル機能の変換** – パスワード保護ワークブック、カスタムフォント、地域フォーマットをサポートし、正確なデータ表現を実現します。
- **高速かつスケーラブルな実行** – クラウドインフラ上でAspose.Cellsの高性能エンジンを活用し、大規模ワークシートを効率的に処理します。
- **シンプルな統合** – 単一のPUT呼び出しで、すぐに使用可能なJSONファイルを返すか、直接ストレージに保存できるため、クライアントアプリケーションのコードが簡潔になります。

## SDK を使用してワークシートをJSONに変換するAPI を使用する方法

### ワークシートをJSONに変換するAPI仕様

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson" rel="noopener noreferrer">ワークシートをJSONに変換するAPI仕様</a> は、Webブラウザから直接RESTインタラクションを実行できるパブリックアクセス可能なプログラミングインターフェースを提供します。

cURLコマンドラインツールを使用することで、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例は、cURLを使用してクラウドAPIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64エンコード済み)",
  "contentType": "MIMEタイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化し、簡潔なコードでスプレッドシートとやり取りできるため、開発が最も迅速になります。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHubリポジトリ</a>をご確認ください。  
以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスとやり合う方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}