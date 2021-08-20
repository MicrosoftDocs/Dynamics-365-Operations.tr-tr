---
title: Maliyet kontrolü çalışma alanı
description: Bu konu, Maliyet kontrolü çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, bir maliyet nesnesini veya maliyet nesneleri dizisi bir boyut içinde veya boyutlar arasında denetlemekten sorumlu yöneticiler için raporlara erişebilmeleri amacıyla merkezi bir noktadır.
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace, CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: db587f5526e0541fc81964d510000a42a671a9bd65224e7167b9d869475c3601
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763202"
---
# <a name="cost-control-workspace"></a>Maliyet kontrolü çalışma alanı 

[!include [banner](../includes/banner.md)]

**Maliyet denetimi** çalışma alanı, bir maliyet nesnesini veya maliyet nesneleri dizisi bir boyut içinde veya boyutlar arasında (örneğin, maliyet merkezleri ve ürün grupları) denetlemekten sorumlu yöneticiler için raporlara erişebilmeleri amacıyla merkezi bir noktadır. Çalışma alanındaki raporlar, raporlama için kullanılan verinin tüm kuruluş çapında istikrarlı olabilmesi için tümüyle maliyet muhasebecileri tarafından kontrol edilir.

## <a name="cost-control-workspace-configuration"></a>Maliyet kontrolü çalışma alanı yapılandırması

Maliyet muhasebecileri, istenilen veri bileşimi veya biçim için ihtiyaç duydukları kadar rapor yapılandırması tanımlayabilir. Bir rapor yapılandırması, her biri ya hedeflenen veri bileşimi ya da biçime katkıda bulunan altı bölümden oluşur.

Bir maliyet denetimi çalışma alanı yapılandırmak için **Maliyet muhasebesi** \> **Kurulum** \> **Maliyet denetimi çalışma alanı** üzerine tıklayın.

### <a name="general"></a>Genel

**Genel** hızlı sekmesi üzerinde, benzersiz bir rapor biçimi oluşturabilirsiniz. Raporun adı, kullanıcıların **Maliyet denetimi** çalışma alanında tanıyabilecekleri benzersiz bir kimlik tanımlayıcı olacaktır. Raporun dahili maliyet muhasebecileri için nerede paylaşılacağını veya tutulacağını da belirtebilirsiniz.

| Alan       | Açıklama |
|-------------|-------------|
| Dosya Adı        | Biçim için benzersiz bir ad girin. |
| Açıklama | Ayrıntılı bir açıklama için girin. |
| Yayınlanmış   | Bu alanı **Evet** olarak ayarlarsanız, aşağıdaki rollerden birine atanmış bir kullanıcı raporu **Maliyet denetimi** çalışma alanında görebilir:<ul><li>Maliyet muhasebesi yöneticisi</li><li>Maliyet muhasebecisi</li><li>Maliyet muhasebe memuru</li><li>Maliyet nesnesi denetleyicisi</li></ul>Bu alanı **Hayır** olarak ayarlarsanız, yalnızca aşağıdaki rollerden birine atanmış kullanıcılar raporu **Maliyet denetimi** çalışma alanında görebilir:<ul><li>Maliyet muhasebesi yöneticisi</li><li>Maliyet muhasebecisi</li><li>Maliyet muhasebe memuru</li></ul> |

### <a name="data-filtering"></a>Veri filtreleme

**Veri filtreleme** hızlı sekmesinde, raporun veri temelini tanımlarsınız. Bu raporun kullanıcıları, kaynak verisi işlendikten sonra değerleri raporda görecektir.

| Alan                                                             | Açıklama |
|-------------------------------------------------------------------|-------------|
| Maliyet muhasebesi defteri                                            | Raporun üzerine dayandığı **Maliyet muhasebesi genel muhasebesi**. Değer **Maliyet kontrol birimi** alanında türetilmiştir. |
| Maliyet kontrolü birimi                                                 | Seçtiğiniz değer, bu raporun üzerine dayanacağı maliyet muhasebesi genel muhasebesini ve maliyet nesnelerini belirler. |
| İstatistiksel boyut hiyerarşisi, Maliyet nesnesi boyut hiyerarşisi | Bir **Maliyet denetimi** çalışma alanı yapılandırması kaydı, bir parasal olmayan veya parasal olan değerleri raporlayabilir ancak aynı biçimde değil. **Maliyet öğesi boyut hiyerarşisi** alanı içinde parasal değerleri raporlamak için bir değer seçin. **İstatistiksel boyut hiyerarşisi** alanı içinde parasal olmayan değerleri raporlamak için bir değer seçin. Seçtiğiniz boyut hiyerarşisi kaydı, raporlama ve toplama düzeylerinin yapısını belirler.<blockquote>[!NOTE]<br>Parasal olmayan ve parasal değerleri yan yana görmek için, veriyi Microsoft Power BI içerik paketi için Microsoft Excel'e aktarabilirsiniz.</blockquote> |
| Maliyet nesnesi boyut hiyerarşisi                                   | Tanımladığınız raporlama amacına uygun maliyet nesnesi boyutunun boyut hiyerarşisini seçin. |
| Orijinal bütçe sürümü                                           | Bu raporun bağlamında orijinal bütçe olarak beliren bütçe sürüm kimliğini seçin. |
| Düzeltilmiş bütçe sürümü                                            | Bu raporun bağlamında revize edilen bütçe olarak beliren bütçe sürüm kimliğini seçin. |

### <a name="assign-calculation-records"></a>Hesaplama kayıtları ata

Genel gider hesaplama, kaynak veri üzerinde çeşitli hesaplama adımlarını gerçekleştirir; örneğin maliyet davranışı sınıflandırması, maliyet dağılımı veya maliyet tahsisatı gibi. Eksik kaynak veri keşfedilirse veya kuralların güncelleştirilmesi gerekirse birden fazla genel gider hesaplaması aynı mali dönem içerisinde gerçekleştirilebilir. Her bir genel gider hesaplama benzersiz bir kimlik ile kaydedilir. Maliyet muhasebecisi, belirli bir genel gider hesaplama kimliği seçebilir. Raporun kullanıcıları, örneğin yöneticiler, genel gider hesaplamasının sonuçlarını **Maliyet denetimi** çalışma alanında görebilirler.

| Alan                  | Açıklama |
|------------------------|-------------|
| Mali takvim dönemi | Bir genel gider hesaplama kimliğinin atanacağı mali takvim dönemini seçin.<blockquote>[!NOTE]<br>Alanda listelenen mali dönemler, maliyet muhasebesi genel muhasebesi ile ilişkilendirilmiş olan mali takvimden gelir.</blockquote> |
| Gerçek sürüm         | Uygun genel gider hesaplama kimliğini seçin. |
| Bütçe sürümü         | Uygun genel gider hesaplama kimliğini seçin. |
| Düzeltilmiş bütçe sürümü | Uygun genel gider hesaplama kimliğini seçin. |

### <a name="fiscal-periods-per-column"></a>Sütuna göre mali dönemler

**Sütun başına mali dönemler** hızlı sekmesinde, maliyet muhasebecisi hangi mali dönemin rapor düzeninde gösterileceğine karar verir.

Sütunlarda seçilen değerler **Mali dönem başına sütun** hızlı sekmesi üzerinde seçilen değerlerle çarpılır.

| Alan                | Açıklama |
|----------------------|-------------|
| Geçerli dönem       | Geçerli mali dönemin bakiyesi gösterilir.<blockquote>[!NOTE]<br>Varsayılan olarak geçerli dönem, dönem tarihi tarafından belirlenir. **Maliyet denetimi** çalışma alanında, belirli bir mali dönem seçilebilir. Seçilen değer daha sonra geçerli dönemi temsil eder.</blockquote> |
| Önceki dönem      | Önceki mali dönemin bakiyesi gösterilir. Aşağıdaki formül kullanılır:<br>Geçerli mali dönem – 1<blockquote>[!NOTE]<br>Varsayılan olarak önceki dönem, oturum tarihinden türetilir. **Maliyet denetimi** çalışma alanında, belirli bir mali dönem geçerli dönem olarak seçilebilir. **Önceki dönem** daha sonra uygun şekilde yeniden hesaplanır.</blockquote> |
| Bir yıllık         | Yılbaşından bugüne tarihi gösterilir. Aşağıdaki formül kullanılır:<br>YearToDate (Geçerli mali dönem)<blockquote>[!NOTE]<br>Varsayılan olarak geçerli dönem, dönem tarihi tarafından belirlenir. **Maliyet denetimi** çalışma alanında, belirli bir mali dönem seçilebilir. Seçilen değer geçerli dönemi temsil eder ve **Yılbaşından bugüne** değeri uygun şekilde güncelleştirilir.</blockquote> |
| Sene başından bugüne ortalaması | Ortalama yılbaşından bugüne tarihi gösterilir. Aşağıdaki formül kullanılır:<br>(YearToDate [Geçerli mali dönem]) ÷ (Sayı [Geçerli mali dönem]);<p><strong>Örnek</strong></p><ul><li>**İstatistiksel boyut üyesi:** Tam zamanlı çalışanlar</li><li>**Geçerli tarih** 21-03-2017</li><li>**Dönem:** Mali dönem 1, Mali dönem 2, Mali dönem 3</li><li>**Büyüklük** 10, 10, 12</li></ul>Bu durumda **Yılbaşından bugüne ortalama** = (10 + 10 + 12) ÷ 3 = 10,67<p>**Ortalama yılbaşından bu güne** değeri maliyet nesneleri boyut üyeleri ve istatistiksel boyut üyeleri için hesaplanabilir.</p><blockquote>[!NOTE]<br>Varsayılan olarak geçerli dönem, dönem tarihi tarafından belirlenir. **Maliyet denetimi** çalışma alanında, belirli bir mali dönem seçilebilir. Seçilen değre daha sonra geçerli dönemi temsil eder ve **Yılbaşından bugüne** ve **Yılbaşından bugüne ortalama** değerleri buna uygun olarak güncelleştirilir.</blockquote> |

### <a name="columns-to-display-for-costs"></a>Maliyetler için görüntülenecek sütunlar

**Maliyetler için görüntülenecek sütunlar** hızlı sekmesinde, maliyet muhasebecisi rapor biçiminin hangi sütunları içereceğine karar verir. Üç kategori mevcuttur: Sabit maliyet, Değişken maliyet ve Sınıflandırılmamış maliyet.

| Alan                 | Açıklama |
|-----------------------|-------------|
| Sabit maliyet            | Bu sütun türü, sabit maliyeti seçilen genel gider hesaplama kimliğine dayalı olarak gösterir.<blockquote>[!NOTE]<br>Bu sütun türü, yalnızca bir genel gider hesaplama kimliği mali dönem için seçilirse bakiyeyi gösterir.</blockquote> |
| Değişken maliyet         | Bu sütun türü, değişken maliyeti seçilen genel gider hesaplama kimliğine dayalı olarak gösterir.<blockquote>[!NOTE]<br>Bu sütun türü, yalnızca bir genel gider hesaplama kimliği mali dönem için seçilirse bakiyeyi gösterir.</blockquote> |
| Sabit + değişken maliyet | Bu sütun türü, değişken ve sabit maliyeti seçilen genel gider hesaplama kimliğine dayalı olarak gösterir.<blockquote>[!NOTE]<br>Bu sütun türü, yalnızca bir genel gider hesaplama kimliği mali dönem için seçilirse bakiyeyi gösterir.</blockquote> |
| Toplam maliyet            | Bu sütun türü, toplam maliyeti gösterir (sınıflandırılmamış maliyet, sabit maliyet ve değişken maliyet).<blockquote>[!NOTE]<br>Sütun türü bakiyeyi her zaman gösterir.</blockquote> |
| Sınıflandırılmamış maliyet     | Bu sütun türü, sınıflandırılmamış maliyeti gösterir.<blockquote>[!NOTE]<br>Bu sütun, tüm maliyetlerin genel gider hesaplaması tarafından doğru şekilde sınıflandırıldığını doğrulamak için kullanılabilir veya aksi takdirde maliyet davranış kurallarının yeniden ayarlanması gerekir.</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>Bütçelenen maliyetler için görüntülenecek sütunlar

**Bütçelenmiş maliyetler için görüntülenecek sütunlar** hızlı sekmesinde, maliyet muhasebecisi hangi sütunların seçilen bütçe sürümleri için gösterileceğini karar verir. Tek tek seçimler orijinal ve revize edilmiş bütçe için yapılabilir.

> [!NOTE]
> Aşağıdaki alanlar orijinal bütçe ve revize edilmiş bütçe için aynı mantığa sahip olduklarından yalnızca bir defa açıklanacaklardır.

| Alan                     | Açıklama |
|---------------------------|-------------|
| Bütçe                    | Bütçe bakiyeleri seçilen sütun başına gösterilir.<blockquote>[!NOTE]<br>Bakiyeler, **Veri filtreleme** hızlı sekmesi üzerinde seçilmiş olan bütçe sürümlerine dayalı olarak gösterilir.</blockquote> |
| Bütçe farkı           | Bütçe ve fiili arasındaki farkı hesapla ve göster. Aşağıdaki formül kullanılır:<br>Bütçe bakiyesi – Gerçek bakiye |
| % cinsinden bütçe farkı      | Bütçe ve fiili arasındaki farkı yüzde olarak hesapla ve göster. Aşağıdaki formül kullanılır:<br>(Bütçe bakiyesi – Gerçek bakiye) ÷ Bütçe bakiyesi |
| Fark dönemi eşiği | Geçerli dönem için parasal tutardaki fark için bir eşik ayarlayın. Eşik aşılırsa, satır **Maliyet denetimi** çalışma alanında kırmızıyla vurgulanır.<blockquote>[!NOTE]<br>Bu alan yalnızca harcamaları temsil eden maliyet öğelerinde geçerlidir.</blockquote> |
| Fark yılı eşiği   | Yıl için parasal tutardaki fark için bir eşik ayarlayın. Eşik aşılırsa, satır **Maliyet denetimi** çalışma alanında kırmızıyla vurgulanır. |
| Fark eşiği %      | Fark için yüzce olarak bir eşik ayarlayın. Eşik aşılırsa, satır **Maliyet denetimi** çalışma alanında kırmızıyla vurgulanır.<blockquote>[!NOTE]<br>Aynı yüzde eşiği geçerli dönem ve yıla uygulanır.</blockquote> |

## <a name="cost-control-workspace"></a>Maliyet kontrolü çalışma alanı

**Maliyet denetimi** çalışma alanı bir web raporu olarak tasarlanmıştır. Bu nedenle, bir maliyet nesnesinden sorumlu tüm yöneticilere erişim, [Maliyet nesnesi denetimcilerine erişim hakları tanımlamak](access-rights-cost-object-controller.md) üzerinde belirtildiği şekilde verilir.

Yöneticiler gibi kullanıcılar tarafından kullanılabilen raporların listesi **Maliyet denetimi çalışma alanı yapılandırmaları** sayfasında bulunan **Yayımlanmış** seçeneği tarafından yönetilir.

![Kullanıcıların Maliyet denetimi çalışma alanında görebilecekleri bir rapor.](./media/report-cost-control.png)

Bir yönetici, görüntülenecek mali yıl dönemini seçebilir. Oturum tarihi, varsayılan geçerli dönemi belirlemek için kullanılır.

Mali takvim dönemindeki değerler, rapor adı ile **Maliyet denetimi çalışma alanı yapılandırmaları** sayfasında, maliyet muhasebesi genel muhasebe için seçilen rapor adı ve mali takvimde belirlenir.

Nesne boyutu hiyerarşisinde, kullanıcılar bakiyelerin gösterileceği toplama seviyesini seçebilirler. Düzey güvenliğin erişim vererek, kullanıcıların yalnızca erişimleri olan hiyerarşi düzeylerini görebilecekleri şekilde izinleri denetleyebilirsiniz. Bu nedenle, yalnızca erişim verilmiş oldukları toplam bakiyeleri görebilirler.

### <a name="add-or-remove-columns"></a>Sütun ekle veya kaldır

Kullanıcılar, ihtiyaçlarına uyması için rapordaki sütunları özelleştirebilirler.

### <a name="view-details"></a>Ayrıntıları görüntüle

Kullanıcılar, çalışma alanında gösterilen bakiyelerin ayrıntılarına inebilirler. Kullanıcılar bir maliyet öğesi boyut hiyerarşi düğümü seçerse ve sonra **Ayrıntıları görüntüle** üzerine tıklarlarsa, **Maliyet öğesi ayrıntıları** iletişim kutusu, düğüm için ayrıntılı bilgi gösterir.

Bir kılavuz, bir maliyet öğesi boyut hiyerarşi düğümü ile ilişkili her bir maliyet öğesini ve değerlerini gösterir. Kılavuzda beliren sütunlar, çalışma alanı ayarlarıyla eşleşir.

İki grafik, döneme göre bütçe ve bütçe farkının gerçek kıyasını gösterir.

![Döneme göre bütçe ve bütçe farkının gerçek kıyasını gösteren grafikler.](./media/cost-element-details-operations.png)

Kullanıcılar, ihtiyaç duydukları zaman giriş ayrıntılarına inmek için **Maliyet girişleri** üzerine tıklayabilirler.

![Maliyet girişleri.](./media/cost-entries.png)

Örneğin, kira, maliyet merkezlerine dağıtılmış bir harcamadır. Kendisine ait maliyet merkezinin taşımak zorunda olduğu kira maliyetini anlamak isteyen bir kullanıcı, kiranın nasıl hesaplandığını görmek için ayrıntılara gidebilir.

Kullanılar **Maliyet girişleri** sayfası üzerindeki **Tahsisat tabanı** üzerine tıklarlarsa, bir iletişim kutusu görüntülenir. Kullanıcılar daha sonra tahsisat tabanını kurala atayabilir ve dönem için kaydedilmiş olan karşılık gelen istatistiksel ölçümleri görüntüleyebilirler.

Aşağıdaki örnekte, tahsisat tabanı **Formül tahsisat tabanı** türündedir ve formül gösterilir. Formülü tanımlayan faktörler listelenir. Ek olarak, bir kılavuz, maliyet nesnesi başına yapılan hesaplamayı gösterir.

![Maliyet nesnesi başına hesaplamalar.](./media/cost-entries-allocation-base.png)

Ek kaynaklar 

[Maliyet nesnesi denetleyicilerinin erişim haklarını tanımlama](access-rights-cost-object-controller.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]