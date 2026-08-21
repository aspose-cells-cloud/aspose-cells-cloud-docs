---
title: "Supprimer une ligne dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Ligne"
type: docs
url: /fr/rows/delete/row/
aliases: [  /fr/delete-row-from-a-worksheet/ ]
description: "Utilisez le point de terminaison DELETE /worksheets/{sheetName}/cells/rows/{rowIndex} pour supprimer une ligne spécifique d'une feuille de calcul Excel via l'API REST Aspose.Cells Cloud. Inclut une commande cURL, des exemples de SDK et une référence complète des paramètres."
keywords: "Aspose.Cells, supprimer une ligne, Excel, API, REST, Cloud, SDK"
weight: 80
ArticleTitle: "Supprimer une ligne dans une feuille de calcul Excel – Guide de l’API Aspose.Cells Cloud"
---

Cet API REST supprime une ligne d'une feuille de calcul Excel.

**Prérequis**  
- Un jeton JWT valide en tant que **Authorization**.  
- Le classeur doit être stocké dans un espace de stockage pris en charge par Aspose Cloud (par défaut ou personnalisé).  
- Le dossier cible (le cas échéant) doit exister dans l’espace de stockage sélectionné.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Paramètres de la requête**

| Nom du paramètre    | Type    | Path / Query | Obligatoire | Description                                                                                         |
| ------------------- | ------- | ------------ | ----------- | --------------------------------------------------------------------------------------------------- |
| **name**            | string  | path         | Oui         | Le nom du classeur.                                                                                 |
| **sheetName**       | string  | path         | Oui         | Le nom de la feuille de calcul.                                                                     |
| **rowIndex**        | integer | path         | Oui         | Index de base zéro de la ligne à supprimer.                                                         |
| **startrow**        | integer | query        | Non         | Index de la première ligne à supprimer (généralement identique à `rowIndex`).                       |
| **totalRows**       | integer | query        | Non         | Nombre de lignes consécutives à supprimer.                                                          |
| **updateReference** | boolean | query        | Non         | Lorsque `true` (par défaut), les formules, les plages nommées et autres références sont mises à jour après la suppression. |
| **folder**          | string  | query        | Non         | Dossier contenant le classeur.                                                                      |
| **storageName**     | string  | query        | Non         | Nom du service de stockage.                                                                         |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre un appel complet et exécutable.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Codes de réponse HTTP possibles**

| Code | Signification                          | Description                                                                          |
|------|----------------------------------------|--------------------------------------------------------------------------------------|
| 200  | OK                                     | La ligne a été supprimée avec succès.                                                |
| 400  | Requête incorrecte                     | Paramètres manquants ou invalides (par ex., `rowIndex` non numérique).              |
| 401  | Non autorisé                           | Jeton JWT invalide ou manquant.                                                      |
| 404  | Non trouvé                             | Le classeur, la feuille de calcul ou la ligne spécifiée n’existe pas.               |
| 500  | Erreur interne du serveur              | Erreur serveur inattendue ; voir la réponse d’erreur pour plus de détails.         |

**Exemple de réponse d’erreur**

```json
{
  "Code": 400,
  "Message": "Index de ligne fourni non valide."
}
```

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen optimal d’accélérer le développement. Un SDK masque les détails de bas niveau afin que vous puissiez vous concentrer sur vos tâches de projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Opérations connexes**  
- [Ajouter une ligne](/cells/rows/add/row/)  
- [Supprimer plusieurs lignes](/cells/rows/delete/rows/)  
- [Obtenir les détails d’une ligne](/cells/rows/get/row/)  
---