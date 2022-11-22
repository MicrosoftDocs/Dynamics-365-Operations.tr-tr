---
title: Stok Görünürlüğü Eklentisi'ne genel bakış
description: Bu makalede, Stok Görünürlüğü'nün ne olduğu açıklanmakta ve özellikleri tanımlanmaktadır.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dd790bcaada0c1a05e46b4edacaa31fc4e15be92
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762820"
---
# <a name="inventory-visibility-add-in-overview"></a>Stok Görünürlüğü Eklentisi'ne genel bakış

[!include [banner](../includes/banner.md)]

Stok Görünürlüğü Eklentisi (*Stok Görünürlüğü hizmeti* olarak da adlandırılır), tüm veri kaynaklarınız ve kanallarınızda gerçek zamanlı eldeki stok değişikliği takibi sağlayan bağımsız ve yüksek düzeyde ölçeklenebilir bir mikro hizmet sunmaktadır. Aşağıdaki listeyi içeren (ancak bununla sınırlı olmayan) işlevleri kullanarak global stoğunuzu yönetmenizi sağlayan bir platform sunar:

- Supply Chain Management veya üçüncü taraf lojistik veri kaynaklarınızı (sipariş yönetimi sistemleri, üçüncü taraf kurumsal kaynak planlama \[ERP \] sistemleri, satış noktası \[POS \] sistemleri ve ambar yönetimi sistemleri gibi) Stok Görünürlüğü hizmetine bağlayarak tüm veri kaynaklarınız, ambarlarınız ve tesislerinizde en güncel stok durumunu (eldeki, sipariş edilmiş, satın alınmış, iade edilmiş ve karantinadaki stok gibi) merkezi bir şekilde takip edin.
- Eldeki stok kullanılabilirliğini ve eksikliklerini sorgulayın ve Stok Görünürlüğü hizmetini doğrudan arayarak hemen yanıt alın.
- Özellikle talebinizin farklı kanallardan geldiği durumlarda Stok Görünürlüğü hizmetinde gerçek zamanlı geçici rezervasyonlar yaparak fazla satış yapmaktan kaçının.
- Çok kanallı karşılanabilir miktar (KM) özelliğinin beklenen sipariş karşılama tarihlerini hesaplayabilmesi için doğru mevcut veya sonraki uygun tarihleri sağlayarak taahhüt edilen siparişleri ve müşteri beklentilerini daha iyi yönetin.

## <a name="extensibility"></a>Genişletilebilirlik

Veri giriş ve çıkışının Microsoft uygulamalarıyla sınırlı olmaması nedeniyle Stok Görünürlüğü hizmeti oldukça genişletilebilirdir. Harici sistemler, RESTful uygulama programlama arabirimleri (API) yoluyla hizmete erişebilir. Supply Chain Management veri kaynağı ve boyutları için sağlanan hazır eşlemelerin kullanımına ek olarak, yapılandırma uygulaması yoluyla ek veri kaynakları, stok durumu ölçüleri (Stok Görünürlüğü hizmetinde *fiziksel ölçüler* şeklinde adlandırılır) ve stok boyutları ayarlayarak Stok Görünürlüğünü çeşitli üçüncü taraf sistemler ile tümleştirebilirsiniz. Bu şekilde, birden çok veri kaynağınızı ve önceden tanımlanmış stok boyutlarını esnek bir şekilde sorgulayabilir ve değiştirebilirsiniz.

Ayrıca, Stok Görünürlüğünün Microsoft Dataverse üzerinde yerleşik olması nedeniyle verileri, Power Apps ile derlemek ve tümleştirmek için kullanılabilir. İş gereksinimlerinizi karşılayan özelleştirilmiş panolar oluşturmak için Power BI'ı da kullanabilirsiniz.

## <a name="scalability"></a>Ölçeklenebilirlik

Veri hacminize bağlı olarak Stok Görünürlüğü hizmeti yukarı veya aşağı yönde ölçeklendirilebilir. Ölçeklenebilirlik deneyimi çoğunlukla sorunsuz olup hareket verilerinizin hacminin otomatik tespiti ve değerlendirmesine dayanarak Microsoft platform ekibi tarafından yürütülür.

Aşağıdaki örnekte Stok Görünürlüğü mimarisi gösterilmektedir.

[<img src="media/inventory-visibility-architecture.png" alt="Inventory Visibility architecture." title="Stok Görünürlüğü mimarisi" width="720" />](media/inventory-visibility-architecture.png)

## <a name="feature-highlights"></a>Özellikle ilgili önemli noktalar

### <a name="get-a-global-view-of-real-time-inventory"></a>Gerçek zamanlı stoğun küresel görünümünü alın

Stok Görünürlüğü tüm kanal, konum ve ambarlarınızda her zaman en güncel stok miktarlarına erişmenizi sağlar. Stok kayıtlarını edinmeniz gerektiğinde günlük operasyonel işlerinizi desteklemek için kullanarak büyük fayda elde edebilirsiniz. Eldeki fiziksel stok, satılan miktarlar ve satın alınan miktarların hepsi kullanıma hazırdır. İlgili ayrıntıları gerçek zamanlı şekilde elde etmek için gereksinim duyduğunuz diğer fiziksel envanter ölçümlerini (iade, karantinaya alınan ve deftere nakledilen veriler) de tümleştirebilirsiniz. Stok Görünürlüğü, milyonlarca stok gönderisini naklini verimli bir şekilde işleyebilir. Bu veriler toplanır ve verilerin gönderildiği aralığa bağlı olarak hizmette bulunan son stok miktarlarına anında, saniyelik veya dakikalık olarak yansıtılabilir. Daha fazla bilgi için bkz. [Stok Görünürlüğü genel API'leri](inventory-visibility-api.md).

### <a name="central-inventory-adjustment"></a>Merkezi stok düzeltmesi

Stok Görünürlüğü, harici sistemlerin stok değişikliklerini deftere nakletmek için kendi API'sini çağırmasına olanak tanır. Değişiklikler hemen stok görünürlüğünde etkili olur. Böylece eldeki stok anında azaltılır.

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Fazla satışın önlenmesi adına tüm sipariş kanallarında geçici rezervasyon

*Geçici rezervasyon*, bir sipariş veya talebin karşılanması için belirli miktarları atamanıza veya bayrakla işaretlemenize olanak tanır. Geçici rezervasyon, fiziksel stoğu etkilememekle birlikte *rezervasyon için kullanılabilir* olan stok miktarından düşülür ve gelecekteki siparişlerin karşılanması için güncel miktarı gösterir. Bu özellik, satış taleplerinin veya siparişlerin kayıt sisteminin kurumsal kaynak planlama (ERP) sisteminizin dışındaki bir ya da birden fazla kanal veya veri kaynağından işletmenize gelmesi durumunda faydalı olacaktır.

Stok Görünürlüğü hizmetinde geçici rezervasyon kullanmamanız halinde fiziksel stok miktarının güncelleştirilmesi için siparişinizin ERP sisteminizle eşitlenmesi ve bu sistem tarafından işlenmesini beklemeniz gerekir. Bu işlemin gecikme süresi genellikle çok uzundur. Ancak geçici rezervasyonlar, satış kanallarınızda bir satış talebi veya sipariş oluşturulduğunda hemen uygulanır. Bu nedenle, çok kanallı siparişlerinizin ERP sistemine ulaştığında birbirine karışmamasını sağlayarak fazla satış durumlarının önlenmesine yardımcı olur. Geçici rezervasyonlar, taahhüt etmiş olduğunuz tüm siparişlerin karşılanmasını da sağlar. Bu nedenle, müşteri beklentilerini karşılamanıza ve müşteri bağlılığını sürdürmenize yardımcı olur. Daha fazla bilgi için bkz. [Stok Görünürlüğü rezervasyonları](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-quantity-and-dates"></a>KM miktar ve tarihi için anında yanıt

Yakın gelecekteki tahmini stoğunuza yönelik görünürlük (arz, talep ve tahmini eldeki stok detayları dahil) önemlidir ve şirketinizin aşağıdaki hedeflere erişmesine yardımcı olur:

- Stok yönetim maliyetlerini azaltmak için stok düzeylerini en aza indirin.
- Satış temsilcilerinin, sipariş edilen ürünlerin kullanılabilirliğine göre gönderi ve teslim tarihlerini hesaplayabilmesi için dahili sipariş işleme sürecini kolaylaştırın.
- Sonraki kullanılabilir tarih bilgisini sağlayarak stokta olmayan bir ürünün ne zaman kullanılabilir olacağı ile ilgili müşterilere şeffaflık sağlayın.

KM özelliği, günlük sipariş karşılama sürecinize kolaylıkla dahil edilebilir. En önemlisi, diğer Stok Görünürlüğü teklifleri gibi KM özelliği de *global ve gerçek zamanlıdır*. Bu nedenle, tüm iş kanallarınızı ve veri kaynaklarınızı kapsayan tam stok kullanılabilirlik sorgusu yapabilmek için birden çok KM hesaplama formülü ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Stok Görünürlüğü eldeki değişiklik zamanlamaları ve karşılanabilir miktarı](inventory-visibility-available-to-promise.md).

### <a name="preallocate-your-stock-to-important-channels-or-customers-with-inventory-allocation"></a>Stoğu, önemli kanallara veya müşterilere Stok Tahsisatı ile önceden tahsis etme

Stok Görünürülüğü tahsisat özelliği önemli kanallar, müşteri grupları veya yerleşimler için değerli eldeki stoğu korumanızı ve sınırlamanızı sağlar. Stok tahsisat edildikten sonra, stok tüketimi tahsis edilen havuza göre sınırlandırılır ve havuzda kalan miktarlar tüketim için halen kullanılabilir olan miktarı yansıtmak üzere gerçek zamanlı olarak eksiltilir. Daha fazla bilgi için bkz. [Stok Görünürlüğü stok tahsisatı](inventory-visibility-allocation.md).

### <a name="compatibility-with-wms-items"></a>WMS maddeleriyle uyumluluk

Microsoft, WMS müşterilerinin de Stok Görünürlüğü hizmetinden faydalanması için ambar yönetimi süreçleri (WMS) ile hazır tümleştirme sağlamayı amaçlamaktadır. 2022 1. Dalga'nın yayımlanması (genel önizlemesi Mart ayında) ile stok hizmeti, WMS eldeki stok sorgularını ve KM'yi destekler. Geçici rezervasyon ve tahsisat özelliği, WMS müşterileri için bir sonraki dalgada desteklenecektir. Daha fazla bilgi için bkz. [WMS öğeleri için Stok Görünürlüğü desteği](inventory-visibility-whs-support.md).

Aşağıdaki şekil varolan özelliklerin üst düzey özetini ve bunların veri akışında nasıl konumlandırılacağını gösterir.

[<img src="media/inventory-visibility-feature-overview.png" alt="Inventory Visibility feature overview." title="Stok Görünürlüğü özelliğine genel bakış" width="720" />](media/inventory-visibility-feature-overview.png)

## <a name="licensing"></a>Lisans

Stok Görünürlüğü hizmeti aşağıdaki sürümlerde kullanılabilir:

- **Microsoft Dynamics 365 Supply Chain Management** için Stok Görünürlüğü Eklentisi - Geçerli bir Supply Chain Management lisansı bulunan şirketler için Stok Görünürlüğü ek bir ücret ödenmesine gerek kalmadan kullanılabilir. Stok Görünürlüğü Microsoft Power Platform'u temel aldığından, Microsoft Power Platform depolama kapasitesi ve API sınırlarına tabidir. Supply Chain Management lisansınız varsayılan depolama ve API kapasitesini içermelidir. Daha fazla depolama ve API kapasitesi istiyorsanız, profesyonel bir lisans satın alabilirsiniz. Varsayılan API tahsisatı ve profesyonel lisans hakkında ayrıntılı bilgi için, bkz: [İstek sınırları ve tahsisatları](/power-platform/admin/api-request-limits-allocations) ve [Microsoft Power Platform için Lisanslamaya genel bakış](/power-platform/admin/pricing-billing-skus). Varsayılan depolama ve API tahsisatları ile hemen Stok Görünürlüğü eklentisini kullanmaya başlayabilirsiniz. Yükleme ayrıntıları için bkz. [Stok Görünürlüğü'nü yükleme ve ayarlama](inventory-visibility-setup.md). Tahmini API ve depolama kullanımınız standart tahsisatı aşarsa, satış temsilcinizle iletişime geçebilir ve özel durum için platform ekibiyle bağlantı kurmalarını isteyebilirsiniz.
- **IOM bileşeni olarak Stok Görünürlüğü Hizmeti** – Bu sürüm, Intelligent Order Management (IOM) müşterileri ve ERP sistemi olarak Supply Chain Management kullanmayan şirketlere yöneliktir. Lisans, Intelligent Order Management ürün demetine dahildir. Daha fazla bilgi için bkz. [Intelligent Order Management'a genel bakış](/dynamics365/intelligent-order-management/overview).

## <a name="inventory-visibility-terminology"></a>Stok Görünürlüğü terminolojisi

Stok Görünürlüğü eklentisi ile çalışırken aşağıdaki kavramları ve koşulları anlamanız önemlidir:

- **Veri kaynağı** - Verilerinizin geldiği sistemi temsil eden veri kaynağı.
- **Boyutlar** – Boyutlar ürün özelliklerini tanımlar. Bunlar depolama boyutları (tesis veya ambar gibi) veya ürün boyutları (renk, boyut veya stil gibi) olabilir.
- **Fiziksel ölçüler** – Fiziksel ölçüler eldeki, satın alınan, sipariş edilen veya satılan gibi farklı stok durumlarını ölçen miktarlardır.
- **Hesaplanan ölçüler** – Hesaplanan ölçüler bir fiziksel ölçüler kümesinden hesaplanan nicelik ölçümleridir. Örneğin, *kullanılabilir toplam* hesaplanan ölçümü, *Eldeki* + *Satın alınan* – *Siparişteki* - *Satılan* olarak hesaplanır.
- **Bölüm** – Bölüm, stok görünürlüğünün alınan verileri nasıl dağıtabileceğini belirten bir hiyerarşi tanımlar. Şu anda varsayılan bölüm tesis ve yerleşimdir.
- **Dizin hiyerarşisi** – Dizin hiyerarşisi, stoğu nasıl sorgulamak ve daha çok ayrıntı düzeyi olan sonuçları elde etmek istediğinizi ayrıntılı olarak tanımlar.

Bu terimler ve kavramlar hakkında daha fazla bilgi için bkz. [Stok Görünürlüğü yapılandırma](inventory-visibility-configuration.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
