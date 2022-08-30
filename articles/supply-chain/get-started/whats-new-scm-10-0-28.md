---
title: Dynamics 365 Supply Chain Management'deki yenilikler veya değişiklikler 10.0.28 (Ağustos 2022)
description: Bu makalede, Microsoft Dynamics 365 Supply Chain Management 10.0.28'deki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 5cca06517fbdcbdae6e54c106b113a83851240c8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334790"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10028-august-2022"></a>Dynamics 365 Supply Chain Management'deki yenilikler veya değişiklikler 10.0.28 (Ağustos 2022)

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Supply Chain Management sürümü 10.0.28'teki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1264 derleme numarasına sahiptir ve aşağıdaki planlamaya göre kullanıma sunulmuştur:

- **Sürümün önizlemesi:** Mayıs 2022
- **Sürüm genel kullanılabilirliği (kendi kendine güncelleştirme):** Temmuz 2022
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Temmuz 2022

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. Bu makale ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---|---|---|---|
| Stok ve lojistik | [Üçüncü taraf nakliye aracıları için Son teslim alma maliyeti tümleştirmesi varlıkları](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Son teslim alma varlıklarına genel bakış](../landed-cost/landed-cost-entities-overview.md) | Varsayılan olarak etkin |
| Planlama | [Talep Temelli Materyal Gereksinimleri Planlaması (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | [Talep Temelli Malzeme Gereksinimleri Planlamasına genel bakış](../master-planning/planning-optimization/ddmrp-overview.md) | Özellik yönetimi:<br>*(Önizleme) Planlama Optimizasyonu için DDMRP* |
| Planlama | [Taahhüt verilebilir plan (CTP) için Planlama İyileştirmesi desteği](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | [CTP kullanarak satış siparişi teslimat tarihlerini hesaplama](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) | Özellik yönetimi:<br>*(Önizleme) Planlama Optimizasyonu için CTP* |
| Planlama | [Raf ömrü için Planlama İyileştirmesi desteği](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | [Sınırlı raf ömrü olan ürünler için master planlama](../master-planning/planning-optimization/shelf-life.md) | Varsayılan olarak etkin |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde dahil edilen özellik iyileştirmeleri listelenmektedir. Bu iyileştirmelerden her biri, mevcut bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca iyileştirme olduğundan [sürüm planında](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmez. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe).

Bu özelliklerden herhangi birini açmak veya kapatmak istiyorsanız bunu [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) yapmalısınız.

| Modül | Özellik yönetiminde özellik adı | Daha fazla bilgi |
|---|---|---|
| Stok ve ambar yönetimi | Şirketlerarası eldeki stokta yalnızca eldeki miktarı sıfır olmayan öğelerin gösterilmesini etkinleştir | Bu özellik, eldeki stok miktarı sıfır olan maddelerin şirketlerarası eldeki stok listesine eklenip eklenmeyeceğini seçmenizi sağlar. Bu özelliğin **Stok ve ambar yönetim parametreleri** sayfasına eklediği **Şirketlerarası eldeki stok listesinde eldeki miktarı sıfır olan öğeleri gösterme** ayarını kullanarak bu seçeneği denetleyebilirsiniz. |
| Stok ve ambar yönetimi | (Hindistan) Transfer fiyat kuralları ile ilgili olarak "Ambar kodundan" alanı "Tümü" olarak ayarlandığında görmezden gelin | <p>Bu özellik yalnızca Hindistan yerelleştirmeleri için geçerlidir. Stok transferlerindeki maddelerin transfer fiyatlarını ayarlama işlemini daha kolay hale getirir.</p><p>Transfer fiyatlarını, her maddeyi transfer fiyatlandırması kurallarıyla yapılandırarak ayarlarsınız. Bu işlemi gerçekleştirmenin bir yolu, **Ambar kodundan** alanının *Tümü* olarak ayarlandığı bir satır kuralı eklemektir. Bu ayarla birlikte ilgili satır tarafından belirlenen transfer fiyatı, maddenin hangi ambardan çekildiğinden bağımsız olarak geçerli olur. Bu özellik etkinleştirildiğinde **Ambar kodundan** alanının *Tümü* olarak ayarlandığı transfer fiyatı kuralları **Yerleşim** ayarını yoksayar. Böylece kural, transfer emrinde belirtilen yerleşimden bağımsız olarak geçerli olur. Depolama boyutu hiyerarşisinde yerleşim, ambarın altında olduğu için beklenen davranışın bu olması muhtemeldir.</p><p>Bu özellik olmadığında sistem, bu ve benzeri kuralları yalnızca transfer emrindeki yerleşim, kural için belirlenen yerleşim ile tamamen uyuştuğunda uygular. (Kural için boş bir yerleşim ayarlandıysa sistem, yalnızca yerleşim değeri boş olan transfer emirleri için geçerli olur).</p> |
| Stok ve ambar yönetimi | Stok eldeki değer raporu verilerini temizleme | Bu özellik, *Eldeki stok rapor depolama alanı* raporları oluşturmak için kullanılan verileri temizlemeye yönelik bir yöntem sunar. |
| Üretim denetimi | Servis sözleşmesi ve servis sipariş satırları için proje faaliyetleri ata | Bu özellik, servis anlaşmasına ve servis siparişi satırlarına **Proje faaliyeti** adlı bir alan ekler; böylece bunlar için proje faaliyeti ayarlayabilirsiniz. Özellik, bir proje faaliyeti belirlenmesi gereken servis yönetimi proje günlüklerini deftere naklederken durdurma hataları almanızı önler.  |
| Ambar yönetimi | Yönetici veya benzer güvenilen kullanıcılar için el ile transfer satırı çekme hizmeti | Bu özellik, yöneticilerin transfer satırlarıyla ilgili stok hareketlerini el ile çekmesine olanak tanır. Bu satırlar, daha önce ambara serbest bırakılmış olan satırları içerir. Yöneticiler bu çekme işlemini, yalnızca sistemin bozuk olduğu durumlar gibi olağanüstü durumlarda uygulamalıdır. |

## <a name="new-and-updated-documentation-resources"></a>Yeni ve güncelleştirilmiş belge kaynakları

Aşağıdaki Yardım makalelerini yakın bir zamanda ekledik veya önemli ölçüde güncelleştirdik. Bu makalelerin, önceki bölümlerde listelendiği üzere bu sürüm için eklenen yeni özelliklerle ilgili olması gerekmez. Ancak mevcut özelliklerden daha fazla yararlanmanıza yardımcı olabilirler.

| Özellik alanı | Yeni veya güncelleştirilmiş makaleler |
|---|---|
| Maliyet yönetimi | [Sabit giriş fiyatı](../cost-management/fixed-receipt-price.md) |
| Maliyet yönetimi | [Stok maliyetlendirme ile ilgili sık sorulan sorular](../cost-management/inventory-costing-faq.md) |
| Maliyet yönetimi | [Gider hesabına naklet muhasebe ilkesi](../cost-management/post-to-charge-account-accounting-principle.md) |
| Stok Yönetimi | [Stok hareketi ayrıntıları](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finans ve operasyon uygulamaları için platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.28 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finans ve operasyon uygulamalarının 10.0.28 sürümü için platform güncelleştirmeleri (Haziran 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.28'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) görüntüleyin.

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

