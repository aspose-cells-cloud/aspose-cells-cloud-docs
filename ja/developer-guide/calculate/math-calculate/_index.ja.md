---
title: "Aspose.Cells Cloud – 数学計算 API（加算、減算、乗算、除算、パーセンテージ）"
second_title: "ドキュメント"
ArticleTitle: "スプレッドシート／Excel での加算、減算、乗算、除算、パーセンテージ計算"
linktitle: "数学計算"
type: docs
url: /ja/math-calculate/
keywords: "数学計算 API, Aspose.Cells Cloud, Excel 計算, 加算, 減算, 乗算, 除算, パーセンテージ, Excel 一括処理, REST API"
description: "Aspose.Cells Cloud 数学計算 API を使用して、Excel の範囲に対して加算、減算、乗算、除算、パーセンテージ操作を一括で適用する方法を学びます。リクエスト形式、サンプルコード、エラー処理を含みます。"
weight: 100
---

## **導入**: スプレッドシートクイック計算 – 1つの実行APIで加算、乗算、減算、除算、パーセンテージ計算

_数式を記述することなく、列全体、行全体、または表全体に一括で計算を実行します。_

- **基本演算**: 任意の数値を範囲内のすべてのセルに加算、減算、乗算、除算
- **パーセンテージ計算**: パーセント増減（例: +15%、-8%）、または数値のパーセンテージ計算（例: 20% of…）
- **一括処理**: 数千のセルに即座に適用 — オートフィルや配列数式、VBA不要

| **計算操作** | 説明 |
| :---------------------- | :---------- |
| **加算 (Add)**                 | +           |
| **減算 (Subtract)**            | -           |
| **乗算 (Multiply)**            | \*          |
| **除算 (Divide)**              | /           |
| **パーセンテージ (Percentage)**          | %           |

## **数学計算 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必須です。

### **リクエストパラメータ**

| パラメータ名 | 型     | パス／クエリ文字列／HTTP ボディ | 説明                                                                 |
| :----------- | :----- | :------------------------------ | :------------------------------------------------------------------- |
| Spreadsheet  | ファイル | FormData                        | 処理対象のスプレッドシートファイルをアップロードします。             |
| operation    | 文字列   | クエリ                          | 実行する数学的演算（Add、Subtract、Multiply、Divide、Percentage）。 |
| value        | 文字列   | クエリ                          | 計算に使用する値（該当する場合）。                                   |
| worksheet    | 文字列   | クエリ                          | 操作を実行するワークシート名。                                       |
| range        | 文字列   | クエリ                          | 計算に含めるセル範囲。                                               |
| region       | 文字列   | クエリ                          | スプレッドシートの地域設定。                                         |
| password     | 文字列   | クエリ                          | パスワードで保護されている場合のスプレッドシートファイルのパスワード。|

### **レスポンス**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**HTTP ステータスコード**

| コード | 意味                 | 説明                                                               |
| ------ | -------------------- | ------------------------------------------------------------------ |
| 200    | OK                   | フィルターの適用に成功。レスポンスには操作の詳細が含まれます。     |
| 400    | Bad Request          | パラメータ不足または無効（例: 未サポートのファイル形式）。         |
| 401    | Unauthorized         | 無効または不足している JWT トークン。                              |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。             |
| 500    | Internal Server Error | 予期しないサーバーエラー。                                         |

## 数学計算 API の使用例

- **金融**: 購入価格の列全体に 13% の VAT を加算。
- **在庫管理**: kg 列を 2.2046 倍して一括でポンド単位に変換。
- **給与計算**: 全従業員のボーナス列に固定額 1,000 を加算。
- **為替変換**: 売上列を最新の為替レートで除算し、USD 金額を算出。
- **評価**: 学生の得点から一律 5 点を減算して出席停止のペナルティを適用。
- **EC**: 商品価格を一括で 15% 引き下げ、プロモーション割引を一瞬で適用。

## なぜ数学計算 API を使うべきなのか？

- **高速な Excel 計算** – 月次締めレポートを数秒で完了。
- **Excel 一括パーセンテージ増加** – 価格、予測、コミッションを一瞬で更新。
- **列全体に同じ数値を加算** – 在庫、通貨変換、単位変換。
- **数式不要の Excel** – 非技術者もシンプルさを享受可能。
- 既存の SDK を通じて開発を迅速に完了。

**注意事項**  
サポートされる最大ファイルサイズは 200 MB です。`range` パラメータには、有効な Excel アドレス（例: A1:B10）を指定してください。非常に大きなワークシートの場合、追加の処理時間がかかることがあります。

## SDK を使用した数学計算 API の利用方法

### 数学計算 API の仕様

[Math Calculate Specification](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) はパブリックにアクセス可能なプログラミングインターフェースを定義し、開発者が Web ブラウザから直接 API とやりとりできるようにしています。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を隠蔽できるため、開発が最も速く進みます。短いコードでセル単位の数学計算を実行できます。  
Aspose.Cells Cloud SDK の完全な一覧は [Aspose.Cells Cloud SDK on GitHub](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{</tab>}}
{{< /tabs >}}

---