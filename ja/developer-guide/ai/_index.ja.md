---
title: "Aspose.Cells Cloud AI – タスクの分解、スプレッドシートおよびテキストの翻訳"
second_title: "ドキュメント"
ArticleTitle: "AIスキルを向上させよう：Excel翻訳、タスク分解など学ぼう"
linktitle: "AI"
type: docs
url: /ja/ai/
keywords: "Aspose.Cells, Cloud AI, Excel翻訳, タスク分解, REST API"
description: "Aspose.Cells Cloud AI を活用して、タスクの分解、Excelワークブックおよびテキストファイルの翻訳を実行します。RESTエンドポイント、サンプルコード、ベストプラクティスを含みます。"
weight: 20
---

Aspose.Cells Cloud AI は、Excelおよびテキストデータの取り扱いを簡素化する3つの強力なAI駆動型サービスを提供しています：**ユーザーのタスクの分解**、**スプレッドシートの翻訳**、および**テキストファイルの翻訳**です。これらのAPIにより、開発者は複雑なユーザー目標を実行可能な手順にプログラムで分解し、ワークブック全体またはプレーンテキストファイルを翻訳し、その結果を独自のアプリケーションに統合できます。以下のエンドポイントを使用してすぐに使い始めることができ、各サービスに関する詳細なリクエスト／レスポンス仕様を参照してください。

- **[ユーザーのタスクの分解](https://docs.aspose.cloud/cells/decompose-user-task/)** – Aspose.Cells Cloud AI を使用して、ユーザーの目標を順序付けられたアクションプランに変換します。  
  - **リクエストメソッド:** `POST`  
  - **エンドポイントURL:** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`  
  - **ヘッダー:** `Authorization: Bearer <access_token>`, `Content-Type: application/json`  
  - **リクエスト本文（JSON）:**  
    ```json
    {
      "task": "チャートとピボットテーブルを含む四半期営業レポートを作成する"
    }
    ```  
  - **レスポンス:** タスクリストを含むスプレッドシートファイルをダウンロード可能ファイルとして返します。  
  - **ステータスコード:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`  
  - **前提条件:** **CellsAI** スコープを持つ有効なアクセストークン。  
  - **レスポンス例（JSON スニペット）:**  
    ```json
    {
      "fileId": "12345abcde",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
    }
    ```  
  - **備考:** 生成されたワークブックには、**TaskList** という名前のワークシートが含まれ、順序付けられた手順が記載されています。レート制限：1分あたり100リクエスト。

- **[スプレッドシートの翻訳](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – Aspose.Cells Cloud AI を使用してスプレッドシート全体を翻訳します。  
  - **リクエストメソッド:** `POST`  
  - **エンドポイントURL:** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`  
  - **ヘッダー:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **リクエストパラメータ:**  
    - `file` – 翻訳するExcelファイル（バイナリ）。  
    - `targetLanguage` – ISO言語コード（例：`fr`, `de`）。  
  - **レスポンス:** 翻訳されたワークブックをダウンロード可能ファイルとして返します。  
  - **ステータスコード:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **前提条件:** **CellsAI** スコープを持つアクセストークンおよび十分なストレージクォータ。  
  - **レスポンス例（JSON スニペット）:**  
    ```json
    {
      "translatedFileId": "f9d8c7b6",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
    }
    ```  
  - **備考:** すべてのセル値、コメント、シート名が翻訳されます。レート制限：1分あたり100リクエスト。

- **[テキストファイルの翻訳](https://docs.aspose.cloud/cells/translate-text-file/)** – Aspose.Cells Cloud AI を使用してテキストファイル全体を翻訳します。  
  - **リクエストメソッド:** `POST`  
  - **エンドポイントURL:** `https://api.aspose.cloud/v4.0/cells/ai/translate-text`  
  - **ヘッダー:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **リクエストパラメータ:**  
    - `file` – 翻訳するテキストファイル（バイナリ）。  
    - `targetLanguage` – ISO言語コード（例：`es`, `ja`）。  
  - **レスポンス:** 翻訳されたテキストファイルを返します。  
  - **ステータスコード:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **前提条件:** **CellsAI** スコープを持つ有効なアクセストークン。  
  - **レスポンス例（JSON スニペット）:**  
    ```json
    {
      "translatedFileId": "a1b2c3d4",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
    }
    ```  
  - **備考:** UTF-8エンコードのプレーンテキストファイル（最大5MB）をサポートします。レート制限：1分あたり100リクエスト。