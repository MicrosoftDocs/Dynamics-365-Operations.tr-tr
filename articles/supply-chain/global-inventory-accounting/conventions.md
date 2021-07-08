---
title: Kurallar
description: Bu konuda, Global Stok Muhasebesinde maliyetlerin nasıl muhasebeleştirileceğini belirlemek üzere nasıl kural ayarlanacağı açıklanmıştır.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 74d99d3eefdcaaa7f6551668990b702396b32ffc
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273240"
---
# <a name="conventions"></a>Kurallar

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Kural, sistem davranışını etkileyen ilke kümesi için bir kapsayıcıdır. İş gereksinimlerinize göre, Global Stok Muhasebesinde maliyetlerin nasıl muhasebeleştirileceğini belirleyen çeşitli ilkelerin bir bileşimini kullanarak kurallar tanımlamanız gerekir. Genel defterlerde uygulanan muhasebe ilkelerine tutarlılığı sağlamak için, her kuralı bir veya daha fazla defterle ilişkilendirebilirsiniz.

Kurallarınızı ayarlamak için, **Global stok muhasebesi \> Kurulum \> Kurallar**'a gidin. Her kural için aşağıdaki alanları ayarlayın:

- **Ad**: Kuralın adını girin.
- **Açıklama**: Kuralın açıklamasını girin.
- **Maliyet Nesnesi ilkesi** – Maliyet nesnesi ilkesi seçin. Bu ilkeler, sistemin stok değerini hesaplamak ve sürdürmek için uyguladığı ayrıntı düzeyini belirler. Önceden tanımlanmış aşağıdaki seçenekler bulunur:

    - Ürün
    - Ürün - Tesis
    - Ürün - Tesis – Ambar

    Örneğin, her stok hareketi (giren veya çıkan) için *Ürün - Tesis* seçerseniz sistem, her bir ürünün stok maliyetini tesis düzeyinde hesaplar ve yönetir. Bu nedenle, alt düzeylerdeki stok hareketleri (örneğin ambar düzeyi) stok değerini etkilemez. (Ambar düzeyinde transfer örneği olarak bir tesisdeki iki ambar arasındaki madde transferi verilebilir.) Benzer şekilde, stok maliyetini ambar düzeyi gibi daha düşük bir düzeyde görüntüleyemezsiniz.

- **Giriş ölçüm esası ilkesi**: Giriş ölçüm esası ilkesi seçin. Bu ilkeler stok hesabına akması gereken maliyetleri ve faturalanması gereken maliyetleri belirler. Ticari şirketlerle ilgili seçenekler şunlardır:

    - **Normal geçmiş**: Tüm maliyet bileşenleri stok hesabına akar.
    - **Standart**: Standart maliyet stok hesaplarına akar ve uygulanan maliyet ile fiili maliyetler arasındaki fark, fark hesaplarına yansıtılır. *Standart* giriş ölçüm esası ilkesi oluşturmak istiyorsanız, öncelikle ilkenin maddenin standart maliyetine bakabileceği bir fiyat listesi oluşturmanız gerekir.
    - **Fiyat listeleri**: Global Stok Muhasebesi, birden çok tüzel kişilikten madde fiyatları getirmeyi destekler. Giriş ölçüm esası ilkesinin kullanacağı bir fiyat listesi tanımlayabilirsiniz. Bu şekilde, sistem madde fiyatını nerede arayacağını bilecektir. Fiyat listeleri ayarlamak için aşağıdaki adımları takip edin:

        1. **Ad** alanına, bir ad girin.
        1. **Açıklama** alanına bir açıklama girin.
        1. **Maliyetlendirme türü** alanında, bir maliyetlendirme türü ( *Standart maliyet* veya *Planlanan maliyet*) seçin.
        1. **Fiyat türü** alanında bir fiyat türü ( *Maliyet*, *Satın alma* veya *Satış fiyatı*) seçin.
        1. Maliyetlendirme sürümü ekleyin.
        1. Eylem Bölmesinde, fiyat listesindeki madde fiyatlarını doğrulamak için **Fiyat**'ı seçin.

- **Maliyet akışı varsayım ilkesi**: Maliyet akışı varsayım ilkesi seçin. Bu ilkeler, maliyetlerin stoktan nasıl kaldırılacağını ve satılan malların maliyeti olarak rapor edileceğini belirler. Önceden tanımlanmış aşağıdaki seçenekler bulunur:

    - Ortalama
    - Belirli – Toplu İş

    > [!NOTE]
    > Global Stok Muhasebesi, kalıcı bir stok sistemidir. Bu nedenle, sistem stok değerini hareket hareket esasında izler.

- **Maliyet öğesi ilkesi**: Maliyet öğesi ilkelerini tanımlayabilir ve bunları bu alana bağlayabilirsiniz. *Maliyet öğesi* bir olay tarafından tüketilen bir kaynağın maliyetidir. Maliyet öğelerini, maliyetleri izlemek ve kategorilere ayırmak için kullanabilirsiniz. Maliyet öğesi ilkeleri oluşturmak için aşağıdaki alanlara bilgi girin:

    - **Ad** alanı
    - **Açıklama** alanı
    - **Maliyet öğesi** listesi
    - **Kurallar** ızgarası

    Stok değerini daha fazla bölmek istemiyorsanız, tek bir maliyet öğesine sahip olan bir maliyet öğesi listesi oluşturmanız gerekir. İlgili tüm ölçüm türlerini (maliyet bileşenleri) bu maliyet öğesiyle eşlemek için maliyet öğesi ilkesi oluşturmanız gerekir.
