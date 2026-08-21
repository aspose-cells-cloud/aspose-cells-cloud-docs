---
title: "Aspose.Cells Cloud Web API - ローカル Excel の範囲データを JSON ファイルに変換する - 無料オンラインツール"
second_title: "ドキュメント"
ArticleTitle: "ローカルスプレッドシートの範囲データを JSON ファイルに変換する方法：ステップ・バイ・ステップガイド"
linktype: "docs"
url: "/convert-range-to-json/"
keywords: "範囲を json に変換, Aspose.Cells Cloud, Excel を json に変換, スプレッドシート変換, API"
description: "Aspose.Cells Cloud API を使用して、ローカル Excel スプレッドシートの特定の範囲を JSON に変換します。"
weight: 100
---

クラウド API を使用して、ローカル Excel ファイルから範囲データを JSON ファイルにエクスポートします。

## **範囲を JSON に変換する API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメーター:**

| パラメーター名 | 型     | パス / クエリ文字列 / HTTP ボディ | 説明                                                               |
| -------------- | ------ | --------------------------- | --------------------------------------------------------------------- |
| Spreadsheet    | ファイル | FormData                    | スプレッドシートファイルをアップロードします。                          |
| worksheet      | 文字列 | クエリ                       | スプレッドシート内のワークシート名。                             |
| range          | 文字列 | クエリ                       | 変換するセル範囲（例: A1:C10）。                                   |
| outPath        | 文字列 | クエリ                       | （オプション）ワークブックが保存されているフォルダーのパス。デフォルトは null です。 |
| outStorageName | 文字列 | クエリ                       | 出力ファイルストレージの名前。                                      |
| fontsLocation  | 文字列 | クエリ                       | ホーム利用向けのカスタムフォントを保存する場所。                       |
| region         | 文字列 | クエリ                       | スプレッドシートの地域設定。                                       |
| password       | 文字列 | クエリ                       | スプレッドシートファイルを開くためのパスワード。                            |

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

| コード | 意味                  | 説明                                                              |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | フィルターの適用に成功しました。レスポンスには操作の詳細が含まれます。 |
| 400  | リクエストエラー      | パラメーターが不足しているか無効です（例：サポートされていないファイル形式）。      |
| 401  | 認証エラー            | JWT トークンが無効または不足しています。                                     |
| 413  | ペイロードが大きすぎます | アップロードされたファイルがサイズ制限を超えています。                                 |
| 500  | サーバーエラー        | 予期しないサーバーエラーが発生しました。                                          |

## **範囲を JSON に変換する API をどこで使用すべきか？**

- リアルタイムダッシュボード：Chart.js や D3.js などのチャートライブラリ用に、ライブ Excel データを JSON に変換します。
- スプレッドシート・アズ・ア・サービス：他のサービス用に Excel 範囲を JSON エンドポイントとして公開します。
- Webhook ペイロード：Webhook 通知用にスプレッドシートデータを JSON に変換します。
- 簡易データプロトタイピング：クリーニング済みの Excel データを Python や R 分析用に迅速に JSON に変換します。
- マシンラーニングパイプライン：ビジネス部門が管理するスプレッドシートからトレーニングデータを前処理します。
- EC 業務：製品カタログや価格表を JSON 経由でウェブサイトと同期します。
- レポーティング自動化：財務モデルから JSON データフィードを生成し、レポーティングを自動化します。
- アプリケーション設定：Excel に保存された機能フラグ、設定、A/B テストパラメーターを JSON に変換します。
- 多言語対応：ローカリゼーション用スプレッドシートを i18n ライブラリ用に JSON に変換します。
- 動的メニューやナビゲーション：ウェブサイトのナビゲーション構造を Excel に保存し、JSON としてデプロイします。

_その他の変換オプションについては、[範囲を CSV に変換する](/convert-range-to-csv/)ガイドをご覧ください。_

## なぜ範囲を JSON に変換する API を使用すべきか？

- **SDK サポート**：Aspose.Cells Cloud は複数の言語向けのライブラリを提供しており、カスタムコードの量を削減できます。
- **ストレージコストの削減**：全ワークブックを先にアップロードすることなく範囲を変換できるため、ストレージ容量を節約できます。
- **Web アプリやモバイルアプリとの互換性**：JSON は、React、Vue、Angular などの最新の JavaScript フレームワークでネイティブにサポートされるデータ形式です。
- **広範な言語サポート**：ほぼすべてのプログラミング言語およびデータベースで JSON を処理できます。
- **構造化データの保持**
  - **インテリジェントな構造検出**：表形式データを適切な JSON 配列またはオブジェクトに自動変換します。
  - **ヘッダーのマッピング**：最初の行を JSON キーとして使用し、クリーンなオブジェクト構造を実現します。
  - **データ型の保持**：プレーンテキストではなく、数値・日付・真偽値などのデータ型を保持します。

## SDK を使用して範囲を JSON に変換する API をどのように使用するか？

### 範囲を JSON に変換する API の仕様

[範囲を JSON に変換する API の仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.json"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も速く、簡潔なコードでデータ範囲を JSON ファイルに変換できます。  
Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにアクセスする方法を示しています。
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}