---
title: "Aspose.Cells Cloud Docker コンテナーを実行する – プル、設定、開始"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud Docker コンテナーの実行方法"
LinkTitle: "Docker コンテナー"
type: docs
url: /ja/getting-started/how-to-run-docker-container/
aliases: [  /ja/how-to-run-docker-container/ ]
description: "Windows または Linux 上で Aspose.Cells Cloud Docker コンテナーをプル、設定、実行する方法を学びます。Docker‑Compose YAML、ライセンス設定、ポートマッピング、トラブルシューティングのヒントを含みます。"
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "Docker コンテナー"
  - "Docker Compose"
  - "ライセンスキー"
  - "Excel"
  - "スプレッドシート"
  - "クラウド API"
  - "Docker"
  - "Aspose Cells"
  - "API"
---

Docker 技術は、軽量コンテナーを使用してアプリケーションのデプロイを自動化することを目的としています。開発者は Docker コンテナーを使用して、アプリケーションとそのすべてのライブラリおよび依存関係を束ね、1 つのパッケージとしてデプロイできます。

Aspose.Cells Cloud チームは、Docker ユーザーを支援するために、Docker <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a> 上に Docker コンテナーを公開しています。

**前提条件** – Docker Engine ≥ 20.x がインストールされており、オペレーティングシステム（Windows 10/Server 2019/2022、またはサポート対象の Linux ディストリビューション）が要件を満たしていることを確認してください。ライセンスモードで実行する場合、オプションでライセンスキーを指定できます。

- Docker Engine ≥ 20.x がインストールされている  
- サポート対象の OS（Windows 10/Server 2019/2022、または Linux ディストリビューション）  
- ライセンスモード用のオプションライセンスキー  

## コンテナーの設定

### 必須ボリューム

| コンテナー内のマウントパス | 説明 |
| :--- | :--- |
| C:\fonts | ドキュメントのレンダリングに使用されるフォントが格納されたフォルダー |
| C:\data | ファイルストレージ用フォルダー |

**Linux/macOS の代替案** – コンテナー内で `/fonts` および `/data` を使用し、コンテナー実行時にホストディレクトリ（例: `/home/user/fonts` および `/home/user/data`）とマッピングしてください。

### パラメーター

| 名前 | 説明 |
| :--- | :--- |
| LicensePublicKey | ライセンスの公開鍵 |
| LicensePrivateKey | ライセンスの秘密鍵 |

**License** パラメーターを省略した場合、アプリケーションはトライアルモードで実行されます。

### 1. Aspose.Cells Cloud イメージをプルする

```bash
# Aspose.Cells Cloud イメージの特定バージョンをプル
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# Windows Server 2019 向けの Aspose.Cells Cloud イメージをプル
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# Windows Server 2022 向けの Aspose.Cells Cloud イメージをプル
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# Windows 11 向けの Aspose.Cells Cloud イメージをプル
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **注意:** 最新のリリースを常に取得するには、`latest` タグをプルすることもできます: `docker pull aspose/cells-cloud:latest`。

### 2. Docker‑Compose ツールの設定

以下の設定を **docker‑compose.yml** ファイルに記述できます。

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # ホスト 5000 → コンテナー 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "yourPublicKey"
    LicensePrivateKey: "yourPrivateKey"
```

> **注意:** ポートマッピング `5000:80` は、API が `http://localhost:5000` でアクセス可能であることを意味します。

### 3. コマンドラインを使用して Docker コンテナーを実行する

```bash
docker run \
  -e "LicensePublicKey=yourPublicKey" \
  -e "LicensePrivateKey=yourPrivateKey" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**トラブルシューティング:**  
- **ポート競合:** ホストのポート 5000 が空いていることを確認するか、未使用のポートにマッピングを変更してください。  
- **ライセンス読み込み失敗:** 公開鍵と秘密鍵が環境変数として、またはファイルとして正しく渡されているか確認してください。  
- **フォント不足:** ドキュメントのフォントが正しく表示されない場合は、フォントディレクトリが正しくマウントされており、必要なフォントファイルが含まれていることを確認してください。

**関連リソース:**  
- <a href="/cells/api/">API リファレンス</a> | <a href="/cells/license/">ライセンス有効化ガイド</a> | <a href="/cells/getting-started/">入門概要</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Run Aspose.Cells Cloud Docker Container",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-pull-asposecells-cloud-image",
      "name": "Docker イメージをプルする",
      "text": "`docker pull aspose/cells-cloud:<version>` を実行して必要なイメージをダウンロードします。"
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-for-docker-compose-tool",
      "name": "docker‑compose ファイルを作成する",
      "text": "`docker‑compose.yml` にイメージ、ポート、ボリューム、ライセンス環境変数を定義します。"
    },
    {
      "@type": "HowToStep",
      "url": "#3-run-a-docker-container-using-the-command-line",
      "name": "コンテナーを実行する",
      "text": "適切な環境変数、ボリュームマウント、ポートマッピングを使用して `docker run` を実行します。"
    }
  ]
}
```