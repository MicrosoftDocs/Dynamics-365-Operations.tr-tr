---
title: Gelir kabulüne genel bakış (video içerir)
description: Bu makalede Gelir kabulü özelliğiyle ilgili bilgi verilir. Bu özellik, birden fazla öğe içeren siparişler için hem gelir fiyatını hem de gelir planını kabul etmeye yönelik şirkete özgü kurallar tanımlamanıza olanak tanıtan esnek bir çerçeve sağlar.
author: bking
ms.date: 03/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 5bf07356b5613f438034f8dabac7db197e69a6c8
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644043"
---
# <a name="revenue-recognition-overview"></a>Gelir kabulüne genel bakış

[!include [banner](../includes/banner.md)]

>[!NOTE]
>Bu işlev Ekim 2023'te kullanımdan kaldırılacağı için yeni kullanıcılar abonelik faturalaması kullanmalıdır.

Ürünler, hizmetler, abonelikler gibi birden fazla öğe satan sektör şirketlerin çok öğeli siparişleri ayırabilmesi gerekir. Böylece, gelir şirkete özel ve sektöre özel kurallar kümesi temel alınarak kabul edilebilir.

Paket işlevi dahil olmak üzere gelir kabulünün, Commerce kanallarında (e-ticaret, POS, çağrı merkezi) kullanımı desteklenmez. Gelir kabulü ile yapılandırılan maddeler, Commerce kanallarında oluşturulan siparişlere veya hareketlere eklenmemelidir.

Genel olarak, gelir kabulü işlemi aşağıdaki görevleri gerçekleştirmek için kullanılabilir:

* Uygun gelir fiyatının çok öğeli siparişlerdeki bileşenlerin değerine göre kabul edilmesini sağlamaya yardımcı olmak amacıyla gelir tahsis etmek.
* Gelirin zaman içinde kabul edilmesine yönelik sözleşmedeki zaman aralığını ve yüzdelerini temsil eden bir gelir planını temel alarak geliri ertelemek.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

[Dynamics 365 Finance'te gelir kabulünü kullanma](https://youtu.be/v3amIsiqvoo) videosu (yukarıda gösterilen) YouTube'daki [Finans ve operasyon oynatma listesine](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) eklenmiştir.

Gelir kabulü özelliği, hem gelir fiyatını hem de gelir planını kabul etmeye yönelik şirkete özgü kurallar tanımlamanıza olanak tanıyan esnek bir çerçeve sağlar.

Serbest bırakılan ürünler, satış siparişi belgelerinde gelir kabulünü desteklemek amacıyla kullanılır. Serbest bırakılan ürünler, gelir fiyatını ve gelir planını belirlemek için gerekli olan ayarı içerir. Satış siparişi bir Zaman ve malzeme projesinden oluşturulabilir.

Şirketler gelir planı işlevini, gelir fiyatı işlevini kullanmadan kullanabilirler. Bu nedenle, satış siparişi satırlarındaki fiyat, gelir veya ertelenen gelir olarak kullanılır. Satış siparişi satırında bir gelir planı varsa, satış siparişi satırındaki fiyat ertelenir. Satış siparişi satırında gelir planı yoksa, satış siparişi satırındaki fiyat faturalandığında bir gelir hesabına nakledilir.

Gelir fiyatı satış siparişi onayladığında veya fatura deftere nakledildiğinde hesaplanır. Fatura deftere nakledilmeden önce gelir fiyatı önizlemesini görmek için satış siparişini onaylamanız gerekir.

Satış siparişi onaylandığında, herhangi bir satış siparişi satırı bir gelir planına sahipse beklenen bir gelir planı da oluşturulur. Satış siparişi faturalandığında, beklenen gelir planı silinir ve beklenen gelir planı gerçek gelir kabulü planıyla değiştirilir.

Gelir kabulü planının ayrıntıları her satış siparişi satırı için korunur. Bu nedenle, gelir kabulü yöneticisi ayrıntıları görebilir ve sözleşme yükümlülüğü yerine getirildiğinde satırları gelir için serbest bırakabilir. Her dönemin sonunda, gelir kabulü yöneticisi, vadesi tanımladığı tarihte veya öncesinde olan plan satırlarını serbest bırakmak için bir gelir günlüğü oluşturabilir. Bu gelir günlüğü hemen deftere nakledilemez. Bu nedenle, gelir kabulü yöneticisi ertelenen gelirden fiili gelire doğru tutarların serbest bırakıldığını doğrulayabilir.

Sözleşmedeki bir değişiklik var olan satış siparişine veya yeni satış siparişine yeni bir satış siparişi satırı eklenmesine neden olursa satış siparişlerindeki tüm satırlarda gelir fiyatını düzeltmek amacıyla bir yeniden tahsisat işlemi çalıştırılabilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

