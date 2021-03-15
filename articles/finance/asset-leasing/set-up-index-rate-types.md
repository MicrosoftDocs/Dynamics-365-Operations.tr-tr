---
title: Endeks oranlarını ayarlama
description: Bu konuda, endeks oranlarının nasıl ayarlanacağı açıklanmaktadır. Kuruluşunuz, kira ödeme tutarlarını bir endeks oranları kümesiyle ilişkilendiriyorsa endeks oranları gereklidir.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f362bf4a6b5de3ce16330aea08880b07b4145792
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992876"
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