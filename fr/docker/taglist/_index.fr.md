---
title: "Balises d’image Docker d’Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Balises d’image Docker d’Aspose.Cells Cloud"
linktitle: "Balises d’image"
type: docs
url: /fr/docker/tag-list/
description: "Trouvez les dernières balises d’image Docker d’Aspose.Cells Cloud pour Windows Server (2016‑2022) et Linux. Obtenez les commandes de pull, les détails d’architecture et les notes de mise à niveau en un seul endroit."
weight: 30
keywords:
  - "Balises d’image Docker d’Aspose.Cells Cloud"
  - "Commandes docker pull"
  - "Balises Docker pour Windows Server"
  - "Balises Docker pour Linux"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud fournit des images Docker prêtes à l’emploi pour Windows Server (2016, 2019, 2022) et Linux.  
Chaque image est versionnée à l’aide d’une **balise** qui identifie la version du produit ainsi que le système d’exploitation cible.  
Utilisez les balises ci-dessous pour extraire (pull) l’image exacte dont vous avez besoin, et consultez les exemples de tirage et d’exécution associés pour une prise en main rapide.

*Dernière mise à jour : 2026-07-01*

**Prérequis :** Assurez-vous que Docker Engine 20.10 ou une version ultérieure est installé, et que vous disposez d’une clé de licence valide d’Aspose.Cells Cloud. Les images sont compilées pour les versions spécifiées de Windows Server ou pour Linux x64.

## Images pour Windows Server 2016 ##

Balises | Architecture | Dockerfile | Remarque
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile non publié – consultez les [notes de version](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016) pour plus de détails sur la compilation. | Aucune nouvelle balise n’est prévue pour Windows Server 2016 ; il s’agit de la dernière version publiée.

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

Ressources complémentaires : [Téléchargement Docker](/cells/docker/downloads/), [Notes de version](/cells/release-notes/), [Prérequis](/cells/docker/prerequisites/).  
Consultez la [Vue d’ensemble de Docker](/cells/docker/) pour plus d’informations.

## Images pour Windows Server 2019 ##

Balises | Architecture | Dockerfile | Remarque
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile non publié – consultez les [notes de version](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019) pour plus de détails sur la compilation. | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

Ressources complémentaires : [Téléchargement Docker](/cells/docker/downloads/), [Notes de version](/cells/release-notes/), [Prérequis](/cells/docker/prerequisites/).  
Consultez la [Vue d’ensemble de Docker](/cells/docker/) pour plus d’informations.

## Images pour Windows Server 2022 ##

Balises | Architecture | Dockerfile | Remarque
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile non publié – consultez les [notes de version](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022) pour plus de détails sur la compilation. | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

Ressources complémentaires : [Téléchargement Docker](/cells/docker/downloads/), [Notes de version](/cells/release-notes/), [Prérequis](/cells/docker/prerequisites/).  
Consultez la [Vue d’ensemble de Docker](/cells/docker/) pour plus d’informations.

## Images Linux ##

Balises | Architecture | Dockerfile | Remarque
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile non publié – consultez les [notes de version](https://github.com/aspose-cells/dockerfiles/tree/main/linux) pour plus de détails sur la compilation. | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

Ressources complémentaires : [Téléchargement Docker](/cells/docker/downloads/), [Notes de version](/cells/release-notes/), [Prérequis](/cells/docker/prerequisites/).  
Consultez la [Vue d’ensemble de Docker](/cells/docker/) pour plus d’informations.

**Journal des modifications de version**

Balise | Modifications
---|---
`ltsc2016.23.5.0` | Dernière version pour Windows Server 2016 ; inclut des correctifs de sécurité et des améliorations de performance.
`ltsc2019.25.10.0` | Mise à jour vers Aspose.Cells 25.10.0 ; ajoute la prise en charge de nouvelles formules et des correctifs de bugs.
`ltsc2022.25.10.0` | Identique à la balise 2019, optimisée pour l’environnement d’exécution de Windows Server 2022.
`linux.25.10.0` | Image Linux de base avec Aspose.Cells 25.10.0 ; inclut des dépendances mises à jour et des optimisations spécifiques à Linux.