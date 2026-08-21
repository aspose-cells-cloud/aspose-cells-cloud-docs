---
title: "Renommer une feuille de calcul dans Excel – API Aspose.Cells Cloud"
second_title: "Document"
articleTitle: "Comment renommer des feuilles de calcul dans Excel – Modifier les noms des onglets"
linktype: "Renommer une feuille de calcul dans un classeur"
type: docs
url: /fr/rename-worksheet-in-spreadsheet/
keywords: "renommer une feuille de calcul, Aspose.Cells Cloud, API Excel, classeur, SDK, API REST"
description: "Renommez facilement des feuilles de calcul Excel via l’API Aspose.Cells Cloud. Découvrez les paramètres requis, voyez des exemples cURL et obtenez du code SDK pour C#, Java, Python et plus encore."
weight: 100
---

Renommez dynamiquement les feuilles de calcul dans des classeurs Excel à l’aide de l’API Aspose.Cells Cloud. Modifiez les noms des feuilles, mettez à jour les libellés d’onglets en temps réel et automatisiez l’organisation des classeurs grâce à des appels d’API REST. Utile pour la standardisation de documents et l’automatisation des flux de travail.

## Renommer une feuille de calcul via l’API Classeur

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName={sourceName}&targetName={targetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

**Exemple cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Feuil1&targetName=Rapport_T1" \
     -H "Authorization: Bearer {access_token}" \
     -F "spreadsheet=@monClasseur.xlsx"
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre   | Type   | Emplacement | Description                                                                                                                                                                                                       |
| ------------------ | ------ | ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Fichier | FormData    | **Requis**. Le fichier de classeur Excel (.xlsx, .xls, etc.) contenant la feuille à renommer.                                                                                                                   |
| **sourceName**     | Chaîne  | Query       | **Requis**. Le nom actuel de la feuille de calcul que vous souhaitez renommer.                                                                                                                                  |
| **targetName**     | Chaîne  | Query       | **Requis**. Le nouveau nom à attribuer à la feuille de calcul. Doit respecter les règles de nommage d’Excel (pas de `:`, `\`, `?`, `*`, `[`, `]`) et être unique dans le classeur.                               |
| **outPath**        | Chaîne  | Query       | **Facultatif**. Le chemin du dossier cible dans le stockage cloud où le classeur renommé sera enregistré. Si `null` ou omis, le service enregistre le fichier dans le même dossier que le classeur source (ou dans un chemin par défaut). |
| **outStorageName** | Chaîne  | Query       | **Facultatif**. L’identifiant du service de stockage cloud configuré (par exemple, `ArchiveStorage`). Si omis, le stockage par défaut est utilisé.                                                              |
| **region**         | Chaîne  | Query       | **Facultatif**. Le paramètre de localisation (par exemple, `fr-FR`) pouvant influencer l’encodage des caractères ou les conventions de nommage régionales.                                                       |
| **password**       | Chaîne  | Query       | **Facultatif**. Le mot de passe de déchiffrement nécessaire pour ouvrir et modifier un classeur protégé par mot de passe. À omettre si le fichier n’est pas chiffré.                                               |

**Remarques** : Les noms de feuilles sont limités à 31 caractères et ne peuvent pas contenir les caractères `:`, `\`, `?`, `*`, `[` ni `]`.

### Réponse

Une requête réussie renvoie un objet JSON contenant des informations d’état et un lien vers le fichier renommé.

```json
[
  {
    "Name": "FichierRéponse",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Codes d’état HTTP**

| Code | Signification         | Description                                                      |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT non valide ou manquant.                                |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.                      |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                       |

## À quoi sert l’API Renommer une feuille de calcul dans un classeur ?

- **Génération de rapports et standardisation de marque** – Lors de la génération automatique de rapports clients, les noms génériques de feuilles (par exemple, `Feuil1`) sont remplacés par des noms spécifiques au client (par exemple, `AcmeCorp_Rapport_T1`) afin d’assurer une livraison professionnelle.
- **Standardisation des pipelines de traitement de données** – Dans les flux de travail ETL, les feuilles exportées avec des noms irréguliers sont renommées selon des noms normalisés tels que `DonnéesBrutes` ou `DonnéesNettoyées`, pour satisfaire aux exigences des analyses en aval.
- **Livraison de contenu multilingue** – En fonction de la préférence linguistique de l’utilisateur, les noms des feuilles sont localisés (par exemple, `données` ou `data`) avant la livraison du fichier, offrant ainsi une expérience personnalisée.

## Pourquoi utiliser l’API Renommer une feuille de calcul dans un classeur ?

- **Convivial pour les développeurs** – Propose des SDK pour plusieurs langages, accompagnés d’une documentation complète, facilitant l’intégration par rapport à la mise en place d’une solution personnalisée.
- **Réduction de la charge de travail** – Automatise le renommage des feuilles, réduisant ainsi l’effort manuel.
- **Modèle de tarification à l’usage** – Facture uniquement les appels API, éliminant les coûts initiaux de licence.
- **Aucune maintenance serveur** – En tant que service cloud, il supprime le besoin d’héberger et de maintenir des serveurs ou d’appliquer des mises à jour logicielles.
- **Support de l’automatisation** – Facilite la standardisation automatisée des documents dans les flux de travail.

## Comment utiliser l’API Renommer une feuille de calcul dans un classeur avec les SDK

### Spécification OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> décrit une interface de programmation accessible publiquement, permettant des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sheetName=Feuil1&destName=NouvelleFeuille" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/chemin/vers/entrée.xlsx"
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

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Le SDK masque les détails HTTP sous-jacents, vous permettant de renommer des feuilles avec un minimum de code. Reportez-vous au dépôt GitHub pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}

---