---
title: Satınalma siparişi satırı veri uyuşmazlıkları
description: Satınalma siparişi satırlarınızda veri uyuşmazlıkları veya veri bozulması görürsünüz.
author: SmithaNataraj
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: PurchLineManualCorrection, PurchTable, PurchLine, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ee2cb9a07c8a00a92c71e3e99d8ec20aa27fb20e
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100811"
---
# <a name="purchase-order-line-data-discrepancies"></a>Satınalma siparişi satırı veri uyuşmazlıkları

## <a name="symptoms"></a>Belirtiler

Bir satınalma siparişinin satırlarını denetlerken aşağıdaki sorunlardan bir veya daha fazlasını görürsünüz:

- Satınalma siparişi satırı kalanlarında (teslimat veya fatura) veri tutarsızlığı veya veri bozulması var.
- Satınalma siparişi satırında veya başlık durumunda bozulma var.
- Örneğin aşağıdaki hata iletilerinden birini veya daha fazlasını aldığınız için bir satınalma siparişini faturalayamıyorsunuz:

    - "Durduruldu (hata): Hareket zaten deftere nakledildi."
    - "Alındı durumunda olan stok hareketleri yetersiz olduğundan miktar faturalanamaz."
    - "Madde %0 Miktar %1 için "Satın alındı" durumundaki stok hareketleri yetersiz."

- Örneğin, aşağıdaki sorunlardan biri nedeniyle bir satınalma siparişini sonlandırlamıyor veya kapatamıyorsunuz.

    - **Sonlandır** düğmesi yok.
    - Onaylandı ve alındı durumundaki bir satınalma siparişi için satınalma siparişi satırının sipariş edilen miktarını iptal edemiyorsunuz.

## <a name="cause"></a>Nedeni

Bu sorunlar genellikle veri bozulmasından veya bir veya daha fazla satınalma siparişi satırı için kalan miktarlarda tutarsızlık olması nedeniyle oluşur.

## <a name="resolution"></a>Çözüm

Bu sorunları genellikle, ilgili satınalma siparişi satırları için satınalma durumunu, teslimat kalanlarını ve/veya fatura kalanlarını aşağıdaki yordamda açıklandığı gibi güncelleştirerek düzeltebilirsiniz.

1. **Tedarik ve kaynak atama \> Periyodik görevler \> Temizleme \> Satınalma siparişi satırlarını el ile düzelt**'e gidin.
1. **Satınalma siparişi** alanında, sorun yaratan satınalma siparişini bulun ve seçin.
1. **Satınalma siparişi satırları** bölümünde, bir tutarsızlık bulunan satırı seçin.
1. **Stok hareketleri** bölümünde gösterilen verileri denetleyin. Bir satınalma siparişi satırı ile stok hareketleri arasında tutarsızlık olduğunu fark ederseniz, tutarsızlıkları nerede gördüğünüze bağlı olarak, Eylem Bölmesinde aşağıdaki komutlardan birini seçin:

    - **Yeniden hesapla \> Teslimat kalanını yeniden hesapla** – Satınalma sipariş satırı ve başlık durumlarını otomatik olarak güncelleştir. Bu işlev yalnızca stoğu tutulan satınalma siparişi satırları için (maddenin stoğu tutulan madde olduğu satırlar) çalışır. Stoğu tutulmayan maddeler ve fiili ağırlık maddeleri şu anda desteklenmemektedir.
    - **Yeniden hesapla \> Fatura kalanını yeniden hesapla** – Satınalma sipariş satırı ve başlık durumlarını otomatik olarak güncelleştir. Bu işlev yalnızca stoğu tutulan satınalma siparişi satırları için (maddenin stoğu tutulan madde olduğu satırlar) çalışır. Stoğu tutulmayan maddeler ve fiili ağırlık maddeleri şu anda desteklenmemektedir.
    - **Yeniden hesapla \> Durumu yeniden hesapla** - Seçili satırın durumunu yeniden hesapla. Bu hesaplama varolan mantığa dayanır. Bu nedenle, satınalma siparişi başlığı durumu gerektiğinde yeni satınalma sipariş satırı durumuna göre güncelleştirilir.

1. Kalan miktarlarla hala tutarsızlıklar görüyorsanız, bunları doğrudan gerektiği şekilde düzenlemek için aşağıdaki alanları kullanabilirsiniz:

    - Teslimat bakiyesi
    - Stok teslimat bakiyesi
    - Fatura kalan tutarı
    - Stok faturası bakiyesi
