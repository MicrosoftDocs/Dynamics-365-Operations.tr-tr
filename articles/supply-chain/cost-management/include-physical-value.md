---
title: "Fiziksel değeri dahil et"
description: "Madde modeli grupları formunun Stok modeli FasTab'indeki Fiziksel değeri dahil et onay kutusu fiziksel olarak güncelleştirilmiş hareketlerin bir madde için devam eden ortalama maliyet fiyatının hesaplanmasına dahili edilip edilmeyeceğinin belirlenmesi için kullanırsınız."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ea8fe31588dd0768e0651c9e1e332212a00cde2
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="include-physical-value"></a>Fiziksel değeri dahil et

[!include [banner](../includes/banner.md)]

Madde modeli grupları formunun Stok modeli FasTab'indeki Fiziksel değeri dahil et onay kutusu fiziksel olarak güncelleştirilmiş hareketlerin bir madde için devam eden ortalama maliyet fiyatının hesaplanmasına dahili edilip edilmeyeceğinin belirlenmesi için kullanırsınız.

**Fiziksel değeri dahil et** onay kutusu aşağıdaki değerlere sahiptir.

| Değer    | Sonuç                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Seçildi | Devam eden ortalama maliyet fiyatının hesaplanması için hem fiziksel olarak güncelleştirilen hareketler hem de mali olarak güncelleştirilen hareketler kullanılır. |
| Temizlendi  | Devam eden ortalama maliyet fiyatının hesaplanması için sadece mali olarak güncelleştirilen hareketler kullanılır.                                     |

Onay kutusu, kullandığınız stok modeline bağlı olarak bir miktar farklı etkilere sahiptir.

-   FIFO (İlk giren, ilk çıkan), LIFO (Son giren, ilk çıkar) veya LIFO tarihi stok modelini kullandığınızda **Fiziksel değeri dahil et** onay kutusunu işaretlerseniz, stok kapanışı ayrıca fiziksel olarak güncelleştirilen hareketlerde de düzenlemeler yapar.
-   Bu stok modellerini kullandığınızda **Fiziksel değeri dahil et** onay kutusunu işaretlemezseniz, stok kapanışı yalnızca mali olarak güncelleştirilen hareketlerde kapatmalar yapar.
-   Ağırlıklı ortalama veya ağırlıklı ortalama tarih stok modelini kullanırken stok, **Fiziksel değeri dahil et** onay kutusunu işaretlemenizden veya işaretlememenizden bağımsız olarak yalnızca mali olarak güncelleştirilmiş hareketleri kapatır.

**Örnek 1** **Fiziksel değeri dahil et** onay kutusunu seçtiniz ve aşağıdaki satın alma emirlerini aldınız:

-   10,00 ABD Doları maliyet fiyatında 2 miktarı için bir satın alma emri için sevk irsaliyesi güncelleştirildi.
-   12,00 ABD Doları maliyet fiyatında 3 miktarı için bir satın alma emri için fatura güncelleştirildi.

Bu durumda, maliyet fiyatının hesaplanmasında hem fiziksel olarak güncelleştirilmiş hem mali olarak güncelleştirilmiş hareketler kullanıldığından, cari ortalama maliyet fiyatı 11,20 ABD Doları olur. **Örnek 2** **Fiziksel değeri dahil et** onay kutusunu işaretlemezseniz ve madde kurulumundaki maliyet fiyatı 10,00 USD ise. 12,00 ABD Doları maliyet fiyatında 20 miktarı için sevk irsaliyesi güncelleştirilmiş bir satın alma emri alırsınız. Bir satış siparişi nakledildiğinde, cari ortalama maliyet fiyatı fiziksel olarak nakledilmiş hareketleri içermeyeceğinden, maliyet tutarı olarak 10,00 ABD Doları nakledilir. **Not:** Karşılaştırma amacıyla, bu madde için **Fiziksel değeri dahil et** onay kutusunu işaretlerseniz, bir satış siparişi deftere nakledildiğinde nakledilen maliyet tutarı 12,00 Amerikan Doları olacaktır.




