---
title: Mühendislik değişikliği yönetimine genel bakış
description: Bu konuda, ürün sürümü oluşturma ve yönetme, ürün yaşam döngüleri ve mühendislik değişikliklerini yönetmenize yardımcı olan mühendislik değişikliği yönetimine genel bir bakış sağlanmaktadır.
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b081cd8d56217b8cf76db824c29482d453fc9ea3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001960"
---
# <a name="engineering-change-management-overview"></a>Mühendislik değişikliği yönetimine genel bakış

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Özellik özeti

Günümüzde üreticiler; sürekli kısalan ürün yaşam döngüleri, yüksek kalite ve güvenilirlik gereksinimleri ve ürün güvenliğine daha fazla önem vermeyi gerektiren koşullarda başarılı olmak için güçlü ürün verileri yönetimi, sürüm denetimi ve mühendislik değişikliği yönetimine ihtiyaç duymaktadır.

Mühendislik değişikliği yönetimi yapıyı ve disiplini ürün verileri yönetim süreciyle birleştirir ve ürünlerin iş akışları tarafından desteklenen denetimli bir şekilde tanımlanmasını, serbest bırakılmasını ve gözden geçirilmesini sağlar. Ürün sürümleri ve mühendislik değişikliği yönetimi aracılığıyla, mühendislik değişikliklerinin etkisini değerlendirebilir ve bu değişiklikleri ürün yaşam döngüsü boyunca uygulayabilirsiniz.

Mühendislik değişikliği yönetimi, ürün sürümü oluşturma ve yönetme, ürün yaşam döngüleri ve mühendislik değişikliklerini yönetmenize yardımcı olur. Temel özelliklerinin listesi aşağıdadır:

- Ürün sürümü oluşturma
- Ürün ana verilerini tek bir tüzel kişilikte (mühendislik şirketi) korumanıza ve tamamıyla yapılandırılmış, piyasaya sunulmuş ürünü diğer tüzel kişiliklere yayımlamanıza olanak tanıyan geliştirilmiş ürün sürümü işlevleri
- Bir ürün sürümü etkinleştirilmeden önce gerekli bilgilerin girildiğini doğrulayan kurallar (hazırlık denetimleri)
- Piyasaya sunulan bir ürünün belirli iş süreçlerinde kullanılabileceği durumlarda ayrıntılı denetim aracılığıyla geliştirilmiş ürün yaşam döngüsü yönetimi
- İş akışları tarafından desteklenen mühendislik değişikliği istekleri
- İş akışları tarafından desteklenen mühendislik değişikliği siparişleri

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Önceki video ([Dynamics 365 Supply Chain Management'taki değişiklik yönetimi özellikleri](https://youtu.be/N313FqvRuBc)) YouTube'daki [Finance and Operations oynatma listesinde](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) yer almaktadır.

## <a name="turn-on-engineering-change-management-for-your-system"></a>Sisteminiz için mühendislik değişikliği yönetimini açma

Önce, aşağıdaki adımları izleyerek mühendislik değişikliği yönetimini açın.

1. [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin.
1. Güncelleştirmeleri denetleyin.
1. **Mühendislik Değişikliği Yönetimi** adlı özelliği açın.

Sonra, aşağıdaki adımları izleyerek **Mühendislik değişikliği Yönetimi** yapılandırma anahtarını açın.

1. Sisteminizi [Bakım modu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım moduna alın.
1. **Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin.
1. **Ticaret** düğümünü genişletin ve **Mühendislik Değişikliği Yönetimi** onay kutusunu işaretleyin.
1. [Bakım modu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım modunu kapatın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]