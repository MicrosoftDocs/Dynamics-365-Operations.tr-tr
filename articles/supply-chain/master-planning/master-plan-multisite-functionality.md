---
title: Master planlama ve birden çok tesis işlevine genel bakış
description: Master planlama, tesis ve ambar stok boyutlarının ayarlarını dikkate alır.
author: roxanadiaconu
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b26ff5c2f580c30113b82302bbad744bbf285ff
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213734"
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



