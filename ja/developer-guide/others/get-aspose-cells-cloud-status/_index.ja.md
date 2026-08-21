---
title: "Aspose.Cells Cloud Web API - Aspose.Cells Cloud のステータスを取得する"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud のステータスを取得する"
linktype: "Aspose.Cells Cloud のステータスを取得する"
type: docs
url: /get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, Cloud API, ヘルスチェック, Excel, REST"
description: "Aspose.Cells Cloud サービスのヘルスステータスをリアルタイムで監視します。"
weight: 100
---

Aspose.Cells Cloud サービスのヘルスステータスをリアルタイムで取得します。

**前提条件:** この API を呼び出すには、Aspose Cloud クライアントの認証情報を使用して Bearer トークンを取得し、`Authorization` ヘッダーに `Bearer {access_token}` の形式でトークンを含める必要があります。

## **Aspose.Cells Cloud のステータスを取得する**

### **Web API**

エンドポイントは HTTP **GET** メソッドを使用し、リクエストボディは必要ありません。

```
GET https://api.aspose.cloud/v4.0/cells
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### **リクエストパラメータ**

| パラメータ名 | 型     | パス/クエリ文字列/HTTP ボディ | 説明                             |
| ------------ | ------ | --------------------------- | --------------------------------- |
| Authorization| 文字列 | ヘッダー                    | 認証用の Bearer トークン（必須）  |
| format       | 文字列 | クエリ                      | 期待する応答形式（例: `json`）   |

### **応答**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**応答スキーマ**

| フィールド    | 型                | 説明                                   |
| ------------- | ----------------- | -------------------------------------- |
| status        | 文字列            | サービスのヘルス状態（`OK`、`Degraded` など） |
| service       | 文字列            | サービス名                             |
| timestamp     | 文字列 (ISO‑8601) | ステータスチェックの実行時刻           |

この API は、Aspose.Cells Cloud サービスの現在のヘルス**ステータス**を含む標準的な JSON ペイロードを返します。

**HTTP ステータスコード**

- **200 OK** – サービスが正常であり、応答にステータス情報が含まれています。
- **401 Unauthorized** – 認証トークンが不足している、または無効です。
- **503 Service Unavailable** – サービスが現在メンテナンス中または何らかの問題が発生しています。

## SDK を使用して Aspose.Cells Cloud のステータス取得 API を利用する方法

### OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus) は、Web ブラウザから直接 REST 通信を実行できるパブリックなプログラミングインターフェースを定義しています。

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、統合が簡素化され、ボイラープレートコードが削減されます。SDK は内部の詳細処理を処理するため、最小限の労力で Aspose.Cells Cloud の実行ステータスを取得できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。