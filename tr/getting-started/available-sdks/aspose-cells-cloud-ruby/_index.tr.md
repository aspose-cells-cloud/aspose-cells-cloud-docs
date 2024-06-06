---
title: Aspose.Cells Rub için Bulut SDK'sı
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/available-sdks/aspose-cells-cloud-ruby/
description: Aspose.Cells Bulut, oluşturma, dönüştürme, birleştirme, bölme, koruma, iç nesne işlemleri vb. için Excel'i destekler
weight: 30
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Ruby
---
 SDK açık kaynaklıdır ve MIT Lisansı kapsamında lisanslanmıştır. Aspose.Cells Cloud için Ruby kütüphanesi kaynak koduna erişebilirsiniz.[Burada](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby).

# **Ruby için Aspose.Cells Bulut SDK'sı nasıl kullanılır?**

Ruby için Aspose.Cells Cloud SDK, geliştiricilerin Ruby programlama dilini kullanarak Microsoft Excel dosyalarını değiştirmesine ve işlemesine olanak tanıyan güçlü bir kitaplıktır. Bu SDK ile, yerel makinenize ek yazılım veya bağımlılık yüklemeden, bulutta Excel belge oluşturabilir, düzenleyebilir ve dönüştürebilirsiniz.

Bu makalede, yeni bir Excel çalışma kitabı oluşturmak, hücrelere veri eklemek ve değiştirilen çalışma kitabını buluta kaydetmek gibi bazı genel görevleri gerçekleştirmek için Ruby için Aspose.Cells Bulut SDK'sının nasıl kullanılacağını keşfedeceğiz.

## Başlarken

 Go için Aspose.Cells Cloud SDK'yı kullanmaya başlamadan önce geliştirme ortamınızı kurmanız ve gerekli bağımlılıkları yüklemeniz gerekir. Bakınız[makale](https://docs.aspose.cloud/cells/quickstart/) Müşteri kimliğinizi ve müşteri sırrınızı almak için Aspose web sitesini ziyaret edin.

## Aspose.Cells Cloud için Ruby paketi nasıl kurulur

Aşağıdaki komutla Ruby için Aspose.Cells Cloud SDK'yı yükleyebilirsiniz:

```bash

    gem install aspose_cells_cloud
  
 ```

## Xlsx'i PDF'e dönüştürmek için Ruby paketi nasıl kullanılır?

- Aspose.Cells Bulut Kitaplığını İçe Aktar
 Gerekli paketi Aspose.Cells Cloud Python SDK'sından projenize aktararak başlayın.
- API İstemcisini Kimlik Bilgileriyle Yapılandırma
 API istemcinizin kimliğini benzersiz istemci kimliğiniz ve istemci sırrınızla doğrulayın.
- Dönüşüm Parametrelerini Hazırlayın
 Kaynak dosya adı, istenilen çıktı formatı ve depolama klasörü yolu dahil, dönüştürme görevi için parametreleri tanımlayın.
- Çalışma Kitabı Dönüşümünü Yürüt
 PostConvertWorkbook yöntemini kullanarak dönüştürme işlemini çağırın ve yanıtı işleyin.

```Ruby
require 'openssl'
require 'bundler'
require 'aspose_cells_cloud'

@instance = AsposeCellsCloud::CellsApi.new(ENV['CellsCloudClientId'], ENV['CellsCloudClientSecret'],'v3.0',ENV['CellsCloudApiBaseUrl'])

remote_folder = 'TestData/In'

local_name = 'Book1.xlsx'
remote_name = 'Book1.xlsx'

format = "csv"

    
mapFiles = { }   
mapFiles = { }               
mapFiles[local_name] = ::File.open(File.expand_path("TestData/"+local_name),"r")  
 
uploadrequest = AsposeCellsCloud::UploadFileRequest.new( { :UploadFiles=>mapFiles,:path=>remote_folder })
@instance.upload_file(uploadrequest)
mapFiles[local_name]= ::File.open(File.expand_path("TestData/"+local_name),"r")
request =   AsposeCellsCloud::PutConvertWorkbookRequest.new(:File=>mapFiles,:format=>format);
@instance.put_convert_workbook(request);


```
