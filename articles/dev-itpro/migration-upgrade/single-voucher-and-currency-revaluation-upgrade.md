---
title: "Tek fiş ve para birimi yeniden değerleme yükseltmesi"
description: "Bazı kuruluşlar, birden fazla müşteri veya satıcı olan tek bir fiş içeren günlükler girer ve ayrıca Alacak hesapları veya Borç hesapları yabancı para birimi yeniden değerleme işlemini çalıştırır. Bu konuda, bu kuruluşlar Microsoft Dynamics 365 for Operations'ı sürüm 1611'e yükseltirken izlemeleri gereken adımlar açıklanmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 13ad43cc77731727525aae1edc4d405c166acbc1
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>Tek fiş ve para birimi yeniden değerleme yükseltmesi

[!include[banner](../includes/banner.md)]


Bazı kuruluşlar, birden fazla müşteri veya satıcı olan tek bir fiş içeren günlükler girer ve ayrıca Alacak hesapları veya Borç hesapları yabancı para birimi yeniden değerleme işlemini çalıştırır. Bu konuda, bu kuruluşlar Microsoft Dynamics 365 for Operations'ı sürüm 1611'e yükseltirken izlemeleri gereken adımlar açıklanmaktadır.

Microsoft Dynamics 365 for Operations'ı sürüm 1611'e yükseltirken aşağıdaki adımları izleyin.

1.  Dynamics 365 for Operations'ı yükseltmeden önce Alacak hesapları ve Borç hesapları için yabancı para birimi yeniden değerleme işlemlerini çalıştırın. **Yöntem** alanı ayarını **Fatura tarihi** yapın. Son yabancı para birimi yeniden değerleme işlemini tersine çeviren bir yeniden değerleme hareketi oluşturulur. Bu nedenle, açık hareketler orijinal muhasebe para birimleriyle değerlendirilir.
2.  Dynamics 365 for Operations'ı sürüm 1611'e yükseltin.
3.  Alacak hesapları ve Borç hesapları yabancı para birimi yeniden değerleme işlemlerini yeniden çalıştırın. Bu kez, **Yöntem** alanı ayarını **Standart** yapın. Geçerli döviz kurları temel alınarak yeni bir yeniden değerleme hareketi oluşturulur. Bu hareket gerçekleşmemiş kazanç/kayıp ve doğru özet genel muhasebe hesabını kaydeder.





