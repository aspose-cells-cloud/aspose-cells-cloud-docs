---
title: "Supprimer les lignes en double d’un ListObject – Documentation de l’API Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Supprimer les doublons"
type: docs
keywords: "supprimer les doublons, listobject, API Aspose.Cells Cloud, Excel, REST"
url: /fr/list-objects/remove-duplicates/
description: "Découvrez comment supprimer les lignes en double d’un ListObject dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’URL du point de terminaison, les paramètres, l’authentification, ainsi que des exemples de requêtes et de réponses."
weight: 20
---

Cet API REST supprime les lignes en double d’un **ListObject** dans une feuille de calcul Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **Paramètres de la requête**

| Nom du paramètre    | Type    | Emplacement | Description                                                    |
| ------------------- | ------- | ----------- | -------------------------------------------------------------- |
| **name**            | String  | Path        | Le nom du fichier Excel.                                       |
| **sheetName**       | String  | Path        | Le nom de la feuille de calcul contenant l’objet liste.       |
| **listObjectIndex** | Integer | Path        | L’index de base zéro de l’objet liste à traiter.               |
| **folder**          | String  | Query       | (Facultatif) Le chemin du dossier où le fichier est stocké.   |
| **storageName**     | String  | Query       | (Facultatif) Le nom du service de stockage.                    |

### Exemple de requête (cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "DuplicateRowsRemoved": 12,
  "Message": "Les lignes en double ont été supprimées avec succès."
}
```

{{< /tab >}}
{{< /tabs >}}

### Réponse

En cas de succès, le service renvoie un objet JSON similaire à l’exemple ci-dessus. Les champs sont les suivants :

- **Code** – Code d’état HTTP (`200` en cas de succès).
- **Status** – Description textuelle de l’état.
- **DuplicateRowsRemoved** – Nombre de lignes supprimées.
- **Message** – Informations supplémentaires sur l’opération.

**Codes d’état HTTP**

| Code | Signification               | Description                                                    |
|------|-----------------------------|----------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la taille limite.              |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                     |

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le dépôt GitHub pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}