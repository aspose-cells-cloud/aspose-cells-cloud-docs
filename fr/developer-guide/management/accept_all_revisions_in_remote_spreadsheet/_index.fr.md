---
title: "Accepter toutes les révisions dans une feuille de calcul distante"
ArticleTitle: "Accepter toutes les révisions dans une feuille de calcul distante – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Accepter toutes les révisions dans une feuille de calcul distante"
type: docs
url: /cells/accept-all-revisions
aliases: ["/cells/accept-all-revisions"]
keywords: "Aspose.Cells, AcceptAllRevisions, feuille de calcul distante"
description: "Accepter toutes les révisions dans une feuille de calcul distante et renvoyer le classeur mis à jour."
weight: 1000
---

## Accepter toutes les révisions dans une feuille de calcul distante avec les services web Aspose.Cells Cloud

Accepte toutes les modifications suivies (révisions) dans le classeur spécifié stocké dans le stockage distant. L’opération peut éventuellement écrire le classeur résultant dans un emplacement ou un stockage différent, puis renvoie le fichier mis à jour sous forme de flux binaire.

### Point de terminaison de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|------|--------------------------------------------------------|-------------|
| name | string | Chemin | Le nom du fichier de classeur stocké dans le stockage distant. |
| folder | string | Chaîne de requête | (Facultatif) Dossier dans le stockage où se trouve le classeur. |
| storageName | string | Chaîne de requête | (Facultatif) Nom du stockage lorsqu’un stockage cloud personnalisé est utilisé. Le stockage par défaut est utilisé si ce paramètre est omis. |
| outPath | string | Chaîne de requête | (Facultatif) Chemin du dossier où le classeur mis à jour doit être enregistré. La valeur par défaut est null. |
| outStorageName | string | Chaîne de requête | (Facultatif) Nom du stockage de destination pour le fichier généré. |
| fontsLocation | string | Chaîne de requête | (Facultatif) Chemin vers l’emplacement personnalisé des polices. |
| region | string | Chaîne de requête | (Facultatif) Paramètre régional/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password | string | Chaîne de requête | (Facultatif) Mot de passe nécessaire pour ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| *Aucun* | *Aucun* | Cette opération ne nécessite pas de corps de requête. |

### **Réponse**

```json
{
  "File": "Flux binaire du classeur mis à jour (par exemple, .xlsx) renvoyé dans le corps de la réponse."
}
```

**Codes d’état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | Le classeur avec toutes les révisions acceptées est renvoyé sous forme de flux binaire. |
| 400 | Mauvaise requête | Paramètres requis manquants ou format de requête invalide. |
| 401 | Non autorisé | Jeton JWT invalide ou manquant. |
| 413 | Charge utile trop volumineuse | La requête dépasse les limites de taille autorisées. |
| 500 | Erreur interne du serveur | Une erreur inattendue s’est produite côté serveur. |

## Comment utiliser l’option « Accepter toutes les révisions dans une feuille de calcul distante » avec les SDK

### Spécification de l’API « Accepter toutes les révisions dans une feuille de calcul distante »

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet" rel="noopener noreferrer">spécification de l’API « Accepter toutes les révisions dans une feuille de calcul distante »</a> définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "Flux binaire du classeur mis à jour (par exemple, .xlsx)."
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :
`[À compléter]`
---