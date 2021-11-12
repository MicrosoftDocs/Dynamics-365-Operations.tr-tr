---
title: Dynamics 365 Supply Chain Management 10.0.22'daki yenilikler veya değişiklikler (Kasım 2021)
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management 10.0.22'daki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a4f9e5a4a318ceaa45b6919e394e1ff335bfb193
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678847"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10022-november-2021"></a>Dynamics 365 Supply Chain Management 10.0.22'daki yenilikler veya değişiklikler (Kasım 2021)

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management 10.0.22 sürümündeki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.995 derleme numarasına sahiptir ve aşağıdaki gibi kullanıma sunulmuştur:

- **Sürümün önizlemesi:** Eylül 2021
- **Sürüm genel kullanılabilirliği (kendi kendini güncelleştirme):** Ekim 2021
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Kasım 2021

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. *Özellik* sütunu, her bir özellik için resmi kullanıma sunma tarihlerini görebileceğiniz [kullanıma sunma planına](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) bağlantılar sağlar. *Ek bilgi* sütunu, ilgili belgelerin diğer ayrıntılrını ve/veya bağlantılarını sağlar. Özelliğin nasıl açılacağını belirlemek için *Etkinleştiren* sütununa bakın. Özellik yönetimini kullanma hakkında daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren   |
|---|---|---|---|
| Planlama | [Yetenek tabanlı kaynak tahsisatı için Planlama Optimizasyonu desteği](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Yeteneğe dayalı kaynak seçimi ile zamanlama](../master-planning/planning-optimization/capability-based-scheduling.md) | Özellik yönetimi (*Planlama Optimizasyonu için sonsuz kapasite zamanlaması*) |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde dahil edilen özellik iyileştirmeleri listelenmektedir. Bu iyileştirmelerden her biri, mevcut bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca iyileştirme olduğundan [sürüm planında](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmez. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe). Bu özelliklerden herhangi birini kullanmak istiyorsanız bunları [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) açıkça etkinleştirmeniz gerekir.

| Modül | Özellik yönetiminde özellik adı | Daha fazla bilgi |
|---|---|---|
| Maliyet yönetimi | Standart maliyet yuvarlama yeniden değerlemeleri için ilgili fişler oluşturma | <p>Bir stok mali deftere nakli (satış siparişi faturası veya stok hareketi gibi) yapıldığında bu özellik, sistemin ilgili standart maliyet yuvarlama yeniden değerlemeleri için ayrı bir fiş oluşturmasına ve bunu mali deftere nakil fişinin ilgili fişi olarak iliştirmesine neden olur.</p><p>Bu özellik olmadan sistem, aynı fiş deftere naklinde ilgili standart maliyet yuvarlama yeniden değerlemelerini kaydeder. Yeniden değerlemeler oturum veya sistem tarihini kullanırken mali deftere nakiller, deftere nakil tarihini kullandığından bu davranış bazen çakışan tarih bilgilerine neden olabilir.</p> |
| Dağıtılmış karma topoloji | *(Özellik yönetimi gerekmez.)* | <p>Bu sürüm, bulut ve uç ölçek birimleri için ambar yönetimi iş yükünün giden yük planlama yeteneklerini genişletir.</p><p>Daha fazla bilgi için bkz. [Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| Mühendislik değişikliği yönetimi | Mühendislik ürünleri için çeşit oluşturma | <p>Bu özellik, bir mühendislik ürünü için renk, boyut, stil veya yapılandırma boyutlarına göre farklı çeşitler oluşturmanıza olanak tanır.</p><p>Daha fazla bilgi için bkz. [Mühendislik ürünleri için çeşitler oluşturma](../engineering-change-management/engineering-variants.md).</p> |
| Stok ve ambar yönetimi | Ayırma farkıyla Stok Görünürlüğü tümleştirmesi | <p>Bu özellik yalnızca *Stok Görünürlüğü Tümleştirmesi* özelliği etkinleştirildikten sonra etkinleştirilebilir. Bu, Stok Görünürlüğü'nde yapılan rezervasyonları denkleştirmede işlevsellik sağlar.</p><p>Daha fazla bilgi için bkz. [Stok Görünürlüğü rezervasyonları](../inventory/inventory-visibility-reservations.md).</p> |

## <a name="new-and-updated-documentation-resources"></a>Yeni ve güncelleştirilmiş belge kaynakları

Aşağıdaki yardım konularını yakın bir zamanda ekledik veya önemli ölçüde güncelleştirdik. Bu konuların, önceki bölümde listelendiği üzere bu sürüm için eklenen yeni özelliklerle ilgili olması gerekmez. Ancak mevcut özelliklerden daha fazla yararlanmanıza yardımcı olabilirler.

| Özellik alanı | Yeni veya güncelleştirilmiş konular |
|---|---|
| Mühendislik değişikliği yönetimi | [Mühendislik değişim yönetimine genel bakış](../engineering-change-management/product-engineering-overview.md) bölümünde artık özellik yönetiminde kullanılabilen tüm ilgili ve isteğe bağlı özellikler listelenmektedir |
| Master planlama | [Talep tahmini kurulumu](../master-planning/demand-forecasting-setup.md) |
| Master planlama | [Planlama Optimizasyonu ile net gereksinimler ve ilişkilendirme bilgileri](../master-planning/planning-optimization/net-requirements.md) |
| Ambar yönetimi | [Ambara serbest bırakma](../warehousing/release-to-warehouse-process.md) bölümünde, tüm ambara serbest bırakma işlemine dair ayrıntılı bir genel bakış sağlanmaktadır |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations uygulamaları için platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.22 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.22 sürümü için platform güncelleştirmeleri (Kasım 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.22'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299) görüntüleyin.

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
