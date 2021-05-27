---
title: Madde kalite grupları
description: Bu konu, otomatik oluşturma ve kalite emirleri oluşturmak üzere kalite ilişkilerine atanabilmeleri için ürünleri mantıksal olarak gruplamak üzere madde kalite gruplarının nasıl kullanılacağını açıklar.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022264"
---
# <a name="item-quality-groups"></a>Madde kalite grupları

[!include [banner](../includes/banner.md)]

Kalite grubu, maddeler için ortak test gereksinimlerini temsil eder. Bu konu, otomatik oluşturma ve kalite emirleri oluşturmak üzere kalite ilişkilerine atanabilmeleri için ürünleri mantıksal olarak gruplamak üzere madde kalite gruplarının nasıl kullanılacağını açıklar.

Bir kalite grubuna atanmış maddeleri veya bir maddeye atanmış kalite gruplarını ayarlamak, düzenlemek ve görüntülemek için **Stok yönetimi \> Kurulum \> Kalite grupları**'na gidin. **Test grupları** sayfasındaki test gereksinimlerini tanımladıktan sonra, kalite emirlerini otomatik olarak oluşturmak için kurallar tanımlayabilirsiniz. İşlemi basitleştirmek için, kuralları her bir öğe için tanımlamanız gerekmez. Bunun yerine, **Kalite ilişkileri** sayfasında bir kalite grubu için kuralları tanımlayabilirsiniz.

## <a name="example-of-an-item-quality-group"></a>Bir madde kalite grubu örneği

Üretim şirketi, gelen denetim için aynı test gereksinimlerine sahip çeşitli hammaddeler satın alıyor. Bu nedenle, şirket bir kalite grubu tanımlar ve artından hammaddeler ile ilişkilendirilmiş olan madde numaralarını bu gruba atar. Daha sonra aynı sınama gereksinimleri olan yeni bir hammadde türü şirket tarafından satın alınır. Yeni malzeme için yeni test gereksinimleri ayarlamak yerine, şirket yeni malzeme için madde numarasını mevcut kalite grubuna ekler.

Aynı şirket, aynı üretim testi gereksinimlerine sahip maddeler de üretiyor ve ön sevkiyat testleri için aynı gereksinimlere sahip maddeleri sevk ediyor. Bu nedenle, şirket iki ek kalite grubu tanımlıyor ve sonra her gruba ilgili madde numaralarını atıyor.

## <a name="create-a-quality-group"></a>Kalite grubu oluşturun

Kalite grubu oluşturmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Kalite grupları** öğesine gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Kalite grubu** – kalite grubu için benzersiz bir kod ya da ad girin.
    - **Açıklama** – Kalite grubunun detaylı bir açıklamasını girin.

1. Sayfayı kapatın.

## <a name="manually-add-items-to-a-quality-group"></a>Kalite grubuna manuel olarak madde ekleme

Kalite grubuna manuel olarak madde eklemek için, aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Kalite grupları** öğesine gidin.
1. Madde eklemek istediğiniz kalite grubunu seçin.
1. Eylem Bölmesinde, **Maddeler**'i seçin.
1. **Kalite grubundaki maddeler** sayfasında, Eylem Bölmesi'nde, ızgaraya satır eklemek için **Yeni**'yi seçin. Yeni satır için **Madde numarası** alanını eklemek istediğiniz madde numarasına ayarlayın.
1. Eklenmesi gereken her ek öğe için önceki adımı tekrarlayın.
1. Sayfaları kapatın.

## <a name="add-multiple-items-to-a-quality-group"></a>Kalite grubuna birden fazla madde ekleme

Kalite grubuna birden fazla madde eklemek için, aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Kalite grupları** öğesine gidin.
1. Madde eklemek istediğiniz kalite grubunu oluşturun ya da seçin.
1. Eylem Bölmesinde, **Madde ekle**'yi seçin.
1. **Sorgulama** iletişim kutusunda, eklemek istediğiniz maddeler için filtre ölçütlerini girin. Örneğin, belirli bir madde grubundaki tüm maddeleri filtreleyebilirsiniz.
1. **Tamam**'ı seçin.
1. **Madde ekle** iletişim kutusunda, bir ızgara sorgunuzla eşleşen tüm öğeleri gösterir. Sonuçları inceleyin.

    Herhangi bir değişiklik yapılması gerekiyorsa, **Sorgulama** iletişim kutusuna dönmek ve sorgunuzu ayarlamak için **Seç**'i seçin.

1. Sonuçlar, eklemek istediğiniz tüm maddeleri kapsadığında, **Tamam**'ı seçin.
1. Sayfayı kapatın.

## <a name="manually-associate-an-item-with-a-quality-group"></a>Bir maddeyi bir kalite grubuyla manuel olarak ilişkilendirme

Bir maddeyi bir kalite grubuyla ilişkilendirmek için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Madde kalite grupları** öğesine gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Madde numarası** – Eklenecek madde numarasını seçin.
    - **Kalite grubu** – Maddeye atanacak kalite grubunu seçin.

1. Bir maddenin ve eklenmesi gereken kalite grubunun her ek birleşimi için önceki adımı tekrarlayın.
1. Sayfaları kapatın.

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>Serbest bırakılan ürünler sayfasından bir kalite grubunu el ile ekleme

**Serbest bırakılan ürünler** sayfasından bir kalite grubunu el ile eklemek için aşağıdaki adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Kalite grubu atamak istediğiniz ürünü seçin.
1. Eylem Bölmesinde, **Stok yönetimi** sekmesindeki **Kalite** grubunda **Madde kalite grupları**'nı seçin.
1. **Kalite grubundaki maddeler** sayfasında, Eylem Bölmesi'nde, ızgaraya satır eklemek için **Yeni**'yi seçin. Yeni satır için, **Kalite grubu** alanını ürüne atamak istediğiniz kalite grubuna ayarlayın.
1. Ürüne atamak istediğiniz her ek kalite grubu için önceki adımı yineleyin.
1. Sayfaları kapatın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimi test gereçleri](quality-test-instruments.md)
- [Kalite yönetimi testleri](quality-tests.md)
- [Kalite yönetimi test grupları](quality-test-groups.md)
- [Kalite yönetimi test değişkenleri](quality-test-variables.md)
- [Kalite ilişkileri](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
