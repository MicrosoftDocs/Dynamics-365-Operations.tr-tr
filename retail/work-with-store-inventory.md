---
title: "Stok yönetimini yönet"
description: "Bu makalede, stok yönetmek için kullanabileceğiniz belge türlerini açıklar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fbe9945799f1e65ed6ad624a3df270fa4eb72b88
ms.lasthandoff: 03/31/2017


---

# <a name="manage-store-inventory"></a>Stok yönetimini yönet

Bu makalede, stok yönetmek için kullanabileceğiniz belge türlerini açıklar.

Kuruluşunuzun stoğunu yönetmek için aşağıdaki belge türlerini kullanabilirsiniz.

## <a name="purchase-orders"></a>Satınalma siparişleri
Satınalma siparişleri merkez ofiste oluşturulur. Perakende ambar satınalma siparişi başlığında eklenirse, Modern POS (MPOS) veya Bulut POS işlemleri - perakende Microsoft Dynamics 365 kullanarak sipariş mağazada alınabilirler. Mağazada alınan miktarların girildikten sonra ek değiştirilmek üzere yerel olarak kaydedilebilir. Alternatif olarak, miktarlar ayrılıp merkez ofise gönderilebilir. Merkez ofiste mağazada alınan miktarların işlemleri için Dynamics 365 içinde görüntülenir **Şimdi Al** alanında bulunan satınalma siparişi.

## <a name="transfer-orders"></a>Transfer emirleri
Transfer emri belirli bir mağazanın maddelerin sevk edilebileceği bir konum olduğunu belirtebilir. Bu durumda, transfer emri malzeme çekme isteği MPOS veya Bulut POS olarak mağazada görünür. Talep edilen miktarlar çekilir sonra bunlar ilenir ve merkez ofise gönderilir. Merkez ofiste mağazada Çekilen miktar işlemleri için Dynamics 365 içinde görüntülenir **Şimdi sevk et** transfer emrindeki alan. Transfer emri belirli bir mağazanın maddelerin sevk edilebileceği bir konum olduğunu belirtebilir. Bu durumda, transfer emrini teslim alma isteği MPOS veya Bulut POS olarak mağazada görünür. Mağazada alınan miktarların girildikten sonra ek değiştirilmek üzere yerel olarak kaydedilebilir. Alternatif olarak, miktarlar ayrılıp merkez ofise gönderilebilir. Merkez ofiste mağazada alınan miktarların işlemleri için Dynamics 365 içinde görüntülenir **Şimdi Al** transfer emrindeki alan.

## <a name="stock-counts"></a>Stok sayımları
Stok sayımları zamanlanmış veya zamanlanmamış olabilir. Planlı stok sayımları sayılması gereken maddeleri belirten merkez ofiste başlatılır. Merkez ofis mağazada, fiili eldeki stok miktarlarını MPOS veya Bulut POS girildiği alınan bir sayım belgesi oluşturur. Planlanmamış stok sayımları bir mağazada başlatılır ve fiili eldeki stok miktarlarını MPOS veya Bulut POS güncelleştirilir. Zamanlanmış stok sayımları farklı olarak, önceden tanımlanmış bir liste öğeleri planlanmamış stok sayımları gerekmez. Her iki türün birinden bir stok sayımı tamamlandığında, özen ve merkez ofise gönderilir. Merkez ofiste sayım doğrulanır ve nakledilir.




