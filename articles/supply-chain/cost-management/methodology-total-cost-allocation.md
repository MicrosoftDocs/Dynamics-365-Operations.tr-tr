---
title: Toplam maliyet tahsisat yöntemi
description: Bu konuda, toplam maliyet tahsisatı (TCA) kullanma yönergeleri sağlanmıştır. Toplam maliyet tahsisatı (TCA), bir toplu iş emrine yönelik ana formül maddesi ile formül için tanımlanmış ortak ürünler arasındaki maliyetin hesaplanmasına yönelik bir yöntemdir.
author: AndersGirke
ms.date: 04/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, PmfFormulaCoBy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 83852
ms.assetid: 7c14c3e5-9476-4a79-a210-e77fc91cc7fc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c11b847b5b7995e4eb61e69888aa00d4a5d4478850ce6a346561e0ea0e256b5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715854"
---
# <a name="total-cost-allocation-method"></a>Toplam maliyet tahsisat yöntemi

[!include [banner](../includes/banner.md)]

Toplam maliyet tahsisi (TCA), bir toplu iş emrine yönelik ana formül maddesi ile formül için tanımlanmış ortak ürünler arasındaki maliyet farklarının hesaplanmasına yönelik bir yöntemdir. Bu dinamik bir yöntemdir. Maliyeti, formül maddesi ve ortak ürün için bitmiş olarak raporlanan miktarlar arasındaki bir ağırlıklı ortalama olarak hesaplar. TCA kullanıldığında, her toplu iş emri için maliyet tahsisatı gözden geçirmeniz gerekmez. TCA kullanılmıyorsa, formül hesaplaması mevcut işlevi kullanır.

## <a name="using-tca-for-coproducts"></a>Ortak ürünler için TCA kullanma
Ortak ürünler için TCA kullanmaya yönelik bazı yönergeler şunlardır:

-   Bir formül sürümü için **Toplam Maliyet Tahsisi** kaydırıcısını **Evet** olarak ayarlarsanız, ortak ürünlerin maliyet fiyatı 0'dan (sıfır) fazla olacaktır. Değer aynı tesise veya formülün tesise özel olmadığı ilk tesise yönelik etkin maliyet sürümünden alınabilir. Bu koşul formül onaylandığında doğrulanır.

    -   Yan ürünler için maliyet tahsisat yüzdelerini el ile girmeniz gerekmez. Bunun yerine, sistem ortak ürünlerin maliyet fiyatlarının etkin ortalama maliyet tahsisat yüzdesini otomatik olarak oluşturur. 
    -   Yan ürünler olan standart olmayan maliyet maddeleri için standart maliyetleri girmeniz gerekmez. Sistemde iki türde maliyetlendirme sürümü vardır: standart maliyet ve planlı maliyet 
    -   Bir madde standart maliyet değerleme yöntemi ile değerlendirilmediyse, planlı maliyet sürümünde bir etkin maliyet fiyatını kullanmanızı öneririz. Bu fiyat maliyet tahmini için kullanılır, örneğin ürün reçetesi hesaplaması, üretim maliyeti tahmini ve stok değerleme işleminde geri dönüş fiyatı. 

-   Formül sürümü için **Toplam Maliyet Tahsisi** kaydırıcısını **Evet** olarak ayarlarsanız ve aşağıdaki koşullar doğru ise, maliyet tahsisi yöntemi **TCA** olur ve maliyet tahsisi yüzdesi değişmez:
    -   Ortak ürünler eklediniz.
    -   Ortak ürünler için farklı bir maliyet tahsisi yöntemi kullandınız.
-   Formül sürümü için **Toplam Maliyet Tahsisi** kaydırıcısını **Hayır** olarak ayarlarsanız ve aşağıdaki koşullar doğruysa, maliyet tahsisi yöntemi **Manuel** olarak değişir ve maliyet tahsisi yüzdesi değişmez:
    -   Ortak ürünler eklediniz.
    -   Maliyet tahsisi yüzdesi 0'dan (sınıf) yüksektir.
-   Başarıyla formül hesaplayabilmek için önce maliyet tahsisatı yüzdelerini tahmin etmeniz gerekir. Bu adımı el ile veya **Ortak ürünler** sayfasındaki **Tahmini maliyet** seçeneğini kullanarak tamamlayabilirsiniz. **Not:** **Tahmini maliyet** seçeneği yalnızca formül sürümü için **Toplam Maliyet Tahsisatı** kaydırıcısı **Evet** olarak ayarlı ise kullanılabilir. Bitmiş olarak rapor edilen toplu iş emri miktarları formülde görülen miktarlarla eşleşiyorsa, beklenen tahsisatı görüntüleyebilirsiniz.
-   Bir toplu iş emri el ile oluşturulduğunda veya planlı bir toplu iş emri kesinleştiğinde formül sürümü için **Toplam Maliyet Tahsisatı** kaydırıcısının değeri toplu iş emrine kopyalanır. Ancak, bu ayarı toplu iş emri üzerinde değiştirebilirsiniz. Formül sürümü için **Toplam Maliyet Tahsisatı** kaydırıcısı **Hayır** olarak ayarlı ise ve sonrasında toplu iş emri için **Evet** olarak değiştirilirse, her bir satır için **Manuel** olarak ayarlanmış olan maliyet tahsisatı yöntemi **TCA** olarak değiştirilir. Maliyet tahsisatı **Hiç** olarak kalır. Formül sürümü için **Toplam Maliyet Tahsisatı** kaydırıcısı **Evet** olarak ayarlı ise ve sonrasında toplu iş emri için **Hayır** olarak değiştirilirse, **Üretim** tipinin her bir ortak ürünü için maliyet tahsisatı yöntemi **TCA** olarak değiştirilir. Tahmini maliyet tahsisatı yüzdesi değişmez.
-   **Ortak ürün maliyet tahsisatı** sayfası hesaplanan maliyet tahsisatı yüzdesini gösterir. Bu sayfayı **Toplu iş emri** sayfasından açabilirsiniz. Bu bilgiler, raporlanan ürün ve miktarlar toplu iş emri üzerinde zamanlanan veya başlatılan miktarlardan farklı olduğunda yararlıdır. Maliyet tamamlandığında, TCA'dan bu yeni yüzde tahsisatları **Ortak ürün maliyet tahsisatı** sayfasında gösterilir.

## <a name="calculating-the-burden-for-byproducts"></a>Yan ürünler için yükü hesaplama
**Ortak ürünler** sayfasındaki **Yan ürün maliyet tahsisatı** alanı yalnızca yan ürünler için kullanılan bir numaralandırıcı alandır. Ortak ürünler için bu alanın değeri her zaman **Hiç**'tir. Yan ürün satırları için bu alan yan ürün satırı için maliyet tutarının toplam üretim maliyetine nasıl ekleneceğini belirler. Aşağıdaki seçenekler bulunur:

-   **Hiç** ─ Bu yan ürün satırı için toplam üretim maliyetine hiçbir tutar eklenmez.
-   **Yüzde** ─ Maliyet tutarı, üretimde tüketilen toplam hammadde maliyeti yüzdesi olarak hesaplanır. Hesaplamada kullanılan yüzde bu alana girilir.
-   **Seri başına** ─ Maliyet tutarı, üretim emrinin standart toplu iş boyutu başına tutar olarak hesaplanır. Bu tutar, üretimde rapor edilen miktardan bağımsızdır. Hesaplamada kullanılan tutar bu alana girilir.
-   **Miktar başına** ─ Maliyet tutarı üretimdeki formül maddenin rapor edilen miktarı başına tutar olarak hesaplanır. Hesaplamada kullanılan tutar bu alana girilir.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]