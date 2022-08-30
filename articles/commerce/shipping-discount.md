---
title: Sevkiyat iskontosu
description: Bu makalede Microsoft Dynamics 365 Commerce'deki sevkiyat iskontosu yetenekleri ve bunları kullanmak için gereken ayarlar açıklanmaktadır.
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: f19566ce64becea4a53a8479cb5a08579567cda1
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346407"
---
# <a name="shipping-discount"></a>Sevkiyat iskontosu

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu makalede Microsoft Dynamics 365 Commerce'deki sevkiyat iskontosu yetenekleri ve bunları kullanmak için gereken ayarlar açıklanmaktadır.

Ücretsiz veya indirimli sevkiyat müşterilerin çevrimiçi satın alma kararlarını etkileyen bir etkendir. Birçok perakendeci, hareket başına gelirini artırmak için müşterilerin alışveriş sepeti tutarını artırmalarını sağlamak üzere ücretsiz sevkiyat avantajını kullanır.

Commerce, hareketteki uygun ürünler için toplam satış tutarı belirli bir ölçütü karşıladığında, perakendecilere belirli bir sevkiyat yöntemi için sevkiyat ücretleri üzerinde indirim yüzdesi yapılandırma olanağı tanıyan sevkiyat iskontosu özelliğini destekler. Sevkiyat iskontosu yeteneğini kullanan bir senaryo örneği olarak "$50 veya daha fazla harca ve ücretsiz ertesi gün gönderi kazan" verilebilir.

## <a name="prerequisites"></a>Ön Koşullar

Sevkiyat iskontosu yeteneği, Commerce'ın [çok kanallı gelişmiş otomatik giderler](/dynamics365/unified-operations/retail/omni-auto-charges) özellikleri tarafından desteklenir. Sevkiyat iskontosu özelliğinin çalışması için, Commerce Headquarters'daki **Commerce parametreleri** sayfasının **Müşteri siparişleri** sekmesinde **Gelişmiş otomatik giderleri kullan** yapılandırmasını etkinleştirmeniz gerekir. Perakendeciler işleme, yükleme ve elden çıkarma gibi çeşitli türde ücretler ayarlamak için gelişmiş otomatik giderler özelliğini kullanabilir.

Sevkiyat iskontosu yalnızca sevkiyat masraflarına uygulanır. Bu nedenle, bir perakendeci hangi giderlerin sevkiyat masrafları olduğunu belirtmelidir. Sevkiyat giderlerini belirtmek için Commerce Headquarters'da **Kanal kurulumu \>Giderler \> Giderler kodu**'na gidin ve istenen gider için **Sevkiyat gideri** seçeneğini **Evet** olarak ayarlayın.

![Bir gideri sevkiyat gideri olarak belirtin.](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>Yapılandırma

Sevkiyat iskontosu yeteneği katman tabanlıdır ve yalnızca **Yüzde oranı** hesaplama türünü destekler. Bir sevkiyat iskontosu ayarlamak için Commerce Headquarters'da **Fiyatlandırma ve iskontolar \> Sevkiyat eşik iskontosu**'na gidin. Daha sonra, iskontonun uygulandığı teslimat şeklini belirtebilir, bir veya daha fazla tutar eşiği tanımlayabilir ve her bir eşik için iskonto yüzdesini ayarlayabilirsiniz. Ayrıca kategori veya ürünlerin listesini uygun maddeler olarak yapılandırabilirsiniz. Bu şekilde, fiyatlandırma altyapısı hareket toplamının eşiğe uyup uymadığını değerlendirirken yalnızca hareketteki bu maddelere karşılık gelen satış tutarı sayılır.

> [!NOTE]
> Diğer iskonto türlerinin aksine, sevkiyat iskontosu iskonto satırları oluşturmaz. Bunun yerine, doğrudan sevkiyat giderini düzenler ve iskonto adını gider açıklamasına ekler.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
