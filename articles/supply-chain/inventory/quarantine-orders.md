---
title: Karantina emirleri
description: Bu konuda, karantina emirlerinin stok durdurma için nasıl kullanıldığı açıklanmaktadır.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14c6f3bae224540968d37de9effa4c430307975c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250884"
---
# <a name="quarantine-orders"></a>Karantina emirleri

[!include [banner](../includes/banner.md)]

Bu konuda, karantina emirlerinin stok durdurma için nasıl kullanıldığı açıklanmaktadır.

Karantina emirleri stok durdurma için kullanılabilir. Örneğin, maddeleri kalite kontrol nedeniyle karantinaya almak isteyebilirsiniz. Karantinaya alınan stok bir karantina ambarına transfer edilir. **Not:** (Ambar yönetiminde) gelişmiş ambar yönetimi işlemleri kullanıyorsanız, karantina emri işleme yalnızca iade satış siparişleri için kullanılır.

## <a name="quarantine-on-hand-inventory-items"></a>Eldeki stok maddelerini karantinaya alın
Maddeleri karantinaya aldığınızda, karantina emirlerini el ile oluşturabilirsiniz veya gelen işleme sırasında karantina emirlerini otomatik olarak oluşturmak için sistemi ayarlayabilirsiniz. Karantina emirlerini otomatik olarak oluşturmak için **Madde modeli grupları** sayfasındaki **Stok ilkeleri** sekmesinde **Karantina yönetimi** seçeneğini seçin. Teslim alma ambarları için **Ambarı karantinaya al** alanında varsayılan bir ambar belirtmeniz de gerekir. Eldeki fiziksel stok satınalma siparişi veya üretim emrinde kaydedildiğinde, karantinaya alınan maddeler otomatik olarak Supply Chain Management'taki karantina ambarına taşınır. Bu taşımanın gerçekleşmesinin nedeni karantina emrinin durumunun **Başladı** olarak değişmesidir. Karantina emirlerini el ile oluşturduğunuzda, ilişkili madde model grubunda karantina yönetimi için maddenin ayarlanmasına gerek yoktur. Bu işlem için karantinaya alınması gereken eldeki stoğu ve kullanılması gereken karantina ambarını belirtmeniz gerekir. Süreci planlamaya yardımcı olması için karantina emri durumlarını kullanabilirsiniz.

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

<a name="additional-resources"></a>Ek kaynaklar
--------

[Stok durdurma](inventory-blocking.md)
