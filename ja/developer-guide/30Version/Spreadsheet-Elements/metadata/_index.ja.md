---
title: "Excel のメタデータおよびプロパティの操作"
second_title: "Document"
linktype: "ja"
type: docs
url: /metadata/
aliases:
  - /document-properties/
  - /working-with-document-properties/
keywords: "Aspose.Cells Cloud, Excel メタデータ, ドキュメント プロパティ API, REST API, メタデータの取得, Excel プロパティの更新, Excel メタデータの削除"
description: "Aspose.Cells Cloud REST API を使用して Excel ファイルのメタデータを読み取り、追加、更新、削除する方法を学びます。Java、.NET、Python、Node.js など、cURL および SDK を使用した例を含みます。"
ArticleTitle: "Excel メタデータおよびドキュメント プロパティの操作 – Aspose.Cells Cloud"
weight: 100
---

Excel ファイルには、ドキュメントの識別、整理、管理を支援するさまざまなメタデータを格納できます。Aspose.Cells Cloud は、このメタデータの読み取り、追加、更新、削除を行うためのシンプルな REST API を提供し、開発者がドキュメント プロパティ管理をアプリケーションに統合できるようになります。このガイドでは、標準プロパティとカスタム プロパティという 2 つの主要なプロパティ カテゴリについて説明し、それらの操作方法を解説するとともに、関連する API エンドポイントへの直接リンクを提供します。また、実装を迅速化するため、リクエスト詳細をまとめた簡潔な API リファレンス表も掲載しています。

**最終更新日:** 2026 年 7 月 8 日  

**ドキュメント プロパティの種類**

Aspose.Cells Cloud API を使用して Excel ドキュメント（ワークブック）内のドキュメント プロパティ（メタデータ）を表示、変更、削除する方法を学ぶ前に、Excel ドキュメントが持つことのできるプロパティの種類について明確にしておきましょう。

- **標準プロパティ** は Excel 共通のものです。タイトル、件名、作成者、カテゴリなどの基本情報を含みます。これらのプロパティにはカスタムのテキスト値を設定でき、ファイルの検索を容易にします。

- **カスタム プロパティ** はユーザー定義のものです。Excel ドキュメントに追加のメタデータを付加できます。

**Excel ファイルでのドキュメント プロパティの操作方法**

- [ストレージを使用して特定のドキュメント プロパティを取得する方法](/cells/document-properties/get/)
- [ストレージを使用せずにドキュメント プロパティを取得する方法](/cells/metadata/get/)
- [ストレージを使用してすべてのドキュメント プロパティを取得する方法](/cells/document-properties/get-all/)
- [ストレージを使用して特定のドキュメント プロパティを更新する方法](/cells/document-properties/update/)
- [ストレージを使用せずに特定のドキュメント プロパティを更新する方法](/cells/metadata/update/)
- [ストレージを使用して特定のドキュメント プロパティを削除する方法](/cells/document-properties/delete/)
- [ストレージを使用せずにドキュメント プロパティを削除する方法](/cells/metadata/delete/)
- [ストレージを使用してすべてのドキュメント プロパティを削除する方法](/cells/document-properties/clear/)

**API リファレンス（ストレージ使用なし）**

| メソッド | エンドポイント | 説明 |
|--------|----------|-------------|
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata` | クラウドに保存されたワークブックのすべてのドキュメント プロパティを取得します。 |
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | `propertyName` で識別される特定のプロパティ（標準またはカスタム）の値を取得します。 |
| **PUT** | `PUT https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | 既存のプロパティの値を更新します。リクエスト本文には新しい値を JSON 形式で含めます。 |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | ワークブックから特定のプロパティを削除します。 |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata` | ワークブックからすべてのカスタムおよび標準プロパティをクリアします。 |

*すべてのリクエストには OAuth 2.0 アクセス トークンが必要です。また、特定のストレージ場所を使用する場合は、`storage` および `folder` などのオプションのクエリ パラメータを含めることができます。*