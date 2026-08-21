---
title: "Excelファイルの暗号化、復号化、およびデジタル署名"
second_title: "ドキュメント"
linktype: "protect-excel"
type: docs
url: /ja/protect/
aliases: [  /ja/workbook/password/ ]
keywords: "Excel, 保護, 暗号化, 復号化, デジタル署名, Aspose.Cells Cloud, REST API, パスワード, セキュリティ"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックを保護・暗号化・復号化・デジタル署名する方法を学びましょう。Android、C#、Java、Python などのコード例を提供しています。"
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ファイルを暗号化・復号化・デジタル署名・保護する"
weight: 36
---

## **Excel ファイルの保護および保護解除**

**Aspose.Cells Cloud における「保護」とは？**  
**Protect** 操作は、パスワードを適用してファイルの開封・編集・構造変更を制限することで Excel ワークブックを安全に保護します。また、この API ではワークブックの暗号化・復号化および改ざん防止検証用のデジタル署名の追加もサポートしています。

**API リファレンス**  

| HTTP メソッド | エンドポイント | 必要なクエリ/本文パラメータ | サンプルリクエスト本文 | 典型的なレスポンス |
|-------------|----------|-----------------------------------|---------------------|-------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName` (パス), `password` (クエリ) | `{ "password": "MySecret123" }` | `200 OK` – 保護適用済み、`400 Bad Request`、`401 Unauthorized`、`500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (パス), `password` (クエリ) | N/A | `200 OK` – 保護解除済み、上記のエラーコード |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName` (パス), `password` (クエリ) | N/A | `200 OK` – ファイル暗号化済み |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName` (パス), `password` (クエリ) | N/A | `200 OK` – ファイル復号化済み |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName` (パス) | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "certPass" }` | `200 OK` – デジタル署名追加済み |

**コード例（C#）**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API クライアントを初期化
var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// ワークブックを保護
var protectRequest = new PostProtectWorkbookRequest(
    name: "Sample.xlsx",
    password: "MySecret123"
);
api.PostProtectWorkbook(protectRequest);
```

**前提条件**  
- アクティブな Aspose.Cells Cloud サブスクリプション  
- 認証用の `AppSid` および `AppKey`  

**認証**  
すべてのリクエストには、Aspose Cloud 認証エンドポイントから取得した有効な JWT トークンを含む `Authorization` ヘッダーを含める必要があります。

**エラーハンドリング**  
HTTP ステータスコードとレスポンス本文で返される `Error` オブジェクトを確認してください。よくあるエラーには、無効なパスワード (`400`)、ファイル不在 (`404`)、認証失敗 (`401`) などがあります。

**注意事項**  
- 同じエンドポイントを、アクションセグメント (`/encrypt`、`/decrypt`) を変更することで**暗号化**または**復号化**に使用できます。  
- デジタル署名には、API からアクセス可能な有効な証明書ファイルが必要です。

- [Aspose.Cells Cloud API で Excel ファイルを暗号化する](/cells/excel-file-encrypt/)
- [Aspose.Cells Cloud API で Excel ファイルを保護する](/cells/protect-excel-file/)
- [Excel ファイルにデジタル署名を追加する](/cells/excel-digital-signature/)
- [Excel ファイルを保護する – 詳細ガイド](/cells/protect-excel-files/)
- [Excel ファイルのパスワードを設定する](/cells/workbook/password/modify/)
- [Excel ファイルを復号化する](/cells/excel-file-decrypt/)
- [Excel ファイルの保護を解除する](/cells/excel-file-unprotect/)
- [Excel ファイルをロック解除する](/cells/unlock-excel-files/)
- [Excel ファイルのパスワードをクリアする](/cells/clear-excel-files-password/)
---