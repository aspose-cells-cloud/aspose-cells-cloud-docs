---
title: "Convertir une plage Excel en PDF avec l’API Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Comment convertir des données locales de plage de feuille de calcul en fichier PDF : guide étape par étape"
linktype: "Convert Range to PDF"
type: docs
url: /convert-range-to-pdf/
keywords: "Aspose.Cells Cloud, convertir une plage Excel en PDF, Excel en PDF, conversion cloud"
description: "Convertir une plage spécifique d’un fichier Excel local en PDF à l’aide de l’API REST d’Aspose.Cells Cloud."
weight: 100
---

Exporter une plage de données à partir d’un fichier Excel local vers un fichier [PDF](https://docs.fileformat.com/pdf/) à l’aide de l’API Cloud.

**Prérequis** : Avant d’utiliser cette API, vous devez disposer d’un compte Aspose.Cells Cloud valide, d’un jeton d’accès JWT et éventuellement d’un SDK Aspose.Cells Cloud pour votre langage de programmation. Assurez-vous que le stockage cible (par défaut ou personnalisé) est configuré si vous prévoyez d’utiliser le paramètre `outStorageName`.

## **API Convert Range to PDF**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                   |
| ---------------- | ------ | ----------------------------------------------------- | ----------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                              | Télécharger le fichier de feuille de calcul.                                  |
| worksheet        | Chaîne  | Chaîne de requête                                      | Le nom de la feuille de calcul à l’intérieur du classeur.                     |
| range            | Chaîne  | Chaîne de requête                                      | La zone de cellules à convertir, par exemple A1:C10.                          |
| outPath          | Chaîne  | Chaîne de requête                                      | (Facultatif) Le chemin du dossier où le classeur est stocké. Par défaut : null. |
| outStorageName   | Chaîne  | Chaîne de requête                                      | Nom du stockage de sortie.                                                    |
| fontsLocation    | Chaîne  | Chaîne de requête                                      | Emplacement pour stocker les polices personnalisées à usage personnel.         |
| region           | Chaîne  | Chaîne de requête                                      | Paramètre de région de la feuille de calcul.                                  |
| password         | Chaîne  | Chaîne de requête                                      | Mot de passe pour ouvrir le fichier de feuille de calcul.                     |

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

_Une réponse typique est un flux PDF binaire renvoyé sous forme de téléchargement de fichier._

**Codes de statut HTTP**

| Code | Signification           | Description                                                    |
| ---- | ----------------------- | -------------------------------------------------------------- |
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.                 |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                  |

## **Dans quelles situations devez-vous utiliser l’API Convert Range to PDF ?**

- **État financiers** : Convertir les bilans, comptes de résultat (plages spécifiques) en PDF pour des documents prêts à être fournis lors d’un audit.
- **Rapports de ventes** : Transformer les tableaux de bord de ventes ou les calculs de commissions en PDF pouvant être diffusés.
- **Métriques opérationnelles** : Exporter les tableaux de KPI et les indicateurs de performance sous forme de rapports PDF formels.
- **Données contractuelles** : Exporter les tableaux de prix et les accords de niveau de service des feuilles de calcul vers des pièces jointes PDF.
- **Traces d’audit** : Préserver les plages de données financières sous forme de preuves PDF non modifiables.
- **Résumés de portefeuille** : Exporter les plages de performances des investissements vers des états de compte PDF prêts à être transmis aux clients.
- **Rapports de contrôle qualité** : Exporter les plages de données d’inspection vers des PDF pour les dossiers de conformité.
- **Résumés de stock** : Transformer les tableaux de niveaux de stock en PDF pour examen par la direction.

## Pourquoi utiliser l’API Convert Range to PDF ?

- **Adapté aux développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, permettant un développement rapide et une documentation complète. Comparé à la création de solutions personnalisées de rendu de graphiques, cela réduit considérablement la charge de développement.
- **Économique** : Vous pouvez convertir des données de plage sans avoir à télécharger préalablement l’ensemble du classeur, ce qui permet d’économiser de l’espace de stockage et de réduire les coûts.
- **Préservation des mises en forme Excel complexes** dans un format PDF universellement accessible.

## Comment utiliser l’API Convert Range to PDF avec les SDK ?

### Spécification de l’API Convert Range to PDF

La [spécification de l’API Convert Range to PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF) définit une interface de programmation accessible publiquement et vous permet d’effectuer directement des interactions REST à partir d’un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et vous permet de convertir une plage de données en fichier PDF à l’aide d’un code concis. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}