---
title: Satış noktası (POS) için nakit kupürlerini yapılandırma
description: Banknotlar ve bozuk paralar için arka ofiste tanımlana nakit para birimleri, kasiyerler, satış sorumluları ve yöneticiler tarafından mağazada POS içerisinden kullanılabilir.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5dbef67728e86259ee48b51c48921f6e44a61015
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793069"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a>Satış noktası (POS) için nakit kupürlerini yapılandırma

[!include [banner](includes/banner.md)]

Banknotlar ve bozuk paralar için arka ofiste tanımlana nakit para birimleri, kasiyerler, satış sorumluları ve yöneticiler tarafından mağazada POS içerisinden kullanılabilir. Bu para birimleri, gün sonu kasa sayımlarında sayıma yardımcı olmak veya bir satışın sayımını hızlıca gerçekleştirmek için kullanılabilir.

## <a name="define-denominations"></a>Para birimlerini tanımla

Para birimleri mağaza başına **Ayarlama** \> **Nakit bildirimi** seçeneğine mağaza varlığı üzerinde ayarlanır.

![Nakit bildirimi seçeneği](./media/image1-denomination.png)

Bir para birimini tanımlamak için:

1. **Yeni**'ye tıklayın.
1. Türü belirtin (bozuk para veya banknot).
1. Tutarı (değeri) belirtin.

![Nakit bildirimi kupürleri sayfası](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>İşlev profilini yapılandırın

POS içinde nakit ile öderken, kullanıcı banknot para birimlerini, müşteri tarafından ödenen tutarı hızlıca girmek için kullanabilir. İşlev profilinde, para birimini POS içerisinde göstermek için iki seçeneği yapılandırabilirsiniz.

- **Vadesi gelen tutara eşit veya büyük** – Varsayılan olarak, POS yalnızca vadesi gelen tutardan büyük olan banknot para birimlerini gösterir, bu da tek dokunuşla kasa sayımına olanak sağlar. Örneğin, vadesi gelen tutar 7,50 $ ise, POS aşağıdaki para birimlerini gösterir: 10 $, 20 $, 50 $ ve 100 $. Bu tutarlardan herhangi birine dokunmak, satış için kasa sayımını otomatik olarak bu tutardan yapar. 1 $ ve 5 $ banknotları, bunların vadesi gelen tutardan daha az olmalarından dolayı görüntülenmez.
- **Tüm para birimleri** – Tüm banknot para birimlerini, vadesi gelen tutardan bağımsız olarak POS içerisinde her zaman göstermek için bu seçeneği seçin. Bu, kullanıcının vadesi gelen tutara ulaşmak için banknot kombinasyonlarını kullanabileceği anlamına gelir. Örneğin, vadesi gelen tutar 25,00 $ ise, kullanıcı satışı tamamlamak için 20 $ ve 5 $ seçebilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]