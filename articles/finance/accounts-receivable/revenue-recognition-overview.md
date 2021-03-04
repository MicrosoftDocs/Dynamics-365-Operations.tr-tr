---
title: Gelir kabulüne genel bakış
description: Bu konuda, Gelir kabulü özelliğiyle ilgili bilgiler verilir. Bu özellik, birden fazla öğe içeren siparişler için hem gelir fiyatını hem de gelir planını kabul etmeye yönelik şirkete özgü kurallar tanımlamanıza olanak tanıtan esnek bir çerçeve sağlar.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a7e37a0800ec7909f79e5a2354f59c7450995641
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995626"
---
# <a name="revenue-recognition-overview"></a>Gelir kabulüne genel bakış

[!include [banner](../includes/banner.md)]

Ürünler, hizmetler, abonelikler gibi birden fazla öğe satan sektör şirketlerin çok öğeli siparişleri ayırabilmesi gerekir. Böylece, gelir şirkete özel ve sektöre özel kurallar kümesi temel alınarak kabul edilebilir.

> [!NOTE]
> Gelir kabulü özelliği Özellik yönetiminden açılamaz. Şu anda, bu özelliği etkinleştirmek için yapılandırma anahtarları kullanmanız gerekir.

> Paket işlevi dahil olmak üzere gelir kabulünün, Commerce kanallarında (e-ticaret, POS, çağrı merkezi) kullanımı desteklenmez. Gelir kabulü ile yapılandırılan maddeler, Commerce kanallarında oluşturulan siparişlere veya hareketlere eklenmemelidir.

Genel olarak, gelir kabulü işlemi aşağıdaki görevleri gerçekleştirmek için kullanılabilir:

* Uygun gelir fiyatının çok öğeli siparişlerdeki bileşenlerin değerine göre kabul edilmesini sağlamaya yardımcı olmak amacıyla gelir tahsis etmek.
* Gelirin zaman içinde kabul edilmesine yönelik sözleşmedeki zaman aralığını ve yüzdelerini temsil eden bir gelir planını temel alarak geliri ertelemek.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

[Dynamics 365 Finance'ta gelir kabulünü kullanma](https://youtu.be/v3amIsiqvoo) videosu (yukarıda gösterilen) YouTube'daki [Finance and Operations oynatma listesine](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) eklenmiştir.

Gelir kabulü özelliği, hem gelir fiyatını hem de gelir planını kabul etmeye yönelik şirkete özgü kurallar tanımlamanıza olanak tanıyan esnek bir çerçeve sağlar.

Serbest bırakılan ürünler, satış siparişi belgelerinde gelir kabulünü desteklemek amacıyla kullanılır. Serbest bırakılan ürünler, gelir fiyatını ve gelir planını belirlemek için gerekli olan ayarı içerir. Satış siparişi bir Zaman ve malzeme projesinden oluşturulabilir.

Şirketler gelir planı işlevini, gelir fiyatı işlevini kullanmadan kullanabilirler. Bu nedenle, satış siparişi satırlarındaki fiyat, gelir veya ertelenen gelir olarak kullanılır. Satış siparişi satırında bir gelir planı varsa, satış siparişi satırındaki fiyat ertelenir. Satış siparişi satırında gelir planı yoksa, satış siparişi satırındaki fiyat faturalandığında bir gelir hesabına nakledilir.

Gelir fiyatı satış siparişi onayladığında veya fatura deftere nakledildiğinde hesaplanır. Fatura deftere nakledilmeden önce gelir fiyatı önizlemesini görmek için satış siparişini onaylamanız gerekir.

Satış siparişi onaylandığında, herhangi bir satış siparişi satırı bir gelir planına sahipse beklenen bir gelir planı da oluşturulur. Satış siparişi faturalandığında, beklenen gelir planı silinir ve beklenen gelir planı gerçek gelir kabulü planıyla değiştirilir.

Gelir kabulü planının ayrıntıları her satış siparişi satırı için korunur. Bu nedenle, gelir kabulü yöneticisi ayrıntıları görebilir ve sözleşme yükümlülüğü yerine getirildiğinde satırları gelir için serbest bırakabilir. Her dönemin sonunda, gelir kabulü yöneticisi, vadesi tanımladığı tarihte veya öncesinde olan plan satırlarını serbest bırakmak için bir gelir günlüğü oluşturabilir. Bu gelir günlüğü hemen deftere nakledilemez. Bu nedenle, gelir kabulü yöneticisi ertelenen gelirden fiili gelire doğru tutarların serbest bırakıldığını doğrulayabilir.

Sözleşmedeki bir değişiklik var olan satış siparişine veya yeni satış siparişine yeni bir satış siparişi satırı eklenmesine neden olursa satış siparişlerindeki tüm satırlarda gelir fiyatını düzeltmek amacıyla bir yeniden tahsisat işlemi çalıştırılabilir.
