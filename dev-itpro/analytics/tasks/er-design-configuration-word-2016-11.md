--- 
title: "Elektronik raporlama (ER) için Microsoft Word biçiminde rapor oluşturmak üzere bir yapılandırma tasarlama"
description: "Aşağıdaki adımlar, bir Sistem yöneticisi veya Elektronik raporlama geliştirici rolündeki bir kullanıcının, Microsoft Word dosyaları şeklinde raporlar oluşturmak için bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5adf1d6e6314ac7ea4084cfb3fcde8b83168c7ae
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-configuration-for-generating-reports-in-microsoft-word-format-for-electronic-reporting-er"></a>Elektronik raporlama (ER) için Microsoft Word biçiminde rapor oluşturmak üzere bir yapılandırma tasarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar, bir Sistem yöneticisi veya Elektronik raporlama geliştirici rolündeki bir kullanıcının, Microsoft Word dosyaları şeklinde raporlar oluşturmak için bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar. Bu adımlar GBSI şirketinde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "OPENXML biçiminde raporlar oluşturmak için bir ER yapılandırması oluşturma" görev kılavuzundaki adımları tamamlamanız gerekir. Aşağıdaki şablonları aynı rapor için önceden indirmeli ve yerel olarak kaydetmelisiniz:

http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReport.docx

http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReportBounded.docx

Bu yordam, Microsoft Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="select-the-existing-er-report-configuration"></a>Mevcut ER rapor yapılandırmasını seçme
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Yapılandırma sağlayıcısı olan "Litware, Inc." şirketinin etkin olarak seçildiğinden emin olun. Etkin olarak işaretlenir.  
2. Raporlama konfigürasyonları'na tıklayın.
    * Rapor çıktısını OPENXML biçiminde oluşturmak için özgün olarak tasarlanmış olan mevcut ER yapılandırmasını yeniden kullanacağız.  
3. Ağaçta, 'Ödeme modeli' öğesini genişletin.
4. Ağaçta, 'Ödeme modeli\Örnek çalışma sayfası raporu' seçin.
5. Tasarımcı'yı tıklatın.

## <a name="replace-the-excel-template-with-the-word-template"></a>Excel şablonunu Word şablonu ile değiştirme
    * Şu anda, Excel belgesi OPENXML biçiminde çıktı üretmek için şablon olarak kullanılmaktadır. Raporun şablonunu Word biçiminde içeri aktaracağız.  
1. Ekler'e tıklayın.
    * Mevcut Excel şablonunu daha önce indirdiğiniz Word şablonuyla (SampleVendPaymDocReport.docx) değiştirin. Bu şablonun yalnızca ER çıktısı olarak oluşturmak istediğimiz belgenin düzenini içerdiğini unutmayın.  
2. Sil'i tıklatın.
3. Evet'i tıklatın.
4. Yeni'ye tıklayın.
5. Dosya'ya tıklayın.
6. Gözat düğmesine tıklayın. Daha önceden indirdiğiniz SampleVendPaymDocReport.docx dosyasına gidin ve dosyayı seçin. Tamam'a tıklayın.
    * Önceki adımda indirdiğiniz şablonu seçin.  
7. Şablon alanına bir değer girin veya seçin.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Özel bir XML bölümü ekleyerek Word şablonunu genişletme
1. Kaydet'e tıklayın.
    * Kaydet eylemi, yapılandırma değişikliklerini depolamanın yanı sıra ekli Word şablonunu da güncelleştirir. Tasarlanan biçimin yapısı, ekli Word belgesine "Rapor" adında yeni bir özel XML bölümü olarak verilir. Ekli Word şablonunun yalnızca ER çıktısı olarak oluşturmak istediğimiz belgenin düzeninin yanı sıra ER'nin çalışma zamanında bu şablonu dolduracağı verilerin yapısını da içerdiğine dikkat edin.  
2. Ekler'e tıklayın.
    * Şimdi de "Rapor" adlı özel XML bölümünün öğelerini Word belgesi bölümlerine bağlamanız gerekiyor.  
    * Özel XML bölümlerinin öğeleriyle bağlı içerik denetimleri içeren formlar olarak tasarlanabilen Word belgeleri kullanıyorsanız bir sonraki alt görevin tüm adımlarını yürüterek bu tür bir belge oluşturun. Daha fazla bilgi için şu bağlantıya bakın: https://support.office.com/tr-tr/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=tr-TR&rs=tr-TR&ad=TR. Aksi durumda, bir sonraki alt görevdeki tüm adımları atlayın.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Veri ilişkilendirmeleri yapmak için özel XML bölümlü Word edinme
    * Bu belgeyi Word'de açın ve aşağıdakileri yapın:  - Word Geliştiricisi sekmesini açın (henüz etkin değilse şeridi özelleştirin).  - XML eşleme bölmesini seçin.  - Aramada "Rapor" özel XML bölümünü seçin.  - Seçili özel XML bölümü öğelerinin ve Word belgesinin içerik denetimlerinin eşlemesini yapın.  - Güncelleştirilmiş Word belgesini bir yerel sürücüye kaydedin.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>İçerik denetimlerine bağlanmış özel XML bölümlü Word şablonunu yükleme
1. Sil'i tıklatın.
2. Evet'i tıklatın.
    * Yeni bir şablon ekleyin. Bir önceki alt görevdeki adımları tamamladıysanız hazırladığınız ve yerel olarak kaydettiğiniz Word belgesini seçin. Aksi durumda, daha önce indirdiğiniz MS Word şablonunu (SampleVendPaymDocReportBounded.docx) seçin.  
3. Yeni'ye tıklayın.
4. Dosya'ya tıklayın.
5. Gözat düğmesine tıklayın. Daha önceden indirdiğiniz SampleVendPaymDocReportBounded.docx dosyasına gidin ve dosyayı seçin. Tamam'ı tıklatın.
6. Şablon alanında, bir önceki adımda indirdiğiniz belgeyi seçin.
7. Kaydet'e tıklayın.
8. Sayfayı kapatın.

## <a name="execute-the-format-to-create-word-output"></a>Word çıktısı oluşturmak için biçimi yürütme
1. Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.
2. Kullanıcı parametreleri'ne tıklayın.
3. Çalıştırma ayarları alanında Evet'i seçin.
4. Tamam'a tıklayın.
5. Düzenle öğesine tıklayın.
6. Taslak Çalıştır alanında Evet'e tıklayın.
7. Kaydet'e tıklayın.
8. Sayfayı kapatın.
9. Sayfayı kapatın.
10. Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.
11. Satırlar seçeneğine tıklayın.
12. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.
13. Ödeme durumu'nu tıklatın.
14. Hiçbiri'ne tıklayın.
15. Ödemeler oluştur'u tıklatın.
16. Tamam'a tıklayın.
17. Tamam'a tıklayın.
    * Oluşturulan çıktıyı analiz edin. Oluşturulan çıktının Word biçiminde sunulduğuna ve işlenen ödemelerin ayrıntılarını içerdiğine dikkat edin.  


