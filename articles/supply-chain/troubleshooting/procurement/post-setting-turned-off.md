---
title: Genel muhasebedeki gider hesabına naklet ayarı açık değil
description: Bu sorun bir satınalma siparişi faturalandığında, "Borç hesapları parametreleri" sayfasındaki "Fatura" sekmesinde "Genel muhasebedeki gider hesabına naklet" seçeneği etkinleştirildiğinde oluşur
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477868"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Genel muhasebedeki gider hesabına naklet ayarı açık değil

## <a name="symptoms"></a>Belirtiler

Bu sorun bir satınalma siparişi faturalandığında, **Borç hesapları parametreleri** sayfasındaki **Fatura** sekmesinde **Genel muhasebedeki gider hesabına naklet** seçeneği *Evet* olarak ayarlandığında oluşur.

## <a name="reproduce-the-issue"></a>Sorunu yeniden oluşturma

Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.

1. **Borç hesapları \> Kurulum \> Borç hesapları parametreleri**'ne gidin.
1. **Fatura** sekmesinde, **Genel muhasebedeki gider hesabına naklet** seçeneğini *Evet* olarak ayarlayın.
1. **Stok Yönetimi \> Kurulum \> Deftere nakil \> Deftere nakil** sayfasına gidin.
1. **Satınalma siparişi** sekmesinde, ürünle ilgili satın alma harcamaları içindeki tüm satırları sildiğinizden emin olun.
1. **Borç hesapları \> Satın alma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Bir satınalma siparişi oluşturmak. **Satıcı hesabı** alanında, *1001 Acme Office Supplies* ögesini seçin.
1. Aşağıdaki ayarlara sahip satınalma siparişi satırı oluşturun:

    - **Malzeme numarası:** *D0011 lazer projektör*
    - **Tesis:** *1*
    - **Ambar:** *11*
    - **Miktar:** *4*

1. Eylem Bölmesi'nde, **Satın al** sekmesindeki **Eylem** grubunda **Onayla**'yı seçin.
1. Eylem Bölmesi'nde, **Teslim al** sekmesindeki **Oluştur** grubunda **Ürün girişi**'ni seçin.
1. **Ürün girişi naklediliyor** iletişim kutusunda, **Ürün girişi** alanında rastgele bir numara girin ve **Tamam**'ı seçin.
1. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda **Fatura**'yı seçin.
1. **Numara** alanına, fatura numarası olarak rasgele bir numara girin.
1. Eşleştirme durumunu güncelleştirin ve deftere nakledin.
1. Bir satınalma siparişinden fatura oluştururken şimdi aşağıdaki hatayı alacağınızı unutmayın: "Ürün için satınalma harcamaları hareket türü için hesap numarası yok."

## <a name="resolution"></a>Çözüm

Bu, fatura ve fatura gruplarının parametre ayarlarına bağlıdır. Daha fazla bilgi için, aşağıdaki Web günlüğü postasına bakın: [Satınalma ücreti ve stok farkı için hesap](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
