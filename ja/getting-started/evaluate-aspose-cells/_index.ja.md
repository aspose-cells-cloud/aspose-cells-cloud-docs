---
title: "Aspose.Cells Cloud の評価"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud の評価"
LinkTitle: "評価"
type: docs
url: /ja/evaluate-aspose-cells-ja/
description: "Aspose.Cells Cloud（Excel ファイルおよびその他のスプレッドシート形式の作成、変換、結合、分割、保護、および操作のための REST API）を探索します。"
weight: 60
keywords:
  - Aspose.Cells Cloud
  - Excel API
  - REST API
  - スプレッドシート操作
  - 無料トライアル
  - 評価
---

Aspose Cloud ダッシュボードで無料トライアルアカウントを作成することで、**Aspose.Cells Cloud** REST API を評価できます。登録後、**Client Id** および **Client Secret** が発行され、これらを使用して月間最大150回の API コールが可能になります。

**前提条件**  
開始する前に、アクティブなインターネット接続とサポートされている開発環境が整っていることを確認してください。API は HTTP 経由で直接呼び出すこともできますし、より簡単な統合のために Aspose.Cells SDK（例：.NET、Java、Python、PHP）のいずれかを使用することもできます。

**クイックスタート手順**

1. **無料トライアルアカウントの作成** – [Aspose Cloud ダッシュボード](https://dashboard.aspose.cloud) にアクセスし、サインアップしてメールアドレスを確認してください。  
2. **認証情報の取得** – ダッシュボードの **Authentication（認証）** セクションで *Client Id* および *Client Secret* を確認してください。  
3. **アクセス トークンの生成** – 認証情報を使用して `POST https://api.aspose.cloud/connect/token` にリクエストを送信します（正確なペイロードについては API リファレンスを参照してください）。  
4. **最初の API コールの実行** – `Authorization: Bearer <token>` ヘッダーにトークンを含め、`GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets` などのシンプルなエンドポイントを呼び出します。  

無料トライアルにより、サービスの機能を実践的に体験し、コストをかけずに早期の開発およびテストが可能になります。

**API リファレンス概要**

| 操作 | メソッド | URL | 必須パラメータ | サンプル応答 |
|------|----------|-----|----------------|--------------|
| アクセス トークンの取得 | POST | `https://api.aspose.cloud/connect/token` | `grant_type=client_credentials`, `client_id`, `client_secret`（フォーム URL エンコード形式） | `{ "access_token": "eyJ0eXAi...", "expires_in": 3600 }` |
| シート一覧の取得 | GET | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets` | パス: `{file}` – アップロードされたワークブックのファイル名； ヘッダー: `Authorization: Bearer <token>` | `{ "Worksheets": { "WorksheetList": [ { "Name": "Sheet1" }, { "Name": "Sheet2" } ] } }` |

詳細な料金、使用制限、追加プランのオプションについては、[トライアルプラン](https://purchase.aspose.cloud/trial) ページをご参照ください。