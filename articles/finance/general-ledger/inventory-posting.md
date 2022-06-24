---
title: Stok deftere nakil işlemi
description: Bu makalede, Stok deftere nakil profili sayfasındaki Stoğun deftere nakli sekmesi açıklanmaktadır.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 7fd507dd171b0d49673bdd0d0900b3f02dbcb65b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891565"
---
# <a name="inventory-posting"></a>Stok deftere nakil işlemi

**Stok deftere nakil profilleri** sayfasındaki **Stok** sekmesi, stok hareketlerinin genel muhasebe defterine nasıl nakledileceğini denetlemek için kullanılır. Stok hareketleri; satış siparişlerinden, satınalma siparişlerinden veya üretim emirlerinden oluşturulmamış hareketlerdir. Stoktaki fiziksel ve mali güncelleştirmeleri otomatik ve eş zamanlı olarak deftere naklederler. Bunun tek istisnası, stoğu sevk ettiğinizde ve aldığınızda fiziksel ve mali güncelleştirmeleri ayıran transfer emirleridir.

Aşağıdaki tabloda stok hareketlerine bazı örnekler gösterilmektedir.

| Hareket türü | Giriş veya çıkış | Fiziksel deftere nakil, mali deftere nakil veya her ikisi | Açıklama |
|---|---|---|---|
| Hareket | İkisi birden | İkisi birden | <p>Hareket günlüğü, stok eklemek veya kaldırmak için kullanabileceğiniz bir stok günlüğüdür. Stok düzeltme günlüğü görevi görür. Ancak temel farklardan biri, girişi mahsup eden ana hesabın belirtilmesidir.</p><p>Hareket günlüğüne başlangıç bakiyeleri ve giderleştirilmesi gereken tek seferlik düzeltmeler girilir. Örneğin, bir stok bir satış örneğinden kaldırıldığında kullanılır.</p><p>Günlük deftere nakledildiğinde, fiziksel ve mali güncelleştirmeler eş zamanlı olarak gerçekleşir.</p><p>Günlük satırlarındaki pozitif miktarlar girişleri, negatif miktarlar ise çıkışları gösterir.</p> |
| Stok düzeltmesi | İkisi birden | İkisi birden | Stok eklemek veya kaldırmak için stok düzeltme günlüğü kullanılır. Bunun için mahsup hesap seçmenize izin verilmez. Yalnızca **Stok deftere nakil profili** sayfasında belirtilen hesaplar, genel muhasebe defteri girişini güncelleştirmek için kullanılır. |
| Transfer (günlük) | İkisi birden | İkisi birden | <p>Transfer günlüğü, stoğu bir yerleşimden diğerine taşımak için kullanılır (depolama boyutları kullanılarak). Bir stok hareketindeki ürün bilgilerini yeni ürün veya izleme boyutlarıyla güncelleştirir.</p><p>Transfer günlüğü, bir maddenin hareketi için bir satır oluşturur. Bu satırda, stok boyutları için "başlangıç" ve "bitiş" alanları bulunur. Transfer günlüğündeki her satır iki stok hareketi oluşturur. Hareketlerden biri "başlangıç" stok boyutları için oluşturulur. Bu, çıkışı temsil eder ve negatif miktara sahiptir. Diğer hareket, "bitiş" stok boyutları için oluşturulur. Bu, girişi temsil eder ve pozitif miktara sahiptir.</p><p>Stoğun hareketi mali olmayan bir transfer olarak kabul edilirse transfer günlükleri fiş oluşturmayabilir. "Başlangıç" ve "bitiş" değerleri için değişen stok boyutları, **Depolama boyutu grubu** veya **İzleme boyutu grubu** sayfasında **Mali stok** seçeneğiyle işaretlenmez. Örneğin, **Mali stok** seçeneği **Yerleşim** boyutunda işaretli değilse ve stoğu aynı tesis ve ambarda bir yerleşimden başka bir yerleşime taşırsanız, fiş oluşturulmaz.</p><p>Transfer günlükleri, taşıma için belge bulunmadığından transfer emirlerinden farklıdır. Güncelleştirme, günlüğü deftere naklederek tek bir harekette gerçekleştirilir. Bunun tersine, bir transfer emri malzeme çekme ve sevkiyat belgeleri oluşturabilir ve hareketi işlemek için iki güncelleştirme gerektirir.</p> |
| Transfer emri sevkiyatı | Sorun | İkisi birden | <p>Yeni bir transfer emri oluşturduğunuzda, satır ve stok boyutunun her birleşimi için iki stok hareketi bulunur: Biri transfer emri sevkiyatı için, diğeri transfer emri girişi içindir. Transfer emrini sevk ettiğinizde, iki stok hareketi güncelleştirilir ve malların aktarılmasına yönelik iki ek stok hareketi oluşturulur. Toplamda dört stok hareketi oluşturulmuş olur.</p><ol><li>İlk stok hareketi, maddeyi kaynak ambar ve yerleşimden çıkarmak için kullanılır. Bu hareketin çıkış durumu, maddenin ambarda artık mevcut olmadığını göstermek için **Satıldı** durumundadır.</li><li>İkinci stok hareketi, maddenin transfer edildiği ambar için seçilen transit ambarına maddeyi eklemek için kullanılır. Bu hareketin giriş durumu **Satın alındı** durumudur.</li><li>Üçüncü stok hareketi, transit ambarından hedef ambara transfer içindir. Bu hareketin çıkış durumu **Fiziksel rezerve miktar**'dır. Bu durum, maddenin hala transit durumundayken başka bir işlem tarafından tüketilmemesini sağlar.</li><li>Dördüncü stok hareketi, malların hedef ambara girişi içindir. Bu hareketin giriş durumu **Sipariş edildi** durumudur.</li></ol> |
| Transfer emri teslim alma | Giriş | İkisi birden | Bir transfer emri hedef ambarda teslim alındığında, transit ambarındaki stok hareketinin stok durumu (önceki örnekteki 3 numaralı ambar) **Satıldı** olarak güncelleştirilir ve hedef ambar için stok hareketinin stok durumu **Satın alındı** olarak güncelleştirilir. |
| Ürün reçeteleri | İkisi birden | İkisi birden | Bir ürünü tamamlandı olarak raporlamak ve bir üretim emri kullanmadan işlem sırasında tüketilen ham maddeleri tüketmek için bir ürün reçetesi (BOM) günlüğü kullanabilirsiniz. Bir ürün reçetesi günlüğü, genellikle mamul mal için en az bir pozitif satır ve tüketilen ham maddeler için bir veya daha fazla negatif satır içerir. Mamul mal satırı stoğa giriş olarak, negatif satırlar ise ham maddeler için stoktan çıkışlar olarak kabul edilir. Bir ürün reçetesi günlüğü oluşturduğunuzda, ilk satır ürün reçetesi üst bilgisidir ve eklenen sonraki satırlar ürün reçetesi satırlardır. |
| Stok sahipliği değişikliği | İkisi birden | İkisi birden | Stok sahipliği değişiklik günlüğü konsinye stoğun sahipliğini satıcıdan kuruluşuna değiştirmek için kullanılır. Stok sahipliği değişiklik günlükleri, iki stok hareketinin her bir satır ve stok boyutu birleşimiyle ilgili olması açısından stok transferi günlüklerine benzer. Bir stok hareketi, **Sahiplik** alanındaki satıcıdan stoğu kaldırır ve diğeri maddeyi **Sahiplik** boyutunda tüzel kişiliğe ekler. |
| Madde varışı | Giriş | Fiziksel | Gelen maddeler günlüğü, stoğun giriş durumunu **Kaydedildi** olarak güncelleştirmek için kullanılır. Genellikle malların ve satış siparişi iadelerinin satınalma siparişi girişi için kullanılır. |
| Üretim girişi | Giriş | Fiziksel | Üretim girişi günlüğü, gelen maddeler günlüğüne benzerdir. Üretim girişi, ambardaki bir üretim emrinden gelen mamul malları almak için kullanılır. Günlük nakledildiğinde, stok hareketinin durumu **Kaydedildi** olarak güncelleştirilir. |
| Sayım | İkisi birden | İkisi birden | Sayım günlüğü, belirli bir stok boyutları birleşimi için sayılan maddelerin miktarını kaydetmek için kullanılır. Stok hareketleri, günlüğün satırında sayım farkı olduğunda oluşturulur. Daha yüksek sayılmış bir miktara sahip satır stoğa girişe neden olur. Daha düşük sayılmış miktara sahip satır stoktan çıkışa neden olur. Sayılan miktarın beklenen miktarla eşleştiği satırlarda stok hareketi yoktur. |
| Etiket sayımı | Uygulanamaz | Uygulanamaz | Etiket sayım günlüğü, tam stok sayımında atanan ve kullanılan stok etiketlerini izlemek için kullanılır. Günlüğü, bir maddenin ve stok boyutunun belirli bir birleşimine etiket numarası atamak ve tam sayım sırasında bu etiketin durumunu izlemek için kullanabilirsiniz. Etiket sayımı günlükleri, stok hareketleri oluşturmaz. |
| Kalite emirleri | Sorun | Fiziksel | <p>Kalite emri, stoktaki belirli bir lotun test sonuçlarını kaydetmek için kullanılır. Her kalite emri, mevcut bir stok hareketiyle veya stok hareketinin bir bölümüyle ilgilidir.</p><p>Kalite emri, iki durumda yeni bir stok hareketi oluşturur:</p><ul><li>Kalite emri **Genel** sekmesinde **Bozucu test** olarak işaretlenmiştir.</li><li>Kalite emri, **Genel** sekmesinde **Doğrulama hatasından sonra karantinaya al** olarak işaretlenmiştir ve test doğrulamada başarısız olur. Bu durumda, iki stok hareketi oluşturulur. Bir stok hareketi, maddeyi orijinal stok boyut birleşimi ve yerleşiminden çıkarır, diğeri ise maddeyi karantina ambarına ekler.</li></ul> |
| Karantina emirleri | İkisi birden | İkisi birden | <p>Karantina emirlerinin stok hareketleri transfer emri gibidir. Karantina ambarı, stoğu izlemek için kullanılır. İki giriş hareketi ve iki çıkış hareketi vardır.</p><p>Emri ilk oluşturduğunuzda, iki hareket oluşturulur. Giriş hareketi, maddenin bulunduğu ambara bağlı karantina ambarı için **Sipariş Edildi** durumundadır. Çıkış hareketi, maddenin depolandığı ambar için **Siparişte** durumundadır.</p><p>Karantina emrini başlattığınızda, iki ek hareket oluşturulur ve mevcut hareketler güncelleştirilir. Karantina ambarı için giriş hareketinin durumu **Alındı** olarak güncelleştirilir ve depolama ambarı için çıkış hareketinin durumu **Düşülen** olarak güncelleştirilir.</p><p>İki yeni hareket, depolama ambarına geri dönüşe yönelik olası hareketi göstermek için kullanılır. Giriş hareketi, depolama ambarı için **Sipariş Edildi** durumundadır ve bu çıkış hareketi,karantina ambarı için **Fiziksel rezerve miktar** durumundadır.</p><p>Bir karantina emrini tamamlandı olarak raporladığınızda, bu işlem karantina emrinin fiziksel güncelleştirmesini temsil eder. Depolama ambarındaki giriş durumu **Alındı** olarak güncelleştirilir.</p><p>Karantina emrini tamamladığınızda bu işlem, karantina emrinin mali güncelleştirmesini temsil eder. Çıkış hareketlerinin durumu **Satıldı** olarak güncelleştirilir ve giriş hareketlerinin durumu **Satın Alındı** olarak güncelleştirilir.</p><p>Alternatif olarak, karantina emrini hurdaya çıkarabilirsiniz. Bu işlem maddeyi stoktan çıkarır. Bir karantina emrini hurdaya çıkardığınızda yalnızca üç işlem kalır. Depolama ambarı için giriş hareketi kaldırılır ve kalan giriş hareketinin durumu **Satın Alındı** olarak güncelleştirilir. İki çıkış hareketinin durumu **Satıldı** olarak güncelleştirilir. Bu işlem, sipariş için fiziksel ve mali bir güncelleştirmedir.</p> |

## <a name="fixed-receipt-price-posting"></a>Sabit giriş fiyatını deftere nakletme

Sabit giriş fiyatı, bir ürün için standart maliyet kullanmanızı sağlar. Bu, bir madde için **Madde model grubu** sayfasındaki **Standart maliyet** seçeneğini belirlemeye alternatiftir. Sabit giriş fiyatı kullandığınızda uygulanacak temel fark, stoğa giriş deftere nakledildiğinde madde için yapılandırılmış geçerli maliyet fiyatının kullanılacak olmasıdır. Sabit giriş fiyatı için maliyet yeniden değerleme işlemi yoktur. Bir mali güncelleştirme deftere nakledildiğinde, geçerli maliyet fiyatı deftere nakil sırasında kullanılır. Girişte kullanılan maliyet fiyatı ve fatura farklıysa bu fark, sabit giriş fiyatı kar ve zarar hesaplarına nakledilir.

İsteğe bağlı olarak bir ürün için sabit giriş fiyatı kullanmak üzere aşağıdaki yapılandırmayı tamamlamanız gerekir:

- Stok hareketi satırında seçili **Madde model grubu** sayfasındaki **Fiziksel stoğu deftere naklet** onay kutusunu seçin.
- **Madde model grubu** sayfasındaki **Sabit giriş fiyatı** onay kutusunu seçin.
- **Stok deftere nakil profili** sayfasında, aşağıdaki deftere nakil türleri için ana hesapları belirtin:

    - Sabit giriş fiyatı karı
    - Sabit giriş fiyatı zararı

Daha fazla bilgi için bkz: [Sabit giriş fiyatı](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="catch-weight-posting"></a>Fiili ağırlığı deftere nakletme

Fiili ağırlık ürünleri, genelde gıda endüstrisi gibi ürünlerin ağırlık, boyut veya her ikisi açısından kısmen değişebildiği endüstrilerde sıkça kullanılır. Fiili ağırlık ürünleri, stok birimi ve fiili ağırlık birimi olmak üzere iki ölçü birimi kullanır. Stoğun ambara girdiğindeki ağırlığı, stoğun ambardan çıktığındaki ağırlıktan farklı olabilir. Fiili ağırlık ürünün işlenmesi stoğu düzeltir.

Fiili ağırlıkta fark varsa bu farklar, **Stok deftere nakil profili** sayfasındaki **Fiili ağırlık zararı** ve **Fiili ağırlık karı** alanlarında belirtilen hesaplara nakledilir. Genellikle, her iki alanda da aynı ana hesap belirtilir.

Aşağıdaki tablo, varsayılan deftere nakil türlerine örnekler gösterir ve örnek ana hesapları ve açıklamaları içerir.

- "Borç/Alacak?" sütun, hareketin genellikle borçlandırdığını veya alacaklandırdığını gösterir. Bazı durumlarda, bir hareket borç veya alacak nakledebilir.
- "Kliring hesabı" sütunu, deftere nakil türünün bir kliring hesabı olduğunu belirtir. Diğer bir ifadeyle, sonraki bir hareket deftere nakledildiğinde, bu hesapta deftere nakledilen tutar için otomatik olarak ters işlem uygulanır.
- "P/F" sütunu deftere nakil türünü gösterir. "P" fiziksel deftere nakilleri, "F" mali deftere nakilleri temsil eder.
- "İzle" sütunu, deftere nakil türü ana hesabının genellikle başka bir deftere nakil türü ana hesabıyla aynı olup olmadığını gösterir. Özel olarak, genellikle deftere nakil için kullanılan deftere nakil türünü gösterir.

> [!NOTE]
> Tablodaki bu ana hesaplar ve ana hesap adları önerilerdir. İş gereksinimleriniz için en iyi yapılandırmayı belirlemek amacıyla muhasebeciniz ile çalışmanızı öneririz.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | P/F | İzle | Açıklama |
|---|---|---|---|---|---|---|---|---|
| Fiili ağırlık zarar hesabı | 510520 | Stok düzeltmesi | Gider | | No. | İkisi birden | Fiili ağırlık kar hesabı | Bu hesap, fiili ağırlık tutarının düşük olduğu bir stok hareketini deftere naklettiğinizde kullanılır. |
| Fiili ağırlık kar hesabı | 510520 | Stok düzeltmesi | Gider | | No. | İkisi birden | Fiili ağırlık zarar hesabı | Bu hesap, fiili ağırlık tutarının yüksek olduğu bir stok hareketini deftere naklettiğinizde kullanılır. |

Fiili ağırlık ürünleri hakkında daha fazla bilgi için bkz. [Fiili ağırlık maddeleri hakkında](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md) ve [Ambar yönetimiyle fiili ağırlık ürünü işleme](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Stoktan sabit kıymete transferi deftere nakletme

Stoktan sabit kıymete transfer günlüğü (**Sabit kıymetler** \> **Günlükler** \> **Stoktan sabit kıymete transfer günlüğü**), maddeleri stoktan çıkarıp sabit kıymetlere dönüştürmek için kullanılır. Daha fazla bilgi için bkz: [Sabit kıymet tümleştirmesi](/fixed-assets/fixed-asset-integration.md).

Aşağıdaki tablo, varsayılan deftere nakil türlerine örnekler gösterir ve örnek ana hesapları ve açıklamaları içerir.

- "Borç/Alacak?" sütun, hareketin genellikle borçlandırdığını veya alacaklandırdığını gösterir. Bazı durumlarda, bir hareket borç veya alacak nakledebilir.
- "Kliring hesabı" sütunu, deftere nakil türünün bir kliring hesabı olduğunu belirtir. Diğer bir ifadeyle, sonraki bir hareket deftere nakledildiğinde, bu hesapta deftere nakledilen tutar için otomatik olarak ters işlem uygulanır.
- "P/F" sütunu deftere nakil türünü gösterir. "P" fiziksel deftere nakilleri, "F" mali deftere nakilleri temsil eder.
- "İzle" sütunu, deftere nakil türü ana hesabının genellikle başka bir deftere nakil türü ana hesabıyla aynı olup olmadığını gösterir. Özel olarak, genellikle deftere nakil için kullanılan deftere nakil türünü gösterir.

> [!NOTE]
> Tablodaki bu ana hesaplar ve ana hesap adları önerilerdir. İş gereksinimleriniz için en iyi yapılandırmayı belirlemek amacıyla muhasebeciniz ile çalışmanızı öneririz.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | P/F | İzle | Açıklama |
|---|---|---|---|---|---|---|---|---|
| Sabit kıymet çıkışı | 180100 | Maddi sabit kıymetler | Varlık | Kredi | No. | İkisi birden | Uygulanamaz | Bu hesap, bir maddeyi stoktan çıkarmak ve sabit kıymete dönüştürmek için stoktan sabit kıymete transfer günlüğünü deftere naklettiğinizde kullanılır. |

## <a name="moving-average-posting"></a>Hareketli ortalamayı deftere nakletme

Hareketli ortalama, ortalama ilkesine dayalı kalıcı bir maliyetlendirme yöntemidir. Stok çıkışlarındaki maliyetler, satınalma maliyeti değiştiğinde değişmez. Fark aktifleştirilir ve orantısal bir hesaplamaya dayanır. Kalan tutar gider gösterilir.

Aşağıdaki tabloda örnek ana hesapları ve açıklamaları olan varsayılan deftere nakil türleri örnekleri gösterilmiştir.

- "Borç/Alacak?" sütun, hareketin genellikle borçlandırdığını veya alacaklandırdığını gösterir. Bazı durumlarda, bir hareket borç veya alacak nakledebilir.
- "Kliring hesabı" sütunu, deftere nakil türünün bir kliring hesabı olduğunu belirtir. Diğer bir ifadeyle, sonraki bir hareket deftere nakledildiğinde, bu hesapta deftere nakledilen tutar için otomatik olarak ters işlem uygulanır.
- "P/F" sütunu deftere nakil türünü gösterir. "P" fiziksel deftere nakilleri, "F" mali deftere nakilleri temsil eder.
- "İzle" sütunu, deftere nakil türü ana hesabının genellikle başka bir deftere nakil türü ana hesabıyla aynı olup olmadığını gösterir. Özel olarak, genellikle deftere nakil için kullanılan deftere nakil türünü gösterir.

> [!NOTE]
> Tablodaki bu ana hesaplar ve ana hesap adları önerilerdir. İş gereksinimleriniz için en iyi yapılandırmayı belirlemek amacıyla muhasebeciniz ile çalışmanızı öneririz.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | P/F | İzle | Açıklama |
|---|---|---|---|---|---|---|---|---|
| Hareketli ortalama için fiyat farkı | 510600 | Hareketli ortalama fiyat farkı | Gider | İkisi birden | No. | İkisi birden | Uygulanamaz | Bu hesap, giriş ile fatura arasında maliyet farkı olduğunda kullanılır. |
| Hareketli ortalama için yeniden değerleme | 510610 | Hareketli ortalama yeniden değerleme | Gider | İkisi birden | No. | İkisi birden | Uygulanamaz | Bu hesap, bir ürünün hareketli ortalama maliyetini düzelttiğinizde kullanılır |

## <a name="sample-posting-profile-configuration"></a>Örnek deftere nakil profili yapılandırması

Aşağıdaki tabloda örnek ana hesapları ve açıklamaları olan varsayılan deftere nakil türleri örnekleri gösterilmiştir.

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | P/F | İzle | Açıklama |
|---|---|---|---|---|---|---|---|---|
| Stok çıkışı | 140100 | Malzeme stoğu | Varlık | Kredi | No. | İkisi birden | Stok girişi | Bu hesap, deftere nakledilen bir stok hareketi çıkış (negatif miktar) olduğunda ve satış, satınalma veya üretimle ilişkili olmadığında kullanılır. Bu hesabın mahsubu, Stok harcaması, zarar hesabıdır. Bu hesap genellikle bilançonuzdaki stoğu temsil eder. |
| Stok harcaması, zarar | 510100 | Stok kar ve zararı | Gider | Borç | No. | İkisi birden | Stok harcaması, kar | Bu hesap, deftere nakledilen bir stok hareketi çıkış (negatif miktar) olduğunda ve satış, satınalma veya üretimle ilişkili olmadığında kullanılır. Bu hesabın mahsubu, Stok çıkışı hesabıdır. |
| Stok girişi | 140100 | Malzeme stoğu | Varlık | Borç | No. | İkisi birden | Stok çıkışı | Bu hesap, deftere nakledilen bir stok hareketi giriş (pozitif miktar) olduğunda ve satış, satınalma veya üretimle ilişkili olmadığında kullanılır. Bu hesabın mahsubu, Stok harcaması, kar hesabıdır. Bu hesap genellikle bilançonuzdaki stoğu temsil eder. |
| Stok harcaması, kar | 510100 | Stok kar ve zararı | Gider | Kredi | No. | İkisi birden | Stok harcaması, zarar | Bu hesap, deftere nakledilen bir stok hareketi giriş (pozitif miktar) olduğunda ve satış, satınalma veya üretimle ilişkili olmadığında kullanılır. Bu hesabın mahsubu, Stok girişi hesabıdır. |
| Birimler arası borç | 231500 | Birimler arası borç | Pasif | Borç | No. | İkisi birden | | Bu hesap, stoğun tesisler gibi stok boyutları arasında transfer edilmesi durumunda ve maddenin maliyeti tesisler arasında farklılık gösteriyorsa kullanılır. |
| Birimler arası alacak | 131500 | Birimler arası alacak | Varlık | Kredi | No. | İkisi birden | | Bu hesap, stoğun tesisler gibi stok boyutları arasında transfer edilmesi durumunda ve maddenin maliyeti tesisler arasında farklılık gösteriyorsa kullanılır. |
