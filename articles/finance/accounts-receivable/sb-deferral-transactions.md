---
title: Abonelik faturalamasında erteleme hareketleri
description: Bu konu, abonelik faturalamasında gelir ve gider ertelemeleri kapsamında erteleme hareketlerinde kullanılabilen çeşitli hareketleri açıklamaktadır.
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
ms.openlocfilehash: 5913308d4ee9fdcb8cf2b862171078f27f651662
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686031"
---
# <a name="deferral-default-transactions"></a>Erteleme varsayılan işlemleri

Bu konuda, gelir ve gider ertelemeleri için izin verilen hareketler açıklanmaktadır. Erteleme planları her zaman kaynak belgeye veya faturalama planına dayanır ve bağlıdır. Erteleme planları varsayılan ayarlar temelinde oluşturulur ve ayrı olarak girilemez veya oluşturulamaz.

## <a name="sales-order-transaction-deferral"></a>Satış siparişi hareket ertelemesi

Bir satış siparişi satırı için erteleme parametrelerini girmek veya düzenlemek için **Ertelemeler** veya **Alacak dekontu oluştur** sayfasını kullanın.

> [!NOTE]
> Bir faturalama planında bir satış siparişi oluşturulduğunda, **Erteleme** veya **Alacak dekontu oluştur** sayfasındaki tüm değerler salt okunurdur ve erteleme parametreleri düzenlenemez. Değerleri düzenlemek için **Planı değiştir** sayfasını kullanın.

### <a name="edit-deferral-options"></a>Erteleme seçeneklerini düzenleme

Bir satırın erteleme seçeneklerini düzenlemek için, aşağıdaki adımları izleyin.

1. Satış siparişi hareketi oluşturun.
2. Satırı seçin ve sonra **Ertelemeler**'i seçin.
3. **Hareket erteleme** sayfasında, **Ertelenmiş** seçeneğinin **Evet** olarak ayarlanması gerekir. Diğer alanları istediğiniz şekilde düzenleyin.
4. Erteleme planını önizlemek için **Önizleme**'yi seçin.
5. Hareket ertelemelerinde herhangi bir değişiklik yaptıysanız **Tamam**'ı seçin ve hareket sayfasına geri dönün.
6. Hareketi işleyin ve deftere nakledin.

Hareket deftere nakledildikten sonra erteleme planını görüntülemek için **Tüm erteleme planları** sayfasını açın.

### <a name="create-a-credit-note"></a>Alacak dekontu oluşturma

Yeni bir alacak dekontu oluşturmak için aşağıdaki adımları izleyin.

1. Satış siparişi hareketi oluşturun.
2. **Satış siparişi satırları** bölümünde, alacak dekontu oluşturmak istediğiniz maddeyi seçin.
3. **Satış siparişi satırı** \> **Yeni**'yi seçin ve ardından **Alacak dekontu**'nu seçin.
4. **Ertelemeler**'i seçin.
5. **Satış siparişi hareket ertelemesi** sayfasında, madde için **Varolan planı düzelt** seçeneğini **Evet** olarak ayarlayın.
6. **Düzeltilen plan** alanında, alacak dekontunu uygulamak istediğiniz ertelemeyi seçin.
7. **Yeniden hesaplama tarihi** ve **Bitiş tarihi** alanlarını gerektiği gibi güncelleştirin.
8. **Tamam**'ı seçin.
9. Satış siparişi hareketini deftere nakletme işlemini tamamlayın.

### <a name="purchase-orders-and-purchase-invoices"></a>Satın alma siparişleri ve satın alma faturaları

Bir satın alma siparişi için erteleme işlevlerini kullanmak istiyorsanız, önce faturayı oluşturun. Daha sonra, **Bekleyen satıcı faturaları** sayfasını kullanarak erteleme maddeleri ekleyebilir veya ekleyebilirsiniz. Doğrudan bir satın alma siparişi üzerinde, ertelemeleri düzenleyemez veya ekleyemezsiniz.

1. Satıcı faturası girmek için **Bekleyen satıcı faturaları** sayfasını kullanın.

    Bir satır girdiğinizde erteleme, erteleme kategorisi için seçtiğiniz madde veya tedarik kategorisine otomatik olarak ayarlanır. Bu erteleme, **Erteleme varsayılan ayarları** sayfasındaki erteleme kurulumuna dayanır. Erteleme, dağıtım düzeyinde düzenlenebilir veya eklenebilir.

3. Satın alma satırında, **Finansal öğeler \> Tutarları dağıt**'ı seçin.
4. Her dağıtım tutarı için **Ertelemeler**'i seçin. Fatura deftere nakledildiğinde, erteleme için belirlenen her bir dağıtım için erteleme planı oluşturulur.

### <a name="tax"></a>Vergi

Bazı durumlarda, vergi tutarı tamamen veya kısmen kurtarılamaz olabilir. Ertelenebilir bir satırın vergi tutarı kurtarılamayan bir tutar içeriyorsa, fatura deftere nakledildiğinde, kurtarılamayan vergi tutarı ertelenebilir plan tutarına dahil edilir.

### <a name="variance"></a>Fark

Satıcı faturası satırındaki tutar satın alma siparişi satırındaki tutardan farklıysa, fark dağıtımları oluşturulur. Satır ertelenirse, bu dağıtımlara ait genel muhasebe hesabı erteleme hesabına ayarlanır ve fatura deftere nakledildiğinde tutarlar, ertelenebilir plan tutarına dahil edilir. Bu dağıtımlar **Fiyat farkı** ve **Maliyet farkı** olarak adlandırılmıştır.

### <a name="general-journals-and-invoice-journals"></a>Yevmiye defterleri ve fatura günlükleri

Bir günlük fiş satırı için erteleme parametrelerini girmek üzere **Ertelemeler** sayfasını kullanın. Ayrıca, eşit paylı ertelemeler için erteleme planını önizleyebilirsiniz. Bir satır girdiğinizde erteleme, **Erteleme varsayılan ayarları** sayfasındaki erteleme hesaplarının kurulumuna göre otomatik olarak ayarlanır. Her satır için erteleme seçeneklerini el ile değiştirebilirsiniz. Günlük fişi deftere nakledildiğinde erteleme planı oluşturulur.

#### <a name="post-and-transfer"></a>Deftere naklet ve aktar

Günlük fişini nakletmek için **Deftere naklet ve aktar** komutunu kullanın. Erteleme seçenekleri, fişin uygulandığı satırı izler. Hata içermeyen fişler için, fiş ertelenmiş ise erteleme planı oluşturulur. Hatalı ve aktarılmış bir fiş için, tüm erteleme seçenekleri de onunla birlikte aktarılır.

#### <a name="tax"></a>Vergi

Bazı durumlarda, vergi tutarı tamamen veya kısmen kurtarılamaz olabilir. Ertelenebilir bir satırın vergi tutarı kurtarılamayan bir tutar içeriyorsa, fatura deftere nakledildiğinde, kurtarılamayan vergi tutarı ertelenebilir plan tutarına dahil edilir.

## <a name="free-text-invoice-transaction-deferral"></a>Serbest metin faturası hareket ertelemesi

Bir serbest metin fatura satırı dağıtımı için erteleme parametrelerini girmek üzere **Ertelemeler** sayfasını kullanın. Bir dağıtım girdiğinizde erteleme, **Erteleme varsayılan ayarları** sayfasındaki erteleme ayarlarına göre otomatik olarak ayarlanır.

## <a name="fields"></a>Alanlar

**Hareket ertelemesi** sayfası, aşağıdaki alanları içerir.

| Alan | Açıklama |
|-------|-------------|
| Ertelenmiş | <p>Satırın bir erteleme olup olmadığını belirtin:</p><ul><li>**Evet** – Satırın bir erteleme olup olmadığını belirtin.</li><li>**Hayır** – Satır erteleme değildir.</li></ul><p>Bu seçenek **Evet** olarak ayarlandığında, **Varolan planı düzelt** seçeneği kullanılamaz. Zaten ertelenmiş olarak ayarlanmış maddeler ve giderler için bu seçenek **Evet** olarak ayarlanır. Varsayılan olarak ertelenmiş olarak ayarlanmayan maddeler ve giderler için bu seçeneği **Evet** olarak ayarlayın.</p> |
| Mevcut planı düzelt | <p>Satırın varolan bir erteleme planına yönelik bir düzeltme olup olmadığını belirtin:</p><ul><li>**Evet** – Yeni satış satırı, varolan bir erteleme planına yönelik bir düzeltmedir. Bu durumda, **Düzeltilen plan** alanında erteleme planı seçebilirsiniz.</li><li>**Hayır** – Yeni satış satırı, varolan bir erteleme planına yönelik bir düzeltme değildir.</li></ul><p>Bu seçenek **Evet** olarak ayarlandığında, **Ertelenmiş** seçeneği kullanılamaz.</p> |
| Düzeltilen plan | <p>Satırın düzelttiği ilgili erteleme planını seçin. Daha sonra sayfadaki tüm değerler, kaynak erteleme planındaki değerlerle güncellenir. Bu değerler düzenlenemez.</p><p>Bu alan yalnızca **Varolan planı düzelt** seçeneği **Evet** olarak ayarlandığında kullanılabilir.</p> |
| Yeniden hesaplama tarihi | <p>Kalan tutarı yeniden hesaplamak istediğiniz dönemin başlangıç tarihini belirtin. Varsayılan tarih, bir sonraki kabul edilmeyen dönemin tarihidir.</p><p>Bu alan yalnızca **Varolan planı düzelt** seçeneği **Evet** olarak ayarlandığında kullanılabilir.</p> |
| Bitiş tarihi | <p>Erteleme türüne bağlı olarak, bitiş tarihi güncelleştirilmiş olabilir veya olmayabilir:</p><ul><li>Eşit paylı erteleme için, planın yeni bitiş tarihini belirtin. Erteleme planının varolan bitiş tarihi varsayılan değerdir.</li><li>Olay tabanlı erteleme için, alacak olay satırının bitiş tarihini belirtin. Bu tarih boş olabilir.</li></ul><p>Bu alan yalnızca **Varolan planı düzelt** seçeneği **Evet** olarak ayarlandığında kullanılabilir.</p> |
| Fatura planı numarası | <p>Faturalama planı numarası.</p><p>Bu alan yalnızca yinelenen sözleşme faturalama planları için kullanılabilir.</p> |
| Erteleme düzeltme yöntemi | <p>Erteleme düzeltme yöntemi. Değer, yinelenen sözleşme faturalama planı için **Toplu sonlandırma işleme** sayfasındaki değerle eşleştirilir.</p><p>Bu alan yalnızca yinelenen sözleşme faturalama planları için kullanılabilir.</p> |
| **Hesaplar - Gelir** | |
| Erteleme hesabı | <p>**Satış siparişi** sayfasında görünen deftere nakil hesabı olan erteleme hesabı.</p><p>Satır ertelenmemişse, bu alan boş kalır. Bu durumda, deftere nakil hesabı varsayılan gelir hesabıdır.</p> |
| Kabul hesabı | <p>Erteleme kabul edildiğinde kullanılan hesabı belirtin. Bu hesap erteleme hesabından farklı olmalıdır.</p><p>**Ertelenmiş** seçeneği başlangıçta **Evet** olarak ayarlandığında, erteleme hesabında kullanılan boyut değerleri kabul hesabına kopyalanır. Erteleme hesabındaki boyut, kabul hesabı için mevcut değilse, yok sayılır.</p> |
| İlk kabul hesabı | <p>Başlangıçtaki gelir kabulü için hesabı seçin. Varsayılan değer **Erteleme varsayılan ayarları** sayfasından alınır.</p><p>Bu alan yalnızca **Gelir ve gider erteleme parametreleri** sayfasındaki **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlandığında kullanılabilir.</p> |
| Kabul mahsup hesabı | <p>Gelir kabulünü mahsup etmeye yönelik hesabı seçin. Varsayılan değer **Erteleme varsayılan ayarları** sayfasından alınır.</p><p>Bu alan yalnızca **Gelir ve gider erteleme parametreleri** sayfasındaki **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlandığında kullanılabilir.</p> |
| **Hesaplar - İskonto** | Bu bölüm yalnızca ertelenen maddeler için görünür. Ertelenmiş giderler için gizlidir. |
| Erteleme hesabı | <p>İskonto erteleme hesap numarasını belirtin. Varsayılan değer **Erteleme varsayılan ayarları** sayfasından alınır.</p><p>Bu alan yalnızca, **Gelir ve gider erteleme parametreleri** sayfasındaki **İskonto erteleme seçeneği** alanı **İskonto için ayrı plan** olarak ayarlandığında kullanılabilir ve satıra bir iskonto uygulanır.</p> |
| Kabul hesabı | <p>İskonto kabul hesap numarasını belirtin. Varsayılan değer **Erteleme varsayılan ayarları** sayfasından alınır.</p><p>Bu alan yalnızca, **Gelir ve gider erteleme parametreleri** sayfasındaki **İskonto erteleme seçeneği** alanı **İskonto için ayrı plan** olarak ayarlandığında kullanılabilir ve satıra bir iskonto uygulanır.</p> |
| İlk kabul hesabı | <p>Başlangıçtaki iskonto kabulü için hesabı seçin. Varsayılan değer **Erteleme varsayılan ayarları** sayfasından alınır.</p><p>Bu alan yalnızca, **Gelir ve gider erteleme parametreleri** sayfasındaki **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlandığında kullanılabilir ve satıra bir iskonto uygulanır.</p> |
| Kabul mahsup hesabı | <p>Gelir kabulünü mahsup etmeye yönelik hesabı seçin. Varsayılan değer **Erteleme varsayılan ayarları** sayfasından alınır.</p><p>Bu alan yalnızca, **Gelir ve gider erteleme parametreleri** sayfasındaki **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlandığında kullanılabilir ve satıra bir iskonto uygulanır.</p> |
| **Hesaplar - Tüketim** | Bu bölüm yalnızca ertelenen maddeler için görünür. Ertelenmiş giderler için gizlidir. |
| Erteleme hesabı | <p>Tüketim erteleme hesap numarasını belirtin.</p><p>Standart ürünler için, iki erteleme planı oluşturulur:</p><ul><li>**Standart satışlar** - Alacak bakiyesi olan bir gelir planı. Bu durumda, tüketim erteleme hesabını seçin.</li><li>**Tüketim** – Borç bakiyesine sahip tüketim (satılan malların maliyeti \[SMM\]) gider planı. Bu durumda, tüketim kabul hesabını seçin.</li></ul><p>Fatura deftere nakledildiğinde, tüketim tutarı belirtilen tüketim erteleme hesabına nakledilir. Bu alanlar servis maddeleri için kullanılamaz.</p> |
| Kabul hesabı | Tüketim kabul hesap numarasını belirtin. |
| İlk kabul hesabı | <p>İlk tüketim kabul tutarı için hesap belirtin. Varsayılan değer **Erteleme varsayılan ayarları** sayfasından alınır.</p><p>Bu alan yalnızca **Gelir ve gider erteleme parametreleri** sayfasındaki **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlandığında kullanılabilir.</p> |
| Kabul mahsup hesabı | <p>Tüketim kabul mahsup tutarı için hesap belirtin. Varsayılan değer **Erteleme varsayılan ayarları** sayfasından alınır.</p><p>Bu alan yalnızca **Gelir ve gider erteleme parametreleri** sayfasındaki **Erteleme deftere nakil yöntemi** alanı **Kar ve zarar** olarak ayarlandığında kullanılabilir.</p> |
| **Plan** | |
| Planlama türü | <p>Erteleme planı türünü seçin: **Eşit paylı** (varsayılan) veya **Olay tabanlı**.</p><p>Sayfada görünen seçenekler seçtiğiniz erteleme planı türünü temel alır.</p><p>Varsayılan şablon, hareket satırının **Erteleme varsayılan ayarları** sayfasında ayarlandıysa, erteleme planı türü seçilen şablon türüne bağlıdır.</p> |
| **Plan - Eşit paylı** | |
| Önceki dönemleri konsolide et | <p>Önceki dönemler için erteleme planı satırlarını konsolide etmek isteyip istemediğinizi belirtin:</p><ul><li>**Evet** – Önceki dönemler için erteleme planı satırlarını konsolide edin.</li><li>**Hayır** – Önceki dönemler için erteleme planı satırlarını konsolide etmeyin.</li></ul><p>Varsayılan değer **Gelir ve gider erteleme parametreleri** sayfasından alınır.</p> |
| Dönem başına eşit | <p>Her dönem için gün sayısının eşit olup olmayacağını veya döneme göre değişiklik gösterip göstermeyeceğini belirtin:</p><ul><li>**Evet** – Her dönemdeki gün sayısı eşittir.</li><li>**Hayır** – Dönemlerdeki gün sayısı aynı değildir.</li></ul><p>Bu seçenek **Hayır** olarak ayarlandığında, erteleme planıyla ilgili her dönemdeki tutar hesaplandığında, dönemdeki gün sayısı dikkate alınır.</p><p>Varsayılan değer **Gelir ve gider erteleme parametreleri** sayfasından alınır.</p> |
| Şablondan planla | <p>Erteleme planının bir şablona mı, yoksa bir bitiş tarihine göre mi oluşturulacağını belirtin:</p><ul><li>**Evet** – Erteleme planı bir şablon temel alınarak oluşturulur.</li><li>**Hayır** – Erteleme planı bir bitiş tarihi temel alınarak oluşturulur.</li></ul> |
| Şablon | Erteleme şablonunu seçin. |
| Başlangıç tarihini geçersiz kıl | <p>Başlangıç tarihini geçersiz kılmak isteyip istemediğinizi belirtin:</p><ul><li>**Evet** – **Başlangıç tarihi** alanına girdiğiniz tarihle başlangıç tarihini geçersiz kılar.</li><li>**Hayır** – Başlangıç tarihi, **Fatura deftere nakli** sayfasında belirtilen fatura tarihine uygulanan **Varsayılan erteleme başlangıç tarihi** kuralıdır. Bu kural **Gelir ve gider erteleme parametreleri** sayfasında ayarlanabilir.</li></ul> |
| Erteleme başlangıç tarihi | Ertelemenin başlangıç tarihini belirtin. Hareket tarihi, varsayılan değerdir. |
| Erteleme bitiş tarihi | <p>Ertelemenin bitiş tarihi.</p><p>Bu tarih erteleme şablonu temel alınarak otomatik olarak hesaplanır. Seçili şablon yoksa, tarihi el ile girmeniz gerekir.</p> |
| **Plan - Olay tabanlı** | |
| Şablon | <p>Olay tabanlı şablonu seçin. Bu alan isteğe bağlıdır.</p><p>Bir şablon seçerseniz, şablondaki değerler tüm olay tabanlı verilerin ve olay satırlarının üzerine yazılır.</p> |
| Tahsisat türü | <p>Olay satırları için tahsisat türünü seçin:</p><ul><li>**Değişken tutarlar** – Her satır için belirli bir tahsisat tutarı girilir.</li><li>**Eşit tutarlar** – Tutar her satır için eşit olarak tahsis edilir.</li><li>**Yüzde** – Tutar her satır için girilen yüzde değeri temel alınarak tahsis edilir.</li><li>**Tamamlanma yüzdesi** – Her satır için toplam tamamlanma değeri girilir.</li><p>**Değişken miktar** – Her satır için belirli bir tahsisat miktarı girilir.</li></ul><p>**Not:** **Tamamlanma yüzdesi**'ni seçmek istiyorsanız, tarihlerin artan sırada olması gerekir.</p> |
| **Her birim için ayrı olaylar oluştur** | |
| Açıklama | <p>Olayları birim başına ayırmak isteyip istemediğinizi belirtin:</p><ul><li>**Evet** – Miktar başına bir satır olacak şekilde olay satırlarını ayırın.<p>Örneğin, üç olay satırı vardır ve faturanın dört miktarı vardır. Bu durumda, sonuçta elde edilen erteleme planının 12 satırı vardır.</p></li><li>**Hayır** – Olay satırlarını ayırmayın.</li></ul> |
| Sona erme hesabı | <p>Kabul edilen süresi geçmiş satırlar için kullanılan hesabı seçin. Erteleme planı oluşturulduktan sonra hesabı seçebilirsiniz.</p><p>Bir olay için sona erme tarihi ayarlanırsa, kabul süreci sırasında kabul tutarı, kabul hesabı yerine sona erme hesabına gider.</p> |
| **Plan - Olay tabanlı satırlar** | |
| Açıklama | Olayın açıklaması. |
| Erteleme bitiş tarihi | <p>Olayın bitiş tarihini seçin.</p><p>**Not:** Bitiş tarihi seçerseniz, **Sona erme tarihi** alanı temizlenir. Bitiş tarihi ve sona erme tarihini birlikte kullanamazsınız.</p> |
| Sona erme tarihi | <p>Olayın sona erme tarihini seçin.</p><p>**Not:** Bitiş tarihi seçerseniz, **Sona erme tarihi** alanı temizlenir. Bitiş tarihi ve sona erme tarihini birlikte kullanamazsınız.</p> |
| Miktar | <p>Tahsisat miktarını belirtin. Tüm satırlar için varsayılan değer **0**'dır (sıfır). Miktarı güncelleştirirseniz, tüm satırların toplam miktarı satış siparişindeki satır maddesi için belirtilen miktara eşit veya bundan az olmalıdır.</p><p>Bu alan, yalnızca **Tahsisat türü** alanı **Değişken miktar** olarak ayarlandığında kullanılabilir.</p><p>Satış siparişindeki satır maddesinin miktarı orijinal miktardan az olacak şekilde değiştirilirse ve fatura oluşturulursa, daha az sayıda olay tabanlı satır oluşturulur. Toplam tahsis edilen miktar, başlangıçtaki satış siparişi veya faturalama planında belirtilen miktarı aşamaz.</p> |
| Tahsisat yüzdesi | <p>Tahsisat yüzdesini belirleyin. **Tahsisat türü** alanı **Yüzde** veya **Tamamlanma yüzdesi** olarak ayarlanmışsa, el ile bir yüzde girebilirsiniz. Aksi takdirde, otomatik olarak hesaplanır.</p><p>**Tahsisat türü** alanı **Yüzde** olarak ayarlanırsa yüzdelerin toplamı 100'e eşit olmalıdır.</p> |
| Tutar | <p>Tahsisat miktarını belirtin. **Tahsisat türü** alanı **Yüzde** veya **Değişken tutarlar** olarak ayarlanmışsa, el ile bir tutar girebilirsiniz.</p><p>**Tahsisat türü** alanı **Tamamlanma yüzdesi** olarak ayarlanmışsa ve buraya tutar girerseniz, **Tamamlanma yüzdesi** alanının değeri otomatik olarak hesaplanır.</p><p>Yuvarlama nedeniyle, hesaplanan tutar el ile girilmiş tutarla tam olarak aynı olmayabilir. Tam bir tutara gereksinim duyarsanız, **Tahsisat türü** alanını **Değişken tutarlar** olarak ayarlayın.</p> |
| Tamamlanma yüzdesi | <p>Tamamlanma yüzdesini belirtin. Değer 0 (sıfır) ile 100 arasında olmalıdır.</p><p>Bu alan, yalnızca **Tahsisat türü** alanı **Tamamlanma yüzdesi** olarak ayarlandığında kullanılabilir.</p> |
| Tamamlanma tutarı | <p>Erteleme planıyla ilgili tüm satırlar için hesaplanan toplam.</p><p>**Tahsisat türü** alanı **Tamamlanma yüzdesi** olarak ayarlanmışsa, el ile bir tutar girebilirsiniz. Bu durumda, **Tamamlanma yüzdesi** alanının değeri girdiğiniz tutara göre hesaplanır.</p><p>Yuvarlama nedeniyle, hesaplanan tutar el ile girilmiş tutarla tam olarak aynı olmayabilir.</p><p>Bu alan, yalnızca **Tahsisat türü** alanı **Tamamlanma yüzdesi** olarak ayarlandığında kullanılabilir.</p> |
| Deftere nakil sonrası kabul | <p>Satırın, hareket deftere nakledildikten hemen sonra otomatik olarak kabul edilip edilmeyeceğini belirtin:</p><ul><li>**Seçildi** – Satır, hareket deftere nakledildikten hemen sonra otomatik olarak kabul edilir.</li><li>**Temizlendi** – Satır, hareket deftere nakledildikten hemen sonra otomatik olarak kabul edilmez.</li></ul> |
| Kabul hesabı | <p>Hesap tüm erteleme planı için kullanılan hesaptan farklıysa, olay için kabul hesabını belirtin.</p><p>Bu alanı, **Deftere nakil sonrası kabul** seçeneğiyle birlikte kullanabilirsiniz.</p> |
