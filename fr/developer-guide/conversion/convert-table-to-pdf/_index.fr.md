---
title: "Aspose.Cells Cloud Web API – Convertir les données locales d’un tableau Excel en fichier PDF – Outil gratuit en ligne"
second_title: "Document"
ArticleTitle: "Comment convertir les données de tableur locales en fichier PDF : Guide pas à pas"
linktitle: "Convertir un tableau en PDF"
type: docs
url: /convert-table-to-pdf/
keywords: "Aspose.Cells, Excel vers PDF, conversion de tableau, API cloud"
description: "Convertissez rapidement un tableau Excel local en fichier PDF à l’aide de l’API REST Aspose.Cells Cloud."
weight: 100
---

Exportez les données d’un tableau à partir d’un fichier Excel local vers un fichier PDF à l’aide de l’API cloud.

## **Convertir un tableau en PDF – API**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                 |
| :--------------- | :----- | :---------------------------------------------------- | :-------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                              | Téléchargez le fichier de feuille de calcul à convertir.                   |
| worksheet        | Chaîne  | Chaîne de requête                                     | Nom de la feuille de calcul dans le classeur.                              |
| tableName        | Chaîne  | Chaîne de requête                                     | Nom du tableau à convertir.                                                 |
| outPath          | Chaîne  | Chaîne de requête                                     | (Facultatif) Chemin du dossier où le PDF converti sera enregistré. Par défaut : null. |
| outStorageName   | Chaîne  | Chaîne de requête                                     | Nom du stockage de sortie à utiliser.                                      |
| fontsLocation    | Chaîne  | Chaîne de requête                                     | Chemin vers des polices personnalisées à utiliser dans le PDF.             |
| region           | Chaîne  | Chaîne de requête                                     | Région à utiliser pour le classeur.                                        |
| password         | Chaîne  | Chaîne de requête                                     | Mot de passe nécessaire pour accéder au fichier de feuille de calcul.      |

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

**Exemple d’en-têtes de réponse**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**Codes de statut HTTP**

| Code | Signification          | Description                                                        |
| ---- | ---------------------- | ------------------------------------------------------------------ |
| 200  | OK                     | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte     | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé           | Jeton JWT invalide ou manquant.                                    |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la taille maximale autorisée.       |
| 500  | Erreur interne du serveur | Erreur inattendue sur le serveur.                                 |

## **À quoi sert l’API Convertir un tableau en PDF ?**

- **États financiers** : Convertissez les bilans, les comptes de résultat (tables spécifiques) en PDF pour des documents prêts à être soumis à un audit.
- **Rapports de ventes** : Transformez les tableaux de bord de ventes ou les calculs de commissions en PDF partageables.
- **Indicateurs opérationnels** : Exportez les tables de KPI et d’indicateurs de performance sous forme de rapports PDF formels.
- **Données contractuelles** : Exportez les tables tarifaires et les accords de niveau de service depuis des feuilles de calcul vers des pièces jointes PDF.
- **Traces d’audit** : Conservez les tables de données financières sous forme de preuves PDF non modifiables.
- **Résumés de portefeuille** : Exportez les tables de performance des investissements vers des états PDF prêts à être envoyés aux clients.
- **Rapports de contrôle qualité** : Exportez les tables de données d’inspection vers des PDF destinés à être archivés pour la conformité.
- **Résumés de stock** : Transformez les tables de niveaux de stock en PDF pour revue par la direction.

## **Pourquoi utiliser l’API Convertir un tableau en PDF ?**

- **Développeur-friendly** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, ce qui permet un développement rapide, accompagné d’une documentation complète. Comparé à la création de solutions personnalisées de rendu de graphiques, cela réduit considérablement la charge de travail de développement.
- **Économique** : Vous pouvez convertir les données d’un tableau sans avoir à télécharger d’abord le classeur, ce qui économise de l’espace de stockage et réduit les coûts.
- **Préservation des mises en forme complexes Excel** dans un format PDF universellement accessible.

## **Comment utiliser l’API Convertir un tableau en PDF avec les SDK ?**

### Spécification de l’API Convertir un tableau en PDF

La [spécification de l’API Convertir un tableau en PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF) fournit une interface de programmation publique accessible permettant d’exécuter directement des interactions REST depuis un navigateur web.
Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de convertir les données de tableurs en fichier PDF avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}