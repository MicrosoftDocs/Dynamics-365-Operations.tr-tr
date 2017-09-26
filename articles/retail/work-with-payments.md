---
title: "Bir çağrı merkezindeki ödeme yöntemleri"
description: "Bu konu Dynamics 365 for Retail içerisinde bir çağrı merkezinde kullanabileceğiniz farklı ödeme yöntemlerini ele alır."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 07cb1bcb3870b96e34f7f6725fe5b7da32628fde
ms.contentlocale: tr-tr
ms.lasthandoff: 06/20/2017

---

# <a name="payment-methods-in-a-call-center"></a>Bir çağrı merkezindeki ödeme yöntemleri

[!include[banner](includes/banner.md)]


Bu konu Dynamics 365 for Retail içerisinde bir çağrı merkezinde kullanabileceğiniz farklı ödeme yöntemlerini ele alır.

Diğer kanallarında kullanılan nakit, çek, kredi kartı ve hediye kartı gibi ödeme yöntemleri çağrı merkezlerinde de kullanılabilir. Çağrı merkezi için bir ödeme yöntemi ayarladıktan sonra bu yöntem çağrı merkezi kullanıcılarının **Satış siparişi** sayfasındaki **Ödemeler** bölümündeki seçeneklerden biri olarak görüntülenir. Ayrıca kuruluşunuzun çağrı merkezi üzerinden sipariş veren müşterilere indirim sunmak üzere kuponlar da ayarlayabilirsiniz. Kuponlar indirimi sabit tutarda veya madde fiyatının veya sipariş toplamının yüzdesi olarak sunabilir. Örneğin tutar tabanlı bir kupon, müşteri 750,00 veya üzerinde harcama yaptığında 75,00 indirim sağlayabilir. Farklı kupon türleri oluşturabilir, üst/alt kuponları ayarlayabilir ve bir kuponu kopyalayabilir veya geçersiz kılabilirsiniz. Kupon oluşturmak için  aşağıdaki tabloda gösterilen seçenekleri kullanın.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Öznitelik**             | **Paraya çevrilme oranı** alanına kuponun beklenen paraya çevrilme oranını yüzde olarak girin ve kuponun tek kullanımlık kupon olup olmadığını, otomatik olarak yeniden çıkarılıp çıkarılmayacağını veya belirli bir müşteriye özel olup olmadığını seçin.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Geçerli**                 | **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına kuponun geçerli olduğu ilk ve son tarihleri girin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Kuralları dahil et/dışarıda bırak** | **Kataloglar** ve **Maddeler** alanlarında, kupona dahil edilen veya dışarıda bırakılan katalog veya madde olup olmadığını seçin. **Dahil et** veya **Dışarıda Bırak** seçeneğini belirlerseniz, **Ayarlar**'a tıklayın, **Katalogları dahil et/dışarıda bırak** veya **Ürünleri dahil et/dışarıda bırak** seçeneklerinden birini belirletin ve katalog veya madde hakkında bilgileri girin. Bu alanlarda **Hiçbiri** seçeneğini belirlerseniz tüm kataloglar veya maddeler kupona dahil edilir.                                                                                                                                                                                                                          |
| **Çeşitli**         | Bu kupon başka indirimlerle birlikte kullanılamazsa **Özel** onay kutusunu seçin. Daha sonra, **Kaynak** alanında kuponun kullanılabileceği yerleri seçin. B kupon bir üretici kuponuysa **Üretici kuponu** onay kutusunu seçin.                                                                                                                                                                                                                                                                                                                                                                |
| **Gelecekteki kupon**         | Bu kupon üst kupon olarak diğer kuponlarla ilişkilendirilecekse **Üst kupon** onay kutusunu seçin. Bu kupon alt kupon olarak mevcut bir kuponla ilişkilendirilecekse **Üst kupon kimliği** alanından üst kuponu seçin. Örneğin gelecek bahar dönemine ait katalog için bir kupon oluşturuyorsunuz. Bahar kataloğu için oluşturduğunuz tüm diğer kuponlar bahar kataloğu kuponunun alt kuponu olacaktır. Alt kuponlar yeni müşteri siparişleri için yüzde 20 indirim, yeni sunulan bir madde için yüzde 10 indirim veya 1.000,00 veya üzerindeki siparişlerde 95,00 indirim içerebilir. |

**Satış siparişi** sayfasından bir kredi kartı ödemesi gönderip kartın yetkili olmadığına ilişkin bir ileti alırsanız, yetkilendirme işlemini el ile gerçekleştirebilirsiniz. **Yetkilendirme yönetimi** sayfasını kullanarak bir kredi kartı hareketini yetkilendirebilir, reddedebilir veya yeniden gönderebilirsiniz. Ek ödeme işleme seçeneklerini yapılandırmak için çağrı merkezi parametreleri sayfasını kullanın:

-   Çek tutmaları finans personelinin ödeme yöntemi olarak çekin kullanıldığı ve çek tutması eşiği tutarının aşıldığı siparişleri işlemesine olanak tanır. Çek tutma durumu el ile serbest bırakılabilir veya yapılandırılan süre sonunda otomatik olarak sona erer.
-   Çek ve kredi kartı üzerinden yapılan geri ödemelerin el ile onaylanması gereken tutarın üzerinde eşikler ayarlayabilirsiniz. Eşik tutarını aşan tüm geri ödemeler onay sırasına eklenir. Geri ödemeyi onayladıktan sonra iade satış siparişi faturalandırılabilir.





