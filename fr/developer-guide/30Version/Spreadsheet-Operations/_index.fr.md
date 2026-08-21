---
title: "Opérations sur feuilles de calcul"
second_title: "Document"
type: docs
url: /spreadsheet-operations/
keywords: "Aspose Cells Cloud, API Excel, opérations sur feuilles de calcul, ajustement automatique, traitement par lots, protection de fichiers, conversion, import/export, traitement de texte"
description: "Découvrez comment effectuer des opérations sur feuilles de calcul telles que l’ajustement automatique, la conversion par lots, la protection, la fusion et la recherche/remplacement à l’aide de l’API REST Aspose.Cells Cloud. Inclut des notes d’utilisation concises et des exemples de code."
weight: 100
ArticleTitle: "Opérations sur feuilles de calcul – Guide de l’API Aspose.Cells Cloud"
---

Les opérations sur feuilles de calcul constituent un guide concis des actions les plus courantes que vous pouvez effectuer sur des classeurs Excel à l’aide de **Aspose.Cells Cloud** (v3.0). Que vous ayez besoin d’ajuster automatiquement la largeur des colonnes, de traiter des fichiers par lots, de protéger des feuilles de calcul ou de manipuler du texte, l’API REST propose des points de terminaison dédiés fonctionnant avec des langages tels que Python, C# et Java. La liste ci-dessous renvoie vers la documentation détaillée de chaque opération et inclut une brève note d’utilisation pour vous aider à démarrer rapidement.

**Prérequis** : Pour appeler ces points de terminaison, vous devez disposer d'une clé API valide Aspose.Cells Cloud et inclure l’en-tête `Authorization` (`Bearer <jeton-d’accès>`). Les exemples supposent l’utilisation de la version v3.0 de l’API.

- **[Options du mode d’ajustement automatique](/cells/auto-fitter-options/)** – Ajuste automatiquement la largeur des colonnes et la hauteur des lignes. `POST /cells/{fichier}/worksheets/{feuille}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MonClasseur.xlsx/worksheets/Feuil1/autoFitColumns
  Authorization: Bearer {jeton-d’accès}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[Traitement par lots de fichiers Excel : conversion, verrouillage, protection, division et déverrouillage](/cells/batch/)** – Effectue des actions en masse (conversion, verrouillage, protection, division, déverrouillage) sur jusqu’à 100 fichiers par demande. `POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {jeton-d’accès}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Livre1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Livre2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[Compression et réparation de fichiers Excel](/cells/compress-and-repair-excel-files/)** – Réduit la taille des fichiers et corrige les problèmes structurels. `POST /cells/{fichier}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {jeton-d’accès}
  ```
- **[Conversion d’un fichier Excel vers un autre format ou enregistrement sous un autre format](/cells/conversion-and-save-as/)** – Convertit Excel en PDF, CSV, HTML, etc., ou modifie le format de sortie. `GET /cells/{fichier}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {jeton-d’accès}
  ```
- **[Options de conversion de classeur](/cells/convert-workbook-options/)** – Affine les paramètres de conversion tels que la taille de page, les options de rendu et la protection par mot de passe. `POST /cells/{fichier}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {jeton-d’accès}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[Création de fichiers Excel ou génération de rapports Excel](/cells/creating-files-and-reports/)** – Génère de nouveaux classeurs à partir de zéro ou à partir de modèles. `PUT /cells/{nouveauFichier}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NouveauRapport.xlsx
  Authorization: Bearer {jeton-d’accès}
  Content-Type: application/json

  {
    "templateFile": "Modele.xlsx",
    "dataSource": { "name": "Ventes T1", "value": 12345 }
  }
  ```
- **[Importation de données dans des fichiers Excel et exportation de données à partir de fichiers Excel](/cells/data-import-and-export/)** – Charge des données à partir de fichiers CSV, JSON ou bases de données, et exporte des données de feuille de calcul. `POST /cells/{fichier}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {jeton-d’accès}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[Chiffrement, déchiffrement et signature numérique de fichiers Excel](/cells/protect/)** – Applique une protection par mot de passe, un chiffrement ou des signatures numériques. `POST /cells/{fichier}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {jeton-d’accès}
  Content-Type: application/json

  {
    "password": "MotDePasseFort!23",
    "encryptionType": "Standard"
  }
  ```
- **[Informations sur le fichier](/cells/file-info/)** – Récupère des métadonnées telles que la taille, le format et la date de création. `GET /cells/{fichier}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {jeton-d’accès}
  ```
- **[Fusion et division de fichiers Excel](/cells/merge-and-split/)** – Combine plusieurs classeurs en un seul ou divise un classeur en fichiers distincts. `POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {jeton-d’accès}
  Content-Type: application/json

  {
    "files": ["T1.xlsx", "T2.xlsx"],
    "outputFile": "AnneeComplete.xlsx"
  }
  ```
- **[Recherche et remplacement de contenu textuel dans des fichiers Excel](/cells/search-and-replace/)** – Recherche et remplace des chaînes de caractères dans les feuilles de calcul. `POST /cells/{fichier}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {jeton-d’accès}
  Content-Type: application/json

  {
    "text": "Brouillon",
    "newText": "Final",
    "options": { "matchCase": false }
  }
  ```
- **[Traitement de texte dans Excel : ajout de texte, suppression de caractères, découpage de texte, modification de la casse des mots, etc.](/cells/text-processing/)** – Effectue des manipulations avancées sur les valeurs des cellules. `POST /cells/{fichier}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {jeton-d’accès}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[Insertion de filigranes ou définition d’arrière-plans dans des fichiers Excel](/cells/watermark-and-background/)** – Ajoute des filigranes image ou texte et définit l’arrière-plan des feuilles de calcul. `POST /cells/{fichier}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {jeton-d’accès}
  Content-Type: application/json

  {
    "type": "text",
    "text": "Confidentiel",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[Travail avec des fichiers Excel : calcul de formules, ajustement automatique, effacement d’objets, etc.](/cells/workbook/)** – Exécute des tâches courantes sur les classeurs telles que le calcul des formules, l’effacement d’objets et l’ajustement automatique. `POST /cells/{fichier}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {jeton-d’accès}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```