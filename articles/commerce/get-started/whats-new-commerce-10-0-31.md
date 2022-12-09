---
title: Dynamics 365 Commerce 10.0.31 önizlemesi (Şubat 2023)
description: Bu makalede, Microsoft Dynamics 365 Commerce 10.0.31'taki yeni veya değişen özellikler açıklanmaktadır.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: ed4325095163415d05a56128cb1f0334440fe0e5
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787539"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Dynamics 365 Commerce 10.0.31 önizlemesi (Şubat 2023)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce önizleme sürümü 10.0.31'daki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1406 derleme numarasına sahiptir ve aşağıdaki planlamaya göre kullanıma sunulmuştur:

- **Sürüm önizlemesi:** Ekim 2022
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Ocak 2023
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Şubat 2023

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. Bu makale ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---|---|---|---|
| Hata kodları | Commerce'de, çevrimiçi alışveriş yapanlara sunulan çevrimiçi kanal ödeme hatalarına dahil edilecek standartlaştırılmış hata başvuruları kullanıma sunulmuştur.| [Ödeme modülü hata kodları](../checkout-module-error-codes.md)  | Varsayılan olarak açık |
| Ödemeler | [Adyen için Dynamics 365 Payment Connector ile Apple Pay'i Etkileştirme](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | E-ticaret müşterileri, desteklenen cihazları veya tarayıcıları kullanarak alışveriş sepeti ve ödeme sayfalarında Apple Pay'i kullanabilirler. | Geliştirici kabulü |
| Ödemeler  |  Commerce'de kullanıcıların Commerce headquarters kullanıcı arabirimi boyunca yinelenen ödeme belirteçleriyle nasıl etkileşim kurduklarını sınırlama özelliği eklenmiştir. **Çağrı Merkezi Satış Siparişleri** sayfası gibi ödeme formlarında artık müşterinin yeni bir harekette kullanmak üzere daha önce yararlandığı yinelenen ödeme belirteci görüntülenmez. Yeni bir hareket için ödeme işlenirken çağrı merkezi veya Commerce headquarters kullanıcılarına Commerce **Müşteri Ödemeleri** ekranında yalnızca belirli bir "kayıtlı kart" girişi veya satış siparişi yoluyla ödeme yaparken bir müşteriyle yapılan anlaşma sunulur. | [Ödeme belirteci kullanımını sınırlama](../dev-itpro/limit-token-usage.md)  |  Özellik yönetimi<p>*Ödeme Belirteci kullanımını Sipariş bağlamıyla sınırla*  |
| POS | [POS'tan satın alma siparişleri oluşturma](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  Satış noktası (POS) uygulamasında gelen stok işlemi kullanıcıların satın alma siparişi isteklerini oluşturmasına, düzenlemesine ve onaylamasına olanak tanımak için iyileştirilmiştir. |  Özellik yönetimi<p>*POS'ta satınalma siparişi talebi oluşturma yeteneği*   |
| Kullanılabilir ek diller | Dört ek dil bulunur | Tercih edilen dil listesinde kullanıcının seçebileceği dört yeni dil vardır: Korece, Portekizce (Portekiz), Vietnamca ve Çince (Geleneksel). Bu seçeneği belirlemek için **Kullanıcı seçenekleri \> Tercihler \> Dil ve ülke/bölge tercihi**'ne gidin. | Yerelleştirilmiş tercihler |  



## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finans ve Operasyon uygulamaları için Platform güncelleştirmeleri

Microsoft Dynamics 365 Commerce 10.0.31 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finans ve operasyon uygulamalarının 10.0.31 sürümü için platform güncelleştirmeleri (Şubat 2023)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md). 
  

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.31 sürümünün parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için Microsoft Dynamics Lifecycle Services'te oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525) görüntüleyin.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 2 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 2 planına](/dynamics365-release-plan/2022wave2/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-commerce-features"></a>Kaldırılan ve kullanım dışı bırakılan Commerce özellikleri

[Dynamics 365 Commerce'teki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-commerce.md) makalesi, Commerce için kaldırılmış veya kullanım dışı bırakılmış özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Commerce'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-commerce.md) makalesinde duyurulacaktır.


Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
