---
title: "Convertir un tableau en PDF"
ArticleTitle: "Convertir un tableau en PDF – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /cells/convert/table/pdf
aliases: []
keywords: "convertir tableau PDF, Aspose.Cells, API"
description: "Convertit un tableau d’un fichier de calcul stocké localement en fichier PDF à l’aide d’Aspose.Cells Cloud."
weight: 1000
---

## Conversion d’un tableau en PDF via les services web Aspose.Cells Cloud

Cette opération lit un fichier de calcul à partir du système de fichiers local, convertit le tableau spécifié en document PDF, puis renvoie le résultat de la conversion. Elle s’exécute entièrement sur le serveur cloud, ce qui élimine le besoin d’un téléversement intermédiaire vers le stockage cloud. L’API prend en charge des paramètres facultatifs pour le chemin de sortie, les polices personnalisées, l’ajustement automatique des lignes et colonnes, les paramètres régionaux, ainsi que les classeurs protégés par mot de passe.

### Point de terminaison de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                     |
|------------------|--------|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fichier| FormData                                              | Téléchargement du fichier de calcul.                                                                                                                            |
| worksheet        | Chaîne | Chaîne de requête                                     | Nom de la feuille de calcul.                                                                                                                                    |
| tableName        | Chaîne | Chaîne de requête                                     | Nom du tableau.                                                                                                                                                 |
| outPath          | Chaîne | Chaîne de requête                                     | (Facultatif) Chemin du dossier dans lequel le classeur est stocké. La valeur par défaut est null.                                                             |
| outStorageName   | Chaîne | Chaîne de requête                                     | Nom du stockage pour le fichier de sortie.                                                                                                                     |
| fontsLocation    | Chaîne | Chaîne de requête                                     | Utilisation de polices personnalisées.                                                                                                                          |
| AutoRowsFit      | Booléen| Chaîne de requête                                     | (Facultatif) Ajuste automatiquement toutes les lignes des feuilles de calcul.                                                                                  |
| AutoColumnsFit   | Booléen| Chaîne de requête                                     | (Facultatif) Ajuste automatiquement toutes les colonnes des feuilles de calcul.                                                                                |
| region           | Chaîne | Chaîne de requête                                     | Paramètres régionaux/langue du fichier de calcul (par ex. `en-US`, `fr-FR`). Affecte la mise en forme des nombres, l’analyse des dates et le comportement lié aux paramètres régionaux. |
| password         | Chaîne | Chaîne de requête                                     | Mot de passe permettant d’ouvrir le fichier de calcul.                                                                                                         |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
|------------------|------|-------------|
| *Aucun*          | *Aucun* | *Aucun corps JSON n’est requis ; le fichier est transmis via multipart/form-data.* |

### **Réponse**

```json
{
  "file": "<contenu binaire PDF>"
}
```

**Codes d’état de la réponse**

| Code | Signification       | Description |
|------|---------------------|-------------|
| 200  | OK                  | Le tableau a été converti avec succès en PDF ; le corps de la réponse contient le flux du fichier PDF. |
| 400  | Requête incorrecte  | Paramètres de requête invalides ou URL mal formée. |
| 401  | Non autorisé        | L’authentification a échoué ou aucune information d’identification n’a été fournie. |
| 404  | Introuvable         | Le fichier source est inaccessible ou la feuille/tableau est introuvable. |
| 413  | Payload trop volumineux | Le fichier de calcul téléversé dépasse la taille maximale autorisée. |
| 500  | Erreur interne du serveur | Une erreur s’est produite lors de la conversion du fichier de calcul en PDF. |

## Comment utiliser la conversion d’un tableau en PDF à l’aide des SDK

### Spécification de la conversion d’un tableau en PDF

La [spécification de l’API de conversion d’un tableau en PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<contenu binaire PDF>"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur vos tâches de projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :

```csharp
// Exemple de code SDK pour C#
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// Exemple de code SDK pour Java
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Exemple de code SDK pour Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[À compléter]`