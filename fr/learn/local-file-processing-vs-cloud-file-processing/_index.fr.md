---
title: "Quelle est la différence entre le traitement local des fichiers et le traitement cloud des fichiers dans Aspose.Cells Cloud ?"
second_title: "Document"
ArticleTitle: "Quelle est la différence entre le traitement local des fichiers et le traitement cloud des fichiers dans Aspose.Cells Cloud ?"
linktitle: "Traitement local des fichiers vs. traitement cloud des fichiers"
type: docs
url: /fr/learn/local-file-processing-vs-cloud-file-processing/
description: "Comparez le traitement local et cloud des fichiers dans Aspose.Cells Cloud : stockage, coûts, sécurité et scénarios typiques. Découvrez quelle approche correspond à votre flux de travail."
keywords: "Aspose.Cells Cloud, traitement local des fichiers, traitement cloud des fichiers, conversion de feuilles de calcul, API"
weight: 10
---

Le traitement local des fichiers et le traitement cloud des fichiers constituent deux paradigmes distincts de gestion des données, avec des différences significatives concernant l’infrastructure de stockage des fichiers, le traitement métier, l’accès, la structure des coûts, la sécurité et les scénarios applicables. Les principales différences entre les deux sont les suivantes :

**Prérequis :** Avant d’utiliser les exemples, assurez-vous de disposer d’un compte Aspose.Cells Cloud valide, de la dernière version du SDK installée, ainsi que de vos identifiants Client Id et Client Secret nécessaires à l’authentification.

## 1. Emplacement du stockage des fichiers et infrastructure

- Fichier local :

  - Les fichiers sont stockés sur des dispositifs physiques possédés ou gérés par l’utilisateur, tels que le disque dur d’un ordinateur personnel, des serveurs internes ou des disques durs externes. **Vous pouvez pointer directement le client Cells Cloud vers un fichier situé sur n’importe quel dispositif de stockage local.**
  - Le client exerce un contrôle total sur le matériel.
  - L’acquisition, la maintenance, la mise à niveau et le retrait de l’infrastructure relèvent de la responsabilité de l’utilisateur ou de son organisation.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest

# Initialiser CellsApi
api = CellsApi('VotreClientIdCellsCloud', 'VotreClientSecretCellsCloud')

# Convertir un fichier Excel local en PDF
api.convert_spreadsheet(
    ConvertSpreadsheetRequest('D:\\Data\\BookSales.xlsx', "pdf"),
    local_outpath="BookSales.pdf"
)
```

**Référence API – Convert Spreadsheet**

| Méthode                 | Verbe HTTP | Point de terminaison | Paramètres (clé)                                         | Réponses                                         |
|-------------------------|------------|----------------------|----------------------------------------------------------|--------------------------------------------------|
| `convert_spreadsheet`   | POST       | `/cells/convert`     | `inputFile` – chemin du fichier source<br>`format` – format cible (ex. `pdf`) | `200 OK` – conversion réussie<br>`400 Bad Request` – paramètres invalides<br>`401 Unauthorized` – échec d’authentification |

- Fichier cloud :

  - Les fichiers sont stockés dans des centres de données distants exploités par des fournisseurs de services cloud tiers (stockage cloud Aspose, Dropbox, AWS, Google Cloud, Microsoft Azure). **AWS, Dropbox, Google Cloud et Microsoft Azure peuvent tous se connecter au stockage cloud Aspose.**
  - Les clients accèdent à ces fichiers via Internet, indépendamment de l’emplacement et de la maintenance du matériel sous-jacent.
  - L’infrastructure relève de la responsabilité du fournisseur de services cloud, que les utilisateurs exploitent à la demande.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import (
    UploadFileRequest,
    ExportSpreadsheetAsFormatRequest,
    SaveSpreadsheet_asRequest,
)

# Initialiser CellsApi
api = CellsApi('VotreClientIdCellsCloud', 'VotreClientSecretCellsCloud')

# Téléverser un fichier local vers le stockage cloud
api.upload_file(
    UploadFileRequest(
        "D:\\Data\\EmployeeSalesSummary.xlsx",
        "PythonSDK/EmployeeSalesSummary.xlsx"
    )
)

# Exporter un fichier cloud vers un fichier dans un format spécifié, stocké localement
api.export_spreadsheet_as_format(
    ExportSpreadsheetAsFormatRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder="PythonSDK"
    ),
    local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf"
)

# Définir le dossier distant (remplacer par le nom réel de votre dossier, le cas échéant)
RemoteFolder = "PythonSDK"

# Enregistrer un fichier Excel dans Aspose.Cells Cloud en un autre format dans Aspose.Cells Cloud
api.save_spreadsheet_as(
    SaveSpreadsheetAsRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder=RemoteFolder
    )
)
```

**Référence API – Opérations sur les fichiers cloud**

| Méthode                        | Verbe HTTP | Point de terminaison           | Paramètres (clé)                                                                                      | Réponses                                         |
|--------------------------------|------------|--------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| `upload_file`                  | PUT        | `/cells/storage/file`          | `localPath` – chemin local du fichier<br>`remotePath` – emplacement dans le stockage cloud           | `200 OK` – téléversement réussi<br>`401 Unauthorized` |
| `export_spreadsheet_as_format` | POST       | `/cells/{name}/export`         | `name` – nom du fichier cloud<br>`format` – format cible (ex. `pdf`)<br>`folder` – dossier optionnel | `200 OK` – export réussi<br>`400 Bad Request` |
| `save_spreadsheet_as`          | POST       | `/cells/{name}/saveas`         | `name` – nom du fichier cloud<br>`format` – format cible<br>`folder` – dossier de destination       | `200 OK` – enregistrement réussi<br>`401 Unauthorized` |

## 2. Traitement métier

Que ce soit le traitement local ou cloud des fichiers, **tous les traitements métier sont exécutés sur le serveur Cells Cloud**, ce qui rend une connexion Internet obligatoire.

## 3. Accès aux données

- Traitement local des fichiers :

  - L’accès est généralement limité à l’appareil lui-même.
  - La collaboration à plusieurs est difficile.
  - Inconvénients lors de changement d’équipement ou de lieu.

- Traitement cloud des fichiers :

  - Accès aux fichiers depuis n’importe quel appareil (ordinateur, téléphone, tablette), à tout moment et en tout lieu, dès lors qu’une connexion Internet est disponible.
  - Prise en charge naturelle de la collaboration en temps réel à plusieurs utilisateurs : plusieurs personnes peuvent modifier simultanément le même document, le système gérant automatiquement le contrôle des versions.
  - Grande mobilité, prise en charge flexible du travail en bureau et du télétravail.

## 4. Structure des coûts et sécurité

- Fichier local :

  - Un investissement initial élevé est requis. Cela entraîne des coûts supplémentaires pour le support opérationnel ultérieur.
  - La sécurité physique et la sécurité réseau sont entièrement contrôlées par les utilisateurs eux-mêmes.

- Fichier cloud :

  - Investissement initial faible, principalement des coûts opérationnels, mode de facturation à l’usage.
  - La sécurité et l’intégrité des données relèvent de la responsabilité du fournisseur de services cloud.

## 5. Scénarios applicables

- Fichier local : Les opérations sur les fichiers ne peuvent être effectuées que localement.  
- Fichier cloud : Les opérations sur les fichiers peuvent être effectuées localement ou dans le cloud.  

**Remarques / Limitations :** L’API prend en charge des fichiers d’une taille maximale de 200 Mo pour le traitement cloud, et seuls les formats listés dans la documentation peuvent être convertis. La latence réseau peut affecter la durée de traitement pour de grandes feuilles de calcul.

_Dernière mise à jour : 30 juillet 2026_