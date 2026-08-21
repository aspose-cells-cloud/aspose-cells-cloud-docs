---
title: "Aspose.Cells Cloud AI – ユーザータスク分解 API（v4.0）｜SMART タスク計画"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud AI タスク分解 API を使用して、ユーザーオブジェクティブを順次アクション計画に変換する方法"
linktype: "Decompose User Task"
type: docs
url: /ja/decompose-user-task/
keywords: "Aspose.Cells AI, タスク分解 API, SMART タスク計画, Redmine インポート, プロジェクト自動化"
description: "Aspose.Cells Cloud AI を使用して、自由形式のオブジェクティブを SMART 準拠の時間推定付きタスクリストに変換します。単一の PUT リクエストで、Redmine、Jira、または Azure DevOps にインポート可能な CSV/XLSX 出力を取得します。"
weight: 100
---

**DecomposeUserTask** エンドポイントは、自由形式のタスク説明を SMART 基準に準拠した詳細な順次アクション計画に変換する REST エンドポイントを提供します。この API は自動的に時間単位の推定時間を割り当て、Redmine 互換のインポート形式で出力を整形し、プロジェクトのマイルストーンノードを作成します。生のタスクリストと任意の時間推定値を提供するだけで、API はプロジェクト管理ツールに直接インポート可能な（CSV、XLSX など）即時使用可能なファイルを返し、タスク分解の自動化と手動作業の削減を実現します。

## **ユーザータスク分解 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/task/decompose
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ:**

| パラメータ名       | 型     | 位置   | 必須／任意 | 説明                                                                                                                                                                                                                                                                              |
| :----------------- | :----- | :----- | :--------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TaskDescription    | 文字列 | 本体   | 必須       | ユーザーの全体的な目的を記述したプレーンテキスト形式の説明。サービスはこの説明を解析し、個別のタスクを生成します。例：「第3四半期向けのマーケティングキャンペーンを実施。内容には、コンテンツ作成、メール送信、SNS広告を含む」。                                                                                                             |

### **レスポンス**

成功レスポンス（200 OK）  
Content‑Type: `application/octet-stream`（バイナリファイルストリーム）

ヘッダー:

- `Content-Disposition: attachment; filename="DecomposedTaskPlan.xlsx"`
- `Content-Length: <バイト単位のサイズ>`

XLSX/ODS 形式の場合も同様の構造を使用し、列は最初のワークシートに配置されます。

**HTTP ステータスコード**

| コード | 意味             | 説明                                         |
| ------ | ---------------- | -------------------------------------------- |
| 200    | OK               | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | 不正なリクエスト | パラメータが不足または無効（例：サポートされていないファイル形式）。     |
| 401    | 認証エラー       | JWT トークンが無効または不足しています。                 |
| 413    | ペイロードが大きすぎます | アップロードされたファイルがサイズ制限を超えています。               |
| 500    | サーバー内部エラー | 予期しないサーバーエラーが発生しました。                   |

**エラーレスポンスの例（400 不正なリクエスト）**

```json
{
  "code": "InvalidParameter",
  "message": "「TaskDescription」フィールドは必須であり、空にできません。"
}
```

**リクエストボディのサンプル（JSON）**

```json
{
  "TaskDescription": "既存システムにタスク分割機能用の Web API を開発する。"
}
```

**レスポンスのサンプル**  
API は生成されたファイルを含むバイナリストリームを返します。CSV レスポンスの先頭数行をプレビューするには、ストリームをデコードし、ヘッダ行を確認します。例：

```
ID,Subject,Trucker,Estimated Duration,Description
1	タスク分割 API の要件定義	Business Analyst	8	新タスク分割エンドポイントの機能要件・非機能要件、ユーザーストーリー、受け入れ基準を収集する。
2	API 仕様書（OpenAPI）の作成	Business Analyst	6	POST /tasks/split の OpenAPI コントラクトを定義。リクエストスキーマ、レスポンス形式、エラーコード、セキュリティ要件を含む。
3	分割アルゴリズムおよびデータモデル設計	Solution Architect	5	親タスクをサブタスクに分割するコアアルゴリズムを設計し、階層構造とメタデータを格納するためのデータモデル（DB テーブル／エンティティ）を拡張する。
4	アーキテクチャ統合レビュー	Solution Architect	4	既存サービス、イベントフロー、データベースマイグレーションへの影響を分析し、統合計画を作成する。
...
```

## ユーザータスク分解 API の活用シーン

- **プロジェクト開始時**: 高レベルのプロジェクト概要を、時間推定付きの Redmine 互換タスクリストに変換し、即座にスプリント計画を開始可能にします。
- **マーケティング自動化**: キャンペーン目標を実行可能なステップに分解し、CSV としてエクスポートしてタスク管理ツールへインポート。チーム間の連携を強化します。
- **リソース配分**: 各サブタスクの時間単位推定値を生成し、プロジェクト開始前にマネージャーがチームメンバー間で作業負荷を調整できます。
- **マイルストーン追跡**: Gantt チャートツールと同期可能なマイルストーンノードを自動作成し、各フェーズの明確な成果物を保証します。

## なぜユーザータスク分解 API を使用すべきか？

- **SMART 準拠の出力**: 各生成タスクが「具体的（Specific）、測定可能（Measurable）、達成可能（Achievable）、関連性あり（Relevant）、期限あり（Time‑bound）」の各基準を満たします。
- **時間単位推定の自動化**: 手動計算が不要になり、予測精度が向上します。
- **即インポート可能なファイル形式**（CSV、XLSX など）: Redmine、Jira、Azure DevOps など、さまざまなプロジェクト管理プラットフォームとの統合が容易です。
- **単一リクエストによる自動化**: 単一リクエストでタスク分解が完了し、プロジェクト開始を加速し、手動作業を最小限に抑えます。

## SDK を使用したユーザータスク分解 API の利用方法

### ユーザータスク分解 API の仕様

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/DecomposeUserTask" target="_blank" rel="noopener noreferrer">ユーザータスク分解 API の仕様</a> は、Web ブラウザから直接 REST 処理を実行できるパブリックなプログラミングインターフェースを提供します。

## Excel API SDK

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化し、簡潔なコードで DecomposeUserTask エンドポイントを呼び出せるため、開発が最も速く行えます。  
Aspose.Cells Cloud SDK の完全な一覧は、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。  
以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスと連携する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_DecomposeUserTask.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_DecomposeUserTask.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_DecomposeUserTask.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_DecomposeUserTask.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_DecomposeUserTask.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_DecomposeUserTask.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_DecomposeUserTask.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_DecomposeUserTask.go" >}}
{{</tab>}}
{{< /tabs >}}

---