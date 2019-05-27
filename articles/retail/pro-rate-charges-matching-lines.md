---
title: Başlık giderlerini eşleşen satış satırlarına eşit dağıt
description: Bu konu, Perakende kanal siparişlerine otomatik giderlerin hesaplanmasını ve uygulanması için ek yeterlilikleri, gelişmiş otomatik masraf özelliğini kullanarak açıklar.
author: hhaines
manager: annbe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 07eea8fd7af4da611b4bd0c9340923f8894fab2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1526027"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a>Başlık giderlerini eşleşen satış satırlarına eşit dağıt


[!include [banner](includes/banner.md)]

Bu konu, başlık düzeyi otomatik masrafları gruplandırmayı ve bunları perakende satış satırlarına eşit dağıtmak için özelliği açıklar. Bu özellik, Microsoft Dynamics 365 for Retail sürüm 10.0.1 içinde satış noktası (POS) içerisinde ve Microsoft Dynamics 365 for Retail sürüm 10.0.2 içinde çağrı merkezinde oluşturulmuş hareketler için kullanılabilirdir.

Bu özellik, yalnızca [gelişmiş otomatik masraflar](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) özelliği, **Perakende parametreleri** sayfasındaki seçenek kullanılarak açılmışsa kullanılabilirdir. Ek olarak, otomatik giderler için gelişmiş hesaplama yöntemi, yalnızca perakende kanalları aracılığıyla oluşturulmuş (POS, çağrı merkezi ve Dynamics e-Ticaret platformu) perakende satış siparişlerine uygulanabilir.

Bu yeni özellik, başlık düzeyi otomatik masrafların hesaplanmasına ve perakende satış hareketlerine uygulanmasında kuruluşlara daha fazla esneklik verir.

Sürüm 10.0.1'den önceki Microsoft Dynamics 365 for Retail sürümlerinde, belirli bir teslimat modu ilişkisine sahip başlık düzeyi otomatik giderleri, yalnızca satış siparişi başlığında tanımlanmış teslimat modu ile bir eşleşme olduğunda hesaplanır.

Örneğin, başlık düzeyi otomatik masraflar, teslimat modu **99** ve teslimat modu **11** için tanımlanmıştır. Bir satış siparişi oluşturulur ve teslimat modu **99**, sipariş başlığında tanımlanır. Ancak, satış satırlarının bazıları, teslimat modu **11** kullanılarak sevk edilmek üzere ayarlanmıştır. Bu durumda, yalnızca teslimat modu **99** ile bağlantılı başlık düzeyi masrafları dikkate alınır ve satış siparişine uygulanır.

Dynamics 365 for Retail içinde, başlık düzeyi masrafları, bir [katmanlı masraf yapılandırması](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) tanımlamanıza izin veren ek bir özelliğe sahiptir. Örneğin, sipariş değeri 50,00 $ ve 200,00 $ arasındaysa, bir kuruluş 5,00 $ tutarında navlun gideri isteyebilir. Ancak, siparişin değeri 200,01 $ ve 500,00 $ arasındaysa, navlun ücreti 4,00 $ olabilir.

Bazı kuruluşlar, başlık düzeyi masraflarla sağlanan katmanlı masraf hesaplamasından faydalanmak ister. Ancak, karma teslimat modları içeren bazı senaryolarda, hesaplanan masrafların her bir satış satırında tanımlanmış teslimat modu ile eşleşmeye dayanmasını da temin etmek isterler.

Şimdi başlık düzeyi otomatik masrafları, sipariş üzerindeki tüm teslimat modlarının masraflar hesaplanırken dikkate alınmasını sağlayacak şekilde yapılandırabilirsiniz. Bu özellik, başlık düzeyi masrafları hesaplamak için daha karmaşık bir hesaplama mantığı gerektirir. Mantık, aynı teslimat modu kullanılarak sevk edilen tüm öğeleri gruplar ve bu grubu, başlık düzeyi otomatik masrafları hesaplarken bir hesaplama grubu olarak kullanır. Aynı teslimat moduna sahip öğeler için otomatik masraflar öğelerin birleştirilmiş satış değerine dayanarak hesaplanır. Bu şekilde, uygun otomatik masraf katmanı belirlenir.

Uygun başlık düzeyi masraflar aynı teslimat modunu kullanan satış satırları için alındıktan sonra, hesaplanan masraflar satış satırı düzeyine eşit şekilde dağıtılır. Bu masraflar satır düzeyinde olduğundan ve başlık düzeyinde tutulmadığından, daha belirgin bir bağlantı öğe ve bunun için hesaplanan masraf değer arasında yapılır. Bu davranış, kuruluşun yalnızca bazı öğeler iade edildiğinde masrafın tamamı yerine yalnızca bir kısmının geri ödenmesini istediği, kısmi iade senaryolarında faydalı olabilir.

## <a name="scenarios"></a>Senaryolar

Aşağıdaki iki örnek senaryo, bu masrafların yeni özellik kullanıldığında ve kullanılmadığında nasıl hesaplandığını gösterir.

### <a name="scenario-1"></a>Senaryo 1

Bu senaryo, **Eşleşen satış satırlarına eşit dağıt** seçeneği, otomatik masraf kurulumunda **Hayır** olarak ayarlanmasını açıklar. (Davranış, sürüm 10.0.1'den önceki Perakende sürümlerindeki başlık düzeyi masrafların davranışına eşdeğerdir)

Bu senaryoda, kuruluş teslimat modu ilişkisi **99** ve teslimat modu ilişkisi **11** için başlık düzeyi masrafları tanımlamıştır. Teslimat modu **21** için otomatik masraf yapılandırılmamıştır.

![Teslimat modu 99 için eşleşen satır eşit dağıtma kapalı olduğunda otomatik masraf](media/99_disabled.png)

![Teslimat modu 11 için eşleşen satır eşit dağıtma kapalı olduğunda otomatik masraf](media/11_disabled.png)

Bir satış siparişi çağrı merkezinde oluşturulur ve teslimat modu **99** olarak ayarlanır. Bu sipariş beş öğe içerir. İki sipariş satırı, teslimat modu **99** kullanmak üzere yapılandırılmıştır, iki satır teslimat modu **11** kullanmak üzere yapılandırılmıştır ve bir satır teslimat modu **21** kullanmak üzere yapılandırılmıştır, aşağıdaki tabloda gösterildiği gibi.

| Madde  | Satır miktarı | Teslimat şekli | Birim başına fiyat |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | 10 $            |
| 81332 | 1             | 99            | $50            |
| 81333 | 2             | 11            | 30 $            |
| 81334 | 3             | 99            | 10 $            |
| 81334 | 3             | 21            | 5 $             |

Bu senaryoda, siparişin tamamı teslimat modu **99** için otomatik masraf tablosuna karşı değerlendirilir. Tüm satış satırlarının son toplamı, otomatik masraf yapılandırmasında eşleşen bir katmanı belirlemek için kullanılır ve bu masraf sipariş başlığı düzeyinde uygulanır. Bu örnekte, sipariş toplamı 165,00 $ tutarındadır ve 15,00 $ navlun masrafı sipariş başlığına uygulanır. Teslimat modu **11** için yapılandırılan otomatik masraflara hiçbir zaman başvurulmaz veya uygulanmaz.

Bu senaryoda, bir müşteri siparişteki bazı öğeleri iade ederse ve [iade edileceği şekilde masraf kodu yapılandırılmışsa](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), toplam başlık düzeyi masrafı iadeye sistematik olarak uygulanır, yalnızca bazı öğeler iade edilmiş olsa bile.

### <a name="scenario-2"></a>Senaryo 2

Bu senaryoda, teslimat modu ilişkisi **99** ve teslimat modu ilişkisi **11** için başlık düzeyi masrafları tanımlanmıştır. Ancak, **Eşleşen satış satırlarına eşit dağıt** seçeneği bu otomatik masraf tabloları için **Evet** olarak ayarlanmıştır.

![Teslimat modu 99 için eşleşen satır eşit dağıtma açık olduğunda otomatik masraf](media/99_enabled.png)

![Teslimat modu 11 için eşleşen satır eşit dağıtma açık olduğunda otomatik masraf](media/11_enabled.png)

Bu senaryo, beş satır içeren aynı satış siparişini kullanır. Sipariş başlığındaki teslimat modu **99** olarak ayarlanmıştır ancak satış siparişindeki her bir öğenin teslimat modu aşağıdaki tablodaki gibi yapılandırılmıştır.

| Madde  | Satır miktarı | Teslimat şekli | Birim başına fiyat |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | 10 $            |
| 81332 | 1             | 99            | $50            |
| 81333 | 2             | 11            | 30 $            |
| 81334 | 3             | 99            | 10 $            |
| 81334 | 3             | 21            | 5 $             |

Otomatik masraf yapılandırması, eşleşen satış satırlarına eşit dağıtılmak üzere yapılandırıldığından, sistem aşağıdaki hesaplama adımlarını gerçekleştirir.

1. Aynı teslimat moduna sahip tüm öğeler birlikte gruplanır ve sistem, gruptaki öğelerin toplam ürün değerini hesaplar.

    **Teslimat modu 11**

    - Öğe 81331, miktar 1 = 10 $
    - Öğe 81333, miktar 2 = 60 $ net (birim başına 30 $)
    - **Teslimat modu 11 için toplam ürün değeri = 70 $**

    **Teslimat modu 99**

    - Öğe 81332, miktar 1 = 50 $
    - Öğe 81334, miktar 3 = 30 $ net
    - **Teslimat modu 99 için toplam ürün değeri = 80 $**

    **Teslimat modu 21**

    - Öğe 81334, miktar 3 = 15 $ net
    - **Teslimat modu 21 için toplam ürün değeri = 15 $**

2. Sistem, her bir öğe grubu için teslimat modunun ve müşterinin eşleştiği başlık düzeyi otomatik masrafları için yapılandırmayı arar. Yapılandırma bulunursa, sistem katmanlı yapılandırmaya bakarak uygulanacak masrafı bulur, teslimat modu grubundaki öğelerin toplam ürün değerine dayanarak.

    **Teslimat modu 11**

    - Toplam perakende ürün değeri = 70 $
    - **Masraf değeri = 7 $**

    **Teslimat modu 99**

    - Toplam perakende ürün değeri = 80 $
    - **Masraf değeri = 15 $**

    **Teslimat modu 21**

    - Toplam perakende ürün değeri = 15 $
    - **Masraf değeri = 0 $** (Bu müşteri ve teslimat modu için herhangi bir otomatik masraf yapılandırılmamıştır.)

    ![Teslimat modu 11 masrafları, vurgulanan katmana düşer](media/step2mode11.png)

    ![Teslimat modu 99 masrafları, vurgulanan katmana düşer](media/step2mode99.png)

3. Sistem, her bir satıra uygulanacak masraf değerini, satırın grubun toplam ürün değerine orantısal ilişkisini dikkate alan eşit dağıtma mantığına dayanarak hesaplar.

    **Teslimat modu 11**

    - Masraf değeri = 7 $
    - Grup ürün değeri = 70 $
    - Satır 1 değeri = 10 $ (= grup değerinin yüzde 14,2857'si)
    - Satır 3 değeri = 60 $ (= grup değerinin yüzde 85,7143'si)
    - **Satır 1 için satır masrafı = 1 $**
    - **Satır 3 için satır masrafı = 6 $**

    **Teslimat modu 99**

    - Masraf değeri = 15 $
    - Grup ürün değeri = 80 $
    - Satır 2 değeri = 50 $ (= grup değerinin yüzde 62,5'si)
    - Satır 4 değeri = 30 $ (= grup değerinin yüzde 37,5'si)
    - **Satır 2 için satır masrafı = 9,38 $**
    - **Satır 4 için satır masrafı = 5,62 $**

    **Teslimat modu 21**

    - Masraf değeri = 0 $
    - Grup ürün değeri = 15 $
    - Satır 5 değeri = 15 $ (= grup değerinin yüzde 100'si)
    - **Satır 5 için satır masrafı = 0 $**

Bu nedenle, bu örnek için öğe 81334'e 5,62 $ tutarında bir navlun masrafı atanacaktır. Bu giderleri satış satırı için **Giderleri koru** sayfasında görebilirsiniz. Aşağıdaki çizim, bu sayfanın öğe 81334 için nasıl gözükeceğini gösterir.

![Öğe 81334 için satış satırında eşit dağıtılmış masraflar](media/proratedlinecharge.png)

Bu hesaplama yöntemi, kısmi iade senaryoları için kullanılırsa, masraf kodu iade edilebilirse, masrafın yalnızca bu satıra tahsis edilmiş kısmı, öğe iade edildiğinde geri ödenecektir.
