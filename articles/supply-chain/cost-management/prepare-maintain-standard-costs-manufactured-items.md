---
title: Üretilmiş maddeler için standart maliyetleri sürdürmeye hazırlanma
description: Bu konu üretilmiş maddeler için maliyetleri korumaya hazırlanmayla ilgili adımları açıklar.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbd7344f3d542cbd46e3568d8a7911ab4ab53b17
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "350631"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Üretilmiş maddeler için standart maliyetleri sürdürmeye hazırlanma

[!include [banner](../includes/banner.md)]

Bu konu üretilmiş maddeler için maliyetleri korumaya hazırlanmayla ilgili adımları açıklar. Üretilmiş maddelerle ilgili adımlar satın alınan maddelerle ilgili adımlardan biraz farklıdır.

Üretilmiş maddelere atanan ilkeler, üretilmiş üst maddelere ait maliyet hesaplarını etkileyebilir. Üretilmiş maddeler için standart maliyetleri korumaya hazırlanmak için aşağıdaki adımları uygulayın.

1. Üretilmiş maddeye bir madde modeli grubu atayın. 

   Madde modeli grubu standart maliyetlerin kullanılacağını belirler.

2. Üretilmiş maddeye bir madde grubu atayın. 

   Madde grubu, üretilmiş maddeye uygulanan genel muhasebe hesaplarını içerir. Bir standart maliyet stok modeli içeren üretilmiş bir maddenin genel muhasebe hesapları çeşitli üretim farklılıkları, maliyet değişim farklılığı ve stok maliyeti yeniden değerleme içerir.

3. Maddeye stok ölçüm birimi atayın. 

   Maddenin maliyetleri her zaman maddenin stok ölçüm biriminde ifade edilir.

4. Üretilmiş maddeye, satın alınmış madde gibi ele alınmadığı sürece bir maliyet grubu atamayın.

5. Üretilmiş maddeye bir ürün reçetesi (BOM) hesap grubu atayın. 

   Maddenin ürün reçetesi hesaplama grubu uygulanacak uyarı durumlarını belirler. Bu şekilde, bir ürün reçetesi hesaplaması yapıldığında, olası hesaplama hatalarının kaynakları hakkında uyarı iletileri oluşturulabilir. Örneğin, bir hata iletisi bir etkin ürün reçetesi veya rotanın olmadığı durumları belirleyebilir. Ürün reçetesi hesap gurubu, üretilmiş bir maddenin ne zaman satın alınan bir madde gibi ele alınması gerektiğini gösteren açılım durdurma ilkesi içerir.

6. Üretilmiş maddenin sabit maliyetleri varsa üretilmiş maddeye standart bir sipariş miktarı atayın. 

   Standart sipariş miktarı, sabit maliyetlerin itfa edilmesi için bir muhasebe lot boyutudur. Sabit maliyet örnekleri rota operasyonlarındaki kurulum sürelerini ve bir ürün reçetesindeki sabit bileşen miktarını içerir.

7. Üretilmiş madde için ürün reçetesini tanımlayın. 

   Üretilmiş madde için bir veya daha fazla ürün reçetesi tanımlanabilir. İstediğiniz versiyonların onaylanmış ve etkin olarak işaretlendiğini ve istediğiniz geçerlilik tarihlerine sahip olduklarını kontrol edin. Ürün reçetesi versiyonu şirket çağında veya tesise özel olabilir.

8. Üretilmiş madde için rotayı tanımlayın. 

   Üretilmiş madde için bir veya daha fazla rota tanımlanabilir. İstediğiniz versiyonların onaylanmış ve etkin olarak işaretlendiğini ve istediğiniz geçerlilik tarihlerine sahip olduklarını kontrol edin. Rota versiyonunun tesise özel olması gerekir.

Rota bilgilerini maliyetlendirme amaçlı kullanmak istemeniz durumunda ek hazırlık adımları gerekir. Örneğin, rota operasyonlarına atanan maliyet kategorilerinin doğru ve tam olması gerekir.

<a name="related-topics"></a>İlgili konular
--------

[Üretilen maddeler için sabit maliyetlerin itfası](amortize-constant-costs-manufactured-item.md)

[Üretilen ya da temin edilen ürünleri ayarlama](manufactured-items-treated-as-purchased-items.md)

