---
title: "Convertir un graphique en PDF"
ArticleTitle: "Convertir un graphique en PDF – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /cells/convert/chart/pdf
aliases: []
keywords: "ConvertChartToPdf, Aspose.Cells, PDF, conversion de graphique"
description: "Convertit un graphique d’un fichier de feuille de calcul local en PDF."
weight: 100
---

## La méthode Convert Chart to PDF des services web Aspose.Cells Cloud

Cette méthode lit un graphique à partir d’un fichier de feuille de calcul fourni via un téléchargement local, le convertit au format PDF, puis renvoie le résultat converti. Elle s’exécute entièrement sur le serveur cloud, donc aucun stockage intermédiaire n’est nécessaire. Le chemin d’accès au fichier source et le format cible doivent être corrects, et des autorisations appropriées sont nécessaires pour lire le fichier source. Les erreurs telles que des fichiers manquants, des problèmes d’accès ou des échecs de conversion entraîneront des réponses HTTP d’erreur appropriées.

### Point de terminaison de l’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (Chemin / Chaîne de requête / Corps HTTP) | Description |
|------------------|--------|-------------------------------------------------------|-------------|
| Spreadsheet      | Fichier| FormData                                              | Télécharger le fichier de feuille de calcul. |
| worksheet        | Chaîne | Chaîne de requête                                     | Nom de la feuille de calcul. |
| chartIndex       | Entier | Chaîne de requête                                     | Index du graphique dans la feuille de calcul. |
| outPath          | Chaîne | Chaîne de requête                                     | (Facultatif) Chemin du dossier où le classeur est stocké. Par défaut : null. |
| outStorageName   | Chaîne | Chaîne de requête                                     | Nom du stockage pour le fichier de sortie. |
| fontsLocation    | Chaîne | Chaîne de requête                                     | Utiliser des polices personnalisées. |
| region           | Chaîne | Chaîne de requête                                     | Paramètres régionaux/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne | Chaîne de requête                                     | Mot de passe pour ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| Spreadsheet      | Fichier | Télécharger le fichier de feuille de calcul. |

### **Réponse**

```json
{
  "ResponseFile": "flux binaire du fichier PDF"
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | Graphique converti avec succès en PDF ; fichier PDF binaire renvoyé. |
| 400 | Mauvaise requête | Paramètres de requête invalides ou URL mal formée. |
| 401 | Non autorisé | L’authentification a échoué ou aucune information d’identification n’a été fournie. |
| 404 | Non trouvé | Le fichier source n’est pas accessible. |
| 413 | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille maximale autorisée. |
| 500 | Erreur interne du serveur | Une erreur s’est produite lors du traitement de la conversion. |

## Comment utiliser la conversion de graphique en PDF à l’aide des SDK

### Spécification de la conversion de graphique en PDF

La [spécification de l’API Convert Chart to PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}
{< tab tabNum="1" >}
```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
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
  "ResponseFile": "flux binaire du fichier PDF"
}
```
{< /tab >}
{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
`[À compléter]`