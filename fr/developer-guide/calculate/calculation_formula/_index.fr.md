---
title: "Calculer une formule"
ArticleTitle: "Calculer une formule – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /fr/cells/calculate/formula
aliases: []
keywords: "Aspose Cells, calculer une formule, feuille de calcul, API"
description: "Calculer une formule dans une feuille de calcul à l’aide de l’API Aspose.Cells Cloud."
weight: 100
---

## La fonction de calcul de formule des services web Aspose.Cells Cloud

Calcule une formule spécifiée dans une feuille de calcul donnée d’un fichier de feuille de calcul téléchargé et renvoie la feuille de calcul résultante sous forme de flux de fichier. Cette opération prend en charge le traitement spécifique à la locale via le paramètre **region** et peut ouvrir des fichiers protégés par mot de passe.

### Point de terminaison de l’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la demande

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|--------|--------------------------------------------------------|-------------|
| Spreadsheet      | Fichier | FormData                                               | Télécharger le fichier de feuille de calcul. |
| worksheet        | Chaîne  | Chaîne de requête                                       | Nom de la feuille de calcul contenant la formule. |
| formula          | Chaîne  | Chaîne de requête                                       | Formule à calculer (par exemple, `=SUM(A1:B2)`). |
| region           | Chaîne  | Chaîne de requête                                       | Paramètre régional/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne  | Chaîne de requête                                       | Mot de passe permettant d’ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la demande

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| [À déterminer] | [À déterminer] | [À déterminer] |

### **Réponse**

```json
{
  "File": "<flux binaire de la feuille de calcul résultante>"
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK            | Le calcul a réussi ; le fichier de feuille de calcul résultant est renvoyé. |
| 400  | Mauvaise demande | Un ou plusieurs paramètres de la demande sont manquants ou non valides. |
| 401  | Non autorisé  | L’authentification a échoué ou le jeton JWT est manquant/non valide. |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille autorisée. |
| 500  | Erreur interne du serveur | Une erreur inattendue s’est produite sur le serveur. |

## Comment utiliser la fonction de calcul de formule à l’aide des SDK

### Spécification de la fonction de calcul de formule

La [spécification de l’API de calcul de formule](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Demande" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUM(A1%3AB2)&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "<flux binaire de la feuille de calcul résultante>"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK abstractise les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
 `[À déterminer]`
---