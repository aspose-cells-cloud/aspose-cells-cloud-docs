---
title: "Créer une API de feuille de calcul – Aspose.Cells Cloud (v5.0) | Générer des fichiers Excel"
second_title: "Document"
ArticleTitle: "Comment créer de nouvelles feuilles de calcul Excel – Générer des fichiers vierges ou basés sur des modèles"
linktype: "Create Spreadsheet"
type: docs
url: /fr/create-spreadsheet/
keywords: "Aspose.Cells, API de feuille de calcul, créer Excel, cloud, XLSX, ODS, CSV, modèle, SDK, automatisation"
description: "Découvrez comment créer des classeurs Excel vierges ou basés sur des modèles à l’aide de l’API Aspose.Cells Cloud (v5.0). Inclut l’endpoint, les paramètres, les codes d’erreur, les étapes d’authentification et des exemples de SDK."
weight: 100
---

Créez programmatically de nouvelles feuilles de calcul Excel à l’aide de l’API Aspose.Cells Cloud. Générez des classeurs vierges ou instanciez des fichiers à partir de modèles personnalisés. L’API RESTful permet la création automatisée de fichiers Excel, idéale pour la génération de rapports, l’automatisation de documents et les flux de travail de traitement des données.

## **API de création de feuille de calcul**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre   | Type   | Emplacement | Description                                                                                                                                       |
| -------------------- | ------ | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**           | String | Query       | **Obligatoire**. Format de fichier pour la nouvelle feuille de calcul (par ex. `XLSX`, `XLS`, `ODS`, `CSV`).                                      |
| **template**         | String | Query       | **Facultatif**. Nom d’un fichier modèle stocké dans votre stockage cloud (par ex. `invoice_template.xlsx`). Si omis, un classeur vide est créé.   |
| **outPath**          | String | Query       | **Facultatif**. Chemin du dossier cible dans le stockage cloud pour le fichier généré. Si `null` ou omis, la feuille de calcul est enregistrée à l’emplacement par défaut. |
| **outStorageName**   | String | Query       | **Obligatoire**. Identifiant du stockage cloud configuré (par ex. `MyDrive`).                                                                     |
| **region**           | String | Query       | **Facultatif**. Paramètre régional (par ex. `fr-FR`) déterminant les formats par défaut des dates, des nombres et des devises.                   |
| **password**         | String | Query       | **Facultatif**. Mot de passe d’un fichier modèle chiffré. Laisser vide si le modèle n’est pas protégé.                                            |

### Réponse

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

**Codes de statut HTTP**

| Code | Signification         | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête      | Paramètres manquants ou invalides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                   |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                      |

## Où utiliser l’API de création de feuille de calcul ?

- **Initialisation d’un système de génération automatisée de rapports** – Créer un nouveau classeur vide ou générer un fichier de rapport à partir d’un modèle standard au début de chaque cycle d’automatisation quotidien/hebdomadaire.
- **Portail d’auto-service pour les utilisateurs** – Permettre aux clients de sélectionner un modèle (devis, planning de projet, etc.) et de télécharger immédiatement un fichier Excel personnalisé.
- **Exportation et distribution en masse de données** – Produire des classeurs distincts au format uniforme pour chaque jeu de données exporté, simplifiant ainsi la distribution et le traitement ultérieurs.

Pour les opérations ultérieures, telles que l’ajout de feuilles de calcul ou la remplissage des cellules, consultez les API suivantes : **Ajouter une feuille de calcul**, **Mettre à jour une cellule** et **Exporter un classeur**.

## Pourquoi utiliser l’API de création de feuille de calcul ?

- **Adapté aux développeurs** – Fournit des bibliothèques SDK pour de nombreux langages ainsi qu’une documentation détaillée, simplifiant l’intégration par rapport à la construction de solutions sur mesure.
- **Gain d’efficacité** – Permet l’automatisation de la consolidation de documents, réduisant ainsi l’effort manuel.
- **Tarification à l’usage** – Les frais sont basés sur l’utilisation de l’API, sans frais de licence initiaux.
- **Service géré** – L’API est entièrement hébergée, éliminant le besoin de maintenance de serveurs locaux ou de mises à jour logicielles.

## Comment utiliser l’API de création de feuille de calcul avec les SDK ?

### Spécification de l’API de création de feuille de calcul

La [Spécification de l’API de création de feuille de calcul](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) définit une interface de programmation accessible publiquement et permet des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels vers l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MyStorage" \
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et permet de créer la feuille de calcul avec un code concis. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}