---
title: Malzeme çekme bilgileri modülü
description: Bu makale teslim bilgileri modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün ödeme sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 57633b7a23e581278ec0bc09ea146f5453570c4e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288419"
---
# <a name="pickup-information-module"></a>Malzeme çekme bilgileri modülü

[!include [banner](includes/banner.md)]

Bu makale teslim bilgileri modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün ödeme sayfalarına nasıl ekleneceğini açıklamaktadır.

Malzeme çekme bilgileri modülü, sipariş alma bilgilerini göstermek amacıyla bir kullanıma alma modülünde kullanılabilir. Müşteriler, mevcut malzeme çekme tarihlerini ve zaman yuvalarını görüntüleyebilir ve sonra siparişini çekmek için uygun bir zaman seçebilirsiniz. Örneğin, bir müşteri San Francisco Store 'dan 21 Mart 'ta 15.00'da siparişi teslim alabilir.

İlgili Mağazalar için malzeme çekme zaman yuvaları Commerce Headquarters 'da konfigüre edilmelidir. Daha fazla bilgi için bkz. [Müşteri malzeme çekme için zaman aralıkları oluşturma ve güncelleştirme](dev-itpro/pickup-timeslots.md).

Malzeme çekme bilgileri modülü kullanıma alma sayfasında oluşturulursa, ancak malzeme çekme için seçilen mağaza için tanımlanmış zaman yuvaları yoksa modül bilgileri gösterir, ancak Kullanıcı herhangi bir zaman dilimini seçemeyecektir. Zaman yuvaları isteğe bağlıdır ve sipariş vermek zorunda değildir.

Çoklu mağazalar arasında malzeme çekme için birden fazla madde seçilmişse, malzeme çekme bilgileri modülü kullanıcının her mağaza için zaman dilimini seçmesini sağlar; bunlar için zaman dilimi kullanılabilir.

> [!NOTE]
> Zaman yuvaları desteği ve kullanıma alma bilgileri modülü Dynamics 365 Commerce sürüm 10.0.15 ve sonrasında mevcuttur.

Aşağıdaki resimde, kullanıma alma sayfasındaki malzeme çekme bilgileri modülü aracılığıyla zaman dilimi seçimi örneği gösterilmektedir.

![Ödeme sayfasındaki teslimat bilgileri modülü örneği.](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Modül özellikleri

- **Başlık** - Ödeme modülü için başlık.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Sipariş yerleştirildikten sonra zaman dilimi bilgilerini göster

Bir sipariş yerleştirildikten sonra, seçilen zaman dilimi hakkındaki bilgiler [sipariş onayı modülünde](order-confirmation-module.md) ve [sipariş ayrıntıları modülünde görüntülenebilir](account-management.md#order-details-page). Bu modüllerin her ikisi de bir **zaman lotu bilgilerini göster** özelliğine sahiptir. Sipariş işlemi sırasında seçilen zaman dilimini gösterebilmek için, bu özelliğin **doğru** olarak ayarlanması gerekir.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Bir sayfadaki ödeme teslimat bilgileri modülü örneği

Bir ödeme sayfasına teslim bilgileri modülü ekleme ve gerekli özellikleri ayarlama yönergeleri için bkz. [Ödeme modülü](add-checkout-module.md).

Aşağıdaki çizimde, malzeme çekme kalemindeki zaman yuvalarını içeren bir e-ticaret kullanıma alma sayfası örneği gösterilmiştir.

![Malzeme çekme kalemindeki zaman yuvalarını içeren bir e-ticaret kullanıma alma sayfası örneği.](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Ek kaynaklar

[Müşterinin teslim alması için zaman aralıkları oluşturma ve güncelleştirme](dev-itpro/pickup-timeslots.md)

[Ödeme yapma modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Sipariş ayrıntıları modülü](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
