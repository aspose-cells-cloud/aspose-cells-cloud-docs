---
title: Quelle est la différence entre le traitement des fichiers locaux et le traitement des fichiers cloud dans Aspose.Cells Cloud
second_title: Documen
ArticleTitle: What is the difference between local file processing and cloud file processing in Aspose.Cells Cloud
linktitle: Traitement de fichiers local vs. traitement de fichiers dans le cloud
type: docs
url: /fr/learn/local-file-processing-vs-cloud-file-processing/
description: Quelle est la différence entre le traitement local et le traitement cloud ? Le traitement local et le traitement cloud sont deux paradigmes de gestion des données fondamentalement différents, avec des différences significatives en termes d'infrastructure de stockage, de traitement métier, d'accès, de structure de coûts, de sécurité et de scénarios d'application.
weight: 10
kwords: Excel Cloud API, REST, Tableur, PDF, CSV, Json, Markdown, Traitement de fichiers local vs. Traitement de fichiers cloud
---
Le traitement local et le traitement cloud des fichiers constituent des paradigmes de gestion des données distincts, avec des différences significatives en termes d'infrastructure de stockage, de traitement métier, d'accès, de structure de coûts, de sécurité et de scénarios d'application. Les principales différences entre les deux sont :

## 1. Emplacement et infrastructure de stockage des fichiers

- Fichier local:

Les fichiers sont stockés sur des supports physiques appartenant à l'utilisateur ou gérés par lui, tels que le disque dur d'un ordinateur personnel, des serveurs internes ou des disques durs externes. Ces supports sont accessibles directement depuis le client Cloud Cells.
 - Le client a un contrôle physique complet sur le matériel.
 - L’achat, la maintenance, la mise à niveau et le retrait de l’infrastructure sont de la responsabilité de l’utilisateur ou de son organisation.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Convert Local Excel file to PDF
api.convert_spreadsheet( ConvertSpreadsheetRequest( 'D:\\Data\\BookSales.xlsx', "pdf" ) , local_outpath = "BookSales.pdf")

```

- Fichier Cloud :

 - Les fichiers sont stockés dans des centres de données distants exploités par des fournisseurs de services cloud tiers (stockage cloud Aspose, Dropbox, AWS, Google Cloud, Microsoft Azure). AWS, Dropbox, Google Cloud et Microsoft Azure peuvent tous connecter des personnes au stockage cloud Aspose.
 - Les clients accèdent à ces fichiers via Internet, quel que soit l’emplacement et la maintenance du matériel sous-jacent.
 - L'infrastructure est la responsabilité du fournisseur de services cloud et les utilisateurs l'utilisent à la demande.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import UploadFileRequest, ExportSpreadsheetAsFormatRequest, SaveSpreadsheetAsRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Upload local file to cloud storage
api.upload_file( UploadFileRequest("D:\\Data\\EmployeeSalesSummary.xlsx", "PythonSDK/EmployeeSalesSummary.xlsx"))
# Export cloud file to specified format file to local storage
api.export_spreadsheet_as_format( ExportSpreadsheetAsFormatRequest( "EmployeeSalesSummary.xlsx","pdf" ,folder= "PythonSDK"  ) , local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf" )
# Or Save an Excel file of Cells Cloud as another format file of Cells Cloud. 
api.save_spreadsheet_as( SaveSpreadsheetAsRequest (  "EmployeeSalesSummary.xlsx","pdf" ,folder= RemoteFolder ) )

```

## 2. Traitement des affaires

Quel que soit le traitement des fichiers locaux ou le traitement des fichiers dans le cloud, tous les traitements commerciaux sont effectués sur le serveur Cloud Cells,**donc un support Internet est nécessaire**.

## 3. Accès aux données

- Traitement des fichiers locaux :

 - L'accès est généralement limité à l'appareil lui-même.
 - La collaboration entre plusieurs personnes est difficile.
 - Inconvénients liés au changement d'équipement ou de lieu.

- Traitement des fichiers dans le cloud :

 - Accédez aux fichiers depuis n'importe quel appareil (ordinateur, téléphone, tablette) à tout moment, n'importe où, à condition de disposer d'une connexion Internet.
 - Prise en charge naturelle de la collaboration multi-personnes en temps réel, plusieurs utilisateurs peuvent modifier le même document en même temps, le système gère automatiquement le contrôle des versions.
 - Forte mobilité, support flexible office et travail à distance.
  
## 4. Structure des coûts et sécurité

- Fichier local:
  
 - Des dépenses d’investissement élevées au début nécessitent certains coûts de soutien opérationnel à un stade ultérieur.
 La sécurité physique et la sécurité du réseau sont toutes deux contrôlées par les utilisateurs eux-mêmes.

- Fichier Cloud :

 - Faible investissement initial, principalement des frais d'exploitation, paiement à la demande.
 - La sécurité et l’intégrité sont les responsabilités du fournisseur de services cloud.

## 5. Scénarios applicables

- Fichier local : les opérations sur les fichiers ne peuvent être effectuées que localement.
- Fichier cloud : les opérations sur les fichiers peuvent être effectuées localement ou dans le cloud.
