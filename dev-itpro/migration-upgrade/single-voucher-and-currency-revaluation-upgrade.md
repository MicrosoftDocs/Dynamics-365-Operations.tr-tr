---
title: "Tek fiş ve para birimi yeniden değerleme işlemleri 1611 sürümü için Microsoft Dynamics 365 için yükseltme"
description: "Bazı kuruluşlar, birden fazla müşteri veya satıcı olan tek bir fiş içeren günlükleri girin ve ayrıca Alacak hesapları veya hesapları ödenecek yabancı para birimi yeniden değerleme işlemi çalıştırın. Bu konu, 1611 işlemleri sürümü için Microsoft Dynamics 365 arası yükselttiğinizde bu kuruluşlar adımları açıklar."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Tek fiş ve para birimi yeniden değerleme işlemleri 1611 sürümü için Microsoft Dynamics 365 için yükseltme

Bazı kuruluşlar, birden fazla müşteri veya satıcı olan tek bir fiş içeren günlükleri girin ve ayrıca Alacak hesapları veya hesapları ödenecek yabancı para birimi yeniden değerleme işlemi çalıştırın. Bu konu, 1611 işlemleri sürümü için Microsoft Dynamics 365 arası yükselttiğinizde bu kuruluşlar adımları açıklar.

Microsoft Dynamics 365 arası işlemler için sürüm 1611'e yükselttiğinizde, aşağıdaki adımları izleyin.

1.  Dynamics 365 işlemleri için yükseltmeden önce yabancı para birimi yeniden değerleme işlemleri için Alacak hesapları ve Borç hesapları çalışır. Set **yöntemi** alanı **fatura tarihi**. Son yabancı para birimi yeniden değerleme tersine çevirir yeniden değerleme hareketi oluşturulur. Bu nedenle, açık hareketler kendi orijinal hesap para biriminden değerli.
2.  Dynamics 365 arası 1611 işlemleri sürüm için yükseltme.
3.  Alacak hesapları ve hesapları ödenecek yabancı para birimi yeniden değerleme işlemleri yeniden çalıştırın. Bu kez, set **yöntemi** alanı **standart**. Geçerli döviz kurları üzerinde temel alan yeni bir yeniden değerleme hareketi oluşturulur. Bu işlem gerçekleşmemiş kazanç/kayıp ve doğru Özet genel muhasebe hesabına kaydeder.



