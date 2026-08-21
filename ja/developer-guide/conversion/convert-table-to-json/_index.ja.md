---
title: "Aspose.Cells Cloud Web API – ローカルの Excel テーブルデータを JSON ファイルに変換する"
second_title: "Document"
ArticleTitle: "ローカルのスプレッドシートテーブルデータを JSON ファイルに変換する方法：ステップ・バイ・ステップガイド"
linktype: "Convert Table to JSON"
type: docs
url: /ja/convert-table-to-json/
keywords: "Excel, API, JSON, 変換, クラウド, ファイル, スプレッドシート"
description: "Aspose.Cells Cloud API を使用して、1 つの PUT リクエストでローカルの Excel テーブルを JSON ファイルに変換します。cURL の例、パラメータ、および C#、Java、Python などの SDK スニペットを含みます。"
weight: 100
---

Aspose.Cells Cloud Web API を使用して、ローカルのスプレッドシート／Excel テーブルを **JSON** ファイルに変換します。

## **テーブルを JSON に変換する API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名       | タイプ | 位置       | 説明                                                                                      |
| ------------------ | ------ | ---------- | ----------------------------------------------------------------------------------------- |
| **Spreadsheet**    | ファイル | FormData   | アップロードする Excel ファイル。                                                         |
| **worksheet**      | 文字列 | クエリ     | テーブルを含むワークシートの名前。                                                        |
| **tableName**      | 文字列 | クエリ     | 変換するテーブルの名前。                                                                  |
| **outPath**        | 文字列 | クエリ     | (省略可) 生成された JSON ファイルを保存するフォルダパス。既定値は **null** です。        |
| **outStorageName** | 文字列 | クエリ     | (省略可) 出力ファイルを配置するストレージの名前。                                         |
| **fontsLocation**  | 文字列 | クエリ     | (省略可) 変換中に使用されるカスタムフォントのパス。                                       |
| **region**         | 文字列 | クエリ     | (省略可) ワークブック用の地域設定。                                                       |
| **password**       | 文字列 | クエリ     | (省略可) 保護されたワークブックを開くためのパスワード。                                   |

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

**HTTP ステータスコード**

| コード | 意味               | 説明                                                            |
| ------ | ------------------ | --------------------------------------------------------------- |
| 200    | OK                 | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400    | Bad Request        | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized       | JWT トークンが無効または不足している。                            |
| 413    | Payload Too Large  | アップロードされたファイルがサイズ制限を超えた。                  |
| 500    | Internal Server Error | 予期しないサーバーエラー。                                        |

## **Convert Table to JSON API の使用例**

- **リアルタイムダッシュボード** – Chart.js や D3.js などのチャートライブラリ用に、ライブの Excel データを JSON に変換します。
- **スプレッドシート・アズ・ア・サービス** – Excel テーブルを他のマイクロサービス向けの JSON エンドポイントとして公開します。
- **Webhook ペイロード** – スプレッドシートデータを JSON に変換し、Webhook 通知に使用します。
- **迅速なデータプロトタイピング** – クリーニング済みの Excel データを Python や R 分析用に迅速に JSON に変換します。
- **機械学習パイプライン** – ビジネススプレッドシートに保存されたトレーニングデータを前処理します。
- **eコマース運用** – 製品カタログや価格表を JSON 経由でウェブサイトと同期します。
- **レポート自動化** – 財務モデルから JSON フィードを生成し、レポートを自動化します。
- **アプリ設定** – Excel で機能フラグ、設定、A/B テストパラメータを管理し、JSON に変換してデプロイします。
- **多言語サポート** – 現地化スプレッドシートを i18n ライブラリ用に JSON に変換します。
- **動的メニュー／ナビゲーション** – ウェブサイトのナビゲーション構造を Excel に保存し、JSON としてデプロイします。

## **Convert Table to JSON API を使用する理由**

- **開発者フレンドリー** – Aspose.Cells Cloud は多言語向け SDK を提供し、開発工数を削減し、包括的なドキュメントを提供します。
- **コスト効率的** – ワークブックを事前にアップロードせずにテーブルデータを変換できるため、ストレージ容量を節約し、コストを削減します。
- **モダンな Web およびモバイル互換性** – JSON は Web のネイティブデータ言語です。この API を使用すると、複雑な解析処理をすることなく、ライブのスプレッドシートデータを React、Vue、Angular、モバイルアプリ、シングルページアプリケーションに直接渡せます。
- **広範な言語サポート** – JSON はほぼすべてのプログラミング言語、データベース、Web サービスと連携可能です。
- **構造化データの保持**
  - **インテリジェントな構造検出** – タブ形式のデータを適切な JSON 配列／オブジェクトに自動変換します。
  - **ヘッダーのマッピング** – 最初の行を JSON キーとして使用し、クリーンなオブジェクト構造を生成します。
  - **データ型の保持** – 数値、日付、真偽値（文字列以外）を保持します。

_バージョン履歴:_ Convert Table to JSON エンドポイントは API バージョン **v4.0**（2024 年）で導入され、現在の安定版リリースです。以前の v3.x エンドポイントは非推奨です。

## **SDK を使用して Convert Table to JSON API を活用する方法**

### Convert Table to JSON API 仕様

[Convert Table to JSON API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson){:target="\_blank" rel="noopener noreferrer"} はパブリックにアクセス可能なプログラミングインターフェースを提供し、ウェブブラウザから直接 REST 通信を行えるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示します。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

```
{
 "Code": 200,
 "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化し、最小限のコードでスプレッドシートテーブルを JSON ファイルに変換できます。Aspose.Cells Cloud SDK の完全なリストは、公式 GitHub リポジトリをご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスと連携する方法を示します。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}