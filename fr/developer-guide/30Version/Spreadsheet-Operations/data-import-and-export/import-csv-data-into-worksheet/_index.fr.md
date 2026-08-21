---
title: "Importer des données CSV dans une feuille Excel"
second_title: "Document"
linktype: "Importer des données CSV"
type: docs
url: /fr/import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "Importer des données CSV, Excel, Aspose.Cells Cloud, API REST, classeur, import CSV"
description: "L’API REST Aspose.Cells Cloud permet d’importer des données CSV dans des feuilles Excel. Les SDK pris en charge incluent Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby et Swift."
weight: 19
---

Cette API REST **importe des données CSV** dans une feuille Excel.

La requête est une requête HTTP contenant un contenu multipart (voir [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) ou [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du contenu multipart contient les données `ImportCSVDataOption`, et la deuxième partie contient le fichier CSV.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

Les paramètres importants sont décrits dans les tableaux ci-dessous.

### ImportCSVDataOption

| Nom du paramètre   | Type                       | Description                                                              |
| ------------------ | -------------------------- | ------------------------------------------------------------------------ |
| SeparatorString    | string                     | Caractère utilisé pour séparer les champs dans le fichier CSV (par exemple `,` ou `;`). |
| ConvertNumericData | string (`true`/`false`)    | Indique si les chaînes numériques doivent être converties en valeurs numériques. |
| FirstRow           | int                        | Indice (à partir de 1) de la première ligne où les données seront insérées. |
| FirstColumn        | int                        | Indice (à partir de 1) de la première colonne où les données seront insérées. |
| SourceFile         | string                     | Nom du fichier CSV source à importer.                                    |
| CustomParsers      | List\<CustomParserConfig\> | Collection de configurations d’analyseurs personnalisés pour des colonnes spécifiques. |

### CustomParserConfig

| Nom du paramètre | Type   | Description                                                              |
| ---------------- | ------ | ------------------------------------------------------------------------ |
| ColumnIndex      | int    | Indice (à partir de 0) de la colonne à laquelle l’analyseur personnalisé s’applique. |
| ParseMethod      | string | Méthode d’analyse de la colonne (par exemple `ToString`, `ToDate`, `ToNumber`). |
| CustomStyle      | string | Style personnalisé (par exemple format numérique) appliqué aux cellules analysées. |

**Exemple**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```
### Réponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                            |
|------|-----------------------------|------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                        |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la taille limite.                       |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                                          |
## Comment utiliser l’API PostImportData à l’aide des SDK

### Spécification de l’API PostImportData

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) définit une interface de programmation accessible publiquement qui permet d’effectuer directement des interactions REST depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen optimal d’accélérer le développement. Un SDK abstractise les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

L’exemple de code suivant montre comment appeler le service web Aspose.Cells à l’aide du SDK PHP :

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}