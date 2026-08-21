---
title: "Convertir une feuille de calcul en PDF, PNG, CSV et plus – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Convertir une feuille de calcul"
type: docs
url: /worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells, conversion de feuille de calcul, API REST, cURL, SDK, PDF, PNG, CSV"
description: "Découvrez comment convertir une seule feuille de calcul à partir d’un classeur Excel en PDF, PNG, CSV et plus de 15 autres formats à l’aide de l’API REST Aspose.Cells Cloud. Inclut un exemple cURL, des extraits de code SDK et une référence complète des paramètres."
weight: 130
ArticleTitle: "Convertir une feuille de calcul en PDF, PNG, CSV et plus – Aspose.Cells Cloud API"
---

**API de conversion de feuille de calcul** – Le point de terminaison `GET /cells/{name}/worksheets/{sheetName}` permet de convertir une seule feuille de calcul (une feuille à l’intérieur d’un classeur Excel) vers un autre type de fichier.

> **Prérequis :** Vous devez posséder un jeton JWT valide et avoir le classeur stocké dans un emplacement pris en charge par le stockage Aspose Cloud avant d’invoquer ce point de terminaison.

Formats **importables** pris en charge (la feuille de calcul peut être lue à partir de) :

- XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT

Formats **exportables uniquement** pris en charge (la feuille de calcul peut être enregistrée en tant que) :

- PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS

## API REST

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) décrit l’interface publiquement accessible.

### **Paramètres de la requête**

| Paramètre                | Type    | Obligatoire | Valeur par défaut | Valeurs autorisées                                                  | Description                                           |
| ------------------------ | ------- | ----------- | ----------------- | ------------------------------------------------------------------- | ----------------------------------------------------- |
| **format**               | string  | Oui         | –                 | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, … (voir liste ci-dessus) | Format de sortie cible.                              |
| **verticalResolution**   | integer | Non         | 96                | 72‑600                                                              | Résolution verticale (DPI) pour la sortie image.     |
| **horizontalResolution** | integer | Non         | 96                | 72‑600                                                              | Résolution horizontale (DPI) pour la sortie image.   |
| **password**             | string  | Non         | –                 | –                                                                   | Mot de passe pour ouvrir un classeur protégé.        |
| **folder**               | string  | Non         | –                 | –                                                                   | Dossier cloud où le classeur source est stocké.      |
| **storage**              | string  | Non         | –                 | –                                                                   | Nom du stockage (par exemple, « Default »).          |

### Réponse

| Code d’état | Description                                                        | Type retourné              |
| ----------- | ------------------------------------------------------------------ | -------------------------- |
| **200**     | Conversion réussie ; flux binaire du fichier converti renvoyé.    | `application/octet-stream` |
| **400**     | Requête incorrecte – paramètres manquants ou non valides.         | Objet d’erreur JSON        |
| **401**     | Non autorisé – jeton JWT invalide ou manquant.                    | Objet d’erreur JSON        |
| **404**     | Introuvable – le classeur ou la feuille de calcul n’existe pas.   | Objet d’erreur JSON        |
| **500**     | Erreur interne du serveur – échec inattendu.                      | Objet d’erreur JSON        |

#### Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Exemple de réponse

```
Image convertie (flux binaire)
```

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus rapide de développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---