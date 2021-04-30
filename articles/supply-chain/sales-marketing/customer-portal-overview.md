---
title: Dynamics 365 Supply Chain Management için Müşteri portalına genel bakış
description: Bu konu müşteri portalını tanıtır ve bunu kimin nasıl çalıştığını açıklar.
author: dasani-madipalli
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 9a85cd2590bd9c6cabcd0001d5de81746c1d4f63
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907851"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Dynamics 365 Supply Chain Management için Müşteri portalına genel bakış

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="what-is-the-customer-portal"></a>Müşteri Portalı nedir?

Modern tedarik zinciri sistemleri tümleştirmeye dayanır. Bunlar ayrı bir siloda değil stok, müşteri talebi ve satış bölümlerinin entegre olmasını gerektirir. Müşteri Portalı, Microsoft Dynamics 365 Supply Chain Management'un Bu tümleştirmeyi geliştirmesine ve müşterilerinin bilgilendirilmesi konusunda daha etkili olmasını sağlayan kuruluşlara yardımcı olur.

Müşteri Portalı, şirketler satış siparişi işlemeyle ilişkili senaryolar için dışarıdan bakan işletmeler arası (B2B) bir Web sitesi oluşturmalarına olanak veren bir [Power Apps portal](/powerapps/maker/portals/overview) şablonudur. Şablon, Harici kurumsal müşterilerin şirketin Dynamics 365 ortamından veri görüntülemesini ve oluşturmasını sağlamak için [çift-yazılır](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md), Supply Chain Management ve Power Apps portalları kullanır.

Müşteri Portalı şablonu, Power Apps'in sunduğu tüm özelleştirme yeteneklerine sahiptir. Şablon, şirketin markasını temsil edecek şekilde değiştirilebilir, artırılmış işlevsellik ekleyebilir ve Kullanıcı deneyimini değiştirebilir. Kutunun dışında sunduğu şablonun tüm işlevleri istenildiği şekilde değiştirilebilir.

> [!IMPORTANT]
> Tek başına, şablonun tamamen işlevsel olması beklenmez. Yalnızca dışarıdan bakan bir Web sitesi oluşturmak isteyen müşteriler için Etkinleştirici görevi görür, böylece kuruluş müşterilerinin Supply Chain Management'nden veri ile dedebilmesini sağlar.

> [!NOTE]
> Müşteri Portalı belgeleri, bir Supply Chain Management yüklemesi için müşteri portalını kuran Yöneticiler, özelleştiriciler ve sistem tümleştiricilerine yönlendirilir. Supply Chain Management çalıştıran bir kuruluşun müşterileri olan kişileri açıklamak için _müşteri_ ve _Kullanıcı_ terimlerini kullanır ve son portalı kullanacak.

## <a name="video"></a>Görüntü

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

[Dynamics 365 Supply Chain Management'ta Müşteri portalı şablonuna genel bakış](https://youtu.be/nPrqoLuHfV8) videosu (yukarıda gösterilen), YouTube'daki [Finance and Operations çalma listesinde](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) yer almaktadır.

## <a name="who-should-use-it"></a>Kimler kullanacak?

Müşteri Portalı, Supply Chain Management çalıştıran ve şu özelliklere sahip şirketler için tasarlanmıştır:

- Sipariş işlem bilgilerini (sipariş durumu veya hesap bilgileri gibi) doğrudan Supply Chain Management sisteminden kurumsal müşterilerine ileten dışarıdan bakan bir Web sitesi oluşturmak ister.
- Dynamics AX 2012, Supply Chain Management'a ve daha önce [AX 2012 Müşteri Self Servis Portalı](/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal)'na geçiş yaparken yapılır.

Aşağıdaki organizasyon tipleri Müşteri portalını gerçekleştirmek için uygun aday **değildir**:

- Kurumsal olmayan müşteriler için Web sitesi oluşturmak isteyen şirketler. Bu şirketler bir [Dynamics 365 Commerce e-ticaret Web sitesi](../../commerce/create-ecommerce-site.md) oluşturmayı düşünmelidir.
- Benzer amaçlarla zaten varolan Power Apps Portal Web sitesini kullanan şirketler. Bu şirketler müşteri portalından hiçbir ek yarar almaz. Müşteri Portalı, iki yazma, Supply Chain Management ve Power Apps portallar arasında "noktaları bağlamak" isteyen müşteriler için kılavuz ve başlangıç noktası görevi gören bir şablon olarak teslim edilir. Bu amaca hizmet eden bir Web sitesini önceden ayarladıysanız, bu Web sitesini yeniden sağlamak için müşteri portalı şablonunu kullanmaktan çok daha fazla değer kazanmayabilir.

## <a name="how-does-it-work"></a>Nasıl çalışır?

Müşteri Portalı, Power Apps portal şablonu olarak sağlanır. Bunlar Power Apps portallarına ve çift yazmaya bağlıdır.

[Power Apps portallar](/powerapps/maker/portals/overview), kullanıcıların, kuruluş dışından kişilerin oturum açmasını sağlayan dışarıdan bakan bir Web sitesi oluşturmalarına olanak tanıyan bir özelliktir. Portalları yapmak için bir kod oluşturma gerekmez. Müşteri Portalı, Microsoft tarafından kullanılabilen birçok [Dynamics 365 Portal şablonlarından](/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) biridir.

[Çift yazma](/powerapps/maker/portals/overview), müşteri etkileşimi uygulamaları ile Finance and Operations uygulamaları arasında gerçek zamanlıya yakın etkileşim sağlayan hazır bir altyapı ürünüdür. Çift-yazma, Finance and Operations uygulamalar ve Microsoft Dataverse arasında çift yönlü tümleştirme sağlar. Bu nedenle, uygulamalar arasında tümleşik bir kullanıcı deneyimi sağlar. Müşteri portalı, çift yazma ile eşitlenen tablolara bağlıdır. Supply Chain Management'tan alınan verilerin Müşteri portalında gösterilebilmesi için uygun tüm tablolarda çift yazmanın etkinleştirilmiş olması gerekir.

![Müşteri portalına bağımlılıklar](media/customer-portal-elements.png "Müşteri portalına bağımlılıklar")

Müşteri Portalı, Supply Chain Management yüklemesinden veri kullanan dışarıdan bakan bir Web sitesi oluşturmak amacıyla Power Apps portalları kullanmak isteyen kuruluşlar için bir başlangıç noktası görevi görür. Kuruluşların çift-yazılır, Supply Chain Management ve Power Apps portallara bağlanmasına yardımcı olur.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]