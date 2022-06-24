---
title: Maddelerin minimum kapsamını güncellemek için emniyet stoğu günlüğünü kullanma
description: Bu makalede, maddelerin emniyet stoku miktarını güncelleştirmek için emniyet stoğu günlüğünün, geçmişteki hareketlere dayalı minimum tedarik tekliflerini hesaplayarak nasıl kullanılacağı açıklanmaktadır.
author: t-benebo
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 385144738b83fcf6873eae5204b4784d6ecd5b80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851783"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Maddeler için minimum kapsamı güncelleştirmek için emniyet stoku günlüğünü kullanma

[!include [banner](../../includes/banner.md)]

Emniyet stoğu, maddenin stokta kalmama riskini azaltmak amacıyla bir madde için stokta tutulan ek miktarı belirtir. Emniyet stoğu, satış siparişlerinin gelmesi ve tedarikçinin müşteri tarafından talep edilen sevk tarihini karşılayacak şekilde teslim edememesi durumunda tampon olarak kullanılır.

Bu makale, geçmiş işlemleri temel alarak minimum kapsam tekliflerini hesaplamak ve ardından tekliflerle madde kapsamının güncelleştirmek için emniyet stoğu günlüğünün nasıl kullanılacağını açıklar.

## <a name="overview-of-minimum-coverage-usage"></a>Minimum tedarik kullanımına genel bakış

Emniyet stoğu, her madde için **Madde tedarik** sayfasında ayarlanır. Farklı stok yenileme türleri farklı karşılama kodlarıyla temsil edilir. (Daha fazla bilgi için bkz. [Maddelere yönelik emniyet stoğu karşılama](safety-stock-replenishment.md).) Ancak, tüm karşılama kodları **Madde karşılama** sayfasındaki **Minimum** alanında ayarlanan değeri kullanır. **Minimum** alanını kullanırken başlıca iki önemli yaklaşım vardır:

- **Min/maks amaçları için minimum miktar** – Bu yaklaşım minimum miktarı min/maks mantığıyla birlikte kullanır. İlgili madde veya karşılama grubu için **Karşılama kodu** alanı *Min/Maks* olarak ayarlandığında geçerlidir. **Minimum** miktar, maddenin sağlama süresine göre çarpılan ortalama günlük kullanımı temsil eder.
- **Stok planı amaçları için minimum miktar** – Bu yaklaşım, talep tahminlerle birlikte bir stok planını temsil etmek için minimum miktarı kullanır. İlgili madde veya karşılama grubu için **Karşılama kodu** alanı *Dönem* veya *Gereksinim* olarak ayarlandığında geçerlidir. **Minimum** miktar, stok aşımlarını, kısmi sevkiyatları ve teslimat sağlama sürelerini azaltmaya yardımcı olmak için istenen müşteri servisi düzeyini yansıtan bir stok planını temsil eder. Minimum miktar, belirli bir maddeyle ilgili tahmin doğruluk yüzdesini yansıtır. İstenen stok konumunu temsil etmez.

**Minimum** değer üç şekilde ayarlanabilir:

- **Öğe karşılama** sayfasında el ile
- Veri Yönetimi çerçevesi kullanarak (*Madde karşılama* veri varlıkları)
- Emniyet stoğu günlükleri tarafından yapılan emniyet stoğu hesaplamasına göre

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Geçmiş kullanımına göre minimum tedariği hesaplama

Emniyet stoğu günlükleri, minimum/maksimum veya stok planı amaçları için olan bir maddenin geçmiş kullanımını temel alan önerilen minimum miktarını hesaplamak için kullanılır. Tarihsel kullanım, belirtilen bir dönem içindeki tüm çıkış hareketlerini gösterir. Bu çıkış hareketleri satış siparişi hareketlerini ve stok düzeltmelerini içerir. Hesaplamalar ayrıca geçerli minimum miktarlarla karşılaştırıldığında, stok değerindeki önerilen minimum miktar değerini ve stok değerindeki değişikliği de tanımlar.

Her emniyet stoğu günlük satırı, bir maddeyi ve bu maddenin karşılama boyutlarını temsil eder. Bu günlük satırları, **Emniyet stoğu günlük satırları** sayfasında oluşturulur ve gösterilir (**Master planlama \> Master planlama \> Çalıştır \>Güvenlik stoğu hesaplaması**). Önerilen minimum miktarları hesaplamak için emniyet stoğu günlüklerini kullanmaya yönelik iş süreci bu makalenin ilerleyen kısımlarında açıklanmıştır.

Planlayıcı, seçili dönemler sırasında geçmişteki kullanımı esas alarak, seçili maddelerin önerilen minimum miktarlarını hesaplamak için bir emniyet stoğu günlüğü kullanır. Önerilen minimum değer gerektiğinde el ile geçersiz kılınabilir ve önerilen minimum değerlerinin potansiyel etkisini gözden geçirebilirsiniz. Günlük deftere nakledildiğinde, madde karşılamasının ilişkili minimum miktarları otomatik olarak güncelleştirilir.

### <a name="create-a-new-safety-stock-journal-name"></a>Yeni bir emniyet stoku günlüğü adı oluşturun.

Bu tür bir günlük oluşturabilmek için en az bir emniyet stoğu günlük adı oluşturmalısınız. Emniyet stoğu hesaplamalarınızı ayırmak için genellikle birkaç günlük adı kullanabilirsiniz.

1. **Master planlama \> Kurulum \> Emniyet stoğu günlük adları**'na gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki alanları ayarlayın:

    - **Ad**: Günlük için kısa bir ad girin.
    - **Açıklama**: Günlüğün açıklamasını girin.
    - **Kullanıcı grubuna özel** - Geçerli günlük adıyla ilgili izleyiciyi sınırlamak için bir kullanıcı grubu seçin.
    - **Deftere nakilden sonra satırları sil** – Günlüğü deftere naklederken varsayılan olarak günlük satırlarını temizlemek için bu onay kutusunu seçin. Tüm deftere nakledilmiş satırları tutmak için bu seçimi kaldırın.

    **Günlük türü** alanı salt okunurdur ve *Emniyet stoğu* olarak önceden ayarlıdır.

1. Sayfayı kapatın.

### <a name="create-a-safety-stock-journal-and-lines"></a>Bir emniyet stoku günlüğü ve satırları oluşturun

Bu adım, bir günlük oluşturur ve otomatik olarak buna satır ekler. Her satır bir maddeyi, kapsam boyutlarını ve kullanım geçmişinden alınan birkaç hesaplanan miktarı tanımlar. Hesaplanan miktarlar, madde sağlama süresine göre ortalama çıkışları, aylık ortalama çıkışları ve aylık standart sapmayı içerir.

#### <a name="automatically-generate-journal-lines"></a>Günlük satırlarını otomatik olarak oluştur

Günlük satırları, yalnızca şu anda gösterilen günlük için herhangi bir satır yoksa otomatik olarak oluşturulabilir.

Günlük satırlarını otomatik olarak oluşturmak için bu adımları izleyin.

1. **Master planlama \> Master planlama \> Çalıştır \> Emniyet stoğu hesaplama**'ya gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin. Yeni bir emniyet stoku günlüğü oluşturulur.
1. **Günlük üst bilgisi ayrıntıları** hızlı sekmesinde aşağıdaki alanları ayarlayın:

    - **Ad** – Satırın ekleneceği emniyet stoğu günlük adını seçin.
    - **Açıklama** – Varsayılan değer, seçtiğiniz günlük adının açıklamasıdır. Ancak, değerleri istediğiniz gibi düzenleyebilirsiniz.
    - **Deftere nakilden sonra satırları sil** – Günlüğü deftere naklederken günlük satırlarını temizlemek için bu onay kutusunu seçin. Tüm deftere nakledilmiş satırları tutmak için bu seçimi kaldırın. Ayar, seçili günlük adından devralınır.

    **Günlük** alanı salt okunurdur ve oluşturmakta olduğunuz ve satır eklediğiniz günlük kod numarasını gösterir.

1. **Günlük satırları** hızlı sekmesinde, araç çubuğundaki **Satır oluştur**'u seçin.
1. **Önerilen minimum stok düzeyleri için günlük satırları oluştur** iletişim kutusuna, aşağıdaki alanları ayarlayın:

    - **Başlangıç tarihi** – Maddelerin hesaplamaya dahil edilmesi gereken dönemin başlangıç tarihini seçin.
    - **Bitiş tarihi** – Maddelerin hesaplamaya dahil edilmesi gereken dönemin bitiş tarihini seçin. Başlangıç ve bitiş tarihleri arasında en az iki ay olmalıdır.
    - **Standart sapmayı hesapla** – Standart sapmayı hesaplamak için bu seçeneği *Evet* olarak ayarlayın. Teklifi hesaplarken (bu makalenin ilerisinde açıklandığı gibi), **Servis** düzeyi kullan seçeneğini kullanmak için bu seçeneği *Evet* olarak ayarlamalısınız.

1. **Dahil edilecek kayıtlar** hızlı sekmesinde, dahil edilecek maddeleri tanımlamak için filtreler ve sınırlamalar ayarlayabilirsiniz. (Örneğin, **Karşılama grubu** değerine göre filtre uygulayabilirsiniz.) Seçim ölçütü, sıralama ölçütü ve birleşim tanımlayabileceğiniz standart bir sorgu düzenleyici iletişim kutusunu açmak için **Filtre**'yi seçin. Alanlar, Microsoft Dynamics 365 Supply Chain Management'taki diğer sorgu türleri için çalıştıkları gibi çalışır.
1. **Arka planda çalıştır** hızlı sekmesinde, işi toplu iş modunda çalıştırmanın ve/veya yinelenen bir zamanlama ayarlamanın gerekip gerekmediğini seçin. Alanlar, Supply Chain Management'ta bulunan diğer [arka plan işleri](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) için çalıştıkları gibi çalışır.
1. **Tamam**'ı seçin. Stok işlemleri olan boyutlar için satırlar oluşturulur.

#### <a name="manually-add-or-remove-journal-lines"></a>Günlük satırlarını el ile ekleme veya kaldırma

Günlük satırlarını istediğiniz zaman el ile ekleyebilir ve/veya kaldırabilirsiniz (satırları otomatik olarak oluşturmak yerine veya bundan sonra). **Günlük satırları** hızlı sekmesinin araç çubuğunda aşağıdaki düğmeleri kullanın:

- **Yeni**: Yeni bir satır ekleyin. Sonra, kullanılacak ürünü tanımlamak ve yeni en düşük değerleri uygulamak için her sütuna bir değer girin. El ile eklenen satırlar için önerilen minimum hesaplamalar kullanılamadığından, bunlar için yeni **Hesaplanan minimum miktar** değerleri gösterilmez. Bu nedenle, **Yeni minimum miktar** değerlerini el ile girmeniz gerekir. Ancak, stok değerindeki **Yeni minimum miktar** değerinin ve geçerli olarak belirtilen minimum değere göre stokta potansiyel değişikliğin olası etkisini görebilirsiniz.
- **Sil**: Seçili satırı silin.
- **Günlük satırlarını sil** - Günlükteki tüm satırları silin.

### <a name="calculate-a-proposal"></a>Teklifi hesaplayın

Bu adım, her bir günlük satırı için önerilen minimum değerini ve satırın stok değerindeki potansiyel etkisini hesaplar. (Önerilen minimum değer **Hesaplanan minimum miktar** değeri olarak gösterilir.) Hesaplamayı, gereksinim duyduğunuz şekilde birçok kez yapabilirsiniz. Hesaplama, tüm günlük satırları için gösterilen **Hesaplanmış minimum miktar** değerini güncelleştirir.

Gösterilen hesaplamalar, Eylem Bölmesinde **Deftere naklet**'i seçene kadar her bir ürün için fiili minimum miktar değerlerini etkilemez. Bu tarihte, her bir ürüne **Yeni minimum miktar** değerleri uygulanacaktır.

1. **Master planlama \> Master planlama \> Çalıştır \> Emniyet stoğu hesaplama**'ya gidin.
1. Teklifi hesaplamak için günlüğü açın. Alternatif olarak, bu makalede daha önce anlatıldığı gibi yeni bir günlük de oluşturabilirsiniz.
1. **Günlük satırları** hızlı sekmesinde, araç çubuğundaki **Teklifi hesapla**'yı seçin. (Herhangi bir satırı seçmeniz gerekmez.)
1. **Minimum stok düzeyi için teklifi hesapla** iletişim kutusuna, aşağıdaki alanları ayarlayın:

    - **Sağlama süresi içinde ortalama sorunu kullan** – Belirtilen dönem boyunca ortalama sorunu temel alarak **Hesaplanan minimum miktar** değerleri oluşturmak için bu seçeneği belirleyin. Sonra, **Çarpma faktörü** alanına, sonucu gerektiği şekilde ayarlamak için bir değer girin. Örneğin, yüzde 10'luk fazladan bir tampon eklemek için tam hesaplanmış *1,1* ortalamayı kullanmak üzere *1,0* girin.
    - **Servis düzeyi kullan** – İstenen servis düzeyine göre önerilen minimum değeri hesaplamak için bu seçeneği belirleyin. Ardından, **Servis düzeyi** alanında tercih edilen servis düzeyinizi seçin.
    - **Sağlama süresi marjı** – Normal sağlama süresini uzatmak için bir değer girin (örneğin, yönetime izin vermek için).
    - **Yeni minimum miktar olarak hesaplanan minimum miktarı kullan** - Hesaplama tamamlandıktan sonra tüm satırlar için **Hesaplanan minimum miktar** sütunundaki değerleri otomatik olarak **Yeni minimum miktar** sütununa kopyalamak için bu seçeneği *Evet* olarak ayarlayın. Bu seçeneği *Hayır* olarak ayarlarsanız, **Geçerli minimum miktar** değeri tüm satırlar için **Yeni minimum miktar** sütununa kopyalanır. Daha sonra, **Yeni minimum miktar** değerlerini gerektiği gibi el ile düzenlemeniz gerekir.

1. **Arka planda çalıştır** hızlı sekmesinde, işi toplu iş modunda çalıştırmanın ve/veya yinelenen bir zamanlama ayarlamanın gerekip gerekmediğini seçin. Alanlar, Supply Chain Management'ta bulunan diğer [arka plan işleri](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) için çalıştıkları gibi çalışır.
1. **Tamam**'ı seçin. Hesaplamanın sonuçları, **Günlük satırları** hızlı sekmesindeki **Hesaplanan minimum miktar** sütununda gösterilir. Şimdilik değerler yalnızca ürünleriniz için henüz uygulanmamış önerilen değerlerdir.

### <a name="update-minimum-quantity"></a>Minimum miktarı güncelleştir

Emniyet stoku günlüğündeki herhangi bir satırı seçebilir ve **Yeni minimum miktar** alanının değerini el ile geçersiz kılabilirsiniz.

1. **Master planlama \> Master planlama \> Çalıştır \> Emniyet stoğu hesaplama**'ya gidin.
1. Düzenlenecek günlüğü açın. Alternatif olarak, daha önce anlatıldığı gibi yeni bir günlük de oluşturabilirsiniz.
1. **Günlük satırları** hızlı sekmesinde, ayarlanacak satırı bulun ve sonra **Yeni minimum miktar** sütunundaki değeri düzenleyin. Örneğin, **Yeni minimum miktar** değerini **Hesaplanmış minimum miktar** değeriyle eşleşecek şekilde ayarlayabilirsiniz. **Hesaplanan minimum miktar** değeri *0* (sıfır) ise istediğiniz gelecek değerini girebilirsiniz.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Yeni minimum miktarı gönderin ve sonucu doğrulayın

Yeni minimum miktarı göndermek ve sonucu doğrulamak için aşağıdaki adımları izleyin.

1. **Master planlama \> Master planlama \> Çalıştır \> Emniyet stoğu hesaplama**'ya gidin.
1. Yeni minimum miktarlarının nakledileceği günlüğü açın. Alternatif olarak, daha önce anlatıldığı gibi yeni bir günlük de oluşturabilirsiniz.
1. Eylem Bölmesinde **Deftere naklet**'i seçin.
1. **Günlüğü deftere naklet** iletişim kutusunda, **Tüm deftere nakil hatalarını yeni günlüğe aktar** alanını gerektiği şekilde ayarlayın. Ardından günlüğü deftere nakletmek için **Tamam**'ı seçin.
1. **Günlük satırları** hızlı sekmesinde bir satırın **Yeni minimum miktar** değerini değiştirdiyseniz, değişikliği aşağıdaki adımları izleyerek doğrulayabilirsiniz:

    1. Düzenlediğiniz satır için **Madde numarası** sütunundaki bağlantıyı seçin.
    1. **Ürün bilgileri** iletişim kutusunda, ilgili serbest bırakılan ürün kaydını açmak için **Madde numarası** alanındaki bağlantıyı seçin.
    1. Eylem Bölmesindeki **Plan** sekmesinde yer alan **Kapsam** grubunda **Madde kapsamı**'nı seçin.
    1. Deftere nakledilen emniyet stoğu günlüğünü kullanarak düzelmiş olduğunuz tesis ve ambar için **Minimum** değerin şimdi düzenlediğiniz ile aynı olacak şekilde güncelleştirilmiş olduğuna dikkat edin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Maddeler için emniyet stoğu karşılama](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
