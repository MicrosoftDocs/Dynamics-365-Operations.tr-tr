---
title: Talep tahminleri ile master planlama
description: Bu konu, Planlama İyileştirmesi ile master planlama sırasında talep tahminlerinin nasıl ekleneceğini açıklamaktadır.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup, ReqReduceKey, ForecastModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 88e93e7a363bf5db3d25d7fe6a0ab390f79912b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833317"
---
# <a name="master-planning-with-demand-forecasts"></a>Talep tahminleri ile master planlama

[!include [banner](../../includes/banner.md)]

Master planlamanızda beklenen talebi dikkate almak için Planlama İyileştirmesi ile birlikte bir talep tahmini kullanabilirsiniz. El ile bir talep tahmini oluşturabilir, içeri aktarabilir veya Microsoft Dynamics 365 Supply Chain Management'ın talep tahmini işlevini kullanarak bunu oluşturabilirsiniz. Talep tahmini hakkında daha fazla bilgi için bkz. [Talep tahminine genel bakış](../introduction-demand-forecasting.md).

> [!NOTE]
> Planlama İyileştirmesi ile ayrı tahmin planlama desteklenmez. Bu nedenle, Planlama İyileştirmesi'ni kullandığınızda **Master planlama parametreleri** sayfasındaki **Geçerli tahmin planı** ayarının hiçbir etkisi olmayacaktır.

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a>Bir talep tahminini dahil etmek için bir master plan ayarlama

Master planınızı bir talep tahmini içerecek şekilde yapılandırmak için bu adımları izleyin.

1. **Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Var olan bir planı seçin veya yeni bir plan oluşturun.
1. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Tahmin modeli**: Uygulanacak tahmin modelini seçin. Geçerli master plan için bir tedarik önerisi oluşturulduğunda, bu model dikkate alınır.
    - **Talep tahminini dahil et**: Geçerli master plana talep tahmini eklemek için bu seçeneği *Evet* olarak ayarlayın. *Hayır* olarak ayarlarsanız talep tahmini hareketleri master plana dahil edilmeyecektir.
    - **Tahmin gereksinimlerini azaltmak için kullanılan yöntem**: Tahmin gereksinimlerini azaltmak için kullanılacak yöntemi seçin. Daha fazla bilgi için bu konuda ileride yer alan [Tahmin azaltma anahtarları](#reduction-keys) bölümüne bakın.

1. **Gün cinsinden zaman dilimi** hızlı sekmesinde, talep tahmininin dahil edildiği dönemi belirtmek için aşağıdaki alanları ayarlayabilirsiniz:

    - **Tahmin planı**: Ayrı kapsam gruplarından kaynaklanan tahmin planı zaman dilimini geçersiz kılmak için bu seçeneği *Evet* olarak ayarlayın. Geçerli master plan için ayrı kapsam gruplarındaki değerleri kullanmak için *Hayır* olarak ayarlayın.
    - **Tahmin zaman dönemi**: **Tahmin planı** seçeneğini *Evet* olarak ayarlarsanız, talep tahmininin uygulanması gereken gün sayısını (bugünün tarihinden itibaren) belirtin.

    > [!IMPORTANT]
    > **Tahmin planı** ayarı, Planlama İyileştirmesi'nde henüz desteklenmemektedir.

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a>Bir talep tahminini dahil etmek için bir kapsama grubu ayarlama

Kapsam grubunuzu bir talep tahmini içerecek şekilde yapılandırmak için bu adımları izleyin.

1. **Master planlama \> Kurulum \> Planlar \> Kapsam grupları**'na gidin.
1. Mevcut bir kapsam grubu seçin veya yeni bir grup oluşturun.
1. **Diğer** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Tahmin planı zaman dilimi**: Talep tahmininin uygulanması gereken gün sayısını (bugünün tarihinden itibaren) girin. Bu değer, önceki bölümde açıklandığı gibi, master plan üzerindeki **Tahmin planı** seçeneği kullanılarak geçersiz kılınabilir.
    - **Azaltma anahtarı**: Uygulanacak azaltma anahtarını seçin. Daha fazla bilgi için bkz. [Tahmin azaltma anahtarı oluşturma ve ayarlama](#create-reduction-key) ve bu konunun ilerleyen kısımlarındaki [Azaltma anahtarı kullanma](#use-reduction-key).
    - **Tahmin azaltma ölçütü**: **Tahmin gereksinimlerini azaltmak için kullanılan yöntem** alanının *Hareketler - azaltma anahtarı* veya *Hareketler - dinamik dönem* olarak ayarlandığı master planlar için hangi hareketlerin tahmini azaltılacağını belirtin. Aşağıdaki değerlerden birini seçin:

        - **Tüm hareketler**: Tüm hareketler tahmini azaltır.
        - **Siparişler**: Yalnızca satış siparişleri tahmini azaltır.

        > [!NOTE]
        > *Tüm hareketler*'i seçerseniz aynı stok boyutlarında hem talep hem de tedarik içeren hareketler nötr kabul edilir ve tahmin azaltma sırasında yoksayılır. Örneğin, planlama boyutu ambar olarak değil, yalnızca tesis olarak ayarlanmışsa tesis 1, ambar 11 ile tesis 1 ambar 13 arasındaki bir transfer emri yoksayılır ve kalan talep tahminini azaltmaz.

    - **Şirketlerarası siparişleri dahil et**: Tahmin azaldığında şirketlerarası siparişlerin dahil edilmesi gerekiyorsa bu seçeneği *Evet* olarak ayarlayın. Aksi durumda *Hayır* olarak ayarlayın.
    - **Talep tahminine müşteri tahminini dahil et**: Bir müşteri tahmininin genel tahmine dahil edilip edilmeyeceğini belirtin. Bu seçenek, gerçek talebin tahmin edilen talebi nasıl azaltacağına karar verir. Master planlamanın belirli müşteriler tarafından satın alınan maddelerin tedariğini kapsadığından emin olmak için bunu kullanabilirsiniz.

        - Genel tahmine müşteri tahminini eklemek için bu seçeneği *Evet* olarak ayarlayın. Bu durumda, gerçek müşteri talebi hem müşteri tahminini hem de genel tahmini azaltır. Master planlama yalnızca genel tahmin miktarını kapsayacak şekilde planlı siparişler oluşturur.
        - Genel tahmine müşteri tahminini eklemek istemiyorsanız bu seçeneği *Hayır* olarak ayarlayın. Bu durumda, gerçek müşteri talebi yalnızca müşteri tahminini azaltır. Master planlama, genel tahmin miktarını ve her müşteri miktarı için tahmini kapsamak üzere planlı siparişler oluşturur.

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a>Tahmin azaltma anahtarları

Bu bölüm, tahmin gereksinimlerini azaltmak için kullanılan farklı yöntemleri hakkında bilgi sağlar. Her yöntemin sonuçlarının örneklerini içerir. Bu aynı zamanda tahmin azaltma anahtarı kullan oluşturmak ve ayarlamayı açıklar. Bazı yöntemler, bir azaltma anahtarını, tahmin gereksinimlerini azaltmak için kullanır.

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Tahmin gereksinimlerini azaltmak için kullanılan yöntemler

Bir tahmini bir master planlama içine dahil ettiğinizde, fiili talep dahil edildiğinde tahmin taleplerinin nasıl azaltıldığını seçebilirsiniz. Master planlamanın, bugünün tarihinden önceki tüm tahmin gereksinimleri anlamına gelen, geçmişte yapılan tahmin gereksinimlerini hariç tuttuğunu unutmayın.

Bir tahmini bir master planlamaya dahil etmek ve tahmin gereksinimlerini azaltmakta kullanılan yöntemi seçmek iin **Master planlama \> Kurulum \> Planlar \> Master planlar**'a gidin. **Tahmin modeli** alanında bir tahmin modeli seçin. **Tahmin gereksinimlerini azaltmakta kullanılan yöntem** alanında bir yöntem seçin. Aşağıdaki seçenekler bulunur:

- Hiçbiri
- Yüzde - azaltma anahtarı
- Hareketler - azaltma anahtarı (Planlama İyileştirmesi ile henüz desteklenmiyor)
- Hareketler - dinamik dönem

Aşağıdaki bölümler her seçenek hakkında daha fazla bilgi sağlar.

#### <a name="none"></a>Hiçbiri

**Hiçbiri**'ni seçerseniz, tahmin talepleri master planlama sırasında azaltılmaz. Bu durumda, master planlama planlanan siparişleri, tahmin edilen talebi (tahmin gereksinimleri) sağlamak için oluşturur. Bu planlı siparişler, önerilen miktarı tutar, diğer talep türlerinden bağımsız olarak. Örneğin, satış siparişleri verilirse, master planlama, satış siparişlerini desteklemek için ek planlanan siparişler oluşturur. Tahmin gereksiniminin miktarı azaltılmaz.

#### <a name="percent--reduction-key"></a>Yüzde - azaltma anahtarı

**Yüzde - azaltma anahtarını seçerseniz**, tahmin gereksinimleri azaltma anahtarı tarafından tanımlanan yüzdelere ve dönemlere göre azaltılır. Bu durumda, master planlama, miktarın tahmin edilen miktar × azaltma anahtarı olarak her dönemde hesaplandığı planlanan siparişleri oluşturur. Başka türde talep varsa, master planlama bu talebi de karşılamak için planlanan siparişleri oluşturur.

##### <a name="example-percent--reduction-key"></a>Örnek : Yüzde - azaltma anahtarı

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

#### <a name="transactions--reduction-key"></a>Hareketler - azaltma anahtarı

**Hareketler - azaltma anahtarını** seçerseniz: Tahmin gereksinimleri azaltma anahtarı tarafından tanımlanan meydana gelen hareketlere göre azaltılır.

##### <a name="example-transactions--reduction-key"></a>Örnek: Hareketler - azaltma anahtarı

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

#### <a name="transactions--dynamic-period"></a>Hareketler - dinamik dönem

**Hareketler - dinamik dönem**'i seçerseniz, tahmin gereksinimleri, dinamik dönemde gerçekleşen fiili sipariş hareketleri kadar azaltılır. Dinamik dönem, geçerli tahmin tarihlerini kapsar ve bir sonraki tahmin başlangıcında sona erer. Bu durumda, master planlama planlanan siparişleri, tahmin edilen talebi (tahmin gereksinimleri) sağlamak için oluşturur. Ancak, gerçek sipariş hareketleri yerleştirildiğinde, tahmin gereksinimleri azaltılır. Gerçek hareketler tahmin edilen gereksinimlerin bir kısmını tüketir.

Bu seçenek kullanıldığında, aşağıdaki davranış ortaya çıkar:

- Azaltma anahtarları gerekli değildir veya kullanılmaz. 
- Tahmin tümüyle azaltıldıysa, geçerli tahminin tahmin gereksinimleri 0 (sıfır) olur.
- Gelecekte başka bir tahmin yoksa, girilen son tahmindeki tahmin gereksinimleri azaltılır.
- Zaman dilimleri, tahmin azaltma hesaplamasına eklenir.
- Artı günler, tahmin azaltma hesaplamasına eklenir.
- Fiili sipariş hareketlerinin tahmin gereksinimlerini aşması durumunda, kalan hareketler sonraki tahmin dönemine iletilmez.

##### <a name="example-1-transactions--dynamic-period"></a>Örnek 1: Hareketler - dinamik dönem

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

##### <a name="example-2-transactions--dynamic-period"></a>Örnek 2: Hareketler - dinamik dönem

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

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a>Bir tahmin azaltma anahtarı oluşturun ve ayarlayın

Bir tahmin azaltma anahtarı **Hareketler - azaltma anahtarı** ve **Yüzde - azaltma anahtarı** yöntemlerinde tahmin gereksinimlerini azaltmak için kullanılır. Bir azaltma anahtarı oluşturmak ve ayarlamak için bu adımları izleyin.

1. **Master planlama \> Kurulum \> kapsam \> Azaltma anahtarları**'na gidin.
2. Yeni bir azaltma anahtarı oluşturmak için **Yeni**'yi seçin.
3. **Azaltma anahtarı** alanında, tahmin edilen azaltma anahtarı için benzersiz bir tanımlayıcı girin. Daha sonra **Adı** alanında, bir ad girin. 
4. Her bir dönemdeki dönemleri ve azaltma anahtarı yüzdesini tanımlayın:

    - **Efektif tarih** alanı, dönem başlangıçlarının oluşturulma tarihlerini belirtir. **Efektif tarihi kullan** seçeneği **Evet** olarak ayarlandığında, dönemler efektif tarihte başlar. **Hayır** olarak ayarlandığında, dönemler master planlamanın çalıştırıldığı tarihlerde başlar.
    - Tahmin azaltmanın gerçekleşeceği dönemleri tanımlayın.
    - Belirli bir dönem için tahmin gereksinimlerinin azaltılacağı yüzdeleri belirtin. Gereksinimlerini azaltmak için artı değerler ya da gereksinimleri artırmak için eksi değerler girebilirsiniz.

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a>Bir azaltma anahtarı kullanın

Bir tahmin azaltma anahtarının, öğenin kapsama grubuna atanmış olması gerekir. Bir öğenin kapsama grubuna bir azaltma anahtarı atamak için şu adımları izleyin.

1. **Master planlama \> Kurulum \> Kapsam \> Kapsam grupları**'na gidin.
2. **Diğer** hızlı sekmesinde, **Azaltma anahtarı** alanında, kapsama grubunu atamak için azaltma anahtarını seçin. Azaltma anahtarı, daha sonra bu kapsama grubuna ait tüm öğelere uygulanır.
3. Master planlama sırasında tahmin azaltmayı hesaplamak için bir azaltma anahtarını kullanmak için bu ayarı, tahmin planlama veya master planlama kurulumunda tanımlamanız gerekir. Aşağıdaki konumlarda birine gidin:

    - **Master planlama \> Kurulum \> Planlar \> Tahmin planları**
    - **Master planlama \> Ayar \> Planlar \> Master planlar**

4. **Tahmin planları** veya **Master planlar** sayfasında, **Genel** hızlı sekmesinde, **Tahmin gereksinimlerini azaltmak için yöntem** alanında, **Yüzde - azaltma anahtarı** veya **Hareketler - azaltma anahtarı**'nı seçin.

### <a name="reduce-a-forecast-by-transactions"></a>Bir tahmini hareketler ile azaltın

**Hareketler - azaltma anahtarı**'nı veya **Hareketler - dinamik dönem**'i tahmin gereksinimlerini azaltmak için bir yöntem olarak seçerseniz, hangi hareketlerin tahmini azaltacağını seçersiniz. **Karşılama grupları** sayfasında, **Diğer** Hızlı Sekmesinde, **Tahmini şunun üzerinden azalt** alanında, tüm hareketler tahmini azaltacaksa **Tüm tahminler**'i seçin veya yalnızca satış siparişleri tahmini azaltacaksa **Siparişler**'i seçin.

## <a name="forecast-models-and-submodels"></a>Tahmin modelleri ve alt modeller

Bu bölümde, tahmin modellerinin nasıl oluşturulacağı ve alt modeller ayarlanarak birden çok tahmin modelinin nasıl birleştirileceği açıklanmaktadır.

*Tahmin modeli* belirli bir tahmini adlandırır ve tanımlar. Tahmin modelini oluşturduktan sonra, buna tahmin satırları ekleyebilirsiniz. Birden çok madde için tahmin satırları eklemek için **Talep tahmin satırları** sayfasını kullanın. Seçili belirli bir madde için tahmin satırları eklemek üzere **Serbest bırakılmış ürünler** sayfasını kullanın.

Tahmin modeli, diğer tahmin modellerinden tahminler içerebilir. Bu sonucu elde etmek için diğer tahmin modellerini bir üst tahmin modelinin *alt modelleri* olarak eklersiniz. İlgili modeli üst tahmin modelinin alt modeli olarak ekleyebilmeniz için önce ilgili her modeli oluşturmanız gerekir.

Elde edilen yapı, birden çok bireysel tahminden gelen girişi birleştirmenizi (toplamanızı) sağladığından, tahminleri kontrol etmenin güçlü bir yolunu sunar. Bu nedenle, planlama açısından simülasyonlar için tahminleri birleştirmek kolaydır. Örneğin, normal bir tahminin bahar promosyonu tahminiyle birleşimini temel alan bir simülasyon ayarlayabilirsiniz.

### <a name="submodel-levels"></a>Alt model düzeyleri

Bir üst tahmin modeline eklenebilecek modül alt model sayısında bir sınırlama yoktur. Ancak yapı sadece bir seviye derinliğinde olabilir. Başka bir deyişle, başka bir tahmin modelinin alt modeli olan bir tahmin modelinin kendi alt modelleri olamaz. Bir tahmin modeline alt modeller eklediğinizde, sistem bu tahmin modelinin zaten başka bir tahmin modelinin alt modeli olup olmadığını denetler.

Master planlama kendi alt modellerine sahip bir alt modelle karşılaşırsa bir hata iletisi alırsınız.

#### <a name="submodel-levels-example"></a>Alt model düzeyleri örneği

Tahmin modeli A, alt model olarak B tahmin modeline sahiptir. Bu nedenle, B tahmin modelinin kendi alt modelleri olamaz. B tahmin modeline bir alt model eklemeye çalışırsanız aşağıdaki hata iletisini alırsınız: "Tahmin modeli B, A modelinin bir alt modelidir."

### <a name="aggregating-forecasts-across-forecast-models"></a>Tahmin modelleri genelinde tahminleri toplama

Aynı gün gerçekleşen tahmin satırları, tahmin modelleri ve alt modelleri genelinde toplanır.

#### <a name="aggregation-example"></a>Toplama örneği

Tahmin modeli A, alt model olarak B ve C tahmin modellerine sahiptir.

- Tahmin modeli A, 15 Haziran'da 2 adet için bir talep tahmini içerir.
- Tahmin modeli B, 15 Haziran'da 3 adet için bir talep tahmini içerir.
- Tahmin modeli C, 15 Haziran'da 4 adet için bir talep tahmini içerir.

Ortaya çıkan talep tahmini, 15 Haziran'da 9 adet (2 + 3 + 4) için tek bir talep olacaktır.

> [!NOTE]
> Her alt model, üst tahmin modelinin parametrelerini değil, kendi parametrelerini kullanır.

### <a name="create-a-forecast-model"></a>Tahmin modeli oluşturma

Tahmin modeli oluşturmak için şu adımları izleyin.

1. **Master planlama \> Kurulum \> Talep tahmini \> Tahmin modelleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni tahmin modeli için aşağıdaki alanları ayarlayın:

    - **Model**: Model için benzersiz bir tanımlayıcı girin.
    - **Ad**: Model için açıklayıcı bir ad girin.
    - **Durduruldu**: Genellikle, bu seçeneği *Hayır* olarak ayarlamanız gerekir. Yalnızca modele atanan tüm tahmin satırlarının düzenlenmesini engellemek istiyorsanız *Evet* olarak ayarlayın.

    > [!NOTE]
    > **Nakit akışı tahminlerine dahil et** alanı ve **Proje** hızlı sekmesindeki alanlar master planlamayla ilişkili değildir. Bu nedenle, bu bağlamda bunları yoksayabilirsiniz. Bunları yalnızca **Proje yönetimi ve muhasebe** modülü için tahminlerle çalışırken göz önünde bulundurmanız gerekir.

### <a name="assign-submodels-to-a-forecast-model"></a>Tahmin modeline alt modeller atama

Bir tahmin modeline alt modeller atamak için şu adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Tahmin \> Tahmin modelleri**'ne gidin.
1. Liste bölmesinde, alt model ayarlamak istediğiniz tahmin modelini seçin.
1. **Alt model** hızlı sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki alanları ayarlayın:

    - **Alt model**: Alt model olarak eklenecek tahmin modelini seçin. Bu tahmin modelinin zaten var olması ve kendi alt modellerine sahip olmaması gerekir.
    - **Ad**: Alt model için açıklayıcı bir ad girin. Örneğin bu ad, alt modelin üst tahmin modeliyle ilişkisini gösterebilir.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

