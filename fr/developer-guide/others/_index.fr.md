---
title: "Aspise.Cells Cloud Web API – Autres fonctionnalités : Vérification de l'état de santé, Récupération de la clé publique"
linktitle: "Autres fonctionnalités"
ArticleTitle: "Autres fonctionnalités : Vérification de l'état de santé, Récupération de la clé publique"
second_title: "Document"
type: docs
url: /fr/other-features/
keywords: "Aspose.Cells, API cloud, vérification de l'état de santé, clé publique, jeton d'accès, Excel, REST"
description: "Découvrez les autres fonctionnalités d’Aspose.Cells Cloud : le point de terminaison de vérification de l’état de santé du service, la récupération de la clé publique et la génération de jetons afin de sécuriser vos intégrations avec l’API Excel."
weight: 180
---

**Conditions préalables** – Pour utiliser les fonctionnalités listées ci-dessous, vous devez disposer d’un abonnement Aspose Cloud valide ainsi que d’une paire **Client ID** / **Client Secret** active pour l’authentification.

Ces « Autres fonctionnalités » fournissent des opérations essentielles de support pour l’API Aspose.Cells Cloud, telles que la confirmation de la disponibilité du service, la récupération des clés cryptographiques et l’obtention de jetons d’accès. Elles sont généralement appelées avant d’utiliser les points de terminaison liés aux classeurs.

- **[Vérification de l’état de santé du service Aspose.Cells Cloud](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  Vérifiez que le service Aspose.Cells Cloud est accessible et fonctionne correctement. Un appel réussi renvoie **HTTP 200** avec le JSON `{ "status": "OK" }`. Utilisez ce point de terminaison au début de votre flux de travail afin d’éviter des échecs inutiles.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">En savoir plus</a>

- **[Obtenir l’état d’exécution d’Aspose.Cells Cloud](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  Récupérez l’état d’exécution actuel du service. La réponse indique si l’API est pleinement opérationnelle, en mode maintenance ou confrontée à des problèmes.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">En savoir plus</a>

- **[Récupération de la clé publique](https://docs.aspose.cloud/cells/get-public-key/)**  
  Obtenez la clé publique RSA (format PEM) utilisée pour vérifier les jetons JWT émis par Aspose.Cells Cloud. Cette clé est nécessaire lorsque vous valider les jetons côté serveur.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">En savoir plus</a>

- **[Obtention d’un jeton d’accès avec Client ID et Client Secret](https://docs.aspose.cloud/cells/post-access-token/)**  
  Générez un jeton d’accès OAuth 2.0 à l’aide du type d’octroi **client_credentials**. Incluez votre **Client ID** et **Client Secret** dans le corps de la demande ; la réponse contient `access_token`, `token_type` et `expires_in`. Ce jeton doit être fourni dans l’en-tête `Authorization` pour toutes les appels API ultérieurs.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">En savoir plus</a>

---