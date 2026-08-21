---
title: "Insérer un filtre dynamique dans un ListObject Excel – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Insérer un filtre dynamique"
type: docs
keywords: "Aspose.Cells, filtre dynamique Excel, ListObject, API REST, SDK cloud"
description: "Découvrez comment ajouter un filtre dynamique à un ListObject Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’URL du point de terminaison, les paramètres, l’authentification, une requête cURL d’exemple et la réponse JSON."
weight: 20
ArticleTitle: "Insérer un filtre dynamique dans un ListObject Excel – Aspose.Cells Cloud API"
---

Cette API REST insère un filtre dynamique pour un objet liste présent sur une feuille de calcul Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                                 |
|------------------|---------|-------------|-----------------------------------------------------------------------------|
| name             | String  | Path        | Le nom du fichier Excel.                                                    |
| sheetName        | String  | Path        | Le nom de la feuille de calcul contenant l’objet liste.                     |
| listObjectIndex  | Integer | Path        | L’indice de base zéro de l’objet liste auquel le filtre dynamique sera ajouté. |
| columnIndex      | Integer | Query       | L’indice de base zéro de la colonne sur laquelle repose le filtre dynamique. |
| destCellName     | String  | Query       | La référence de la cellule (par ex., **A1**) où le filtre dynamique sera placé. |
| folder           | String  | Query       | Le dossier de stockage contenant le fichier Excel.                          |
| storageName      | String  | Query       | Le nom du service de stockage Aspose Cloud.                                 |

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler l’API :

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

> **Remarque :** La requête nécessite un jeton porteur JWT valide obtenu auprès du service d’authentification Aspose Cloud. Ce point de terminaison ne nécessite pas de corps de requête ; envoyez un objet JSON vide `{}` si votre bibliothèque client exige la présence d’un payload.

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **En‑tête de réponse :** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**Codes de statut HTTP**

| Code | Signification               | Description                                                           |
|------|-----------------------------|-----------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                        |
| 413  | Payload trop volumineux     | Le fichier téléchargé dépasse la limite de taille.                   |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                            |

### Gestion des erreurs

En cas d’erreur, l’API renvoie un objet JSON contenant un champ `ErrorMessage` décrivant le problème. Examinez le code de statut HTTP ainsi que le champ `ErrorMessage` pour déterminer les actions correctives à entreprendre.

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le dépôt GitHub pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}