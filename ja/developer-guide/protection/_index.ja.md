---
title: "Aspose.Cells Cloud Web API – Excel ファイルのオープンパスワードの設定・変更"
second_title: "包括的な開発者ガイド"
ArticleTitle: "スプレッドシート保護 – オープンパスワードと編集パスワードの設定"
linktype: "docs"
url: /ja/protection/
keywords: "Aspose.Cells, Cloud, API, スプレッドシート, 保護, オープンパスワード, 編集パスワード, Excel"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックにオープンパスワードまたは編集パスワードで保護する方法を学びます。リクエスト構文、コードサンプル、エラー処理を含みます。"
weight: 60
---

このガイドでは、Aspose.Cells Cloud Web API を使用してスプレッドシートの**オープンパスワード**と**編集パスワード**（読み書きパスワード）を設定・変更・削除する方法を学びます。これらの機能は、Excel ワークブック内の機密データを保護するのに役立ちます。

**前提条件**  
- 有効な API キーと SID を持つアクティブな Aspose.Cells Cloud アカウント。  
- 保護したいワークブックは、Aspose Cloud ストレージにアップロードされているか、公開 URL でアクセス可能である必要があります。  

**API リファレンス**  

| **HTTP メソッド** | **エンドポイント** | **クエリ / パスパラメータ** | **説明** |
|-----------------|------------------|---------------------------|---------|
| `PUT` | `/cells/{fileName}/protection` | `fileName`（パス）– ワークブックの名前<br>`openPassword`（クエリ、オプション）– ファイルを開くために必要なパスワード<br>`readWritePassword`（クエリ、オプション）– ファイルを編集するために必要なパスワード | 指定されたワークブックのオープンパスワードおよび／または編集パスワードを設定または更新します。 |
| `DELETE` | `/cells/{fileName}/protection` | `fileName`（パス）– ワークブックの名前 | ワークブックを保護するパスワードをすべて削除します。 |

**リクエスト本文の例（JSON）**  

```json
{
  "OpenPassword": "MyOpenPwd123",
  "ReadWritePassword": "MyEditPwd456"
}
```

**レスポンスの例（JSON）**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "ワークブックの保護が正常に更新されました。"
}
```

**HTTP ステータスコード**

| コード | 意味                      | 説明                                           |
|------|-------------------------|-----------------------------------------------|
| 200  | OK                      | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request             | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized            | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large       | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error   | 予期しないサーバーエラーが発生しました。 |

**コードサンプル**

*C#（Aspose.Cells Cloud SDK）*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Sample.xlsx",
    openPassword: "MyOpenPwd123",
    readWritePassword: "MyEditPwd456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python（Aspose.Cells Cloud SDK）*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Sample.xlsx",
    open_password="MyOpenPwd123",
    read_write_password="MyEditPwd456"
)
api.set_workbook_protection(request)
```

**エラー処理**  
エラーが発生した場合、API は `Code`、`Message`、およびオプションで `Description` を含む JSON ペイロードを返します。ステータスコードを確認し、アプリケーションのロジックに応じて適切に処理してください。

**関連トピック**  

- **[Aspose.Cells Cloud を使用してスプレッドシートをパスワードで保護する方法](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[Aspose.Cells Cloud を使用してスプレッドシートのパスワード保護を解除する方法](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  
---