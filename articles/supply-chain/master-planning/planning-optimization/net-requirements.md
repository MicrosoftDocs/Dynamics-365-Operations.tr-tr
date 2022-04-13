---
title: Planlama Optimizasyonu ile ilgili net gereksinimler ve ilişkilendirme bilgileri
description: Bu konuda, Planlama Optimizasyonu'nda hesaplanan net gereksinimler ve ilişkilendirme bilgileri hakkında bilgi sağlanmaktadır.
author: t-benebo
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: edfa6010074a4b04b3200115891723cd45871624
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468874"
---
# <a name="net-requirements-and-pegging-information-with-planning-optimization"></a>Planlama Optimizasyonu ile ilgili net gereksinimler ve ilişkilendirme bilgileri

[!include [banner](../../includes/banner.md)]

Planlama Optimizasyonu'nda master planlama çalıştırdığınızda bunun çıktısını, mevcut tedarikin talebi nasıl kapsadığını ve özel tedarik oluşturulma nedenini anlamanız önemlidir. Master planlamanın ürettiği hesaplanmış gereksinimleri daha iyi anlamak için **Net gereksinimler** sayfasını kullanabilirsiniz.

**Net gereksinimler** sayfasında, Planlama Optimizasyonu'nun ürün için hesapladığı net gereksinimler gösterilmektedir. Ayrıca master planlama çalıştırması sırasında uygulanan kapsam ayarları, hareket türüne göre gereksinim toplamları dökümü ve ilişkilendirme bilgileri de gösterilmektedir.

## <a name="open-the-net-requirements-page"></a>Net gereksinimler sayfasını açma

**Net gereksinimler** sayfasını aşağıdaki yollardan biriyle açabilirsiniz:

- **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin. Bir ürün seçin veya açın. Ardından Eylem Bölmesi'nde, **Plan** sekmesindeki **Gereksinim** gurubunda **Net gereksinimler**'i seçin.
- **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin. Bir satış siparişi açın. Ardından görev çubuğundaki **Satış siparişi satırları** hızlı sekmesinde **Ürün ve tedarik \> Net gereksinimler**'i seçin.
- **Master planlama \> Master planlama \> Planlı siparişler** öğesine gidin. Planlanan bir sipariş seçin veya açın. Ardından Eylem Bölmesi'nde, **Görünüm** sekmesindeki **Gereksinimler** gurubunda **Gereksinim profili**'ni seçin.

## <a name="use-the-net-requirements-page"></a>Net gereksinimler sayfasını kullanma

**Net gereksinimler** sayfası, üst ve alt bölümlerden oluşur. Bu sayfadaki Eylem Bölmesi bir **Güncelleştir** düğmesi içerir. Bu düğme seçildiğinde bir komut menüsü görüntülenir.

### <a name="select-a-master-plan-to-view"></a>Görüntülenecek bir master plan seçme

Ürünün net gereksinimlerini incelemeden önce sayfanın üst kısmındaki **Plan** alanında ilgili master planı seçtiğinizden emin olun.

### <a name="upper-section"></a>Üst bölüm

Sayfanın üst bölümünde aşağıdaki sekmeler bulunur:

- **Genel bakış**: Ürün boyutlarının madde gereksinimlerini görüntüleyin.
- **Madde karşılama**: Gereksinim hesaplaması sırasında kullanılan kapsam ayarlarını görüntüleyin.
- **Özet**: Hareket türüne göre gereksinim toplamları dökümünü görüntüleyin.
- **Dönem**: Dönem şablonu tarafından tanımlanan her dönem için girişleri, çıkışları ve tahmini kullanılabilir stoku görüntüleyebilirsiniz. Ayrıca tahmini kullanılabilir stokun grafik görünümünü de alabilirsiniz.

### <a name="lower-section"></a>Alt bölüm

Sayfanın alt bölümünde aşağıdaki sekmeler bulunur:

- **Genel bakış**: Gereksinimlere karşılık gelen çıkış ve giriş hareketleriyle birlikte master planlama sırasında hesaplanan ürün gereksinimlerinin listesini görüntüleyin. Varsayılan olarak liste, gereksinim tarihine göre sıralanır. Gereksinim seçtiğinizde alt bölümdeki **İlişkilendirme** hızlı sekmesinde, gereksinimin kaynağı veya gereksinimi karşılayan hareketler gösterilir.
- **Genel**: Seçili gereksinim hakkında ayrıntılı bilgileri görüntüleyin.
- **Eylem**: Gereksinimler için eylem iletilerini görüntüleyin.

### <a name="the-action-pane"></a>Eylem Bölmesi

Eylem Bölmesi'nde aşağıdaki komutlar kullanılabilir:

- **Güncelleştir \> Master planlama**: Master planlamayı doğrudan **Net gereksinimler** sayfasından çalıştırın.
- **Güncelleştir \> Tahmin planlama**: Tahmin planlamayı doğrudan **Net gereksinimler** sayfasından çalıştırın. Planlama Optimizasyonu henüz bu işlemi desteklememektedir.
- **Güncelleştir \> Devamlık planlama**: Devamlık planlamayı doğrudan **Net gereksinimler** sayfasından çalıştırın. Planlama Optimizasyonu henüz bu işlemi desteklememektedir.

## <a name="example-scenario"></a>Örnek senaryo

Bu örnekte, ilişkilendirme bilgilerinin **Net gereksinimler** sayfasında nasıl sunulduğu gösterilmektedir.

### <a name="prerequisites"></a>Önkoşullar

Senaryo üzerinde çalışmaya başlamadan önce aşağıdaki önkoşulları hazırlayın:

1. Standart örnek verilerin bulunduğu bir sistem üzerinde çalışmanız ve tüzel kişiliği *USMF* olarak ayarlamanız gerekir.
2. Bu örnekte, USMF örnek verilerinin parçası olarak *1000* ürünü kullanılmaktadır. Bu ürünün kullanılabilir olduğundan ve aşağıdaki şekilde ayarlandığından emin olun:

    - **Varsayılan sipariş türü:** *Satınalma siparişi*
    - **Eldeki stok:** *10,00*

3. *1000* ürününden miktar olarak *25,00* adet için bir satış siparişi oluşturun. Eldeki stokun bulunduğu depolama boyutlarını kullanın.
4. *DynPlan* master planı için master planlama çalıştırın.

### <a name="review-the-calculated-requirements"></a>Hesaplanan gereksinimleri inceleme

Ardından, hesaplanan gereksinimlerin birbirlerine nasıl karşılık geldiğini incelemek üzere *1000* ürünü için **Net gereksinimler** sayfasını açarsınız.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. *1000* için **Madde numarası** değerine sahip ürünü seçin.
1. Eylem Bölmesi'nde, **Plan** sekmesindeki **Gereksinim** gurubunda **Net gereksinimler**'i seçin.
1. **Net gereksinimler** sayfasında, **Plan** alanını *DynPlan* olarak ayarlayın.
1. Sayfanın alt bölümündeki **Genel Bakış** sekmesinde, aşağıdaki gereksinimlerin ızgarada satır olarak listelendiğini doğrulayın.

    | Referans | Gereksinim miktarı | Kümülatif |
    |---|---|---|
    | Eldeki | 10,00 | 10,00 |
    | Planlı satınalma siparişleri | 15.00 | 25.00 |
    | Satış siparişi | -25,00 | (Boş) |

    > [!NOTE]
    > **Gereksinim miktarı** alanı, gereksinim için gereken (değer negatifse) veya tedarik edilen (değer pozitifse) toplam miktarı temsil eder. **Kümülatif** alanı, seçili dönem boyunca biriktirilen toplam giriş ve çıkış miktarlarını temsil eder.

1. *Eldeki* gereksinim satırını seçin ve ardından **İlişkilendirme** hızlı sekmesinde, bu tedarik tarafından kapsanan gereksinimleri inceleyin. Aşağıdaki satır burada görünmelidir.

    | Referans | Gereksinim miktarı | Karşılanan miktar |
    |---|---|---|
    | Satış siparişi | -25,00 | -10,00 |

    Mevcut eldeki stok kısmen satış siparişinden gelen talebi kapsar.

    ![Eldeki stok için ilişkilendirme bilgileri](media/pegging-on-hand.png "Eldeki stok için ilişkilendirme bilgileri")

1. *Planlı satınalma siparişleri* gereksinim satırını seçin ve ardından **İlişkilendirme** hızlı sekmesinde, bu tedarik tarafından kapsanan gereksinimleri inceleyin. Aşağıdaki satır burada görünmelidir.

    | Referans | Gereksinim miktarı | Karşılanan miktar |
    |---|---|---|
    | Satış siparişi | -25,00 | -15,00 |

    Satış siparişi kısmen karşılandığından sistem, kalan karşılanmamış miktar için bir planlı satınalma siparişi oluşturur.

    ![Planlı satınalma siparişi için ilişkilendirme bilgileri](media/pegging-planned-purchase-order.png "Planlı satınalma siparişi için ilişkilendirme bilgileri")

1. *Satış siparişi* gereksinim satırını seçin ve ardından **İlişkilendirme** hızlı sekmesinde bu talebi kapsayan gereksinimleri inceleyin. Aşağıdaki satırlar burada görünmelidir.

    | Referans | Gereksinim miktarı | Karşılanan miktar |
    |---|---|---|
    | Eldeki | 10,00 | 10,00 |
    | Planlı satınalma siparişleri | 15.00 | 15.00 |

    ![Satış siparişi için ilişkilendirme bilgileri](media/pegging-planned-purchase-order.png "Satış siparişi için ilişkilendirme bilgileri")

> [!NOTE]
> Planlama Optimizasyonu henüz bazı özellikleri desteklemediğinden *Emniyet stoku* ve *Süresi dolan toplu iş* gereksinim türleri, **Net gereksinimler** sayfasına dahil değildir. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).
>
> Yerleşik Master planlama altyapısını kullanıyorsanız toplu iş denetimli ürünler desteklenir. Toplu iş denetimli ürünler için süresi dolan eldeki stok, **Net gereksinimler** sayfasında gösterilir ancak talep gereksinimleriyle ilişkilendirilmez. Bu tür için süresi dolan eldeki satırlar, **Net gereksinimler** sayfasında *Süresi dolan toplu iş* gereksinim satırları olarak gösterilir.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
