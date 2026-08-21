---
title: "Aspise.Cells Cloud Web API – その他の機能：ヘルスチェック、公開鍵の取得"
linktitle: "その他の機能"
ArticleTitle: "その他の機能：ヘルスチェック、公開鍵の取得"
second_title: "ドキュメント"
type: docs
url: /other-features/
keywords: "Aspose.Cells、Cloud API、ヘルスチェック、公開鍵、アクセス トークン、Excel、REST"
description: "Aspose.Cells Cloud のその他の機能を確認してください：ヘルスチェック エンドポイント、公開鍵の取得、およびトークン生成機能で、Excel API 統合のセキュリティを強化します。"
weight: 180
---

**前提条件** – 以下に示す機能を使用するには、有効な Aspose Cloud サブスクリプションおよび認証用にアクティブな **Client ID** / **Client Secret** のペアが必要です。

これらの「その他の機能」は、Aspose.Cells Cloud API の基本的なサポート操作を提供します。たとえば、サービスの可用性の確認、暗号鍵の取得、およびアクセス トークンの取得などです。通常、ワークブック関連のエンドポイントを操作する前にこれらの機能を呼び出します。

- **[Aspose.Cells Cloud のヘルスチェック](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  Aspose.Cells Cloud サービスが到達可能で正常に動作していることを確認します。成功した呼び出しは、JSON `{ "status": "OK" }` と **HTTP 200** を返します。作業フローの初期段階でこのエンドポイントを使用し、不要なエラーを回避してください。  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">さらに詳しく</a>

- **[Aspose.Cells Cloud の実行状態の取得](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  サービスの現在の実行時ステータスを取得します。応答には、API が完全に動作しているか、メンテナンス中であるか、または問題が発生しているかが示されます。  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">さらに詳しく</a>

- **[公開鍵の取得](https://docs.aspose.cloud/cells/get-public-key/)**  
  Aspose.Cells Cloud が発行した JWT トークンの検証に使用される RSA 公開鍵（PEM 形式）を取得します。この鍵は、サーバーサイドでトークンを検証する際に必要です。  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">さらに詳しく</a>

- **[Client ID と Secret を使用したアクセス トークンの取得](https://docs.aspose.cloud/cells/post-access-token/)**  
  **client_credentials** グラントタイプを使用して OAuth 2.0 アクセス トークンを生成します。**Client ID** と **Client Secret** をリクエスト本文に含めると、応答には `access_token`、`token_type`、`expires_in` が含まれます。このトークンは、以降のすべての API 呼び出しで `Authorization` ヘッダーに指定する必要があります。  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">さらに詳しく</a>