---
title: Dynamics 365 Talent'daki yenilikler veya değişiklikler (7 Ocak 2020)
description: Bu makalede, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462835"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Dynamics 365 Talent'daki yenilikler veya değişiklikler (7 Ocak 2020)

Bu makalede Dynamics 365 Talent'te yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-onboard"></a>Onboard'taki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2697 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>İşe alma kayıtları olmayan çalışanlar silinemez-(386157)

Bu değişiklik, **çalışmayan işçiler** formuna bir silme seçeneği ekler. Çalışan için hiçbir ileri, etkin veya geçmiş istihdam mevcut olduğunda çalışanlar bu formda görünür. Bu sürümde, silme işlemi yalnızca sistem yöneticileri için etkinleştirilir. Ancak, gelecek haftaki sürümde, güvenlik güncelleştirmesi, HR yardımcısı rolüne sahip tüm kullanıcıların istihdam içermeyen çalışanları kaldırmasına olanak verecek şekilde güncelleştirilecektir. Bu değişiklikleri aşağıdaki adımları izleyerek de el ile yapabilirsiniz.

1. **Güvenlik konfigürasyonu**'na gidin.
2. **Ayrıcalıklar** sekmesinde , **çalışanları korumak** için **ayrıcalıklar** listesine filtre uygulayın.
3. **Başvurular** sütununda, **menü öğelerini görüntüle**'yi seçin.
4. **menü öğelerini görüntüle** sütununda, **HcmWOrkersWithoutEmployment**'yi seçin.
5. Izin vermek için **Silme** iznini ayarlayın.
6. **Yayımlanmamış nesneler** sekmesini seçin.
7. **Tümünü yayımla**'yı seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]