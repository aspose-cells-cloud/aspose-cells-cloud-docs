---
title: "Excelデータ検証の操作"
second_title: "Document"
linktype: "Validations"
type: docs
url: /validations/
keywords: "Excelデータ検証、Aspose.Cells Cloud、REST API、スプレッドシート、Office Cloud"
description: "Aspose.Cells Cloud REST API を使用して、Excelデータ検証ルールをプログラムで追加、取得、更新、削除、クリアする方法を学びます。.NET、Java、Python、PHP の各言語での例を含みます。"
weight: 100
ArticleTitle: "Excelデータ検証の操作 - Aspose.Cells Cloud API ドキュメント"
---

Excelデータ検証は、Microsoft Excel の機能の一つで、ワークシートのセルに入力できる内容を制御するために使用されます。特定の日付範囲や整数のみ、さらにはドロップダウンリストを作成し、スペースを節約して単一セルに値を表示することも可能です。また、ユーザーが誤った値や無効な形式を入力した際に表示されるカスタムメッセージを定義することもできます。

例えば、ユーザーは「9:00から18:00までの会議」をスケジュールできるよう設定できます。

データ検証は、値が正の数であること、月の15日から30日の間の日付であること、今後30日以内の日付であること、25文字未満のテキストが入力されていることなどを確認するために使用できます。

### API概要

| 操作 | HTTPメソッド | エンドポイント | 説明 |
|------|--------------|----------------|------|
| 追加 | POST | `/cells/{file}/worksheets/{sheet}/validations` | 検証ルールの作成 |
| 取得 | GET | `/cells/{file}/worksheets/{sheet}/validations/{index}` | 特定のルールの取得 |
| すべて取得 | GET | `/cells/{file}/worksheets/{sheet}/validations` | すべてのルールのリスト表示 |
| 更新 | PUT | `/cells/{file}/worksheets/{sheet}/validations/{index}` | ルールの変更 |
| 削除 | DELETE | `/cells/{file}/worksheets/{sheet}/validations/{index}` | ルールの削除 |
| クリア | POST | `/cells/{file}/worksheets/{sheet}/validations/clear` | すべてのルールの削除 |

## Excelファイルでの検証の操作

- [Excelワークシートに検証ルールを追加する方法](/cells/validations/add/)
- [Excelワークシートから検証ルールを取得する方法](/cells/validations/get/)
- [Excelワークシートからすべての検証ルールを取得する方法](/cells/validations/get-all/)
- [Excelワークシートから検証ルールを削除する方法](/cells/validations/delete/)
- [Excelワークシートからすべての検証ルールをクリアする方法](/cells/validations/clear/)
- [Excelワークシート上の検証ルールを更新する方法](/cells/validations/update/)
---