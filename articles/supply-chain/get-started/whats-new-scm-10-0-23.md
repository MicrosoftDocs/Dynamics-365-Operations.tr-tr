---
title: Dynamics 365 Supply Chain Management 10.0.23 sürümündeki yenilikler veya değişiklikler (Ocak 2022)
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management 10.0.23'daki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 83d19f92984c9f67242946aa8faf445d9d2bd881
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920212"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10023-january-2022"></a>Dynamics 365 Supply Chain Management 10.0.23 sürümündeki yenilikler veya değişiklikler (Ocak 2022)

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management 10.0.23 sürümündeki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1037 derleme numarasına sahiptir ve aşağıdaki gibi kullanıma sunulmuştur:

- **Sürüm önizlemesi:** Ekim 2021
- **Sürüm genel kullanılabilirliği (kendi kendini güncelleştirme):** Aralık 2021
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Ocak 2022

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. *Özellik* sütunu, her bir özellik için resmi kullanıma sunma tarihlerini görebileceğiniz [kullanıma sunma planına](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) bağlantılar sağlar. *Ek bilgi* sütunu, ilgili belgelerin diğer ayrıntılrını ve/veya bağlantılarını sağlar. Özelliğin nasıl açılacağını belirlemek için *Etkinleştiren* sütununa bakın. Özellik yönetimini kullanma hakkında daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---|---|---|---|
| Genel adres defteri | Adres kurulumundaki her ülke/bölge için varsayılan il/bölge tanımlama | Artık, global adres defteri için adres kurulumundaki her bir ülke/bölge için varsayılan bir il/bölge tanımlayabilirsiniz. Varsayılan il/bölge ayarlandığında, o ülke/bölge için yeni bir ilçe veya şehir kaydı oluşturduğunuzda, bu değer il/bölge alanlarında girilen varsayılan değerdir. Ayrıca bkz. [Adres kurulumu](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) | Varsayılan olarak etkinleştirilir. |
| Stok&nbsp;ve&nbsp;lojistik | [Warehouse Management mobil uygulamasında görevleri durdurma](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [Mobil cihaz menü öğelerindeki adımlar için sapmaları yapılandırma](../warehousing/warehouse-app-detours.md) | Özellik yönetimi (*Warehouse Management uygulama sapmaları*) |
| Stok&nbsp;ve&nbsp;lojistik | [Ambar uygulaması yükseltilen alanları](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Mobil cihazdaki adımlar için yükseltilen alanları yapılandırma](../warehousing/warehouse-app-promoted-fields.md)| Özellik yönetimi (*Ambar uygulaması tanıtılan alanlar*) |
| İmalat | [Üretim yürütme sistemleri tümleştirmesi](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-systems-integration) | [Üçüncü taraf üretim yürütme sistemleriyle tümleştirme](../production-control/mes-integration.md) | Özellik yönetimi (*Üretim yürütme sistemi tümleştirmesi*) |
| İmalat | [Üretim katı yürütme arabiriminden ortak ve yan ürünler raporu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [Çalışanlar üretim katı yürütme arabirimini nasıl kullanır?](../production-control/production-floor-execution-use.md) | Özellik yönetimi (*Üretim katı yürütme arabiriminden ortak ve yan ürünler raporu*) |
| Planlama | [Öncelik temelli planlama için Planlama Optimizasyonu desteği](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-priority-based-planning) | [Öncelik tabanlı planlama](../master-planning/planning-optimization/priority-based-planning.md) | Özellik yönetimi (*Planlama Optimizasyonu için önceliği temel alan MRP desteği*) |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümdeki yeni özellik iyileştirmeleri listelenmektedir. Bu iyileştirmelerden her biri, mevcut bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca iyileştirme olduğundan [sürüm planında](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmez. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe).

Bu özelliklerden herhangi birini etkinleştirmek veya devre dışı bırakmak istiyorsanız, bunu [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) yapabilirsiniz. Bunlar, aşağıdaki tablonun *Özellik yönetiminde özellik adı* sütunundaki gösterilen adlar kullanılarak listelenmiştir.

| Modül | Özellik yönetiminde özellik adı | Daha fazla bilgi |
|---|---|---|
| Kıymet yönetimi | İş emri günlüklerindeki giderler için mahsup hesaplar | Bu özellik, bir iş emri günlüğünde listelenen her gider için bir mahsup hesap belirtmenizi sağlar. Genellikle bir satıcı hesabı ile her bir gideri ilişkilendirebilirsiniz, ancak diğer hesap tipleri de desteklenir. Bu , **İş emri günlüğü** sayfasındaki **Gider** hızlı sekmesine iki yeni sütun (**Mahsup hesap türü** ve **Mahsup hesap**) ekler.|
| Maliyet yönetimi | Standart maliyet yuvarlama yeniden değerlemeleri için ilgili fişler oluştur | <p>Bir stok mali deftere nakli (satış siparişi faturası veya stok hareketi gibi) yapıldığında bu özellik, sistemin ilgili standart maliyet yuvarlama yeniden değerlemeleri için ayrı bir fiş oluşturmasına ve bunu mali deftere nakil fişinin ilgili fişi olarak iliştirmesine neden olur.</p><p>Bu özellik olmadan sistem, aynı fiş deftere naklinde ilgili standart maliyet yuvarlama yeniden değerlemelerini kaydeder. Yeniden değerlemeler oturum veya sistem tarihini kullanırken mali deftere nakiller, deftere nakil tarihini kullandığından bu davranış bazen çakışan tarih bilgilerine neden olabilir.</p> |
| Stok ve ambar yönetimi | \[Rusya\] Satış siparişleri için mali fişteki düzeltme bayrağına göre Storno mali stok hareketlerini deftere naklet | Bu özellik, Rusya için kredi notu düzeltmeleri işlevini etkiler. Genel muhasebedeki düzeltme seçeneğine göre satış faturalarına ait stok hareketlerinin deftere nakledilmesini sağlar. Bu özellik etkinleştirildiğinde, stok hareketinin mali fişindeki **Düzeltme** işareti ve stok hareketlerinde **Storno** işareti arasında başka tutarsızlık yoktur. |
| Stok ve ambar yönetimi | (Rusya) Stok bakiyesi ciro raporu hesaplamasını toplu olarak çalıştır | Supply Chain Management'ın Rus yerelleştirmeleri için bu özellik, *Stok bakiyesi ciro* raporunu toplu iş içinde çalıştırma, depolama ve daha önce oluşturulan raporları görüntüleme olanağı sağlar. |
| Stok ve ambar yönetimi | (Rusya) Stok yönetiminde ülkeye veya bölgeye özgü birincil formlarda yerel dildeki çevirileri kullan | Supply Chain Management'ın Rus yerelleştirmeleri için bu özellik Rusya'ya özgü şu stok belgesi çıktılarında ürün/madde adları ve ölçü birimleri için Rusça çevirilerin kullanılmasını sağlar: Sayım listesi (INV-3), Sayım listesi (INV-5) ve Sayım listesi (INV-6). |
| Master planlama | Talep tahmini için Azure Machine Learning Hizmeti | Bu özellik, Azure Machine Learning Hizmeti'nin tarihsel verilere dayalı olarak talep tahminleri oluşturmasına olanak tanır. Daha fazla bilgi için bkz. [Talep tahmini kurulumu](../master-planning/demand-forecasting-setup.md). |
| Tedarik ve kaynak atama | Satınalma siparişi güncelleştirme geçmişini temizle | Bu özellik, satınalma siparişi güncelleştirmeleri ile ilgili geçici geçmiş kayıtları temizlemenizi sağlar. **Tüm satınalma siparişleri** sayfasındaki eylem bölmesine **Satınalma güncelleştirme geçmişini temizle** adı verilen yeni bir düğme ekler. Varsayılan olarak bu özellik etkindir. |
| Üretim denetimi | (Önizleme) Otomatik olarak deftere nakledilen malzeme çekme listeleri için ambarın etkinleştirildiği malzemeleri otomatik çekme | Bu özellik, otomatik olarak deftere nakledilen, türetilen ve geriye dönük malzeme çekme listesi günlükleri için stok boyutlarını otomatik olarak çekmenize ve çözümlemenize olanak tanır. |
| Üretim denetimi | Planlanan tüketim tarihine göre hammadde son tarihlerini doğrula | Bu özellik, üretim sırasında kullanılmak üzere toplu iş hariç bir madde rezerve edildiğinde toplu sona erme tarihlerinin nasıl doğrulanacağını değiştirir. Bu özellik etkinleştirildiğinde, toplu iş sona erme tarihi, üretim ürün reçetesi satırında veya toplu iş emri formülü satırında belirlendiği şekilde planlanan tüketim tarihine (hammadde tarihi) göre doğrulanır. Bu özellik devre dışı bırakıldığında toplu iş sona erme tarihi, üretim emri veya toplu iş emrinin planlanan teslim tarihine (daha önce) göre doğrulanır. |
| Satış ve pazarlama | Yaşına göre satış güncelleştirme geçmişini temizle | Bu özellik, **Satış güncelleştirme geçmişi temizliği** periyodik görevini çalıştırırken tutulacak maksimum kayıt yaş kaydını ayarlamanızı sağlar. Eski kayıtlar silinecek. Bu, geçerlilik süresi her zaman görevin çalıştırıldığı tarihe göre hesaplandığı için, görevi belirli aralıklarla çalışacak şekilde ayarladığınızda yararlıdır. Bu özellik olmadan, yalnızca tutulacak en eski kayıtlar için belirli bir tarih ayarlayabilirsiniz. |
| Satış ve pazarlama | "İlk 100" müşteri raporunun performansını iyileştir | Bu özellik, raporu özel sorgulara izin verilmektense raporu her zaman tüm müşteriler genelinde her çalıştırarak **İlk 100** müşterini raporunun performansını artırır. Bu özellik etkinleştirildiğinde, tüm **Dahil edilecek kayıtlar** ayarları, **İlk 100** rapor iletişim kutusunda devre dışı bırakılır. |
| Ambar yönetimi | Giden siparişlerin ambara serbest bırakılmasına yönelik ölçek birimi desteği | Bu özellik etkinleştirildiğinde, giden siparişler merkezden, doğrudan siparişlerin karşılanacağı ölçek birimine bırakılabilir. |

## <a name="new-and-updated-documentation-resources"></a>Yeni ve güncelleştirilmiş belge kaynakları

Aşağıdaki yardım konularını yakın bir zamanda ekledik veya önemli ölçüde güncelleştirdik. Bu konuların, önceki bölümde listelendiği üzere bu sürüm için eklenen yeni özelliklerle ilgili olması gerekmez. Ancak mevcut özelliklerden daha fazla yararlanmanıza yardımcı olabilirler.

| Özellik alanı | Yeni veya güncelleştirilmiş konular |
|---|---|
| Mühendislik değişikliği yönetimi | [Mühendislik öznitelikleri ve mühendislik özniteliği araması](../engineering-change-management/engineering-attributes-and-search.md), artık mühendislik özniteliği devralmasının nasıl çalıştığını açıklar. |
| Master planlama | [Talep tahminleriyle ana planlama](../master-planning/planning-optimization/demand-forecast.md) ve [Tahmin azaltma anahtarları](../master-planning/reduction-keys.md) artık azaltma anahtarlarıyla nasıl çalışılacağı hakkında daha fazla bilgi sağlar. |
| Master planlama | [Maddeler için güvenlik stoku karşılama](../master-planning/safety-stock-replenishment.md) artık minimum/maksimum anahtar kullanma hakkında daha fazla bilgi sağlar. |
| Master planlama | [Stok tahminleri](../master-planning/inventory-forecast.md) artık tahmin tahsisi hakkında daha fazla bilgi sağlar. |
| Master planlama | [Tedarik planı](../master-planning/supply-schedule.md) |
| Ambar yönetimi | [Genel mobil cihaz parametreleri](../warehousing/mobile-device-parameters.md) |
| Ambar yönetimi | [Bağlama](../warehousing/anchoring.md) |
| Satış ve pazarlama | Şirketlerarası ticaret artık [Şirketlerarası ticaret kurulumu](../sales-marketing/intercompany-trade-set-up.md)ve ilgili konuları ile başlayarak ayrıntılı olarak açıklanmıştır. |
| Stok Yönetimi | Stok Görünürlüğü belgeleri, [Stok Görünürlüğü Eklentisine genel bakış](../inventory/inventory-visibility.md) ve ilgili konularıyla başlayarak artık genişletilmiş ve güncelleştirilmiştir. |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations uygulamaları için platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.23 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.23 sürümü için platform güncelleştirmeleri (Kasım 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.23'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910) görüntüleyin.

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 ve sektör bulutları: 2021 sürüm dalgası 2 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2021 sürüm dalgası 2 planına](/dynamics365-release-plan/2021wave2/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) konusu Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) konusunda duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
