---
title: POS'ta iskontoları gösterme
description: Bu makale, Microsoft Dynamics 365 Commerce'ın satış görevlilerine promosyonlar hakkında bilgi edinme ve bunları çapraz satış ve yukarı satış için kullanma konusunda nasıl yardımcı olduğunu açıklamaktadır.
author: ShalabhjainMSFT
ms.date: 07/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: e3ec16c5051088ed2777309899b26094e8d67743
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878552"
---
# <a name="show-discounts-in-pos"></a>POS'ta iskontoları gösterme

[!include [banner](includes/banner.md)]

Promosyonlar, satın alma kararları veren müşterileri motive etmede önemli bir rol oynar. Örneğin, tüm perakende pazarında baştan çıkarıcı promosyonlar ve indirimler olduğundan, tatiller perakendeciler için en yüksek sayıda satışı üretebilir. Mağaza görevlileri kullanılabilir promosyonlar hakkında bilgi sahibiyse ve mevcut promosyonları anlıyorsa, çapraz satış ve yukarı satış yapmak için bu promosyonlardan yararlanabilirler. Bu makale, Microsoft Dynamics 365 Commerce'ın satış görevlilerine promosyonlar hakkında bilgi edinme ve bunları çapraz satış ve yukarı satış için kullanma konusunda nasıl yardımcı olduğunu açıklamaktadır.

## <a name="learn-about-store-discounts"></a>Mağaza iskontoları hakkında bilgi edinme

Commerce, "Tüm iskontoları görüntüle" adlı bir işlem içerir. Bu işlem, bir mağazada yürütülen tüm iskontoları gösterir. "Tüm iskontoları görüntüle" işlemi satış noktasındaki (POS) bir düğmeyle eşlenebilir ve söz konusu düğme **Karşılama** sayfasına veya **Hareket** sayfasına eklenebilir. Aşağıdaki örnekte açılan **Tüm iskontolar** sayfasının bir örneği gösterilmektedir.

![Tüm iskontolar sayfası.](./media/View_all_discounts.png "Tüm iskontolar sayfası")

İskontoları görüntülemek için, sistem aşağıdaki koşullardan bir veya daha fazlasıyla eşleşen tüm iskontoları arar:

- İskontonun fiyat grubu, mağazanın fiyat grubuyla eşleşir.
- İskontonun fiyat grubu bir ilişki veya bağlılık programıyla eşlenir.
- İskontonun fiyat grubu, mağaza ile ilişkilendirilmiş bir katalogla eşlenir.

**Tüm iskontolar** sayfası yalnızca bazı kupon tabanlı iskontoları gösterir, çünkü perakendeciler benzersiz müşteriler için genellikle binlerce kupon ve bunlara karşılık gelen iskontolar oluşturur ve bu sayfa müşteriye özel iskontoları göstermeye yönelik değildir. Kupon tabanlı iskontolar yalnızca her kupon başlığında **Kupon kodu olmadan uygula** seçeneği açık olduğunda görüntülenir. Bu durumda, kasiyerler herhangi bir kupon kodu veya bar kod girmek veya taramak zorunda kalmadan kuponu uygulayabilir.

**Kupon kodu olmadan uygula** seçeneği açık olduğunda çeşitli senaryolar kullanılabilir hale gelir. Örneğin, kasiyerler müşteriyi yatıştırma veya ürün arızaları nedeniyle müşterilere ek indirimler verebilir. Yazdırılan kupon kodları veya barkodların kasiyerlere dağıtılması gerekmez. Bunun yerine, kasiyerler **Kupon uygula** düğmesini seçebilir. Kupon harekete otomatik olarak uygulanır. Kupon başlığı için birden çok kupon varsa, sistem otomatik olarak hareketteki ilk etkin kuponu seçer.

**Tüm iskontolar** sayfasında, satış görevlileri iskontoları anahtar sözcüklere göre arayabilir. Anahtar sözcük araması, indirim adını ve indirim açıklamasını içeren alanları arar. Satış görevlileri, iskontonun kupon kodu gerektirip gerektirmediğini temel alarak da iskontoları filtreleyebilir.

## <a name="cross-sell-and-upsell-by-using-discounts"></a>İskontoları kullanarak çapraz satış ve yukarı satış

Miktar iskontoları, karıştır ve eşle iskontoları ve eşik iskontoları gibi çok satırlı iskontolar, müşterileri daha büyük indirimler elde etmek amacıyla daha fazla ürün satın almaya ikna etmek için ideal bir yoldur. Bu nedenle, müşterinin sepetinin boyutunu ve satıcının gelirini artırmaya da yardımcı olurlar. Bu iskontolar e-ticaret web sitelerinde, sosyal medyada ve mağazadaki panolarda duyurulabilir.

Ancak, tüm bu tanıtım yöntemleri kullanıldığında bile, müşteriler promosyonlardan yararlanma fırsatını kaçırabilir. Satış görevlilerinin, seçili bir satıra veya alışveriş sepetinin tamamına hangi promosyonların uygulanabilir olduğunu olduğunu öğrenmesine olanak sağlamak için, perakendeciler **"Kullanılabilir iskontoları görüntüle"** işlemi için **Hareket** sayfasındaki düğme ızgarasına düğme ekleyebilir. Sonuç olarak, bir satış görevlisi bir hareket satırını seçip seçili satır için kullanılabilir olan tüm iskontoları görmek için düğmeyi seçebilir. Satış görevlisi, tüm hareket için geçerli olan iskontoları görüntülemek için başka bir sekme de seçebilir. İskonto bilgileri zaten satış satırında gösterildiğinden, **Kullanılabilir iskontoları görüntüle** seçeneğinin satış satırında uygulanan iskontoları göstermediğine dikkat edin. Bu senaryonun amacı, yalnızca henüz uygulanmamış olan iskontoları göstermektedir. Bunun özel durumu, "Kupon kodu olmadan uygula" olarak işaretlenmiş bir kuponu temel alarak uygulanmış iskontolardır. Bu, satış görevlisinin uyguladıkları kuponu kaldırmasını kolaylaştırır.

**Tüm İskontolar** sayfası yalnızca uygulanan indirimlerle rekabet vermeyen iskontoları gösterir. Bu davranış, bir satış görevlisinin müşteriyi bir iskontoyla ilgili bilgilendirmesi ve müşterinin gerekli eylemi yapması durumunda (örneğin, müşterinin yüzde 10 indirim almak için bir ürün daha satın alması), iskontonun harekete uygulanmasını sağlar. Kupon tabanlı iskontolar yalnızca **Kupon kodu olmadan uygula** seçeneği açık olduğunda görüntülenir.

Tüm iskontoların aynı önceliğe sahip olduğu basit bir senaryoda, iskonto eşzamanlılık modu **Bileşik** olur ve iskonto eşzamanlılık denetimi **En iyi fiyat ve öncelik içinde bileşim, öncelikler arasında kesinlikle bileşim yok** olarak ayarlanır; İskontolar bileşik olduğundan ve birbirleriyle rekabet etmediğinden **Tüm iskontolar** sayfası bir ürün için kullanılabilir tüm iskontoları gösterir.

Aşağıdaki örnekler, indirim eşzamanlılık modunun **En iyi fiyat** veya **Özel** olduğu ve iki veya daha fazla önceliğin kullanıldığı bir senaryo gibi ileri düzey senaryolarda hangi iskontoların gösterileceğini belirleyen mantığı gösterir. Bu senaryolarda, gösterilen indirimler indirim eşzamanlılık denetiminin **En iyi fiyat ve öncelik içinde bileşim, öncelikler arasında kesinlikle bileşim yok** veya **Yalnızca öncelik içinde en iyi fiyat, daima öncelik üzerinde birleştir** olarak ayarlanmış olmasına bağlı olarak daha fazla etkilenebilir.

Aşağıdaki örnek, indirim eşzamanlılık denetimi **En iyi fiyat ve öncelik içinde bileşim, öncelikler arasında kesinlikle bileşim yok** olarak ayarlandığında kullanılan mantığı gösterir.

![En iyi fiyat ve öncelik içinde bileşim, öncelikler arasında kesinlikle bileşim yok mantığı.](./media/Model_1.png "En iyi fiyat ve öncelik içinde bileşim, öncelikler arasında kesinlikle bileşim yok mantığı").

Aşağıdaki örnek, indirim eşzamanlılık denetimi **Yalnızca öncelik içinde en iyi fiyat, daima öncelik üzerinde birleştir** olarak ayarlandığında kullanılan mantığı gösterir.

![Yalnızca öncelik içinde en iyi fiyat, daima öncelik üzerinde birleştir.](./media/Model_2.png "Yalnızca öncelik içinde en iyi fiyat, daima öncelik üzerinde birleştir mantığı").


[!INCLUDE[footer-include](../includes/footer-banner.md)]