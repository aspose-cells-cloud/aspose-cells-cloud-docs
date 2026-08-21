---
---
title: "Traitement par lots de fichiers Excel : conversion, verrouillage, protection, division et déverrouillage"
second_title: "Document"
linktitle: "Fichiers Excel en lot"
type: docs
url: /batch/
keywords: "Traitement par lots, Excel, conversion, verrouillage, protection, division, déverrouillage, API Aspose.Cells Cloud, référence API, opérations par lots"
description: "L'API Aspose.Cells Cloud permet le traitement par lots de plusieurs fichiers Excel pour la conversion, le verrouillage, la protection, la division et le déverrouillage. Inclut des spécifications API détaillées et une prise en charge des SDK pour Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift."
weight: 35
ArticleTitle: "Traitement par lots de fichiers Excel – Convertir, verrouiller, protéger, diviser et déverrouiller avec l'API Aspose.Cells Cloud"
---

L'API Aspose.Cells Cloud fournit des points de terminaison en lot qui vous permettent d'effectuer des opérations courantes sur plusieurs fichiers Excel en une seule requête. Ci-dessous, un aperçu rapide des opérations par lots disponibles, accompagné de spécifications API concises pour chacune.

- **["Conversion par lots de fichiers Excel"](https://docs.aspose.cloud/cells/batch/convert "Conversion par lots de fichiers Excel")**  
  *Convertir plusieurs fichiers Excel vers un format de sortie choisi en une seule requête.*  

  **Détails de l’API**  
  ```http
  POST /cells/batch/convert
  Content-Type: multipart/form-data
  Authorization: Bearer {access_token}
  ```  

  **Paramètres**  

  | Nom           | Type     | Description                                   |
  |---------------|----------|-----------------------------------------------|
  | files         | file[]   | Un ou plusieurs fichiers Excel à convertir.  |
  | outputFormat  | string   | Format de sortie souhaité (par ex. pdf, csv, html). |
  | storage       | string   | (Facultatif) Nom du stockage dans le cloud.  |

  **Réponses**  

  | Code | Description                                |
  |------|--------------------------------------------|
  | 200  | Conversion réussie ; renvoie les fichiers. |
  | 400  | Paramètres fournis non valides.            |
  | 401  | Accès non autorisé – jeton manquant ou non valide. |
  | 500  | Erreur interne du serveur.                 |

- **["Verrouillage par lots de fichiers Excel"](https://docs.aspose.cloud/cells/batch/lock "Verrouillage par lots de fichiers Excel")**  
  *Appliquer un verrouillage par mot de passe à plusieurs fichiers Excel simultanément.*  

  **Détails de l’API**  
  ```http
  POST /cells/batch/lock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Paramètres**  

  | Nom      | Type   | Description                             |
  |----------|--------|-----------------------------------------|
  | files    | array  | Liste d'identifiants de fichiers ou d'URL. |
  | password | string | Mot de passe à utiliser pour verrouiller les classeurs. |
  | storage  | string | (Facultatif) Nom du stockage dans le cloud. |

  **Réponses**  

  | Code | Description                               |
  |------|-------------------------------------------|
  | 200  | Fichiers verrouillés avec succès.         |
  | 400  | Paramètres manquants ou non valides.      |
  | 401  | Accès non autorisé.                       |
  | 500  | Erreur serveur.                           |

- **["Protection par lots de fichiers Excel"](https://docs.aspose.cloud/cells/batch/protect "Protection par lots de fichiers Excel")**  
  *Appliquer des paramètres de protection (par ex. en lecture seule, structure) à plusieurs classeurs.*  

  **Détails de l’API**  
  ```http
  POST /cells/batch/protect
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Paramètres**  

  | Nom           | Type   | Description                                      |
  |---------------|--------|--------------------------------------------------|
  | files         | array  | Liste d'identifiants de fichiers ou d'URL.      |
  | protection    | object | Options de protection (par ex. readOnly, structure). |
  | storage       | string | (Facultatif) Nom du stockage dans le cloud.     |

  **Réponses**  

  | Code | Description                               |
  |------|-------------------------------------------|
  | 200  | Protection appliquée avec succès.         |
  | 400  | Données de requête non valides.           |
  | 401  | Échec de l'authentification.              |
  | 500  | Erreur serveur inattendue.                |

- **["Division par lots"](https://docs.aspose.cloud/cells/batch/split "Division par lots")**  
  *Diviser de grands classeurs Excel en fichiers plus petits selon les feuilles de calcul ou des plages de lignes.*  

  **Détails de l’API**  
  ```http
  POST /cells/batch/split
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Paramètres**  

  | Nom         | Type   | Description                                    |
  |-------------|--------|------------------------------------------------|
  | files       | array  | Fichiers à diviser.                            |
  | splitBy     | string | Critère : "worksheet" ou "rowRange".           |
  | criteria    | object | Détails de la méthode de division choisie.    |
  | storage     | string | (Facultatif) Nom du stockage dans le cloud.   |

  **Réponses**  

  | Code | Description                               |
  |------|-------------------------------------------|
  | 200  | Opération de division terminée ; renvoie les parties. |
  | 400  | Paramètres de division incorrects.         |
  | 401  | Requête non autorisée.                     |
  | 500  | Erreur de traitement.                      |

- **["Déverrouillage par lots"](https://docs.aspose.cloud/cells/batch/unlock "Déverrouillage par lots")**  
  *Supprimer la protection par mot de passe de plusieurs fichiers Excel en une seule appel.*  

  **Détails de l’API**  
  ```http
  POST /cells/batch/unlock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Paramètres**  

  | Nom      | Type   | Description                                   |
  |----------|--------|-----------------------------------------------|
  | files    | array  | Liste d'identifiants de fichiers verrouillés ou d'URL. |
  | password | string | Mot de passe actuel des fichiers.            |
  | storage  | string | (Facultatif) Nom du stockage dans le cloud.  |

  **Réponses**  

  | Code | Description                               |
  |------|-------------------------------------------|
  | 200  | Fichiers déverrouillés avec succès.       |
  | 400  | Mot de passe incorrect ou fichiers manquants. |
  | 401  | Accès non autorisé.                       |
  | 500  | Échec côté serveur.                       |
---