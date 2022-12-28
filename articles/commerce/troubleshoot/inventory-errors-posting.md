---
title: Kullanılabilir stok veya güncelleştirme çakışması nedeniyle ekstre deftere nakil hataları
description: Bu makale, Microsoft Dynamics 365 Commerce'de ekstre deftere nakli sırasında stokla ilgili sorunlar için olası geçici çözümler sağlar.
author: Shajain
ms.date: 12/19/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: cebb890b42def6e9b002b01be63266b88bfc35a4
ms.sourcegitcommit: 4ad87483ba0bfea3e04fdb7e578d8abc34e607a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2022
ms.locfileid: "9887638"
---
# <a name="statement-posting-errors-due-to-unavailable-inventory-or-update-conflicts"></a>Kullanılabilir stok veya güncelleştirme çakışması nedeniyle ekstre deftere nakil hataları

[!include [banner](../../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'de ekstre deftere nakli sırasında stokla ilgili sorunlar için olası geçici çözümler sağlar.

## <a name="description"></a>Açıklama

Ticari hareketlerin deftere nakledilmesi sırasında, stok sorunları veya güncelleştirme çakışmaları ile ilgili hata iletileri alabilirsiniz.

### <a name="inventory-issues-error-message"></a>Stok çıkışları hata iletisi

Stok sorunlarıyla karşılaşırsanız, aldığınız hata iletisi bu örneğe benzeyecektir:

> Stokta yalnızca yy madde bulunduğundan, ambardan xx çekilemez

### <a name="update-conflict-error-messages"></a>Çakışma hata iletilerini güncelleştir

Stok değerleme yöntemi *standart maliyet* veya *hareketli ortalama* olduğunda güncelleştirme çakışması sorunu oluşuyor. Bu yöntemlerin her ikisi de kalıcı maliyetlendirme yöntemleri olduğundan, son maliyet deftere nakil sırasında belirlenir.

*Hareketli ortalama* yöntemini kullanıyorsanız, güncelleştirme çakışması hata iletisi aşağıdaki örneğe benzer:

> Orantılı gider hesaplamasından sonra xx.xx stok değeri beklenmez

*Standart maliyet* yöntemini kullanıyorsanız, güncelleştirme çakışması hata iletisi aşağıdaki örneğe benzer:

> Standart maliyet, güncelleştirmeden sonraki mali stok değeriyle eşleşmez. Değer = xx.xx, Miktar = yy.yy, Standart maliyet = zz.zz

## <a name="resolutions"></a>Çözümler

### <a name="workaround-for-the-inventory-error"></a>Stok hatası için geçici çözüm

Stok hatasını, maddenin envanterini el ile güncelleştirerek veya Commerce Headquarters'taki maddeyle ilişkilendirilmiş madde modeli grubu için fiziksel negatif stoğu etkinleştirerek azaltabilirsiniz.

Tutarlı bir deftere nakil deneyimi için Microsoft, öğe model grubu için fiziksel negatif stok etkinleştirmenizi önerir. Bazı senaryolarda, fiziksel negatif stok olmadığında negatif ekstrelerin deftere nakledilmesi mümkün olmayabilir.

Örneğin, bir madde için stok yok ise ancak kasiyer maddeyi iade ediyorsa ve ardından fiyat eşleşmesini taklit etmek için, daha sonra hareketi daha azaltılmış bir fiyatla yeniden ekler. Bu durumda, hem iade hareketi hem de satış hareketi, tek müşteri siparişinin aynı ekstresine çekilir. Ancak, iade satırının (stoğu artıran) satış satırı (stok miktarını azaltır) deftere nakledildiği konusunda deftere nakledilecek bir garanti olmadığı için stok hataları oluşabilir. Bu senaryoda fiziksel negatif stok açıksa hareket deftere nakli negatif olarak etkilenmez ve sistem stoğu doğru şekilde yansıtır.

#### <a name="enable-negative-physical-inventory-for-an-item-model-group"></a>Madde modeli grubu için negatif fiziksel stoğu etkinleştir

Commerce Headquarters'ta bir madde modeli grubu için negatif fiziksel stok etkinleştirmek üzere, aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Stok** öğelerini seçin.
1. Soldaki gezinti bölmesinde öğe model grubunu seçin.
1. **Stok ilkeleri** bölümünde, **Negatif stok** altında, **Fiziksel negatif stok** onay kutusunu seçin.

![Fiziksel negatif stok etkin.](./media/Physical_Negative_Inventory.png)

### <a name="workaround-for-the-update-conflict-error"></a>Güncelleştirme çakışması hatası için geçici çözüm

Güncelleştirme çakışma hatasıyla ilgili olası çözümler için bkz. [Stok değerlendirme yöntemi standart maliyet veya hareketli ortalama olduğunda bir güncelleştirme çakışması yaşanıyor](/troubleshoot/dynamics-365/supply-chain/costing/update-conflict-standard-cost-moving-average-inventory-valuation).

> [!NOTE]
> Güncelleştirme çakışması hatası için, deftere nakil için toplama adımı kullanılarak oluşturulan müşteri siparişlerini silmeniz gerekmez. Önerilen geçici çözümleri uyguladıktan sonra, ekstreyi deftere yeniden nakletmeyi denediğinizde ekstre deftere nakledilmelidir.
