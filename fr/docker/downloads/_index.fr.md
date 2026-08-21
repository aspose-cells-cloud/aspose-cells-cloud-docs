---
title: "Téléchargement de l'image Docker Aspose.Cells Cloud"  
second_title: "Document"  
ArticleTitle: "Téléchargement de l'image Docker Aspose.Cells Cloud"  
linktitle: "Téléchargement d'image"  
type: docs  
url: /docker/downloads/  
description: "Obtenez les dernières images Docker Aspose.Cells Cloud pour Windows Server 2016/2019 et Linux. Suivez les instructions étape par étape, les prérequis et les conseils de sécurité pour exécuter le conteneur localement."  
weight: 30  
keywords: "Aspose.Cells, Cloud, Docker, conteneur, image, téléchargement, Windows Server, Linux, API REST"  
---  

## Vue d'ensemble  

`aspose/cells-cloud` – l’image Docker officielle hébergeant l’**API REST Aspose.Cells Cloud**. Cette image vous permet d’exécuter l’ensemble du moteur de traitement de feuilles de calcul à l’intérieur d’un conteneur, permettant ainsi des déploiements hors ligne ou en cloud privé sans dépendre des services cloud publics d’Aspose.  

**Dernière mise à jour :** 2026‑06‑30  

**Liste de contrôle pour une prise en main rapide**

- Vérifiez que la version de Docker Engine est égale ou supérieure à 20.10.  
- Téléchargez l’image adaptée à votre système d’exploitation (voir sections ci-dessous).  
- Définissez les variables d’environnement `ASPOSE_CLIENT_ID` et `ASPOSE_CLIENT_SECRET`.  
- Exécutez le conteneur en mappant le port 8080 du hôte vers le port 80 interne.  

---  

## Prérequis  

| Exigence | Détails |
|----------|---------|
| **Docker Engine** | Docker 20.10 ou version ultérieure installé sur le système hôte. |
| **Système d’exploitation** | Windows Server 2016, Windows Server 2019 ou toute distribution Linux récente. |
| **Accès à Docker Hub** | Un compte Docker Hub actif (facultatif mais recommandé pour les images privées). Exécutez `docker login` si vous devez tirer une image depuis un dépôt privé. |
| **Identifiants Aspose Cloud** | `ASPOSE_CLIENT_ID` et `ASPOSE_CLIENT_SECRET` – obtenez-les depuis le tableau de bord Aspose Cloud. |

> **Conseil :** Vérifiez l’installation de Docker avec `docker --version`.  

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

## Exécution du conteneur  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=VOTRE_ID_CLIENT \
  -e ASPOSE_CLIENT_SECRET=VOTRE_SECRET_CLIENT \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **Variables d’environnement** – `ASPOSE_CLIENT_ID` et `ASPOSE_CLIENT_SECRET` fournissent les identifiants requis par l’API.  
* **Mappage de ports** – Le conteneur expose le port 80 ; mappez-le à un port hôte (par exemple 8080) pour accéder au service.  
* **Mode détaché (`-d`)** – Exécute le conteneur en arrière-plan.  

---  

## Gestion des versions et mises à jour  

| Système d’exploitation | Tag | Date de publication | Comment obtenir la dernière version |
|------------------------|-----|---------------------|-------------------------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:linux.latest` |

> **Remarque :** Le tag `21.9` correspond à la version stable actuelle. Utilisez le tag `latest` ou consultez les [notes de version d’Aspose.Cells Cloud](/cells/release-notes/) pour obtenir les versions plus récentes.  

---  

## Vérification et sécurité  

* **Vérification du hachage d’image (digest)**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **Analyse de vulnérabilités** (recommandé)  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **Bonnes pratiques** – Tenez Docker à jour, exécutez les conteneurs avec les privilèges minimaux requis, et scannez régulièrement les images à la recherche de CVE connus.  

* **Données structurées (exemple JSON-LD)**  

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Image Docker Aspose.Cells Cloud",
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

## Problèmes courants et dépannage  

| Symptôme | Cause possible | Solution |
|----------|----------------|----------|
| `docker : commande introuvable` | Docker non installé ou chemin (PATH) non défini | Installez Docker et redémarrez le terminal. |
| Échec d’authentification lors du tirage d’image | `docker login` manquant ou incorrect | Exécutez `docker login` avec des identifiants Docker Hub valides. |
| Le conteneur s’arrête immédiatement | Variables d’environnement requises absentes | Fournissez `ASPOSE_CLIENT_ID` et `ASPOSE_CLIENT_SECRET` comme indiqué dans la section **Exécution du conteneur**. |
| Conflit de port sur l’hôte | Port hôte déjà utilisé | Choisissez un autre port hôte (par exemple `-p 8081:80`). |

---  

## Voir aussi  

* [Documentation de l’API Aspose.Cells Cloud](/cells/cloud/api/)  
* [Notes de version d’Aspose.Cells Cloud](/cells/release-notes/) – journal détaillé des modifications pour la version 21.9 et les versions ultérieures.  
* [Fonctionnalités du conteneur Docker Aspose.Cells](/cells/docker/features/)  
* [Tags des images Docker Aspose.Cells](/cells/docker/tag-list/)  

---  

*Rédigé par l’équipe d’ingénierie Aspose Cloud.*