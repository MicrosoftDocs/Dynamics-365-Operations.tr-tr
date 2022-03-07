---
title: Yük satırlarındaki miktar sıfır olduğundan sevkiyat onaylanamıyor
description: Yük satırlarındaki miktar sıfır olduğundan sevkiyat onaylanamıyor.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 5dc5f8962ba37d21d7ef505fea940dc8767a9d9295588cb0e12e9eebe379a35c
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012223"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>Yük satırlarındaki miktar sıfır olduğundan sevkiyat onaylanamıyor

Hata kodu: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>Belirtiler

Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> %1 yükündeki tüm satırların miktarı sıfır.  
> Yük %1 sevkiyatı onaylanamadı.

Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.

## <a name="cause"></a>Nedeni

Sistem, oluşturulan iş kimliklerine, yük satırı miktarına ve eksik teslimat yüzdesine göre yük satırının sevkiyatının onaylanıp onaylanamayacağını değerlendirir. Sistem hiçbir iş kimliği olmadığını tespit ederse ve eksik teslimat yüzdesi yüzde 100 olarak ayarlanmışsa sevkiyatı onaylayamazsınız.

Örneğin, iş iptal edilirse ve yükleme satırındaki eksik teslimat yüzdesi yüzde 100 ise bu sorun oluşabilir.

## <a name="resolution"></a>Çözüm

Yükleme veya sevkiyat işlemi şu anda sevkiyat onayının başarısız olduğu bir durumdadır. Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:

- Yük satırlarınızı tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olmak üzere gözden geçirin.
- Eksik teslimat yüzdesinin ve miktarların, teslim alınan işle uyumlu olduğundan emin olmak için yükleme satırlarını gözden geçirin.

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Yük satırlarınızı tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olmak üzere gözden geçirin

Yük satırlarınızı, tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olmak üzere gözden geçirmek için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın onaylanamadığı ilgili yükü açın.
1. **Yük satırları** hızlı sekmesinde, yük satırını seçin.
1. **Oluşturulan iş miktarı** alanının değerini not alın.
1. Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.
1. İşin son sevkiyat konumunda tamamlandığını ve teslim alınan iş miktarının yükleme satırındaki oluşturulan iş miktarıyla eşleştiğini doğrulayın.
1. Uyumsuzluk bulursanız ilgili işi iptal edin, konum yönergesini yeniden yapılandırın ve yükü yeniden serbest bırakın. Yönergeler için bkz. [Maddeler alınmadığı için sevkiyat onaylanamıyor](picked-quantity-is-not-on-final.md).
1. Tüm ölçütlerin karşılandığından emin olmak için bu prosedürü tüm yükleme satırları için yineleyin.

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>Eksik teslimat yüzdesinin ve miktarların, teslim alınan işle uyumlu olduğundan emin olmak için yükleme satırlarını gözden geçirin

Eksik teslimat yüzdesinin ve miktarların, teslim alınan işle uyumlu olduğundan emin olmak için yükleme satırlarını gözden geçirmek üzere aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın onaylanamadığı ilgili yükü açın.
1. **Yük satırları** hızlı sekmesinde, eksik teslimat yüzdesini aşan maddenin yük satırını seçin.
1. **Eksik teslimat** alanının veya **Miktar** alanının değerini gerektiği gibi ayarlayın.

> [!TIP]
> Sorun hala düzelmezse mevcut miktar, yükleme veya sevkiyat ile uyumlu hale gelene kadar ilgili satış siparişleri veya transfer emirleri için daha fazla teslim alma işi tamamlamanız gerekebilir.
