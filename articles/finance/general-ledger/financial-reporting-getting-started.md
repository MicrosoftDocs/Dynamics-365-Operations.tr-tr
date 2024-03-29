---
title: Mali raporlamaya genel bakış
description: Bu makalede, Microsoft Dynamics 365 Finance'te mali raporlara nereden erişileceği ve finansal raporlama özelliklerinin nasıl kullanılacağı açıklanmaktadır.
author: aprilolson
ms.date: 06/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "10444"
- intro-internal
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d0c2e821ee504cd62a536674ef91ee89a25c0a9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066432"
---
# <a name="get-started-with-financial-reporting"></a>Mali raporlamayı kullanmaya başlama 

[!include [banner](../includes/banner.md)]

Bu makalede, Mali raporlamalara nereden erişileceği ve mali raporlama özelliklerinin nasıl kullanılacağı açıklanmaktadır. Ayrıca, sağlanan varsayılan mali raporların bir açıklamasını da içerir.

## <a name="enable-financial-reporting"></a>Mali raporlamayı etkinleştirme
Kuruluşunuz için mali raporlama hizmetini kullanmak için, bu servisi bir Lifecycle Services (LCS) yöneticisinin, LCS portalında kuruluşunuza yönelik olarak etkinleştirmesi gerekir. Ortamınız için finansal raporlama sağlanmadıysa, hizmeti etkinleştirmesi için LCS yöneticinize başvurun. 

## <a name="accessing-financial-reporting"></a>Mali raporlamaya erişme

**Finansal raporlama** menüsünü aşağıdaki konumlarda bulabilirsiniz:

- **Genel Muhasebe** > **Sorgulamalar ve raporlar**
- **Bütçeleme** > **Sorgular ve raporlar** > **Temel bütçeleme**
- **Bütçeleme** > **Sorgular ve raporlar** > **Bütçe planlama**
- **Bütçeleme** > **Sorgular ve raporlar** > **Bütçe denetimi**
- Konsolidasyonlar

Bir tüzel kişilik için finansal raporlar oluşturmak ve üretmek için, bu tüzel kişilik için aşağıdaki bilgileri ayarlamanız gerekir:

- Mali takvim
- Genel muhasebe
- Hesap planı
- Para Birimi
- En az bir hesaba hareket nakletme
- MainAccount, **Mali raporlama ayarı** sayfasında (**Genel muhasebe > Genel muhasebe ayarı > Mali raporlama ayarı**) **Seçili** sütununda listelenir

## <a name="granting-security-access-to-financial-reporting"></a>Financial Reporting'e güvenlik erişimi verme

Finansal raporlama işlevleri uygun ayrıcalıklara sahip ve güvenlik rolleri aracılığıyla görevler atanmış kullanıcılar için kullanılabilirdir. Aşağıdaki bölümlerde bu ayrıcalıklar ve görevler, ilişkili rollerle birlikte listelenmiştir.

### <a name="duties"></a>Görev

| Görev etiketi                            | Tanım                                                             | AOT adı                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Mali raporlama güvenliğini sağla | Mali raporlama güvenliğini sağlayın ve yönetici görevlerini gerçekleştirin. | MaliRaporlarGüvenlikSağlama |
| Mali raporları koru            | Mali raporları tasarla ve koru.                                  | MaliRaporlarıKoru         |
| Mali raporlar oluştur            | Mali raporları oluştur ve yenile.                                 | MaliRaporlarOluştur         |
| Mali performansı gözden geçir          | Mali performansı gözden geçir ve çözümle.                               | MaliRaporlarPerformansGözdenGeçirme       |

### <a name="privileges"></a>Ayrıcalıklar

| Ayrıcalık etiketi                       | Tanım                                                             | AOT adı                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Mali raporlama güvenliğini sağla | Mali raporlama güvenliğini sağlayın ve yönetici görevlerini gerçekleştirin. | FinancialReportsSecuritySystemMaintain |
| Mali raporları koru            | Mali raporları tasarla ve koru.                                  | MaliRaporlarRaporlarıKoru  |
| Mali raporlar oluştur            | Mali raporları oluştur ve yenile.                                 | MaliRaporlarRaporlarOluştur  |
| Mali raporları görüntüle                | Mali raporları görüntüle.                                                 | MaliRraporlarıGörüntüle             |

### <a name="roles"></a>Roller

| Ayrıcalık etiketi                       | Vergi                                  | Roller                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Mali raporlama güvenliğini sağla | Mali raporlama güvenliğini sağla | Güvenlik yöneticisi                                                          |
| Mali raporları koru            | Mali raporları koru            | Muhasebe Yöneticisi, Muhasebe Gözetmeni, Mali Denetleyici, Bütçe Yöneticisi |
| Mali raporlar oluştur            | Mali raporlar oluştur            | CEO, CFO, Muhasebeci                                                            |
| Mali raporları görüntüle                | Mali performansı gözden geçir          | Hiçbiri atanmadı                                                                   |

Bir kullanıcı eklendikten veya bir rol değiştikten sonra, kullanıcının birkaç dakika içinde Financial Reporting'e erişebilmesi gerekir. 

> [!NOTE]
> sysadmin rolü finansal raporlamadaki tüm rollere eklenir.

## <a name="report-deletions-and-expirations"></a>Silme ve süre sonlarını bildir

Rapor oluşturan kullanıcılar kendi raporlarını silebilir. **Finansal Raporlama Güvenlik** vergisi olan kullanıcıların diğer raporlarını silebilir. 

Sürüm 10.0.8'de, bitiş tarihleri kavramı kullanıma sunulmuştur. Özellik yönetimi çalışma alanı içindeki **Tümü** sayfasında yeni bir gerekli özellik etkinleştirilmiştir. **Finansal rapor tutma ilkeleri** özelliği aşağıdaki değişiklikleri içerir:
* Yeni oluşturulan raporlar, oluşturulduklarında süresi sona 90 gün geçerlilik tarihine sahip olacak şekilde otomatik olarak işaretlenecek.
* Özelliğin yüklenmesi öncesinde varolan tüm raporlara, 90 günlük bir geçerlilik süresi verilir. Mali raporlama hizmeti tamamlanana kadar tarih kısa bir süre için boş olarak gösterilebilir, bir rapor oluşturulur ve hizmet güncelleştirmeyi boş bitiş tarihi olan mevcut raporlar için gerçekleştirir. 
* **Finansal Raporlama güvenliğini koru** ayrıcalığına sahip kullanıcıların bu işlevlere erişimi vardır. **Finansal rapor kullanım süresi sonu** hakkı verilen **Finansal raporu koru**'daki her kullanıcının, kullanım süresi sonu süresini değiştirme olanağı da vardır. Şu anda iki tutma seçeneği kullanılabilir: 

    * 90 günlük bitiş tarihi.
    * Raporu asla sona erme olarak ayarlamak için bir seçenek.

90 gün gibi bir süre sonu seçildiğinde, bugünden itibaren 90 gün sonra uygulanır. Bu, raporun oluşturulduğu sırada ayarlanan özgün oluşturma tarihinden itibaren 90 günden farklı bir davranıştır. 

Gelecekteki işlevler içinde ek seçenekler dikkate alınacaktır. Varsayılan değer 90 günlük bitiş tarihi olacak ve uygun izinlere sahip kullanıcılar **Mali raporlar** liste sayfasında varsayılan değeri geçersiz kılabilecektir.

## <a name="default-reports"></a>Varsayılan raporlar

Finansal raporlama 22 varsayılan mali rapor sağlar. Her rapor, varsayılan ana hesap kategorilerini kullanır. Bu raporları olduğu gibi veya gerekli finansal raporlama için bir başlangıç noktası olarak kullanabilirsiniz. Gelir tablosu ve Bilanço gibi geleneksel mali tablolara ek olarak, bu varsayılan raporlar da oluşturabileceğiniz farklı mali rapor türlerini gösteren varsayılan raporlar içerir. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Varsayılan rapor                                                                                         | Açıklama                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 Aylık Geri Alınan Tek Sütun Gelir Tablosu – Varsayılan | Kuruluşun son 12 ay içindeki karlılığını tek bir sütun olarak görüntüleyin.                                                                                                                                                                                                                                      |
| 12 aylık Eğilim Gelir Tablosu – Varsayılan                 | Son 12 ayın her biri için kuruluşun karlılığını görüntüleyin. Bu 12 ay birden fazla mali yıla yayılabilir.                                                                                                                                                                                             |
| Gerçek ile Bütçe karşılaştırması – Varsayılan                                | Orijinal bütçe için tüm hesapların bakiye bilgilerini görüntüleyin ve gözden geçirilmiş bütçeyi fark içeren fiili değerlerle karşılaştırın.                                                                                                                                                                          |
| Denetim Ayrıntıları – Varsayılan                                  | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, borç ve alacak bakiyelerini raporlama para biriminde ve yerel para biriminde, kullanıcı kimliği, veriyi değiştiren kullanıcı, son değiştirilme tarihi ve günlük kimliği gibi ek hareket bilgileriyle birlikte gösterir. |
| Bakiye Listesi – Varsayılan                                   | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, açılış ve kapanış bakiyelerini ve geçerli dönem ve yıl başından bugüne borç ve alacak bakiyelerini, fiş gibi ek hareket bilgileriyle birlikte gösterir.                                                                    |
| Bakiye – Varsayılan                                   | Kuruluşun o yıl için mali pozisyonunu görüntüleyin.                                                                                                                                                                                                                                                             |
| Bilanço ve Gelir Beyanı Yan Yana - Varsayılan | Kuruluşun yıl içindeki mali pozisyonunu ve karlılığını yan yana görüntüleyin.                                                                                                                                                                                                                              |
| Nakit Akışı – Varsayılan                                       | Kuruluşa giden ve gelen nakit hakkında bir anlayış kazan.                                                                                                                                                                                                                                   |
| Ayrıntılı JE ve TB Gözden Geçirme – Varsayılan                      | Tüm hesaplar için açılış bakiyesini ve etkinlik bilgilerini görüntüle.                                                                                                                                                                                                                                                      |
| [Ayrıntılı Mizan - Varsayılan](trial-balance-financial-reports.md)| Borç ve alacak bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve hareket tarihi, fiş ve günlük açıklamasıyla birlikte bu bakiyelerin net değerini görüntüleyin.                                                                                                                                  |
| Giderler Üç Yıl Üç Aylık Eğilim – Varsayılan             | Önceki üç yıl üzerinden geçen 12 çeyreğin giderleri hakkında anlayış kazanın.                                                                                                                                                                                                                                   |
| Mali Sekmeler JE ve TB Gözden Geçirme – Varsayılan            | Varlık, borç, şirket sahibinin öz varlığı, gelir, gider, kazanç veya zarar mali sekmeleri için bakiyelere ve faaliyetlere ilişkin genel bakışı inceleyin.                                                                                                                                                                           |
| [Gelir Beyanı – Varsayılan](income-statement-financial-report.md)| Kuruluşun geçerli dönem için ve yıl başından bu güne kadar olan süre içindeki karlılığını görüntüleyin.                                                                                                                                                                                                                                   |
| Genel Muhasebe Hareket Listesi – Varsayılan                        | Tüm hesaplar için ayrıntılı bakiye bilgilerini görüntüleyin. Bu rapor, hareket tarihi, günlük numarası, fiş, deftere nakil türü ve izleme numarası gibi ek hareket bilgileriyle birlikte borç ve alacak bakiyelerini gösterir.                                                                            |
| Oranları– Varsayılan                                          | Kuruluşun o yıl için ödeme gücü, karlılık ve verimlilik oranlarını görüntüleyin.                                                                                                                                                                                                                           |
| Geri alınan 12 Aylık Giderler – Varsayılan                       | Son 12 ayın her biri için harcamaları hakkında bir anlayış kazanın. Bu 12 ay birden fazla mali yıla yayılabilir.                                                                                                                                                                                                       |
| Geri Alınan Üç Aylık Gelir Tablosu – Varsayılan               | Kuruluşun karlılığını geçen yıl için ve yılbaşından bugüne kadar olan süre içinde üç aylık dönemler halinde görüntüleyin.                                                                                                                                                                                                                   |
| Yan Yana Bilanço – Varsayılan                      | Kuruluşun o yıl için mali pozisyonunu görüntüleyin. Bu raporda, kıymetler ve pasif ve hissedar öz varlığı yan yana gösterilir.                                                                                                                                                                                |
| [Özet Mizan – Varsayılan](trial-balance-financial-reports.md)| Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve net farklarıyla birlikte borç ve alacak bakiyelerini görüntüleyin.                                                                                                                                                                  |
| [Özet Mizan Yıl Yıl – Varsayılan](trial-balance-financial-reports.md)| Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve bu yıl ve geçen yıl için net farklarıyla birlikte, borç ve alacak bakiyelerini görüntüleyin.                                                                                                                           |
| Haftalık Satış ve İndirimler - Varsayılan                     | Bir ayın her haftası için satış ve indirimler hakkında anlayış kazanın. Bu rapor dört haftalık toplamı içerir.                                                                                                                                                                                                              |
| Bütçe Fonları Kullanılabilir - Varsayılan                         | Tüm kullanılabilir hesaplar için gözden geçirilmiş bütçenin, fiili harcamaların, bütçe ayırmalarının ve bütçe fonlarının ayrıntılı bir karşılaştırmasını görüntüleyin.                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Mali raporları açmak

**Finansal raporlama** menüsünü seçtiğinizde şirketin varsayılan finansal raporlarının listesi gösterilir. Sonra bir raporu açabilir veya değiştirebilirsiniz. Varsayılan raporlardan birini açmak için, rapor adını seçin. Bir rapor ilk defa açıldığında, otomatik olarak önceki ay için oluşturulur. Örneğin, bir raporu ilk kez Ağustos 2019'de açarsanız, rapor 31 Temmuz 2019 tarihi için oluşturulur. Rapor açıldıktan sonra, belirli veri parçalarında ayrıntıya inerek ve rapor seçeneklerini değiştirerek keşfetmeye başlayabilirsiniz.

## <a name="creating-and-modifying-financial-reports"></a>Mali raporları oluşturma ve değiştirme

Finansal raporlar listesinden yeni bir rapor oluşturabilir veya varolan bir raporu değiştirebilirsiniz. Uygun izinlere sahipseniz, Eylem Bölmesinde **Yeni**'yi seçerek yeni bir mali rapor oluşturabilirsiniz. Bir rapor tasarımcısı programı cihazınıza indirilir. Rapor tasarımcısı çalıştıktan sonra, yeni raporu oluşturabilirsiniz. Yeni raporu kaydettikten sonra, mali raporlar listesinde görünür. Liste yalnızca Dynamics 365 Finance'ta kullanmakta olduğunuz şirket için oluşturulan raporları gösterir. 

## <a name="reporting-tree-definitions"></a>Raporlama ağacı tanımları

Mali raporlar oluşturmak için kullanılan bileşenlerden biri raporlama ağacı tanımıdır. Raporlama ağacı tanımı kuruluşunuzun yapısı ve hiyerarşisini tanımlamaya yardımcı olur. Mali verilerinizde boyutlu ilişkilere dayanan çapraz boyutlu hiyerarşik bir yapıdır. Ağaçtaki tüm birimler için raporlama birimi düzeyinde ve özet düzeyinde bilgi sağlar.

Kuruluşunuzun verilerini çeşitli şekillerde görüntülemek için sınırsız sayıda raporlama ağacı oluşturabilirsiniz. Her raporlama ağacı bölümlerin ve özet birimlerinin herhangi bir bileşimini içerebilir, ancak bir rapor tanımı bir seferde yalnızca bir raporlama ağacına bağlanabilir. 

## <a name="update-the-financial-reporting-version-through-slipstreaming"></a>Mali raporlama sürümünü birleştirilmiş yükleme yoluyla güncelleştirme

Finans ve operasyon uygulamaları her ay güncellenir. Ancak, Mali raporlamanın bu hızda güncelleştirilmesi gerekmez. Ayrıca müşteriler, finans ve operasyon uygulamaları güncelleştirmelerini ne zaman uygulayacakları konusunda daha fazla seçeneğe sahiptir. Mali raporlama güncelleştirmeleri otomatik olarak yüklenir. Mali raporlamanın hizmet güncelleştirmesi uygulandığında, kesinti süresi başlatıldığında veya bir müşterinin ortamı Bakım modundayken müşteri ortamında çalışan belirlenmiş bir sürümü bulunur. Tüm müşteri uygulamaları aynı Mali raporlama sürümüne ayarlandığından bu süreç *birleştirilmiş yükleme* veya *doğrultma* olarak bilinir.

Her sürümde yayınlanan değişiklikler [Dynamics 365 Finance uygulamasındaki yenilikler veya değişiklikler](../../finance/get-started/whats-new-home-page.md) bölümünde bulunabilir. Platform güncelleştirmeleri ve hata düzeltmeleri, her sürüm için sayfanın altındaki "Ek Kaynaklar" bölümünde bulunabilir.

Seçilen birleştirilmiş yükleme sürümü üretime hazır, gözden geçirilmiş ve onaylanmış bir Mali raporlama sürümüdür. Dynamics 365 Finance uygulamasının önceki veya gelecekteki sürümleriyle uyumludur. Örneğin, müşteri hala 10.0.16 uygulama sürümündeyken Mali raporlama en son 10.0.19 derlemesinde olabilir.

> [!NOTE]
> Müşterilerin önceki bir sürüme geçebileceği (bir sürüm düşürme senaryosu) tek durum Microsoft'un bir sorun nedeniyle doğrultma sunumunu durdurması durumunda ortaya çıkar. Düzeltme kullanılabilir olur olmaz otomatik olarak uygulanacaktır.

Birleştirilmiş yükleme süreci tamamen otomatiktir ve herhangi bir müşteri eylemi gerektirmez. Üç topolojinin her biri birleştirilmiş yükleme sürecini birbirinden biraz farklı bir şekilde uygular:

- **Şirket içi**: Şirket içi dağıtımlar, birleştirilmiş yükleme ve doğrultmayı desteklemez.
- **Hizmet olarak altyapı (IaaS)**: Mali raporlamayı güncelleştirmeye çalışan herhangi bir işlem sırasında birleştirilmiş yükleme mantığı uygulanır. Bu durum, ikili güncelleştirmeler veya ikili güncelleştirmeler içeren yayınları içerir.
- **Self servis**: Mali raporlamada kesinti süresi gerektiren herhangi bir işlem, birleştirilmiş yükleme mantığını uygular:

    - İkili güncelleştirmeler veya ikili güncelleştirmeler içeren yayınlar
    - S yaması veya diğer altyapı kesinti süreleri
    - AOT paketi dağıtımları

## <a name="troubleshooting-issues-opening-report-designer"></a>Rapor Tasarımcısı açma sorunlarını giderme

Rapor Tasarımcısı'nı açtığınızda sorunlara neden olabilen bazı genel sorunlar bulunmaktadır. Bu sorunlar ve bunları gidermek için gereken adımlar aşağıdaki gibidir.

Sorun 1: **Yeni** veya **Düzenle**'yi seçtiğinizde Rapor Tasarımcısı başlamıyor.

* Internet Explorer'da **Ayarlar**'ı ve ardından **İnternet Seçenekleri**'ni seçin. **Güvenlik** sekmesini seçin. Güvenilen Siteler'i ve sonra **Siteler**'i seçin. **Bu web sitesini bölgeye ekle** alanında "\*\.dynamics.com" (tırnak işaretleri olmadan) girin ve **Ekle**'yi seçin. 
* Internet Explorer'da **Ayarlar**'ı ve ardından **İnternet Seçenekleri**'ni seçin. **Güvenlik** sekmesini seçin. Güvenilen Siteler'i seçin. Bu bölge için Güvenlik düzeyi etiketli alanda, seçeneği **Orta-Düşük** olarak değiştirin.
* Tarayıcınızdaki açılır pencere engelleyicisini devre dışı bırakın.
* Microsoft .NET Framework 4.7.2 veya üstünü yüklemek için iş istasyonları gereklidir. Microsoft .NET Framework'ün bu sürümünü [Microsoft Download Center'dan](https://dotnet.microsoft.com/download/dotnet-framework/net472) indirebilir ve kurabilirsiniz.
* Chrome tarayıcı kullanıyorsanız Rapor Tasarımcısı istemcisini indirebilmek için ClickOnce eklentisini yüklemeniz gerekir. Chrome'u gizli modda çalıştırıyorsanız ClickOnce eklentisinin gizli mod için etkinleştirildiğinden emin olun. Chrome ClickOnce Eklentisi hakkında daha fazla bilgi için bkz. [Bulut dağıtımları için sistem gereksinimleri](../../fin-ops-core/fin-ops/get-started/system-requirements.md).
* Chrome tarayıcıyla Microsoft Edge kullanıyorsanız Edge Chromium için ClickOnce eklentisi yüklemeniz gerekmez. Ancak, Rapor Tasarımcısı istemcisini indirebilmek için ClickOnce seçeneğini etkinleştirmelisiniz. İncognito modunda kullanıyorsanız, ClickOnce eklentisinin incognito modu için etkin olduğundan emin olun.

    1. Microsoft Edge'de yeni bir tarayıcı açın.
    2. **edge://flags** girin ve **Enter** seçeneğini belirleyin.
    3. **ClickOnce Destek** seçeneğini arayın veya bu doğrudan bağlantıyı kullanın: **edge://flags/#edge-click-once**.
    4. Açılır menü seçeneğini **Etkin** olarak ayarlayın.
    5. **Tarayıcıyı Yeniden Başlat**'ı seçin.

Sorun 2: Kullanıcıya Mali raporlama kullanmak için gerekli izinler atanmadı. 

* Kullanıcının izni olup olmadığını doğrulamak için şu hata iletisi altında **Evet**'i seçin: "Financial Reporting sunucusuna bağlanılamıyor. Devam etmek istiyorsanız Evet'i seçin ve farklı bir sunucu adresi belirtin." Ardından **Bağlantı Sınama** sekmesini seçin. İzniniz yoksa şu iletiyi alırsınız: "Bağlantı girişimi başarısız oldu. Kullanıcı sunucuya bağlanmak için uygun izinlere sahip değil. Sistem yöneticinize başvurun."
* Gerekli izinler, yukarıdaki [Financial Reporting'e güvenlik erişimi verme](#granting-security-access-to-financial-reporting) bölümünde listelenmiştir. Financial Reporting'de güvenlik, bu ayrıcalıkları temel alır. Bu ayrıcalıklar (veya bu ayrıcalıkları içeren başka bir güvenlik rolü) size atanmadıkça erişiminiz olmayacaktır. 
* **Şirket Kullanıcıları Sağlayıcısı'dan Şirkete** tümleştirme görevi (kullanıcı tümleştirmesinden sorumludur ve kullanıcı tümleştirmesi olarak da bilinir) 5 dakikalık bir aralıkta çalışır. Tüm izin değişikliklerinin Mali raporlamada geçerli olması 10 dakika kadar sürebilir. 

    Başka bir kullanıcı Rapor Tasarımcısını açabiliyorsa, **Araçlar**'ı ve ardından **Tümleştirme Durumu**'nu seçin. Mali raporlama kullanma izni atadığınız için "Şirket Kullanıcıları Sağlayıcısından Şirkete" tümleştirme eşlemesinin başarılı şekilde çalışıp çalışmadığını doğrulayın. 

* Başka bir hata **Dynamics kullanıcısı ile Financial Reporting kullanıcısı tümleştirmesinin** tamamlanmasını engellemiş olabilir. Ya da, bir veri reyonu sıfırlama işlemi başlatılmış ve henüz tamamlanmamış veya başka bir sistem hatası oluşmuş olabilir. İşlemi daha sonra yeniden çalıştırmayı deneyin. Sorun devam ederse, sistem yöneticinize başvurun.

Sorun 3: Önceki **ClickOnce Report Designer** oturum açma sayfasından devam edebilirsiniz ancak Report Designer içinde oturum açma işlemini tamamlayamazsınız. 

* Oturum açma kimlik bilgilerinizi girdiğinizde yerel bilgisayarınızda ayarlanan saat ile Financial Reporting sunucusundaki saat arasında en fazla beş dakikalık bir fark olmalıdır. Beş dakikadan uzun bir fark varsa, sistem oturum açma işlemine izin vermez. 
* Bilgisayarınızdaki saat, Financial Reporting sunucusundaki saatten farklıysa bilgisayarınızın saatini otomatik olarak ayarlamak için Windows seçeneğini etkinleştirmenizi öneririz. 

## <a name="troubleshoot-report-designer-issues-with-event-viewer"></a>Olay görüntüleyici ile Report Designer sorunlarını giderme

Financial Reporting'i kullanırken ortaya çıkan sorunlardan bazılarını analiz etmek için Olay görüntüleyiciyi kullanabilirsiniz. 

### <a name="what-happens-when-you-have-connections-issues-with-financial-reporting"></a>Financial Reporting ile ilgili bağlantı sorunlarınız olduğunda ne olur? 

Microsoft desteği ile konuşmanızı daha etkili hale getirmek ve daha hızlı çözüme ulaşmak için atabileceğiniz bazı adımlar aşağıdadır. 
 
Aşağıdaki adımlar, Financial Reporting için Olay görüntüleyicisi iletilerini açma işlemi konusunda yol gösterir. Olay görüntüleyicinin oluşturduğu günlükler, bağlantı sorununun kaynağını hızlıca belirlemek için destek mühendislerine yardımcı olur. Destek ile iletişim kurarken bu günlüklerin kopyalarını biletle birlikte gönderin.


1. RegisterETW.zip dosyasını istemci iş istasyonuna (tercihen Masaüstü) kopyalayın ve [RegisterETW.zip](https://mbs2.microsoft.com/fileexchange/?fileID=60b1106b-d5f8-4e0f-8041-039102505122) dosyasını ayıklayın.
2. Windows Olay görüntüleyicinin kapalı olduğundan emin olun.
3. Yönetici PowerShell komut istemi açın ve RegisterETW.ps1 dosyasının bulunduğu dizine gidin.
4. Şu komutu çalıştırın: .\RegisterETW.ps1

    PowerShell'de başarılı bir çıkış, **Tamamlanan RegisterETW komut dosyası** iletisiyle doğrulanır.

    Olay görüntüleyiciyi yeniden açtığınızda artık **Microsoft > Dynamics** altında şu günlükleri görürsünüz:

    * MR-Client
    * MR-DVT
    * MR-Integration
    * MR-Logger
    * MR-Reporting
    * MR_SchedulerTasks
    * MR-Sql
    * MR-TraceManager

5. Sorunu Report Designer'da yeniden oluşturun.
6. Olay görüntüleyiciyi kullanarak MR-Logger olaylarını dışarı aktarın.

## <a name="troubleshoot-issues-connecting-to-financial-reporting"></a>Financial Reporting'e bağlanma ile ilgili sorunları giderme

Sorun: "Financial Reporting sunucusuna bağlanılamıyor" hatasını alıyorsunuz.

* Sorunun Chrome ve Edge internet tarayıcılarında oluşup oluşmadığını belirleyin.
* Sorun yalnızca tek tarayıcıda oluşuyorsa ClickOnce sorunu olabilir. 
* Bağlantı hatası iletisini aldığınızda hangi iletinin görüntülendiğini görmek için bağlantıyı test etmek üzere **Test Et**'i seçin. 
* Bu sorun, başka bir kullanıcının Financial Reporting erişimi olmamasından kaynaklanabilir. Erişimi yoksa kullanıcı, izne sahip olmadığını belirten bir ileti alır.
* Sorun birden çok tarayıcıda meydana geliyorsa iş istasyonunuzdaki saatin Otomatik olarak ayarlandığından emin olun.
* Bağlanıp bağlanamadığını görmek için iş istasyonunuzda oturum açmak üzere Dynamics 365 Finance'te güvenlik yöneticisi haklarına ve ağ etki alanında yönetici haklarına sahip bir kullanıcıyla birlikte çalışın. Bu kullanıcı bağlanabiliyorsa sorun ağ izinleriyle ilgili olabilir.
* İş istasyonunda, güvenlik duvarını geçici olarak devre dışı bırakın. Ardından Report Designer'a bağlanabiliyorsanız sorun güvenlik duvarınızla ilgilidir. Sorunu çözmek için kuruluşunuzun BT departmanıyla birlikte çalışın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Mali raporları görüntüle](view-financial-reports.md)
- [Mali raporlarda raporlama ağacı tanımları](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

