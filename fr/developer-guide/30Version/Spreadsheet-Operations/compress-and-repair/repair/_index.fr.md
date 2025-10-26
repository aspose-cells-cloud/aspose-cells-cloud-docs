---
title: Réparer le fichier Excel
second_title: Documen
type: docs
linktitle: Réparer le fichier Excel
url: /fr/repair-excel-files/
keywords: Repair Excel, ODS, WPS, and so on files
description: Réparez les fichiers Excel en utilisant Aspose.Cells Cloud REST API. Le API prend en charge plusieurs langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift pour une intégration rapide dans vos projets.
weight: 39
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Réparation
---
Ce REST API indique les fichiers `repair` Excel.

- Réparer XLS, XLSX, XLSM, XLSB, ODS, etc.
- Prise en charge de plusieurs fichiers.

L'application Aspose.Cells Cloud Repair Excel récupère les données des fichiers corrompus Excel en ligne, sans installation. Les fichiers corrompus Excel peuvent poser problème, car vous ne pourrez pas les ouvrir. Vous pouvez essayer l'application Aspose.Cells Cloud Repair Excel pour récupérer les données des fichiers corrompus Excel.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/repair

```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| déposer| déposer| données de formulaire| Fichier à télécharger|
| format| chaîne| requête| Format de sortie, la valeur par défaut est nulle, le format de sortie est égal au format du fichier d'entrée.|

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/repair" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash

{
    "Files":
    [
        {
            "Filename":"xxxx1.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        {
            "Filename":"xxxx2.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}

```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}
