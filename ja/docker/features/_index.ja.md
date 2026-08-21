---
title: "Aspose.Cells Cloud Docker のコア機能：スプレッドシートの変換、結合、分割、保護、データ処理など"
second_title: "ドキュメント"
articleTitle: "Aspose.Cells Cloud Docker のコア機能"
linktitle: "機能"
type: docs
url: /ja/docker-container-features/
description: "Aspose.Cells Cloud Docker コンテナを使用して、Aspose.Cells Cloud API をローカル環境で実行します。Docker ベースのコンテナ化サービスであり、Aspose のパブリッククラウドを使用せずに、完全なスプレッドシート処理、プライバシー保護、オフライン対応を実現します。"
weight: 30
keywords:
  - Aspose.Cells
  - Docker
  - スプレッドシート変換
  - Excel 処理
  - PDF エクスポート
  - CSV 処理
  - REST API
  - コンテナ化サービス
  - プライベートクラウド
  - オフライン処理
---

## Aspose.Cells Cloud Docker コンテナとは？

Aspose.Cells Cloud Docker コンテナは、Aspose が提供するコンテナ化サービスであり、Docker をベースとしています。このサービスにより、Aspose のパブリッククラウドサービスに依存せずに、Aspose.Cells Cloud API の機能をローカル環境またはプライベートクラウド環境にデプロイできます。

## なぜ Aspose.Cells Cloud Docker コンテナを使用するのですか？

Aspose.Cells Cloud Docker コンテナは、スプレッドシート処理を実行する強力なサービスコンテナであり、以下の機能をサポートします。

### コア機能

- Excel ファイルの読み書き（XLS、XLSX、CSV、ODS など）
- 数式計算、チャート、条件付き書式、ピボットテーブルなど
- フォーマット変換（Excel を PDF、HTML、画像などに変換）
- セル操作、スタイル設定、ワークシート管理など

Aspose.Cells Cloud Docker コンテナは、これらの機能を RESTful API としてカプセル化し、Docker イメージとしてパッケージ化することで、独自のインフラストラクチャ上で実行可能にします。

### 主な利点

| 利点                   | 説明                                                                 |
| ---------------------- | ------------------------------------------------------------------- |
| データのプライバシーとセキュリティ | すべてのファイル処理がプライベートネットワーク内で実行されるため、サードパーティのクラウドにファイルをアップロードする必要がありません。 |
| オフライン対応         | Aspose パブリッククラウドに依存しないため、イントラネットや分離環境でも利用可能です。 |
| スケーラビリティ       | Docker/Kubernetes を通じて簡単にスケールアウトできます。             |
| 统一された API         | Aspose.Cells Cloud パブリック API と完全に互換性があり、コード変更は不要です。 |
| ライセンス管理         | 2 種類の認証方式をサポートしており、状況に応じて適切な方式を選択できます。 |

## Aspose.Cells Cloud Docker コンテナの使用方法

ユーザー手册を参照してください：[Aspose.Cells Cloud Docker コンテナの使用方法](https://docs.aspose.cloud/cells/docker-developer-guide/#run-asposecells-cloud-docker-container)

**前提条件**

- ホストマシンに Docker Engine 20.10 以降がインストールされていること。  
- 典型的なワークロードに対して、コンテナに最低 2 GB の RAM と 2 個の CPU コアを割り当てること。  
- 有効な Aspose.Cells Cloud ライセンスファイル（またはアクセストークン）を、コンテナにマウントされるディレクトリに配置すること。

**クイックスタート**

1. Docker イメージをプルします：`docker pull aspose/cells-cloud`  
2. ライセンスとデータディレクトリをマウントしてコンテナを実行します。例：  
   ```bash
   docker run -d -p 8080:80 \
     -v /path/to/license:/app/license \
     -v /path/to/data:/app/data \
     aspose/cells-cloud
   ```  
3. REST API に `http://localhost:8080/v3.0/` でアクセスします。API の詳細な使用方法については、[Aspose.Cells Cloud API リファレンス](https://docs.aspose.cloud/cells/api-reference/) を参照してください。

## 参考ドキュメント

- [Aspose.Cells Cloud Docker コンテナのストレージ設定方法](https://docs.aspose.cloud/cells/docker/storage/)