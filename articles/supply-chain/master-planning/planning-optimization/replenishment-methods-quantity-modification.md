---
title: Stok yenileme yöntemleri ve miktar değişikliği
description: Bu konu, Planlamayı En İyi Duruma Getirme'deki stok yenileme yöntemleri hakkında bilgi sağlar. Ayrıca, bir ürün için birden çok sipariş miktarının sonucu nasıl etkilediğini açıklar.
author: t-benebo
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc7eb00f62b334ba032af6fef87c243a7ba0835a
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468552"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Stok yenileme yöntemleri ve miktar değişikliği

[!include [banner](../../includes/banner.md)]

Bu konu, Planlamayı En İyi Duruma Getirme'deki stok yenileme yöntemleri hakkında bilgi sağlar. Ayrıca, bir ürün için birden çok sipariş miktarının sonucu nasıl etkilediğini açıklar.

Stok yenileme yöntemleri, karşılama yöntemleri ve lot boyutlandırma yöntemleri olarak da bilinir.

## <a name="coverage-codes"></a>Karşılama kodları

Planlamayı En İyi Duruma Getirme farklı stok yenileme yöntemleri kullanacak şekilde yapılandırılabilir. Stok yenileme yöntemleri, sistemin bir ürünün gereksinimlerini hesaplamak için kullandığı tekniklerdir. Stok yenileme yöntemleri, karşılama grubunda veya üründe ayarlayabileceğiniz karşılama kodları tarafından tanımlanır.

Planlamayı En İyi Duruma Getirme'de aşağıdaki karşılama kodları kullanılabilir:

- **Dönem**: Ürün için bir döneme ait tüm talepleri tek bir siparişte olacak şekilde birleştiren stok karşılama yöntemi. Sipariş dönemin ilk günü için planlanacaktır ve miktarı ayarlanan dönem içindeki net gereksinimleri karşılayacaktır. Dönem, ürüne yapılan ilk taleple başlar ve tanımlanan süreyi olduğu gibi kapsar. Sonraki dönem, ürünün sonraki gereksinimleri itibarıyla başlar. *Dönem* karşılama kodu genellikle tahmin edilemeyen stok çekme, sezondan etkilenen ürünler veya yüksek maliyetli ürünler için kullanılır. Aşağıdaki şekilde bir örneği gösterilmiştir.

    ![Dönem karşılama kodu kullanımı örneği.](./media/coverage-code-period.png "Dönem karşılama kodu kullanımı örneği")

- **Gereksinim**: Sistemin ürün için her gereksinim başına bir planlı satınalma, transfer veya üretim emri oluşturduğu stok yenileme yöntemidir. Bu yöntem, aralıklı talebi olan pahalı ürünler için kullanılır. *Gereksinim* karşılama kodu genellikle yapılandırılabilir ürünler veya siparişe göre üretim senaryoları için kullanılır. Aşağıdaki şekilde bir örneği gösterilmiştir.

    ![Gereksinim karşılama kodu kullanımı örneği.](./media/coverage-code-requirement.png "Gereksinim karşılama kodu kullanımı örneği")

- **Minimum/Maksimum** – Stok yenileme yöntemi stok düzeyini temel alır. Tahmin edilen eldeki düzey belirli bir eşiğin altında olduğunda, stoğun belirli bir düzeye kadar yenilenmesini tanımlar. Stok yenileme miktarı maksimum düzey ve eldeki tahmini düzey arasındaki fark olur. *Min./Maks.* karşılama kodu genellikle öngörülebilir stok çekme, hızlı giden öğeler veya daha ucuz ürünler için kullanılır. Aşağıdaki şekilde bir örneği gösterilmiştir.

    ![Min./Maks. karşılama kodu kullanımı örneği.](./media/coverage-code-min-max.png "Min./Maks. karşılama kodu kullanımı örneği")

- **El ile**: Sistemin ürün için satın alma, transfer veya üretim emirleri önermediği stok yenileme yöntemi. Bunun yerine, ürünün planlayıcısı, ürün stoğunun yenilenmesi için gerekli siparişleri oluşturmaktan sorumludur. *Manuel* karşılama kodu genellikle sistem tarafından oluşturulan planlı siparişlerin istenmediği ürünler için kullanılır.

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a>Sipariş miktarının ayarlarındaki sipariş miktarının etkisi

Serbest bırakılmış bir ürünün **Varsayılan sipariş ayarı** sayfasında, **Satınalma siparişi**, **Stok** ve **Satış siparişi** Hızlı Sekmelerinde aşağıdaki miktar ayarlarının her birini belirtebilirsiniz. (**Stok** Hızlı Sekmesi hem transfer emirleri hem de üretim emirleri için kullanılır.)

- **Çarpan**: Planlı siparişler bu miktarın katı olacaktır.

    Örneğin, **Çarpan** alanı *5* olarak ayarlanmışsa, sipariş 5, 10, 15, 20 vb. bir miktar için olabilir.

- **Minimum sipariş miktarı**: Planlı siparişler belirtilen değerden az olmayacaktır.

    Örneğin, **Minimum sipariş miktarı** alanı *10* olarak ayarlanırsa, talebi karşılamak için yalnızca dört tane gerekli olsa bile, 10 adet için planlı bir sipariş oluşturulur.

- **Maksimum sipariş miktarı**: Planlı siparişler belirtilen değeri aşamaz. Talep **Maksimum sipariş miktarı** değerinden fazlaysa, bunu karşılamak için birden çok planlı sipariş oluşturulur.

    Örneğin, **Maksimum sipariş miktarı** alanı *100* olarak ayarlanırsa ve talep 450 ise, 100 miktarı için dört planlı sipariş ve 50 miktarı için bir planlı sipariş oluşturulur.

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a>Min/Maks kullanan stok yenileme örnekleri karşılama kodu

**Varsayılan sipariş ayarı** sayfasındaki bir ürün için **Çarpan** alanında bir değer belirtmezseniz ve *Min/Maks* stok yenileme yöntemi kullanıyorsanız Planlamayı En İyi Duruma Getirme, tahmin edilen eldeki stok düzeyi belirli bir eşiğin altında olduğunda, stoğun belirli bir düzeye kadar yeniler.

Bir ürün için çarpan miktarı tanımlarsanız, *Min./Maks.* yenileme yöntemi davranışını değiştirir ve **Çarpan** değerini dikkate alır.

Başka bir deyişle, Planlamayı En İyi Duruma Getirme, tahmin edilen eldeki stok düzeyi tanımlanan minimum düzeyden daha az olduğunda stoğu tanımlanan maksimum düzeye kadar yenilemeye devam eder. Ancak, stok yenileme miktarı **Çarpan** değerinin katı olmalıdır.

Stok yenileme miktarı (maksimum düzey ile tahmin edilen eldeki stok düzeyi arasındaki fark) tanımlanan çarpan miktarının katı değilse, Planlamayı En İyi Duruma Getirme, tahmin edilen eldeki stok düzeyiyle birlikte en yüksek düzeyin altında olacak ilk olası değeri kullanır. Toplam minimum düzeyden küçükse, Planlamayı En İyi Duruma Getirme, tahmin edilen eldeki stokla birlikte maksimum düzeyin üzerinde olacak ilk değeri kullanır.

Aşağıdaki alt bölümler, bir ürün için çarpan miktarının *Min./Maks* stok yenileme yönteminin sonucunu nasıl etkilediğini gösteren bazı örnekler sağlar.

### <a name="example-1"></a>Örnek 1

Bir ürün aşağıdaki yapılandırmaya sahiptir:

- **Karşılama kodu:** *Min./Maks.*
- **Minimum:** *15*
- **Maksimum:** *22*
- **Çarpan:** *0*

Ürün için eldeki stok 10 adettir ve başka bir talep veya tedarik yoktur.

Master planlama çalıştırıldığında, stoğu maksimum miktara yenilemek için 12 parça için planlı bir sipariş oluşturulur.

### <a name="example-2"></a>Örnek 2

Bir ürün aşağıdaki yapılandırmaya sahiptir:

- **Karşılama kodu:** *Min./Maks.*
- **Minimum:** *15*
- **Maksimum:** *22*
- **Çarpan:** *5*

Ürün için eldeki stok 10 adettir ve başka bir talep veya tedarik yoktur.

Master planlama çalıştırılğında, 10 adet için planlı bir sipariş oluşturulur (çünkü 15 adet stok yenileme artı 10 adet eldeki stok maksimum miktarı aşacaktır).

### <a name="example-3"></a>Örnek 3

Bir ürün aşağıdaki yapılandırmaya sahiptir:

- **Karşılama kodu:** *Min./Maks.*
- **Minimum:** *21*
- **Maksimum:** *24*
- **Çarpan:** *5*

Ürün için eldeki stok 10 adettir ve başka bir talep veya tedarik yoktur.

Master planlama çalıştırılğında, 15 adet için planlı bir sipariş oluşturulur (çünkü 10 adet stok yenileme artı 10 adet eldeki minimum miktardan az olacaktır).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
