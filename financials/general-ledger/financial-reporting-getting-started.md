---
title: Mali raporlama
description: "Bu konu, Microsoft Dynamics 365 işlemleri için de finansal raporlama erişmek yer ve mali raporlama yeteneklerini kullanmayı açıklar. Sağlanan varsayılan finansal raporlar için bir açıklama içerir."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d13747f17b5f382b3a530b1f166681eeec0b9d73
ms.lasthandoff: 03/31/2017


---

# <a name="financial-reporting"></a>Mali raporlama

Bu konu, Microsoft Dynamics 365 işlemleri için de finansal raporlama erişmek yer ve mali raporlama yeteneklerini kullanmayı açıklar. Sağlanan varsayılan finansal raporlar için bir açıklama içerir.

<a name="accessing-financial-reporting"></a>Mali raporlamaya erişmek
-----------------------------

Bulabilirsiniz **finansal raporlama** yerler menüsü aşağıdaki işlemleri için Dynamics 365 içinde:

-   **Genel muhasebe**&gt;**Sorgulamalar ve raporlar**
-   **Bütçeleme**&gt;**Inquires ve raporları**&gt;**temel bütçeleme**
-   **Bütçeleme**&gt;**sorgu ve raporlarda**&gt;**bütçe planlama**
-   **Bütçeleme**&gt;**sorgu ve raporlarda**&gt;**bütçe denetimi**
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
| Mali raporları koru            | Mali raporları koru            | Finansal muhasebe müdürü, muhasebe gözetmen denetleyicisi, bütçe Yöneticisi |
| Mali raporlar oluştur            | Mali raporlar oluştur            | CEO, CFO, muhasebeci                                                            |
| Mali raporları görüntüle                | Mali performansı gözden geçir          | Hiçbiri atanmadı                                                                   |

Bir kullanıcı eklendikten veya bir rol değiştikten sonra, kullanıcının birkaç dakika içinde mali raporlamaya erişebilmesi gerekir. **Not:** sysadmin rolünün finansal raporlama tüm rolleri eklenir.

## <a name="default-reports"></a>Varsayılan raporlar
Finansal raporlama 22 varsayılan mali rapor sağlar. Her rapor varsayılan ana hesap kategorileri içinde Dynamics 365 işlemler için kullanır. Bu raporları olduğu gibi veya gerekli finansal raporlama için bir başlangıç noktası olarak kullanabilirsiniz. Gelir tablosu ve Bilanço gibi geleneksel mali tablolara ek olarak, bu varsayılan raporlar da oluşturabileceğiniz farklı mali rapor türlerini gösteren varsayılan raporlar içerir. Aşağıdaki tablo Office karışımı sunu bağlantılar içerisindeki her raporun rapor hakkında.

| Varsayılan rapor                                                                                         | Açıklama                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 Month Rolling Single Column Income Statement – Default](https://mix.office.com/watch/76kc7bm3wnt1) | Bir kuruluşun son 12 ay içindeki karlılığını tek bir sütun olarak görüntüleyin.                                                                                                                                                                                                                                      |
| [12 Month Trend Income Statement – Default](https://mix.office.com/watch/12brmfge5p8r)                 | Bir kuruluşun her 12 ay için karlılığını görüntüleyin. Bu 12 ay birden fazla mali yıla yayılabilir.                                                                                                                                                                                             |
| [Actual vs Budget – Default](https://mix.office.com/watch/fi439lkwr0no)                                | Orijinal bütçe için tüm hesapların bakiye bilgilerini görüntüleyin ve gözden geçirilmiş bütçeyi fark içeren fiili değerlerle karşılaştırın.                                                                                                                                                                          |
| [Audit Details – Default](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, borç ve alacak bakiyelerini raporlama para biriminde ve yerel para biriminde, kullanıcı kimliği, veriyi değiştiren kullanıcı, son değiştirilme tarihi ve günlük kimliği gibi ek hareket bilgileriyle birlikte gösterir. |
| [Balance List – Default](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, açılış ve kapanış bakiyelerini ve geçerli dönem ve yıl başından bugüne borç ve alacak bakiyelerini, fiş gibi ek hareket bilgileriyle birlikte gösterir.                                                                    |
| [Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                                   | Kuruluşun o yıl için mali pozisyonunu görüntüleyin.                                                                                                                                                                                                                                                             |
| [Balance Sheet and Income Statement Side by Side - Default](https://mix.office.com/watch/zkgq0u7visw9) | Organizasyonun mali pozisyonunu ve karlılığını yıl için yan yana görüntüleyin.                                                                                                                                                                                                                              |
| [Cash Flow – Default](https://mix.office.com/watch/jd3go9pz6390)                                       | Kuruluşa giden ve gelen nakit hakkında bir anlayış kazan.                                                                                                                                                                                                                                   |
| [Detailed JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Tüm hesaplar için açılış bakiyesini ve etkinlik bilgilerini görüntüle.                                                                                                                                                                                                                                                      |
| [Detailed Trial Balance - Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Borç ve alacak bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve hareket tarihi, fiş ve günlük açıklamasıyla birlikte bu bakiyelerin net değerini görüntüleyin.                                                                                                                                  |
| [Expenses Three Year Quarterly Trend – Default](https://mix.office.com/watch/gwm4zu7tmtj8)             | Önceki üç yıl üzerinden geçen 12 çeyreğin giderleri hakkında anlayış kazanın.                                                                                                                                                                                                                                   |
| [Financial Captions JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Kıymet, sorumluluk, sahibinin öz varlığı, gelir, gider, kazanç veya kayıp mali sekmeleri için yazıları için bakiye ve etkinliklere genel bakış konusunda bakın.                                                                                                                                                                           |
| [Income Statement – Default](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Geçerli dönem ve yıl başından bugüne kuruluşun karlılığını görüntüleyin.                                                                                                                                                                                                                                   |
| [Ledger Transaction List – Default](https://mix.office.com/watch/19h9v2rmh48vy)                        | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, hareket tarihi, günlük numarası, fiş, deftere nakil türü ve izleme numarası gibi ek hareket bilgileriyle birlikte borç ve alacak bakiyelerini gösterir.                                                                            |
| [Ratios – Default](https://mix.office.com/watch/b08hfc5h92me)                                          | Kuruluşun o yıl için ödeme gücü, karlılık ve verimlilik oranlarını görüntüleyin.                                                                                                                                                                                                                           |
| [Rolling 12 Month Expenses – Default](https://mix.office.com/watch/iywod5qmqhz7)                       | Son 12 ayın her biri için harcamaları hakkında bir anlayış kazanın. Bu 12 ay birden fazla mali yıla yayılabilir.                                                                                                                                                                                                       |
| [Rolling Quarter Income Statement – Default](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Geçen yıl ve yıl başından bugüne, ayda bir kuruluşun Karlılık görüntüleyin.                                                                                                                                                                                                                   |
| [Side by Side Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                      | Kuruluşun o yıl için mali pozisyonunu görüntüleyin. Bu raporda, kıymetler ve pasif ve hissedar öz varlığı yan yana gösterilir.                                                                                                                                                                                |
| [Summary Trial Balance – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve net farklarıyla birlikte borç ve alacak bakiyelerini görüntüleyin.                                                                                                                                                                  |
| [Summary Trial Balance Year Over Year – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Bu yıl ve geçen yıl için açılış ve kapanış bakiyeleri ve Borç ve alacak bakiyelerinin kendi net fark ile birlikte olan tüm hesaplar için Bakiye bilgilerini görüntüleyin.                                                                                                                           |
| [Weekly Sales and Discounts - Default](https://mix.office.com/watch/112ng0hy5de0j)                     | Bir ayın her haftası için satış ve indirimler hakkında anlayış kazanın. Bu rapor dört haftalık toplamı içerir.                                                                                                                                                                                                              |
| [Bütçe fon kullanılabilir - varsayılan](https://mix.office.com/watch/15hcpezcbx7tv)                         | Ayrıntılı gözden geçirilmiş bütçe, fiili harcamaları, bütçe ayırmaları ve bütçe fon tüm hesapları için kullanılabilir karşılaştırması                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Mali raporları açmak
**Finansal Raporlama** menüsüne tıklattığınızda, şirketin varsayılan finansal raporlarının listesi gösterilir. Sonra bir raporu açabilir veya değiştirebilirsiniz. Varsayılan raporlardan birini açmak için, rapor adını seçin. Bir rapor ilk defa açıldığında, otomatik olarak önceki ay için oluşturulur. Örneğin, bir raporu ilk kez Ağustos 2016 açarsanız, rapor 31 Temmuz 2016 için oluşturulur. Rapor açıldıktan sonra, belirli veri parçalarında ayrıntıya inerek ve rapor seçeneklerini değiştirerek keşfetmeye başlayabilirsiniz.

## <a name="creating-and-modifying-financial-reports"></a>Mali raporları oluşturma ve değiştirme
Finansal raporlar listesinden yeni bir rapor oluşturabilir veya varolan bir raporu değiştirebilirsiniz. Uygun izinleriniz varsa, yeni bir mali rapor tıklatarak oluşturabilirsiniz **yeni** eylem bölmesi. Rapor Tasarımcısı bir programın aygıtınıza karşıdan yüklenir. Rapor Tasarımcısı başladıktan sonra yeni bir rapor oluşturabilirsiniz. Yeni raporu kaydettikten sonra, mali raporlar listesinde görünür. Liste içinde Dynamics 365 işlemleri için kullanmakta olduğunuz şirket için oluşturulan raporları gösterir. Oluşturma ve değiştirme işlemleri için Dynamics 365 finansal raporları hakkında daha fazla bilgi için işlem, bunlar için başvuruda [blog postaları](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) blog Dynamics finansal raporlama. **Not:** Rapor Tasarımcısı istemci üzerinde sürüm 4.6.2 Microsoft .NET Framework'ün bilgisayarda yüklü olması gerekir karşıdan yüklediğiniz bilgisayar. Microsoft .NET Framework'ün bu sürümü karşıdan ve installed from [burada](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Krom kullanıyorsanız, Rapor Tasarımcısı istemci yüklemek için ClickOnce uzantısı yüklemeniz gerekir. İncognito modda çalıştırıyorsanız, ClickOnce uzantısı için incognito modu etkin olduğundan emin olun. Ayrıca mali rapor listesinde görünen bir raporu değiştirebilirsiniz. Rapor adı etrafındaki alan seçildiğinde, Eylem Bölmesinden **Düzenleme** tıklatın. Rapor tasarımcısı programı başlar.

<a name="see-also"></a>Ayrıca bkz.
--------

[View financial reports](view-financial-reports.md)

[Dynamics Mali Raporlama blogu](http://blogs.msdn.com/b/dynamics_financial_reporting/)


