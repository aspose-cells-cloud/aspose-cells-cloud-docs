---
title: "Grouper des colonnes – Documentation de l’API Aspise.Cells Cloud"
description: "Grouper les colonnes d'une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud (v3.0). Inclut la syntaxe de la requête, les paramètres, des exemples cURL et SDK, ainsi que les détails de la réponse."
keywords: "Aspose.Cells, grouper des colonnes, API Excel, REST, SDK cloud"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# Grouper des colonnes sur une feuille de calcul Excel

**Version de l’API :** v3.0  
**Opération :** `PostGroupWorksheetColumns` – Grouper des colonnes d’une feuille de calcul.

---

## Vue d’ensemble

Cette API REST vous permet de grouper une plage de colonnes dans une feuille de calcul. Les colonnes groupées peuvent être affichées ou masquées, ce qui vous permet de créer des sections repliables semblables à celles de Microsoft Excel.

---

## Conditions préalables

- Un **jeton d’accès JWT** valide obtenu à partir du service d’authentification Aspose Cloud.  
- Le classeur doit être stocké dans un emplacement accessible à Aspose.Cells Cloud (stockage par défaut ou nom d’un stockage personnalisé).  
- Version requise du SDK (si un SDK est utilisé) : la dernière version prenant en charge l’API **v3.0**.  

---

## Authentification

Toutes les requêtes nécessitent une authentification par **jeton Bearer**.

```http
Authorization: Bearer <access_token>
```

Pour plus d’informations sur l’obtention d’un jeton, consultez le [guide d’authentification JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Requête HTTP

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| Paramètre | Emplacement | Obligatoire | Description |
|-----------|-------------|-------------|-------------|
| `name` | chemin d’accès | Oui | Nom du fichier classeur (par exemple, `test.xlsx`). |
| `sheetName` | chemin d’accès | Oui | Feuille de calcul contenant les colonnes à grouper. |
| `firstIndex` | requête | Oui | Index de base zéro de la première colonne à inclure dans le groupe. |
| `lastIndex` | requête | Oui | Index de base zéro de la dernière colonne à inclure dans le groupe. |
| `hide` | requête | Non | Si `true`, les colonnes groupées sont masquées ; sinon, elles restent visibles. |
| `folder` | requête | Non | Chemin d’accès au dossier contenant le classeur. |
| `storageName` | requête | Non | Nom du service de stockage où le fichier est situé. |

---

## Exemple de requête (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **Remarque :** La requête utilise **HTTPS** pour garantir une communication chiffrée.

---

## Réponse

### Succès (200)

| Champ | Type | Description |
|-------|------|-------------|
| `Code` | entier | Code d’état HTTP (`200`). |
| `Status` | chaîne | État textuel de l’opération (`OK`). |

**Exemple**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Erreur (par exemple, 400 Mauvaise requête)

| Champ | Type | Description |
|-------|------|-------------|
| `Code` | entier | Code d’état HTTP (`400`, `401`, `404`, `500`, etc.). |
| `Status` | chaîne | État textuel (`Error`). |
| `ErrorMessage` | chaîne | Description lisible par l’humain du problème. |
| `ErrorCode` | chaîne | Identifiant programmatique de l’erreur. |

**Exemple – Mauvaise requête**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "Index de colonne non valide.",
  "ErrorCode": "InvalidParameter"
}
```

---

## Exemples de SDK

Les extraits suivants montrent comment appeler l’opération **Grouper des colonnes de feuille de calcul** à l’aide des SDK pris en charge.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## Remarques

- **Comportement du groupement :** L’API crée un groupe de colonnes qui peut être développé ou réduit dans Excel. Définir `hide=true` réduit immédiatement le groupe.  
- **Indexation à base zéro :** `firstIndex` et `lastIndex` commencent à **0** ; la première colonne d’une feuille de calcul a l’index 0.  
- **Considérations sur le stockage :** Si le classeur réside dans un stockage non par défaut, fournissez les deux paramètres de requête `folder` et `storageName`.  

---

## Voir aussi

- [Authentification – Jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Spécification OpenAPI pour Grouper des colonnes de feuille de calcul](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [SDK Aspose.Cells Cloud (GitHub)](https://github.com/aspose-cells-cloud)  
- [Grouper des lignes sur une feuille de calcul Excel](/rows/group/)  

---

> *Illustration :* ![Capture d’écran montrant des colonnes groupées dans une feuille de calcul Excel](./images/group-columns.png){: .img-fluid alt="Capture d’écran montrant des colonnes groupées dans une feuille de calcul Excel" }

*L’image factice ci-dessus doit être remplacée par une capture d’écran réelle illustrant le résultat visuel du groupement des colonnes.*