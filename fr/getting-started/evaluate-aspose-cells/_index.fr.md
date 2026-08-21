---
title: "Évaluer Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Évaluer Aspose.Cells Cloud"
LinkTitle: "Évaluer"
type: docs
url: /evaluate-aspose-cells/
description: "Découvrez Aspose.Cells Cloud, l'API REST permettant de créer, convertir, fusionner, diviser, protéger et manipuler des fichiers Excel et d'autres formats de feuilles de calcul."
weight: 60
keywords:
  - Aspose.Cells Cloud
  - Excel API
  - REST API
  - manipulation de feuilles de calcul
  - essai gratuit
  - évaluer
---

Vous pouvez évaluer les **API REST Aspose.Cells Cloud** en créant un compte d’essai gratuit sur le Tableau de bord Aspose Cloud. Après inscription, vous recevrez un **Client Id** et un **Client Secret**, qui vous permettront d’effectuer jusqu’à 150 appels d’API par mois.

**Prérequis**  
Avant de commencer, assurez-vous de disposer d’une connexion Internet active et d’un environnement de développement pris en charge. L’API peut être appelée directement via HTTP, ou vous pouvez utiliser l’un des SDK Aspose.Cells (par exemple, .NET, Java, Python, PHP) pour une intégration plus facile.

**Étapes de démarrage rapide**

1. **Créer un compte d’essai gratuit** – visitez le [Tableau de bord Aspose Cloud](https://dashboard.aspose.cloud), inscrivez-vous et confirmez votre adresse e-mail.  
2. **Obtenir les identifiants** – localisez le *Client Id* et le *Client Secret* dans la section **Authentication** du tableau de bord.  
3. **Générer un jeton d’accès** – envoyez une requête `POST` vers `https://api.aspose.cloud/connect/token` avec vos identifiants (consultez la référence de l’API pour connaître la charge utile exacte).  
4. **Effectuer votre premier appel d’API** – incluez le jeton dans l’en-tête `Authorization: Bearer <token>` et appelez un point de terminaison simple, par exemple `GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets`.  

L’essai gratuit vous permet d’apprécier concrètement les capacités du service, vous permettant ainsi de développer et de tester rapidement vos applications sans aucun coût.

**Résumé de la référence de l’API**

| Opération | Méthode | URL | Paramètres obligatoires | Exemple de réponse |
|-----------|---------|-----|-------------------------|--------------------|
| Obtenir un jeton d’accès | POST | `https://api.aspose.cloud/connect/token` | `grant_type=client_credentials`, `client_id`, `client_secret` (encodés en `application/x-www-form-urlencoded`) | `{ "access_token": "eyJ0eXAi...", "expires_in": 3600 }` |
| Lister les feuilles de calcul | GET | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets` | chemin : `{file}` – nom du classeur téléchargé ; en-tête : `Authorization: Bearer <token>` | `{ "Worksheets": { "WorksheetList": [ { "Name": "Sheet1" }, { "Name": "Sheet2" } ] } }` |

Pour des informations détaillées sur les tarifs, les limites d’utilisation et les options de forfaits supplémentaires, consultez la page [Forfait d’essai](https://purchase.aspose.cloud/trial).