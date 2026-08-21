---
title: "Aspose.Cells Cloud API – 公開キーの取得 (v4.0) | REST ドキュメント"
second_title: "ドキュメント"
ArticleTitle: "公開キーの取得"
linktype: "docs"
url: /ja/get-public-key/
keywords: "Aspose.Cells, 公開キー, RSA, API, クラウド"
description: "Aspose.Cells Cloud でデータを暗号化するために使用される RSA 公開キーを取得します。エンドポイント、パラメータ、リクエスト/レスポンスのサンプル、HTTP ステータスコード、SDK 使用例を含みます。"
weight: 100
---

この API は、非対称暗号化アルゴリズムから公開キーを取得します。

**概要:** Aspose.Cells の「公開キーの取得」API を使用して、クラウド上で Excel ファイルを処理する際にデータを暗号化するために必要な RSA 公開キー（2048 ビット）を取得します。エンドポイントは JSON 形式でキーを返し、OAuth 2.0 で保護されています。

## **公開キーの取得 API**

**前提条件:**  
このエンドポイントを呼び出す前に、`Cells.Read` スコープを含む有効な OAuth 2.0 アクセストークンを取得してください。

### **Web API**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

**リクエストのサンプル (cURL)**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名 | 種類   | 位置   | 説明                                                                 |
| ------------ | ------ | ------ | -------------------------------------------------------------------- |
| Authorization  | 文字列 | ヘッダー | OAuth2 認証用のベアラートークン（必須）                             |
| Accept       | 文字列 | ヘッダー | レスポンス形式（例: `application/json`、オプション、デフォルトは JSON） |

### **レスポンス**

```json
{
  "Code": 200,
  "Status": "OK",
  "CellsCloudPublicKey": {
    "PublicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAr...",
    "Algorithm": "RSA",
    "KeySize": 2048
  }
}
```

**HTTP ステータスコード**

| コード | 意味             | 説明                                                      |
| ------ | ---------------- | --------------------------------------------------------- |
| 200    | OK               | フィルターが正常に適用され、レスポンスに操作詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足または無効（例：サポートされていないファイル形式） |
| 401    | Unauthorized     | JWT トークンが無効または不足しています。                    |
| 413    | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。       |
| 500    | Internal Server Error | サーバーで予期しないエラーが発生しました。                 |

## SDK を使用した公開キー取得 API の使い方

### **OpenAPI 仕様**

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) はパブリックに利用可能なプログラミングインターフェースを定義しており、Web ブラウザから直接 REST での操作を実行できます。

### **Aspose.Cells Cloud SDK の使用**

SDK を使用すると、開発を大幅に加速できます。SDK が下層の詳細を処理するため、最小限のコードで cells の公開キー取得を実装できます。  
Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下に、最も一般的な言語の具体例を示します：

---