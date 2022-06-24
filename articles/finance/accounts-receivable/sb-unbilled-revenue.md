---
title: Faturalanmamış gelir
description: Bu makalede, Abonelik faturalamasında madde ve hesapların faturalandırılmamış gelir özelliğini kullanmak üzere nasıl ayarlanacağı açıklanmaktadır.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: b3fe58fc06df3f61433c8457b337ae895283e12b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879696"
---
# <a name="unbilled-revenue"></a>Faturalanmamış gelir

Bu makalede, tüm ödeme zamanlamalarına ait tutarları bilançoya dahil etmenize olanak sağlayan faturalanmamış gelir özelliği açıklanmıştır. Bu tutarlar, faturalandırılmamış gelir hesabına ve faturalandırılmamış gelir mahsup hesabına dahil edilir ve sözleşme taksitli olarak faturalandırılır.

## <a name="set-up-unbilled-revenue"></a>Faturalanmamış gelir ayarlama

Faturalanmamış gelir ayarlamak için bu adımları izleyin.

- **Yinelenen sözleşme fatura parametreleri** sayfasında, **Faturalanmamış gelir** bölümünde alanları ayarlayın.
- Faturalanmamış gelir özelliği, **Madde türü** alanının **Standart** olarak ayarlandığı maddeler için kullanılabilir. Ayrıca, bunlar erteleme maddeleri için de kullanılabilir. Kısa dönemli işlevlerle faturalanmamış geliri kullanmak için, **Yinelenen sözleşme faturalama parametreleri** sayfasında kısa dönemli seçenekleri ayarlayın.

Faturalanmamış gelir için kullanılacak maddeleri ayarlamak için bu adımları izleyin.

1. **Faturalanmamış gelir kurulumu** sayfasında, **Maddeler** sekmesinde, **Ekle**'yi seçin.
2. Yeni satırda, **Madde kodu** alanında madde kodunu seçin.
3. **Madde ilişkisi** alanında madde ilişkisini seçin.
4. Daha fazla satır eklemek için bu adımları tekrarlayın.
5. **Kaydet**'i seçin.

Maddeler ve faturalanmamış gelir hesaplarını kurmak için bu adımları izleyin.

1. **Faturalanmamış gelir kurulumu** sayfasında, **Hesaplar** sekmesinde, **Ekle**'yi seçin.
2. Yeni satırda, **Madde kodu** alanında madde kodunu seçin.
3. **Madde ilişkisi** alanında madde ilişkisini seçin.
4. Faturalanmamış gelir, faturalanmamış iskonto ve faturalanmamış gelir mahsubu için hesapları seçin. Kısa vadeli hesapları kullanmak için, **Yinelenen sözleşme faturalama parametreleri** sayfasında, **Kısa vadeli faturalanmamış yöntem** alanını **Yuvarlama dönemleri** veya **Sabit yıl** olarak ayarlamalısınız.
5. Daha fazla satır eklemek için bu adımları tekrarlayın.
6. **Kaydet**'i seçin.

## <a name="use-unbilled-revenue"></a>Faturalanmamış gelir kullanma

1. **Tüm faturalama zamanlamaları** sayfasında, bir fatura planı oluşturun.
2. Madde henüz faturalanmamış geliri kullanacak şekilde ayarlanmamışsa, fatura zamanlaması satırında **Faturalanmamış gelir** onay kutusunu seçin.
3. **Faturalanmamış gelir** seçeneğinde **Evet**'i işaretleyin. Ardından faturalanmamış gelir, faturalanmamış iskonto ve faturalanmamış gelir mahsubu hesaplarını gerektiği şekilde inceleyip düzenleyin.
4. Faturalama planında, **Faturalanmamış gelir işleminin** altında , faturalanmayan gelir için başlangıç günlük girişi oluşturmak üzere **Günlük girişi oluştur** seçeneğini belirleyin. Ödeme çizelgesi faturalanmadan önce bu adımın tamamlanması gerekir.
5. İlk günlük girişi oluşturulduktan sonra, satış siparişleri oluşturmak için **Fatura oluştur**'u seçin ve faturalama zamanlamalarına ait faturaları deftere nakledin.
6. Faturalar deftere nakledildikten sonra, **Tüm faturalama zamanlamaları** sayfasındaki **Yenilemeler** sekmesinde bulunan denetim bilgilerini gözden geçirebilirsiniz.

### <a name="milestone-billing"></a>Aşama bazında faturalama

Aşama bazında faturalama faturalanmamış gelirle aşağıdaki koşullarda çalışır:

- Kilometre taşı üst maddesi faturalanmadığı takdirde ( **Faturalanmamış gelir** onay kutusu seçili) ve kilometre taşı alt maddeleri faturalandı ( **Faturalanmamış gelir** onay kutusu temizlenmiştir), ana maddenin başlangıç ve bitiş tarihleri belirtilmelidir. Bu tarihler, ilk günlük girişini oluşturmak için kullanılır.
- Kilometre taşı üst maddesi faturalanmadığı takdirde ( **Faturalanmamış gelir** onay kutusu seçili) ve kilometre taşı alt maddeleri faturalandı ( **Faturalanmamış gelir** onay kutusu seçili), yalnızca ilk günlük girişini oluşturmak istediğiniz alt maddeler için son tarih belirtilmelidir.

Her kilometre taşı alt öğesi ayrı olarak işlenebilir. Bitiş tarihleri, ilk günlük girişini oluşturmaya hazır olduğunuzda belirtilebilir.

> [!NOTE]
> Kilometre taşı ana maddesinin veya alt öğelerinin ilk günlük girişi zaten oluşturulmuşsa veya bir fatura oluşturulmuşsa, başlangıç ve bitiş tarihleri düzenlenemez.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Sabit amortisman erteleme ile faturalanmamış gelir

Faturalanmış olmayan geliri, düz çizgi erteleme zamanlamalarıyla kullanmak için aşağıdaki adımları izleyin.

1. **Tüm faturalama zamanlamaları** sayfasında, bir fatura planı oluşturun.
2. Faturalama satırına bir madde ekleyin.
3. Satır için **Ertelemeler**'i seçin.
4. **Hareket ertelemesi** sayfası üzerinde, aşağıdaki adımları izleyin:

    1. **Ertelenmiş** seçeneğini **Evet** olarak ayarlayın.
    2. Hesapları gerekli şekilde değiştirin.
    3. **Zamanlama** bölümünde, **Düz satır**'ı seçin ve diğer değerleri gerekli şekilde düzenleyin.
    4. **Tamam**'ı seçin.

5. Satır için **Faturalanmamış gelir**'i seçin ve şu adımları izleyin:

    1. **Faturalanmamış gelir** seçeneğinde **Evet**'i işaretleyin.
    2. Gelir, iskonto ve gelir mahsubu için kullanılacak hesapları seçin.

6. Faturalama planında, **Faturalanmamış gelir işleminin** altında, **Günlük girişi oluştur**'u seçin. Alternatif olarak, günlük girişi oluşturmak için **Faturalanmamış gelir toplu işlem** sayfasını kullanın.
7. Erteleme zamanlaması oluşturuldu. Ayrıntıları, **Tüm erteleme planları** sayfasında görüntüleyebilirsiniz. Erteleme zamanlaması oluşturulduktan sonra, fatura zamanlama satırı maddesi için çeşitli değerleri düzenleyebilirsiniz. Örneğin, birim fiyatı, miktarı veya tarihleri düzenleyebilirsiniz.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Olay tabanlı erteleme ile faturalanmamış gelir

Faturalanmış olmayan geliri, olay tabanlı zamanlamalarıyla kullanmak için aşağıdaki adımları izleyin.

1. **Tüm faturalama zamanlamaları** sayfasında, bir fatura planı oluşturun.
2. Faturalama satırına bir madde ekleyin.
3. Satır için **Ertelemeler**'i seçin.
4. **Hareket ertelemesi** sayfası üzerinde, aşağıdaki adımları izleyin:

    1. **Ertelenmiş** seçeneğini **Evet** olarak ayarlayın.
    2. Hesapları gerekli şekilde değiştirin.
    3. **Zamanlama** bölümünde, **Olay tabanlı**, **Şablon**, **Tahsisat türü** ve **Sona erme hesabı**'nı seçin.
    4. **Tamam**'ı seçin.

5. Satır için **Faturalanmamış gelir**'i seçin ve şu adımları izleyin:

    - **Faturalanmamış gelir** seçeneğinde **Evet**'i işaretleyin.
    - Gelir, iskonto ve gelir mahsubu için kullanılacak hesapları seçin.

6. Faturalama planında, **Faturalanmamış gelir işleminin** altında, **Günlük girişi oluştur**'u seçin. Alternatif olarak, günlük girişi oluşturmak için **Faturalanmamış gelir toplu işlem** sayfasını kullanın.
7. Erteleme zamanlaması oluşturuldu. Ayrıntıları, **Tüm erteleme planları** sayfasında görüntüleyebilirsiniz. Erteleme zamanlaması oluşturulduktan sonra, fatura zamanlama satırı maddesi için çeşitli değerleri düzenleyebilirsiniz. Örneğin, birim fiyatı, miktarı veya tarihleri düzenleyebilirsiniz. Erteleme zamanlaması yeni değerlere göre yeniden hesaplanır.

Dağıtımlar, seçilen tahsisat türüne göre yeniden hesaplanır (**Yüzde**, **Yüzde tamamlama** veya **Eşit tutarlar**). **Değişken tutarlar** tahsisat türü için, olayın başlangıç değerinin yüzde olarak eşdeğeri temel alınarak, dağıtım yeniden hesaplanır. Örneğin, orijinal birim fiyatı $100,00 başlangıç değerinin yüzdesi ise $55,00'tir (yüzde 55). Birim Fiyat $200,00 olarak değiştirilirse, olayın değişken tutarı $110,00 olur (yine de yüzde 55).

> [!NOTE]
> Erteleme zamanlama satırları tanınırsa, faturalama çizelgesi satır maddesi düzenlenemez. Satır maddesini düzenlemek için önce kabul ettiğiniz satırları ters çevirmeniz gerekir. Fatura planı satırları ardından güncelleştirilebilir.

### <a name="unbilled-revenue-and-top-billing"></a>Faturalanmamış gelir ve üst ödeme

Üç yıl için bir faturalama planı girilir ve faturalar üç yıllık bir dönem içinde yıllık olarak faturalandırılır. Tüm sözleşme tutarı, yıllık faturaların oluşturulduğu faturalanmamış gelir hesabına kaydedilir. Mahsup hesap gelir veya ertelenen gelir hesabıdır.

Genel muhasebede mutabakat sorunları oluşamadığından, en iyi faturalama ve faturalanmamış gelir birlikte çalışmaz. Örneğin, **Madde grubu kurulumu** sayfasında, madde grubu A, **Üst satır sayısı** alanı **2** olarak ayarlanmış şekilde ayarlanır. **Faturalama zamanlamaları** sayfasında, üç madde eklenir. Her üç madde de A madde grubuna aittir. İlk günlük girişi faturalanmamış gelir özelliği için oluşturulduğunda, tüm üç maddeyle ilgili tutar faturalanan hesaba geri işlenir. Faturalama çizelgesi için fatura oluşturulduğunda, yalnızca en üstteki iki maddenin tutarları dahil edilir. Bu nedenle, fatura tutarı faturalanmamış gelir hesabına işlenmiş olan tutarla eşleşmiyor ve mutabakat sorunları genel muhasebede ortaya çıkar.

Faturalanmış olmayan geliri kullanmak istiyorsanız, **Madde grubu kurulum** sayfasını boş bırakın veya tüm madde gruplarını, **Üst satır sayısı** alanı **0** (sıfır) ayarlamak için ayarlayın. En iyi faturalamayı kullanmak istiyorsanız, faturalanmayan gelir eylemleri yok demektir.

### <a name="examples"></a>Örnekler

Sürüm 10.0.27 itibariyle, faturalanmış olmayan gelir kullanıldığında yeni bir hesap ortaya çıkar. İlk **Günlük oluşturma girişi** işlemi deftere nakledildiğinde, alacak yeni faturalanmamış gelir mahsup hesabıyla gerçekleştirilir. Ödeme planı faturalandığında aynı değerin ters çevrilmesi gerektiğinden, gelir hesabı yerine bu hesap kullanılır. Döviz kuru veya yuvarlama farkları oluşursa, **Fatura oluştur** işlemi sırasında hesaplanan tutarlar farklı olabilir. Bu davranış, hesapların net tutarının 0 (sıfır) olmasını sağlar.

Bu örnek, bilançodaki bir sözleşmenin tüm tutarını faturalanmamış gelir olarak tanımak için faturalanmamış gelirin nasıl kullanılacağını gösterir. Girişin diğer tarafı faturalanmamış gelir farkıdır. Müşteriyi faturaladığınızda, faturalanmamış gelir ve faturalanmamış gelir farkı ters çevrilir. Gelir kabulü, faturalama sırasında veya ayarlanan erteleme kabulünün zamanlamasına göre gerçekleştirilir.

#### <a name="assumptions"></a>Varsayımlar

- Bir müşteri, geçerli yılın 1 Ocak tarihinde $390 için üç yıllık sözleşmeyi imzalar.
- Sözleşmede iki parça vardır: lisanslar ve bir bakım anlaşması.
- Lisans masrafına ait satış fiyatı $300'dır, müşteri her sözleşme yılında 1 Ocak'ta $100 faturalanacaktır. $300 lisans ücreti, sözleşme imzalandığında gelir olarak alınacaktır.
- Bakım masrafına ait satış fiyatı $90'dır, müşteri her sözleşme yılında 1 Ocak'ta $30 faturalanacaktır. $90 bakım ücreti ertelenir ve sözleşmenin ömrünün her ay $2,50 tanınacaktır.
- Müşteri, sözleşmenin üç yıllık başlangıcında (1 Ocak) $130 faturalanacaktır.

#### <a name="steps"></a>Adımlar

1. Serbest bırakılmış iki maddeyi faturalanmamış olarak ayarlayın. Faturalanmamış geliri kullanan maddeleri ve hesapları ayarlamak için **Faturalanmamış gelir kurulumu** sayfasını kullanın.
2. Bu örnekte, bakım ücreti ertelenir. Bu öğe, **Erteleme şablonları** sayfasında ayarlanmış olan erteleme şablonunu gerektirir. Şablonda **Aylık** dönem sıklığı ve tanınma dönemi uzunluğu olarak 36 ay vardır. Böylece, ay başı gelir $2,50'dir.
3. **Varsayılan olarak ertelenen maddeler** sayfasında, **Bakım ücreti** alanını **Ertelenebilir madde** olarak ayarlayın. Bu adım ve sonraki, satılan veya bir ödeme planına dahil olan bakım harcı maddesinin ertelenebilir.
4. **Erteleme varsayılanları** \> **Şablon** öğesini seçin ve ardından bakım ücreti için maddeyi ve adım 2'deki düz satır şablonunu ekleyin. Bakım ücreti maddesi 36 aylık erteleme zamanlamasına bağlıdır.
5. Faturalanmamış iki maddeyi içeren bir ödeme planı oluşturun. Sözleşmeye ilişkin faturalama planı aşağıdaki maddelerle ayarlanır.

    | Öğe | Başlangıç tarihi | Bitiş tarihi | Tutar | Faturalama sıklığı | Erteleme maddesi | Faturalanmamış gelir | Açıklama |
    |---|---|---|---|---|---|---|---|
    | Lisans | 01 Ocak, CY | 31 Aralık CY + 2 | $100,00 | Yıllık | No. | Evet | Müşteri her yıl $100,00 faturalanacaktır. Toplam $300,00 bilançoya fatura bakiyesi olarak, kar ve zarar üzerinde gelir olarak önceden faturalandı olarak kaydedilir. Her fatura faturalanmayan tutarı azaltacaktır. |
    | Bakım | 01 Ocak, CY | 31 Aralık CY + 2 | $30,00 | Yıllık | Evet | Evet | Müşteri her yıl $30,00 faturalanacaktır. Toplam $90,00, en baştan faturalanmamış gelir olarak kaydedilecektir ve bilançoda ertelenmiş gelir olacaktır. Her fatura faturalanmayan tutarı azaltacaktır. Ertelenen gelir 36 ay içinde aylık olarak tanınacak. |

6. **Tüm faturalama zamanlamaları** sayfasında, sözleşme değerini bilançoya faturalanmış olmayan gelir olarak deftere nakletmek için **Günlük girişi oluştur** işlemini kullanın.

Faturalama planında her bir satır için bir tane olmak üzere iki günlük girişi oluşturulur.

| Faturalanmamış gelir hesabı | Faturalandırılmamış gelir mahsup hesabı | Borç tutarı | Alacak tutarı |
|---|---|---|---|
| Faturalanmamış gelir hesabı | | $300,00 | |
| | Faturalandırılmamış gelir mahsup hesabı | | $300,00 |

| Faturalanmamış gelir hesabı | Ertelenmiş gelir | Borç tutarı | Alacak tutarı |
|---|---|---|---|
| Faturalanmamış gelir hesabı | | $90,00 | |
| |Ertelenmiş bakım geliri | | $90,00 |

İlk günlük girişi faturalanmayan bir gelir mahsup hesabına nakledilir ve ikincisi ertelenen gelir hesabına nakledilir. Faturalama satırında hem faturalanmamış gelir hem de ertelenen gelir varsa, faturalanmamış gelir farkı değil, ertelenen gelir hesabı kullanılır. Sözleşme, müşterinin faturasının her yılın başlangıcında oluşturulmasını gerektirir. Faturayı oluşturmak için **Fatura oluştur** işlemini kullanın. Fatura oluşturulduğunda, aşağıdaki günlük girişleri oluşturulur.

| Ana hesap | Faturalanmamış gelir hesabı | Borç tutarı | Alacak tutarı |
|---|---|---|---|
| Faturalandırılmamış gelir mahsubu | | $100,00 | |
| | Faturalanmamış gelir hesabı | | $100,00 |
| Alacak hesapları | | $100,00 | |
| | Gelir hesabı | | $100,00 |

| Ana hesap | Faturalanmamış gelir hesabı | Borç tutarı | Alacak tutarı |
|---|---|---|---|
| Ertelenen bakım geliri hesabı | | $30,00 | |
| | Faturalanmamış gelir hesabı | | $30,00 |
| Alacak hesapları | | $30,00 | |
| | Ertelenen bakım geliri hesabı | | $30,00 |

Bu günlük girişi, sonraki iki yılın başlangıcında deftere nakledilen faturalar tarafından oluşturulacak. Yuvarlama veya döviz kuru farkı olmadığından, ertelenen gelir hesabının net tutarı 0 (sıfır) olacaktır. Ertelenen gelir tam olarak, **Günlük girişi oluşturma** sırasında alacaklandırıldığı için ters çevrilmelidir. Gelir ertelenmeye devam edildiğinden ve daha sonra tanınabilmeleri için, ertelenen gelir hesabına yapılan alacak yeniden gerçekleşir.

Son adımda, ertelenmiş bakım ücreti gelirini tanımak için her ay tanıma günlüğü girişi oluşturulur. Günlük girişi, **Tanıma işleme** sayfası kullanılarak oluşturulabilir. Alternatif olarak, **Erteleme zamanlama** sayfalarındaki satırların **Tanınması** seçilerek de oluşturulabilir.

| Ertelenen gelir hesabı | Gelir hesabı | Borç tutarı | Alacak tutarı |
|---|---|---|---|
| Ertelenmiş Bakım Geliri | | $2,50 | |
| | Bakım Geliri | | $2,50 |

Bu ertelenmiş madde (Toplam 36 defa) için tanınma süreci her çalıştırıldığında bu günlük girdisi oluşturulur.

#### <a name="short-term-fixed-year"></a>Kısa vadeli: Sabit yıl

**Yinelenen sözleşme faturalama parametreleri** sayfasında **Kısa vade faturalanmamış** alanını ayarlayarak faturalanmamış gelir özelliğini kısa vade özelliği ile birlikte kullanabilirsiniz. Aşağıdaki örnek, faturalanmamış gelir **Sabit yıl** kısa vadeli faturalandırılma yöntemiyle birlikte kullanıldığında yapılan hesaplamaları gösterir.

Aşağıdaki ölçütlere sahip bir faturalama zamanlaması oluşturulur:

- **Başlangıç Tarihi:** 1 Haziran 2020
- **Bitiş Tarihi:** 31 Aralık 2021
- **Birim Fiyatı:** $100
- **Sıklık:** Aylık

**Tüm faturalama zamanlamaları** sayfasında, ilk günlük girişi, **Günlük girişi oluşturma** işlemi tarafından oluşturulur. Geçerli kısa vadeli ve uzun dönemli tutarlar aşağıdaki şekilde hesaplanır:

- **Geçerli kısa dönemli faturalanmamış gelir tutarı:** $700
- **Geçerli uzun dönemli faturalanmamış gelir tutarı:** $1.200

Fatura, 1 Haziran 2020 ile 30 Kasım 2020 tarihinden itibaren ödeme dönemi için oluşturulur. Geçerli kısa vadeli ve uzun dönemli tutarlar aşağıdaki şekilde hesaplanır:

- **Geçerli kısa dönemli faturalanmamış gelir tutarı:** $100
- **Geçerli uzun dönemli faturalanmamış gelir tutarı:** $1.200

Fatura, 1 Aralık 2020 ile 31 Aralık 2020 tarihinden itibaren ödeme dönemi için oluşturulur. Geçerli kısa vadeli ve uzun dönemli tutarlar aşağıdaki şekilde hesaplanır:

- **Geçerli kısa dönemli faturalanmamış gelir tutarı:** $1.200
- **Geçerli uzun dönemli faturalanmamış gelir tutarı:** $0

#### <a name="short-term-rolling-periods"></a>Kısa vadeli: Yuvarlama dönemleri

**Yinelenen sözleşme faturalama parametreleri** sayfasında kısa vade faturalanmamış alanını ayarlayarak faturalanmamış gelir özelliğini kısa vade özelliği ile birlikte kullanabilirsiniz. Aşağıdaki örnek, faturalanmamış gelir **Yuvarlama dönemleri** kısa vadeli faturalandırılma yöntemiyle birlikte kullanıldığında yapılan hesaplamaları gösterir.

Aşağıdaki ölçütlere sahip bir faturalama zamanlaması oluşturulur:

- **Başlangıç Tarihi:** 1 Haziran 2020
- **Bitiş Tarihi:** 31 Aralık 2021
- **Birim Fiyatı:** $100
- **Sıklık:** Aylık

**Tüm faturalama zamanlamaları** sayfasında, ilk günlük girişi, **Günlük girişi oluşturma** işlemi tarafından oluşturulur. Geçerli kısa vadeli ve uzun dönemli tutarlar aşağıdaki şekilde hesaplanır:

- **Geçerli kısa dönemli faturalanmamış gelir tutarı:** $1.200
- **Geçerli uzun dönemli faturalanmamış gelir tutarı:** $700

Fatura, 1 Haziran 2020 ile 30 Kasım 2020 tarihinden itibaren ödeme dönemi için oluşturulur. Geçerli kısa vadeli ve uzun dönemli tutarlar aşağıdaki şekilde hesaplanır:

- **Geçerli kısa dönemli faturalanmamış gelir tutarı:** $1.200
- **Geçerli uzun dönemli faturalanmamış gelir tutarı:** $100

Fatura, 1 Aralık 2020 ile 31 Aralık 2020 tarihinden itibaren ödeme dönemi için oluşturulur. Geçerli kısa vadeli ve uzun dönemli tutarlar aşağıdaki şekilde hesaplanır:

- **Geçerli kısa dönemli faturalanmamış gelir tutarı:** $1.200
- **Geçerli uzun dönemli faturalanmamış gelir tutarı:** $0

### <a name="items-with-revenue-allocation"></a>Gelir tahsisatı olan maddeler

Faturalama planına farklı faturalama sıklıkları olan iki madde eklenir. Her ikisi de faturalanmış olmayan geliri kullanır ve bu maddeler ertelenebilirdir.

- **Madde numarası 1000:** Surface Pro 128GB

    - **Faturalama sıklığı:** Bir sefer
    - **Birim fiyatı:** $1.500
    - **Tek başına satış fiyatı:** $1.600
    - **Sözleşme geliri:** $1.465,26

- **Madde numarası S0021:** Madde numarası 1000 ile birlikte satılan sigorta

    - **Faturalama sıklığı:** 12 ay boyunca aylık
    - **Birim fiyatı:** Ay başına $20
    - **Tek başına satış fiyatı:** $25
    - **Sözleşme geliri:** $264,74

Her iki madde de faturalanmamış gelir ve gelir tahsisatı kullandığından, yenileme satırındaki toplam sözleşme tutarı 0'dır (sıfır). **Sözleşme geliri** sütunu eklenir ve sözleşmenin gelir tutarını gösterir.

Aşağıdaki tabloda, maddeler ve faturayla ilgili ilk günlük girişi gösterilmektedir.

| Faturalanmamış gelir hesabı | Ertelenen gelir hesabı | Borç tutarı | Alacak tutarı |
|---|---|---|---|
| **Madde 1000 günlük girişi** | | | |
| Borç faturalanmamış gelir hesabı ayarları (401250) | | $1.465,26 | |
| | Alacak ertelenen gelir hesabı (250600) | | $1.465,26 |
| **Madde 0021 Günlük girişi** | | | |
| Borç faturalanmamış gelir hesabı ayarları (401250) | | $274,74 | |
| | Alacak ertelenen gelir hesabı (250600) | | $274,74 |
| **Fatura** | | | |
| | Alacak faturalanmamış gelir hesabı | | $1.465,26 |
| | Alacak faturalanmamış gelir hesabı | | $274,74 |
| Borç AR hesabı (130100) | | $1.488,16 | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Ödeme çizelgesi satırında, fatura ayrıntısı satırında veya gelir tahsisatına ilişkin değişiklikler

Birim fiyatı veya miktarı değiştiğinde, gelir tahsisatının parçası olan her madde için sözleşme gelir tutarı güncelleştirilmelidir. Bu nedenle, günlük girdisi yeniden hesaplanır.

Örneğin, madde 1000 için birim fiyat $1.500'den $1.600'e değiştirilir. Bu durumda, sözleşme gelir tutarı otomatik olarak $1.549,47 olarak yeniden hesaplanır. Madde S0021 için sözleşme geliri $290,53 olarak yeniden hesaplanır.

Değiştirilen doğrulanıp taahhüt edildiğinde, her iki maddenin ilk günlük girişleri ters çevrilir ve yeni günlük girişleri oluşturulur:

- **Madde 1000:** $1.465,26 özgün başlangıç günlük girişi tersine çevrildi. $1.549,47 değerinde yeni bir günlük girişi oluşturulur.
- **Madde S0021:** $274,74 özgün başlangıç günlük girişi tersine çevrildi. $290,53 değerinde yeni bir günlük girişi oluşturulur.

#### <a name="termination"></a>Sonlandırma

Madde S0021 başlangıç tarihi 2020 ve bitiş tarihi 2020 Aralık olur ancak Haziran 2020'de sona erer. Her iki maddeyle ilgili olarak sözleşme gelir tutarı yeniden hesaplanmalıdır:

- **Madde 1000:** Sözleşme geliri $1.567,67 olarak yeniden hesaplanır.
- **Madde S0021:** Sözleşme geliri $124,00 olarak yeniden hesaplanır.

Sona erdirilen satır için bir düzeltme günlüğü girişi oluşturulur. Aynı çoklu öğe düzenlemesi (MEA) numarasına ait olan satır için günlük girişi ters çevrilir ve yeni bir günlük girişi oluşturulur:

- **Madde 1000:** $1.465,26 özgün başlangıç günlük girişi tersine çevrildi. $1.549,47 değerinde yeni bir düzenleme günlük girişi oluşturulur.
- **Madde S0021:** $274,74 özgün başlangıç günlük girişi tersine çevrildi. $124,00 değerinde yeni bir günlük girişi oluşturulur.
