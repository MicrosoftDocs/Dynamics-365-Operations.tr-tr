---
title: "Çağrı merkezi işlevi"
description: "Bu makale Microsoft Dynamics 365 işlemleri için çağrı merkezi satış işlevlerini genel bir bakış sağlar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf93b1f91679cdb520ead2a12a5e52108a83fbb2
ms.lasthandoff: 03/31/2017


---

# <a name="call-center-functionality"></a>Çağrı merkezi işlevi

Bu makale Microsoft Dynamics 365 işlemleri için çağrı merkezi satış işlevlerini genel bir bakış sağlar.

Microsoft Dynamics AX'teki perakende ve ticaret çağrı merkezlerini bir perakende kanalı türü olarak destekler. Çağrı merkezlerinde, çalışanlar telefonda müşteri siparişlerini alır ve satış siparişleri oluşturur. Çağrı Merkezi işlevi telefon sipariş almak ve müşteri servis sipariş karşılama işlemi boyunca işlemek kolaylaştırmak için tasarlanmış özellikler içerir. Örneğin, çağrı merkezi çalışanlarının doğrudan satış siparişine ödeme bilgileri girebilirsiniz ve bunlar sipariş göndermeden önce ücretleri ve ödemeler ayrıntılı bir özetini görüntüleyebilirsiniz. Çalışanların ayrıca fiyatlandırma denetlemek için seçeneği vardır ve **satış sipariş** sayfasından müşteriler, ürünler ve fiyatları ile ilgili çeşitli verilere erişebilir. Ayrıca, çağrı merkezleri Gelişmiş müşteri geçmişi ve sipariş durumunu izlemek için işlevlere sahiptir. Her bir çağrı merkezinin kendi kullanıcıları, ödeme yöntemleri, fiyat grupları, mali boyutları ve teslimat modları olabilir. Çağrı merkezi oluşturduğunuzda, bu seçenekleri yapılandırabilirsiniz. Ek olarak **çağrı merkezi** sayfasını çağrı merkezlerine özgü aşağıdaki özellikler gruplarını etkinleştirmek veya devre dışı bırakmak için kullanabilirsiniz.

-   **Sipariş tamamlama** – Bu grup ödemelerle ve **satış sipariş** sayfasındaki sipariş tamamlamayla ilgili özellikleri içerir.
-   **Yönlendirilen satış** – Bu grup kaynak kodlar, komut dosyaları ve katalog talepleriyle ilgili özellikleri içerir.

Bu özellikleri çağrı Merkezi ayarlarında etkinleştirdikten sonra **satış sipariş** sayfasında çağrı merkezi ile ilişkili olan kullanıcılar için kullanılabilir. Bu özelliklerin çoğu kullanılabilmesi için önce ek kurulum gerektirir. Kullanıcılar çağrı merkezi siparişleri oluşturmadan üzere önce, bu kullanıcıları çağrı merkezine çağrı merkezi kullanıcıları olarak eklemeniz gerekir. Bu adım çağrı merkezi kanal özgü yapılandırma ve işlevselliği sağlar. Burada, kullanılabilir hale gelen işlevlere bazı örnekler verilmiştir:

-   Destekli satış, tele-satış kodları ve ürün resimleri, siparişler'i alırken satış elemanı rehberlik ve Yardım için yapılandırma seçenekleri sağlar.
-   Siparişler, satış elemanı en az bir ödeme yöntemi yakalayana kadar tamamlanamaz.
-   Üst model satış ve çapraz satış kuralları belirli ürünleri müşteriye tanıtmak satış elemanından istenecek şekilde yapılandırılabilir.
-   Satış elemanı müşteri tarafından sipariş kataloğu için kaynak kodunu yakalayabilir.
-   Satış elemanı satıcısı kuponlarını siparişe ekleyebilir.
-   Satış elemanı süreklilik programları satabilir.
-   Siparişler el ile veya otomatik olarak, sipariş işlenmeden önce ek araştırma olduğunu göstermek için beklemeye alınabilir.



