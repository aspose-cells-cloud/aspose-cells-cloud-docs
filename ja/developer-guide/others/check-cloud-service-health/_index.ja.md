---
title: "Aspose.Cells Cloud – サービスのヘルスチェック（API）"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud ヘルスチェック"
linktype: "docs"
url: /check-cloud-service-health/
keywords: "Aspose.Cells Cloud、API ヘルスチェック、REST ステータス、クラウドサービスモニタリング"
description: "Aspose.Cells Cloud のヘルス状態をリアルタイムで監視します。GET /v4.0/cells/status/check エンドポイント、パラメーター、レスポンス形式、SDK の例について学習します。"
weight: 100
---

Aspose.Cells Cloud サービスのヘルス状態を確認します。

**前提条件**  
このエンドポイントを呼び出すには、有効な Aspose Cloud アクセストークンが必要です。アカウントを Aspose Cloud ダッシュボードに登録し、クライアント ID とクライアント シークレットを使用して OAuth2 トークンエンドポイントからベアラートークンを取得してください。取得したトークンは、以下のように `Authorization` ヘッダーに含めてください。

## **クラウドサービスのヘルスチェック**

### **Web API**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### **リクエストパラメーター**

| パラメーター     | 型     | 必須   | 説明                                                                 |
| --------------- | ------ | ------ | --------------------------------------------------------------------- |
| Authorization   | ヘッダー | はい    | 認証用のベアラートークン (`Authorization: Bearer <token>`)            |
| detail          | クエリ   | いいえ  | 詳細なコンポーネント情報を含める場合は `true` を設定します。           |
| Accept          | ヘッダー | いいえ  | 期望するレスポンス形式。デフォルトは `application/json` です。        |

### **レスポンス**

リクエストが成功すると、サービスは JSON ペイロードを返します。

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "正常",
    "storage": "正常",
    "database": "正常"
  }
}
```

**HTTP ステータスコード**

| コード | 意味               | 説明                                                      |
| ------ | ------------------ | --------------------------------------------------------- |
| 200    | OK                 | サービスが正常です。上記の JSON 例を参照してください。    |
| 401    | 認証エラー         | 無効な、または不足している認証トークンです。              |
| 503    | サービス利用不可   | サービスが現在正常でないか、メンテナンス中です。          |
| 4xx    | クライアントエラー | 不正なリクエストパラメータ、または不正な形式のリクエストです。 |
| 5xx    | サーバーエラー     | 予期せぬサーバー障害が発生しました。後ほど再試行してください。 |

## Aspose.Cells Cloud ステータス API を SDK で使用する方法

### OpenAPI 仕様

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">OpenAPI 仕様</a> は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できます。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を効率的に進めることができます。SDK は低レベルの詳細を処理し、最小限のコードで Cells のクラウドヘルスチェックを実装できます。  
Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下は、最も一般的な SDK を使用してヘルスチェックエンドポイントを呼び出す方法のサンプルコードです。

---