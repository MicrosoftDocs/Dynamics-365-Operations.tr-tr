---
title: Dynamics 365 Supply Chain Management 10.0.30 önizlemesi (Kasım 2022)
description: Bu makalede, Microsoft Dynamics 365 Supply Chain Management 10.0.30'daki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 09/08/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 477b27bf77d2a3ef91a5c2d39f2dfb06d8ad4e59
ms.sourcegitcommit: 562ea02e1f7409f18ee1cc4750a838bff4381e91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429136"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10030-november-2022"></a>Dynamics 365 Supply Chain Management 10.0.30 önizlemesi (Kasım 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu makalede, Microsoft Dynamics 365 Supply Chain Management önizleme sürümü 10.0.30'daki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1362 derleme numarasına sahiptir ve aşağıdaki planlamaya göre kullanıma sunulmuştur:

- **Sürümün önizlemesi:** Eylül 2022
- **Sürüm genel kullanılabilirliği (kendi kendini güncelleştirme):** Ekim 2022
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Kasım 2022

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. Bu makale ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---|---|---|---|
| İmalat | [Sensör Veri Yönetim Bilgileri ile ekipmanları izleme](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Sensör Veri Yönetim Bilgileri giriş sayfası](../sensor-data-intelligence/sdi-home-page.md) | Özellik yönetimi:<br>*(Önizleme) Algılayıcı Veri Zekası* |
| Ambar yönetimi | Warehouse Management mobil uygulaması için çok düzeyli sapmalar <!-- KFM: Add link when RP updates --> | [Mobil cihaz menü öğelerindeki adımlar için sapmaları yapılandırma](../warehousing/warehouse-app-detours.md) | Özellik yönetimi:<br>*Warehouse Management mobil uygulaması için çok düzeyli sapmalar* |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde dahil edilen özellik iyileştirmeleri listelenmektedir. Bu iyileştirmelerden her biri, mevcut bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca iyileştirme olduğundan [sürüm planında](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmez. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe).

Bu özelliklerden herhangi birini açmak veya kapatmak istiyorsanız bunu [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) yapmalısınız.

| Modül | Özellik yönetiminde özellik adı | Daha fazla bilgi |
|---|---|---|
| Üretim denetimi | Serbest bırakılacak üretim siparişlerindeki eldeki bilgiler | **Serbest bırakılacak üretim siparişleri** sayfasındaki satırlar bölümünde satır öğesi için eldeki stok miktarı için bir sütun ekler. |
| Taşıma yönetimi | İlgili rota segmentlerine sevkiyat atama | Bu özellik, sistemin tek bir rota boyunca çeşitli segment hedeflerine teslim edilen birden fazla sevkiyata sahip yükler de dahil olmak üzere gönderi navlun maliyetlerini daha doğru bir şekilde paylaştırmasını sağlar. Her sevkiyatı, sevkiyatın ve segmentin hedef adreslerine göre en uygun rota segmentine atar. Bu özellik daha sonra her gönderinin navlun maliyetini, sevkiyatın göreceli ağırlığına, hacmine, miktarına ve kat edilen mesafeye bağlı olarak yükün toplam navlun maliyetinin bir oranı olarak hesaplar. Bu özellik yalnızca Taşıma yönetimi (TMS) modülü kullanılarak yönetilen sevkiyatlar için geçerlidir. |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finans ve Operasyon uygulamaları için Platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.30 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finance ve Operations uygulamalarının 10.0.30 sürümü için platform güncelleştirmeleri (Kasım 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md). <!--KFM: Confirm link -->

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.29 sürümünün parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [KB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) görüntüleyin.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 1 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 2 planına](/dynamics365-release-plan/2022wave2/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) makalesi Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) makalesinde duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
