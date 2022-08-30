---
title: Tahmin azaltma anahtarları
description: Bu makalede bir azaltma anahtarının nasıl ayarlanacağını gösteren örnekler verilmiştir. Çeşitli azaltma anahtarı ayarları ve her birinin sonuçları hakkında da bilgiler içerir. Bir zzaltma anahtarını, tahmin gereksinimlerinin nasıl azaltılacağını tanımlamak için kullanabilirsiniz.
author: t-benebo
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqReduceKeyDefaultDataWizard, ReqReduceKey
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7eaf57e0f02c0b9dd6454a58184db7bb3f58c04
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337155"
---
# <a name="forecast-reduction-keys"></a>Tahmin azaltma anahtarları

[!include [banner](../includes/banner.md)]

Bu makale, tahmin gereksinimlerini azaltmak için kullanılan farklı yöntemleri hakkında bilgi sağlar. Her yöntemin sonuçlarının örneklerini içerir. Bu aynı zamanda tahmin azaltma anahtarı kullan oluşturmak ve ayarlamayı açıklar. Bazı yöntemler, bir azaltma anahtarını, tahmin gereksinimlerini azaltmak için kullanır.

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Tahmin gereksinimlerini azaltmak için kullanılan yöntemler

Bir tahmini bir master planlama içine dahil ettiğinizde, fiili talep dahil edildiğinde tahmin taleplerinin nasıl azaltıldığını seçebilirsiniz. Master planlamanın, bugünün tarihinden önceki tüm tahmin gereksinimleri anlamına gelen, geçmişte yapılan tahmin gereksinimlerini hariç tuttuğunu unutmayın.

Bir tahmini bir master planlamaya dahil etmek ve tahmin gereksinimlerini azaltmakta kullanılan yöntemi seçmek iin **Master planlama \> Kurulum \> Planlar \> Master planlar**'a gidin. **Tahmin modeli** alanında bir tahmin modeli seçin. **Tahmin gereksinimlerini azaltmakta kullanılan yöntem** alanında bir yöntem seçin. Aşağıdaki seçenekler bulunur:

- Hiçbiri
- Yüzde - azaltma anahtarı
- Hareketler - azaltma anahtarı
- Hareketler - dinamik dönem

Aşağıdaki bölümler her seçenek hakkında daha fazla bilgi sağlar.

### <a name="none"></a>Hiçbiri

**Hiçbiri**'ni seçerseniz, tahmin talepleri master planlama sırasında azaltılmaz. Bu durumda, master planlama planlanan siparişleri, tahmin edilen talebi (tahmin gereksinimleri) sağlamak için oluşturur. Bu planlı siparişler, önerilen miktarı tutar, diğer talep türlerinden bağımsız olarak. Örneğin, satış siparişleri verilirse, master planlama, satış siparişlerini desteklemek için ek planlanan siparişler oluşturur. Tahmin gereksiniminin miktarı azaltılmaz.

### <a name="percent--reduction-key"></a>Yüzde - azaltma anahtarı

**Yüzde - azaltma anahtarını seçerseniz**, tahmin gereksinimleri azaltma anahtarı tarafından tanımlanan yüzdelere ve dönemlere göre azaltılır. Bu durumda, master planlama, miktarın tahmin edilen miktar × azaltma anahtarı olarak her dönemde hesaplandığı planlanan siparişleri oluşturur. Başka türde talep varsa, master planlama bu talebi de karşılamak için planlanan siparişleri oluşturur.

#### <a name="example-percent--reduction-key"></a>Örnek : Yüzde - azaltma anahtarı

Bu örnek bir azaltma anahtarının, talep tahmini gereksinimlerini azaltma anahtarı tarafından tanımlanan yüzdelere ve dönemlere göre nasıl azalttığını gösterir.

Bu örnek için aşağıdaki talep tahminini bir master planlamaya dahil edebilirsiniz.

| Ay    | Talep tahmini |
|----------|-----------------|
| Ocak  | 1,000           |
| Şubat | 1,000           |
| Mart    | 1,000           |
| Nisan    | 1,000           |

**Azaltma anahtarları** sayfasında aşağıdaki satırları ayarlayın.

| Değiştirme | Birim  | Yüzde |
|--------|-------|---------|
| 1      | Ay | 100     |
| 2      | Ay | 75      |
| 3      | Ay | 50      |
| 4      | Ay | 25      |

Azaltma anahtarını ürünün kapsam grubuna atayın. Sonra, **Master planlar** sayfasında, **Tahmin gereksinimlerini azaltmak** alanında, **Yüzde - azaltma anahtarı**'nı seçin.

Bu durumda, tahmin planını 1 Ocak'ta çalıştırırsanız, talep tahmini gereksinimleri **Azaltma anahtarları** sayfasında ayarladığınız yüzdelere göre tüketilir. Aşağıdaki gereksinim miktarları ana plana transfer edilir.

| Ay                | Planlanan sipariş miktarı | Hesaplama    |
|----------------------|------------------------|----------------|
| Ocak              | 0                      | = %0 × 1.000   |
| Şubat             | 250                    | = %25 × 1.000  |
| Mart                | 500                    | = %50 × 1.000  |
| Nisan                | 750                    | = %75 × 1.000  |
| Mayıs - Aralık arası | 1,000                  | = %100 × 1.000 |

### <a name="transactions--reduction-key"></a>Hareketler - azaltma anahtarı

**Tahmin gereksinimlerini azaltmak için kullanılan yöntem** alanını *Hareketler: azaltma anahtarı* olarak ayarlarsanız azaltma anahtarı ile tanımlanan dönemlerde gerçekleşen donanımlı talep hareketleri ile tahmin gereksinimleri azaltılır.

Uygun bulunan talep, **Karşılama grupları** sayfasındaki **Tahmin azaltma ölçütü** alanıyla tanımlanır. **Tahmin azaltma ölçütü** alanını *Siparişler* olarak ayarlarsanız yalnızca satış siparişi hareketleri uygun bulunan talep olarak kabul edilir. *Tüm hareketler* olarak ayarlarsanız tüm şirketlerarası olmayan çıkış stok hareketleri uygun bulunan talep olarak kabul edilir. Şirketlerarası satış siparişlerinin de uygun bulunan talep olarak değerlendirilmesi gerekiyorsa **Şirketlerarası siparişleri dahil et** seçeneğini *Evet* olarak ayarlayın.

Tahmin azaltma, azaltma anahtarı dönemindeki ilk (en erken) talep tahmini kaydıyla başlar. Donanımlı stok hareketlerinin miktarı, aynı azaltma anahtarı dönemindeki talep tahmin satırlarının miktarından fazlaysa stok hareketlerinin bakiyesi önceki dönemdeki talep tahmin miktarını (tüketilmemiş tahmin varsa) azaltmak için kullanılır.

Önceki azaltma anahtarı döneminde tüketilmeyen tahmin kalmamışsa bir sonraki aydaki tahmin miktarını azaltmak için stok hareketleri bakiyesi (tüketilmemiş tahmin varsa) kullanılır.

Azaltma anahtarı satırlarındaki **Yüzde** alanının değeri, **Tahmin gereksinimlerini azaltmak için kullanılan yöntem** alanı *Hareketler: azaltma anahtarı* olarak ayarlandığında kullanılmaz. Azaltma anahtarı dönemini tanımlamak için yalnızca tarihler kullanılır.

> [!NOTE]
> Bugünün tarihinde veya öncesinde yayımlanan herhangi bir tahmin yok sayılır ve planlı siparişler oluşturmak için kullanılmaz. Örneğin, ay için talep tahmininiz 1 Ocak'ta oluşturulur ve 2 Ocak'ta talep tahminini içeren master planlamayı çalıştırırsanız hesaplama 1 Ocak tarihli talep tahmini satırını yoksayar.

#### <a name="example-transactions--reduction-key"></a>Örnek: Hareketler - azaltma anahtarı

Bu örnek, azaltma anahtarı tarafından tanımlanan dönemler boyunca gerçekleşen fiili siparişlerin talep tahmini gereksinimlerini nasıl azalttığını gösterir.

Bu örnek için **Hareketler - azaltma anahtarı**'nı **Tahmin gereksinimlerini azaltma yöntemi** alanında, **Master planlamalar** sayfasında seçin.

Aşağıdaki satış siparişleri 1 Ocak'tadır.

| Ay    | Gerekli parça sayısı |
|----------|--------------------------|
| Ocak  | 956                      |
| Şubat | 1.176                    |
| Mart    | 451                      |
| Nisan    | 119                      |

Önceki örnekte kullanılan aylık 1.000 parçalık aynı talep tahminini kullanıyorsanız, aşağıdaki gereksinim miktarları ana planlamaya aktarılır.

| Ay                | Gerekli parça sayısı |
|----------------------|---------------------------|
| Ocak              | 44                        |
| Şubat             | 0                         |
| Mart                | 549                       |
| Nisan                | 881                       |
| Mayıs - Aralık arası | 1,000                     |

### <a name="transactions--dynamic-period"></a>Hareketler - dinamik dönem

**Hareketler - dinamik dönem**'i seçerseniz, tahmin gereksinimleri, dinamik dönemde gerçekleşen fiili sipariş hareketleri kadar azaltılır. Dinamik dönem, geçerli tahmin tarihlerini kapsar ve bir sonraki tahmin başlangıcında sona erer. Bu durumda, master planlama planlanan siparişleri, tahmin edilen talebi (tahmin gereksinimleri) sağlamak için oluşturur. Ancak, gerçek sipariş hareketleri yerleştirildiğinde, tahmin gereksinimleri azaltılır. Gerçek hareketler tahmin edilen gereksinimlerin bir kısmını tüketir.

Bu seçenek kullanıldığında, aşağıdaki davranış ortaya çıkar:

- Azaltma anahtarları gerekli değildir veya kullanılmaz. 
- Tahmin tümüyle azaltıldıysa, geçerli tahminin tahmin gereksinimleri 0 (sıfır) olur.
- Gelecekte başka bir tahmin yoksa, girilen son tahmindeki tahmin gereksinimleri azaltılır.
- Talep tahmini azaltma zaman aralığı tahmin azaltma hesaplamasına dahil edilmez. Bunun yerine, tahmin azaltma için karşılama grubu zaman aralığı kullanılır.
- Artı günler, tahmin azaltma hesaplamasına eklenir.
- Fiili sipariş hareketlerinin tahmin gereksinimlerini aşması durumunda, kalan hareketler sonraki tahmin dönemine iletilmez.

#### <a name="example-1-transactions--dynamic-period"></a>Örnek 1: Hareketler - dinamik dönem

Burada **Hareketler - dinamik dönem** yönteminin asıl çalıştığını gösteren basit bir örnek vardır.

Bu örnek için aşağıdaki talep tahminini bir master planlamaya dahil edebilirsiniz.

| Tarih       | Talep tahmini |
|------------|-----------------|
| 1 Ocak  | 1,000           |
| Şubat 1 | 1,000             |

Aşağıdaki satış siparişlerini de oluşturabilirsiniz.

| Tarih        | Satış siparişi miktarı |
|-------------|----------------------|
| 15 Ocak  | 200                  |
| Şubat 15 | 400                  |

Bu durumda, aşağıdaki planlı siparişleri oluşturulur.

| Talep tahmini tarihi | Miktar | Açıklama                           |
|--------------------- |----------|---------------------------------------|
| 1 Ocak            | 800      | Tahmin gereksinimleri (= 1.000 – 200) |
| 15 Ocak           | 200      | Satış siparişi gereksinimleri             |
| Şubat 1           | 600      | Tahmin gereksinimleri (= 1.000 – 400) |
| Şubat 15          | 400      | Satış siparişi gereksinimleri             |

#### <a name="example-2-transactions--dynamic-period"></a>Örnek 2: Hareketler - dinamik dönem

Çoğu durumda, hareketlerin haftalık, aylık ve benzeri tahmin dönemlerinde talep tahminini azaltabilmesi için sistemler ayarlanır. Bu dönemler azaltma anahtarında tanımlanır. Ancak, iki tahmin satırı arasındaki süre bir dönemi *gösterebilir*.

Bu örnekte, aşağıdaki tarihler ve miktarlar için bir talep tahmin oluşturursunuz.

| Tarih       | Talep tahmini |
|------------|-----------------|
| 1 Ocak  | 1,000           |
| 5 Ocak  | 500             |
| 12 Ocak | 1,000           |

Bu tahminde, tahmin tarihleri arasında net bir dönem olmadığına dikkat edin. İlk ve ikinci tarihler arasında dört günlük bir aralık vardır ve ikinci ve üçüncü tarihler arasında yedi günlük bir aralık vardır. Bu aralıklar dinamik dönemdir.

Aşağıdaki satış siparişi satırlarını da oluşturabilirsiniz.

| Tarih                             | Satış siparişi miktarı |
|----------------------------------|----------------------|
| Önceki yılın 15 Aralık tarihi | 500                  |
| 3 Ocak                        | 100                  |
| 10 Ocak                       | 200                  |

Bu durumda, tahmin aşağıdaki şekilde azaltılır:

- İlk satış siparişi herhangi bir dönemde olmadığı için herhangi bir tahmini azaltmaz.
- İkinci satış siparişi 1 Ocak ve 5 Ocak arasında olduğu için 1 Ocak için olan tahmini 100 azaltır.
- Üçüncü satış siparişi 5 Ocak ve 12 Ocak arasında olduğu için 5 Ocak için olan tahmini 200 azaltır.

Bu nedenle, aşağıdaki planlı siparişleri oluşturulur.

| Talep tahmini tarihi             | Miktar | Açıklama                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| Önceki yılın 15 Aralık tarihi | 500      | Satış sipariş gereksinimleri                                            |
| 1 Ocak                        | 900      | Tahmin gereksinimleri dönemi 1 Ocak - 5 Ocak (= 1.000 - 100) |
| 3 Ocak                        | 100      | Satış sipariş gereksinimleri                                            |
| 5 Ocak                        | 300      | Tahmin gereksinimleri dönemi 5 Ocak - 10 Ocak (= 500 - 200)  |
| 12 Ocak                       | 1,000    | Tahmin gereksinimleri dönemi Ocak 12'den sona kadar                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a>Bir tahmin azaltma anahtarı oluşturun ve ayarlayın

Bir tahmin azaltma anahtarı **Hareketler - azaltma anahtarı** ve **Yüzde - azaltma anahtarı** yöntemlerinde tahmin gereksinimlerini azaltmak için kullanılır. Bir azaltma anahtarı oluşturmak ve ayarlamak için bu adımları izleyin.

1. **Master planlama \> Kurulum \> kapsam \> Azaltma anahtarları**'na gidin.
2. Yeni bir azaltma anahtarı oluşturmak için **Yeni**'yi seçin.
3. **Azaltma anahtarı** alanında, tahmin edilen azaltma anahtarı için benzersiz bir tanımlayıcı girin. Daha sonra **Adı** alanında, bir ad girin. 
4. Her bir dönemdeki dönemleri ve azaltma anahtarı yüzdesini tanımlayın:

    - **Efektif tarih** alanı, dönem başlangıçlarının oluşturulma tarihlerini belirtir. **Efektif tarihi kullan** seçeneği **Evet** olarak ayarlandığında, dönemler efektif tarihte başlar. **Hayır** olarak ayarlandığında, dönemler master planlamanın çalıştırıldığı tarihlerde başlar.
    - Tahmin azaltmanın gerçekleşeceği dönemleri tanımlayın.
    - Belirli bir dönem için tahmin gereksinimlerinin azaltılacağı yüzdeleri belirtin. Gereksinimlerini azaltmak için artı değerler ya da gereksinimleri artırmak için eksi değerler girebilirsiniz.

## <a name="use-a-reduction-key"></a>Bir azaltma anahtarı kullanın

Bir tahmin azaltma anahtarının, öğenin kapsama grubuna atanmış olması gerekir. Bir öğenin kapsama grubuna bir azaltma anahtarı atamak için şu adımları izleyin.

1. **Master planlama \> Kurulum \> Kapsam \> Kapsam grupları**'na gidin.
2. **Diğer** hızlı sekmesinde, **Azaltma anahtarı** alanında, kapsama grubunu atamak için azaltma anahtarını seçin. Azaltma anahtarı, daha sonra bu kapsama grubuna ait tüm öğelere uygulanır.
3. Master planlama sırasında tahmin azaltmayı hesaplamak için bir azaltma anahtarını kullanmak için bu ayarı, tahmin planlama veya master planlama kurulumunda tanımlamanız gerekir. Aşağıdaki konumlarda birine gidin:

    - Master planlama \> Kurulum \> Planlar \> Tahmin planları
    - Master planlama \> Ayar \> Planlar \> Master planlar

4. **Tahmin planları** veya **Master planlar** sayfasında, **Genel** hızlı sekmesinde, **Tahmin gereksinimlerini azaltmak için yöntem** alanında, **Yüzde - azaltma anahtarı** veya **Hareketler - azaltma anahtarı**'nı seçin.

## <a name="reduce-a-forecast-by-transactions"></a>Bir tahmini hareketler ile azaltın

**Hareketler - azaltma anahtarı**'nı veya **Hareketler - dinamik dönem**'i tahmin gereksinimlerini azaltmak için bir yöntem olarak seçerseniz, hangi hareketlerin tahmini azaltacağını seçersiniz. **Karşılama grupları** sayfasında, **Diğer** Hızlı Sekmesinde, **Tahmini şunun üzerinden azalt** alanında, tüm hareketler tahmini azaltacaksa **Tüm tahminler**'i seçin veya yalnızca satış siparişleri tahmini azaltacaksa **Siparişler**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Master planlara genel bakış](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
