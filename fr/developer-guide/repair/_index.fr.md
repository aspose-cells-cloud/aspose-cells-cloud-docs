---
title: Réparer
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/repair/
keywords: Repair Excel, ODS, WPS, and so on files
description: Aspose.Cells Cloud REST API prend en charge la réparation des fichiers Excel. Le SDK prend en charge différents types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 39
---
Ce REST API indique les fichiers `repair` Excel.

- Réparez XLS, XLSX, XLSM, XLSB, ODS, etc.
- Prise en charge de plusieurs fichiers.

Aspose.Cells Cloud Excel Repair récupère les données des fichiers Excel corrompus en ligne sans installation. Les fichiers Excel corrompus peuvent poser problème car vous ne pourrez pas les ouvrir. Vous pouvez essayer l'application de réparation Aspose.Cells Cloud Excel pour récupérer les données des fichiers Excel corrompus.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/repair

```

 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| déposer| déposer| Données de formulaire| Fichier à télécharger|
| format| chaîne| requête| Format de sortie, la valeur par défaut est nulle, le format de sortie est égal au format du fichier d'entrée.|
 
 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
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
 


## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}


{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "" >}}
{{< /tab >}}

{{< /tabs >}}
