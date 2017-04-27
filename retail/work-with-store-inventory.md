---
title: "Stok yönetimini yönet"
description: "Bu makalede, stoku yönetmek için kullanabileceğiniz belge türleri açıklanmaktadır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
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

[!include[banner](includes/banner.md)]


Bu makalede, stoku yönetmek için kullanabileceğiniz belge türleri açıklanmaktadır.

Kuruluşunuzun stoğunu yönetmek için aşağıdaki belge türlerini kullanabilirsiniz.

## <a name="purchase-orders"></a>Satınalma siparişleri
Satınalma siparişleri merkez ofiste oluşturulur. Satınalma siparişi başlığına bir perakende ambarı dahil edilirse, sipariş, Microsoft Dynamics 365 for Operations - Perakende'de Modern POS (MPOS) veya Cloud POS kullanılarak mağazadan teslim alınabilir. Mağazada teslim alınan miktarlar girildikten sonra ek değişiklikler için yerel olarak kaydedilebilir. Alternatif olarak, miktarlar ayrılıp merkez ofise gönderilebilir. Merkez ofiste, mağazada alınan miktarlar Dynamics 365 for Operations'ta, satınalma siparişindeki **Şimdi al** alanında görüntülenir.

## <a name="transfer-orders"></a>Transfer emirleri
Transfer emri belirli bir mağazanın maddelerin sevk edilebileceği bir konum olduğunu belirtebilir. Bu durumda, transfer emri MPOS'ta veya Cloud POS'ta bir malzeme çekme isteği olarak mağazada görünür. Talep edilen miktarlar çekildikten sonra taahhüt edilip merkez ofise gönderilir. Merkez ofiste, mağazada alınan miktarlar Dynamics 365 for Operations'ta, transfer emrindeki **Şimdi sevk et** alanında görüntülenir. Transfer emri belirli bir mağazanın maddelerin sevk edilebileceği bir konum olduğunu belirtebilir. Bu durumda, transfer emri MPOS'ta veya Cloud POS'ta teslim alma isteği olarak mağazada görünür. Mağazada teslim alınan miktarlar girildikten sonra ek değişiklikler için yerel olarak kaydedilebilir. Alternatif olarak, miktarlar ayrılıp merkez ofise gönderilebilir. Merkez ofiste, mağazada alınan miktarlar Dynamics 365 for Operations'ta, transfer emrindeki **Şimdi al** alanında görüntülenir.

## <a name="stock-counts"></a>Stok sayımları
Stok sayımları zamanlanmış veya zamanlanmamış olabilir. Planlı stok sayımları sayılması gereken maddeleri belirten merkez ofiste başlatılır. Merkez ofis mağazada alınabilecek bir sayım belgesi oluşturur ve fiili eldeki stok miktarları burada MPOS'a veya Cloud POS'a girilir. Mağazada planlanmamış stok sayımları başlatılır ve fiili eldeki stok miktarları MPOS'ta veya Cloud POS'te güncelleştirilir. Planlı stok sayımlarından farklı olarak, planlanmamış stok sayımlarında önceden tanımlanmış bir madde listesi yoktur. Her iki türün birinden bir stok sayımı tamamlandığında, özen ve merkez ofise gönderilir. Merkez ofiste sayım doğrulanır ve nakledilir.






