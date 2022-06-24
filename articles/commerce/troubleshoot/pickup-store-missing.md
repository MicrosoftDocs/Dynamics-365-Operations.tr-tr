---
title: Perakende mağazası, ürünlerin teslim alınacağı mağazalar listesinde görünmüyor
description: Bu makale, ürünlerin teslim alınabileceği mağazalar listesinde bir perakende mağazası yer almadığında size yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 936b3df3194fbdacf8e853ed60431b077f4015cd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905268"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Perakende mağazası, ürünlerin teslim alınacağı mağazalar listesinde görünmüyor

[!include [banner](../../includes/banner.md)]

Bu makale, ürünlerin teslim alınabileceği mağazalar listesinde bir perakende mağazası yer almadığında size yardımcı olabilecek sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Bir perakende mağazası, ürünlerin teslim alınabileceği mağazalar listesinde görünmüyor.

## <a name="resolution"></a>Çözünürlük

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>Commerce Headquarters'da mağaza adresi için boylam ve enlemi yapılandırın

Commerce Headquarters'da mağaza adresi için boylam ve enlemi yapılandırmak için şu adımları izleyin.

1. **Retail ve Commerce \> Kanallar \> Mağazalar \> Tüm mağazalar**'a gidin.
1. E-ticaret sitesinde ürün teslim alma seçenekleri arasında görünmesini istediğiniz mağazayı bulun. **İşletme birimi numarası** değerini not alın.
1. **Kuruluş yönetimi \> Kuruluşlar \> İşletme birimleri** seçeneğine gidin.
1. Daha önce not ettiğiniz işletme birimi numarasını arayın ve arama sonuçlarında işletme birimini seçin.
1. **Adresler** hızlı sekmesinde, **diğer seçenekler**'i seçin ve sonra **Gelişmiş**'i seçin.
1. **Genel** hızlı sekmesinde, **boylam** ve **enlem** alanlarının doğru ayarlandığından emin olun. Bu adımın bir parçası olarak, değerlerin pozitif veya negatif sayılar olarak doğru belirtildiğinden emin olun.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Commerce Headquarters'da karşılama gruplarını yapılandırın

Commerce Headquarters'da karşılama gruplarını yapılandırmak için şu adımları izleyin.

1. **Retail ve Commerce \> Kanallar \> Çevrimiçi mağazalar**'a gidin.
1. Yapılandırılacak çevrimiçi mağazayı seçin.
1. Eylem bölmesinde, **Kurulum** sekmesini ve ardından **Karşılama grubu ataması**'nı seçin.
1. **Karşılama grubu ataması** sayfasında, çevrimiçi mağaza için karşılama grubunu seçin.
1. **Kurulum altında** perakende mağazanın karşılama grubu için doğru yapılandırıldığından emin olun.

## <a name="additional-resources"></a>Ek kaynaklar 

[Faaliyet birimi oluşturma](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[Çevrimiçi kanalı ayarlama](../channel-setup-online.md)