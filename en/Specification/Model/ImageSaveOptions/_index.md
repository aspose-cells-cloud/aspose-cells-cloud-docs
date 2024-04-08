---
title: "ImageSaveOptions"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/imagesaveoptions/
description: "Represents options of saving image file."
weight: 50
---

## **imageSaveOptions**

Represents options of saving image file. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| ChartImageType | String | True |  False |  | Indicate the chart imagetype when converting. |  
| EmbededImageNameInSvg | String | True |  False |  | Indicate the filename of embeded image in svg. This should be full path with directory like "c:\\xpsEmbeded" |  
| HorizontalResolution | Integer | True |  False |  | Gets or sets the horizontal resolution for generated images, in dots per inch.                 Applies generating image method except Emf format images.               The default value is 96. |  
| ImageFormat | String | True |  False |  | Gets or sets the format of the generated images.  Don't apply the method that returns a Bitmap object.             The default value is ImageFormat.Bmp.  Don't apply the method that returns a Bitmap object. |  
| IsCellAutoFit | Boolean | True |  False |  | Indicates whether the width and height of the cells is automatically fitted by cell value. The default value is false. |  
| OnePagePerSheet | Boolean | True |  False |  | If OnePagePerSheet is true , all content of one sheet will output to only                one page in result. The paper size of pagesetup will be invalid, and the                other settings of pagesetup will still take effect. |  
| OnlyArea | Boolean | True |  False |  | If this property is true , onle Area will be output, and no scale will take effect. |  
| PrintingPage | String | True |  False |  | Indicates which pages will not be printed. |  
| PrintWithStatusDialog | Boolean | True |  False |  | If PrintWithStatusDialog = true , there will be a dialog that shows current print status.  else no such dialog will show. |  
| Quality | Integer | True |  False |  | Gets or sets a value determining the quality of the generated images to apply only when saving pages to the Jpeg format.            Has effect only when saving to JPEG.  The value must be between 0 and 100. The default value is 100. |  
| TiffCompression | String | True |  False |  | Gets or sets the type of compression to apply only when saving pages to the Tiff format.            Has effect only when saving to TIFF.  The default value is Lzw. |  
| VerticalResolution | Integer | True |  False |  | Gets or sets the vertical resolution for generated images, in dots per inch.            Applies generating image method except Emf format image.            The default value is 96. |  
| SaveFormat | String | True |  False |  |  |  
| CachedFileFolder | String | True |  False |  |  |  
| ClearData | Boolean | True |  False |  |  |  
| CreateDirectory | Boolean | True |  False |  |  |  
| EnableHTTPCompression | Boolean | True |  False |  |  |  
| RefreshChartCache | Boolean | True |  False |  |  |  
| SortNames | Boolean | True |  False |  |  |  
| ValidateMergedAreas | Boolean | True |  False |  |  |  

**Parent Name** : (SaveOptions)[saveoptions]

