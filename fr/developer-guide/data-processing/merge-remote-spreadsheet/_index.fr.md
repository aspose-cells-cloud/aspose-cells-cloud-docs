---
title: "Aspose.Cells Cloud – Fusionner des fichiers Excel dans le cloud | Combiner des classeurs via l’API"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Fusionner des fichiers Excel dans le cloud – Combiner des classeurs en ligne avec l’API Aspose.Cells Cloud"
linktitle: "Fusionner un classeur distant"
type: docs
url: /fr/merge-remote-spreadsheet/
keywords: "Aspose.Cells, fusionner Excel, API cloud, combiner classeur"
description: "Fusionner des classeurs Excel stockés dans le stockage cloud à l’aide de l’API Aspose.Cells Cloud. Spécifiez le format de sortie, le dossier cible et le mode de fusion en une seule requête HTTPS."
weight: 100
---

Fusionnez rapidement des fichiers Excel stockés dans le cloud avec d’autres classeurs à l’aide de l’API Aspose.Cells Cloud, et spécifiez le format de sortie ainsi que l’emplacement de stockage.

## API de fusion de classeur distant

Avant d’appeler cette opération, assurez-vous de disposer des éléments suivants :

- D’un **jeton d’accès JWT** valide (voir le guide d’authentification).
- Du classeur source et de tous les fichiers à fusionner uploadés dans votre stockage cloud.
- Des permissions appropriées pour lire depuis le dossier source et écrire dans le dossier cible.

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête :

| Nom du paramètre  | Type    | Chemin / Chaîne de requête / Corps HTTP | Description                                                                                                                          |
| :---------------- | :------ | :-------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------- |
| name              | String  | Chemin                                  | Le nom du fichier du classeur source à fusionner.                                                                                  |
| mergedSpreadsheet | String  | Chaîne de requête                       | Une liste séparée par des virgules des noms des fichiers classeurs à fusionner dans le classeur source.                             |
| folder            | String  | Chaîne de requête                       | Le chemin du dossier dans le stockage cloud contenant le classeur source.                                                          |
| outFormat         | String  | Chaîne de requête                       | Le format souhaité pour le fichier de sortie fusionné (par exemple, `XLSX`, `PDF`, `CSV`).                                         |
| mergeInOneSheet   | Boolean | Chaîne de requête                       | Définir sur `true` pour fusionner toutes les données sources dans une seule feuille de calcul ; `false` crée des feuilles séparées pour chaque fichier. |
| storageName       | String  | Chaîne de requête                       | _(Facultatif)_ Le nom du stockage cloud où réside le classeur source. Si omis, le stockage par défaut est utilisé.                 |
| outPath           | String  | Chaîne de requête                       | _(Facultatif)_ Le chemin du dossier cible dans le stockage cloud pour enregistrer le fichier fusionné. Si omis, le fichier est enregistré dans le dossier source. |
| outStorageName    | String  | Chaîne de requête                       | Le nom du stockage cloud utilisé pour enregistrer le fichier de sortie.                                                            |
| fontsLocation     | String  | Chaîne de requête                       | _(Facultatif)_ Chemin personnalisé du dossier contenant les fichiers de police utilisés lors de la conversion au format image/PDF. |
| region            | String  | Chaîne de requête                       | _(Facultatif)_ Paramètres régionaux/locales pour la mise en forme des dates, nombres et devises dans le fichier de sortie (par exemple, `fr-FR`, `de-DE`). |
| password          | String  | Chaîne de requête                       | _(Facultatif)_ Mot de passe requis pour ouvrir le classeur source s’il est protégé.                                                |

### Réponse

**Statut :** `200 OK`

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

Le fichier peut être téléchargé directement ou enregistré à l’emplacement spécifié par `outPath`.

**Détails de la réponse en cas de succès**

| Code d’état | Content‑Type               | Description                                   |
| ----------- | -------------------------- | --------------------------------------------- |
| 200 OK      | `application/octet-stream` | Flux binaire du fichier classeur fusionné.   |

**Codes d’état HTTP**

| Code | Signification           | Description                                                    |
| ---- | ----------------------- | -------------------------------------------------------------- |
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                |
| 413  | Charge utile trop grande | Le fichier uploadé dépasse la taille maximale autorisée.     |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                  |

## Où utiliser l’API de fusion de classeur distant ?

### Intégration de données à l’échelle entreprise

- **Consolidation des rapports multi-départements** – Consolider des rapports Excel séparés soumis par les équipes commerciales, marketing, finance, etc.
- **Synthèse des données des succursales** – Résumer les données de performance de chaque succursale dans le monde entier.
- **Consolidation des données partenaires** – Fusionner les soumissions de données de plusieurs partenaires dans un seul classeur.

### Flux de travail de traitement de documents dans le cloud

- **Traitement de fichiers dans le stockage cloud** – Fusionner directement des fichiers Excel stockés dans AWS S3, Azure Blob ou Google Cloud Storage.
- **Consolidation multi-sources** – Combiner des fichiers provenant de différents emplacements cloud dans un seul classeur.
- **Pipelines de données automatisés** – Intégrer l’API dans des processus ETL pour automatiser la fusion de fichiers.

### Automatisation de la gestion de documents

- **Consolidation de versions** – Fusionner différentes versions d’un plan de projet ou d’un classeur budgétaire.
- **Remplissage de modèles** – Insérer des fichiers de données dans des modèles de rapports standardisés.
- **Génération automatique de rapports** – Automatiser la génération hebdomadaire, mensuelle et trimestrielle de rapports synthétiques.

### Collaboration multiplateforme

- **Collaboration d’équipes distantes** – Consolider le travail soumis par des membres d’équipe dispersés géographiquement.
- **Organisation des données clients** – Fusionner des données de commande ou des retours clients provenant de plusieurs clients.
- **Résumé des informations fournisseurs** – Combiner des devis ou des informations produit provenant de plusieurs fournisseurs.

## Pourquoi utiliser l’API de fusion de classeur distant ?

- **Facile à utiliser pour les développeurs** – Aspose.Cells Cloud fournit des SDK pour de nombreux langages, ce qui réduit le temps de développement et propose une documentation complète. Comparé à la construction d’une solution personnalisée, cela diminue considérablement la charge de travail.
- **Réduction des coûts de main-d’œuvre** – Diminue la nécessité d’avoir du personnel dédié à la consolidation manuelle des documents.
- **Paiement à l’usage** – Aucun investissement initial ; vous ne payez que pour les appels à l’API que vous utilisez réellement.
- **Zéro coût de maintenance** – Aucun serveur à maintenir, aucune mise à jour logicielle à gérer, aucune préoccupation de compatibilité.

## Comment utiliser l’API de fusion de classeur distant avec les SDK ?

### Spécification de l’API de fusion de classeur distant

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet" target="_blank" rel="noopener noreferrer">spécification de l’API de fusion de classeur distant</a> décrit l’interface REST qui peut être appelée directement depuis n’importe quel client HTTP.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/merge/spreadsheet?mergedSpreadsheet=Report1.xlsx&outFormat=XLSX&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (encodé en Base64)",
  "contentType": "type MIME",
  "fileDownloadName": "nom de fichier optionnel"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle abstractise les détails de bas niveau et vous permet de fusionner un classeur dans un autre à l’aide d’un court extrait de code.  
Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}