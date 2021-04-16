---
title: Kiralama sonlandırma teklifi
description: Bu konu, sonlandırma için bir kiralama önermeyi açıklamaktadır.
author: moaamer
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e303821bd41751cb0a07442613b8b20e8061b052
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819878"
---
# <a name="propose-a-lease-for-termination"></a>Sonlandırma için kiralama önerme

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bir kiralama erken sonlandırıldıysa, Varlık kiralama, kiralama yükümlülüğünü, varlık kullanım hakkını (ROU) ve birikmiş amortismanı silebilir ve kazanç ya da kaybı deftere nakledebilir. Erken sonlandırma işlemi, bir kiralamayı ve onunla ilişkili kiralama rehberlerini sonlandırır. Kiralama rehberlerini tek tek sonlandırmaz. Bu konu, sonlandırma için kiralama önermeyi ve kiralama sonlandırma günlük girişini işlemeyi açıklamaktadır.

Kiralama, ertelenmiş kira tipi kiralama olarak sınıflandırılmamış ve bir sabit kıymetle ilişkili değilse Varlık kiralama aşağıdaki sonlandırma günlüğü girişini oluşturur.

| Hareket                           | Borç (Br.) | Alacak (Al.) |
|---------------------------------------|-------------|--------------|
| Br. Kiralama yükümlülüğü                   | X           |              |
| Br. Birikmiş amortisman          | X           |              |
| Br. Kiralama değişikliğinde kazanç (kayıp) | X           |              |
| Al. Kiralama kıymeti                       |             | X            |
| Al. Kiralama değişikliğinde kazanç (kayıp) |             | X            |

Kiralama rehberi ertelenmiş bir rehber olarak sınıflandırılabilir, burada gösterildiği gibi giriş, kazanç veya zarar hesabına sonlandırmadan önceki ertelenmiş gerçek bakiyesini siler.

| Hareket                           | Borç (Br.) | Alacak (Al.) | 
|---------------------------------------|-------------|--------------|
| Br. Ertelenmiş kira                     | X           |              |
| Al. Kiralama değişikliğinde kazanç (kayıp) |             | X            |
| Al. Ertelenmiş kira                     |             | X            |
| Br. Kiralama değişikliğinde kazanç (kayıp) | X           |              |

Kiralama rehberi bir sabit kıymete bağlıysa, sabit kıymetler için ROU varlığı hesaba katılmış olarak görüntülenir. Bu hesap, erken sonlandırmalar için hesaplama içerir. Varlık kiralama işlemi, kiralama yükümlülüğünü silmek için aşağıdaki günlük girişini üretir.

| Hareket                           | Borç (Br.) | Alacak (Al.) |
|---------------------------------------|-------------|--------------|
| Br. Kiralama yükümlülüğü                   | X           |              |
| Al. Kiralama değişikliğinde kazanç (kayıp) |             | X            |

Bir ROU varlığını atmanın doğru yolu hakkında bilgi için bkz. [Sabit kıymeti hurda olarak atma](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).

## <a name="propose-a-lease-for-termination"></a>Sonlandırma için kiralama önerme

1. Sonlandırılması gereken kiralamaya gidin ve sonra eylem bölmesinde **Sonlandırma teklifi**'ni seçin.

    > [!NOTE]
    > Herhangi bir rehberde deftere nakledilmemiş günlük girişi varsa, **Sonlandırılan teklifi** düğmesi kullanılamaz. Kiralamayı sona erdirmeden önce, kiralamaya karşı oluşturulan günlük girişlerini deftere nakletmeli veya silmelisiniz.

2. Görüntülenen iletişim kutusunda, sonlandırma günlüğü girişi için **Geçerlilik tarihi** ve **Deftere nakil tarihi** alanlarını ayarlayın.
3. Sonlandırma için kiralama önermek üzere **Sonlandırma teklifini** seçin.
4. Kiralama sonlandırma günlüğü girişini otomatik olarak deftere nakletmek için **Kiralama sonlandırmayı deftere naklet**'i seçin.
5. **Kiralama sonlandırmaları** sayfasında, kiralama satırlarını görüntülemek için sonlandırma için önerdiğiniz kiralamanın kimliğini seçin. Sonlandırma satırları, ROU varlığının değerlerini, kiralama yükümlülüğünü, birikmiş amortismanı, ertelenmiş kirayı (uygulanabiliyorsa) ve ve kiralama sonlandırıldığında tanınması gereken kazanç veya kaybı gösterir.

Kiralama artık sona erdirmeye hazırdır. Kira rehberinin **Sonlandırma durumu** alanının değeri, **Sonlandırma için hazır** olarak değiştirilir. Bu aşamada, artık kiralama karşılığında günlük girişlerini deftere nakledemezsiniz; aksi halde ayarlayıp bozabilirsiniz. 

## <a name="process-leases-that-are-ready-for-termination"></a>Sonlandırma için hazır olan kiralamaları işleme

Sonlandırmaya hazır olan kiralamaları işlemek ve sonlandırma günlüğü girişini deftere nakletmek için aşağıdaki adımları izleyin.

1. **Kiralama sonlandırmaları** sayfasında, işlenecek kiralamayı seçin ve ardından **Sonlandır**'ı seçin.
2. Görünen iletişim kutusunda **Tamam**'ı seçin.

Sistem, sonlandırma günlüğü girişini deftere nakleder. Kiralama rehberinin **Kiralama durumu** alanı, **Sonlandırıldı** olarak ayarlanır ve **Sonlandırma teklifi durumu** alanı **Tamamlandı** olarak ayarlanır.

## <a name="reverse-a-lease-termination"></a>Kiralama sonlandırmasını tersine çevirme

Kiralama sonlandırma günlüğünü ters kaydetmek ve sonlandırılan bir kiralamayı açmak için bu adımı izleyin.

- **Kiralama sonlandırmaları** sayfasında, ters kaydedilecek sonlandırılmış kiralamayı seçin ve ardından **Sonlandırmayı ters kaydet**'i seçin.

Sistem, sonlandırma günlüğü girişini ters kaydeder. Kiralama rehberinin **Kiralama durumu** alanı **Açık** olarak ayarlanır. Kiralama artık **Kira sonlandırmaları** sayfasında görünmez ve sonlandırma için tekrar teklif edilebilir.

## <a name="example-of-a-lease-termination"></a>Kiralama sonlandırması örneği

Bu örnekte kiralama, özelleştirilmemiş bir varlıkla ilişkilendirilmiştir ve varlığın sahipliğini aktarmaz veya kiracıya varlığı satın alma seçeneği sunmaz.

### <a name="setup"></a>Ayar

Aşağıdaki tablolarda, bu örnekte kullanılan kiralama için **Genel** ve **Ödeme planı satırları** sekmelerinde ayarlanan değerler gösterilir.

**Genel sekmesi**

| Alan                      | Değer            |
|----------------------------|------------------|
| Kıymetin adil değeri    | 600,000          |
| Para Birimi                   | ABD Doları              |
| Başlangıçtaki doğrudan maliyetler       | 1,000            |
| Alternatif borçlanma oranı | %7               |
| Bileşim aralığı       | Yıllık         |
| Varlık faydalı ömrü (ay) | 600              |
| Yıllık ödeme türü               | Normal yıllık ödeme |
| Başlangıç tarihi          | 01.01.2019         |

**Ödeme planı satırları sekmesi**

| Alan             | Değer      |
|-------------------|------------|
| Başlangıç tarihi        | 01.01.2019   |
| Dönem aralığı   | Monthly    |
| Dönemler           | 120        |
| Bitiş tarihi          | 31.12.2028 |
| Ödeme sıklığı | Yıllık   |
| Ödeme tutarı    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>Kiralamayı sona erdirme adımları

1. Bu konuda daha önce açıklandığı gibi kiralamayı oluşturduktan sonra, kiralama defterine gidin ve ödeme planını onaylayın. Ardından, ilk kabul günlüğü girişini deftere nakledin. İlk ROU varlığı 71.235,81 ABD dolarıdır ve kira yükümlülüğü 70.235,81 ABD doları olmalıdır. Bu örnekte kiralama, Muhasebe Standartları Kodlama Konusu 842 (ASC 842) kapsamında bir işletme kirası olarak sınıflandırılmıştır.
2. Kira ödemeleri, faiz giderleri ve amortisman giderleri için üç yılın geçtiği simülasyonunu oluşturmak için toplu iş günlük işlemeyi üç kez çalıştırın.
3. Üç toplu işin hepsini çalıştırdıktan sonra, kiralama defterine geri dönün ve ROU varlığı ile kiralama yükümlülüğünün geçerli defter değerini görüntülemek için Yükümlülük ve Varlık hareketleri tablolarını açın. Üç yıldan sonra, yükümlülüğün değeri yaklaşık -53.893,00 ABD doları, varlığın değeri yaklaşık 54.593,00 ABD doları olmalıdır.

    Üç yıl geçtikten sonra, işletme ve kiraya veren kirayı sonlandırmak için ortak karar almalıdır. Bu nedenle, artık kirayı sonlandırmanız gerekir.

4. Sonlandırılması gereken kiralamaya gidin ve sonra eylem bölmesinde **Sonlandırma teklifi**'ni seçin. 
5. **Geçerlilik tarihi** ve **Deftere nakil tarihi** alanında, görüntülenen iletişim kutusuna **1/1/2021** girin.
6. Sonlandırma için kiralama önermek üzere **Sonlandırma teklifini** seçin.

    **Kira sonlandırmaları** sayfası görüntülenir ve sonlandırılacak kirayı gösterir.

7. Sonlandırma satırlarını görüntülemek için sonlandırma için önerdiğiniz kiralamanın kiralama kimliğini seçin. Sonlandırma satırları kiralamanın taşıma değerlerini gösterir. Aşağıdaki tabloda bu değerlerin bu örnekte ne olması gerektiği gösterilir. 

    | Alan                                                 | Değer      |
    |-------------------------------------------------------|------------|
    | Hareket para birimi cinsinden yükümlülüğün taşıma bakiyesi | 53.892,89 ABD doları |
    | Hareket para birimi cinsinden kullanım hakkı varlığı            | 71.235,81 ABD doları |
    | Hareket para birimi cinsinden birikmiş amortisman      | 16.642,92 ABD doları |
    | Hareket para birimi cinsinden kazanç (kayıp)                   | -700,00 ABD doları   |

8. Sonlandırma günlüğü girişini deftere nakletmek için **Kiralama sonlandırmaları** sayfasında, kiralamayı seçin ve ardından **Sonlandır**'ı seçin.
9. Görünen iletişim kutusunda **Tamam**'ı seçin.
10. Oluşturulan ve deftere nakledilen sonlandırma günlüğü girişini görüntülemek için kıymetin kira defterindeki Kiralama günlüğüne gidin. Aşağıdaki tabloda bu değerin bu örnekte ne olması gerektiği gösterilir.

    | Hareket                           | Borç (Br.) | Alacak (Al.) |
    |---------------------------------------|-------------|--------------|
    | Br. Kiralama yükümlülüğü                   | 53,892.89   |              |
    | Br. Birikmiş amortisman          | 16,642.92   |              |
    | Br. Kiralama değişikliğinde kazanç (kayıp) | 700.00      |              |
    | Al. Kiralama kıymeti                       |             | 71,235.81    |

11. ROU varlığının ve kiralama yükümlülüğünün 0 (sıfır) olacağı sonlandırma işleminin net etkisini görüntülemek için Borç ve Varlık hareketleri tablolarını açın.

Şimdi kiralama durumu **Sonlandırıldı** olmalıdır. Sonlandırma ters çevrilmediği sürece, bu kiralamaya karşı hiçbir ek günlük girişi deftere nakledilemez.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]