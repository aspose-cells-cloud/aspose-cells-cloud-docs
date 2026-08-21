---
title: "Aspose.Cells Cloud Docker イメージのダウンロード"  
second_title: "ドキュメント"  
ArticleTitle: "Aspose.Cells Cloud Docker イメージのダウンロード"  
linktitle: "イメージのダウンロード"  
type: docs  
url: /docker/downloads/  
description: "Windows Server 2016/2019 および Linux 向けの最新 Aspose.Cells Cloud Docker イメージを入手しましょう。ローカル環境でコンテナを実行するためのステップ・バイ・ステップの手順、前提条件、およびセキュリティに関するヒントを確認してください。"  
weight: 30  
keywords: "Aspose.Cells, Cloud, Docker, container, image, download, Windows Server, Linux, REST API"  
---  

## 概要  

`aspose/cells-cloud` – **Aspose.Cells Cloud** REST API をホストする公式 Docker イメージです。このイメージを使用すると、スプレッドシート処理エンジン全体をコンテナ内で実行でき、Aspose のパブリッククラウドサービスに依存することなく、オフラインまたはプライベートクラウド環境でのデプロイが可能になります。

**最終更新日:** 2026‑06‑30  

**クイックスタート チェックリスト**

- Docker Engine のバージョンが 20.10 以降であることを確認してください。  
- 使用する OS に適したイメージをプルしてください（以下の各セクションを参照）。  
- 環境変数 `ASPOSE_CLIENT_ID` および `ASPOSE_CLIENT_SECRET` を設定してください。  
- コンテナを実行し、ポート 8080 を内部ポート 80 にマッピングしてください。  

---  

## 前提条件  

| 必須項目 | 詳細 |
|----------|------|
| **Docker Engine** | ホスト OS に Docker 20.10 以降がインストールされていること。 |
| **オペレーティング システム** | Windows Server 2016、Windows Server 2019、または最新の Linux ディストリビューション。 |
| **Docker Hub アクセス** | 有効な Docker Hub アカウント（オプションですが、プライベートイメージをプルする場合は推奨されます）。プライベートリポジトリからプルする場合は、`docker login` を実行してください。 |
| **Aspose Cloud 認証情報** | `ASPOSE_CLIENT_ID` および `ASPOSE_CLIENT_SECRET` – Aspose Cloud ダッシュボードから取得してください。 |

> **ヒント:** `docker --version` コマンドで Docker のインストール状態を確認してください。  

---  

## Windows Server 2016  

```powershell
docker pull aspose/cells-cloud:ltsc2016.21.9
```

---  

## Windows Server 2019  

```powershell
docker pull aspose/cells-cloud:ltsc2019.21.9
```

---  

## Linux  

```sh
docker pull aspose/cells-cloud:linux.21.9
```

---  

## コンテナの実行  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=YOUR_CLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=YOUR_CLIENT_SECRET \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **環境変数** – `ASPOSE_CLIENT_ID` および `ASPOSE_CLIENT_SECRET` は、API が必要とする認証情報を提供します。  
* **ポートマッピング** – コンテナはポート 80 を公開します。ホスト側のポート（例：8080）にマッピングすることで、サービスにアクセスできます。  
* **デタッチモード (`-d`)** – コンテナをバックグラウンドで実行します。  

---  

## バージョン管理と更新  

| OS | タグ | リリース日 | 最新バージョンの取得方法 |
|----|------|------------|--------------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:linux.latest` |

> **注意:** タグ `21.9` は現在の安定版リリースです。最新バージョンについては、`latest` タグを使用するか、[Aspose.Cells Cloud リリースノート](/cells/release-notes/) を確認してください。  

---  

## 検証とセキュリティ  

* **イメージダイジェストの確認**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **脆弱性スキャン**（推奨）  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **ベストプラクティス** – Docker を最新の状態に保ち、必要な最小限の権限でコンテナを実行し、既知の CVE を定期的にスキャンしてください。  

* **構造化データ（JSON-LD）の例**  

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Aspose.Cells Cloud Docker イメージ",
    "operatingSystem": "Windows Server 2016/2019, Linux",
    "softwareVersion": "21.9",
    "downloadUrl": "https://hub.docker.com/r/aspose/cells-cloud",
    "offers": {
      "price": "0",
      "priceCurrency": "USD"
    }
  }
  </script>
  ```

---  

## 一般的な問題とトラブルシューティング  

| 症状 | 考えられる原因 | 解決策 |
|------|----------------|--------|
| `docker: command not found` | Docker がインストールされていない、または PATH が設定されていない | Docker をインストールして、ターミナルを再起動してください。 |
| プル時の認証エラー | `docker login` の実行漏れ、または不正な認証情報 | 有効な Docker Hub 認証情報を使用して `docker login` を実行してください。 |
| コンテナが直ちに終了する | 必須の環境変数が設定されていない | **コンテナの実行**セクションに示された方法で `ASPOSE_CLIENT_ID` および `ASPOSE_CLIENT_SECRET` を指定してください。 |
| ホスト側のポート競合 | ホスト側のポートが既に使用中 | 別のホストポートを選択してください（例：`-p 8081:80`）。 |

---  

## 関連項目  

* [Aspose.Cells Cloud API ドキュメント](/cells/cloud/api/)  
* [Aspose.Cells Cloud リリースノート](/cells/release-notes/) – バージョン 21.9 以降の詳細な変更ログ。  
* [Aspose.Cells Docker コンテナの機能](/cells/docker/features/)  
* [Aspose.Cells Docker イメージタグ一覧](/cells/docker/tag-list/)  

---  

*Aspose Cloud エンジニアリングチームが執筆。*