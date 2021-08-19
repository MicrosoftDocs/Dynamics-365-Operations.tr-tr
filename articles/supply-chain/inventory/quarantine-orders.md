---
title: Karantina emirleri
description: Bu konuda, karantina emirlerinin stok durdurma için nasıl kullanıldığı açıklanmaktadır.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7676c6520fd7ed6e66dad11b23fae23f15ecba53c8bc4b62c193ee3643fb798e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718047"
---
# <a name="quarantine-orders"></a>Karantina emirleri

[!include [banner](../includes/banner.md)]

Bu konuda, karantina emirlerinin stok durdurma için nasıl kullanıldığı açıklanmaktadır.

Karantina emirleri, stoğu durdurmanıza olanak sağlar. Örneğin, maddeleri kalite kontrol nedeniyle karantinaya almak isteyebilirsiniz. Karantinaya alınan stok bir karantina ambarına transfer edilir.

> [!NOTE]
> (Ambar yönetiminde) gelişmiş ambar yönetimi işlemleri kullanıyorsanız, karantina emri işleme yalnızca iade satış siparişleri için kullanılır.

## <a name="quarantine-on-hand-inventory-items"></a>Eldeki stok maddelerini karantinaya alın

Maddeleri karantinaya aldığınızda, karantina emirlerini el ile oluşturabilirsiniz veya gelen işleme sırasında karantina emirlerini otomatik olarak oluşturmak için sistemi ayarlayabilirsiniz.

Sistemi karantina emirlerini otomatik olarak üretecek şekilde ayarlamak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Stok \> Madde modeli grupları** öğesine gidin.
1. Liste bölmesinde ilgili bir model grubu seçin veya yeni bir model grubu oluşturun.
1. **Stok ilkeleri** hızlı sekmesinde, **Karantina yönetimi** onay kutusunu seçin.
1. Sayfayı kapatın.
1. Teslim alma ambarları için **Ambarı karantinaya al** alanında varsayılan bir ambar alanı belirtin.

Ambarda alındı olarak kaydedilen bir madde **Karantina yönetimi** onay kutusunun seçildiği bir model grubuna aitse sistem bunun için bir karantina emiri oluşturur. Karantina emiri, çalışanların maddeyi karantina ambarına taşıması gerektiğini belirtir.

Karantina emirlerini el ile oluşturduğunuzda, **Karantina emirleri** sayfasında ilişkili madde model grubunda karantina yönetimi için maddenin ayarlanmasına gerek yoktur. Bu işlem için karantinaya alınması gereken eldeki stoğu ve kullanılması gereken karantina ambarını belirtmeniz gerekir. Süreci planlamaya yardımcı olması için karantina emri durumlarını kullanabilirsiniz.

## <a name="quarantine-order-statuses"></a>Karantina emri durumları

Karantina siparişleri aşağıdaki durumlarda olabilir:

- Oluşturulma
- Başladı
- Bitirildi olarak bildirildi
- Bitti

### <a name="created"></a>Oluşturulma

Karantina emri el ile oluşturulduğunda, fakat madde henüz karantina ambarına yerleştirilmediğinde karantina emrinin durumu **Oluşturuldu** olur. İki stok hareketi oluşturulur. Bir hareket, durumu **Siparişte**, **Fiziksel olarak ayrıldı** veya **Çekildi** olan çıkış hareketidir. Diğer hareket ise karantina ambarında durumu **Sipariş edildi** veya **Kayıtlı** olan giriş hareketidir. Normal işlemleri kullanarak stok güncelleştirmelerini ayırabilir, seçebilir ve kaydedebilirsiniz.

### <a name="started"></a>Başladı

Bir karantina emrinin durumu **Başlatıldı** ise, stok normal ambardan karantina ambarına taşınır ve iki stok hareketi oluşturulur. Bir hareketin durumu **kesinti yapıldı** ve diğer hareket durumu **alınan**. Aynı zamanda, iade aktarımının işlenmesi için iki stok hareketi oluşturulur. Bu hareketler tarihli değildir. Bir hareketin durumu **Ayrıldı fiziksel** ve diğer hareket durumu **sipariş edildi**.

### <a name="reported-as-finished"></a>Tamamlandığı bildirildi

Başlatılan bir karantina emrini tamamlandı olarak bildirmek için, emiri açın ve Eylem Bölmesinde **Tamamlandı olarak bildir**'i seçin. Madde karantinadan serbest bırakılır fakat henüz normal ambara geri taşınmaz. Normal ambara taşıma rapor sırasında başlatılabilen madde varış günlüğü ile tamamlanmış olarak işlenebilir.

### <a name="ended"></a>Bitti

Karantina emri sonlandırıldığında, madde karantina ambarından normal ambara geri taşınır. Madde hareketinin durumu karantina ambarında *satıldı* ve normal ambarda *satın alınan* olarak ayarlanır.

## <a name="quarantine-order-scrap"></a>Karantina siparişi hurda

Karantina emri işleminin bir parçası olarak stoğu hurdaya çıkartabilirsiniz. Hurdayı işlerken, stoğun durumu karantina ambarından çıkış hareketi tarafından *Satıldı* olarak ayarlanır.

## <a name="additional-resources"></a>Ek kaynaklar

- [Stok durdurma](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
