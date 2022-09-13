---
title: Dynamics 365 Commerce 10.0.30 önizlemesi (Kasım 2022)
description: Bu makalede, Microsoft Dynamics 365 Commerce 10.0.30'taki yeni veya değişen özellikler açıklanmaktadır.
author: josaw1
ms.date: 08/31/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0149c9671e8baeb26965b4f136ed91d09e2d039b
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405571"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Dynamics 365 Commerce 10.0.30 önizlemesi (Kasım 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce önizleme sürümü 10.0.30'daki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1362 derleme numarasına sahiptir ve aşağıdaki planlamaya göre kullanıma sunulmuştur:

- **Sürümün önizlemesi:** Eylül 2022
- **Sürüm genel kullanılabilirliği (kendi kendini güncelleştirme):** Ekim 2022
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Kasım 2022

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. Bu makale ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---------|------------------|----------------|--------------| 
| Müşteri desteği   | Power Virtual Agents botu kullanarak bir e-ticaret sitesinde sohbet etme. | Bu özellik, e-ticaret sitesi kullanıcılarına destek istekleri için Power Virtual Agents sohbet botunu kullanma seçeneği sunar. | Son kullanıcılar için yönetici/yetkililer tarafından etkinleştirilir |
| Öngörüler  |  Application Insights hesabınıza satış noktası (POS) operasyonel içgörülerini akışla aktarma. | [Application Insights'ta erişim günlükleri](../dev-itpro/retail-component-events-diagnostics-troubleshooting.md#enable-diagnostic-events-in-application-insights)   |  BT Uzmanı/geliştirici kabulü   |
|  Ödemeler  | 29 günlük yetkilendirme süresinden sonra PayPal sipariş desteği. | PayPal için maksimum yetkilendirme süresi 29 gündür. Bu süreden sonra yeni bir yetkilendirme ve sipariş kimliği oluşturulması gerekir. Alternatif olarak PayPal, bir PayPal siparişinin genel bir sipariş olarak başvurulabildiği bir seçenek sunar; böylece 29. günde yeni bir yetkilendirme ve sipariş kodu oluşturmak yerine, aynı sipariş kimliğine karşı birden fazla yetkilendirme ve yakalama yapılabilir.) | PayPal ödeme bağlayıcısını Commerce Headquarters'da yapılandırırken **OrderIntent** alanı eklenmiştir ve iki değere sahip olabilir:<p><p>- **Yetkilendir** - Bu yapılandırma varsayılandır (alan boş bırakılmışsa, **Yetkilendir** varsayılan olarak davranır). **OrderIntent** öğesini **Yetkilendir** olarak yapılandırmak, **NO_INSTRUCTION** şeklindeki PayPal **processing_instruction** değeriyle ilişkilidir. Sipariş PayPal ile yetkilendirilecektir ve bu değer kullanıldığında yetkilendirme değiştirilemez.<p>- **Kaydet** - **OrderIntent** değeri **Kaydet** olarak ayarlandığında bu, **ORDER_SAVED_EXPLICITLY** şeklindeki PayPal **processing_instruction** değeriyle ilişkilidir. Bu değer kullanıldığında, sipariş referansları PayPal hizmetine kaydedilir.  |
| POS oturum açma  | [POS oturumu açma için kendi kendine tanı yeteneklerini etkinleştirme](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  Bu özellik, mağaza çalışanlarının ve yöneticilerinin POS oturum açma sorunlarının temel nedenlerini hızla tanımlayıp gidermesine yardımcı olmak amacıyla satış noktasında (POS) ve Commerce Headquarters'da kendi kendine tanı olanakları sağlar.<p><p>- POS oturum açma ekranında gösterilen hata iletileri, POS'u kullanan çalışanların sorunu çözmek için gerekli eylemleri gerçekleştirebilmeleri için neyin yanlış olduğunu anlamalarına yardımcı olabilecek somut bilgileri sağlayacak şekilde iyileştirilmiştir.<p>- **Test oturumu** işlevi, POS cihazlarını kuran mağaza yöneticilerinin POS oturum açma işleminin benzetimini yapabilmesi için Commerce Headquarters'daki **Çalışanlar** sayfasında yer alır. Bir oturum açma hatası durumunda bu işlev, yöneticilerin uygun yapılandırmaları denetleyebilmesi, sorunları giderebilmesi ve düzeltmeleri doğrulayabilmesi için işlem yapılabilir sorun giderme kılavuzları sağlar.  | Varsayılan olarak açık |


## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finans ve Operasyon uygulamaları için Platform güncelleştirmeleri

Dynamics 365 Finance 10.0.30, platform güncelleştirmelerini içerir. Daha fazla bilgi için bkz. [Finans ve operasyon uygulamaları 10.0.30 sürümü için platform güncelleştirmeleri](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.30 sürümünün parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [KB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) görüntüleyin. 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 2 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 2 planına](/dynamics365-release-plan/2022wave2/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-features"></a>Kaldırılan ve kullanım dışı olan özellikler

[Dynamics 365 Commerce'teki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-commerce.md) makalesi, Commerce için kaldırılmış veya kullanım dışı bırakılmış özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Commerce'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-commerce.md) makalesinde duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
