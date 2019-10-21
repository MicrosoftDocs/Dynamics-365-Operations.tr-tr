---
title: Gelir kabulüne genel bakış
description: Bu konuda, Gelir kabulü özelliğiyle ilgili bilgiler verilir. Bu özellik, birden fazla öğe içeren siparişler için hem gelir fiyatını hem de gelir planını kabul etmeye yönelik şirkete özgü kurallar tanımlamanıza olanak tanıtan esnek bir çerçeve sağlar.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: d1aeb0cf556582ff53ca00c6bb8d863a088950b9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184129"
---
# <a name="revenue-recognition-overview"></a>Gelir kabulüne genel bakış

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> Gelir kabulü özelliği henüz Özellik yönetiminden açılamamaktadır. Şu anda, bu özelliği etkinleştirmek için yapılandırma anahtarları kullanmanız gerekir.

Ürünler, hizmetler, abonelikler gibi birden fazla öğe satan sektör şirketlerin çok öğeli siparişleri ayırabilmesi gerekir. Böylece, gelir şirkete özel ve sektöre özel kurallar kümesi temel alınarak kabul edilebilir.

Genel olarak, gelir kabulü işlemi aşağıdaki görevleri gerçekleştirmek için kullanılabilir:

* Uygun gelir fiyatının çok öğeli siparişlerdeki bileşenlerin değerine göre kabul edilmesini sağlamaya yardımcı olmak amacıyla gelir tahsis etmek.
* Gelirin zaman içinde kabul edilmesine yönelik sözleşmedeki zaman aralığını ve yüzdelerini temsil eden bir gelir planını temel alarak geliri ertelemek.

Gelir kabulü özelliği, hem gelir fiyatını hem de gelir planını kabul etmeye yönelik şirkete özgü kurallar tanımlamanıza olanak tanıtan esnek bir çerçeve sağlar.

Serbest bırakılan ürünler, satış siparişi belgelerinde gelir kabulünü desteklemek amacıyla kullanılır. Serbest bırakılan ürünler, gelir fiyatını ve gelir planını belirlemek için gerekli olan ayarı içerir. Satış siparişi bir Zaman ve malzeme projesinden oluşturulabilir.

Şirketler gelir planı işlevini, gelir fiyatı işlevini kullanmadan kullanabilirler. Bu nedenle, satış siparişi satırlarındaki fiyat, gelir veya ertelenen gelir olarak kullanılır. Satış siparişi satırında bir gelir planı varsa, satış siparişi satırındaki fiyat ertelenir. Satış siparişi satırında gelir planı yoksa, satış siparişi satırındaki fiyat faturalandığında bir gelir hesabına nakledilir.

Gelir fiyatı satış siparişi onayladığında veya fatura deftere nakledildiğinde hesaplanır. Fatura deftere nakledilmeden önce gelir fiyatı önizlemesini görmek için satış siparişini onaylamanız gerekir.

Satış siparişi onaylandığında, herhangi bir satış siparişi satırı bir gelir planına sahipse beklenen bir gelir planı da oluşturulur. Satış siparişi faturalandığında, beklenen gelir planı silinir ve beklenen gelir planı gerçek gelir kabulü planıyla değiştirilir.

Gelir kabulü planının ayrıntıları her satış siparişi satırı için korunur. Bu nedenle, gelir kabulü yöneticisi ayrıntıları görebilir ve sözleşme yükümlülüğü yerine getirildiğinde satırları gelir için serbest bırakabilir. Her dönemin sonunda, gelir kabulü yöneticisi vadesi tanımladığı tarihte veya öncesinde olan plan satırlarını serbest bırakmak için bir gelir günlüğü oluşturabilir. Bu gelir günlüğü hemen deftere nakledilemez. Bu nedenle, gelir kabulü yöneticisi ertelenen gelirden fiili gelire doğru tutarların serbest bırakıldığını doğrulayabilir.

Sözleşmedeki bir değişiklik var olan satış siparişine veya yeni satış siparişine yeni bir satış siparişi satırı eklenmesine neden olursa satış siparişlerindeki tüm satırlarda gelir fiyatını düzeltmek amacıyla bir yeniden tahsisat işlemi çalıştırılabilir.
