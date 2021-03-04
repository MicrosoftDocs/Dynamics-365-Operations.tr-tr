---
title: Dynamics 365 Talent'taki yenilikler veya değişiklikler (14 Şubat 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462838"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a>Dynamics 365 Talent'taki yenilikler veya değişiklikler (14 Şubat 2019)

Bu konuda, Talent'taki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler
Bu sürümde küçük hata gidermeleri vardır.

## <a name="changes-in-onboarding"></a>İş almadaki değişiklikler
Bu sürümde küçük hata gidermeleri vardır.
 
## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler 
**Derleme 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>Personel sabit ücret varlığı tüm kayıtları dışa aktarmaz
Bu değişiklik ile **Personel sabit ücret** varlığı şimdi tüm kayıtlara dışa aktarır. Bu varlık, personeller için mevcut sabit ücret kayıtlarını oluşturmak ve güncelleştirmekte kullanılabilir. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>Çalışma sonlandırma tarihi, personelin tercih ettiği saat dilimi ayarlarını dikkate almaz.
Çalışma sonlandırma tarihleri, artık kullanıcı tarafından tercih edilen saat dilimlerini, bir şirket ile çalışma oluştururken veya sonlandırırken artık dikkate almaktadır.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Analizlerdeki İngiltere adresleri, Doğu İsviçre adresleri olarak görüntülenmektedir
Bu sürümde, bir değişiklik **Personel Yönetimi** "Konuma göre kişi sayısı" raporundaki hatalı hizalamaları düzeltmek üzere yapılmıştır.
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>Sonlandırma kodu çalışanın pozisyon atama kaydında, pozisyonu sonlandırırken doldurulmamıştır.
Bir personelin konum atamasını sonlandırırken, bir değişiklik varsayılan "Sonlandırma sebebi" koduna yapılmıştır.

### <a name="new-entity-created-for-job-compensation-levels"></a>İş ücret düzeyleri için yeni varlık oluşturuldu
Yeni bir veri yönetimi çerçevesi (DMF) varlığı oluşturuldu. Varlık, sistemde tanımlanmış her iş için ücret seviyeleri, piyasa değerleri ve anket bilgisi için oluşturma ve güncelleştirme sağlar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]