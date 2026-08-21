---
title: "Calculer la formule d'une cellule – API Aspose.Cells Cloud"
type: docs
url: /fr/calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, calculer la formule d'une cellule, API Excel, API REST, SDK"
description: "Calculez la formule d'une cellule Excel via l'API REST Aspose.Cells Cloud (v3.0). Inclut le point de terminaison, les paramètres, un exemple cURL et des extraits de code SDK."
ArticleTitle: "Calculer la formule d'une cellule – Documentation de l'API Aspose.Cells Cloud"
---

## API REST

Cette API REST calcule la **formule de cellule** dans un classeur Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## Sécurité et authentification

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement du paramètre (chemin/interrogation/ corps) | Description                                                          |
| ---------------- | ------ | ------------------------------------------------------- | -------------------------------------------------------------------- |
| name             | string | chemin                                                  | Nom du fichier Excel (par exemple, `Book1.xlsx`).                   |
| sheetName        | string | chemin                                                  | Nom de la feuille de calcul contenant la cellule.                   |
| cellName         | string | chemin                                                  | Adresse de la cellule à calculer (par exemple, `A1`).                |
| options          | object | corps                                                   | Objet JSON contenant les options de calcul (voir tableau **Objet options**). |
| folder           | string | interroger                                               | Dossier dans le stockage où le fichier est situé.                    |
| storageName      | string | interroger                                               | Nom du stockage Aspose Cloud.                                        |

#### Objet options

| Champ           | Type    | Description                                                                              | Valeur par défaut |
| --------------- | ------- | ---------------------------------------------------------------------------------------- | ----------------- |
| CalcStackSize   | string  | Taille maximale de la pile de calcul.                                                    | `"1"`             |
| IgnoreError     | boolean | Si `true`, les erreurs de calcul sont ignorées et la valeur de la cellule est définie à `#N/A`. | `false`           |
| Recursive       | boolean | Active le calcul récursif des cellules dépendantes.                                      | `false`           |
| Precision       | string  | Nombre de décimales pour les résultats numériques.                                       | `"15"`            |
| UseThreading    | boolean | Active le calcul multi‑thread.                                                            | `false`           |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                                               |

## Comment utiliser l’API PostCellCalculate avec les SDK

### Spécification de l’API PostCellCalculate

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud avec cURL. **Obtenez d’abord un jeton JWT** en vous authentifiant auprès du point de terminaison `/connect/token`, puis remplacez `<jwt token>` par la valeur du jeton.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L'utilisation d'un SDK est le moyen le plus efficace d'accélérer le développement. Un SDK masque les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}