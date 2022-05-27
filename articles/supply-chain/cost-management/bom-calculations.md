---
title: BOM hesaplamaları
description: Maliyet toplaması ve satış fiyatı hesaplamaları, ürün reçetesi (BOM) hesaplamaları olarak bilinir ve onları Hesaplamalar sayfasından başlatırsınız. Bu konu, BOM hesaplamaları hakkında bilgiler sağlar.
author: JennySong-SH
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice, ProdSetupCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 0a71a17efbca3945c5a1010cf7d523a85420e8e2
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674603"
---
# <a name="bom-calculations"></a>BOM hesaplamaları

[!include [banner](../includes/banner.md)]

Maliyet toplaması ve satış fiyatı hesaplamaları, ürün reçetesi (BOM) hesaplamaları olarak bilinir ve onları Hesaplamalar sayfasından başlatırsınız. Bu konu, BOM hesaplamaları hakkında bilgiler sağlar.

Maliyet toplaması ve satış fiyatı hesaplamaları, ürün reçetesi (BOM) hesaplamaları olarak bilinir ve onları **Hesaplamalar** sayfasından başlatırsınız. Aşağıdaki görevleri gerçekleştirmek için **Hesaplamalar** sayfasını kullanın:

-   Üretilmiş bir maddenin maliyetini hesaplamak ve maliyetlendirme versiyonu içerisinde ilişkili bir madde maliyet kaydı oluşturmak.
-   Üretilmiş bir maddenin satış fiyatını hesaplayın ve bir maliyetlendirme versiyonu içerisinde ilişkili bir madde satış fiyatı kaydı oluşturun.

**Hesaplamalar** sayfasını kullanma şekliniz, ürün reçetesi hesaplamalarını nasıl başlattığınıza göre bir miktar değişiklik gösterebilir. **Hesaplamalar** sayfasını nasıl kullandığınız ayrıca, ürün reçetesi hesaplamalarının standart maliyetlerin mi yoksa planlanan maliyetlerin mi maliyetlendirme versiyonuna ve ürün reçetesi hesaplamalarında kullanılan maliyetlendirme versiyonu içerisinde tanımlanan birçok ilkeye bağlıdır. **Not:** **Hesaplamalar** sayfasının bir varyasyonu satış siparişi, satış teklifi veya servis siparişi satırı maddesi bağlamında kullanılır. Bu hesaplamalar, siparişe özel ürün reçetesi hesaplamaları olarak da bilinir. Siparişe özel ürün bir reçetesi hesaplaması maliyet versiyonunda bir madde maliyet kaydı oluşturmaz. Bunun yerine, **Ürün reçetesi hesaplama ayrıntıları** sayfası üzerinde görünen bir hesaplama kaydı oluşturur. Hesaplama kaydı hesaplanan bir maliyet ve hesaplanan bir satış fiyatı içerir. **Hesaplamalar** sayfası, tek bir üretilen ürün için veya bir maliyetlendirme sürümü için açılabilir:

-   Tek bir üretilen maddenin maliyetlerini hesaplamak için ürün reçetesi hesaplamalarını **Madde fiyatı** sayfasından başlatırsınız. **Hesaplamalar** sayfası, madde tanımlayıcısını devralır. Maliyetlendirme sürümü, ürün reçetesi sürümü, rota sürümü, hesaplama miktarı, hesaplama tarihi ve tesisin belirtilmesi gerekir.
    -   Varsayılan olarak, ürün reçetesi sürümü ve rota sürümü, maddenin, tesisin, tarihin ve hesaplama miktarının etkin sürümlerine ayarlanır. Ancak, varsayılan değerleri, onaylanan sürümlerle devre dışı bırakabilirsiniz.
    -   Varsayılan olarak, hesaplama miktarı maddenin standart sipariş miktarına ayarlanır. Ancak, varsayılan değeri geçersiz kılabilirsiniz.
    -   Hesaplama tarihi ve tesisi maliyetlendirme sürümü tarafından zorunlu kılınabilir veya kullanıcı tarafından belirtilen değerler, tarih veya tesis maliyetlendirme sürümü tarafından zorunlu kılınmazsa ayarlanabilir. İleriki bir hesaplama tarihi, bekleyen maliyet kayıtlarının nasıl kullanıldığını belirler. Ürün reçetesi hesaplamaları, en yakın başlangıç tarihine sahip veya hesaplama tarihinden önceki bir bekleyen maliyet kaydını kullanır.
-   Tüm üretilen maddeler veya seçilen maddeler için maliyetleri hesaplamak veya nerede kullanıldığına dayanarak maddeleri güncelleştirmek için, ürün reçetesi hesaplamalarını **Maliyet sürümü kurulumu** sayfasından veya **Maliyet sürümü bakımı** sayfasından başlatırsınız. **Hesaplamalar** sayfası, maliyetlendirme sürümünü devralır.
    -   Üretilmiş bir bileşen belirli bir alt ürün reçetesi veya alt rota içermediği sürece, hesaplamalar için üretilmiş bir madde için etkin ürün reçetesi versiyonu ve rota versiyonunun (ve ilgili tesis, tarih ve miktar) kullanıldığını varsayılır.
    -   Hesaplamalar için, standart sipariş miktarının üretilen maddeler için kullanıldığı varsayılır. Standart sipariş miktarı, bileşen miktarlarının hesaplanması, ilgili ürün reçeteleri ve rota sürümlerinin belirlenmesi (miktara dayalı hassas ürün reçeteleri ve rotaları kullandığınızda) ve sabit maliyetlerin itfasının gerekli temeli sağlar. Ancak, miktarlar belirtilen hesaplama miktarını yansıtacağından, üretilmiş bir bileşen, **Üretim** veya **Satıcı** tipinde bir ürün reçetesine sahip olduğunda ya da ürün reçetesi hesaplamaları için siparişe göre üretim açılım modu kullandığınızda, bu varsayım geçerli olmaz.
    -   Hesaplama tarihi ve tesisi maliyetlendirme sürümü tarafından zorunlu kılınabilir veya kullanıcı tarafından belirtilen değerler, tarih veya tesis maliyetlendirme sürümü tarafından zorunlu kılınmazsa ayarlanabilir.

Ürün reçetesi hesaplamasındaki değer farklılıklar, maliyetlendirme türü ve maliyetlendirme sürümünü kısıtlamalarını yansıtır:

-   Standart maliyetleri kullanan ürün reçetesi hesaplamaları, maliyetlendirme sürümü ilkeleri tarafından sınırlandırılmalıdır çünkü sınırlamalar, standart maliyetlendirme ilkelerinin kullanılmasını garanti eder. Standart maliyetlendirme ilkeleri, satınalınan maddelere ait standart maliyetler ile tek düzeyli bir açılım modunun kullanımı ve sair giderlerin birim maliyetlere dahil edilmesi hakkındaki kısıtlamaların uygulanmasını gerektirir.
-   Planlanan maliyetleri kullanan ürün reçetesi hesaplamaları, standart maliyetlendirme ilkelerini uygulamasını gerektirmez. Bu ürün reçetesi hesaplamaları; farklı açılım modları, satınalınan maddelere yönelik olarak alternatif maliyet verisi kaynakları ve maliyetlendirme versiyonu içersinde isteğe bağlı kısıtlama uygulamaları kullanabilir.

### <a name="bom-calculations-that-use-standard-costs"></a>Standart maliyetleri kullanan ürün reçetesi hesaplamaları

Maliyetlendirme versiyonu (standart maliyetler için) içersindeki ilkeler, beş ürün reçetesi hesaplama ilkesinin uygulama emrini verebilir. Maliyetlendirme sürümü içerisindeki **Kayıt kısıtlaması** seçeneği, sair giderlerin birim fiyatına dahil edildiği bu ilkelerden birini zorunlu kılar. Satınalınan maddelere ait sair giderler el ile girilebilirken, üretilmiş maddelerin sair giderleri sabit maliyetlerin hesaplanan itfasını yansıtır. Maliyetlendirme versiyonu içerisindeki **Hesaplama kısıtlama** seçeneği, diğer dört ürün reçetesi hesaplama ilkesi için emir verir:

-   Satınalınan maddeler için maliyet katkıları, standart maliyetlere dayandırılmalıdır. Başka bir deyişle, ürün reçetesi hesaplamaları, belirtilen maliyetlendirme versiyonu içersindeki ya da standart maliyetleri içeren geri dönüş içersindeki madde maliyeti kayıtlarını kullanmalıdır.
-   Standart maliyetlerin doğru ve tutarlı hesaplandığından emin olunması için, açılım modu tek düzeyli olmalıdır.
-   Maddelerin satış fiyatı hesaplandığında tutarlı sonuçları garanti etmeye yardımcı olmak için kar ayarı zorunlu olmalıdır. Sadece maliyetlendirme sürümü satış fiyatları içeriğine izin verdiğinde kar ayarı kullanılabilir ve madde satış fiyatı kayıtları oluşturulabilir.
-   Geri dönüş ilkesi zorunlu olmalıdır ve **Yok**, **Etkin** (etkin maliyet kayıtları için) veya **Maliyetlendirme sürümü** (belirli bir maliyetlendirme sürümü için) ayarlanabilir.

### <a name="bom-calculations-that-use-planned-costs"></a>Planlanan maliyetleri kullanan ürün reçetesi hesaplamaları

Maliyetlendirme versiyonu (planlanan maliyetler için) içerisindeki ilkeler, beş ürün reçetesi hesaplama ilkesinin uygulama emrini isteğe bağlı olarak verebilir. Alternatif olarak, ilkeler yalnızca varsayılan değerleri sağlar. Maliyetlendirme versiyonu içeresindeki **Kayıt kısıtlama** seçeneği, sair giderlere ilişkin ürün reçetesi hesaplama ilkesinin emir olarak mı verileceğini yoksa varsayılan bir değer gibi mi davranacağını belirler. Sair giderler birim fiyata isteğe bağlı olarak dahil edilebilir. Maliyetlendirme versiyonu içeresindeki **Hesaplama kısıtlama** seçeneği, diğer dört ürün reçetesi hesaplama ilkesinin emir olarak mı verileceğini yoksa varsayılan değerler gibi mi davranacaklarını belirler:

-   Satın alınan bir madde için maliyet katkılarının kaynağı, bir maliyetlendirme sürümü içindeki madde maliyet kayıtları olabilir. Alternatif olarak, kaynak maddeye atanan ürün reçetesi hesaplama grubuna göre tanımlanabilir. Örneğin, ürün reçetesi hesaplama grubu, maliyet katkısı verileri olarak satınalma fiyatı ticari anlaşmalarını tanımlayabilir.
-   Açılım modu tek düzeyli, çok düzeyli veya siparişe göre üretimden biri olabilir veya ürün reçetesi satırına dayanıyor olabilir. Ürün reçetesi satırının tipine ait açılım modu, üretim emri tahminlerinin maliyet hesaplama mantığını tekrarlar.
-   Kar ayarı emir olarak verilebilir veya varsayılan bir değer olabilir. Sadece maliyetlendirme sürümü satış fiyatları içeriğine izin verdiğinde kar ayarı kullanılabilir ve madde satış fiyatı kayıtları oluşturulabilir.
-   Geri dönüş ilkesi emir olarak verilebilir veya varsayılan bir değer olabilir. Geri dönüş ilkesi **Yok**, **Etkin** (etkin maliyet kayıtları için) veya **Maliyetlendirme sürümü** (belirli bir maliyetlendirme sürümü için) olarak ayarlanabilir.

Ürün reçetesi hesaplaması, uyarı iletileri ve diğer ileti tiplerini oluşturabilir. İletilerin tipini birden fazla ürün reçetesi hesaplama ilkesi belirler. Uyarı koşulları, maddelere atanmış olan ürün reçetesi grubunda tanımlanmıştır. Ancak, bir ürün reçetesi hesaplaması başlattığınızda bu uyarı koşullarını geçersiz kılabilirsiniz. Geri dönüş ilkesi kullanıldığında, geri dönüş bir bilgi iletisi olarak gösterilirse bu çoğu zaman yararlıdır. Kayıp maliyet katırlarına sahip maddeler için hesaplanan maliyetleri güncelleştirmeye çalışırken, bilgi iletisi, güncelleştirilmeyen maddeleri de tanımlarsa bu faydalı olur.

## <a name="bom-calculations-that-use-the-fallback-principle"></a>Geri dönüş ilkesini kullanan ürün reçetesi hesaplamaları
Aşağıdaki durumlar geri dönüş ilkesinin iki kullanımını gösterir:

-   **Standart maliyet güncelleştirmelerine iki versiyonlu yaklaşım** − Bir maliyet sürümü, standart maliyetlerdeki artımlı değişiklikleri içerebilir (örneğin yenide maddeleri veya maliyet değişikliklerini temsil eden beklemedeki maliyetler). Bu durumda geri dönüş ilkesi, diğer maliyet versiyonlarının içerisindeki etkin standart maliyetlerin kullanımını tanımlayabilir.
-   **Planlanan maliyetler tarafından maliyet değişikliklerinin etkisinin simülasyonu** - Planlanmış maliyetler için bir maliyetlendirme sürümü, simülasyon amaçları için artımlı değişiklikler içerebilir. Bu maliyetlendirme sürümü, maddelerde, maliyet kategorilerinde ve dolaylı maliyetler için hesaplama formüllerinde gerçekleşen maliyet değişikliklerinin simüle edilmiş bekleyen maliyet kayıtlarını içerecektir. Bu durumda geri dönüş ilkesi, diğer maliyet versiyonlarının içerisindeki etkin standart maliyetlerin kullanımını tanımlayabilir.

## <a name="bom-calculation-of-a-suggested-sales-price"></a>Önerilen bir satış fiyatının ürün reçetesini hesaplama
Maliyet artı kar marjı yaklaşımı kullandığınızda, bir maddenin hesaplanan satış fiyatı, ürün reçetesi hesaplaması için belirtilen kar ayarı yüzdelerini ve maddenin bileşen maddeleriyle ilişkili maliyetleri, rota operasyonlarını ve uygulanabilir üretim genel giderlerini yansıtacaktır. Kar marjı, maliyet gruplarına atanan kar ayarı yüzdesini ve maddelere, rota operasyonları için maliyet kategorilerine ve üretim genel giderleri için dolaylı maliyet hesaplama formüllerine atanan maliyet gruplarını yansıtır. Kar ayarı yüzdelerinin ayarlaması **Standart**, **Kar 1**, **Kar 2** ve **Kar 3** olarak etiketlenmiştir. Örneğin Kar 1 kümesi içerisinde, yüzde 50'lik bir kar ayarı yüzdesi, satın alınan malzemeye atanmış olan bir maliyet grubu için tanımlanabilir ve yüzde 80'lik bir kar ayarı yüzdesi, rota operasyonları için maliyet kategorilerine atanmış bir maliyet grubu için tanımlanabilir. Ürün reçetesinin bağlamı, hesaplanan bir satış fiyatının sonuçlarının nasıl ele alındığını belirler:

-   **Bir madde için geçerli ürün reçetesi hesaplaması ve belirtilen maliyetlendirme sürümü** − Ürün reçetesi, maliyetlendirme versiyonu içeresinde bekleyen bir satış fiyatı kaydı oluşturur. Bu satış fiyatı kaydı, hesaplama ayrıntılarının görüntülenmesi için bir başlangıç noktası sağlar (örneğin **Madde maliyetini hesapla** sayfasında). Satış fiyatı kaydı öncelikli olarak başvuru bilgileri olarak kullanılır ve satış siparişlerindeki bir satış fiyatı için temel olarak kullanılamazlar.
-   **Siparişe özel ürün reçetesi hesaplaması** − **Ürün reçetesi hesaplama** sayfasının değişik bir şekli satış siparişi, satış teklifi veya servis siparişi satırı maddesi bağlamında kullanılır. Bir siparişe özel ürün reçetesi hesaplaması bir maliyetlendirme versiyonu dahilinde bir kayıt oluşturmamaktadır. Bunun yerine, **Ürün reçetesi hesaplama sonuçları** sayfası üzerinde görünen bir hesaplama kaydı oluşturur. Bu hesaplama kaydı, hesaplama ayrıntılarının görüntülenmesi için bir başlangıç noktası sağlar (örneğin **Madde maliyetini hesapla** sayfasında). Seçilen bir hesaplama kaydı hakkında bilgi, kaynak satır maddesine aktarılabilir. Örneğin, hesaplanan satış fiyatı, bir satış sipariş satırı maddesine aktarılabilir.

## <a name="order-specific-bom-calculations"></a>Siparişe özel ürün reçetesi hesaplamaları
Siparişe özel bir ürün reçetesi hesaplaması, ürün reçetesi hesaplamasının üretilen bir maddeye ilişkin değişimini temsil eder. Siparişe özel ürün reçetesi hesaplaması bir satış siparişi, satış teklifi veya servis sipariş satırı maddesi bağlamında gerçekleştirilir. Siparişe özel ürün reçetesi hesaplaması, **Ürün reçetesi hesaplama** sayfasında görünen bir hesaplama kaydı oluşturur. Hesaplama kaydı hesaplanmış bir ağırlık, etkin maliyet kayıtlarını temel alan hesaplanmış bir maliyet ve hesaplanmış bir satış fiyatı içerir. Bir madde için her siparişe özel ürün reçetesi hesaplamasının **Ürün reçetesi sonuçları** sayfasında oluşturduğu hesaplama kaydı, bir hesaplama numarası ile benzersiz şekilde tanımlanır. Bir hesaplama kaydının sonuçları, isteğe bağlı olarak kaynak satır maddesine transfer edilebilir. Siparişe özel ürün reçetesi hesaplaması, üretilen bir maddenin ürün reçetesi hesaplamasından iki şekilde farklıdır:

-   Siparişe özel ürün bir reçetesi hesaplaması maliyet versiyonunda bir madde maliyet kaydı oluşturmaz. Bu nedenle, ürün reçetesi hesaplama ilkeleri, bir madde maliyet kaydı oluşturulduğunda veya bir maliyet kaydı geçersiz kılında yazıldığında uygulanmaz.
-   Bir siparişe özel ürün reçetesi hesaplaması bileşenler, maliyet kategorileri ve dolaylı maliyet hesaplama formülleri için her zaman etkin maliyet kayıtlarını kullanır.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]