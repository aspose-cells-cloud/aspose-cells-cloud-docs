---
title: "Aspose.Cells Cloud Web API - Post Access Token"
second_title: "ドキュメント"
ArticleTitle: "クライアント ID とシークレットでアクセス トークンを取得する"
linktitle: "Post Access Token"
type: docs
url: /ja/post-access-token/
keywords: "Aspose.Cells, Cloud, アクセス トークン, OAuth2, API, 認証, REST, Excel, Office Cloud"
description: "クライアント ID とシークレットを使用して POST /cells/connect/token エンドポイントを呼び出すことで、Aspose.Cells Cloud の OAuth2 アクセス トークンを取得します。"
weight: 100
---

クライアント ID とシークレットを使用して Cells Cloud Get Token API でアクセス トークンを取得します。

## Post Access Token API

エンドポイントを呼び出す前に、以下の条件を満たしていることを確認してください。

* 登録済みの Aspose Cloud アカウント。
* Aspose Cloud ポータルで生成された **Client ID** と **Client Secret**。

### Web API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエスト パラメーター

| パラメーター名 | 型     | 位置                         | 説明                                             |
| -------------- | ------ | ---------------------------- | ------------------------------------------------- |
| grant_type     | string | 本文（form‑url‑encoded）     | OAuth に必要な固定値 `client_credentials`        |
| client_id      | string | 本文（form‑url‑encoded）     | 発行されたクライアント識別子                     |
| client_secret  | string | 本文（form‑url‑encoded）     | クライアント ID に関連付けられたシークレット      |

**リクエスト例（cURL）**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET"
```

### レスポンス

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**HTTP ステータス コード**

| コード | 意味                         | 説明                                               |
|------|-----------------------------|---------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400  | Bad Request                 | パラメーターが不足しているか無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足している。             |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えている。 |
| 500  | Internal Server Error       | 予期しないサーバー エラー。                        |

**エラー処理の例**

```json
{
  "error": "invalid_client",
  "error_description": "Client authentication failed."
}
```

## SDK を使用して Get public key API を利用する方法

### OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) は、パブリックにアクセス可能なプログラミング インターフェースを定義しており、Web ブラウザーから直接 REST によるやり取りを実行できます。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、最も迅速に開始できます。SDK は基盤となる HTTP の詳細を抽象化し、最小限のコードで Cells のアクセス トークンを取得できます。

Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリー](https://github.com/aspose-cells-cloud) を確認してください。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。  
---