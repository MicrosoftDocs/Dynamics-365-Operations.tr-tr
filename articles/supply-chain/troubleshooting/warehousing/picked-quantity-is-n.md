---
title: Sevk irsaliyesi oluşturma sırasında çekilen miktar yeterli değil
description: Sevk irsaliyesi oluşturduğunuzda giden yük, yük satırında oluşturulan iş miktarıyla eşleşmeyen bir çekilen miktar içerir.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 361b61690e9e16a690234ed9319478d864c743e7559746654e4868272de13524
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716480"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a>Sevk irsaliyesi oluşturma sırasında çekilen miktar yeterli değil

Hata kodu: SYS54073

## <a name="symptoms"></a>Belirtiler

Sevk irsaliyesi oluşturduğunuzda giden yük, yük satırında oluşturulan iş miktarıyla eşleşmeyen bir çekilen miktar içerir.

Sevk irsaliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> %1 çekilmiş olduğundan ve buna bağlı bakiyenin %3 olması gerektiğinden, %2 güncelleştirmesi için yeterli değil.

Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.

## <a name="cause"></a>Nedeni

Aşağıdaki koşullardan biri mevcut olduğu için sevk irsaliyesi oluşturulamıyor:

- İlgili iş henüz teslim alınmadı ve son sevkiyat konumuna taşınmadı.
- Teslim alınan iş miktarı, yükleme satırında oluşturulan iş miktarıyla eşleşmiyor.
- Yük satırı miktarı, işin oluşturduğu miktar ve çekilen miktar eşleşmiyor.

## <a name="resolution"></a>Çözüm

Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır. Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:

- Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.
- Yük satırı miktarını ayarlama
- Tüm çekme kayıtlarını tersine çevirin ve çekme işlemini yineleyin.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun

Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevk irsaliyesinin oluşturulamadığı yükü seçin.
1. **Yük satırları** hızlı sekmesinde, yük satırını seçin.
1. **Oluşturulan iş miktarı** alanının değerini not alın.
1. Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.
1. İşin son sevkiyat konumunda tamamlandığını ve teslim alınan iş miktarının yükleme satırındaki oluşturulan iş miktarıyla eşleştiğini doğrulayın.
1. Tüm ölçütlerin karşılandığından emin olmak için bu prosedürü tüm yükleme satırları için yineleyin.

### <a name="adjust-the-load-line-quantity"></a>Yük satırı miktarını ayarlama

Yük satırı miktarını ayarlamak için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevk irsaliyesinin oluşturulamadığı yükü seçin.
1. Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevkiyat onayını tersine çevir**'i seçin.
1.  **Yük satırları** sekmesinde, soruna neden olan maddenin yük satırını seçin.
1. Çekilen miktarı ayarlamak için **Çekilen miktarı düş**'ü seçin.
1. Yük satırındaki ayarlamaları yansıtacak şekilde **Yük satırını azalt** alanını ayarlayın.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Tüm çekme kayıtlarını tersine çevirme ve çekme işlemini yineleme

Sorun, birisi iş olmayan yük satırını kapatmak için çekme kaydı kullandığını için oluşabilir. Bu durumda, el ile çekme kaydı tersine çevrilmeli ve çekme işlemi Warehouse Management mobil uygulaması kullanılarak tamamlanmalıdır.

Çekme kaydını tersine çevirmek için aşağıdaki yordamı kullanın.

1. **Alacak hesapları \> Siparişler \> Tüm siparişler**'e gidin.
1. Yük için sevk irsaliyesini deftere nakledemeyeceğiniz satış siparişini seçin.
1.  **Satış siparişi satırları** sekmesinde, çekme kaydının yapıldığı satış siparişi satırını seçin.
1. Madde çekmeyi iptal etmek için **Satırı güncelleştir \> Çek**'i seçin.
