---
title: "Accepter toutes les révisions"
ArticleTitle: "Accepter toutes les révisions – Aspose.Cells Cloud"
second_title: "Document"
linktype: "Accepter toutes les révisions"
type: docs
url: /cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, feuille de calcul, révisions"
description: "Accepter toutes les révisions dans un fichier de feuille de calcul à l’aide de l’API Aspose.Cells Cloud."
weight: 100
---

## AcceptAllRevisions des services web Aspose.Cells Cloud

Accepte toutes les révisions dans le fichier de feuille de calcul téléchargé et renvoie le classeur traité.

### Endpoint de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|--------|--------------------------------------------------------|-------------|
| Spreadsheet      | File   | FormData (corps HTTP)                                  | Télécharger le fichier de feuille de calcul. |
| outPath          | string | Chaîne de requête                                       | (Facultatif) Chemin du dossier où le classeur est stocké. La valeur par défaut est null. |
| outStorageName   | string | Chaîne de requête                                       | Nom du stockage pour le fichier de sortie. |
| fontsLocation    | string | Chaîne de requête                                       | Utiliser des polices personnalisées. |
| region           | string | Chaîne de requête                                       | Paramètre de région/langue de la feuille de calcul (par ex., `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement propre à la localisation. |
| password         | string | Chaîne de requête                                       | Mot de passe pour ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| Spreadsheet      | File | Télécharger le fichier de feuille de calcul. |

### **Réponse**

```json
{
  "File": "Flux binaire de la feuille de calcul traitée"
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK            | Les révisions ont été acceptées avec succès et le fichier traité est renvoyé. |
| 400  | Requête incorrecte | La requête est invalide (par ex., fichier requis manquant ou paramètres invalides). |
| 401  | Non autorisé  | L’authentification a échoué ou le jeton JWT est manquant/invalide. |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite autorisée. |
| 500  | Erreur interne du serveur | Une erreur inattendue s’est produite côté serveur. |

## Comment utiliser AcceptAllRevisions avec les SDK

### Spécification d’AcceptAllRevisions

La [spécification de l’API AcceptAllRevisions](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=dossierDeSortie&outStorageName=MonStockage&fontsLocation=/fonts&region=fr-FR&password=12345" \
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
  "File": "Flux binaire de la feuille de calcul traitée"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="[TBD]" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
 `[TBD]`
---