---
title: "Chiffrer, déchiffrer et signer numériquement des fichiers Excel"
second_title: "Document"
linktype: "Protéger Excel"
type: docs
url: /fr/protect/
aliases: [  /fr/workbook/password/ ]
keywords: "Excel, protéger, chiffrer, déchiffrer, signature numérique, Aspose.Cells Cloud, API REST, mot de passe, sécurité"
description: "Découvrez comment protéger, chiffrer, déchiffrer et signer numériquement des classeurs Excel à l'aide de l'API REST Aspose.Cells Cloud – exemples de code pour Android, C#, Java, Python et plus encore."
ArticleTitle: "Chiffrer, déchiffrer, signer numériquement et protéger des fichiers Excel à l'aide de l'API Aspose.Cells Cloud"
weight: 36
---

## **Protéger et déprotéger des fichiers Excel**

**Qu’est-ce que la fonction « Protéger » dans Aspose.Cells Cloud ?**  
L’opération **Protect** sécurise un classeur Excel en appliquant un mot de passe qui restreint l’ouverture, la modification ou la modification de la structure du fichier. L’API prend également en charge le chiffrement du classeur, son déchiffrement et l’ajout d’une signature numérique pour une vérification inviolable.

**Référence de l’API**  

| Méthode HTTP | Point de terminaison | Paramètres requis (requête / corps) | Corps de la requête exemple | Réponses typiques |
|-------------|----------|-----------------------------------|---------------------|-------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName` (chemin), `password` (requête) | `{ "password": "MonSecret123" }` | `200 OK` – protection appliquée, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (chemin), `password` (requête) | N/A | `200 OK` – protection supprimée, codes d’erreur comme ci-dessus |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName` (chemin), `password` (requête) | N/A | `200 OK` – fichier chiffré |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName` (chemin), `password` (requête) | N/A | `200 OK` – fichier déchiffré |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName` (chemin) | `{ "certificatePath": "/certs/moncertificat.pfx", "certificatePassword": "motdepasseCertificat" }` | `200 OK` – signature numérique ajoutée |

**Exemple de code (C#)**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Initialiser le client API
var config = new Configuration
{
    AppSid = "VOTRE_APP_SID",
    AppKey = "VOTRE_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// Protéger le classeur
var protectRequest = new PostProtectWorkbookRequest(
    name: "Exemple.xlsx",
    password: "MonSecret123"
);
api.PostProtectWorkbook(protectRequest);
```

**Prérequis**  
- Un abonnement actif à Aspose.Cells Cloud.  
- `AppSid` et `AppKey` pour l’authentification.  

**Authentification**  
Toutes les requêtes doivent inclure l’en-tête `Authorization` avec un jeton JWT valide obtenu à partir du point de terminaison d’authentification d’Aspose Cloud.

**Gestion des erreurs**  
Vérifiez le code de statut HTTP et l’objet `Error` retourné dans le corps de la réponse. Les erreurs courantes incluent un mot de passe invalide (`400`), un fichier manquant (`404`) et des échecs d’authentification (`401`).

**Notes**  
- Le même point de terminaison peut être utilisé pour **chiffrer** ou **déchiffrer** en modifiant la section d’action (`/encrypt`, `/decrypt`).  
- Les signatures numériques exigent un fichier de certificat valide accessible à l’API.

- [Chiffrer un fichier Excel avec l’API Aspose.Cells Cloud](/cells/excel-file-encrypt/)
- [Protéger un fichier Excel avec l’API Aspose.Cells Cloud](/cells/protect-excel-file/)
- [Ajouter une signature numérique à un fichier Excel](/cells/excel-digital-signature/)
- [Protéger les fichiers Excel – guide détaillé](/cells/protect-excel-files/)
- [Définir un mot de passe pour un fichier Excel](/cells/workbook/password/modify/)
- [Déchiffrer un fichier Excel](/cells/excel-file-decrypt/)
- [Déprotéger un fichier Excel](/cells/excel-file-unprotect/)
- [Déverrouiller des fichiers Excel](/cells/unlock-excel-files/)
- [Effacer le mot de passe d’un fichier Excel](/cells/clear-excel-files-password/)
---