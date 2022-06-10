---
title: Dynamics 365 Supply Chain Management 10.0.27 Önizlemesi (2022 Temmuz)
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management 10.0.27'daki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 77c79c88b08844bf7e399a762bb9eb9746ffb71a
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2022
ms.locfileid: "8812958"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10027-july-2022"></a>Dynamics 365 Supply Chain Management 10.0.27 Önizlemesi (2022 Temmuz)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management önizleme sürümü 10.0.27'daki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1227 derleme numarasına sahiptir ve aşağıdaki planlamaya göre kullanıma sunulmuştur:

- **Sürümün önizlemesi:** Nisan 2022
- **Sürüm genel kullanılabilirliği (kendi kendine güncelleştirme):** Haziran 2022
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Temmuz 2022

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---|---|---|---|
| Stok ve lojistik | [Stok Görünürlüğü Eklentisi için stok tahsisatı](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [Stok Görünürlüğü stok tahsisatı](../inventory/inventory-visibility-allocation.md) | Varsayılan olarak etkin |
| İmalat | Üretim katı yürütme arabirimi için "Günüm" görünümü | [Çalışanlar üretim kat yürütme arabirimini nasıl kullanır](../production-control/production-floor-execution-use.md) ve [Üretim tabanı yürütme arabirimindeki tatil bakiyelerini görüntüleme](../production-control/production-floor-execution-payroll-stats.md) | Özellik yönetimi:<br>*Üretim katı yürütme arabirimi için "Günüm" görünümü* |
| Planlama | [Alt sözleşme için Planlama Optimizasyonu desteği](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Üretimdeki alt sözleşme işini yönetme](../production-control/manage-subcontract-work-production.md) | Varsayılan olarak etkin |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde dahil edilen özellik iyileştirmeleri listelenmektedir. Bu iyileştirmelerden her biri, mevcut bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca iyileştirme olduğundan [sürüm planında](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmez. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe).

Bu özelliklerden herhangi birini açmak veya kapatmak istiyorsanız bunu [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) yapmalısınız.

| Modül | Özellik yönetiminde özellik adı | Daha fazla bilgi |
|---|---|---|
| Master planlama | Planlı transfer emri oluştururken stok sağlama süresini hesaba kat | Bu özellik, planlı bir transfer emri siparişi oluşturulduğunda sistemin, *Hiçbiri* veya *Satış* saülama süresi olarak teslimatı tarihi denetim ayarı için planlanan transfer emrinin giriş tarihini hesaplarken kullanılan maddenin varsayılan emir ayarlarında belirtilen stok sağlama süresini hesaba katmasını sağlar. Transfer sağlama süresi belirtildiğinde, değeri giriş tarihi hesaplaması için kullanılır ve taşıma günleri yok sayılacaktır. |
| Tedarik ve kaynak atama | Satıcı fatura satırlarındaki varsayılan aracı sözleşmesi vergi bilgileri | Bu özellik, aracı sözleşmesi satıcı fatura satırlarındaki **Satış vergisi** ve **Madde satış vergisi** alanları için varsayılan değerleri ayarlama mantığını tanıtır. Bu mantık yalnızca aracı sözleşme satırındaki gider türü genel muhasebe/genel muhasebe olduğunda uygulanır. Madde satış vergisi grubu varsayılan değerini broker tedarik kategorisinden (ayarlanmışsa) veya gider türünden alır. Satış vergisi grubunun varsayılan değerini satıcı hesabından alınır. |
| Tedarik ve kaynak atama | Toplu iş görevi başına satınalma siparişi satırlarının sayısını sınırla | Bu özellik, teyitler ve ürün makbuzları deftere nakledilirken sistem performansını en iyi duruma getirmenize yardımcı olur. **Görev başına satırlar** olarak adlandırılan yeni bir ayarı, **Tedarik ve kaynak parametreleri** sayfasının **Teslim** sekmesine ekler. Bu yeni ayar, her toplu iş görevinin işlediği satınalma siparişi satırı sayısını sınırlandırmanıza olanak tanır. Bu nedenle, büyük toplu iş görevlerinin sistemi yavaşlatmasını engellemeye yardımcı olabilir. |
| Ürün bilgileri yönetimi | Ürün öznitelik değerlerini doldur | Bu özellik, *Ürün öznitelik değerlerini doldur* adlı periyodik bir görev ekler. Bu yeni periyodik görev, ürün kategorisi aracılığıyla ürünlerle ilişkilendirilmiş öznitelikler için eksik ürün özniteliği değer kayıtlarını oluşturur. |
| Üretim denetimi | Üretim katı yürütme arabirimindeki ek yapılandırma | <p>Bu özellik, **Üretim taban yürütmesini konfigüre et** sayfasına aşağıdaki seçenekleri ekler:</p><ul><li>**Arama tamamlarken başlangıç iletişim kutusunu otomatik olarak aç**: Bu seçenek kullanıldığında **İşi başlat** iletişim kutusu, çalışanlar işi bulmak için arama çubuğunu kullandığında otomatik olarak açılır.</li><li>**Arama tamamlarken başlangıç rapor ilerlemesini otomatik olarak aç**: Bu seçenek kullanıldığında **Rapor ilerlemesi** iletişim kutusu, çalışanlar işi bulmak için arama çubuğunu kullandığında otomatik olarak açılır.</li><li>**Rapor ilerleme durumu iletişim kutusunda varsayılan kalan miktar** – Bu seçenek etkinleştirildiğinde, **Rapor ilerleme durumu** iletişim kutusu bir üretim işinde raporlanacak kalan miktarı gösterir.</li></ul><p>Daha fazla bilgi için bkz. [Üretim katı yürütme arabirimini yapılandırma](../production-control/production-floor-execution-configure.md).</p> |
| Üretim denetimi | Üretim katı yürütme arabiriminde üretim takımları | <p>Aynı üretim işine birden fazla işçi atandığında, artık bir işçiyi pilot olarak aday gösterebilirler. Kalan işçiler otomatik olarak bu pilotun asistanı olurlar. Ortaya çıkan ekip için, yalnızca pilot iş durumunu kaydetmelidir, oysa zaman kayıtları tüm ekip üyeleri için geçerlidir. Bu özellik, *yardım kaynağı* adlı bir senaryoyu da destekler. Bu senaryoda, bir çalışan başka bir çalışanın asistanı olarak kaydolabilir ve bu çalışan daha sonra yeni oluşturulan grup için pilot olur.</p><p>Daha fazla bilgi için bkz. [Çalışanlar üretim katı yürütme arabirimini nasıl kullanır?](../production-control/production-floor-execution-use.md).</p> |
| Üretim denetimi | Üretim katı yürütme arabiriminde planlama maddelerini raporla | Bu özellik, üretim katı yürütme arabirimindeki planlama kalemleri için toplu iş emirleri üzerinde raporlama işlemini basitleştirir. Üretim türü *Planlama maddesi* olan bir ürün için toplu iş emri oluşturulduğunda, bitmiş olarak raporlama yalnızca bu toplu iş emrinin ortak ürünlerinde ve yan ürünlerinde yapılabilir. Planlama kalemleri için toplu iş emirleri tipik olarak, bir hammadde ürününün birden fazla farklı ürüne demonte edildiği sökme işlemlerini desteklemek için kullanılır. Bir çalışan bir planlama kalemi için bir toplu iş emrini tamamlandı olarak bildirdiğinde, **İlerlemeyi raporla** iletişim kutusu artık yalnızca ortak ürünleri ve yan ürünleri gösterecektir. Önceden, planlama öğesini de gösteriyordu ve bu davranış işçilerin kafasını karıştırabiliyordu. |

## <a name="new-and-updated-documentation-resources"></a>Yeni ve güncelleştirilmiş belge kaynakları

Aşağıdaki Yardım konularını yakın bir zamanda ekledik veya önemli ölçüde güncelleştirdik. Bu konuların, önceki bölümlerde listelendiği üzere bu sürüm için eklenen yeni özelliklerle ilgili olması gerekmez. Ancak mevcut özelliklerden daha fazla yararlanmanıza yardımcı olabilirler.

| Özellik alanı | Yeni veya güncelleştirilmiş konular |
|---|---|
| Maliyet yönetimi | [Fiziksel değer ve işaretlemeyi dahil et ile ağırlıklı ortalama tarihi](../cost-management/weighted-average-date.md) |
| Dağıtılmış karma topoloji | [Dağıtılmış karma topolojideki ölçek birimlerini deneme](../cloud-edge/cloud-edge-try-out.md) |
| Çift yazma | [Supply Chain Management fiyatlandırma altyapısıyla istek üzerine eşitleme](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Ambar yönetimi | [Ambara serbest bırakma](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance ve Operations uygulamaları için Platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.27 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finans ve Operasyon uygulamalarının 10.0.27 sürümü için platform güncelleştirmeleri (Haziran 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.27'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271) görüntüleyin.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 1 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 1 planına](/dynamics365-release-plan/2022wave1/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) konusu Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) konusunda duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
