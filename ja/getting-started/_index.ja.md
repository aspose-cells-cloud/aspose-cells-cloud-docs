---
title: "Aspose.Cells Cloud API による始めてのガイド — Excel ファイルを 3 つの簡単なステップで処理する"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud 始めてのガイド"
linktitle: "始めてのガイド"
type: docs
url: /getting-started/
description: "Aspose.Cells Cloud REST API を使用して、Excel ファイルをアップロード、変換、ダウンロードする方法を 3 つの簡単なステップで学びます。cURL のコードサンプルを含みます。"
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, スプレッドシート変換, Excel から PDF へ, クラウドスプレッドシート, Aspose.Cells Cloud API"
---

- [概要](/cells/overview/)
- [クイックスタート](/cells/quickstart/)
- [利用可能な SDK](/cells/available-sdks/)
- [サポートされているプラットフォーム](/cells/supported-platforms/)
- [サポートされているファイル形式](/cells/supported-file-formats/)
- [Aspose.Cells Cloud の評価](/cells/evaluate-aspose-cells/)
- [料金プラン](/cells/pricing-plan/)
- [技術サポート](/cells/technical-support/)
- [Docker コンテナの実行方法](/cells/how-to-run-docker-container/)

**始めてのガイド**

開始する前に、有効な **Aspose Cloud API キー** と **ストレージ名** をご用意ください。これらの認証情報は、その後のすべての API コールに必要です。

**ステップ 1: Excel ファイルをアップロードする**  
ソースのワークブックを Aspose Cloud ストレージへアップロードします。

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*リクエストボディ*: ファイルはバイナリストリーム (`application/octet‑stream`) として送信されます。  
*必須パラメータ*:

- `path` – ファイルが保存されるストレージパス（例: `folder/sample.xlsx`）。

**ステップ 2: ワークブックを PDF に変換する**  
ファイルが保存されたら、変換リクエストを送信します。

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*必須パラメータ*:

- `name` – アップロードされたワークブックの名前（例: `sample.xlsx`）。
- `format` – 変換後のフォーマット（`pdf`）。
- `outputPath` – 変換されたファイルが保存されるストレージパス（例: `folder/result.pdf`）。

*サンプルレスポンスペイロード* (JSON):

```json
{
  "status": "OK",
  "outputPath": "folder/result.pdf"
}
```

**ステップ 3: 変換された PDF をダウンロードする**  
ストレージから生成された PDF を取得します。

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*必須パラメータ*:

- `outputPath` – 前のステップで生成された PDF のパス。

**サンプル リクエスト / レスポンス概要**

| 操作 | HTTP メソッド | エンドポイント（例） | パラメータ | 成功ステータス |
|-----------|-------------|--------------------|------------|----------------|
| アップロード | PUT | /cells/storage/file/{path} | `path`（ストレージの場所） | 200 OK |
| 変換 | POST | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| ダウンロード | GET | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**よくあるエラーコード**

- **400 Bad Request** – パラメータが不足している、または無効です。  
- **401 Unauthorized** – アクセストークンが無効または不足しています。  
- **404 Not Found** – 指定されたファイルまたはパスが存在しません。  
- **500 Internal Server Error** – 予期しないサーバーエラーが発生しました。再試行するか、サポートへお問い合わせください。  
---