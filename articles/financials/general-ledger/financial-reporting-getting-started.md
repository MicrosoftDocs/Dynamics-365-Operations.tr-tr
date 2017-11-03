---
title: Mali raporlama
description: "Bu konu, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition içerisinden mali raporlara nereden erişileceğini ve finansal raporlama yeteneklerinin nasıl kullanılacağını açıklar. Sağlanan varsayılan mali raporların bir açıklamasını da içerir."
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ed207bdc04041ec2f21cb1038451fc75b8d061a1
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="financial-reporting"></a>Mali raporlama

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition içerisinden mali raporlara nereden erişileceğini ve finansal raporlama yeteneklerinin nasıl kullanılacağını açıklar. Sağlanan varsayılan mali raporların bir açıklamasını da içerir.

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
Finansal raporlama 22 varsayılan mali rapor sağlar. Her rapor, Finance and Operations uygulamasında varsayılan ana hesap kategorilerini kullanır. Bu raporları olduğu gibi veya gerekli finansal raporlama için bir başlangıç noktası olarak kullanabilirsiniz. Gelir tablosu ve Bilanço gibi geleneksel mali tablolara ek olarak, bu varsayılan raporlar da oluşturabileceğiniz farklı mali rapor türlerini gösteren varsayılan raporlar içerir. Aşağıdaki tablolardaki her rapor, rapor hakkında bir Office Mix sunumuna bağlanır.

| Varsayılan rapor                                                                                         | Açıklama                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 Aylık Geri Alınan Tek Sütun Gelir Tablosu – Varsayılan](https://mix.office.com/watch/76kc7bm3wnt1) | Bir kuruluşun son 12 ay içindeki karlılığını tek bir sütun olarak görüntüleyin.                                                                                                                                                                                                                                      |
| [12 aylık Eğilim Gelir Tablosu – Varsayılan](https://mix.office.com/watch/12brmfge5p8r)                 | Bir kuruluşun her 12 ay için karlılığını görüntüleyin. Bu 12 ay birden fazla mali yıla yayılabilir.                                                                                                                                                                                             |
| [Gerçek ile Bütçe karşılaştırması – Varsayılan](https://mix.office.com/watch/fi439lkwr0no)                                | Orijinal bütçe için tüm hesapların bakiye bilgilerini görüntüleyin ve gözden geçirilmiş bütçeyi fark içeren fiili değerlerle karşılaştırın.                                                                                                                                                                          |
| [Denetim Ayrıntıları – Varsayılan](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, borç ve alacak bakiyelerini raporlama para biriminde ve yerel para biriminde, kullanıcı kimliği, veriyi değiştiren kullanıcı, son değiştirilme tarihi ve günlük kimliği gibi ek hareket bilgileriyle birlikte gösterir. |
| [Bakiye Listesi – Varsayılan](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, açılış ve kapanış bakiyelerini ve geçerli dönem ve yıl başından bugüne borç ve alacak bakiyelerini, fiş gibi ek hareket bilgileriyle birlikte gösterir.                                                                    |
| [Bakiye – Varsayılan](https://mix.office.com/watch/zkgq0u7visw9)                                   | Kuruluşun o yıl için mali pozisyonunu görüntüleyin.                                                                                                                                                                                                                                                             |
| [Bilanço ve Gelir Beyanı Yan Yana - Varsayılan](https://mix.office.com/watch/zkgq0u7visw9) | Organizasyonun mali pozisyonunu ve karlılığını yıl için yan yana görüntüleyin.                                                                                                                                                                                                                              |
| [Nakit Akışı – Varsayılan](https://mix.office.com/watch/jd3go9pz6390)                                       | Kuruluşa giden ve gelen nakit hakkında bir anlayış kazan.                                                                                                                                                                                                                                   |
| [Ayrıntılı JE ve TB Gözden Geçirme – Varsayılan](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Tüm hesaplar için açılış bakiyesini ve etkinlik bilgilerini görüntüle.                                                                                                                                                                                                                                                      |
| [Ayrıntılı Mizan - Varsayılan](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Borç ve alacak bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve hareket tarihi, fiş ve günlük açıklamasıyla birlikte bu bakiyelerin net değerini görüntüleyin.                                                                                                                                  |
| [Giderler Üç Yıl Üç Aylık Eğilim – Varsayılan](https://mix.office.com/watch/gwm4zu7tmtj8)             | Önceki üç yıl üzerinden geçen 12 çeyreğin giderleri hakkında anlayış kazanın.                                                                                                                                                                                                                                   |
| [Mali Sekmeler JE ve TB Gözden Geçirme – Varsayılan](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Kıymet, sorumluluk, sahibinin öz varlığı, gelir, gider, kazanç veya kayıp mali sekmeleri için yazıları için bakiye ve etkinliklere genel bakış konusunda bakın.                                                                                                                                                                           |
| [Gelir Beyanı – Varsayılan](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Geçerli dönem ve yıl başından bugüne kuruluşun karlılığını görüntüleyin.                                                                                                                                                                                                                                   |
| [Genel Muhasebe Hareket Listesi – Varsayılan](https://mix.office.com/watch/19h9v2rmh48vy)                        | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, hareket tarihi, günlük numarası, fiş, deftere nakil türü ve izleme numarası gibi ek hareket bilgileriyle birlikte borç ve alacak bakiyelerini gösterir.                                                                            |
| [Oranları– Varsayılan](https://mix.office.com/watch/b08hfc5h92me)                                          | Kuruluşun o yıl için ödeme gücü, karlılık ve verimlilik oranlarını görüntüleyin.                                                                                                                                                                                                                           |
| [Geri alınan 12 Aylık Giderler – Varsayılan](https://mix.office.com/watch/iywod5qmqhz7)                       | Son 12 ayın her biri için harcamaları hakkında bir anlayış kazanın. Bu 12 ay birden fazla mali yıla yayılabilir.                                                                                                                                                                                                       |
| [Geri Alınan Üç Aylık Gelir Tablosu – Varsayılan](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Geçen yıl ve yıl başından bugüne kadar bir kuruluşun üç aylık karlılığını görüntüleyin.                                                                                                                                                                                                                   |
| [Yan Yana Bilanço – Varsayılan](https://mix.office.com/watch/zkgq0u7visw9)                      | Kuruluşun o yıl için mali pozisyonunu görüntüleyin. Bu raporda, kıymetler ve pasif ve hissedar öz varlığı yan yana gösterilir.                                                                                                                                                                                |
| [Özet Mizan – Varsayılan](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve net farklarıyla birlikte borç ve alacak bakiyelerini görüntüleyin.                                                                                                                                                                  |
| [Özet Mizan Yıl Yıl – Varsayılan](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve bu yıl ve geçen yıl için net farklarıyla birlikte, borç ve alacak bakiyelerini görüntüleyin.                                                                                                                           |
| [Haftalık Satış ve İndirimler - Varsayılan](https://mix.office.com/watch/112ng0hy5de0j)                     | Bir ayın her haftası için satış ve indirimler hakkında anlayış kazanın. Bu rapor dört haftalık toplamı içerir.                                                                                                                                                                                                              |
| [Bütçe Fonları Kullanılabilir - Varsayılan](https://mix.office.com/watch/15hcpezcbx7tv)                         | Tüm kullanılabilir hesaplar için gözden geçirilmiş bütçenin, fiili harcamaların, bütçe ayırmalarının ve bütçe fonlarının ayrıntılı bir karşılaştırmasını görüntüleyin.                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Mali raporları açmak
**Finansal Raporlama** menüsüne tıklattığınızda, şirketin varsayılan finansal raporlarının listesi gösterilir. Sonra bir raporu açabilir veya değiştirebilirsiniz. Varsayılan raporlardan birini açmak için, rapor adını seçin. Bir rapor ilk defa açıldığında, otomatik olarak önceki ay için oluşturulur. Örneğin, bir raporu ilk kez Ağustos 2016'de açarsanız, rapor 31 Temmuz 2016 tarihi için oluşturulur. Rapor açıldıktan sonra, belirli veri parçalarında ayrıntıya inerek ve rapor seçeneklerini değiştirerek keşfetmeye başlayabilirsiniz.

## <a name="creating-and-modifying-financial-reports"></a>Mali raporları oluşturma ve değiştirme
Finansal raporlar listesinden yeni bir rapor oluşturabilir veya varolan bir raporu değiştirebilirsiniz. Uygun izinlere sahipseniz, Eylem Bölmesinde **Yeni** üzerine tıklayarak yeni bir mali rapor oluşturabilirsiniz. Bir rapor tasarımcısı programı cihazınıza indirilir. Rapor tasarımcısı çalıştıktan sonra, yeni raporu oluşturabilirsiniz. Yeni raporu kaydettikten sonra, mali raporlar listesinde görünür. Liste yalnızca Finance and Operations'da kullanmakta olduğunuz şirket için oluşturulan raporları gösterir. Mali raporları Finance and Operations içerisinde oluşturma ve değiştirme süreci hakkında daha fazla bilgi için, bkz. Dynamics mali raporlama blogundaki şu [blog postaları](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/). **Not:** Rapor tasarımcısı istemcisini indirdiğiniz bilgisayarın Microsoft .Net Framework'ün 4.6.2 sürümüne sahip olması gerekir. Microsoft .NET Framework'ün bu sürümünü [buradan](https://www.microsoft.com/en-us/download/details.aspx?id=53345) indirebilir ve kurabilirsiniz. Chrome kullanıyorsanız, rapor tasarımcısı istemcisini indirebilmek için ClickOnce eklentisini yüklemeniz gerekir. İncognito modunda kullanıyorsanız, ClickOnce eklentisinin incognito modu için etkin olduğundan emin olun. Ayrıca mali rapor listesinde görünen bir raporu değiştirebilirsiniz. Rapor adı etrafındaki alan seçildiğinde, Eylem Bölmesinden **Düzenleme** tıklatın. Rapor tasarımcısı programı başlar.

<a name="see-also"></a>Ayrıca bkz.
--------

[Mali raporları görüntüle](view-financial-reports.md)

[Dynamics Mali Raporlama blogu](http://blogs.msdn.com/b/dynamics_financial_reporting/)




