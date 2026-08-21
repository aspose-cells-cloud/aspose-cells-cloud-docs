---
title: "Fusionner plusieurs fichiers Excel en un seul classeur – API Aspose.Cells Cloud"
second_title: "Document"
articleTitle: "Combiner plusieurs fichiers Excel en un seul – Fusion par lots de classeurs vers plus de 30 formats"
linktype: "Fusionner des classeurs"
type: docs
url: /fr/merge-spreadsheets/
keywords: "Aspose.Cells, fusionner des classeurs, API Excel, classeur cloud, fusion par lots, conversion PDF, fusion CSV, fusion ODS, référence API, SDK"
description: "Fusionner plusieurs fichiers locaux Excel, CSV ou ODS en un seul classeur, puis convertir le résultat vers plus de 30 formats (PDF, HTML, etc.) à l’aide d’Aspose.Cells Cloud. Inclut l’endpoint, les paramètres, un guide d’authentification et des exemples d’SDK."
weight: 100
---

Fusionnez plusieurs fichiers locaux Excel, CSV ou ODS en un seul classeur, puis convertissez-le vers plus de 30 formats de sortie à l’aide de l’API Aspose.Cells Cloud.

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement       | Description                                                                                       |
| ---------------- | ------- | ----------------- | ------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData          | Le fichier de classeur local à télécharger. Prend en charge XLSX, XLS, CSV, ODS, etc.            |
| outFormat        | String  | Query             | Format de sortie souhaité (par ex. `XLSX`, `PDF`, `CSV`, `HTML`). Prend en charge plus de 30 formats. |
| mergeInOneSheet  | Boolean | Query             | `true` → toutes les données fusionnées dans une seule feuille ; `false` → chaque feuille originale est conservée. |
| outPath          | String  | Query (optionnel) | Chemin du dossier cloud où le fichier fusionné sera enregistré. Si omis, l’emplacement par défaut est utilisé. |
| outStorageName   | String  | Query             | Nom du stockage cloud à utiliser (par défaut ou personnalisé).                                   |
| fontsLocation    | String  | Query (optionnel) | Dossier cloud contenant les polices personnalisées pour un rendu correct en PDF ou image.        |
| region           | String  | Query (optionnel) | Région (locale) pour le formatage des nombres, dates et devises (par ex. `fr-FR`, `en-US`, `zh-CN`). |
| password         | String  | Query (optionnel) | Mot de passe pour ouvrir un classeur protégé.                                                    |

### **Réponse**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

Le fichier peut être téléchargé directement ou enregistré à l’emplacement spécifié par `outPath`.

**Détails de la réponse en cas de succès**

| Code d’état | Type de contenu          | Description                                    |
| ----------- | ------------------------ | ---------------------------------------------- |
| 200 OK      | `application/octet-stream` | Flux binaire du fichier classeur fusionné.     |

**Codes d’état HTTP**

| Code | Signification             | Description                                                     |
| ---- | ------------------------- | --------------------------------------------------------------- |
| 200  | OK                        | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte        | Paramètres manquants ou non valides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé              | Jeton JWT invalide ou manquant.                                 |
| 413  | Charge utile trop grande   | Le fichier téléchargé dépasse la taille limite.                |
| 500  | Erreur interne du serveur  | Erreur inattendue du serveur.                                   |

## Où faut-il utiliser l’API de fusion de classeurs ?

### **Éducation et applications académiques**

- **Correction des devoirs étudiants** – Fusionner plusieurs fichiers de devoirs étudiants pour des commentaires et une notation unifiés.
- **Collecte de données de recherche** – Consolidation des classeurs de données provenant de différents groupes expérimentaux.
- **Création de supports pédagogiques** – Fusionner des exercices provenant de plusieurs chapitres dans un seul classeur de banque de questions.

### **Traitement et analyse de données**

- **Intégration de petits jeux de données** – Fusionner des fichiers CSV ou Excel exportés à partir de sources variées.
- **Prétraitement pour l’analyse de données** – Combiner les fichiers de données pertinents avant l’analyse.
- **Remplissage de modèles de rapports** – Remplir des modèles de rapports prédéfinis avec les données fusionnées.

### **Développement et support technique**

- **Préparation de données de test** – Fusionner plusieurs fichiers de cas de test pour les tests automatisés.
- **Analyse de journaux système** – Consolidation des rapports Excel contenant les journaux système provenant de différentes périodes.
- **Gestion de configuration** – Fusionner plusieurs classeurs de configuration en un seul fichier de configuration unifié.

## Pourquoi utiliser l’API de fusion de classeurs ?

- **Adaptée aux développeurs** – Des bibliothèques SDK sont disponibles pour de nombreux langages, réduisant l’effort de développement par rapport à la création d’une solution personnalisée.
- **Réduction des coûts de main-d’œuvre** – Élimine le besoin de personnel dédié à la consolidation manuelle des documents.
- **Paiement à l’usage** – Vous ne payez que pour les appels API effectués ; aucun investissement initial requis.
- **Coûts de maintenance nuls** – Aucun serveur à maintenir, aucune mise à jour logicielle à effectuer, aucune préoccupation de compatibilité.

## Comment utiliser l’API de fusion de classeurs avec les SDK ?

### Spécification OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">spécification OpenAPI</a> fournit une description lisible par machine de l’API, permettant des interactions REST directes.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L’exemple suivant montre comment effectuer des appels vers l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/chemin/vers/Book1.xlsx" \
  -F "Spreadsheet=@/chemin/vers/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (encodé en Base64)",
  "contentType": "type MIME",
  "fileDownloadName": "nom de fichier facultatif"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation des SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et permet d’importer des données dans une feuille de calcul à l’aide de code concis. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}