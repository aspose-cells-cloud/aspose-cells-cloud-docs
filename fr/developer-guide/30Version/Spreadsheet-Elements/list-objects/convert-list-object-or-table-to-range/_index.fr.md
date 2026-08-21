---
title: "Convertir un objet liste en plage – Aspose.Cells Cloud API"
ArticleTitle: "Convertir un objet liste en plage à l’aide de l’API Aspose.Cells Cloud"
second_title: "Document"
linktype: "Conversion"
type: docs
url: /list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "API Aspose Cells, convertir un objet liste en plage, API REST Excel"
description: "Découvrez comment convertir un ListObject (tableau) Excel en plage à l’aide de l’API REST Aspose.Cells Cloud. Inclut la syntaxe de la requête, les paramètres, un exemple cURL, le schéma de réponse, les détails d’authentification, les codes d’erreur et des exemples de SDK."
weight: 30
---

Cet API REST convertit un **ListObject (tableau)** en **plage** au sein d’une feuille de calcul Excel.

**Prérequis :**  
Avant d’appeler l’endpoint, assurez-vous que le classeur a été uploadé dans votre espace de stockage Aspose Cloud, que la feuille de calcul contient l’objet ListObject cible, et que vous utilisez un format de fichier pris en charge (par exemple, .xlsx, .xlsm).

## API REST

**Authentification**  
Pour appeler cette opération, vous devez inclure un jeton JWT valide dans l’en-tête `Authorization`. Obtenez le jeton en envoyant une requête POST à l’endpoint OAuth 2.0 avec votre client ID et votre client secret. Le jeton doit inclure la portée `Cells.ReadWrite` et reste valable pendant la durée indiquée par le service de jetons.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom                  | Type    | Emplacement | Obligatoire | Valeur par défaut | Description                                                 |
| --------------------- | ------- | ----------- | ----------- | ---------------- | ------------------------------------------------------------ |
| **name**             | string  | path        | Oui         | –                | Le nom du fichier Excel.                                    |
| **sheetName**        | string  | path        | Oui         | –                | Le nom de la feuille de calcul contenant l’objet ListObject. |
| **listObjectIndex**  | integer | path        | Oui         | –                | Index à base zéro de l’objet ListObject (tableau) à convertir. |
| **folder**           | string  | query       | Non         | –                | Chemin du dossier dans lequel le fichier est stocké.        |
| **storageName**      | string  | query       | Non         | –                | Nom du service de stockage.                                 |

> **Remarque :** Cette opération ne fonctionne qu’avec les formats modernes d’Excel tels que **.xlsx** et **.xlsm**. L’objet ListObject ne doit pas être protégé. Pour plus d’informations sur les ListObjects, consultez la [vue d’ensemble des ListObjects](/list-objects/). Pour plus de détails sur la manipulation des plages, reportez-vous à la [documentation sur les plages](/ranges/).

### Exemple cURL (requête)

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <votre-jeton-jwt>"
```

{{< /tab >}}

#### Schéma de réponse

L’API renvoie une réponse **200 OK** contenant les détails de la plage nouvellement créée.

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| Champ             | Type    | Description                                                |
| ----------------- | ------- | ---------------------------------------------------------- |
| **Code**          | integer | Code d’état similaire à HTTP (200 indique la réussite).    |
| **Status**        | string  | Message d’état textuel.                                    |
| **RangeName**     | string  | Nom attribué à la plage créée.                             |
| **Address**       | string  | Adresse complète de la plage, incluant le nom de la feuille. |
| **FirstRow**      | integer | Index à base zéro de la première ligne de la plage.        |
| **FirstColumn**   | integer | Index à base zéro de la première colonne de la plage.      |
| **RowCount**      | integer | Nombre de lignes dans la plage.                            |
| **ColumnCount**   | integer | Nombre de colonnes dans la plage.                          |

**Codes d’état HTTP**

| Code | Signification               | Description                                                  |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                              |
| 413  | Charge utile trop grande     | Le fichier uploadé dépasse la limite de taille.             |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                   |

**Schéma de réponse d’erreur (exemple) :**

```json
{
  "Code": 400,
  "Message": "listObjectIndex invalide. L'index doit être compris entre 0 et 5."
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}
---