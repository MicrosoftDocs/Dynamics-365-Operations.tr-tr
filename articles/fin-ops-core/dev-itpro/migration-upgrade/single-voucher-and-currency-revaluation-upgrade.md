---
title: Tek fiş günlüklerini ve para birimi yeniden değerlemelerini yükseltme
description: Bu konuda, tek fiş günlüklerinin ve para birimi yeniden değerlemelerinin nasıl yükseltileceği açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb4eca4933716105789d3bbc21dd374395211d1d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559533"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Tek fiş günlüklerini ve para birimi yeniden değerlemelerini yükseltme

[!include [banner](../includes/banner.md)]

Bazı kuruluşlar, birden fazla müşteri veya satıcı olan tek bir fiş içeren günlükler girer ve ayrıca Alacak hesapları veya Borç hesapları yabancı para birimi yeniden değerleme işlemini çalıştırır. Bu konuda, bu kuruluşlar Microsoft Dynamics 365 for Operations'ı sürüm 1611'e yükseltirken izlemeleri gereken adımlar açıklanmaktadır.

Microsoft Dynamics 365 for Operations sürüm 1611'e yükseltmek için bu adımları izleyin.

1.  Finance and Operations'ı yükseltmeden önce Alacak hesapları ve Borç hesapları için yabancı para birimi yeniden değerleme işlemlerini çalıştırın. **Yöntem** alanı ayarını **Fatura tarihi** yapın. Son yabancı para birimi yeniden değerleme işlemini tersine çeviren bir yeniden değerleme hareketi oluşturulur. Bu nedenle, açık hareketler orijinal muhasebe para birimleriyle değerlendirilir.
2.  Sürüm 1611'e yükseltin.
3.  Alacak hesapları ve Borç hesapları yabancı para birimi yeniden değerleme işlemlerini yeniden çalıştırın. Bu kez, **Yöntem** alanı ayarını **Standart** yapın. Geçerli döviz kurları temel alınarak yeni bir yeniden değerleme hareketi oluşturulur. Bu hareket gerçekleşmemiş kazanç/kayıp ve doğru özet genel muhasebe hesabını kaydeder.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]