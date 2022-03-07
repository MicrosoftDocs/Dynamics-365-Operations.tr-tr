---
title: Güncelleştirmeye çalıştığınız miktar alınan/teslim edilen miktarı aşıyor.
description: Sevk irsaliyesi oluşturduğunuzda giden yük, satış siparişi için çekilen ve rezerve edilen iş miktarını aşan bir miktar içeriyor.
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
ms.openlocfilehash: 25507a482b2db7c01f56679bf3e8454249de3a6b9965f9c359a2ebe2cc8445ce
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711699"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>Güncelleştirmeye çalıştığınız miktar alınan/teslim edilen miktarı aşıyor

Hata kodu: SYS7676

## <a name="symptoms"></a>Belirtiler

Sevk irsaliyesi oluşturduğunuzda giden yük, satış siparişi için çekilen ve rezerve edilen iş miktarını aşan bir miktar içeriyor.

Sevk irsaliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> Güncelleştirmeye çalıştığınız miktar, alınan/teslim edilen miktarı aşıyor.

Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.

## <a name="cause"></a>Nedeni

Teslim alınan iş miktarı, yükleme satırında oluşturulan iş miktarıyla eşleşmiyor. Örneğin, yükleme satırı miktarı, oluşturulan iş miktarı veya çekilen miktar doğru değilse bu sorun oluşabilir.

## <a name="resolution"></a>Çözüm

Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır. Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:

- Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.
- Yük satırı miktarını ayarlama
- Tüm çekme kayıtlarını tersine çevirin ve çekme işlemini yineleyin.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun

Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın oluşturulamadığı ilgili yükü seçin.
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

Birisi bir yük satırını iş olmadan kapatmak için çekme kaydını kullandıysa, yük satırı miktarı ile çekilen miktar arasında bir tutarsızlık oluşabilir. Bu durumda, el ile çekme kaydı tersine çevrilmeli ve çekme işlemi Warehouse Management mobil uygulaması kullanılarak tamamlanmalıdır.

Çekme kaydını tersine çevirmek için aşağıdaki yordamı kullanın.

1. **Alacak hesapları \> Siparişler \> Tüm siparişler**'e gidin.
1. Yük için sevk irsaliyesini deftere nakledemeyeceğiniz satış siparişini seçin.
1.  **Satış siparişi satırları** sekmesinde, çekme kaydının yapıldığı satış siparişi satırını seçin.
1. Madde çekmeyi iptal etmek için **Satırı güncelleştir \> Çek**'i seçin.
