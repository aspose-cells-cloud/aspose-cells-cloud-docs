---
title: "Aspose.Cells Cloud Web API – Convertir une feuille de calcul Excel locale en fichier PDF – Outil gratuit en ligne"
second_title: "Document"
ArticleTitle: "Comment convertir une feuille de calcul de classeur local en fichier PDF : guide pas à pas"
linktitle: "Convertir une feuille de calcul en PDF"
type: docs
url: /convert-worksheet-to-pdf/
keywords: "Aspose.Cells, Excel vers PDF, conversion de feuille de calcul, API REST, conversion cloud, PDF de feuille de calcul, point de terminaison API, génération de PDF"
description: "Utilisez l’API Aspose.Cells Cloud pour convertir rapidement et en toute sécurité une feuille de calcul d’un fichier Excel local en document PDF."
weight: 100
---

Exportez une feuille de calcul d’un fichier Excel local vers un fichier [PDF](https://docs.fileformat.com/pdf/) à l’aide de l’API Cloud.

## **API de conversion de feuille de calcul en PDF**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Path/Query String/HTTPBody | Description                                                           |
| ---------------- | ------ | -------------------------- | --------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                   | Télécharger le fichier de feuille de calcul.                          |
| worksheet        | Chaîne  | Query                      | Nom de la feuille de calcul dans le classeur.                        |
| outPath          | Chaîne  | Query                      | (Facultatif) Le chemin du dossier où stocker le classeur ; par défaut : null. |
| outStorageName   | Chaîne  | Query                      | Nom du stockage de sortie pour le fichier.                           |
| fontsLocation    | Chaîne  | Query                      | Utiliser des polices personnalisées pour le PDF.                      |
| region           | Chaîne  | Query                      | Définir le paramètre de région de la feuille de calcul.              |
| password         | Chaîne  | Query                      | Mot de passe requis pour ouvrir le fichier de feuille de calcul.     |

### **Réponse**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**Codes d’état HTTP**

| Code | Signification         | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte    | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                   |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.                 |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                     |

## **Dans quelles situations devez-vous utiliser l’API de conversion de feuille de calcul en PDF ?**

- **État financiers** : Convertir les bilans, les comptes de résultat (tables spécifiques) en PDF pour des documents prêts à l’audit.
- **Rapports de ventes** : Transformer les tableaux de bord de ventes ou les calculs de commissions en PDF distribuables.
- **Indicateurs opérationnels** : Exporter les tableaux de KPI et les métriques de performance sous forme de rapports PDF formels.
- **Données contractuelles** : Exporter les tableaux tarifaires et les accords de niveau de service des feuilles de calcul vers des pièces jointes PDF.
- **Traces d’audit** : Conserver les feuilles de calcul financières sous forme de preuves PDF non modifiables.
- **Résumés de portefeuille** : Exporter les tableaux de performance des investissements en tant que relevés PDF prêts à être transmis aux clients.
- **Rapports de contrôle qualité** : Exporter les feuilles de contrôle d’inspection en PDF pour les archives de conformité.
- **Résumés de stock** : Transformer les feuilles de stock en PDF pour examen par la direction.

## Pourquoi utiliser l’API de conversion de feuille de calcul en PDF ?

- **Adaptée aux développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, facilitant un développement rapide et accompagné d’une documentation complète. Par rapport à la création de solutions personnalisées de rendu graphique, cela réduit considérablement la charge de développement.
- **Économique** : Vous pouvez convertir les données des tableaux sans avoir à télécharger préalablement le classeur, ce qui économise de l’espace de stockage et réduit les coûts.
- **Préservation du formatage** : Conserve le formatage complexe d’Excel dans un format PDF universellement accessible.

## Comment utiliser l’API de conversion de feuille de calcul en PDF avec les SDK ?

### Spécification de l’API de conversion de feuille de calcul en PDF

La [Spécification de l’API de conversion de feuille de calcul en PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF) fournit une interface de programmation publiquement accessible et permet des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@monClasseur.xlsx" \
  -o converted.json
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de convertir les données de tableaux de feuilles de calcul en fichier PDF avec un code minimal. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}