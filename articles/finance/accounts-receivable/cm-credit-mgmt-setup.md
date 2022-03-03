---
title: Kredi yönetimi parametreleri kurulumu
description: Bu konuda, işletmenizin Kredi yönetimini işletmenizin gereksinimlerini karşılayacak şekilde yapılandırmak için kullanabileceğiniz seçenekler açıklanmaktadır.
author: JodiChristiansen
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d8bc4f0a981b75c1b65d51aa1d8fada9c2187e22
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323422"
---
# <a name="credit-management-parameters-setup"></a>Kredi yönetimi parametreleri kurulumu

[!include [banner](../includes/banner.md)]

Bu konuda, işletmenizin Kredi yönetimini işletmenizin gereksinimlerini karşılayacak şekilde yapılandırmak için kullanabileceğiniz seçenekler açıklanmaktadır. Alacak yönetimi özelliklerini kullanmaya başlamak için, **Kredi ve koleksiyonlar parametreleri** sayfasında (**Kredi ve koleksiyonlar \>Kurulum \>Kredi ve koleksiyonlar parametreleri**) parametreleri ayarlayın.

## <a name="credit-parameters"></a>Kredi parametreleri

Kredi yönetimini denetleyen parametreleri değiştirebileceğiniz **Kredi** bölümünde dört hızlı sekme vardır: **Kredi bekletme işlemleri**, **Kredi yönetimi denetim noktası**, **Kredi yönetim istatistikleri** ve **Kredi limitleri**. Aşağıdaki bölümlerde, her bir hızlı sekmede kullanılabilen ayarlar açıklanmaktadır.

### <a name="credit-holds"></a>Alacak tutmalar

- Satış siparişi bekletme listesinden serbest bırakıldıktan sonra satış siparişi değeri (genişletilmiş fiyat) arttığı zaman deftere nakil kurallarının yeniden denetlenmesini zorunlu kılmak için **Bekletilen sipariş serbest bırakıldıktan sonra satış siparişi değerinin düzenlemesine izin ver** seçeneğini **Hayır** olarak ayarlayın.
- **İptal edilen siparişlerin nedenleri** alanında, bir satış siparişinin kredi yönetimi bekletme işlemi iptal edildiğinde varsayılan olarak kullanılacak serbest bırakma nedenini seçin.
- Bir satış siparişindeki müşteri bir müşteri kredi grubuna dahil olduğu zaman müşteri kredi grubunun kredi limitini denetlemek için **Müşteri kredi grubunun kredi limitini denetle** seçeneğini **Evet** olarak ayarlayın. Grubun kredi limiti kontrol edilir ve yeterliyse, müşterinin kredi limiti kontrol edilir.
- Satış siparişindeki yeni ödeme koşullarının müşterinin varsayılan ödeme koşullarından farklı olup olmadığını belirlemek amacıyla ödeme koşulları derecelerini kontrol etmek için **Ödeme koşulları yükseldiği zaman kredi limitini denetle**'yi **Evet** olarak ayarlayın. Yeni ödeme koşullarının derecesi orijinal ödeme koşullarınınkinden daha yüksekse, sipariş, kredi yönetimi bekletme işlemine alınır.
- Satış siparişindeki nakit iskontosunun müşterinin varsayılan nakit iskontosundan farklı olup olmadığını belirlemek amacıyla kapatma iskontosu derecelerini kontrol etmek için **Kapatma iskontosu artırıldığı zaman kredi limitini denetle**'yi **Evet** olarak ayarlayın. Yeni nakit iskontusunun derecesi, orijinal nakit iskontusununkinden daha yüksekse, sipariş, kredi yönetimi bekletme işlemine alınır.
- **Değiştirilmiş siparişleri serbest bırakma nedeni** alanında, değiştirilen siparişler kredi yönetimi bekletmesinden otomatik olarak serbest bırakıldığında varsayılan olarak kullanılacak serbest bırakma nedenini seçin.
- **Kredi limiti süresi dolmuş** kuralının davranışını denetlemek için **Bitiş tarihi boşsa kredi limiti süresi dolduğu için durdurma kuralını yoksay** seçeneğini **Evet** yapın. Bitiş tarihi boş olduğu zaman bir siparişi durdurmak için bu seçeneği **Hayır** olarak ayarlayın.
- Ambar yönetiminde yükler satış siparişi girişi sırasında oluşturulabilir. Satış siparişi kredi bekletmedeyken satış siparişi satırlarını yükte bırakmak için **Durdurulan yük satırlarını kaldır** seçeneğini **Hayır** olarak ayarlayın. Satış siparişi bekletmedeyken yük işlenemez. Satış siparişi kredi bekletmedeyken satış siparişi satırlarını yükten kaldırmak için seçeneği **Evet** olarak ayarlayın. Bunun ardından yük işlenebilir.
- Satış siparişleri, kredi yönetimi incelemesinden otomatik olarak serbest bırakılabilir. **Otomatik olarak serbest bırakma nedeni** alanında, satış siparişleri otomatik olarak serbest bırakıldığı zaman varsayılan olarak kullanılacak serbest bırakma nedenini seçin.
- Satış siparişleri, kredi yönetimi incelemesinden otomatik olarak serbest bırakılabilir. **Otomatik olarak serbest bırak** alanında, bir siparişi beklemeden çıkarmak için **Deftere nakletmeden**'i seçin. Siparişi beklemeye alan işlemi el ile çalıştırmanız gerekir. Satış siparişi beklemeye alındığı zaman çalıştırılan deftere nakil işleminin aynısını kullanarak siparişi deftere nakletmek için **Deftere nakil ile**'yi seçin.

### <a name="credit-management-checkpoint"></a>Alacak yönetimi denetim noktası

Satış siparişlerinde kredi sorunlarını denetlemek için kullanılacak zamanlamayı ayarlayabilirsiniz. **Kredi yönetimi denetim noktası** hızlı sekmesi, kredi yönetimi kurallarının işlenmesini içeren belge deftere nakil işlemlerini tanımlar. Ayrıca, proforma deftere nakil işlemi veya satış siparişinin tam bir deftere nakli sırasında da kredi kurallarını denetleyebilirsiniz. Kredi yönetimi durdurma kuralları işlendikten sonra bir sorun bulunduğunda bir siparişi beklemeye alması gereken deftere nakil işlemlerini tanımlamak için onay kutularını seçin.

Ayrıca, kredi kuralları yeniden denetlenmeden önceki mehil gün sayısını da tanımlayabilirsiniz. Deftere nakil sırasında kredi yönetimi kurallarının denetlenmesini belirtebilseniz de, belirtilen mehil gün sayısı için kurallar denetlenmez. Örneğin, 1. gün bir satış siparişini onaylıyor ve onay adımı için mehil süresi olarak iki gün belirtiyorsunuz. Bu durumda, sonraki deftere nakil adımında (örneğin, siparişin sevk irsaliyesini oluşturma veya faturalama) 4. güne kadar kredi kuralları denetlenmez. 4. gün veya sonrasında, deftere nakil gerçekleştiği zaman kurallar denetlenir ve mehil gün sayısı, sonraki deftere nakil denetim noktası için belirtilen değere değişir.

Mehil gün sayısını belirlemezseniz, kredi yönetimi kurallarını çalıştırmak üzere ayarlanmış her deftere nakil adımında kredi kuralları denetlenir. Satış siparişini deftere nakletmeden serbest bırakırsanız ve aynı sipariş işleme adımını yeniden çalıştırırsanız, kredi kuralları yine denetlenir. Örneğin bir sipariş bir onaydan sonra beklemeye alınıyor ve bu siparişi deftere naklederek ya da nakletmeden serbest bırakıyorsunuz. Bu durumda, siparişi yeniden onaylarsanız sipariş yine beklemeye alınır. Siparişin bir sonraki işleme adımına yeniden bekletilmeksizin devam ettirilmesi gerekiyorsa mehil gün sayısını kullanın.

> [!Note]
> Bir deftere nakil denetim noktası için girilşmiş mehil gün sayısı varsa, deftere nakil için işaretlenen tüm kontrol noktalarının mehil günleri olması gerekir.

- Satırda gösterilen deftere nakil denetim noktası çalıştırıldığında kredi yönetimi kurallarını çalıştırmak için **Deftere nakil** onay kutusunu işaretleyin. Onay kutusunu işaretlemezseniz, tüm deftere nakil sürecinde kurallar yalnızca bir kez denetlenir.
- **Deftere nakil** onay kutusunu işaretlerseniz, durdurma kuralları denetlenmeden önce geçilmesi gereken mehil gün sayısını belirtin. **Deftere nakil** onay kutusu işaretsizse mehil gün sayısı ekleyemezsiniz.
- Satırda gösterilen proforma deftere nakil denetim noktası çalıştırıldığında kredi yönetimi kurallarını çalıştırmak için **Proforma** onay kutusunu işaretleyin. Çoğu durumda, bir satış siparişi deftere nakledildiğinde görüntülenen iletişim kutusunda **Deftere nakil** alanı **Hayır** olarak ayarlanır.
- **Deftere nakil** onay kutusunu işaretlerseniz, durdurma kuralları denetlenmeden önce geçilmesi gereken mehil gün sayısını belirtin. **Deftere nakil** onay kutusu işaretsizse mehil gün sayısı ekleyemezsiniz.

### <a name="credit-management-statistics"></a>Alacak yönetimi istatistikleri

**Müşteri** sayfasındaki **Müşteri kredi yönetimi istatistikleri** bilgi kutusunda çeşitli kredi yönetimi istatistikleri yer alır. Bu istatistikleri hesaplamak için gereken bazı değerleri belirtmeniz gerekir. **Müşteri kredi yönetimi istatistikleri** bilgi kutusunda aşağıdaki değerleri hesaplamak için kullanılan ay sayısını girin:

1. Bekleyen Satış Gün Sayısı 1
2. Bekleyen Satış Gün Sayısı 2
3. Ortalama bakiye 1
4. Ortalama bakiye 2
5. Ortalama kredi limiti %
6. Ortalama kapsam %

### <a name="credit-limits"></a>Alacak limitleri

- Kredi yönetiminde, müşteri kredi limiti müşterinin para birimiyle gösterilir. Müşterinin para biriminde kredi limiti için döviz kuru türünü tanımlamanız gerekir. **Kredi limiti döviz kuru türü** alanında, birincil kredi limitini müşterinin kredi limitine dönüştürmek için kullanılması gereken döviz kuru türünü seçin.
- Kullanıcıların kredi limitlerini **Müşteri** sayfasında düzenlemelerini engellemek için **Kredi limitlerinin el ile düzenlenmesine izin ver** seçeneğini **Hayır** yapın. Bu seçenek **Hayır** olarak ayarlanırsa, müşterinin kredi limitindeki değişiklikler yalnızca kredi limiti düzeltme hareketleriyle yapılabilir.
- Kredi yönetimi engelleme kuralları işaretlendiğinde stok rezervasyonlarını göz ardı etmek için **Stok rezervasyonlarını atla** seçeneğini **Evet** olarak ayarlayın. Bu durumda sistem, stok rezervasyon miktarından bağımsız olarak satır miktarlarının tamamını denetler ve denetim noktası mehil sürelerini etkinleştirir.
- Kredi yönetimi etkinleştirildiğinde, **Kredi limiti aşıldığında ileti** alanının ayarı yalnızca serbest metin faturalarını işlemek için kullanılır. Müşteriler kredi limitini aştığında iletiler yine de satış siparişlerine eklense de bu iletilerin varlığı, malzeme çekme listeleri ile sevk irsaliyelerinin onaylanıp yazdırılmasını veya faturaların deftere nakledilmesini engellemez.

    Kredi yönetimi varsayılan olarak etkindir, ancak bunu devre dışı bırakabilirsiniz. Etkinleştirildiğinde, müşterilerin kredi limitini ne zaman aştığını belirlemek için kredi yönetimi engelleme kurallarını ve denetim noktalarını kullanırsınız. Devre dışı bırakılmışsa, **Kredi limiti aşıldığında ileti** alanının ayarına bağlı olarak satış siparişlerine eklenen iletiler, müşterilerin kredi limitini ne zaman aştığını belirlemenize yardımcı olabilir.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Numara serileri ve paylaşılan numara serisi parametreleri

Kredi limiti düzeltmelerini işlemek için bir günlük kodu gereklidir. Günlük kodunu oluşturmak için kullanılması gereken kredi limiti düzeltme numarasını eklemeniz gerekir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
