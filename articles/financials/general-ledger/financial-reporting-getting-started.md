---
title: Mali raporlama
description: "Bu konu, Microsoft Dynamics 365 for Finance and Operations içerisinden mali raporlara nereden erişileceğini ve finansal raporlama yeteneklerinin nasıl kullanılacağını açıklar. Sağlanan varsayılan mali raporların bir açıklamasını da içerir."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 83648a93f367510d7b04bbd04a9f37689ecfaa59
ms.openlocfilehash: 613fcf941576b9fb05f5c059699e4cc9c4cabe3e
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="financial-reporting"></a>Mali raporlama

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 for Finance and Operations içerisinden mali raporlara nereden erişileceğini ve finansal raporlama yeteneklerinin nasıl kullanılacağını açıklar. Sağlanan varsayılan mali raporların bir açıklamasını da içerir.

<a name="accessing-financial-reporting"></a>Mali raporlamaya erişmek
-----------------------------

**Finansal raporlama** menüsünü Finance and Operations'ta aşağıdaki yerlerde bulabilirsiniz:

-   **Genel muhasebe** &gt; **Sorgulamalar ve raporlar**
-   **Bütçeleme** &gt; **Sorgular ve raporlar** &gt; **Temel bütçeleme**
-   **Bütçeleme** &gt; **Sorgular ve raporlar** &gt; **Bütçe planlama**
-   **Bütçeleme** &gt; **Sorgular ve raporlar** &gt; **Bütçe denetimi**
-   Konsolidasyonlar

Bir tüzel kişilik için finansal raporlar oluşturmak ve üretmek için, bu tüzel kişilik için aşağıdaki bilgileri ayarlamanız gerekir:

-   Mali takvim
-   Genel muhasebe
-   Hesap planı
-   Para Birimi

Finansal raporlama işlevleri uygun ayrıcalıklara sahip ve güvenlik rolleri aracılığıyla görevler atanmış kullanıcılar için kullanılabilirdir. Aşağıdaki bölümlerde bu ayrıcalıklar ve görevler, ilişkili rollerle birlikte listelenmiştir.

### <a name="duties"></a>Görev

| Görev etiketi                            | Açıklama                                                             | AOT adı                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Mali raporlama güvenliğini sağla | Mali raporlama güvenliğini sağla ve yönetici görevlerini gerçekleştir. | MaliRaporlarGüvenlikSağlama |
| Mali raporları koru            | Mali raporları tasarla ve koru.                                  | MaliRaporlarıKoru         |
| Mali raporlar oluştur            | Mali raporları oluştur ve yenile.                                 | MaliRaporlarOluştur         |
| Mali performansı gözden geçir          | Mali performansı gözden geçir ve çözümle.                               | MaliRaporlarPerformansGözdenGeçirme       |

### <a name="privileges"></a>Ayrıcalıklar

| Ayrıcalık etiketi                       | Açıklama                                                             | AOT adı                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Mali raporlama güvenliğini sağla | Mali raporlama güvenliğini sağla ve yönetici görevlerini gerçekleştir. | MaliRaporlarGüvenlikSağlama |
| Mali raporları koru            | Mali raporları tasarla ve koru.                                  | MaliRaporlarRaporlarıKoru  |
| Mali raporlar oluştur            | Mali raporları oluştur ve yenile.                                 | MaliRaporlarRaporlarOluştur  |
| Mali raporları görüntüle                | Mali raporları görüntüle.                                                 | MaliRraporlarıGörüntüle             |

### <a name="roles"></a>Roller

| Ayrıcalık etiketi                       | Görev                                  | Roller                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Mali raporlama güvenliğini sağla | Mali raporlama güvenliğini sağla | Güvenlik yöneticisi                                                          |
| Mali raporları koru            | Mali raporları koru            | Muhasebe Yöneticisi, Muhasebe Gözetmeni, Mali Denetleyici, Bütçe Yöneticisi |
| Mali raporlar oluştur            | Mali raporlar oluştur            | CEO, CFO, Muhasebeci                                                            |
| Mali raporları görüntüle                | Mali performansı gözden geçir          | Hiçbiri atanmadı                                                                   |

Bir kullanıcı eklendikten veya bir rol değiştikten sonra, kullanıcının birkaç dakika içinde mali raporlamaya erişebilmesi gerekir. **Not:** sysadmin rolünü finansal raporlamada tüm rollere eklenir.

## <a name="default-reports"></a>Varsayılan raporlar
Finansal raporlama 22 varsayılan mali rapor sağlar. Her rapor, Finance and Operations uygulamasında varsayılan ana hesap kategorilerini kullanır. Bu raporları olduğu gibi veya gerekli finansal raporlama için bir başlangıç noktası olarak kullanabilirsiniz. Gelir tablosu ve Bilanço gibi geleneksel mali tablolara ek olarak, bu varsayılan raporlar da oluşturabileceğiniz farklı mali rapor türlerini gösteren varsayılan raporlar içerir. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Varsayılan rapor                                                                                         | Açıklama                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 Aylık Geri Alınan Tek Sütun Gelir Tablosu – Varsayılan | Bir kuruluşun son 12 ay içindeki karlılığını tek bir sütun olarak görüntüleyin.                                                                                                                                                                                                                                      |
| 12 aylık Eğilim Gelir Tablosu – Varsayılan                 | Bir kuruluşun her 12 ay için karlılığını görüntüleyin. Bu 12 ay birden fazla mali yıla yayılabilir.                                                                                                                                                                                             |
| Gerçek ile Bütçe karşılaştırması – Varsayılan                                | Orijinal bütçe için tüm hesapların bakiye bilgilerini görüntüleyin ve gözden geçirilmiş bütçeyi fark içeren fiili değerlerle karşılaştırın.                                                                                                                                                                          |
| Denetim Ayrıntıları – Varsayılan                                  | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, borç ve alacak bakiyelerini raporlama para biriminde ve yerel para biriminde, kullanıcı kimliği, veriyi değiştiren kullanıcı, son değiştirilme tarihi ve günlük kimliği gibi ek hareket bilgileriyle birlikte gösterir. |
| Bakiye Listesi – Varsayılan                                   | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, açılış ve kapanış bakiyelerini ve geçerli dönem ve yıl başından bugüne borç ve alacak bakiyelerini, fiş gibi ek hareket bilgileriyle birlikte gösterir.                                                                    |
| Bakiye – Varsayılan                                   | Kuruluşun o yıl için mali pozisyonunu görüntüleyin.                                                                                                                                                                                                                                                             |
| Bilanço ve Gelir Beyanı Yan Yana - Varsayılan | Organizasyonun mali pozisyonunu ve karlılığını yıl için yan yana görüntüleyin.                                                                                                                                                                                                                              |
| Nakit Akışı – Varsayılan                                       | Kuruluşa giden ve gelen nakit hakkında bir anlayış kazan.                                                                                                                                                                                                                                   |
| Ayrıntılı JE ve TB Gözden Geçirme – Varsayılan                      | Tüm hesaplar için açılış bakiyesini ve etkinlik bilgilerini görüntüle.                                                                                                                                                                                                                                                      |
| Ayrıntılı Mizan - Varsayılan                         | Borç ve alacak bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve hareket tarihi, fiş ve günlük açıklamasıyla birlikte bu bakiyelerin net değerini görüntüleyin.                                                                                                                                  |
| Giderler Üç Yıl Üç Aylık Eğilim – Varsayılan             | Önceki üç yıl üzerinden geçen 12 çeyreğin giderleri hakkında anlayış kazanın.                                                                                                                                                                                                                                   |
| Mali Sekmeler JE ve TB Gözden Geçirme – Varsayılan            | Kıymet, sorumluluk, sahibinin öz varlığı, gelir, gider, kazanç veya kayıp mali sekmeleri için yazıları için bakiye ve etkinliklere genel bakış konusunda bakın.                                                                                                                                                                           |
| Gelir Beyanı – Varsayılan                                | Geçerli dönem ve yıl başından bugüne kuruluşun karlılığını görüntüleyin.                                                                                                                                                                                                                                   |
| Genel Muhasebe Hareket Listesi – Varsayılan                        | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, hareket tarihi, günlük numarası, fiş, deftere nakil türü ve izleme numarası gibi ek hareket bilgileriyle birlikte borç ve alacak bakiyelerini gösterir.                                                                            |
| Oranları– Varsayılan                                          | Kuruluşun o yıl için ödeme gücü, karlılık ve verimlilik oranlarını görüntüleyin.                                                                                                                                                                                                                           |
| Geri alınan 12 Aylık Giderler – Varsayılan                       | Son 12 ayın her biri için harcamaları hakkında bir anlayış kazanın. Bu 12 ay birden fazla mali yıla yayılabilir.                                                                                                                                                                                                       |
| Geri Alınan Üç Aylık Gelir Tablosu – Varsayılan               | Geçen yıl ve yıl başından bugüne kadar bir kuruluşun üç aylık karlılığını görüntüleyin.                                                                                                                                                                                                                   |
| Yan Yana Bilanço – Varsayılan                      | Kuruluşun o yıl için mali pozisyonunu görüntüleyin. Bu raporda, kıymetler ve pasif ve hissedar öz varlığı yan yana gösterilir.                                                                                                                                                                                |
| Özet Mizan – Varsayılan                          | Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve net farklarıyla birlikte borç ve alacak bakiyelerini görüntüleyin.                                                                                                                                                                  |
| Özet Mizan Yıl Yıl – Varsayılan           | Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve bu yıl ve geçen yıl için net farklarıyla birlikte, borç ve alacak bakiyelerini görüntüleyin.                                                                                                                           |
| Haftalık Satış ve İndirimler - Varsayılan                     | Bir ayın her haftası için satış ve indirimler hakkında anlayış kazanın. Bu rapor dört haftalık toplamı içerir.                                                                                                                                                                                                              |
| Bütçe Fonları Kullanılabilir - Varsayılan                         | Tüm kullanılabilir hesaplar için gözden geçirilmiş bütçenin, fiili harcamaların, bütçe ayırmalarının ve bütçe fonlarının ayrıntılı bir karşılaştırmasını görüntüleyin.                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Mali raporları açmak
**Finansal Raporlama** menüsüne tıklattığınızda, şirketin varsayılan finansal raporlarının listesi gösterilir. Sonra bir raporu açabilir veya değiştirebilirsiniz. Varsayılan raporlardan birini açmak için, rapor adını seçin. Bir rapor ilk defa açıldığında, otomatik olarak önceki ay için oluşturulur. Örneğin, bir raporu ilk kez Ağustos 2016'de açarsanız, rapor 31 Temmuz 2016 tarihi için oluşturulur. Rapor açıldıktan sonra, belirli veri parçalarında ayrıntıya inerek ve rapor seçeneklerini değiştirerek keşfetmeye başlayabilirsiniz.

## <a name="creating-and-modifying-financial-reports"></a>Mali raporları oluşturma ve değiştirme
Finansal raporlar listesinden yeni bir rapor oluşturabilir veya varolan bir raporu değiştirebilirsiniz. Uygun izinlere sahipseniz, Eylem Bölmesinde **Yeni** üzerine tıklayarak yeni bir mali rapor oluşturabilirsiniz. Bir rapor tasarımcısı programı cihazınıza indirilir. Rapor tasarımcısı çalıştıktan sonra, yeni raporu oluşturabilirsiniz. Yeni raporu kaydettikten sonra, mali raporlar listesinde görünür. Liste yalnızca Finance and Operations'da kullanmakta olduğunuz şirket için oluşturulan raporları gösterir. Mali raporları Finance and Operations içerisinde oluşturma ve değiştirme süreci hakkında daha fazla bilgi için, bkz. Dynamics mali raporlama blogundaki şu [blog postaları](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/). **Not:** Rapor tasarımcısı istemcisini indirdiğiniz bilgisayarın Microsoft .Net Framework'ün 4.6.2 sürümüne sahip olması gerekir. Microsoft .NET Framework'ün bu sürümünü [buradan](https://www.microsoft.com/en-us/download/details.aspx?id=53345) indirebilir ve kurabilirsiniz. Chrome kullanıyorsanız, rapor tasarımcısı istemcisini indirebilmek için ClickOnce eklentisini yüklemeniz gerekir. İncognito modunda kullanıyorsanız, ClickOnce eklentisinin incognito modu için etkin olduğundan emin olun. Ayrıca mali rapor listesinde görünen bir raporu değiştirebilirsiniz. Rapor adı etrafındaki alan seçildiğinde, Eylem Bölmesinden **Düzenleme** tıklatın. Rapor tasarımcısı programı başlar.

## <a name="additional-resources"></a>Ek kaynaklar
- [Mali raporları görüntüleme](view-financial-reports.md)
- [Dynamics Mali Raporlama blogu](http://blogs.msdn.com/b/dynamics_financial_reporting/)




