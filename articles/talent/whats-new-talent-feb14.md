---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (14 Şubat 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
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
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "859402"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a>Dynamics 365 for Talent'daki yenilikler veya değişiklikler (14 Şubat 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Talent'daki yeni veya değişen özellikler açıklanmaktadır.

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
