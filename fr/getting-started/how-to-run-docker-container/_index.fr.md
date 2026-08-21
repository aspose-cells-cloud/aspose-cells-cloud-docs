---
title: "Exécuter le conteneur Docker Aspose.Cells Cloud – Téléchargement, configuration et démarrage"
second_title: "Document"
ArticleTitle: "Comment exécuter le conteneur Docker Aspose.Cells Cloud"
LinkTitle: "Conteneur Docker"
type: docs
url: /getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: "Découvrez comment télécharger, configurer et exécuter le conteneur Docker Aspose.Cells Cloud sur Windows ou Linux. Inclut le fichier YAML Docker‑Compose, la configuration de la licence, le mappage des ports et des conseils de dépannage."
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "Conteneur Docker"
  - "Docker Compose"
  - "Clés de licence"
  - "Excel"
  - "Feuille de calcul"
  - "API cloud"
  - "Docker"
  - "Aspose Cells"
  - "API"
---

La technologie Docker est conçue pour automatiser le déploiement d’applications à l’aide de conteneurs légers. Les développeurs peuvent utiliser un conteneur Docker pour regrouper une application avec toutes ses bibliothèques et dépendances, et déployer l’ensemble en tant que package unique.

L’équipe Aspose.Cells Cloud a publié le conteneur Docker sur <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a> afin de faciliter l’utilisation de Docker par les développeurs.

**Prérequis** – Assurez-vous que Docker Engine ≥ 20.x est installé et que votre système d’exploitation (Windows 10/Server 2019/2022 ou une distribution Linux prise en charge) répond aux exigences. Une clé de licence facultative peut être fournie pour exécuter le conteneur en mode avec licence.

- Docker Engine ≥ 20.x installé  
- Système d’exploitation pris en charge (Windows 10/Server 2019/2022 ou une distribution Linux)  
- Clé de licence facultative pour le mode avec licence  

## Configuration du conteneur

### Volumes requis

| Chemin de montage dans le conteneur | Description |
| :--- | :--- |
| C:\fonts | Dossier contenant les polices à utiliser pour le rendu des documents |
| C:\data | Dossier de stockage des fichiers |

**Alternative pour Linux/macOS** – Utilisez `/fonts` et `/data` dans le conteneur, et mappez-les vers des répertoires hôtes tels que `/home/user/fonts` et `/home/user/data` lors de l’exécution du conteneur.

### Paramètres

| Nom | Description |
| :--- | :--- |
| LicensePublicKey | Clé publique de la licence |
| LicensePrivateKey | Clé privée de la licence |

Si les paramètres **License** sont omis, l’application s’exécute en mode d’essai.

### 1. Télécharger l’image Aspose.Cells Cloud

```bash
# Télécharger une version spécifique de l’image Aspose.Cells Cloud
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# Télécharger l’image Aspose.Cells Cloud pour Windows Server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# Télécharger l’image Aspose.Cells Cloud pour Windows Server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# Télécharger l’image Aspose.Cells Cloud pour Windows 11
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **Remarque :** Pour toujours obtenir la version la plus récente, vous pouvez également utiliser le tag `latest` : `docker pull aspose/cells-cloud:latest`.

### 2. Configurations pour l’outil Docker‑Compose

Vous pouvez écrire la configuration suivante dans un fichier **docker‑compose.yml** :

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # hôte 5000 → conteneur 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "votreCléPublique"
    LicensePrivateKey: "votreCléPrivée"
```

> **Remarque :** Le mappage de port `5000:80` signifie que l’API sera accessible à l’adresse `http://localhost:5000`.

### 3. Exécuter un conteneur Docker via la ligne de commande

```bash
docker run \
  -e "LicensePublicKey=votreCléPublique" \
  -e "LicensePrivateKey=votreCléPrivée" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**Dépannage :**  
- **Conflit de port :** Assurez-vous que le port 5000 sur l’hôte est libre ou changez le mappage vers un port inutilisé.  
- **Échec du chargement de la licence :** Vérifiez que les clés publique et privée sont correctement transmises en tant que variables d’environnement ou montées en tant que fichiers.  
- **Polices manquantes :** Si les documents sont rendus avec des polices incorrectes, confirmez que le répertoire des polices est correctement monté et contient les fichiers de police requis.

**Ressources associées :**  
- <a href="/cells/api/">Référence de l’API</a> | <a href="/cells/license/">Guide d’activation de la licence</a> | <a href="/cells/getting-started/">Vue d’ensemble du démarrage</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Exécuter le conteneur Docker Aspose.Cells Cloud",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-télécharger-limage-asposecells-cloud",
      "name": "Télécharger l’image Docker",
      "text": "Exécutez `docker pull aspose/cells-cloud:<version>` pour télécharger l’image requise."
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-pour-loutil-docker-compose",
      "name": "Créer un fichier docker‑compose",
      "text": "Définissez l’image, les ports, les volumes et les variables d’environnement de licence dans `docker‑compose.yml`."
    },
    {
      "@type": "HowToStep",
      "url": "#3-exécuter-un-conteneur-docker-via-la-ligne-de-commande",
      "name": "Exécuter le conteneur",
      "text": "Exécutez `docker run` avec les variables d’environnement, les montages de volumes et le mappage de port appropriés."
    }
  ]
}
```