---
title: Dynamics 365 Supply Chain Management'daki yenilikler veya değişiklikler 10.0.26 (Mayıs 2022)
description: Bu makalede, Microsoft Dynamics 365 Supply Chain Management 10.0.26'daki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: db8799aba8095c8144d878c96590e8d90276726b
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428236"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10026-may-2022"></a>Dynamics 365 Supply Chain Management'daki yenilikler veya değişiklikler 10.0.26 (Mayıs 2022)

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Supply Chain Management sürümü 10.0.26'teki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1192 derleme numarasına sahiptir ve aşağıdaki gibi kullanıma sunulmuştur:

- **Sürümün önizlemesi:** Mart 2022
- **Sürüm genel kullanılabilirliği (kendi kendine güncelleştirme):** Nisan 2022
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Mayıs 2022

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. Bu makale ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---|---|---|---|
| Stok ve lojistik | [Gelişmiş ambar yönetimi maddelerini desteklemek için Stok Görünürlüğü eldeki sorgu](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [WMS öğeleri için Stok Görünürlüğü desteği](../inventory/inventory-visibility-whs-support.md) | Özellik yönetimi:<br>*Stok Görünürlüğünde ambar maddelerini etkinleştir* |
| Stok ve lojistik | [Stok Görünürlüğü Eklentisi için mevcut karşılanabilir](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Stok Görünürlüğü eldeki değişiklik zamanlamaları ve karşılanabilir miktarı](../inventory/inventory-visibility-available-to-promise.md) | Hizmet yapılandırması tarafından etkinleştirilir |
| İmalat | [Üretim katı yürütme arabiriminde fiili ağırlık maddeleri](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Çalışanlar üretim katı yürütme arabirimini nasıl kullanır?](../production-control/production-floor-execution-use.md) | Özellik yönetimi:<br>*Üretim katı yürütme arabiriminden elde edilen fiili ağırlık öğeleriyle ilgili rapor* |
| İmalat | Üretim katı yürütme arabirimindeki işlerim sekmesi | [Çalışanlar üretim katı yürütme arabirimini nasıl kullanır?](../production-control/production-floor-execution-use.md) | Özellik yönetimi:<br>*Üretim katı yürütme arabirimindeki işlerim sekmesi* |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde dahil edilen özellik iyileştirmeleri listelenmektedir. Bu iyileştirmelerden her biri, mevcut bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca iyileştirme olduğundan [sürüm planında](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmez. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe).

Bu özelliklerden herhangi birini açmak veya kapatmak istiyorsanız bunu [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) yapmalısınız.

| Modül | Özellik yönetiminde özellik adı | Daha fazla bilgi |
|---|---|---|
| Tedarik ve kaynak atama | Stoğu tutulan ürünlerin miktarları ve stoğu tutulmayan ürünlerin kalanlarını, girişler ve satıcı faturaları için deftere naklet | Bu özellik, stok faturaları ve satınalma siparişlerine göre gelen sevk irsaliyeleri işlenirken, stoklanmayan ürünlerin (servisler gibi) miktarlarının nasıl deftere nakledildiğini değiştirir. Özellik, deftere nakil makbuzları ve satıcı faturalarının *Kayıtlı miktar ve hizmetler* miktarı seçeneğinin davranışını, bunu satış sevk irsaliyeleri için miktarları deftere naklederken zaten sağlanan *Kayıtlı miktar ve stoğu tutulmayan ürünler* seçeneği davranışıyla eşleyerek değiştirir.<br><br>*Kayıtlı miktar ve servis miktarı* seçeneğini kullanarak bir ürün girişini veya satıcı faturasını deftere naklettiğinizde, sistem, kaydedilen stoğu tutulan ürünlerin kayıtlı miktarını deftere nakleder ve kalan teslim edilmemiş ürün miktarını (hem servisler hem de servisler olmayanlar dahil) deftere nakleder. Bu özellik olmadan, sistem, stoğu tutulan ürünlerin kayıtlı miktarını (stoklu maddeler olarak konfigüre edilen servisler dahil) deftere nakleder, ancak her zaman stoklanmamış servis ürünlerinin tam sipariş edilen miktarını deftere nakleder (ve *Hizmet* türünde olmayan, stoklanmayan ürünleri yoksayar). |
| Tedarik ve kaynak atama | Şirketlerarası satış ve satınalma siparişi satırlarında izleme boyutlarını eşitle | Bu özellik, seri ve toplu iş numarası izleme boyutlarının şirketlerarası satış ve satınalma siparişi satırları arasında eşitlenip eşitlenmeyeceğini denetlemenize olanak tanır. Bu, müşteri ve satıcılar için **Şirketlerarası** kurulum sayfasının **Satınalma siparişi ilkeleri** ve **Satış siparişi ilkeleri** sekmelerine yeni ayarlar ekler. Ayrıca, daha az ilişkili, yakındaki ayarların adlarını da güncelleştirir.<br><br>Ambar yönetimi süreçleri (WMS) kullanıyorsanız, bu özelliğin yalnızca parti ve seri numaralarını, bu boyutlar hedef rezervasyon hiyerarşisindeki konumun üzerinde olduğunda eşitlendiğini unutmayın. |
| Ürün bilgileri yönetimi | Ürün öznitelik değerlerini temizle | Bu özellik, **Ürün öznitelik değerlerini temizle** adlı bir periyodik görev ekler. Bu görev, artık ürün kategorisi aracılığıyla herhangi bir ürünle ilişkili olmayan ürün özniteliği değer kayıtlarını temizler. |
| Stok ve ambar yönetimi | (Rusya) WMS'nin etkin olduğu öğeleri içeren satınalma siparişleri için GTD'ler verilirken ortaya çıkabilecek tutarsızlıkları engelle | Bu özellik yalnızca Rusya yerelleştirmesi içindir. Depo yönetimi süreçleri (WMS) için etkinleştirilen maddeleri içeren ithalat satınalma siparişleri için Rus gümrük beyannamesi numaraları (GTD'ler) düzenlenirken ortaya çıkan uyuşmazlıkları önler. GTD sağlama işlemi, özel günlükte yer alan faturalar için ilgili stok hareketlerinde yer alan ve satınalma siparişi için iş kayıtları ve satınalmayla ilgili stok hareketleri arasında tutarsızlık bulunan fatura boyut değerlerini değiştirir. Bu özellik etkinleştirildiğinde, GTD sağlayan işlem, bu tür tutarsızlıkları ortadan kaldıran düzeltme çalışması oluşturur. |
| Ambar yönetimi | GS1 barkodları için geliştirilmiş ayrıştırıcı | Bu özellik, GS1 sembol verileri için gelişmiş bir Ayrıştırıcı ekler. Yeni ayrıştırıcı, GS1 sembolleri ayrıştırmak için GS1 Genel Belirtim algoritmasını uygular ve daha güçlü veri doğrulaması sağlar. Daha fazla bilgi için bkz. [GS1 barkod taraması](../warehousing/gs1-barcodes.md). |
| Ambar yönetimi | Ambar yönetimi uygulaması - boş GTD | Bu özellik yalnızca Rusya yerelleştirmesi içindir. Gerektiğinde, Warehouse Management mobil uygulamasını kullanan çalışanların Rusça gümrük beyanname numaralarını (GTD'ler) boş bırakmasını sağlar. GTD izleme boyutu boş değerlere izin verecek şekilde ayarlandıysa, sistem sağlanan eldeki stok operasyonları için GTD için boş değerleri kabul eder. |

## <a name="new-and-updated-documentation-resources"></a>Yeni ve güncelleştirilmiş belge kaynakları

Aşağıdaki yardım makalelerini yakın bir zamanda ekledik veya önemli ölçüde güncelleştirdik. Bu makalelerin, önceki bölümlerde listelendiği üzere bu sürüm için eklenen yeni özelliklerle ilgili olması gerekmez. Ancak mevcut özelliklerden daha fazla yararlanmanıza yardımcı olabilirler.

| Özellik alanı | Yeni veya güncelleştirilmiş makaleler |
|---|---|
| Maliyet yönetimi | Aşağıdaki makalelerin her birine güncelleştirilmiş örnekler ve diyagramlar eklendi:<ul><li>[Fiziksel değer ve işaretleme ile FIFO](../cost-management/fifo-physical-value-marking.md)</li><li>[Fiziksel değer ve işaretleme ile LIFO](../cost-management/lifo-physical-value-marking.md)</li><li>[Fiziksel değer ve işaretleme ile LIFO Tarihi](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Cari ortalama maliyet fiyatı](../cost-management/running-average-cost-price.md)</li><li>[Fiziksel değer ve işaretleme ile ağırlıklı ortalama](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finans ve operasyon uygulamaları için platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.26 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finans ve operasyon uygulamalarının 10.0.26 sürümü için platform güncelleştirmeleri (Mayıs 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.26'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) görüntüleyin.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 1 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 1 planına](/dynamics365-release-plan/2022wave1/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) makalesi Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) makalesinde duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

