---
title: Üretilen ya da temin edilen ürünleri ayarlama
description: Ürünler çeşitli şekillerde bulunabilir - üretilebilir (mamul) veya tedarik edilebilir (satın alınan). Bu makalede birden fazla kaynak kullanımının desteklenmesi için ürünlerin nasıl yapılandırılacağı ile ilgili bazı genel hususlar açıklanmıştır.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4910faa2e66cb61f6064e686c49369d14526cc1f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674519"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a>Üretilen ya da temin edilen ürünleri ayarlama

[!include [banner](../includes/banner.md)]

Ürünler çeşitli şekillerde bulunabilir - üretilebilir (mamul) veya tedarik edilebilir (satın alınan). Bu makalede birden fazla kaynak kullanımının desteklenmesi için ürünlerin nasıl yapılandırılacağı ile ilgili bazı genel hususlar açıklanmıştır. 

Çoklu kaynak, genellikle arada sırada üretilen satın alınmış bir ürün için ya da esas olarak üretilen bir ürün esasen satın alınan bir ürün haline gelecek şekilde değiştirildiğinde kullanılır. Ürün, ürün reçetesi ve rota bilgilerinin tanımlanabilmesi ve ürünün üretim emirlerinin desteklenmesi için önce üretilen ürün olarak belirlenir. Üretim türü, **Ürün reçetesi** (ya da süreç üretimi için **Formül** veya **Ortak ürün**) şeklinde ayarlanmalıdır.

Standard maliyet kullandığınızda, üretilen ürün için ürün maliyet kaydı hesaplanabilir. Ancak, ürün maliyeti kaydı satın alma amaçlarıyla istediğiniz standart maliyet ile eşleşmeyebilir. Bu durumda, istediğiniz standart maliyet ürün maliyet kaydı için el ile girilmeli ve etkinleştirilmelidir. Maliyet hesaplaması için, zaman içinde ortaya çıkan farkları minimize etmek için bir mali dönem boyunca ürünün tedarik karmasını gösteren özel bir ürün reçetesi ve rota kullanmayı düşünün. Ek olarak, bir tesiste üretilen bir ürün başka bir tesise aktarılabilir. Bu nedenle, ürünün maliyeti el ile girilmeli ve transfer edildiği tesis için etkinleştirilmelidir. Üretilmiş bir ürünü daha üst düzeylerdeki ürünler için bir bileşen olarak kullandığınızda, satınalınan bir ürün olarak ele alınmalıdır. Bu kılavuz, bileşenin maliyetinin hesaplanıp hesaplanmadığına veya el ile girilip girilmediğine bakılmaksızın geçerlidir. Diğer bir deyişle, Ürün reçetesi hesaplaması ürünün maliyetini maliyetleri hesaplamak amacıyla ürünün ürün reçetesini ve rota bilgileri kullanmak yerine satın alınan bir bileşen olarak ele almalıdır. 

Hesaplamanın gerçekleşmesini önlemek için, ürüne atanan ürün reçetesi hesaplama grubunda gömülü **Açılımı durdur** bayrağını seçin. Master planlama hesaplamalarının ürün üzerinden gereksinimleri açmasını önlemek için ürün açılımı ya da ürün açılımı grubunda açılım dilimini 0 (sıfır) gün olarak ayarlayın. Master planlama hesaplaması, ürünü satın alınan bir ürün olarak ele alacaktır ve ürünün ürün reçetesi ve rota bilgileri için daha fazla hesaplama gerçekleştirmeyecektir.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]