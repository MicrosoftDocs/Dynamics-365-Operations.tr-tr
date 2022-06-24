---
title: Eşik sınırı ve özel durum eşik sınırı
description: Bu makalede, Kaynakta Kesilen Vergi (TDS) için eşik ve istisna sınırları açıklanmaktadır.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: aceebad08b5454b64059e7ef374b9634bad35c37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877950"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>Eşik sınırı ve özel durum eşik sınırı

[!include [banner](../includes/banner.md)]

Bu makalede, Kaynakta Kesilen Vergi (TDS) için eşik ve istisna sınırları açıklanmaktadır. Fatura ve ödemelerle ilgili TDS, **Stopaj vergisi bileşenleri** sayfasındaki TDS vergi bileşenleri için belirlenen eşik sınırı ve istisna eşik sınırı dikkate alınarak hesaplanır. TDS vergi bileşenleri, TDS vergi gruplarına dahil olan TDS vergi kodlarına bağlıdır. TDS vergi grupları, TDS'yi fatura düzeyinde veya ödeme düzeyinde hesaplamak için satıcılara ve müşterilere iliştirilir.

TDS, bir hareket tutarı ya da bir satıcı için belirli birTDS grubuyla deftere nakledilen kümülatif hareketler, **Stopaj vergisi bileşenleri** sayfasında belirtilen eşik sınırını aşarsa hesaplanır. TDS, kümülatif hareket tutarı belirtilen eşik sınırını aşıncaya kadar hesaplanmaz.

Bir TDS bileşeni için eşik sınırının yanı sıra bir de istisna eşik sınırı belirlenmişse TDS, belirli bir hareket tutarı istisna eşik sınırını aştığında hesaplanır (kümülatif hareket tutarı, belirtilen eşik tutarını aşmasa bile).

### <a name="example"></a>Örnek
TDS adlı bir vergi bileşeni ayarlandı ve Yüklenici adlı TDS vergi grubuna iliştirildi. Eşik 50.000 olarak tanımlanmıştır ve istisna eşik değeri TDS vergi bileşeni için 20.000 olarak tanımlanmıştır. TDS grubu yüklenicisi, satıcı 1 için varsayılan TDS grubu olarak tanımlanmıştır.

Satıcı 1'in 10.000 değerindeki satınalma faturası 001, deftere nakledildi. Fatura tutarı, eşik sınırını veya istisna eşik sınırını aşmadığı için fatura için TDS hesaplanmadı. Satıcı 1'in 25.000 değerindeki satınalma faturası 002, deftere nakledildi. Fatura tutarı, eşik istisna eşik sınırını aştığından fatura için TDS hesaplandı. Satıcı 1'in 20.000 değerindeki satınalma faturası 003, deftere nakledildi. Satıcıya kesilen üç faturanın toplam miktarı eşik sınırını aştığından fatura için TDS hesaplandı. TDS, satıcıya kesilen ve daha önce TDS'nin hesaplanmadığı tüm faturalarda hesaplanır. Bu nedenle TDS, 001 ve 003 fatura tutarının toplam fatura tutarı olan 30.000 değerinden hesaplanır.

Hareketle ilişkili TDS grubunda TDS vergi kodları için **Eşiği dikkate alma** onay kutusu seçiliyse TDS hesaplamasında eşik sınırı ve istisna eşik sınırı dikkate alınmaz. **Eşiği dikkate alma** onay kutusunun ait olduğu TDS grubundaki TDS vergi kodlarında eşik sınırı kullanılmaz.

Bazı faturaların belirli TDS grubu için **Eşiği dikkate alma** onay kutusu işaretlenmiş ancak belirli bir satıcı/müşteri için oluşturulmuş diğer faturalar için işaretlenmemişse, birkaç faturanın eşik sınırını dikkate alan TDS hesaplaması, TDS'nin daha önce hesaplanmadığı tüm faturalarda kümülatif tutar dikkate alınarak hesaplanabilir.

Örneğin, eşik sınırı 25.000 olsun. Satıcı A için aşağıdaki faturalar oluşturulur.

- Fatura 1 – 20.000-( **Eşiği dikkate alma** onay kutusu seçili değil): TDS hesaplanmaz.

- Fatura 2 – 4.000 – ( **Eşiği dikkate alma** onay kutusu seçili): TDS, 4.000'de hesaplanmaz.

- Fatura 2 – 3.000 – ( **Eşiği dikkate alma** onay kutusu seçili değil): TDS kümülatif fatura tutarı olarak hesaplanır, yani 27.000 (20.000+4.000+3.000) eşik sınırını aştı. TDS, TDS'nin daha önce hesaplanmadığı kümülatif fatura tutarında hesaplanır, yani 23.000'de (20.000+3000).
