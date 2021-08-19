---
title: Fiziksel değeri dahil et
description: Madde modeli grupları formunun Stok modeli FasTab'indeki Fiziksel değeri dahil et onay kutusu fiziksel olarak güncelleştirilmiş hareketlerin bir madde için devam eden ortalama maliyet fiyatının hesaplanmasına dahili edilip edilmeyeceğinin belirlenmesi için kullanırsınız.
author: AndersGirke
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 711c30376c4f1ecc5c1a747c675e6438a867c51ed066b6c15cdace6a071f7cfd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751134"
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

-   10,00 ABD Doları maliyet fiyatında 2 adetlik bir satınalma siparişi için sevk irsaliyesi güncelleştirildi.
-   12,00 ABD Doları maliyet fiyatında 3 adetlik bir satınalma siparişi için fatura güncelleştirildi.

Bu durumda, maliyet fiyatının hesaplanmasında hem fiziksel olarak güncelleştirilmiş hem mali olarak güncelleştirilmiş hareketler kullanıldığından, cari ortalama maliyet fiyatı 11,20 = (2x10+3x12)/(2+3) ABD Doları olur. 

**Örnek 2** **Fiziksel değeri dahil et** onay kutusunu işaretlemezseniz ve madde kurulumundaki maliyet fiyatı 10,00 USD ise. 

-   12,00 ABD Doları maliyet fiyatında 20 miktarı için sevk irsaliyesi güncelleştirilmiş bir satın alma emri alırsınız.

Bir satış siparişi nakledildiğinde, cari ortalama maliyet fiyatı fiziksel olarak nakledilmiş hareketleri içermeyeceğinden, maliyet tutarı olarak 10,00 ABD Doları nakledilir. 

> [!NOTE]
> Karşılaştırma amacıyla, bu madde için **Fiziksel değeri dahil et** onay kutusunu işaretlerseniz bir satış siparişi deftere nakledildiğinde nakledilen maliyet tutarı 12,00 ABD Doları olacaktır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]