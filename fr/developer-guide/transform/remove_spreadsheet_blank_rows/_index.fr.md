---
title: "Supprimer les lignes vides d'une feuille de calcul"
ArticleTitle: "Supprimer les lignes vides d'une feuille de calcul – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "Supprimer les lignes vides d'une feuille de calcul"
type: docs
url: /cells/remove/blank-rows
aliases: []
keywords: "Aspose.Cells, supprimer les lignes vides, feuille de calcul, API"
description: "Supprime toutes les lignes vides d’un fichier de feuille de calcul."
weight: 100
---

## La méthode Supprimer les lignes vides d'une feuille de calcul des services web Aspose.Cells Cloud

Cette méthode supprime les lignes d'une feuille de calcul qui sont entièrement vides, c’est-à-dire ne contenant aucune donnée ni aucun objet. Elle analyse toutes les feuilles et identifie les lignes dont toutes les cellules sont vides. L’opération est effectuée directement sur la feuille de calcul, garantissant que seules les lignes sans contenu sont supprimées. Cela permet de nettoyer la feuille de calcul et d’éliminer les lignes vides inutiles, rendant les données plus organisées et plus faciles à gérer. Les utilisateurs doivent s’assurer que la feuille de calcul est sauvegardée avant d’effectuer cette opération, car les lignes supprimées ne peuvent pas être récupérées.

### Point de terminaison de l'API web

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/blank-rows
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|--------|-------------------------------------------------------|-------------|
| Spreadsheet      | Fichier | FormData                                             | Télécharger le fichier de feuille de calcul. |
| outPath          | Chaîne  | Chaîne de requête                                     | (Facultatif) Le chemin du dossier dans lequel le classeur est stocké. La valeur par défaut est null. |
| outStorageName   | Chaîne  | Chaîne de requête                                     | Nom du stockage pour le fichier de sortie. |
| region           | Chaîne  | Chaîne de requête                                     | Paramètre de région/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne  | Chaîne de requête                                     | Le mot de passe pour ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type   | Description |
|------------------|--------|-------------|
| Spreadsheet      | Fichier | Télécharger le fichier de feuille de calcul. |

### **Réponse**

```json
{
  "ResponseFile": "flux binaire"
}
```

**Codes d'état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK            | Le fichier de feuille de calcul traité, avec les lignes vides supprimées, est renvoyé. |
| 400  | Mauvaise requête | URL ou paramètres de requête invalides. |
| 401  | Non autorisé | L’authentification a échoué, ou aucune identification n’a été fournie. |
| 404  | Introuvable | Le fichier source n’est pas accessible. |
| 413  | Charge utile trop grande | La charge utile de la requête dépasse la taille autorisée. |
| 500  | Erreur interne du serveur | La feuille de calcul a rencontré une anomalie lors de l’obtention des données. |

## Comment utiliser la fonction Supprimer les lignes vides d'une feuille de calcul avec les SDK

### Spécification de la méthode Supprimer les lignes vides d'une feuille de calcul

La [Spécification de l’API Supprimer les lignes vides d'une feuille de calcul](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankRows) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}
{< tab tabNum="1" >}
```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/remove/blank-rows?outPath=dossierSortie&outStorageName=MonStockage&region=fr-FR&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F 'Spreadsheet=@exemple.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "flux binaire"
}
```
{< /tab >}
{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
`[TBD]`
---