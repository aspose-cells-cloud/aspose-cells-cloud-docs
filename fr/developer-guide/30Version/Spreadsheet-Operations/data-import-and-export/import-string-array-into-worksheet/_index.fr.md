---
title: "Importer un tableau de chaînes dans une feuille de calcul Excel – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Importer un tableau de chaînes"
type: docs
url: /import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, importer un tableau de chaînes, API REST Excel, téléchargement multipartite, import de données dans une feuille de calcul, SDK cloud"
description: "Découvrez comment importer un tableau de chaînes dans une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud (v3.0). Inclut le format de la requête, les paramètres et des exemples de SDK."
weight: 40
ArticleTitle: "Importer un tableau de chaînes dans une feuille de calcul Excel – Aspose.Cells Cloud"
---

Importer un tableau de chaînes dans une feuille de calcul Excel est une tâche courante lors de la remplissage de feuilles de calcul avec des données basées sur des listes. Cette opération est utile dans des scénarios tels que le chargement de valeurs de configuration, le transfert de données depuis des sources externes ou l'initialisation de feuilles de calcul avec des collections prédéfinies de chaînes.

**Prérequis :**  
- Un jeton JWT valide obtenu via le mécanisme d’authentification d’Aspose.Cells Cloud.  
- Un classeur existant (ou la possibilité d’en créer un) dans votre espace de stockage Aspose Cloud.  
- La version appropriée du SDK prenant en charge le modèle `ImportStringArrayOption`.

Cette API REST permet d’importer des données de type tableau de chaînes dans une feuille de calcul Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

La requête utilise du contenu HTTP multipart (voir [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) ou [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
La première partie du corps multipart contient une charge utile **ImportStringArrayOption** ; la deuxième partie contient le fichier source des données.

Les paramètres importants sont décrits dans le tableau suivant :

<caption>Paramètres de ImportStringArrayOption</caption>
### **ImportStringArrayOption**

| Nom du paramètre     | Type       | Description                                                                                                                                                                         |
| -------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Index de ligne de départ (1‑basé) où les données seront placées.                                                                                                                   |
| FirstColumn          | int        | Index de colonne de départ (1‑basé) où les données seront placées.                                                                                                                  |
| IsVertical           | boolean    | `true` pour insérer les données verticalement ; `false` pour les insérer horizontalement.                                                                                         |
| Data                 | String[]   | Le tableau de chaînes à importer.                                                                                                                                                   |
| DestinationWorksheet | string     | Le nom de la feuille de calcul qui recevra les données.                                                                                                                            |
| IsInsert             | boolean    | `true` pour insérer des lignes/colonnes (décalant les cellules existantes) ; `false` pour écraser les cellules existantes.                                                        |
| ImportDataType       | string     | Type de données à importer (par exemple, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource | Indique l’emplacement du fichier de données lorsque **BatchData** est null (par exemple, `CloudFileSystem`, `LocalFile`). Obligatoire si `BatchData` n’est pas fourni.            |

### Exemple

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
```

### Réponse

Une requête réussie renvoie **HTTP 200** avec une charge utile JSON similaire à :

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Codes d’état possibles :

| Code | Signification                                     |
| ---- | ------------------------------------------------- |
| 200  | L’importation a réussi                           |
| 400  | Requête incorrecte – données manquantes ou invalides |
| 401  | Accès non autorisé – jeton invalide ou manquant  |
| 500  | Erreur interne du serveur                         |


## Comment utiliser l’API PostImportData avec les SDK

### Spécification de l’API PostImportData

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
---