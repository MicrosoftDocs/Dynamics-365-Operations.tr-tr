---
title: Müşteri kayıtları Commerce headquarters'da görünmüyor
description: Bu konu, müşteri kayıtlarının Commerce Headquarters'da hemen görünmemesine yardımcı olabilecek sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: f551f94cec71ba7d740756c383b55741e9f8d42e20e63846ea6242383dc3ba32
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733905"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Müşteri kayıtları Commerce headquarters'da görünmüyor

[!include [banner](../../includes/banner.md)]

Bu konu, müşteri kayıtlarının Commerce Headquarters'da hemen görünmemesine yardımcı olabilecek sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

E-ticaret mağazasında kaydolma akışını kullanarak yeni bir müşteri kaydı oluşturduğunuzda, ilgili müşteri kaydı hemen Commerce Headquarters'da görünmüyor.

## <a name="resolution"></a>Çözünürlük

### <a name="disable-customer-creation-in-async-mode"></a>Zaman uyumsuz modda müşteri oluşturmayı devre dışı bırakın

> [!IMPORTANT]
> Zaman uyumsuz müşteri oluşturmayı devre dışı bırakırsanız, her kaydın oluşturulması Commerce Headquarters'a gönderilen gerçek zamanlı bir talep üreteceği için sistem performansı etkilenebilir. Ayrıca, Commerce Headquarters kapalı ise (örneğin, bakım akışları sırasında), tüm yeni müşteri oluşturma akışlarında hata ortaya çıkaracaktır.

Commerce Headquarters'da zaman uyumsuz modda müşteri oluşturmayı devre dışı bırakmak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> Çevrimiçi mağaza kurulumu \> İşlevsellik profilleri** öğesine gidin.
1. Çevrimiçi kanallarınız için henüz bir işlevsellik profili kullanmıyorsanız, bir tane oluşturun.
1. **Zaman uyumsuz modda müşteri oluştur** seçeneğinin **Hayır** olarak ayarlandığından emin olun.
1. **Retail ve Commerce \> Kanallar \> Çevrimiçi mağazalar**'a gidin.
1. Zaman uyumsuz müşteri oluşturmayı devre dışı bırakmak istediğiniz çevrimiçi mağazayı seçin.
1. **Genel** sekmesinde, **işlevsellik profili** alanının çevrimiçi kanalınız için kullanmakta olduğunuz işlevsellik profiline ayarlandığından emin olun.

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce'te B2C kiracısı ayarlama](../set-up-b2c-tenant.md)
