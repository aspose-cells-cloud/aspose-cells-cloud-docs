---
title: "Excelワークブックでのワークシート削除の操作方法"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /ja/worksheets/delete/
keywords: "Aspose.Cells, クラウド, REST API, ワークシート削除, Excel, C#, Java, Python"
description: "Aspose.Cells Cloud REST API を使って Excel ワークブックから単一または複数のワークシートを削除する方法を学びます。C#、Java、Python のコード例、前提条件、エラー処理のヒント、関連操作を含みます。"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API を使って Excel ワークブックからワークシートを削除する"
---

## Excelワークブックでのワークシート削除の操作

アプリケーションが動的に Excel ファイルを生成または修正する際、不要になったワークシート（一時的なレポート、プレースホルダーシート、古いデータなど）を削除する必要が生じることがあります。Aspose.Cells Cloud API を使えば、単一ワークシートまたは複数ワークシートを1回のリクエストで簡単に削除できます。

**API リファレンス**  

| 項目 | 詳細 |
|------|------|
| **HTTP メソッド** | `DELETE` |
| **エンドポイント** | `/cells/{fileName}/worksheets` |
| **パスパラメータ** | `fileName` – Excel ファイル名（必須） |
| **クエリパラメータ** | `sheetName` – 削除するワークシート名（省略可、単一削除時に使用） <br> `folder` – ストレージ内のソースフォルダ（省略可） <br> `storage` – ストレージ名（省略可） |
| **リクエストボディ** | *なし* |
| **成功レスポンス** | `200 OK` – ワークシートの削除に成功。操作ステータスを含む JSON オブジェクトを返します。 |
| **エラーレスポンス** | `400 Bad Request` – 不正なパラメータ <br> `401 Unauthorized` – 認証失敗 <br> `404 Not Found` – ファイルまたはワークシートが見つからない <br> `500 Internal Server Error` – サーバーサイドのエラー |

**リクエスト**  

1つまたは複数のワークシートを削除するには、上記のエンドポイントに対して `DELETE` リクエストを送信し、必須の `fileName` を含めます。単一シートの削除の場合は、オプションで `sheetName` クエリパラメータを指定します。`sheetName` を省略した場合、ワークブック内のすべてのワークシートが削除されます。

**パラメータ**  

- `fileName`（文字列、必須）：拡張子を含む Excel ファイル名。  
- `sheetName`（文字列、省略可）：削除する特定のワークシート名。省略した場合、API はすべてのワークシートを削除します。  
- `folder`（文字列、省略可）：ストレージ内のファイルを含むフォルダのパス。  
- `storage`（文字列、省略可）：使用する Aspose Cloud ストレージの名前。

**レスポンス**  

- **200 OK** – 例の JSON：  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "Worksheet(s) deleted successfully."
  }
  ```
- **400 Bad Request** – 不正なリクエストパラメータ。  
- **401 Unauthorized** – 認証トークンが欠落または無効。  
- **404 Not Found** – 指定されたファイルまたはワークシートが存在しない。  
- **500 Internal Server Error** – 予期しないサーバーエラー。

**コード例**  

*以下は、3つの人気言語で削除エンドポイントを呼び出す方法を示す短いコードスニペットです。*

**C# の例**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"Error: {ex.Message}");
}
```

**Java の例**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("Status: " + response.getStatus());
        } catch (Exception e) {
            System.err.println("Error: " + e.getMessage());
        }
    }
}
```

**Python の例**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"Status: {response.status}")
except ApiException as e:
    print(f"Error: {e}")
```

**エラー処理**  

- リクエストを送信する前に、認証トークンが有効であることを確認してください。  
- レスポンスのステータスコードを確認し、`400`、`401`、`404`、`500` を適切に処理してください。  
- try-catch ブロック（または同等の機構）を使用して、ネットワークエラーや SDK 例外をキャッチしてください。

**関連操作**  

- [ワークシートの追加](/worksheets/add/) – 既存のワークブックに新しいワークシートを作成します。  
- [ワークシートのコピー](/worksheets/copy/) – 既存のワークシートを複製します。  
- [ワークシートの名前変更](/worksheets/rename/) – ワークシートの名前を変更します。  
- [ワークシートの移動](/worksheets/move/) – ワークブック内でワークシートの順序を変更します。  
---