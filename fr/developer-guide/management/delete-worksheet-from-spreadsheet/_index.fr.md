---
title: "API Web Aspose.Cells Cloud pour supprimer une feuille Excel - Supprimer des feuilles de calculs de classeurs de manière programmatique"
second_title: "Document"
ArticleTitle: "Comment supprimer des feuilles de calcul Excel - Supprimer des feuilles de classeurs"
linktype: "Supprimer une feuille de calcul à partir d’un classeur"
type: docs
url: /delete-worksheet-from-spreadsheet/
keywords: "Aspose Cells, API de suppression de feuille de calcul, suppression de feuille Excel, classeur dans le cloud, API REST"
description: "Découvrez comment supprimer une feuille de calcul à partir d’un fichier Excel à l’aide de l’API Aspose.Cells Cloud. Inclut le point de terminaison, les paramètres, des exemples cURL et des exemples SDK."
weight: 100
---

Supprimez de manière programmatique des feuilles de calcul à partir de classeurs Excel à l’aide de l’API Aspose.Cells Cloud. Supprimez en toute sécurité une ou plusieurs feuilles, nettoyez la structure du classeur et automatisez l’optimisation des classeurs. API RESTful dédiée à la gestion et aux flux de travail de traitement de documents Excel de qualité professionnelle.

## API de suppression d’une feuille de calcul à partir d’un classeur

### API Web

```http
PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName={sheetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}"
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête :

| Nom du paramètre | Type   | Emplacement | Description                                                                                                                                                                                             |
| :--------------- | :----- | :---------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet      | Fichier | FormData    | **Obligatoire.** Le fichier de classeur Excel source (.xlsx, .xls, etc.) à partir duquel une feuille de calcul sera supprimée.                                                                          |
| sheetName        | Chaîne  | Query       | **Obligatoire.** Le nom exact de la feuille de calcul à supprimer (par exemple `Feuil1`, `DonnéesTemporaires`).                                                                                       |
| outPath          | Chaîne  | Query       | **Facultatif.** Le chemin du dossier cible dans le stockage cloud où le classeur modifié sera enregistré. Si omis ou `null`, le classeur est enregistré à l’emplacement du fichier source ou dans un chemin par défaut. |
| outStorageName   | Chaîne  | Query       | **Facultatif.** L’identifiant du service de stockage cloud (par exemple `ProjectStorage`) dans lequel le fichier de sortie sera écrit. Si non fourni, le stockage par défaut est utilisé.                 |
| region           | Chaîne  | Query       | **Facultatif.** Le paramètre de paramètres régionaux (par exemple `fr-FR`) qui peut affecter les formules ou données spécifiques à la région lors de l’opération d’enregistrement.                     |
| password         | Chaîne  | Query       | **Facultatif.** Le mot de passe requis pour ouvrir et modifier un classeur protégé par mot de passe. À omettre si le fichier n’est pas chiffré.                                                         |

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

| Code | Signification         | Description                                                      |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                  |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.             |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                       |

## À quelles situations faut-il utiliser l’API de suppression d’une feuille de calcul à partir d’un classeur ?

- **Post-traitement automatisé des rapports** – Après la génération d’un rapport financier final, supprimez automatiquement les feuilles intermédiaires utilisées pour les calculs temporaires, afin de conserver un fichier final propre et professionnel.
- **Nettoyage dynamique des fichiers modèles** – Lorsque les utilisateurs génèrent des documents personnalisés (par exemple, des devis) à partir d’un modèle, supprimez les pages facultatives non sélectionnées.
- **Optimisation de l’archivage des flux de travail** – Une fois un projet ou un audit terminé, supprimez les feuilles de brouillon ou de collaboration, en conservant uniquement la version finale pour l’archivage et la conformité.

## Pourquoi utiliser l’API de suppression d’une feuille de calcul à partir d’un classeur ?

- **Conçu pour les développeurs** – Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, permettant un développement rapide et offrant une documentation complète.
- **Réduction des coûts de main-d’œuvre** – Élimine la nécessité de personnel dédié pour consolider manuellement les documents.
- **Pay-as-you-go** – Aucun investissement initial ; vous ne payez que pour les appels API que vous utilisez réellement.
- **Coûts de maintenance nuls** – Aucun serveur à maintenir, aucune mise à jour logicielle, aucune préoccupation de compatibilité.

## Comment utiliser l’API de suppression d’une feuille de calcul à partir d’un classeur à l’aide des SDK

### Spécification de l’API de suppression d’une feuille de calcul à partir d’un classeur

La <a href="https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet" rel="noopener noreferrer">spécification de l’API de suppression d’une feuille de calcul à partir d’un classeur</a> définit une interface de programmation accessible publiquement, vous permettant d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName=Feuil1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et vous permet de supprimer une feuille de calcul avec un minimum de code. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}