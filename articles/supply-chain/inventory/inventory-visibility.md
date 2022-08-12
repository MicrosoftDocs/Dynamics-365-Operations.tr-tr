---
title: Stok Görünürlüğü Eklentisi'ne genel bakış
description: Bu makalede, Stok Görünürlüğü'nün ne olduğu açıklanmakta ve özellikleri tanımlanmaktadır.
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 274f9b368a6074725d1938de5f2172d2810a5985
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066655"
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

## <a name="feature-highlights"></a>Özellikle ilgili önemli noktalar

### <a name="get-a-global-view-of-real-time-inventory"></a>Gerçek zamanlı stoğun küresel görünümünü alın

Stok Görünürlüğü tüm kanal, konum ve ambarlarınızda her zaman en güncel stok miktarlarına erişmenizi sağlar. Stok kayıtlarını edinmeniz gerektiğinde günlük operasyonel işlerinizi desteklemek için kullanarak büyük fayda elde edebilirsiniz. Eldeki fiziksel stok, satılan miktarlar ve satın alınan miktarların hepsi kullanıma hazırdır. İlgili ayrıntıları gerçek zamanlı şekilde elde etmek için gereksinim duyduğunuz diğer fiziksel envanter ölçümlerini (iade, karantinaya alınan ve deftere nakledilen veriler) de tümleştirebilirsiniz. Stok Görünürlüğü, milyonlarca stok gönderisini naklini verimli bir şekilde işleyebilir. Bu veriler toplanır ve verilerin gönderildiği aralığa bağlı olarak hizmette bulunan son stok miktarlarına anında, saniyelik veya dakikalık olarak yansıtılabilir. Daha fazla bilgi için bkz. [Stok Görünürlüğü genel API'leri](inventory-visibility-api.md).

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Fazla satışın önlenmesi adına tüm sipariş kanallarında geçici rezervasyon

*Geçici rezervasyon*, bir sipariş veya talebin karşılanması için belirli miktarları atamanıza veya bayrakla işaretlemenize olanak tanır. Geçici rezervasyon, fiziksel stoğu etkilememekle birlikte *rezervasyon için kullanılabilir* olan stok miktarından düşülür ve gelecekteki siparişlerin karşılanması için güncel miktarı gösterir. Bu özellik, satış taleplerinin veya siparişlerin kayıt sisteminin kurumsal kaynak planlama (ERP) sisteminizin dışındaki bir ya da birden fazla kanal veya veri kaynağından işletmenize gelmesi durumunda faydalı olacaktır.

Stok Görünürlüğü hizmetinde geçici rezervasyon kullanmamanız halinde fiziksel stok miktarının güncelleştirilmesi için siparişinizin ERP sisteminizle eşitlenmesi ve bu sistem tarafından işlenmesini beklemeniz gerekir. Bu işlemin gecikme süresi genellikle çok uzundur. Ancak geçici rezervasyonlar, satış kanallarınızda bir satış talebi veya sipariş oluşturulduğunda hemen uygulanır. Bu nedenle, çok kanallı siparişlerinizin ERP sistemine ulaştığında birbirine karışmamasını sağlayarak fazla satış durumlarının önlenmesine yardımcı olur. Geçici rezervasyonlar, taahhüt etmiş olduğunuz tüm siparişlerin karşılanmasını da sağlar. Bu nedenle, müşteri beklentilerini karşılamanıza ve müşteri bağlılığını sürdürmenize yardımcı olur. Daha fazla bilgi için bkz. [Stok Görünürlüğü rezervasyonları](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-dates-confirmation"></a>KM tarih onayıyla ilgili anında yanıt

Yakın gelecekteki tahmini stoğunuza yönelik görünürlük (arz, talep ve tahmini eldeki stok detayları dahil) önemlidir ve şirketinizin aşağıdaki hedeflere erişmesine yardımcı olur:

- Stok yönetim maliyetlerini azaltmak için stok düzeylerini en aza indirin.
- Satış temsilcilerinin, sipariş edilen ürünlerin kullanılabilirliğine göre gönderi ve teslim tarihlerini hesaplayabilmesi için dahili sipariş işleme sürecini kolaylaştırın.
- Sonraki kullanılabilir tarih bilgisini sağlayarak stokta olmayan bir ürünün ne zaman kullanılabilir olacağı ile ilgili müşterilere şeffaflık sağlayın.

KM özelliği, günlük sipariş karşılama sürecinize kolaylıkla dahil edilebilir. En önemlisi, diğer Stok Görünürlüğü teklifleri gibi KM özelliği de *global ve gerçek zamanlıdır*. Bu nedenle, tüm iş kanallarınızı ve veri kaynaklarınızı kapsayan tam stok kullanılabilirlik sorgusu yapabilmek için birden çok KM hesaplama formülü ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Stok Görünürlüğü eldeki değişiklik zamanlamaları ve karşılanabilir miktarı](inventory-visibility-available-to-promise.md).

### <a name="compatibility-with-warehouse-management-processes-wms-items"></a>Ambar yönetimi süreçleri (WMS) öğeleriyle uyumluluk

Microsoft, WMS müşterilerinin de Stok Görünürlüğü hizmetinden faydalanması için ambar yönetimi süreçleri (WMS) ile hazır tümleştirme sağlamayı amaçlamaktadır. 2022 1. Dalga'nın yayımlanması (genel önizlemesi Mart ayında) ile stok hizmeti, WMS eldeki stok sorgularını ve KM'yi destekler. Geçici rezervasyon ve tahsisat özelliği, WMS müşterileri için bir sonraki dalgada desteklenecektir. Daha fazla bilgi için bkz. [WMS öğeleri için Stok Görünürlüğü desteği](inventory-visibility-whs-support.md).

## <a name="licensing"></a>Lisans

Stok Görünürlüğü hizmeti aşağıdaki sürümlerde kullanılabilir:

- **Microsoft Dynamics 365 Supply Chain Management** için Stok Görünürlüğü Eklentisi - Geçerli bir Supply Chain Management lisansı bulunan şirketler için Stok Görünürlüğü ek bir lisans ücreti ödenmesine gerek kalmadan kullanılabilir. Hemen deneyebilirsiniz. Yükleme ayrıntıları için bkz. [Stok Görünürlüğü'nü yükleme ve ayarlama](inventory-visibility-setup.md).
- **IOM bileşeni olarak Stok Görünürlüğü Hizmeti** – Bu sürüm, Intelligent Order Management (IOM) müşterileri ve ERP sistemi olarak Supply Chain Management kullanmayan şirketlere yöneliktir. Lisans, IOM ürün demetinde bulunmaktadır. Daha fazla bilgi için bkz. [Intelligent Order Management'a genel bakış](/dynamics365/intelligent-order-management/overview).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
