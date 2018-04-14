---
title: "İş ürün demetindeki işlere zaman atama"
description: "İmalat yürütmede, işleri gruplayabilirsiniz. Ardından İş listesi sayfasında birden fazla işi aynı anda başlatabilirsiniz."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a5204288ce3eaabb605f136ea788d235f408f349
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>İş ürün demetindeki işlere zaman atama

[!INCLUDE [banner](../includes/banner.md)]

İmalat yürütmede, işleri gruplayabilirsiniz. Ardından İş listesi sayfasında birden fazla işi aynı anda başlatabilirsiniz.

İşleri gruplandırırsanız, tüm işler için toplam kayıt süresinin her bir iş için nasıl atanacağını tanımlamanız gerekir. Bu atamayı **Atama anahtarları** sayfasındaki **Grup türü** alanından aşağıdaki seçeneklerden birini seçerek tanımlarsınız:

-   **Tahmin** – Süre işler arasında, iş için tahmin edilen süreye dayalı olarak bölünür.
-   **İşler** – Süre, paketlenen toplam işe ve tüm işleri tamamlamak için ne kadar süre harcandığına göre bölünür.
-   **Net süre** – Süre, pakette bulunan işler arasında eşit şekilde bölünür.
-   **Gerçek zaman** – Gerçek iş süresi tahsis edilir. Maliyet, gerçek bordro maliyetine dayalı olarak hesaplanabilir. **Not:** **Gerçek zaman** atama anahtarı sadece bilgisayarınız Zaman ve katılım altında bordro işlevini kullanıyorsa geçerlidir.

Aşağıdaki örneklerde çeşitli atama anahtarlarının sonuçları gösterilmiştir.

## <a name="example-scenario"></a>Örnek senaryo
İş sıranızdaki üç işin mutlaka tamamlanması gerekir. İlk işi başlatırsınız ve ardından iş devam ederken ikinci ve üçüncü işleri başlatırsınız. Bu nedenle, üç işten meydana gelen bir grup bulunur. Aşağıdaki tabloda her bir iş için tahmini üretim süresini gösterilmiştir.

| İş   | Üretim süresi |
|-------|-----------------|
| İş 1 | 1 saat          |
| İş 2 | 3 saat         |
| İş 3 | 4 saat         |
| Toplam | 8 saat         |

Aşağıdaki tabloda her bir iş için harcanan gerçek çalışma süresi gösterilmiştir.

| İş    | Başlama zamanı | Bitiş saati | Paket saati |
|--------|------------|----------|-------------|
| İş 1  | 09:00      | 11:00    | 2 saat     |
| İş 2  | 10:00      | 13:00    | 3 saat     |
| İş 3  | 10:00      | 15:00    | 5 Saat     |
| Ürün demeti | 09:00      | 15:00    | 6 saat     |

Aşağıdaki bölümlerde her bir atama anahtarı için hesaplanan sürenin sonuçları açıklanmıştır.

## <a name="estimation-allocation-key"></a>Tahmin tahsisat anahtarı
Aşağıdaki tabloda atanan sürenin hesaplanması için kullanılan formül gösterilmiştir. Formül şu şekildedir: İş başına süre = Toplam grup süresi × (Tahmini iş süresi ÷ Tahmini toplam süre)

| İş   | Formül           | Tahsis edilen süre |
|-------|-------------------|----------------|
| İş 1 | 6 × (1 ÷ 8) saat | 0,75 saat      |
| İş 2 | 6 × (3 ÷ 8) saat | 2,25 saat     |
| İş 3 | 6 × (4 ÷ 8) saat | 3,00 saat     |

## <a name="jobs-allocation-key"></a>İş tahsisat anahtarı
Aşağıdaki tabloda atanan sürenin hesaplanması için kullanılan formül gösterilmiştir. Formül şu şekildedir: İş başına süre = Toplam grup süresi ÷ İş sayısı

| İş   | Formül | Tahsis edilen süre |
|-------|---------|----------------|
| İş 1 | 6 ÷ 3   | 2 saat        |
| İş 2 | 6 ÷ 3   | 2 saat        |
| İş 3 | 6 ÷ 3   | 2 saat        |

## <a name="net-time-allocation-key"></a>Net süre tahsisat anahtarı
Aşağıdaki tabloda atanan sürenin hesaplanması için kullanılan formül gösterilmiştir. Formül şu şekildedir: Raporlama başına hesaplanan süre = Grup süresi ÷ İş sayısı

|                              | 09:00–10:00 (1 saat) | 10:00–11:00 (1 saat) | 11:00–13:00 (2 saat) | 13:00–15:00 (2 saat) | Tahsis edilen süre |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Gruptaki iş sayısı | 1                    | 3                    | 2                     | 1                     | Geçerli değil |
| İş 1                        | 1 ÷ 1 = 1 saat       | 1 ÷ 3 = 0.33 saat    | Geçerli değil        | Geçerli değil        | 1,33 saat     |
| İş 2                        | Geçerli değil       | 1 ÷ 3 = 0.33 saat    | 2 ÷ 2 = 1 saat        | Geçerli değil        | 1,33 saat     |
| İş 3                        | Geçerli değil       | 1 ÷ 3 = 0.33 saat    | 2 ÷ 2 = 1 saat        | 2 ÷ 1 = 2 saat       | 3,33 saat     |

## <a name="real-time-allocation-key"></a>Gerçek zamanlı tahsisat anahtarı
Üretim maliyetlerinin gerçek maliyetlere dayalı olarak hesaplanmasını istiyorsanız, **Üretim emri varsayılan ayarları** sayfasındaki **Maliyet kategorisi** seçimini kaldırmanız gerekir. Aşağıdaki tabloda atanan sürenin hesaplanması için kullanılan formül gösterilmiştir. Formül şu şekildedir:İş başına gerçek süre = Gruptaki gerçek süre

| İş   | Gerçek zaman |
|-------|-------------|
| İş 1 | 2 saat     |
| İş 2 | 3 saat     |
| İş 3 | 5 Saat     |

Ortalama ücreti 12,00 USD olan bir çalışan tarafından üç iş gerçekleştirildiğini kabul edelim. İşlere harcanan süreler için fazla mesai veya prim kazanılmamıştır. Çalışan bu üç gruplandırılmış iş için toplam altı saat çalıştı. Bu nedenle, maaş maliyeti 6 × 12,00 USD = 72.00 USD olacaktır. Gerçek zamanlı atama kullanırsanız saat başına maliyet, Net zaman formülünden elde edilen faktör değeri kullanılarak yeniden hesaplanır. Her bir işe harcanan gerçek süre daha sonra saat başına düzeltilen maliyet fiyatıyla birlikte transfer edilir. Örnekte, altı saat harcanmıştır, ancak 10 saat atanmıştır. Aşağıdaki tabloda maliyetin hesaplanması için kullanılan formül gösterilmiştir. Formül şu şekildedir: Saat başına maliyet = (İş başına toplam grup süresi (Net süre) ÷ İş başına gerçek süre) × Saat başına standart maliyet fiyatı

| İş   | Saat başına düzeltilen maliyetin hesaplanması | Saat başına düzeltilen maliyet | Tahsis edilen süre | İşin toplam maliyeti |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| İş 1 | (1.33 ÷ 2) × 12.00 USD                 | 8.00 USD                | 2 saat        | 16.00 USD         |
| İş 2 | (1.33 ÷ 3) × 12.00 USD                 | 5.33 USD                | 3 saat        | 16.00 USD         |
| İş 3 | (3.33 ÷ 5) × 12.00 USD                 | 8.00 USD                | 5 Saat        | 40.00 USD         |

Saat başına düzeltilen maliyet ve iş süresi bir üretim günlüğüne nakledilir. **Not:** **Üretim emri varsayılan ayarları** sayfasındaki **Genel** sekmesinden **Maliyet kategorisi** seçimini yaparsanız her bir iş için gerçek süre bir üretim defterine transfer edilir ve burada maliyet, ilgili işin maliyet kategorisine uygulanır.




