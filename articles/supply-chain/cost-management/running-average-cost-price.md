---
title: Cari ortalama maliyet fiyatı
description: Stok kapanışı işlemi, maddenin madde modeli grubunda seçilen stok değerleme yöntemine dayanarak çıkış hareketlerini giriş hareketlerine karşılık kapatır. Ancak, stok kapanışı çalıştırılmadan önce, sistem çoğu durumda çıkış hareketlerini deftere nakletmek için kullanılan bir cari ortalama maliyet fiyatı hesaplar.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d324324312ce9e47b07de8e3de952b8d7c53647
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672192"
---
# <a name="running-average-cost-price"></a>Cari ortalama maliyet fiyatı

[!include [banner](../includes/banner.md)]

Stok kapanışı işlemi, maddenin madde modeli grubunda seçilen stok değerleme yöntemine dayanarak çıkış hareketlerini giriş hareketlerine karşılık kapatır. Ancak, stok kapanışı çalıştırılmadan önce, sistem çoğu durumda çıkış hareketlerini deftere nakletmek için kullanılan bir cari ortalama maliyet fiyatı hesaplar.

Sistem, aşağıdaki formülü kullanarak maddenin söz konusu yürütülen ortalama maliyet fiyatını tahmin eder:

Tahmini fiyat = (Fiziksel tutar + Mali tutar) ÷ (Fiziksel miktar + Mali miktar)

## <a name="default-item-cost"></a>Varsayılan madde maliyeti

Serbest bırakılan bir ürünün varsayılan madde maliyeti, **Serbest bırakılan ürün ayrıntıları** sayfasındaki iki yoldan biriyle yapılandırılabilir:

- Eylem Bölmesi'nin **Maliyetleri yönet** sekmesinin **Kurulum** grubunda **Madde fiyatı**'nı seçerek standart maliyet oluşturun. Bu yöntemi kullanırsanız, standart bir maliyet maliyetleme sürümü kullanmanız ve maliyetin etkinleştirilmesi gerekir.
- **Maliyetleri yönet** Hızlı Sekmesindeki **Fiyat** alanına bir değer girerek serbest bırakılmış bir ürün için varsayılan madde maliyet fiyatı tanımlayın.

Fiyat girmenin veya oluşturmanın yanı sıra, **Serbest Bırakılan ürün ayrıntıları** sayfasının **Maliyetleri Yönet** Hızlı Sekmesinde **En son maliyet fiyatını kullan** onay kutusunu seçebilirsiniz. Bu durumda, bir mali güncelleştirme deftere nakletdiğinizde sistem **Fiyat** alanını otomatik olarak güncelleştirir. Örneğin, bir satınalma siparişi faturasını deftere naklederseniz, alan bu faturadan satınalma fiyatı olarak ayarlanır.

Etkin bir maliyetleme sürümünde maliyet fiyatınız varsa ve **Maliyetleri yönet** Hızlı Sekmesinde bir fiyat girerseniz sistem **Maliyetleri yönet** Hızlı Sekmesinde tanımlanan fiyatı kullanmadan önce etkin maliyet sürümündeki fiyatı kullanır.

## <a name="using-the-running-average-cost-price"></a>Cari ortalama maliyet fiyatını kullanma

Aşağıdaki tabloda sistemin ne zaman stok hareketlerini cari ortalama maliyet fiyatını kullanarak deftere naklettiği ve ne zaman madde master kaydında tanımlı maliyet fiyatını kullandığı gösterilmiştir.

| Koşul | Sistem, tahmini cari ortalama maliyet fiyatını kullanır | Sistem varsayılan madde maliyet fiyatını kullanır |
| --- | --- | --- |
| Hem pay\* hem de payda\*\* pozitiftir. | Evet | Hayır |
| Pay\*, payda\*\* veya her ikisi de negatiftir. | Hayır | Evet |
| Payda\*\* 0'dır (sıfır). | Hayır | Evet |

\* Pay = (Fiziksel tutar + Mali tutar)  
\*\* Payda = (Fiziksel miktar + Finansal miktar)

> [!NOTE]
> Bir madde için **Fiziksel değeri dahil et** seçeneği seçilmezse, sistem hem fiziksel tutar hem de fiziksel miktar için 0 (sıfır) kullanır. Bu seçenek hakkında daha fazla bilgi için, bkz. [Fiziksel değeri dahil et](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Fiyat yükselmesinden kaçınma

Bazı nadir durumlarda sistem fiyat için temel alacağı yeterli girişe sahip olmadan birkaç çıkış fiyatlandırır. Bu senaryo, cari ortalama maliyet fiyatı tahmininde aşırı şişmeye neden olabilir. Ancak, fiyat yükselmesinden kaçınmak veya olduğu zaman etkilerini azaltmak için alabileceğiniz önlemler vardır.

**Senaryo:** **Fiziksel değeri dahil et** seçeneğini belirlediğiniz bir madde için aşağıdaki hareketler gerçekleşir:

1. Mali olarak 100,00 Amerikan dolarında 100 miktarını alırsınız.
2. Mali olarak 200 miktarını çıkarırsınız.
3. Fiziksel olarak 202,00 Amerikan dolarında 101 miktarını alırsınız.

Bir madde için tahmini cari ortalama maliyet fiyatını incelediğinizde, 1,51 Amerikan doları maliyet fiyatı beklersiniz. Bunun yerine, aşağıdaki formülü temel alan, tahmini ortalama 102,00 ABD dolarını bulursunuz:

Tahmini fiyat = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102

Bu fiyatlandırma amplifikasyonu, 2. adımda 200 madde mali olarak çıkış yaptığında sistemin karşılık gelen girişler oluşmadan önce bu maddelerin 100 tanesini fiyatlandırması gerektiği için oluşur. Bu durum, negatif stok sonucunu doğurur. Ardından, sistem, bekleyebileceğiniz gibi 1,00 Amerikan dolarlık bir birim fiyatı tahmin eder. Ancak karşılık gelen 100 giriş geldiğinde, her birinin birim fiyatı 2,00 Amerikan doları olur.

> [!NOTE]
> Çıkışlar negatif stok oluşturmasına rağmen, çıkış fiyatı hesaplandığında stok pozitiftir. Madde masterındaki fiyat yerine cari ortalama maliyet fiyatının kullanılmasının nedeni budur. Bu noktada, sistemdeki stok mahsup değeri 100,00 USD'dir. Bu mahsup 100 parça üzerinden oluşturulmuş olsa da, her biri 1,00 Amerikan dolarlık bir birim mahsup olduğunda artık yalnızca tek parça stokunuz olur. Bu nedenle, bu tek parçaya 100,00 Amerikan dolarlık bir mahsup tahsis edilir. Sonuç, aşırı şişirilmiş maliyet fiyatıdır.
>
> Karşılaştırma için, senaryodaki 2. ve 3. adımlar yer değiştirdiğinde 1,51 Amerikan dolarlık bir birim fiyatına 200 maddenin çıkarılacağını ve bir parçanın 1,51 Amerikan doları birim fiyatında kalacağını görebilirsiniz. Bu fiyat yükseliş senaryosu negatif stok durumunda gerçekleşebildiğinden, aşağıdaki durumlarda kaçınılması zordur:
>
> - Çıkış fiyatlarını eldeki değer ve miktarda tahmin etmeniz gerekiyorsa.
> - Çıkış ve girişlerde eldeki değeri ve miktarı ayarlamanız gerekiyorsa.
> - İş modeliniz elinizde olandan daha çok parçayı göndermenize veya fiyatlandırmanıza olanak veriyorsa.
> - Size gönderilen giriş değerini ve miktarını kabul etmeniz gerekiyorsa.

İş modeliniz bunlara olanak verse de, aşağıdaki uygulamalar fiyat yükseliş senaryosuna neden olabilecek negatif miktarların oluşmasını engellemenize yardımcı olabilir:

- Bir madde için **Fiziksel değeri dahil et** seçeneğini belirlerseniz, **Madde model grupları** sayfasındaki **Fiziksel negatif stok** onay kutusunun seçimini kaldırın.
- Bir madde için **Fiziksel değeri dahil et** seçeneğini **belirlemezseniz**, **Madde model grupları** sayfasındaki **Mali negatif stok** onay kutusunun seçimini kaldırın.

Ayrıca, fiziksel stok değerinizdeki maksimum mahsubun, fiziksel hareket sayısı ile fiziksel ve mali fiyatlar arasındaki farkla sınırlı olduğunu aklınızda bulundurun. Tüm fiziksel hareketler sonunda mali olarak güncelleştirildiği sürece fiziksel değer aşırı düzeylere yükselemez. Son olarak, biriken mahsup sadece tek parça yerine eldeki birden çok parça üzerine dağıtıldığında, yükselmenin etkisi önemli ölçüde azalır.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Çıkışlarda sıfır maliyet fiyatından kaçının

**Madde modeli grubu** sayfasında **Fiziksel değeri dahil et** seçeneği işaretlenmediğinde, stokta mali olarak güncelleştirilmiş giriş yoksa stoktaki bir numara sıfır maliyet fiyatına sahip olabilir. Bu senaryoyu önlemeye yardımcı olmak için aşağıdaki seçenekleri göz önünde bulundurun:

- **Madde modeli grubu** sayfasında bir **Fiziksel değeri dahil et** seçeneğini seçin. Bu seçenek, girişin fiziksel olarak güncelleştirilmesi koşuluyla, bir çıkışta sıfır maliyet fiyatını önler. Negatif fiziksel stoka izin vermezseniz çıkışlar fiziksel olarak güncelleştirilmiş hareketlerden ortalamayı hesaplar.
- Standart maliyeti olan bir maliyet sürümünü etkinleştirerek varsayılan bir madde maliyet fiyatı oluşturun veya **Serbest Bırakılan ürün ayrıntıları** sayfasının **Maliyetleri yönet** Hızlı Sekmesinde fiyatı girin. Bu seçenek, **Madde modeli grubu** sayfasında **Fiziksel değeri dahil et** seçeneği seçilmediğinde en iyisidir, çünkü sistemin her zaman kullanılacak bir geri dönüş fiyatı olacaktır.
- **Serbest bırakılan ürün ayrıntıları** sayfasının **Maliyetleri Yönet** Hızlı Sekmesinde **En son maliyet fiyatını kullan** seçeneğini belirleyin. Bu seçenek, bir alış irsaliyesini her mali olarak güncelleştirdiğinizde **Fiyat** alanını güncel tutar. Bu seçeneği belirlerseniz ancak standart bir maliyet sürümünde varsayılan bir fiyat girmez veya bir maliyeti etkinleştirmezseniz, bir çıkışta sıfır maliyetiniz olabilir.

Maliyeti sıfır olan hareketler çıkardıysanız, *Stok kapatma ve ayarlama* işlemi, girişler mali olarak güncelleştirildikten sonra bir ayarlama oluşturarak maliyet fiyatını düzeltir. Bu güncelleştirmenin gerçekleştiği mali dönemin, maddelerin fiziksel olarak alındığı veya verildiği mali dönemden farklı olabileceğini unutmayın.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
