﻿---
title: Option de conversion du classeur
second_title: Aspose.Cells Cloud Documen
linktitle: Option de conversion du classeur
type: docs
url: /fr/convert-workbook-options/
keywords: ConvertWorkbookOptions
description: Aspose.Cells Cloud REST API prend en charge l'extraction de fichiers Excel vers différents formats. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 79
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Options de conversion de classeur
---
# Propriétés de ConvertWorkbookOptions

Nom | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Source de données** | **Objet** | Source du fichier de données : CloudFileSystem, RequestFiles, HttpUri. |
**[FileInfo](/cells/file-info/)** | **Objet** | Description des informations sur le fichier. Comprend le nom du fichier, la taille du fichier et le contenu du fichier (chaîne base64). |
**[Mise en page](/cells/page-setup/)** | **Objet** | Propriétés de configuration de la page. |
**Options de sauvegarde** | **Objet** Options d'enregistrement : DbfSaveOptions, DifSaveOptions, DocxSaveOptions, HtmlSaveOptions, XlsSaveOptions, XlsxSaveOptions, XpsSaveOptions, PngSaveOptions, JpgSaveOptions, GifSaveOptions, EmfSaveOptions, BmpSaveOptions, MdSaveOptions, NumbersSaveOptions, WmfSaveOptions, SvgSaveOptions, TxtSaveOptions, TifSaveOptions, XlsbSaveOptions |
**ConvertirFormat** | **chaîne** | Le format de fichier : csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg, etc. |
**CheckExcelRestriction** | **booléen** | Obtient et définit le type de texte enveloppé à ajustement automatique. |

## **Propriétés de fileSource**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Type de source de fichier|Chaîne|vrai| FAUX||Une propriété nommée FileSourceType de type FileSourceType qui peut être consultée et modifiée. (CloudFileSystem/RequestFiles/HttpUri)|
|Chemin du fichier|Chaîne|vrai| FAUX||Le chemin de position du fichier.|

## **Propriétés de DbfSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Exporter comme chaîne|Booléen|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés DifSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés de DocxSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Police par défaut|Chaîne|vrai| FAUX|||
|Vérifier la police par défaut du classeur|Booléen|vrai| FAUX|||
|Vérifier la compatibilité des polices|Booléen|vrai| FAUX|||
|Granularité de IsFontSubstitutionChar|Booléen|vrai| FAUX|||
|Une page par feuille|Booléen|vrai| FAUX|||
|Toutes les colonnes sur une page par feuille|Booléen|vrai| FAUX|||
|IgnorerErreur|Booléen|vrai| FAUX|||
|Sortie d'une page vierge lorsque rien à imprimer|Booléen|vrai| FAUX|||
|Index des pages|Entier|vrai| FAUX|||
|Nombre de pages|Entier|vrai| FAUX|||
|Type de page d'impression|Chaîne|vrai| FAUX|||
|Type de ligne de grille|Chaîne|vrai| FAUX|||
|TexteCrossType|Chaîne|vrai| FAUX|||
|Langue par défaut|Chaîne|vrai| FAUX|||
|EmfRenderSetting|Chaîne|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés HtmlSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Exporter les en-têtes de page|Booléen|vrai| FAUX|||
|Exporter les pieds de page|Booléen|vrai| FAUX|||
|Exporter les en-têtes de lignes et de colonnes|Booléen|vrai| FAUX|||
|Afficher toutes les feuilles|Booléen|vrai| FAUX|||
|Options d'image|Classe|vrai| FAUX|||
|Enregistrer sous un seul fichier|Booléen|vrai| FAUX|||
|Exporter la feuille de travail masquée|Booléen|vrai| FAUX|||
|Exporter les lignes de grille|Booléen|vrai| FAUX|||
|Préférence de présentation|Booléen|vrai| FAUX|||
|Préfixe CellCss|Chaîne|vrai| FAUX|||
|TableCssId|Chaîne|vrai| FAUX|||
|IsFullPathLink|Booléen|vrai| FAUX|||
|Exporter la feuille de calcul CSS séparément|Booléen|vrai| FAUX|||
|Exporter un style de bordure similaire|Booléen|vrai| FAUX|||
|FusionnerVideTdForcely|Booléen|vrai| FAUX|||
|Exporter les coordonnées de la cellule|Booléen|vrai| FAUX|||
|Exporter des en-têtes supplémentaires|Booléen|vrai| FAUX|||
|Exporter les en-têtes|Booléen|vrai| FAUX|||
|ExportFormula|Booléen|vrai| FAUX|||
|Ajouter un texte d'info-bulle|Booléen|vrai| FAUX|||
|Exporter des données de ligne fictives|Booléen|vrai| FAUX|||
|Exclure les styles inutilisés|Booléen|vrai| FAUX|||
|ExportDocumentProperties|Booléen|vrai| FAUX|||
|ExportWorksheetProperties|Booléen|vrai| FAUX|||
|Exporter les propriétés du classeur|Booléen|vrai| FAUX|||
|Exporter les scripts et les propriétés du cadre|Booléen|vrai| FAUX|||
|Répertoire des fichiers attachés|Chaîne|vrai| FAUX|||
|Préfixe d'URL des fichiers attachés|Chaîne|vrai| FAUX|||
|Codage|Chaîne|vrai| FAUX|||
|ExporterActiveWorksheetOnly|Booléen|vrai| FAUX|||
|ExportChartImageFormat|Chaîne|vrai| FAUX|||
|Exporter les images en base 64|Booléen|vrai| FAUX|||
|Type d'affichage caché|Chaîne|vrai| FAUX|||
|HiddenRowDisplayType|Chaîne|vrai| FAUX|||
|HtmlCrossStringType|Chaîne|vrai| FAUX|||
|IsExpImageToTempDir|Booléen|vrai| FAUX|||
|Titre de la page|Chaîne|vrai| FAUX|||
|AnalyserHtmlTagInCell|Booléen|vrai| FAUX|||
|Attribut de nom de cellule|Chaîne|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés ImageSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Type d'image de graphique|Chaîne|vrai| FAUX|||
|Nom de l'image intégrée dans SVG|Chaîne|vrai| FAUX|||
|Résolution horizontale|Entier|vrai| FAUX|||
|Format d'image|Chaîne|vrai| FAUX|||
|IsCellAutoFit|Booléen|vrai| FAUX|||
|Une page par feuille|Booléen|vrai| FAUX|||
|Zone Unique|Booléen|vrai| FAUX|||
|Impression de la page|Chaîne|vrai| FAUX|||
|ImprimerAvecDialogueD'état|Booléen|vrai| FAUX|||
|Qualité|Entier|vrai| FAUX|||
|Compression Tiff|Chaîne|vrai| FAUX|||
|Résolution verticale|Entier|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés JsonSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Zone d'exportation|Classe|vrai| FAUX|||
|HasHeaderRow|Booléen|vrai| FAUX|||
|Exporter comme chaîne|Booléen|vrai| FAUX|||
|Retrait|Chaîne|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés MarkdownSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Codage|Chaîne|vrai| FAUX|||
|FormatStratégie|Chaîne|vrai| FAUX|||
|Séparateur de ligne|Chaîne|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés OoxmlSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|ExporterCellName|Booléen|vrai| FAUX|||
|Mise à jourZoom|Booléen|vrai| FAUX|||
|ActiverZip64|Booléen|vrai| FAUX|||
|Intégrer OoxmlAsOleObject|Booléen|vrai| FAUX|||
|Type de compression|Chaîne|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés de PclSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|fontFullName|Chaîne|vrai| FAUX|||
|fontPclName|Chaîne|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés de PdfSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Afficher le titre du document|Booléen|vrai| FAUX|||
|Structure du document d'exportation|Booléen|vrai| FAUX|||
|EmfRenderSetting|Chaîne|vrai| FAUX|||
|Exportation de propriétés personnalisées|Chaîne|vrai| FAUX|||
|Type d'optimisation|Chaîne|vrai| FAUX|||
|Producteur|Chaîne|vrai| FAUX|||
|Compression PDF|Chaîne|vrai| FAUX|||
|Encodage des polices|Chaîne|vrai| FAUX|||
|Filigrane|Classe|vrai| FAUX|||
|CalculateFormula|Booléen|vrai| FAUX|||
|Vérifier la compatibilité des polices|Booléen|vrai| FAUX|||
|Conformité|Chaîne|vrai| FAUX|||
|Police par défaut|Chaîne|vrai| FAUX|||
|Une page par feuille|Booléen|vrai| FAUX|||
|Type de page d'impression|Chaîne|vrai| FAUX|||
|Options de sécurité|Classe|vrai| FAUX|||
|IPP souhaité|Entier|vrai| FAUX|||
|Qualité jpeg|Entier|vrai| FAUX|||
|Type d'image|Chaîne|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés de PptxSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Ignorer les lignes cachées|Booléen|vrai| FAUX|||
|Ajuster la taille de la police pour le type de ligne|Chaîne|vrai| FAUX|||
|ExportViewType|Chaîne|vrai| FAUX|||
|Police par défaut|Chaîne|vrai| FAUX|||
|Vérifier la police par défaut du classeur|Booléen|vrai| FAUX|||
|Vérifier la compatibilité des polices|Booléen|vrai| FAUX|||
|Granularité de IsFontSubstitutionChar|Booléen|vrai| FAUX|||
|Une page par feuille|Booléen|vrai| FAUX|||
|Toutes les colonnes sur une page par feuille|Booléen|vrai| FAUX|||
|IgnorerErreur|Booléen|vrai| FAUX|||
|Sortie d'une page vierge lorsque rien à imprimer|Booléen|vrai| FAUX|||
|Index des pages|Entier|vrai| FAUX|||
|Nombre de pages|Entier|vrai| FAUX|||
|Type de page d'impression|Chaîne|vrai| FAUX|||
|Type de ligne de grille|Chaîne|vrai| FAUX|||
|TexteCrossType|Chaîne|vrai| FAUX|||
|Langue par défaut|Chaîne|vrai| FAUX|||
|EmfRenderSetting|Chaîne|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés de SqlScriptSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Vérifier si la table existe|Booléen|vrai| FAUX|||
|ColumnTypeMap|Chaîne|vrai| FAUX|||
|Vérifier toutes les données pour le type de colonne|Booléen|vrai| FAUX|||
|Ajouter une ligne vide entre les lignes|Booléen|vrai| FAUX|||
|Séparateur|Chaîne|vrai| FAUX|||
|Type d'opérateur|Chaîne|vrai| FAUX|||
|Clé primaire|Entier|vrai| FAUX|||
|Créer une table|Booléen|vrai| FAUX|||
|Nom d'identification|Chaîne|vrai| FAUX|||
|ID de démarrage|Entier|vrai| FAUX|||
|Nom de la table|Chaîne|vrai| FAUX|||
|Exporter comme chaîne|Booléen|vrai| FAUX|||
|Zone d'exportation|Classe|vrai| FAUX|||
|HasHeaderRow|Booléen|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés SvgSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Index des feuilles|Entier|vrai| FAUX|||
|Type d'image de graphique|Chaîne|vrai| FAUX|||
|Nom de l'image intégrée dans SVG|Chaîne|vrai| FAUX|||
|Résolution horizontale|Entier|vrai| FAUX|||
|Format d'image|Chaîne|vrai| FAUX|||
|IsCellAutoFit|Booléen|vrai| FAUX|||
|Une page par feuille|Booléen|vrai| FAUX|||
|Zone Unique|Booléen|vrai| FAUX|||
|Impression de la page|Chaîne|vrai| FAUX|||
|ImprimerAvecDialogueD'état|Booléen|vrai| FAUX|||
|Qualité|Entier|vrai| FAUX|||
|Compression Tiff|Chaîne|vrai| FAUX|||
|Résolution verticale|Entier|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés TxtSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Type de citation|Chaîne|vrai| FAUX|||
|Séparateur|Chaîne|vrai| FAUX|||
|Séparateur de chaîne|Chaîne|vrai| FAUX|||
|Toujours cité|Booléen|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés XlsSaveOptions et XlsbSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Correspondance des couleurs|Booléen|vrai| FAUX|||
|Compatibilité Wps|Booléen|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés XmlSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Index des feuilles|Tableau|vrai| FAUX|||
|Zone d'exportation|Classe|vrai| FAUX|||
|HasHeaderRow|Booléen|vrai| FAUX|||
|Nom de la carte Xml|Chaîne|vrai| FAUX|||
|NomDeLaFeuilleCommeNomDeL'Élément|Booléen|vrai| FAUX|||
|Données comme attribut|Booléen|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||

## **Propriétés XpsSaveOptions**

| Nom de la propriété| Type de propriété| Nullable| Lecture seule| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
|Police par défaut|Chaîne|vrai| FAUX|||
|Vérifier la police par défaut du classeur|Booléen|vrai| FAUX|||
|Vérifier la compatibilité des polices|Booléen|vrai| FAUX|||
|Granularité de IsFontSubstitutionChar|Booléen|vrai| FAUX|||
|Une page par feuille|Booléen|vrai| FAUX|||
|Toutes les colonnes sur une page par feuille|Booléen|vrai| FAUX|||
|IgnorerErreur|Booléen|vrai| FAUX|||
|Sortie d'une page vierge lorsque rien à imprimer|Booléen|vrai| FAUX|||
|Index des pages|Entier|vrai| FAUX|||
|Nombre de pages|Entier|vrai| FAUX|||
|Type de page d'impression|Chaîne|vrai| FAUX|||
|Type de ligne de grille|Chaîne|vrai| FAUX|||
|TexteCrossType|Chaîne|vrai| FAUX|||
|Langue par défaut|Chaîne|vrai| FAUX|||
|EmfRenderSetting|Chaîne|vrai| FAUX|||
|Fusionner les zones|Booléen|vrai| FAUX|||
|Trier les noms externes|Booléen|vrai| FAUX|||
|Mise à jourSmartArt|Booléen|vrai| FAUX|||
|EnregistrerFormat|Chaîne|vrai| FAUX|||
|Dossier de fichiers en cache|Chaîne|vrai| FAUX|||
|ClearData|Booléen|vrai| FAUX|||
|Créer un répertoire|Booléen|vrai| FAUX|||
|Activer la compression HTTP|Booléen|vrai| FAUX|||
|Actualiser le cache du graphique|Booléen|vrai| FAUX|||
|Trier les noms|Booléen|vrai| FAUX|||
|Valider les zones fusionnées|Booléen|vrai| FAUX|||
|CheckExcelRestriction|Booléen|vrai| FAUX|||
|EncryptDocumentProperties|Booléen|vrai| FAUX|||
