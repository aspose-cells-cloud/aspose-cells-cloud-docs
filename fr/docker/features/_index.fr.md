---
title: "Fonctionnalités de base d'Aspose.Cells Cloud Docker : conversion de classeurs, fusion, découpage, protection, traitement des données, et plus encore."
second_title: "Document"
ArticleTitle: "Fonctionnalités de base d'Aspose.Cells Cloud Docker"
linktitle: "Fonctionnalités"
type: docs
url: /fr/docker-container-features/
description: "Exécutez localement l’API Aspose.Cells Cloud à l’aide du conteneur Docker Aspose.Cells Cloud — un service conteneurisé basé sur Docker, offrant un traitement complet des classeurs, une confidentialité renforcée et la possibilité de fonctionner hors ligne, sans recourir au cloud public d’Aspose."
weight: 30
keywords:
  - Aspose.Cells
  - Docker
  - Conversion de classeurs
  - Traitement Excel
  - Export PDF
  - Gestion CSV
  - API REST
  - Service conteneurisé
  - Cloud privé
  - Traitement hors ligne
---

## Qu’est-ce que le conteneur Docker Aspose.Cells Cloud ?

Le conteneur Docker Aspose.Cells Cloud est un service conteneurisé fourni par Aspose, fondé sur Docker, qui vous permet de déployer les fonctionnalités de l’API Aspose.Cells Cloud dans des environnements locaux ou en cloud privé, sans dépendre des services cloud publics d’Aspose.

## Pourquoi utiliser le conteneur Docker Aspose.Cells Cloud ?

Le conteneur Docker Aspose.Cells Cloud est un service puissant de traitement de classeurs, conteneurisé et prenant en charge :

### Fonctionnalités de base

- Lecture et écriture de fichiers Excel (XLS, XLSX, CSV, ODS, etc.)
- Calculs de formules, graphiques, mise en forme conditionnelle, tableaux croisés dynamiques, etc.
- Conversion de formats (par exemple Excel vers PDF, HTML, images, etc.)
- Opérations sur les cellules, paramétrage des styles, gestion des feuilles de calcul, etc.

Le conteneur Docker Aspose.Cells Cloud encapsule ces fonctionnalités sous forme d’une API RESTful, puis les intègre dans une image Docker, vous permettant de l’exécuter sur votre propre infrastructure.

### Avantages principaux

| Bénéfices                      | Description                                                                 |
| ------------------------------ | --------------------------------------------------------------------------- |
| Confidentialité et sécurité des données | Tous les traitements de fichiers s’effectuent au sein de votre réseau privé ; aucune donnée n’est envoyée vers un cloud tiers. |
| Disponibilité hors ligne       | Ne dépend pas du cloud public d’Aspose, convient aux réseaux intranet ou aux environnements isolés. |
| Évolutivité                    | Facilement extensible via Docker/Kubernetes.                                |
| API unifiée                    | Complètement compatible avec l’API publique d’Aspose.Cells Cloud ; aucune modification de code n’est requise. |
| Contrôle des licences          | Prend en charge deux types d’autorisation ; choisissez celle qui correspond à votre situation. |

## Comment utiliser le conteneur Docker Aspose.Cells Cloud ?

Consultez le guide utilisateur — [Comment utiliser le conteneur Docker Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker-developer-guide/#run-asposecells-cloud-docker-container).

**Prérequis**

- Docker Engine 20.10 ou version ultérieure installé sur la machine hôte.  
- Au moins 2 Go de RAM et 2 cœurs CPU alloués au conteneur pour des charges de travail typiques.  
- Un fichier de licence valide Aspose.Cells Cloud (ou un jeton d’accès) placé dans un répertoire qui sera monté dans le conteneur.

**Démarrage rapide**

1. Extraire l’image Docker : `docker pull aspose/cells-cloud`.  
2. Lancer le conteneur, en montant les répertoires de licence et de données, par exemple :  
   ```bash
   docker run -d -p 8080:80 \
     -v /path/to/license:/app/license \
     -v /path/to/data:/app/data \
     aspose/cells-cloud
   ```  
3. Accéder à l’API REST via `http://localhost:8080/v3.0/`. Pour une utilisation détaillée de l’API, voir la [documentation de référence de l’API Aspose.Cells Cloud](https://docs.aspose.cloud/cells/api-reference/).

## Document de référence

- [Comment configurer le stockage du conteneur Docker Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/docker/storage/)