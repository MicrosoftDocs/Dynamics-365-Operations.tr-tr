---
title: "Yeni üretilmiş bir madde için standart maliyetleri güncelleştirme"
description: "Bu makalede, yeni üretilen bir madde için standart maliyetlerin güncellenmesine yönelik yönergeler sağlanmıştır."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1cfb04a98f7d01f7766bea97157ca3c44c51e326
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-for-a-new-manufactured-item"></a>Yeni üretilmiş bir madde için standart maliyetleri güncelleştirme

[!include[banner](../includes/banner.md)]


Bu makalede, yeni üretilen bir madde için standart maliyetlerin güncellenmesine yönelik yönergeler sağlanmıştır. 

Aşağıdaki yönergelerde, standart maliyetleri iki sürümlü bir yaklaşım kullanarak güncellediğiniz varsayılmaktadır. Bu yaklaşımda bir maliyet sürümü orijinal olarak donmuş dönem için tanımlanmış olan standart maliyetleri, ikinci maliyetlendirme sürümü ise yeni üretilen maddelere ait artımlı güncellemeleri içerir. Artımlı güncelleştirmeler ikinci maliyetlendirme versiyonu içersindeki maliyet kayıtları olarak girilir ve en sonunda etkinleştirilir. İki sürümlü yaklaşım ikinci bir maliyetlendirme sürümü tanımlamanızı gerektirir. Bu maliyetlendirme sürümünü tanımlamaya yönelik yönergeler şunlardır:

-   **Standart maliyet** için bir maliyetlendirme tipi atayın.
-   Maliyetlendirme sürümünün içeriklerini belirtmek için **2016-UPDATES** gibi anlamlı bir tanımlayıcı atayın.
-   **Fiyat türlerine izin ver** alan grubunda, **Maliyet fiyatı** öğesinin **Evet** konumuna ayarlandığından emin olun.
-   Tüm sahalar için girilecek maliyet kayıtlarına izin verin (yani, **Saha** alanını boş bırakın). Bir tesis girerseniz, maliyet kayıtları yalnızca o tesis için girilebilir.
-   **Etkin** maliyetler için bir geri dönüş ilkesi kullanın.

Donmuş dönem boyunca yeni üretilmiş maddeler eklemek için aşağıdaki adımları takip edin.

1.  Maliyet kayıtlarının artışlı güncelleştirmeler içeren ikinci maliyetlendirme sürümüne girilebilmesini sağlamak için **Maliyetlendirme sürümü** ayarlar sayfasını kullanın. Bekleyen maliyetlerin etkinleştirilmesini önleyin; etkinleştirmeye bekleyen maliyetler tamamen ve doğru şekilde tanımlandıktan sonra izin verilir. Maliyetlendirme versiyonunda bir ilke olarak boş bir başlangıç tarihi belirtin ve her maliyet kaydını girdiğiniz başlangıç tarihini girin. Başlangıç tarihi, yeni maddelerin satın alınmasından veya üretilmesinden önceki bir tarihi temsil etmelidir.
2.  Yeni satın alınan maddeler için maliyet kayıtları girmek amacıyla **Madde fiyatı** sayfasını kullanın. Her maliyet kaydı için, artımlı güncelleştirmeleri içeren maliyetlendirme versiyonunu girin ve yeni üretilmiş maddeler için, öngörülen üretim tarihinden önce olan bir başlangıç tarihi kullanın.
3.  **Hesaplama** sayfasını kullanarak yeni üretilmiş maddelerin maliyetini hesaplayın. **Hesaplama** sayfasını **Maliyetlendirme sürümü bakımı** sayfasından açın ve ardından artışlı güncelleştirmeleri içeren maliyet sürümünü seçin. Yeni üretilmiş madde ile üretilmiş bileşenlerinden birini belirlemek için seçme ölçütlerini kullanın. Bileşen olarak yeni üretilmiş maddeler içeren ana maddeleri (çok düzeyli bir ürün yapısı içerisinde) tanımlamak da gerekli olabilir. Yeni üretilmiş maddelerin üretiminin başlangıcına karşılık gelen ürün reçetesi (BOM) hesaplaması için bir başlangıç tarihi girin. Başlangıç tarihi, maddenin ürün reçetesi ve rota versiyonu için olan yürürlük tarihleri arasında olmalıdır. **Not:** Eksik bir maliyet kaydı yeni bir üretilen maddeyi işaret ediyor olabilir. Ürün reçetesi hesaplamaları, maliyetleri eksik olan öğelerle sınırlı olabilir.
4.  Eksiklik olmaması ve doğruluğun sağlanması için yeni üretilmiş maddelerin hesaplanan maliyetlerini kontrol edin. Her bir madde maliyeti kaydı için hesaplanan maliyetleri ve ayrıca Infolog uyarı mesajlarını gözden geçirmek için **Tamamla** sayfasını kullanın. Alternatif olarak hesaplanan maliyetleri gözden geçirmek için **Hesaplama** sayfasını kullanın.
5.  İkinci maliyetlendirme sürümünde bekleyen maliyet kayıtlarının etkinleştirilmesine izin vermek için engelleme bayrağını değiştirmek üzere **Maliyetlendirme sürüm kurulumu** sayfasını kullanın.
6.  İkinci maliyetlendirme sürümüne alınmış tüm bekleyen maliyet kayıtlarını etkinleştirmek için **Etkin fiyatlar** sayfasını (**Maliyetlendirme sürüm bakımı** sayfasından açabilirsiniz) kullanın. Tek tek maddelere yönelik bekleyen maliyet kayıtlarını **Madde fiyatı** sayfasında **Madde fiyatı** düğmesine tıklayarak da etkinleştirebilirsiniz.
7.  Ek veri bakımını önlemek için, **Maliyetlendirme sürümü ayarları** sayfasını kullanarak ikinci maliyetlendirme sürümüne alınmış engelleme bayraklarını değiştirin. Durdurma ilkeleri yeni bekleyen maliyetler girilmesini ve bekleyen maliyetlerin etkinleştirilmesini önler.





