---
title: Perakende hareketlerinin mali boyutlarını düzenleme
description: Bu makalede, Microsoft Dynamics 365 Commerce'te perakende hareketlerinin mali boyutlarının nasıl düzenleneceği açıklanmaktadır.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: b382907cd79a13319601dd694261319875565947
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268409"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Perakende hareketlerinin mali boyutlarını düzenleme

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te perakende hareketlerinin mali boyutlarının nasıl düzenleneceği açıklanmaktadır.

## <a name="edit-financial-dimensions"></a>Mali boyutları düzenleme

Commerce genel merkezindeki perakende hareketlerinin mali boyutlarını düzenlemek için aşağıdaki adımları izleyin.

1. **Uygulamaları tümleştirmek için mali boyut konfigürasyonu** sayfasını açın.
1. Etkin **Varsayılan boyut tümleştirmesi** kaydını seçin.
1. **Mali boyutlar** hızlı sekmesinde, Excel çalışma sayfasındaki düzenlemek istediğiniz tüm boyutların **Seçili** listesinde bulunduğundan emin olun. Daha fazla bilgi için bkz. [Veri varlıkları](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).
1. Excel dosyasını **Ekstreler** sayfasından, **Perakende hareketleri** sayfasından veya **Mağaza mali öğeleri** çalışma alanındaki **Hareket doğrulama hataları** kutucuğundan indirin ve açın.
1. Hareket mali boyutunu değiştirmek için **Tasarım**'ı seçin ve ardından **Hareket (denetlenebilir)** satırının yanındaki kalem simgesini seçin.
1. **FinancialDimensionDisplayValue** alanını bulup seçin, Excel çalışma sayfasının başlık bölümünde bir hücre seçin ve ardından **Etiket ekle**'yi seçin.
1. Önceki adımda seçtiğiniz hücrenin altında bir hücre seçin, **Değer Ekle**'yi ve ardından **Yenile**'yi seçin. Mali boyutlar Excel çalışma sayfasına eklenir ve daha sonra düzenlenebilir ve yayımlanabilir.
1. Hareket satırlarındaki boyutları değiştirmek için **Satış hareketleri (denetlenebilir)** satırını seçin, kalem simgesini seçin ve ardından 6. ve 7. adımları tekrarlayın.
1. Ödeme satırlarındaki boyutları değiştirmek için **Ödeme hareketleri (denetlenebilir)** satırını seçin, kalem simgesini seçin ve ardından 6. ve 7. adımları tekrarlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Peşin ve nakit yönetimi hareketlerini düzenleme ve denetleme](edit-cash-trans.md)

[Çevrimiçi siparişi ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme ve denetleme](edit-order-trans.md)

[Perakende hareketlerini düzenlemek için bir Excel çalışma kitabı oluşturma](create-excel-edit.md)

[Perakende hareketlerini düzenlemek için Excel çalışma kitabına alanlar ekleme](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
