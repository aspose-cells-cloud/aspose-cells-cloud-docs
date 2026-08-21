---
title: "ワークシートの背景画像の追加または削除 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "背景"
type: docs
url: /worksheets/background/
keywords: "Aspose.Cells Cloud, ワークシート背景, Excel API, 背景画像の追加, ワークシート背景の削除, SDK サンプル"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートに背景画像を追加または削除する方法を学びます。リクエスト構文、Java、.NET、Python、PHP の SDK サンプル、およびエラー処理を含みます。"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API を使用してワークシート背景画像を追加または削除する"
---

## Excel ワークシートでの背景の操作

**概要:** ワークシート背景とは、ワークシートのセルの背後に表示される画像で、ブランド表示や視覚的なヒントに役立ちます。Aspose.Cells Cloud API を使用すると、この背景画像をプログラムで追加または削除できます。

**前提条件:**  
- 有効な Aspose.Cells Cloud アクセストークン（OAuth 2.0）  
- クラウド上に保存された Excel ワークブック  
- 背景に使用する画像ファイル（PNG、JPEG、BMP）

- **背景の追加** – ワークシートに背景画像を設定します。詳細なガイドは [Excel ワークシートに背景を設定する方法](/cells/worksheets/background/add/) を参照してください。  
- **背景の削除** – ワークシートから既存の背景画像を削除します。詳細なガイドは [Excel ワークシートの背景を削除する方法](/cells/worksheets/background/delete/) を参照してください。

ワークシート背景を使用すると、ブランドの強化、重要なセクションの強調、エンドユーザー向けの視覚的ヒントの提供などが可能になります。Aspose.Cells Cloud API を使用すれば、アプリケーションから直接この背景画像を設定またはクリアできます。

### API リファレンス

| 操作 | HTTP メソッド | エンドポイント | パスパラメータ | リクエストボディ | 成功時のレスポンス |
|------|---------------|----------------|----------------|------------------|------------------|
| 背景の追加 | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` – ワークブックのファイル名<br>`sheetName` – 対象ワークシート名 | 画像ファイル（PNG、JPEG、BMP）を multipart/form‑data 形式で | `200 OK` – 背景が適用されました |
| 背景の削除 | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` – ワークブックのファイル名<br>`sheetName` – 対象ワークシート名 | *なし* | `200 OK` – 背景が削除されました |

#### サンプル（Java SDK）

```java
// 背景画像の追加
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("path/to/background.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// 背景画像の削除
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### サンプル（Python SDK）

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")

# 背景の追加
with open("background.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# 背景の削除
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

その他の言語（C#、PHP、Ruby）のサンプルについては、SDK ドキュメントを参照してください。

**関連トピック**  
- ワークシートの一般的な管理方法について詳しくは：[ワークシート概要](/cells/worksheets/)  
- Aspose.Cells Cloud の認証方法については：[API 認証ガイド](/cells/authentication/)  
- チャート、テーブル、数式などのその他のスプレッドシート要素については：[スプレッドシート要素インデックス](/cells/elements/)  
---