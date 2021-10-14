---
title: Master planlama ve birden çok tesis işlevine genel bakış
description: Master planlama, tesis ve ambar stok boyutlarının ayarlarını dikkate alır.
author: ChristianRytt
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2434"
- intro-internal
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edcf35ea0a5be870d8a57cd782664d0a0b77de5c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575693"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Master planlama ve birden çok tesis işlevine genel bakış

[!include [banner](../includes/banner.md)]

Master planlama, tesis ve ambar stok boyutlarının ayarlarını dikkate alır. 

Tesis boyutu zorunludur ve ambar boyutunu da zorunlu olacak şekilde ayarlayabilirsiniz.

Bir boyut zorunlu olduğunda tüm boyut hareketlerine bir boyut değeri girilmelidir. Böylece master planlama sırasında, başlangıç talebi için tesis ve ambar bilinir. Ayrıca tesis boyutu, daha alt düzey taleplerin açılımı sırasında tesisin değeri değişmeyecek şekilde tutarlıdır.

Ambar zorunlu olarak ayarlanmadığında başlangıç talebinden bilinemez. Planlama altyapısı, kullanılacak ambarı madde ve ayrı ambar için tanımlanan ayarlara ve sipariş satırının ayrıntılarına göre belirlemelidir.

Aşağıdaki konularda, farklı ayarlar tanımlandığında planlama altyapısının kullanılacak ambarı belirlemek için nasıl çalıştığını açıklanır.

[Tesis ve ambar kapsamı için master planlama, ambar zorunlu](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Tesis kapsamı için master planlama, ambar zorunlu](master-plan-site-coverage-warehouse-mandatory.md)

[Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Tesis kapsamı için master planlama, ambar zorunlu değil](master-plan-site-coverage-warehouse-not-mandatory.md)

[Ürün reçetesi sürümünü belirleme](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]