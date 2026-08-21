---
title: "Aspose.Cells Cloud – Convertir un tableau en HTML"
description: "Convertissez rapidement des tableaux Excel en HTML avec l’API Aspose.Cells Cloud – sécurisée, préservant le formatage et facile à intégrer."
keywords: "Aspose.Cells, Excel vers HTML, convertir un tableau en HTML, API cloud, conversion de feuille de calcul"
weight: 100
date: 2026-07-30
last_updated: 2026-07-30
version: "v4.0"
url: /fr/convert-table-to-html/
type: docs
---

**Résumé rapide** – Ce point de terminaison lit un classeur Excel local, extrait le **tableau** spécifié, le convertit en fichier **HTML**, puis renvoie le résultat sous forme de flux téléchargeable. Aucun téléversement intermédiaire vers le stockage Aspose Cloud n’est requis.

## API ConvertTableToHTML

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom                  | Emplacement  | Type       | Obligatoire | Description                                                                                 |
| --------------------- | ------------ | ---------- | ----------- | ------------------------------------------------------------------------------------------- |
| **Spreadsheet**       | Form‑Data    | `File`     | **Oui**     | Le classeur Excel contenant le tableau à convertir.                                         |
| **worksheet**         | Query        | `String`   | **Oui**     | Nom de la feuille de calcul contenant le tableau.                                           |
| **tableName**         | Query        | `String`   | **Oui**     | Nom exact du tableau à convertir.                                                           |
| **outPath**           | Query        | `String`   | Non         | Chemin du dossier dans le stockage Aspose Cloud où le fichier HTML sera enregistré (facultatif). |
| **outStorageName**    | Query        | `String`   | Non         | Nom du stockage pour le fichier de sortie (facultatif).                                    |
| **fontsLocation**     | Query        | `String`   | Non         | Chemin vers un dossier contenant les polices personnalisées nécessaires à la conversion.   |
| **region**            | Query        | `String`   | Non         | Identifiant de paramètres régionaux (par exemple, `en-US`, `fr-FR`). Affecte le format des nombres et des dates. |
| **password**          | Query        | `String`   | Non         | Mot de passe pour ouvrir un classeur protégé.                                              |
| **AutoRowsFit**       | Query        | `Boolean`  | Non         | Ajuster automatiquement toutes les lignes de la feuille de calcul (`true`/`false`).        |
| **AutoColumnsFit**    | Query        | `Boolean`  | Non         | Ajuster automatiquement toutes les colonnes de la feuille de calcul (`true`/`false`).      |

### **Réponse**

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

**Codes d’état HTTP**

| Code | Signification            | Description                                                         |
| ---- | ------------------------ | ------------------------------------------------------------------- |
| 200  | OK                       | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte       | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé             | Jeton JWT invalide ou manquant.                                     |
| 413  | Charge utile trop grande | Le fichier téléversé dépasse la taille limite.                     |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                       |

## Quand utiliser l’API Convert Table to HTML ?

- **Contenu web dynamique** – Intégrez des tableaux tarifaires, des planning ou des listes de produits directement dans des pages web ou des CMS.
- **Modèles d’e-mail** – Générez des extraits HTML pour des récapitulatifs de commandes ou des rapports qui s’affichent de manière cohérente dans tous les clients de messagerie.
- **Tableaux de bord et outils de reporting** – Affichez des données de feuille de calcul en temps réel sans charger le classeur complet ni utiliser des composants de grille lourds.
- **Aperçus de documents** – Fournissez des aperçus rapides et fidèles aux formats de sections spécifiques d’une feuille de calcul.

## Comment utiliser l’API Convert Table to HTML avec les SDK ?

### Spécification de l’API Convert Table to HTML

La [Spécification de l’API Convert Table to HTML](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToHTML) fournit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/html?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@monClasseur.xlsx" \
  -o converted.html
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

L’utilisation des SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de convertir les données d’un tableau de feuille de calcul en fichier CSV avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :