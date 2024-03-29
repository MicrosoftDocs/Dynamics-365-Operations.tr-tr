---
title: Kanallara genel bakış
description: Bu makale, Microsoft Dynamics 365 Commerce'teki kanallar hakkında genel bilgi vermektedir.
author: samjarawan
ms.date: 01/27/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.assetid: ''
ms.openlocfilehash: ad31f466563aeb38f28f9761828e6708895005b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280433"
---
# <a name="channels-overview"></a>Kanallara genel bakış


[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'teki kanallar hakkında genel bilgi vermektedir. Makalede, her bir kanalı ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır.

## <a name="types-of-channels"></a>Kanal Türleri

Dynamics 365 Commerce üç farklı kanal türünü destekler: perakende, çağrı merkezi ve çevrimiçi kanallar.

### <a name="retail-channels"></a>Perakende kanalları

Perakende kanalları geleneksel mağazaları temsil eder. Her mağazanın kendi satış noktası (POS) kasaları, gelir ve gider hesapları ve personeli olabilir. 

### <a name="call-center-channels"></a>Çağrı merkezi kanalları

Çağrı merkezi kanalları, çağrı merkezi sipariş ve müşteri yönetimini temsil eder.

### <a name="online-channels"></a>Çevrimiçi kanallar

Çevrimiçi kanallar, çevrimiçi e-ticaret mağazalarını temsil eder. Çevrimiçi kanal oluşturulduktan sonra, Microsoft Dynamics 365 Commerce Site Builder aracı veya başka bir üçüncü taraf e-ticaret çözümü kullanılarak bir site oluşturulması gerekir.

## <a name="channel-setup-basics"></a>Kanal kurulumu hakkında temel bilgiler

Kanal kurulumu Commerce aracında yapılır. Her kanalın kendi ödeme yöntemleri, fiyat grupları, ürün hiyerarşileri, sınıflamaları ve ürün kümeleri olabilir. Bir kanal oluşturduktan sonra, kanalı taşımasını ve satmasını istediğiniz ürünleri atarsınız. Her kanal türünün yapılandırmanız gerekebilecek benzersiz bir özellikler kümesi vardır. Örneğin, bir perakende kanalında çalışanların, kasaların ve müşterilerin atanması gerekir. Yeni bir kanal oluşturulunca, bir organizasyon hiyerarşisine atanması gerekir.

## <a name="channel-setup-prerequisites"></a>Kanal kurulum önkoşulları

Bir kanalı ayarlamadan önce, kanal türüne göre önkoşul olan bazı görevleri tamamlamanız gerekir. Daha fazla bilgi için bkz. [Kanal kurulum önkoşulları](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>Kanal ayarlama

Önkoşul görevleri tamamlandıktan sonra diğer kurulum yönergeleri için aşağıdaki bağlantıları kullanın.

- [Perakende kanalını ayarlama](channel-setup-retail.md)
- [Çağrı merkezi kanalını ayarlama](channel-setup-callcenter.md)
- [Çevrimiçi kanal ayarlama](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Ek kaynaklar

[Kanal kurulum önkoşulları](channels-prerequisites.md)

[Perakende kanalını ayarlama](channel-setup-retail.md)
    
[Çevrimiçi kanal ayarlama](channel-setup-online.md)

[Çağrı merkezi kanalını ayarlama](channel-setup-callcenter.md)

[Kuruluş hiyerarşilerini ayarlama](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
