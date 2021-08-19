---
title: Serbest bırakılan miktar negatif olacağından bir yük satırı güncelleştirilemiyor
description: Bu sorun bir yük satırını güncelleştirmenin veya silmenin negatif serbest bırakılan miktara neden olacağı durumlarda oluşur.
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728471"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>Serbest bırakılan miktar negatif olacağından bir yük satırı güncelleştirilemiyor

Hata kodu: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>Belirtiler

Bu sorun bir yük satırını güncelleştirmenin veya silmenin negatif serbest bırakılan miktara neden olacağı durumlarda oluşur. Bu durumda, yük satırını güncelleştirmeye veya silmeye çalıştığınızda sistem aşağıdaki hata iletisini gösterir:

> %1 öğesi, %2 lotu için serbest bırakılan miktar değeri negatif olamaz.

Bu nedenle, yük satırını güncelleştiremez veya silemezsiniz.

## <a name="cause"></a>Nedeni

Yük satırını güncelleştirdikten veya sildikten sonra sistem, ilgili satış satırının serbest bırakılan miktarını (*whsSalesLine.ReleaseQty*) güncelleştirir. Sistem serbest bırakılan miktarı değerlendirir ve satırın serbest bırakılan miktarının güncelleştirmeden sonra negatif olacağını belirlerse satırı güncelleştirmenize veya silmenize izin vermez. Yükleme satırı silme, sevkiyat silme, yükleme satırının miktarını değiştirme, çekilen miktarı azaltma ve eksik malzeme çekme gibi çeşitli eylemler üzerinden yükleme satırı miktarını veya ölçü birimini güncelleştirmeye çalıştığınızda bu doğrulama gerçekleşir.

Bu sorunun en yaygın kök nedeni, açık yük satırları için kullanılan birim dönüştürmedeki bir değişikliktir. Örneğin, satış siparişi serbest bırakıldığında birim dönüştürme *50 Ea = 1 PL* idi. Ancak ilgili yük sevkiyatı tamamlandığında birim dönüştürme *100 Ea = 1 PL* olarak değiştirildi.

## <a name="resolution"></a>Çözüm

Çözüm, birim dönüştürme değişikliklerini geri almak, yük satırını güncelleştirmek veya silmek ve ardından dönüştürmeyi yeniden uygulamaktır. Sorun çözülünceye kadar soruna neden olan öğeyi içeren diğer yüklerin işlenmesini de önlemeniz gerekir. Aksi takdirde, yeni dönüştürmeler zaten açık olan diğer yükler için kullanılabilir.

Bu sorunu gidermek için aşağıdaki görevleri tamamlayın:

1. Yük satırı için kullanılan birim dönüştürmeyi inceleyin.
2. Maddeyle ilgili geçerli birim dönüştürmeyi inceleyin ve yük satırının güncelleştirilmesini veya silinmesini sağlayacak ayarlamaları yapın.
3. Yük satırını güncelleştirin veya silin ve birim dönüştürme ayarlamalarını geri alın.

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>Yük satırı için kullanılan birim dönüştürmeyi inceleme

Yük satırlarını incelemek ve yük satırı için kullanılan birim dönüştürmeyi not etmek üzere aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Silinemeyen veya güncelleştirilemeyen yük satırını içeren yükü seçin.
1. Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.
1. Üst ızgarada, ilgili iş kodunu seçin.
1. Sayfanın alt kısmındaki **Genel** sekmesinde, **Stok iş miktarı** değeri ile **İş miktarı** değeri arasındaki dönüştürme oranını hesaplayın. Oranı not edin.
1. Aynı dönüştürmenin kullanıldığından emin olmak için ilgili tüm iş kodları için bu yordamı yineleyin.

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>Madde için geçerli birim dönüştürmeyi inceleme ve ayarlamalar yapma

Ürününüzün birim dönüştürmesini incelemek için aşağıdaki yordamı kullanın ve birim dönüştürmenin yük satırıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Serbest bırakılan ürün ayrıntıları** sayfasına gitmek için ilgili ürünü açın.
1. Eylem Bölmesi'nde, **Ürün** sekmesindeki **Ayar** gurubunda **Birim dönüştürmeleri**'ni seçin.
1. Birimler arasında dönüştürmeyi seçin ve önceki bölümde bulduğunuz dönüştürmeyi kullanarak ayarlamalar yapın.

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>Yük satırını güncelleştirme veya silme ve birim dönüştürme ayarlamalarını geri alma

Yük satırını gerektiği gibi işlemek ve birim dönüştürmelerini geri almak için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Silinemeyen veya güncelleştirilemeyen yük satırını içeren yükü açın.
1. **Yük satırları** hızlı sekmesinde, yük satırını seçin.
1. Gerektiğinde gerekli eylemlerle devam edin. (Örneğin, yük satırını silin veya miktarını değiştirin.)
1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Serbest bırakılan ürün ayrıntıları** sayfasına gitmek için ilgili ürünü açın.
1. Eylem Bölmesi'nde, **Ürün** sekmesindeki **Ayar** gurubunda **Birim dönüştürmeleri**'ni seçin.
1. Birimler arasında dönüştürmeyi seçin ve önceki bölümde yaptığınız ayarlamaları geri alın.
