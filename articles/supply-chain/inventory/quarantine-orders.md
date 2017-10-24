---
title: Karantina emirleri
description: "Bu makalede, karantina emirlerinin stok durdurma için nasıl kullanıldığını açıklanmaktadır."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 17dde4a4e3380beb98eeb71c719fb898b40a94f7
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="quarantine-orders"></a>Karantina emirleri

[!include[banner](../includes/banner.md)]


Bu makalede, karantina emirlerinin stok durdurma için nasıl kullanıldığını açıklanmaktadır.

Karantina emirleri stok durdurma için kullanılabilir. Örneğin, maddeleri kalite kontrol nedeniyle karantinaya almak isteyebilirsiniz. Karantinaya alınan stok bir karantina ambarına transfer edilir. **Not:** (Ambar yönetiminde) gelişmiş ambar yönetimi işlemleri kullanıyorsanız, karantina emri işleme yalnızca iade satış siparişleri için kullanılır.

## <a name="quarantine-onhand-inventory-items"></a>Eldeki stok maddelerini karantinaya alma
Maddeleri karantinaya aldığınızda, karantina emirlerini el ile oluşturabilirsiniz veya gelen işleme sırasında karantina emirlerini otomatik olarak oluşturmak için sistemi ayarlayabilirsiniz. Karantina emirlerini otomatik olarak oluşturmak için **Madde modeli grupları** sayfasındaki **Stok ilkeleri** sekmesinde **Karantina yönetimi** seçeneğini seçin. Teslim alma ambarları için **Ambarı karantinaya al** alanında varsayılan bir ambar belirtmeniz de gerekir. Eldeki fiziksel stok satınalma siparişi veya üretim emrinde kaydedildiğinde, karantinaya alınan maddeler otomatik olarak Microsoft Dynamics 365 for Finance and Operations içindeki karantina ambarına taşınır. Bu taşımanın gerçekleşmesinin nedeni karantina emrinin durumunun **Başladı** olarak değişmesidir. Karantina emirlerini el ile oluşturduğunuzda, ilişkili madde model grubunda karantina yönetimi için maddenin ayarlanmasına gerek yoktur. Bu işlem için karantinaya alınması gereken eldeki stoğu ve kullanılması gereken karantina ambarını belirtmeniz gerekir. Süreci planlamaya yardımcı olması için karantina emri durumlarını kullanabilirsiniz.

## <a name="quarantine-order-statuses"></a>Karantina emri durumları
Karantina siparişleri aşağıdaki durumlarda olabilir:

-   Oluşturulma
-   Başladı
-   Bitirildi olarak bildirildi
-   Bitti

### <a name="created"></a>Oluşturulma

Karantina emri el ile oluşturulduğunda, fakat madde henüz karantina ambarına yerleştirilmediğinde karantina emrinin durumu **Oluşturuldu** olur. İki stok hareketi oluşturulur. Bir hareket, durumu **Siparişte**, **Fiziksel olarak ayrıldı** veya **Çekildi** olan çıkış hareketidir. Diğer hareket ise karantina ambarında durumu **Sipariş edildi** veya **Kayıtlı** olan giriş hareketidir. Normal işlemleri kullanarak stok güncelleştirmelerini ayırabilir, seçebilir ve kaydedebilirsiniz.

### <a name="started"></a>Başladı

Bir karantina emrinin durumu **Başlatıldı** ise, stok normal ambardan karantina ambarına taşınır ve iki stok hareketi oluşturulur. Bir hareketin durumu **kesinti yapıldı** ve diğer hareket durumu **alınan**. Aynı zamanda, iade aktarımının işlenmesi için iki stok hareketi oluşturulur. Bu hareketler tarihli değildir. Bir hareketin durumu **Ayrıldı fiziksel** ve diğer hareket durumu **sipariş edildi**.

### <a name="reported-as-finished"></a>Bitirildi olarak bildirildi

**Tamamlandı olarak bildir**'e tıklayarak başlatılan bir karantina siparişinin tamamlandığını bildirebilirsiniz. Madde karantinadan serbest bırakılır fakat henüz normal ambara geri taşınmaz. Normal ambara taşıma Rapor sırasında başlatılabilen Madde varış günlüğü ile tamamlanmış olarak işlenebilir.

### <a name="ended"></a>Bitti

Karantina emri sonlandırıldığında, madde karantina ambarından normal ambara geri taşınır. Madde hareketinin durumu karantina ambarında **satıldı** ve normal ambarda **satın alınan** olarak ayarlanır.

## <a name="quarantine-order-scrap"></a>Karantina siparişi hurda
Karantina emri işleminin bir parçası olarak stoğu hurdaya çıkartabilirsiniz. Hurdayı işlerken, stoğun durumu karantina ambarından çıkış hareketi tarafından **Satıldı** olarak ayarlanacaktır.

<a name="see-also"></a>Ayrıca bkz.
--------

[Stok durdurma](inventory-blocking.md)

