---
title: Endeks oranlarını ayarlama
description: Bu makalede, endeks oranlarının nasıl ayarlanacağı açıklanmaktadır. Kuruluşunuz, kira ödeme tutarlarını bir endeks oranları kümesiyle ilişkilendiriyorsa endeks oranları gereklidir.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRateType
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e700c6c0c66b855a3e329302ac27681f4d0144a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883401"
---
# <a name="set-up-index-rates"></a>Endeks oranlarını ayarlama

[!include [banner](../includes/banner.md)]

Kira ödemeleri bir endekse bağlıysa endeks oranı türleri sisteme eklenebilir ve korunabilir. Kira ödemelerini **Endeks oranı türü** sayfasında yeniden değerlemek için, endeks oranı yeniden değerleme işleminde yeniden değerleme tarihindeki en güncel endeks oranı kullanılır.

Endeks oranı türleri ve endeks oranları eklemek için bu adımları izleyin.

1. **Varlık kiralama \> Kurulum \> Endeks oranı türü**'ne gidin.
2. **Yeni**'yi seçin.
3. Uygun alanlara oran türünü ve endeks oranı adını girin.
4. Yeni bir endeks oranı değeri eklemek için endeks oranı türünü seçin ve ardından **Ekle**'yi seçin.
5. Oranın efektif başlangıç tarihini seçin ve oran değerini belirleyin.

Endeks oranı yöntemi olarak **Endeks oranı değer farkı**'nı veya **Endeks oranı değeri**'ni seçmeniz gerekir.

- Başlangıç tarihindeki endeks oranı ve en güncel endeks oranı arasındaki farkı temel alarak yeni bir kira ödemesini hesaplamak için **Endeks oranı değer farkı** yöntemini seçin. Endeks oranı **Endeks oranı (%)** alanında tanımlanır.
- **Endeks oranı (%)** alanında belirtilen yüzdeyi kullanarak kira ödemesini hesaplamak için **Endeks oranı değeri** yöntemini seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
