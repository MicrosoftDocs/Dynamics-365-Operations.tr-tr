---
title: "Master planlama ve birden çok tesis işlevi"
description: "Master planlama, tesis ve ambar stok boyutlarının ayarlarını dikkate alır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19eeee753c15cf2670948ce2c615a112813c16ad
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-and-multisite-functionality"></a>Master planlama ve birden çok tesis işlevi

Master planlama, tesis ve ambar stok boyutlarının ayarlarını dikkate alır. 

Tesis boyutu zorunludur ve ambar boyutunu da zorunlu olacak şekilde ayarlayabilirsiniz.

Bir boyut zorunlu olduğunda tüm boyut hareketlerine bir boyut değeri girilmelidir. Böylece master planlama sırasında, başlangıç talebi için tesis ve ambar bilinir. Ayrıca tesis boyutu, daha alt düzey taleplerin açılımı sırasında tesisin değeri değişmeyecek şekilde tutarlıdır.

Ambar zorunlu olarak ayarlanmadığında başlangıç talebinden bilinemez. Planlama altyapısı, kullanılacak ambarı madde ve ayrı ambar için tanımlanan ayarlara ve sipariş satırının ayrıntılarına göre belirlemelidir.

Aşağıdaki wiki makaleleri, farklı ayarlar tanımlandığında planlama altyapısının kullanılacak ambarı belirlemek için nasıl çalıştığını açıklanır.

[Master planlama - tesis ve ambar kapsamı, ambar zorunlu](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Master planlama - tesis kapsamı, ambar zorunlu](master-plan-site-coverage-warehouse-mandatory.md)

[Master planlama - tesis ve ambar kapsamı, ambar zorunlu değil](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Master planlama - tesis kapsamı, ambar zorunlu değil](master-plan-site-coverage-warehouse-not-mandatory.md)

[Master planlama - Ürün reçetesi sürümünün nasıl belirlendiği](master-plan-bom-version-determined.md)


