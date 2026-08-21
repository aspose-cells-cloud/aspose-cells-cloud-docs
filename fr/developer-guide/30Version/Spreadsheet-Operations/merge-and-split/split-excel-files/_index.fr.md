---
title: "Découper un classeur Excel en plusieurs fichiers"
ArticleTitle: "Comment découper un classeur Excel en plusieurs fichiers à l'aide de l'API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /split-multi-excel-files/
aliases: [/split/multi-files/]
keywords: "Excel, Aspose.Cells Cloud, API REST, découper un classeur, plusieurs fichiers, JPEG, PNG, PDF, CSV, JSON"
description: "L'API REST Aspose.Cells Cloud permet de découper un classeur Excel en plusieurs fichiers dans divers formats. Cette documentation fournit les paramètres de requête, un exemple cURL et des exemples de code SDK pour les langages C#, Java, PHP, Ruby, Node.js, Python, Perl et Go."
weight: 130
---

Cette API REST permet de découper un **classeur** Excel en plusieurs fichiers dans différents formats.

> **Prérequis** – Pour utiliser cette API, vous devez obtenir un jeton JWT valide, vous assurer que vous utilisez une version prise en charge du SDK et vérifier que votre classeur est stocké dans un emplacement de stockage pris en charge. L’API applique également des limites de taille de fichier documentées dans les directives de la plateforme.

## API PostWorkbookSplit

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une authentification basée sur <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre     | Type    | Emplacement | Description                                                                                     | Obligatoire |
| --------------------- | ------- | ----------- | ----------------------------------------------------------------------------------------------- | ----------- |
| files[]               | fichier | formData    | Un ou plusieurs classeurs Excel à **découper**. Utilisez `file1`, `file2`, etc. dans la requête. | Oui         |
| format                | chaîne  | Query       | Format de sortie souhaité pour les fichiers découpés.                                         | Non         |
| from                  | entier  | Query       | Index de la première feuille de calcul.                                                       | Non         |
| to                    | entier  | Query       | Index de la dernière feuille de calcul.                                                       | Non         |
| horizontalResolution  | entier  | Query       | Résolution horizontale de l’image.                                                            | Non         |
| verticalResolution    | entier  | Query       | Résolution verticale de l’image.                                                              | Non         |
| outFolder             | chaîne  | Query       | Dossier de sortie pour les fichiers découpés.                                                 | Non         |
| splitNameRule         | chaîne  | Query       | Règle de nommage appliquée aux fichiers découpés.                                             | Non         |
| folder                | chaîne  | Query       | Dossier contenant le classeur d’origine.                                                      | Non         |
| storageName           | chaîne  | Query       | Nom du stockage à utiliser.                                                                   | Non         |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[nom du fichier1]",
        "Filesize" : [taille du fichier],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[nom du fichier2]",
        "Filesize" : [taille du fichier],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[nom du fichier3]",
        "Filesize" : [taille du fichier],
        "FileContent" : "[Base64String]"
      }
    ]
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                                  |

## Comment utiliser l’API PostWorkbookSplit à l’aide des SDK

### Spécification de l’API PostWorkbookSplit

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
---