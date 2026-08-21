---
title: "Aspose.Cells Cloud – API Web de fractionnement de feuilles de calcul – Diviser un classeur Excel en plusieurs fichiers dans plus de 30 formats"
second_title: "Document"
ArticleTitle: "Fractionner un fichier Excel dans le cloud pour créer des fichiers distincts et exporter vers plus de 30 formats"
linktitle: "Fractionner une feuille de calcul distante dans le cloud"
type: docs
url: /fr/split-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, fractionner un classeur Excel, outil de fractionnement de feuille de calcul, API cloud, exporter vers PDF, exporter vers CSV, exporter vers JSON, export multiformat, traitement de feuilles de calcul dans le cloud"
description: "Utilisez l’API Aspose.Cells Cloud pour fractionner un classeur Excel stocké dans le stockage cloud en feuilles de calcul individuelles, puis exporter chaque partie vers plus de 30 formats tels que PDF, CSV, JSON, XLSX, HTML, ODS et XPS."
weight: 100
---

Divisez un grand classeur Excel stocké dans le cloud en fichiers distincts par feuille de calcul, puis exportez chaque partie vers plus de 30 formats de sortie tels que PDF, CSV, JSON, ODS et XPS à l’aide d’Aspose.Cells Cloud.

## **API de fractionnement de feuille de calcul distante**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                  |
| :--------------- | :------ | :----------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| name             | String  | Chemin                                                 | Le nom du fichier de classeur (par exemple, `data.xlsx`) à fractionner, situé dans le dossier spécifié du stockage cloud.                                   |
| folder           | String  | Chaîne de requête                                      | Le chemin du dossier du stockage cloud où le classeur source est stocké.                                                                                    |
| from             | Integer | Chaîne de requête                                      | L’index de départ (à partir de 0) de la feuille de calcul pour l’opération de fractionnement. Par exemple, `0` indique la première feuille de calcul.      |
| to               | Integer | Chaîne de requête                                      | L’index de fin (à partir de 0) de la feuille de calcul pour l’opération de fractionnement. Par exemple, `2` fractionne les feuilles de calcul 0, 1 et 2.    |
| outFormat        | String  | Chaîne de requête                                      | Le format de fichier de sortie pour les fichiers fractionnés. Les formats pris en charge incluent `XLSX`, `PDF`, `CSV`, `JSON`, `HTML` et plus de 30 autres. |
| storageName      | String  | Chaîne de requête                                      | _(Facultatif)_ Le nom du stockage cloud où réside le classeur source. Si omis, le stockage cloud par défaut est utilisé.                                    |
| outPath          | String  | Chaîne de requête                                      | _(Facultatif)_ Le chemin du dossier cible dans le stockage cloud où les fichiers fractionnés seront enregistrés. Si omis, les fichiers sont enregistrés dans le dossier source. |
| outStorageName   | String  | Chaîne de requête                                      | Le nom du stockage cloud où les fichiers fractionnés de sortie seront stockés.                                                                              |
| fontsLocation    | String  | Chaîne de requête                                      | _(Facultatif)_ Spécifie un chemin personnalisé vers un dossier cloud contenant les fichiers de police pour un rendu correct du texte dans les sorties PDF/images. |
| region           | String  | Chaîne de requête                                      | _(Facultatif)_ Définit la locale pour le formatage des nombres, dates et devises dans les fichiers de sortie (par exemple, `"en-US"`, `"zh-CN"`, `"de-DE"`). |
| password         | String  | Chaîne de requête                                      | _(Facultatif)_ Si le classeur source est protégé par mot de passe, fournissez le mot de passe pour ouvrir le fichier.                                        |

## **Réponse**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Le fichier peut être téléchargé directement ou enregistré à l’emplacement spécifié par `outPath`.

**Détails de la réponse en cas de succès**

| Code d’état | Type de contenu             | Description                                        |
| ----------- | --------------------------- | -------------------------------------------------- |
| 200 OK      | `application/octet-stream`  | Flux binaire du fichier de classeur fusionné.     |

**Codes d’état HTTP**

| Code | Signification              | Description                                                             |
| ---- | -------------------------- | ----------------------------------------------------------------------- |
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                                         |
| 413  | Charge utile trop grande   | Le fichier téléchargé dépasse la limite de taille.                     |
| 500  | Erreur interne du serveur  | Erreur serveur inattendue.                                              |

## À quoi sert l’API de fractionnement de feuille de calcul distante ?

- **Distribution des données par service** : Fractionner un classeur unifié contenant des données provenant de plusieurs services en fichiers spécifiques à chaque service.
- **Distribution des rapports régionaux** : Fractionner les états de ventes nationaux en fichiers régionaux distincts selon la région.
- **Distribution avec masquage des données clients** : Fractionner un classeur contenant des informations sensibles en un fichier dédié avec accès limité aux données client.
- **Fractionnement de rapports périodiques** : Fractionner automatiquement les rapports synthétiques en rapports hebdomadaires ou quotidiens chaque mois.
- **Distribution multiformat** : Fractionner un fichier Excel unique en plusieurs versions au format PDF, CSV, JSON, etc., simultanément.
- **Fractionnement basé sur des modèles** : Fractionner des fichiers de données en fichiers de sortie normalisés selon des modèles prédéfinis.
- **Prétraitement des sources de données** : Fractionner le fichier Excel en fichier CSV standardisé avant de charger les données dans la base de données.
- **Préparation des données pour l’API** : Fractionner de grands ensembles de données en lots plus petits, adaptés au transfert via API.
- **Distribution de données aux microservices** : Fractionner le fichier de données central en fichiers de données séparés requis par chaque microservice.

## Pourquoi utiliser l’API de fractionnement de feuille de calcul distante ?

- **Développeur-friendly** : Aspose.Cells Cloud propose des bibliothèques SDK dans de nombreux langages, ce qui permet un développement rapide, accompagné d’une documentation complète. Comparé à la création de solutions personnalisées de rendu graphique, cela réduit considérablement la charge de travail de développement.
- **Réduction des coûts de main-d’œuvre** : Diminue le besoin de postes dédiés à la consolidation de documents.
- **Pay-per-use** : Aucun investissement initial ; vous ne payez que pour les appels API effectivement utilisés.
- **Zéro coût de maintenance** : Aucune maintenance de serveurs, mise à jour logicielle ou gestion des problèmes de compatibilité.
- **Préservation de la mise en forme Excel complexe** dans un format PDF universellement accessible.

## Comment utiliser l’API de fractionnement de feuille de calcul distante avec les SDK ?

### Spécification de l’API de fractionnement de feuille de calcul distante

La [Spécification de l’API de fractionnement de feuille de calcul distante](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) définit une interface de programmation publiquement accessible et permet des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Report.xlsx/split/spreadsheet?folder=Input&outFormat=PDF&from=0&to=2" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de fractionner la feuille de calcul stockée dans le cloud en fichiers distincts à l’aide d’un code concis.  
Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.  
Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{</tab>}}
{{< /tabs >}}