---
title: Abonelik faturalamasında gelir ve gider ertelemeleri
description: Bu konuda, Abonelik faturalamasında gelir ve gider ertelemelerini ayarlama işlemi açıklanmaktadır.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 5ff8d2f4663c53bf6dece1ef9af6609d5f0c5b50
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544533"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Abonelik faturalamasında gelir ve gider ertelemeleri

Bu konuda, Abonelik faturalamasında gelir ve gider ertelemelerinin nasıl ayarlanacağı ve kullanılacağı açıklanmaktadır. Erteleme planları her zaman temeldeki kaynak belgeye veya faturalama planına dayanır ve bağlıdır. Bunlar varsayılan değerler temelinde oluşturuldukları için ayrı olarak girilemez veya oluşturulamaz.

Gelir ve gider ertelemelerinin ayarlanması ve kullanılması süreci birden fazla sayfada gerçekleşir:

- **Gelir ve gider erteleme parametreleri** sayfasında, şirket tercihlerini tanımlayabilirsiniz.
- **Erteleme varsayılan ayarları** sayfasında, erteleme planları için kullanılan varsayılan hesapları ve şablonları ayarlayabilirsiniz.
- **Erteleme şablonları** ve **Olay tabanlı erteleme şablonları** sayfalarında, erteleme planları için kullanılan şablonları tanımlayabilirsiniz.
- **Tüm erteleme planları** sayfasında, herhangi bir erteleme planını görüntüleyebilir ve düzenleyebilirsiniz.

Gelir ve gider ertelemeleri, yinelenen sözleşme faturalamasıyla birlikte kullanılabilir.

## <a name="revenue-and-expense-deferral-parameters"></a>Gelir ve gider erteleme parametreleri

**Gelir ve gider erteleme parametreleri** sayfası aşağıdaki alanları içerir.

| Alan | Açıklama |
|---|---| 
| **Plan** sekmesi | |
| Dönem başına eşit | <p>Bir erteleme planı için dönem başına tutar hesaplanırken dönemdeki gün sayısının kullanılıp kullanılmayacağını belirtin:</p><ul><li>**Evet** – Her dönemin tutarı, dönemdeki gün sayısından bağımsız olarak aynıdır. Kısmi dönemler (erteleme planının başındaki veya sonundaki dönemler gibi) eşit olarak dağıtılır.</li><li>**Hayır** – Tutar, her bir dönemdeki gün sayısına göre hesaplanır.</li></ul><p>Bu ayarı hareket düzeyinde geçersiz kılabilirsiniz.</p> |
| Satış iskontosu erteleme seçeneği | <p>İskonto ve satış siparişi tutarları için ayrı erteleme planları oluşturulup oluşturulmayacağını belirtin:</p><ul><li>**İskonto için ayrı plan** – İskonto tutarı, gelir tutarından ayrı tutulur.<p>Bu durumda, bir satış siparişi oluşturulduğunda ve ardından deftere nakledildiğinde iki erteleme planı oluşturulur. İskonto ve gelir tutarları farklı erteleme hesaplarına nakledilecektir.</p></li><li>**İskontoyu gelirle birleştir** – İskonto tutarı gelir tutarıyla birleştirilir. Bir erteleme planı oluşturulur ve hem iskonto tutarı hem de gelir tutarı aynı erteleme hesabına nakledilir.<p>Bu durumda, bir satış siparişi oluşturulduğunda ve ardından deftere nakledildiğinde bir erteleme planı oluşturulur. Hem iskonto tutarı hem de gelir tutarı aynı erteleme hesabına nakledilir.</p></li></ul><p>**Not:** Faturalanmamış gelir özelliğini kullanan maddelere iskonto uygulamak için **İskonto için ayrı plan** seçeneğini belirleyin. İskontolar daha sonra faturalanmamış gelir özelliğinin kullanılıp kullanılmadığına bakılmaksızın tüm kalemlere uygulanabilir. **İskontoyu gelirle birleştir** seçeneği işaretliyse, faturalanmamış gelir özelliğini kullanan maddelere iskontolar uygulanamaz.</p> |
| Satın alma iskontosu erteleme seçeneği | <p>İskonto ve satış alma siparişi tutarları için ayrı erteleme planları oluşturulup oluşturulmayacağını seçin:</p><ul><li>**İskonto için ayrı plan** – İskonto tutarı, gider tutarından ayrı tutulur.<p>Bu durumda, bir satın alma siparişi oluşturulduğunda ve ardından deftere nakledildiğinde iki erteleme planı oluşturulur. İskonto ve gider tutarları farklı erteleme hesaplarına nakledilecektir.</p></li><li>**İskontoyu gelirle birleştir** – İskonto tutarı gider tutarıyla birleştirilir. Bir erteleme planı oluşturulur ve hem iskonto tutarı hem de gider tutarı aynı erteleme hesabına nakledilir.<p>Bu durumda, bir satın alma siparişi oluşturulduğunda ve ardından deftere nakledildiğinde bir erteleme planı oluşturulur. Hem iskonto tutarı hem de gider tutarı aynı erteleme hesabına nakledilir.</p></li></ul> |
| Önceki dönemleri konsolide et | <p>Önceki dönemler için erteleme planı satırlarının konsolide edilip edilmeyeceğini belirtin:</p><ul><li>**Evet** – Erteleme başlangıç tarihi hareket tarihinden önceki bir dönemdeyse, hareket tarihi dönemine kadar olan tüm tutarlar tek bir erteleme planı satırında birleştirilir.</li><li>**Hayır** – Tüm dönemlere ait tutarlar ayrı erteleme planı satırlarında tutulur.<p>Erteleme başlangıç tarihi, hareket tarihiyle aynı dönemde veya daha sonraki bir dönemdeyse, bu seçeneğin bir etkisi yoktur.</p></li></ul><p>Bu ayar hareket düzeyinde güncelleştirilebilir.</p> |
| Varsayılan erteleme başlangıç tarihi | <p>Erteleme planının başlangıç tarihini belirlemek için kullanılan kuralı seçin:</p><ul><li>**Hareket tarihi** – Hareket tarihini başlangıç tarihi olarak kullanın.</li><li>**Geçerli ayın başlangıcı** – Başlangıç tarihi olarak geçerli ayın ilk gününü kullanın. Hareket tarihi herhangi bir ayın ilk günüyse geçerli ayın ilk günü başlangıç tarihidir.</li><li>**Sonraki ayın başlangıcı** – Başlangıç tarihi olarak sonraki ayın ilk gününü kullanın. Hareket tarihi ayın ilk günüyse hareket tarihi kullanılır. Aksi takdirde, bir sonraki ayın ilk günü kullanılır.</li><li>**15 Kuralı** – Hareket tarihi, ayın ilk günü ile on beşinci günü arasındaysa, başlangıç tarihi olarak geçerli ayın ilk gününü kullanın. Hareket tarihi herhangi bir ayın on altıncı günü veya daha sonraysa sonraki ayın ilk günü başlangıç tarihidir.</li></ul><p>Bu ayarı hareket düzeyinde güncelleştirebilirsiniz.</p> |
| Kısa vadeli erteleme yöntemi | <p>Kısa vadeli erteleme yöntemini seçin: **Yok**, **Dinamik dönemler** veya **Sabit yıl**.</p><p>|
| Erteleme deftere nakil yöntemi | <p>Erteleme hareketleri oluşturmak için kullanılan yöntemi seçin:</p><ul><li>**Bilanço** – Erteleme hareketleri oluşturmak için bilanço deftere nakil yöntemini kullanın.</li><li>**Kar ve zarar** – Erteleme hareketleri oluşturmak için kar ve zarar deftere nakil yöntemini kullanın. Hareketler deftere nakledildiğinde, ilk kabul ve kabul mahsup tutarlarını dengeleyen ek girişleri görmek için fatura fişini gözden geçirebilirsiniz.</li></ul> |
| Alacaktaki kar ve zararı tersine çevir | <p>**Not:** Bu alan yalnızca **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlandığında kullanılabilir.</p><p>Bir faturalama planına veya satış siparişine ters işlem, sona erdirme veya geri ödeme uygulandığında kar ve zarar tutarlarının tersine çevrilip çevrilmeyeceğini belirtin:</p><ul><li>**Evet** – Kar ve zarar tutarlarını tersine çevirin ve erteleme planına bir kredi düzeltme tutarı uygulayın.<p>Ters işlem bir faturalama döneminin ortasında gerçekleşirse, tutarlar eşit olarak dağıtılır.</p></li><li>**Hayır** – Bir faturalama planına veya satış siparişine ters işlem, sona erdirme veya geri ödeme uygulandığında kar ve zarar için tersine çevirme hareketi oluşturulmaz.</li></ul> |
| **Kabul** sekmesi | |
| Yevmiye defterlerini otomatik olarak deftere naklet | <p>Gelir ve gider ertelemeleri tarafından oluşturulan günlük girişlerinin otomatik olarak deftere nakledilip nakledilmeyeceğini belirtin:</p><ul><li>**Evet** – Gelir ve gider ertelemeleri tarafından oluşturulan günlük girişlerini otomatik olarak deftere nakledin.<p>**İpucu:** **Evet**'i seçerek, fişlerdeki el ile yapılan değişikliklerin neden olduğu hesap tutarsızlıklarını engellemeye yardımcı olabilirsiniz.</p></li><li>**Hayır** – Gelir ve gider ertelemeleri tarafından oluşturulan günlük girişleri otomatik olarak deftere nakledilmez. Günlükleri el ile deftere nakletmeniz gerekir.</li></ul> |
| Kabul günlüğünü özetle | <p>Kabul fişlerinin varsayılan olarak konsolide edilip edilmeyeceğini belirtin:</p><ul><li>**Evet** – Aynı tarihe sahip tüm kabul satırları için tek bir fiş oluşturun. Aynı hesaba sahip bir fişteki tüm satırlar tek bir satırda birleştirilir.</li><li>**Hayır** – Her kabul satırı için bir fiş oluşturun.</li></ul><p>Bu ayarı **Kabul işleme** sayfasında güncelleştirebilirsiniz.</p> |
| Varsayılan günlük adı | Kabul işlemi gibi gelir ve gider erteleme işlemlerinden oluşturulan günlükler için günlük adını seçin. |
| Kabul günlüğü satır açıklaması | <p>Günlük fiş satırı açıklamasında görüntülenecek açıklamayı seçin:</p><ul><li>**Plan satırı tarihleri** – Günlük satırı açıklamasında plan satırı tarihlerini gösterin.</li><li>**Kaynak hareket ayrıntıları** – Günlük satırı açıklamasında kaynak hareket bilgilerini gösterin.<p>**Örnek:** USMF-0001, CIV-00839, Yazılım Geliri</p></li></ul> |
| **Numara serileri** sekmesi | Kiralama numarası serilerinin varsayılan değerlerini ayarlamak için bu sekmeyi kullanın. Numara serisi oluşturma sihirbazı otomatik olarak numara serileri oluşturmak ve atamak için kullanılır. Oluşturulan numara sıralarında el ile değişiklik yapmak istemediğiniz sürece numara serisini değiştirmeniz gerekmez. |
| Plan numarası | Erteleme planları için kullanılan seri olan numara. |

## <a name="deferral-templates"></a>Erteleme şablonları

Erteleme planları için kullanılan eşit paylı şablonları tanımlamak için **Erteleme şablonları** sayfasını kullanın.

Şablon kullanmanın yararlarından bazıları şunlardır:

* Erteleme uzunluğu otomatik olarak hesaplanır.
* Kabulün atlandığı dönemler içeren erteleme planlarına olanak tanıyabilirsiniz.
* Şablonu bir ürüne, ürün grubuna, ürün kategorisine, müşterilere veya müşteri grubuna atayarak, ertelemeyi otomatikleştirebilirsiniz. Şablon ataması **Erteleme varsayılan ayarları** sayfasından gerçekleştirilir.

Şablonlar için birkaç dönem sıklığı kullanılabilir: günlük, aylık veya mali dönemler.

Şablon satırları bir tür ( **Kabul edildi** veya **Atlandı**) ve dönem uzunluğu içerir. Atlanan satırların erteleme planı satırlarında tutar olarak 0 (sıfır) yer alır. Geliri tüm dönemlerde kabul etmek istemiyorsanız, bu davranış yararlı olabilir.

### <a name="create-a-deferral-template"></a>Erteleme şablonu oluşturma

Erteleme şablonu oluşturmak için şu adımları izleyin.

1. **Erteleme şablonları** sayfasında, **Yeni**'yi seçin.
2. **Şablon** alanına bir ad girin.
3. **Açıklama** alanına bir açıklama girin.
4. **Dönem sıklığı** alanında, dönem sıklığını seçin.
5. Satırlar listesinin başına bir satır eklemek için **Ekle**'yi veya listenin en altına bir satır eklemek için **Sonuna ekle**'yi seçin.
6. **Tür** alanında dönem türünü seçin.
7. **Dönem uzunluğu** alanında, dönemin uzunluğunu belirtin.
8. Gereksinim duyduğunuz her ek satır için 5 ile 7 arasındaki adımları yineleyin.
9. **Kaydet**'i seçin.

## <a name="deferral-defaults"></a>Erteleme varsayılanları

Maddeler için varsayılan erteleme hesapları ayarlamak ve ertelenebilir maddelere varsayılan şablonlar atamak için **Erteleme varsayılan ayarları** sayfasını kullanın. Ayrıca giderler için erteleme hesapları ayarlayabilir ve ertelenebilir giderlere şablon atayabilirsiniz.

**Maddeye göre ertele**

Madde içeren hareketlerde (örneğin, satış siparişleri), belirli madde ve müşterilere hesap ve şablon atayabilirsiniz. Bir hareket ertelendiğinde bu ayarlar varsayılan değerler olarak kullanılacaktır. Hareketin varsayılan olarak ertelenmesi için, maddeleri **Ertelenebilir maddeler** sayfasında ayarlamanız gerekir.

**Hesaba göre ertele**

Maddeleri olmayan hareketler (örneğin, genel günlükler) için erteleme hesaplarını belirtebilirsiniz. Bu hesaplar bir hareket satırında kullanıldığında, hareket otomatik olarak ertelendi şeklinde işaretlenir. Karşılık gelen şablon ve kabul hesabı hareket satırına atanır.

**Tüm hareket tipleri (örneğin, Satış siparişi, Satın alma ve Yevmiye defteri sekmelerinde)**

Sayfadaki hesaplar, finansal boyutları olmayan ana hesaplardır. Kabul hesabının finansal boyutları kuruluşunuza bağlı olarak müşteriden veya maddeden alınır.

Her şablon satırının, eşit paylı bir şablonu veya olay tabanlı bir şablonu olmalıdır. Her ikisini birden içeremez.

### <a name="for-sales-orders"></a>Satış siparişleri için

Satış siparişleri için erteleme varsayılan değerlerini belirtmek için, aşağıdaki adımları izleyin.

1. **Satış siparişi** sekmesinde erteleme türünü seçin.
2. Bir satır eklemek için **Ekle**'yi seçin.
3. **Madde kodu** alanında madde kodunu seçin. Madde kodu, erteleme varsayılan değerlerinin nasıl uygulanacağını belirler.
4. Madde kodunun nasıl uygulanacağını belirtin:

    * **Madde kodu** alanı **Tablo** veya **Grup** olarak ayarlandıysa **Madde ilişkisi** alanında madde ilişkisini seçin.
    * **Madde kodu** alanı **Kategori** olarak ayarlanmışsa, **Kategori ilişkisi** alanında kategori ilişkisini seçin.
    * **Madde kodu** alanı **Tümü** olarak ayarlanırsa, varsayılan değerler uygulanabilir tüm kayıtlara uygulanır.

5. Hesap kodunun nasıl uygulanacağını belirtin:

    * **Hesap kodu** alanı **Tablo** veya **Grup** olarak ayarlandıysa **Hesap ilişkisi** alanında hesap ilişkisini seçin.
    * **Hesap kodu** alanı **Tümü** olarak ayarlanırsa, hesap tüm kayıtlara uygulanır.

6. **Ana hesap** alanında, erteleme için ana hesabı seçin.
7. **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlanmışsa, **İlk gelir hesabı** alanında başlangıçtaki gelir hesabını ve **Gelir mahsup hesabı** alanında gelir mahsup hesabını seçin.
8. **Kısa vadeli erteleme yöntemi** alanı **Dinamik dönemler** veya **Sabit yıl** olarak ayarlanmışsa, **Kısa vadeli erteleme hesabı** alanında kısa vadeli erteleme hesabını seçin.
9. Şablon için, satır eklemek üzere **Ekle**'yi seçebilirsiniz.
10. **Madde kodu** alanında madde kodunu seçin.
11. Madde kodunun nasıl uygulanacağını belirtin:

    * **Madde kodu** alanı **Tablo** veya **Grup** olarak ayarlandıysa **Madde ilişkisi** alanında madde ilişkisini seçin.
    * **Madde kodu** alanı **Kategori** olarak ayarlanmışsa, **Kategori ilişkisi** alanında kategori ilişkisini seçin.
    * **Madde kodu** alanı **Tümü** olarak ayarlanırsa, varsayılan değerler uygulanabilir tüm kayıtlara uygulanır.

12. Hesap kodunun nasıl uygulanacağını belirtin:

    * **Hesap kodu** alanı **Tablo** veya **Grup** olarak ayarlandıysa **Hesap ilişkisi** alanında hesap ilişkisini seçin.
    * **Hesap kodu** alanı **Tümü** olarak ayarlanırsa, hesap uygun tüm kayıtlara uygulanır.
    * **Eşit paylı şablon** alanında eşit paylı şablonu veya **Olay tabanlı şablon** alanında olay tabanlı şablonu seçin.

13. **Kaydet**'i seçin.

### <a name="for-purchase-orders"></a>Satın alma siparişleri için

Satın alma siparişleri için erteleme varsayılan değerlerini belirtmek için, aşağıdaki adımları izleyin.

1. **Satın alma** sekmesinde erteleme türünü seçin.
2. Bir satır eklemek için **Ekle**'yi seçin.
3. **Madde kodu** alanında madde kodunu seçin.
4. Madde kodunun nasıl uygulanacağını belirtin:

    * **Madde kodu** alanı **Tablo** veya **Grup** olarak ayarlandıysa **Madde ilişkisi** alanında madde ilişkisini seçin.
    * **Madde kodu** alanı **Kategori** olarak ayarlanmışsa, **Kategori ilişkisi** alanında kategori ilişkisini seçin.
    * **Madde kodu** alanı **Tümü** olarak ayarlanırsa, varsayılan değerler uygulanabilir tüm kayıtlara uygulanır.

5. Hesap kodunun nasıl uygulanacağını belirtin:

    * **Hesap kodu** alanı **Tablo** veya **Grup** olarak ayarlandıysa **Hesap ilişkisi** alanında hesap ilişkisini seçin.
    * **Hesap kodu** alanı **Tümü** olarak ayarlanırsa, hesap uygun tüm kayıtlara uygulanır.

6. **Ana hesap** alanında, erteleme için ana hesabı seçin.
7. **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlanmışsa, **İlk gelir hesabı** alanında başlangıçtaki gelir hesabını ve **Gelir mahsup hesabı** alanında gelir mahsup hesabını seçin.
8. **Kısa vadeli erteleme yöntemi** alanı **Dinamik dönemler** veya **Sabit yıl** olarak ayarlanmışsa, **Kısa vadeli erteleme hesabı** alanında kısa vadeli erteleme hesabını seçin.
9. Şablon için, satır eklemek üzere **Ekle**'yi seçin. 
10. **Madde kodu** alanında madde kodunu seçin.
11. Madde kodunun nasıl uygulanacağını belirtin:

    * **Madde kodu** alanı **Tablo** veya **Grup** olarak ayarlandıysa **Madde ilişkisi** alanında madde ilişkisini seçin.
    * **Madde kodu** alanı **Kategori** olarak ayarlanmışsa, **Kategori ilişkisi** alanında kategori ilişkisini seçin.
    * **Madde kodu** alanı **Tümü** olarak ayarlanırsa, varsayılan değerler uygulanabilir tüm kayıtlara uygulanır.

12. Hesap kodunun nasıl uygulanacağını belirtin:

    * **Hesap kodu** alanı **Tablo** veya **Grup** olarak ayarlandıysa **Hesap ilişkisi** alanında hesap ilişkisini seçin.
    * **Hesap kodu** alanı **Tümü** olarak ayarlanırsa, hesap uygun tüm kayıtlara uygulanır.
    * **Eşit paylı şablon** alanında eşit paylı şablonu veya **Olay tabanlı şablon** alanında olay tabanlı şablonu seçin.

13. **Kaydet**'i seçin.

### <a name="for-general-journals"></a>Yevmiye defterleri için

Yevmiye defteri girişleri için erteleme varsayılan değerlerini belirtmek için, aşağıdaki adımları izleyin.

1. **Yevmiye defteri** sekmesini seçin.
2. Erteleme için, satır eklemek üzere **Ekle**'yi seçin.
3. **Kısa vadeli erteleme yöntemi** alanı **Dinamik dönemler** veya **Sabit yıl** olarak ayarlanmışsa, **Kısa vadeli erteleme hesabı** alanında kısa vadeli erteleme hesabını seçin.
4. **Erteleme hesabı** alanında, erteleme hesabını seçin.
5. **Kabul hesabı** alanında, kabul hesabını seçin.
6. **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlanmışsa, **İlk gelir hesabı** alanında başlangıçtaki gelir hesabını ve **Gelir mahsup hesabı** alanında gelir mahsup hesabını seçin.
7. **Eşit paylı şablon** alanında eşit paylı şablonu veya **Olay tabanlı şablon** alanında olay tabanlı şablonu seçin.
8. **Kaydet**'i seçin.

### <a name="for-free-text-invoices"></a>Serbest metin faturaları için

Serbest metin faturaları için erteleme varsayılan değerlerini belirtmek için, aşağıdaki adımları izleyin.

1. **Serbest metin faturası** sekmesini seçin.
2. Erteleme için, satır eklemek üzere **Ekle**'yi seçin.
3. Hesap kodunun nasıl uygulanacağını belirtin:

    * **Hesap kodu** alanı **Tablo** veya **Grup** olarak ayarlandıysa **Hesap ilişkisi** alanında hesap ilişkisini seçin.
    * **Hesap kodu** alanı **Tümü** olarak ayarlanırsa, hesap kodu uygun tüm kayıtlara uygulanır.

4. **Erteleme hesabı** alanında, erteleme hesabını seçin.
5. **Kısa vadeli erteleme yöntemi** alanı **Dinamik dönemler** veya **Sabit yıl** olarak ayarlanmışsa, **Kısa vadeli erteleme hesabı** alanında kısa vadeli erteleme hesabını seçin.
6. **Kabul hesabı** alanında, kabul hesabını seçin.
7. **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlanmışsa, **İlk gelir hesabı** alanında başlangıçtaki gelir hesabını ve **Gelir mahsup hesabı** alanında gelir mahsup hesabını seçin.
8. **Eşit paylı şablon** alanında eşit paylı şablonu veya **Olay tabanlı şablon** alanında olay tabanlı şablonu seçin.
9. **Kaydet**'i seçin.

### <a name="for-invoice-journals"></a>Satıcı günlükleri için

Fatura günlüğü girişleri için erteleme varsayılan değerlerini belirtmek için, aşağıdaki adımları izleyin.

1. **Fatura günlüğü** sekmesini seçin.
2. Erteleme için, satır eklemek üzere **Ekle**'yi seçin.
3. Hesap kodunun nasıl uygulanacağını belirtin:

    * **Hesap kodu** alanı **Tablo** veya **Grup** olarak ayarlandıysa **Hesap ilişkisi** alanında hesap ilişkisini seçin.
    * **Hesap kodu** alanı **Tümü** olarak ayarlanırsa, hesap kodu uygun tüm kayıtlara uygulanır.

4. **Erteleme hesabı** alanında, erteleme hesabını seçin.
5. **Kısa vadeli erteleme yöntemi** alanı **Dinamik dönemler** veya **Sabit yıl** olarak ayarlanmışsa, **Kısa vadeli erteleme hesabı** alanında kısa vadeli erteleme hesabını seçin.
6. **Kabul hesabı** alanında, kabul hesabını seçin.
7. **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlanmışsa, **İlk gelir hesabı** alanında başlangıçtaki gelir hesabını ve **Gelir mahsup hesabı** alanında gelir mahsup hesabını seçin.
8. **Eşit paylı şablon** alanında eşit paylı şablonu veya **Olay tabanlı şablon** alanında olay tabanlı şablonu seçin.
9. **Kaydet**'i seçin.

### <a name="items-that-are-deferred-by-default"></a>Varsayılan olarak ertelenen maddeler

Varsayılan olarak hangi maddelerin ertelenmiş olduğunu tanımlamak için **Varsayılan olarak ertelenen maddeler** sayfasını kullanın. Maddelerin hangi hareket tiplerinde erteleneceğini ayarlayabilirsiniz. Tek bir maddenin ertelenmesini veya bir madde grubunun veya kategorinin tamamının ertelenmesini belirtebilirsiniz.

Maddeleri ertelenen olarak ayarladığınızda, **Erteleme varsayılan ayarları** sayfasında varsayılan hesapları ve şablonları seçin. Hesaplar ve şablonlar seçilmezse, bu maddelerin girildiği hareket satırları ertelenmez.

İlişkili oldukları satış veya satın alma kategorisine göre ertelenen maddeler için erteleme ayarları kategoriye dayanır. Ancak **Kategori ilişkisi** alanında kategori seçilmemişse, daha üst dereceli kategorinin erteleme ayarları kullanılır. Örneğin, bir **Ev videosu** satış kategorisi ekliyor ancak **Televizyon** satış kategorisi eklemiyorsunuz. **Televizyon** kategorisiyle ilişkilendirilmiş bir erteleme öğesi eklediğinizde, bu madde için **Ev videosu** kategorisinin erteleme ayarları kullanılır.

### <a name="set-up-deferred-items"></a>Ertelenen maddeleri ayarlama

Varsayılan olarak ertelenen maddeleri ayarlamak için, aşağıdaki adımları izleyin.

1. **Varsayılan olarak ertelenen maddeler** sayfasında, istediğiniz sekmeyi seçin: **Satış siparişi** veya **Satın alma**.
2. Bir satır eklemek için **Ekle**'yi seçin.
3. **Madde kodu** alanında madde kodunu seçin.
4. Madde kodunun nasıl uygulanacağını belirtin:

    * **Madde kodu** alanı **Grup** veya **Tablo** olarak ayarlandıysa **Madde ilişkisi** alanında madde ilişkisini seçin.
    * **Madde kodu** alanı **Kategori** olarak ayarlanmışsa, **Kategori ilişkisi** alanında kategori ilişkisini seçin.

5. Gereksinim duyduğunuz her ek satır için 2 ile 4 arasındaki adımları yineleyin.
6. **Kaydet**'i seçin.

## <a name="deferred-charges"></a>Ertelenen giderler

Varsayılan olarak hangi giderlerin ertelenmiş olduğunu belirtmek için **Erteleme masrafları** sayfasını kullanın.

> [!NOTE]
> * Şu anda, ertelenebilir masraflar yalnızca satış siparişleri için kullanılabilir.
> * Masraflar yalnızca satır düzeyinde ertelenebilir. Bir masrafı satış siparişi başlığı düzeyinde ertelemek için, masrafı satış siparişindeki ayrı bir satırda ertelenen madde olarak ayarlayabilirsiniz.
> * Ücretsiz metin faturası için bir masrafı ertelemek amacıyla, masrafı ayrı bir ertelenen fatura satırı olarak girmeniz gerekir.
> * Bu işlevsellik destek ücretleri ve gelir bölme işlevleri için kullanılamaz.

### <a name="set-up-deferred-charges"></a>Ertelenen masrafları ayarlama

Ertelenen masrafları ayarlamak için bu adımları izleyin.

1. **Erteleme masrafları** sayfasında satır eklemek için **Ekle**'yi seçin.
2. **Masraf kodu** alanında masraf kodunu seçin.
3. **Masraf ilişkisi** alanında masraf ilişkisini seçin.
4. Gereksinim duyduğunuz her ek satır için 1 ile 3 arasındaki adımları yineleyin.
5. **Kaydet**'i seçin.

## <a name="event-based-deferral-templates"></a>Olay tabanlı erteleme şablonları

Erteleme hareketlerinde kullanabileceğiniz ve **Erteleme varsayılan ayarları** sayfasında atayabileceğiniz olay tabanlı erteleme şablonlarını tanımlamak için **Olay tabanlı erteleme şablonları** sayfasını kullanın.

### <a name="create-an-event-based-template"></a>Olay tabanlı şablon oluşturma

Olay tabanlı erteleme şablonu oluşturmak için aşağıdaki adımları izleyin.

1. **Olay tabanlı erteleme şablonları** sayfasında, **Yeni**'yi seçin.
2. **Şablon** alanına, şablon için benzersiz bir ad girin.
3. **Açıklama** alanına bir açıklama girin.
4. **Tahsisat türü** alanında tahsisat türünü seçin:

    * **Değişken tutar** – Girilen her satır için belirli bir tutar tahsis edin.
    * **Eşit tutar** – Girilen her satır için aynı tutarı tahsis edin. 
    * **Yüzde** – Her satır için girilen yüzde değerine dayanan bir tutar tahsis edin.
    * **Tamamlanma yüzdesi** – Girilen her satır için toplam tamamlanma değeri tahsis edin.
    * **Değişken miktar** – Girilen her satır için belirli bir miktar tahsis edin.

5. Her bir olay satırının, fatura hareketindeki birim sayısına göre eşit olarak bölünmesini istiyorsanız, **Her birim için ayrı olaylar oluştur** seçeneğini **Evet** olarak ayarlayın. Olay satırlarını ayırmak istemiyorsanız **Hayır** olarak ayarlayın.
6. **Sona erme hesabı** alanında, sona erme hesabını seçin.
7. Satırlar listesinin başına bir satır eklemek için **Ekle**'yi veya listenin en altına bir satır eklemek için **Sonuna ekle**'yi seçin.
8. **Açıklama** alanında olay için bir açıklama girin.
9. **Tahsisat türü** alanı **Yüzde** olarak ayarlandıysa **Tahsisat yüzdesi** alanında tahsisat yüzdesini belirtin. Yüzde, 0 (sıfır) ile 100 arasında olmalıdır. **Tahsisat yüzdesi** alanını boş bırakırsanız, yüzde 0 olarak kabul edilir. Tüm yüzdelerin toplamı, sayfanın en altındaki **Toplam yüzde** alanında gösterilir ve bu değer 100'e eşit olmalıdır.
10. **Sona erme tarihine kalan ay sayısı** alanında, olayın geçerli olduğu ay sayısını belirtin. Hareket ertelemesindeki sona erme tarihi, bu değere dayanarak otomatik olarak girilir.
11. Hareket deftere nakledildiğinde, geliri otomatik olarak kabul etmek için **Deftere nakledildiğinde kabul et** onay kutusunu seçin. Onay kutusunu işaretli bırakırsanız, gelir el ile kabul edilmelidir.
12. Olay, tüm erteleme planında farklı bir hesap kullanıyorsa, **Kabul hesabı** alanında olaya ait kabul hesabını seçin. Bu alan, **Deftere nakledildiğinde kabul et** onay kutusu ile birlikte kullanılır.
13. Gereksinim duyduğunuz her ek satır için 7 ile 12 arasındaki adımları yineleyin.
14. **Kaydet**'i seçin.
