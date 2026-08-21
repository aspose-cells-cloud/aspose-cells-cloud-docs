---
title: "Convertir un tableau en CSV"
ArticleTitle: "Convertir un tableau en CSV – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Convertir un tableau en CSV"
type: docs
url: /fr/cells/convert/table/csv
aliases: []
keywords: "Convertir un tableau en CSV, Aspose.Cells, API cloud"
description: "Convertit un tableau d’une feuille de calcul située sur un disque local en fichier CSV."
weight: 1
---

## Convertir un tableau en CSV via les services web Aspose.Cells Cloud

Cette méthode lit un fichier de feuille de calcul à partir du système de fichiers local, convertit le tableau spécifié en fichier CSV, puis renvoie le résultat de la conversion. Elle s’exécute entièrement sur le serveur cloud, donc aucune mise en ligne intermédiaire vers un espace de stockage cloud n’est nécessaire. Le chemin du fichier source et le format cible doivent être correctement spécifiés, et des autorisations appropriées sont requises pour lire le fichier source. Les erreurs telles que l’absence du fichier, l’inaccessibilité du chemin ou les échecs de conversion entraîneront des exceptions appropriées.

### Point de terminaison de l’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|--------|--------------------------------------------------------|-------------|
| Spreadsheet      | Fichier | FormData                                              | Télécharger le fichier de feuille de calcul. |
| worksheet        | Chaîne  | Chaîne de requête                                      | Nom de la feuille de calcul. |
| tableName        | Chaîne  | Chaîne de requête                                      | Nom du tableau. |
| outPath          | Chaîne  | Chaîne de requête                                      | (Facultatif) Chemin du dossier où le classeur sera stocké. Valeur par défaut : null. |
| outStorageName   | Chaîne  | Chaîne de requête                                      | Nom du stockage de destination. |
| fontsLocation    | Chaîne  | Chaîne de requête                                      | Utiliser des polices personnalisées. |
| AutoRowsFit      | Booléen | Chaîne de requête                                      | (Facultatif) Ajuster automatiquement la hauteur de toutes les lignes dans les feuilles de calcul. |
| AutoColumnsFit   | Booléen | Chaîne de requête                                      | (Facultatif) Ajuster automatiquement la largeur de toutes les colonnes dans les feuilles de calcul. |
| region           | Chaîne  | Chaîne de requête                                      | Paramètres régionaux/langue de la feuille de calcul (par ex. `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne  | Chaîne de requête                                      | Mot de passe pour ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| *Aucun*          | *Aucun* | *Aucun corps de requête n’est requis ; le fichier est transmis en tant que multipart/form-data.* |

### **Réponse**

```json
{
  "file": "flux binaire du fichier CSV généré"
}
```

**Codes de statut de réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK            | Le tableau a été converti avec succès et le fichier CSV est renvoyé. |
| 400  | Mauvaise requête | Paramètres de requête invalides ou URL mal formée. |
| 401  | Non autorisé  | L’authentification a échoué ou aucune information d’identification n’a été fournie. |
| 404  | Introuvable   | Le fichier source n’est pas accessible ou n’existe pas. |
| 413  | Charge utile trop volumineuse | Le fichier téléversé dépasse la taille maximale autorisée. |
| 500  | Erreur interne du serveur | Une anomalie s’est produite lors de la conversion de la feuille de calcul. |

## Comment utiliser la conversion de tableau en CSV avec les SDK

### Spécification de la conversion de tableau en CSV

La [spécification de l’API Convert Table to CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCsv) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton JWT>" \
  -F "Spreadsheet=@exemple.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "flux binaire du fichier CSV généré"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK abstrait les détails de bas niveau, vous permettant de vous concentrer sur vos tâches de projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
`[TBD]`
---