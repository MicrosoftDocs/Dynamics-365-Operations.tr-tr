---
title: Kalite yönetimi test değişkenleri
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle niteliksel testlerin kullanılabilmesi için, test değişkenlerinin nasıl oluşturulacağını açıklar.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8233864d6b668c8462a59a425e66b1aec38576633922062573d8605c9c73d2a8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734223"
---
# <a name="quality-management-test-variables"></a>Kalite yönetimi test değişkenleri

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle niteliksel testlerin kullanılabilmesi için, test değişkenlerinin nasıl oluşturulacağını açıklar.

**Testler** sayfasında tanımlanan her niteliksel test için bir test değişkeni ve bu değişkenin olası çıktılarını (sonuçlar) tanımlamalısınız. (Niteliksel testler için, **Testler** sayfası üzerinde **Tür** alanı *Seçenek* olarak ayarlanmıştır.)

Bir niteliksel testle ilişkili bir test değişkenine ait olası sonuçları ayarlamak, düzenlemek ve görüntülemek için **Test değişkenleri** sayfasını kullanın. Her bir sonuç için, test sonucu olarak bu sonucun seçildiği durumda testin başarılı veya başarısız olduğunu belirtmek için *Başarılı* veya *Başarısız* seçeneklerinden birini sonuç durumu olarak atarsınız. **Test grupları** sayfasını kullanarak bir test değişkenini ve test değişkeninin varsayılan sonucunu bir niteliksel teste atayabilirsiniz.

Her test değişkeni için en az iki sonuç tanımlamanız önerilir: bu sonuçlardan birinin sonuç durumu *Başarılı* ve diğeri ise *Başarısız* olmalıdır. Tanımlanabilecek değişkenlerin veya sonuç sayısının bir limiti yoktur. Ek olarak, birden fazla test, sonuçları kaydetmek için aynı test değişkenlerini kullanabilir.

## <a name="examples-of-test-variables"></a>Test değişkenlerine örnekler

### <a name="example-1"></a>Örnek 1

Bir üretim şirketi, üretilen malzemeler üzerinde iki test yapar. Bir testte, pH düzeyi bir renk şeridiyle ilişkilendirilmiştir. Kabul edilebilir pH düzeyleri daha açık renklerde ve kabul edilemez pH düzeyleri daha koyu renklerdedir. Başka bir testte, birden çok görsel inceleme gerçekleştirilir ve kalite çalışanları, görsel incelemeden geçen maddelerin hatalı olup olmadığını belirlemek için kendi yargılarını kullanır.

### <a name="example-2"></a>Örnek 2

Kurabiye üreten bir üretim şirketi, tamamlanan ürüne yönelik bir denetim testi uyguluyor. Bu inceleme testinin birçok değişkeni vardır. Bir değişken lezzettir ve bu değişkenin olası sonuçları iyi veya kötü olabilir. İkinci bir değişken, çok koyu, çok açık ve doğru sonuçları ile temsil edilen renk değişkeni oluyor.

## <a name="create-a-test-variable"></a>Yeni bir test değişkeni oluşturma

Test değişkeni oluşturmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Test değişkenleri** öğesine gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Değişken** – Değişken için benzersiz bir kod ya da ad girin.
    - **Açıklama**: – Değişkenin detaylı bir açıklamasını girin.

1. Yeni satır seçiliyken, Eylem Bölmesinde **Sonuçlar**'ı seçin.
1. **Test değişkeni sonuçları** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Sonuç** – Sonuç için benzersiz bir kod ya da ad girin.
    - **Açıklama**: – Sonucun detaylı bir açıklamasını girin.
    - **Sonuç durumu** – Her bir sonuç için, test sonucu olarak sonucun seçildiği durumda testin başarılı veya başarısız olduğunu belirtmek için *Başarılı* veya *Başarısız* seçeneklerinden birini sonuç durumu olarak atarsınız.

1. Her bir ek sonuç için önceki adımı tekrarlayın. En az bir sonucun *Başarılı* sonuç durumuna sahip olduğundan ve en azından bir sonucun *Başarısız* sonuç durumuna sahip olduğundan emin olun.
1. Sayfaları kapatın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimi test gereçleri](quality-test-instruments.md)
- [Kalite yönetimi testleri](quality-tests.md)
- [Kalite yönetimi test grupları](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
