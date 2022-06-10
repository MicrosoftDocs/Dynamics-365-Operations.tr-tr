---
title: Stok maliyetlendirme ile ilgili SSS
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta stok maliyetlendirme hakkında sık sorulan sorulardan bazıları yanıtlanır.
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 45f65bd4a5cfb9bd0c4eb03ceb56eca452f6ec95
ms.sourcegitcommit: cbe9493d479f96f271d94599ec1b85131b26169f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809298"
---
# <a name="inventory-costing-faq"></a>Stok maliyetlendirme ile ilgili SSS

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta stok maliyetlendirme hakkında sık sorulan sorulardan bazıları yanıtlanır.

## <a name="inventory-close-adjustments-and-recalculation"></a>Stok kapatma, düzeltme ve yeniden hesaplama işlemleri

### <a name="is-the-inventory-close-required"></a>Stok kapanışı zorunlu mu?

Stok arşivleme özelliğini kullanmayı planlıyorsanız, stok kapanışı gereklidir. Stok arşivleme özelliğini kullanmayı planlamıyorsanız, kullandığınız maliyetlendirme modellerinden bağımsız olarak yine de stok kapanışını çalıştırmanızı öneririz.

### <a name="how-often-should-the-inventory-close-be-run"></a>Stok kapanışı hangi sıklıkta çalıştırılmalıdır?

Stok kapanışı, her genel muhasebe dönemi başına en az bir kez çalıştırılmalıdır. Örneğin, genel muhasebeniz bir takvim ayı tabanlı mali takvim olarak ayarlanmışsa stok kapanışını ayda bir kez çalıştırmanız gerekir.

### <a name="is-the-inventory-recalculation-required"></a>Stok yeniden hesaplama işlemi zorunlu mu?

Hayır, stok yeniden hesaplama işlemi zorunlu değildir. İlk giren ilk çıkar (FIFO), son giren ilk çıkar (LIFO) veya ağırlıklı ortalama gibi bir dönemsel maliyetlendirme modeli kullanıyorsanız stok yeniden hesaplama işlemini çalıştırmanız gerekip gerekmediğini dikkatlice değerlendirmelisiniz. Seçtiğiniz buluşsal modellerde daha doğru maliyetlendirme sağlar.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Stok yeniden hesaplama işlemi hangi sıklıkta çalıştırılmalıdır?

Stok yeniden hesaplama işlemini çalıştırmayı planlıyorsanız, bu işlemi toplu işlem olarak her gün çalıştırmanız önerilir. Kuruluşunuz dönemsel maliyetlendirme modelleri için stok değerlerinin sıkça raporlanmasını gerektirmiyorsa, stok hesaplamasını daha az sıklıkla çalıştırabilirsiniz.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Kapanış ve düzeltmeler sayfasında eldeki stokların düzeltilmesi işlemini ne zaman kullanmalıyım?

Eldeki stokların düzeltilmesi, yalnızca bir stok kapanışı tamamlandıktan sonra çalıştırılabilir. Genellikle son kapanıştan sonraki tarih için çalışır. Eldeki stokların düzeltilmesi, yalnızca düzeltmeyi çalıştırdığınız tarih itibarıyla hala elde olan stoğu düzeltebilir.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Kapanış ve düzeltmeler sayfasında stok hareketinin düzeltilmesi işlemini ne zaman kullanmalıyım?

Stok hareketinin düzeltilmesi işlemini stok kapanışını çalıştırmadan önce kullanmalısınız. Genellikle yanlış bir girişi düzeltmek için kullanılır. Bir stok kapanışı çalıştırıldıktan ve hareket kapatıldıktan sonra stok hareketi düzeltmesini deftere nakledemezsiniz.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Stok kapanışı sırasında satınalma siparişi iadeleri diğer çıkışlarla aynı şekilde mi işlenir?

Evet. Satınalma siparişi girişi, madde için seçtiğiniz buluşsal modelde bir girişle karşılaştırılarak kapatılan bir çıkıştır. Dönemsel maliyetlendirme modeli kullanıyorsanız, buluşsal maliyeti geçersiz kılmak için işaretlemeyi kullanabilirsiniz.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Stok kapanışı sırasında satış siparişi iadelerine ne olur?

Stok kapanışını çalıştırdığınızda, satış siparişi iadesi stoğa giriş olarak kabul edilir. Çıkışlar, madde için seçtiğiniz buluşsal modele göre stokla karşılaştırılarak kapatılır.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Satış siparişi iadesi için hangi maliyet fiyatı kullanılır?

Bir satış siparişiyle ilişkili bir iade oluşturduğunuzda, **Birim fiyatı** alanının değeri orijinal satış siparişinden kopyalanır ve iadedeki **İade maliyet fiyatı** , iade edilen satış siparişi satırı için orijinal stok hareketindeki düzeltilmiş maliyet fiyatına ayarlanır. İlgili stok hareketi için **Değer açık** seçeneği *Evet* olarak ayarlanmışsa, stok kapanışı orijinal satış siparişindeki çıkış maliyetine güncelleştirme yapılmasına neden olabilir. Bu senaryoda, **İade maliyet fiyatı** alanı güncelleştirilmez. Ancak, bir sipariş iadesi sevk irsaliyesini deftere naklettiğinizde, sistem maliyet fiyatını denetler ve iade stok hareketinde güncelleştirilmiş maliyeti kullanır.

Bir satış siparişiyle ilişkili standart maliyet maddesinin iade işlemi için sistem, madde için yeni bir standart maliyet etkin olsa dahi, orijinal satış siparişinin gerçekleştirildiği zamandaki standart maliyeti kullanır.

Bir satış siparişiyle ilişkili olmayan bir iade oluşturduğunuzda, **İade maliyet fiyatı** alanı iade emrini oluşturduğunuz tesiste maddenin etkin madde fiyatına göre ayarlanır. Maddenin maliyetlendirme versiyonunda etkin maliyet fiyatı yoksa değer 0 (sıfır) olur. Değeri 0 (sıfır) olarak bırakırsanız iade lot kodunun veya iade maliyet fiyatının belirtilmediğini gösteren bir uyarı alırsınız.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Stok kapanışından beklenen performans nedir?

Birçok etken, stok kapanışının performansını etkileyebilir. Bu etkenler arasında toplam madde sayısı, dönemdeki toplam hareket sayısı, kullandığınız stok modelleri, stok ve ambar yönetimi parametrelerinde yapılandırdığınız toplu iş yardımcılarının sayısı yer alır. Kapanışın birkaç dakika kadar kısa bir sürede veya birkaç saatte tamamlanmasını bekleyebilirsiniz. Kapanışın çalışması için gereken süre ile ilgili özel bir yönerge yoktur. Stok kapanışının performansı için işlevsiz iş gereksinimlerinizi tanımlamanız ve stok kapanışı işlemini çalıştırma planını tanımlamak için iş ortağınızla sıkı bir işbirliğiyle çalışmanız gerekir. Stok kapanış işleminin beklenmedik bir şekilde düşük performans göstermesi durumunda, bir destek bileti açmalısınız.

## <a name="costing-sheet-and-indirect-costs"></a>Maliyetlendirme tablosu ve dolaylı maliyetler

### <a name="which-costing-models-support-the-costing-sheet"></a>Hangi maliyetlendirme modelleri maliyetlendirme tablosunu destekler?

Maliyetlendirme tablosu genellikle standart maliyetlendirme kullanan kuruluşlarda kullanılmakla birlikte, bunu Supply Chain Management'ta bulunan tüm maliyetlendirme modelleriyle kullanabilirsiniz.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Kuruluşumun çeşitli bölümleri için birden çok maliyetlendirme tablom olabilir mi?

Hayır. Her tüzel kişilik için yalnızca bir maliyetlendirme tablonuz olabilir.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Her tesis için farklı maliyetlendirme tablolarım olabilir mi?

Hayır, her tesis için farklı maliyetlendirme tablonuz olamaz. Her tüzel kişilik için yalnızca bir maliyetlendirme tablosu oluşturabilirsiniz. Ancak, her tesis için toplam düğümlerini, maliyet gruplarını veya dolaylı maliyet düğümlerini yapılandırabilirsiniz. Bu yapılandırma el ile gerçekleştirilen bir işlemdir. Kuruluş veya operasyonla ilgili değişiklikler olduğunda maliyetlendirme tablosundaki hiyerarşiyi ve madde atamalarını korumanız gerekir. Tek bir madde birden fazla tesiste üretiliyor veya satın alınıyorsa, maliyetlendirme tablosunda her tesis için maddeyi farklı şekilde değerlendirmenize olanak tanıyan bir mekanizma bulunmamaktadır. Ek olarak, tüm dolaylı maliyet kodlarının maliyetlendirme sürümünüzde tanımlanan bir fiyata veya ek ücrete sahip olduğunu unutmayın. Tanımladığınız maliyetler her zaman tesise özgüdür.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Maliyetlendirme tablosunun sürümlerini devre dışı bırakabilir ve etkinleştirebilir miyim?

Maliyetlendirme tablosu için herhangi bir ayrıntılı sürüm geçmişi tutulmasa da, maliyetlendirme tablosunda değişiklikler yapabilir, daha sonra hazır olduğunuzda tabloyu kaydedebilir ve doğrulayabilirsiniz. Maliyetlendirme tablosunun eski bir sürümüne geri gitmenize veya maliyetlendirme tablosunda yapılan değişiklikleri görüntülemenize olanak veren bir mekanizma yoktur. Değişiklikleri başlatır ve etkili olmasını istemezseniz, değişiklikleri kaydetmeden ve doğrulamadan bu sayfayı kapatabilirsiniz. Değişiklikleri atmak isteyip istemediğiniz sorulur.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Her madde için dolaylı maliyetler oluşturabilir miyim?

Maliyetlendirme tablonuzda, **Düğüm türü** alanının *Ek maliyet*, *Oran* veya *Çıkış birimi tabanlı* olarak ayarlandığı dolaylı maliyet kodları oluşturabilirsiniz. Daha sonra, madde numarasına özel olacak şekilde oran veya ek maliyet tanımlayabilirsiniz. **Oran** veya **Ek maliyet** hızlı sekmesinde, ızgaraya bir satır ekleyin. **Geçerli** alanını *Tablo* olarak, **İlişki** alanını belirli bir madde numarası olarak ayarlayın.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Belirli bir maddeyle ilgili olmayan bir dolaylı maliyet oluşturabilir miyim?

Evet. **Düğüm türü** alanının *Çıkış birimi tabanlı* olarak ayarlandığı bir dolaylı maliyet kodu oluşturabilirsiniz. Ardından, ürettiğiniz maddenin miktarını, ağırlığını veya hacmini belirtmek için **Alt tür** alanını *Miktar* , *Ağırlık* veya *Hacim* olarak ayarlayabilirsiniz. **Oran** hızlı sekmesinde belirttiğiniz oran seçtiğiniz alt türe uygulanır. Örneğin, **Alt tür** alanını *Miktar* olarak, **Oran** alanını *1,00 USD* olarak ayarladığınızı ve ardından miktarı 10 adet olan bir üretim veya toplu iş emri oluşturduğunuzu varsayalım. Bu durumda, mamule eklenecek dolaylı maliyet 10,00 USD'dir.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Üretim maliyetlerimi saat ve malzeme miktarına göre bölmek için maliyetlendirme tablosunu kullanabilir miyim?

Evet. Maliyetleri, istediğiniz gruplandırmaya göre ayırmak için maliyetlendirme tablonuzda **Toplam** düğümleri oluşturabilirsiniz. Örneğin, *Saatler* olarak adlandırılan ve *Malzemeler* olarak adlandırılan iki ayrı **Toplam** düğümü oluşturabilirsiniz. **Saatler** düğümü altında, saatlerinizle ilgili her bir kod grubunu ekleyin. **Malzemeler** düğümü altında, malzemelerinizle ilgili her bir maliyet grubunu ekleyin.

## <a name="dimension-groups"></a>Boyut grupları

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Maliyeti parti veya seri numarası düzeyinde yönetebilir miyim?

Evet. FIFO, LIFO, LIFO tarihi, ağırlıklı ortalama veya ağırlıklı ortalama tarihi gibi dönemsel bir maliyetlendirme modeli kullanıyorsanız, maliyetleri ayrıntılı bir düzeyde izlemek için izleme boyutu grubunda **Parti** veya **Seri numarası** için **Mali stok** seçeneğini etkinleştirin.

### <a name="can-i-manage-costs-at-the-location-level"></a>Maliyetleri yerleşim düzeyinde yönetebilir miyim?

Hayır. Depolama boyutu grubundaki **Yerleşim** boyutu için **Mali stok** seçeneğini etkinleştiremezsiniz. Kuruluşunuzun maliyetleri daha ayrıntılı bir düzeyde izlemesi gerekiyorsa, sanal ambarlar oluşturup oluşturamayacağınızı değerlendirin ve ardından depolama boyutu grubunuzdaki **Ambar** boyutu için **Mali stok** seçeneğini belirleyin.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Depolama boyutu grubu için Ambar yönetimi süreçlerini kullan seçeneğini etkinleştirmeli miyim?

İleride ileri düzey ambar yönetimi özelliklerini kullanmak isteyebileceğinizi düşünüyorsanız, **Ambar yönetimi süreçlerini kullan** seçeneğini etkinleştirmelisiniz. Depolama boyutu grubunu kaydettikten sonra, grubun **Ambar yönetimi süreçlerini kullan** seçeneğinin ayarını değiştiremezsiniz. İleride ambar yönetimi süreçlerini kullanmaya karar verirseniz seçeneğin etkin olduğu yeni bir ambar oluşturmanız gerekir. Tüm stoğu bir ambardan başka bir ambara taşımak veya ilgili yapılandırmaları yeni bir ambara kopyalamak için kullanabileceğiniz otomatik bir işlem yoktur.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-advanced-warehousing"></a>İleri düzey ambar özelliklerini kullanmayı planlamadığım halde, depolama boyutu grubu için Ambar yönetimi süreçlerini kullan seçeneğini etkinleştirebilir miyim?

Evet, ileri düzey ambar yönetimi özelliklerini kullanmayı planlamasanız bile, depolama boyutu grubu için **Ambar yönetimi süreçlerini kullan** seçeneğini etkinleştirebilirsiniz. Hareketleri oluşturmak ve işlemek için rezervasyon hiyerarşileri ve birim sıra grupları gibi minimum düzeydeki yapılandırmaları tamamlamanız gerekir. Ancak, malzeme çekme listelerini, sevk irsaliyelerini ve ürün girişlerini (ör. satış siparişi ve satınalma siparişi sayfalarında) el ile işlediğinizde, ileri düzey ambar özelliklerinin ayarları genellikle yoksayılır.

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Depolama veya izleme boyutu grubu için Fiziksel stok seçeneğini ne zaman etkinleştirmem gerekir?

Depolama ve izleme boyutunu temel alan ayrıntılı stok kayıtları tutmanız gerektiğinde söz konusu boyut grubu için **Fiziksel stok** seçeneğini etkinleştirmeniz gerekir. Genellikle, etkin olan boyutlar fiziksel olarak da izlenir. Böylece, stoktaki tüm giriş, çıkış veya stok hareketleri seçili boyuta göre izlenir. Boyut zorunlu değilse (ör. plaka), boyut belirtilmediğinde bile kullanıcıların stoğu almasına, çıkarmasına veya taşımasına izin vermek için **Boş girişe izin verilir** ve **Boş çıkışa izin verilir** seçeneklerini etkinleştirebilirsiniz.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Depolama veya izleme boyutu grubu için Mali stok seçeneğini ne zaman etkinleştirmem gerekir?

Depolama ve izleme boyutunu temel alan ayrıntılı mali kayıtlar tutmanız gerektiğinde söz konusu boyut grubu için **Mali stok** seçeneğini etkinleştirmeniz gerekir. **Tesis** boyutları her zaman mali olarak izlenir ancak diğer boyutlar için mali izleme isteğe bağlıdır. FIFO, LIFO veya ağırlıklı ortalama gibi dönemsel bir maliyetlendirme modeli kullanıyorsanız, bir boyut için **Mali stok** seçeneğini etkinleştirmek, yalnızca giriş ve çıkışın aynı boyut değerlerine sahip olduğu durumlarda kapatma işlemi yapacağınızı gösterir. Örneğin, **Ambar** boyutu için **Mali stok** seçeneğini etkinleştirirseniz, her ambar için farklı bir maliyetiniz olur ve farklı ambarlardaki giriş ve çıkışlar kapatılamaz.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Hareketler gerçekleştikten sonra ürün, depolama veya izleme boyutu grubunda değişiklik yapabilir miyim?

Madde modeli grubu oluşturduktan sonra, madde modeli grubunda bir boyut için **Etkin** onay kutusu seçiliyse **Boyuta göre tedarik planı**, **Satınalma fiyatları için** ve **Satış fiyatları için** alanlarının ayarlarını değiştirebilirsiniz. Başka değişikliğe izin verilmez. Örneğin; **Etkin**, **Boş çıkışa izin verilir**, **Boş girişe izin verilir**, **Fiziksel stok** ve **Mali stok** seçeneklerini etkinleştiremez veya devre dışı bırakamazsınız.

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Serbest bırakılan bir ürünle ilgili ürün, depolama veya izleme boyutu grubunu değiştirebilir miyim?

Bir ürün için eldeki stok 0 (sıfır) ise ve **Değer açık** seçeneği tüm stok hareketleri için *Hayır* olarak ayarlanmışsa, serbest bırakılmış üretim sayfasındaki depolama ve izleme boyutu gruplarını değiştirebilirsiniz. Kayıt oluşturulduktan sonra ürün boyutu grubunu değiştiremezsiniz.

## <a name="item-model-groups"></a>Madde model grupları

### <a name="when-should-i-enable-the-stocked-product-option"></a>Stoğu tutulan ürün seçeneğini ne zaman etkinleştirmeliyim?

Stoğunuzda izlenecek her madde için **Stoğu tutulan ürün** seçeneğini etkinleştirmeniz gerekir. Bu seçenek etkinleştirildiğinde, maddenin girişini ve çıkışını izleyen ayrıntılı stok hareketleri saklanır. Bu seçenek, örneğin ambarınızda tuttuğunuz tüm somut maddeler için etkinleştirilir. Ayrıca ürün reçetelerinize (BOM) veya formüllerinize somut olmayan bir madde (ör. servis maddesi) eklemeyi planlıyorsanız bu seçeneği etkinleştirmelisiniz. **Stoğu tutulan ürün** seçeneğini etkinleştirmezseniz, Stok yardımcı defterinde stok hareketleri izlenmez ve maddelerin maliyeti genellikle genel muhasebe defterinizde giderleştirilir. Bu seçenek genellikle ürün reçetelerinize veya formüllerinize eklenmeyen mağaza gereçleri veya servisleri için kullanılır.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Fiziksel stoğu deftere naklet seçeneğini ne zaman etkinleştirmem gerekir?

**Fiziksel stoğu deftere naklet** seçeneği, genellikle **Stoğu tutulan ürün** seçeneği etkinleştirildiğinde etkinleştirilir. Bu seçeneği etkinleştirdiğinizde, sistem stok hareketinde maddeyle ilgili fiziksel güncelleştirmeyi izler. Bu seçenek, fiziksel güncelleştirmenin fiş oluşturması gerektiğini belirten Borç hesapları, Alacak hesapları ve Üretim denetimindeki parametrelerle birlikte kullanılır. Bu seçeneği genellikle, stoğu fiziksel olarak güncelleştirdiğinizde genel muhasebe defterinin güncelleştirilmesini istediğinizde etkinleştirirsiniz. Supply Chain Management mali kayıtlar için kayıt sisteminiz değilse, bu seçeneği devre dışı bırakmanız önerilir.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Mali stoğun deftere nakli seçeneğini ne zaman etkinleştirmeliyim?

**Mali stoğun deftere nakli** seçeneği, genellikle **Stoğu tutulan ürün** seçeneği etkinleştirildiğinde etkinleştirilir. Bu seçenek, mali güncelleştirmenin fiş oluşturması gerektiğini belirten Borç hesapları, Alacak hesapları ve Üretim denetimindeki parametrelerle birlikte kullanılır. Bu seçeneği genellikle, stoğu mali olarak güncelleştirdiğinizde (ör. satış siparişlerini ve satınalma siparişlerini faturalayarak veya bir üretim emrini sona erdirerek) genel muhasebe defterinin güncelleştirilmesini istediğinizde etkinleştirirsiniz. Supply Chain Management mali kayıtlar için kayıt sisteminiz değilse, bu seçeneği devre dışı bırakmanız önerilir.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Satış Teslimatındaki Ertelenmiş Gelir Hesabına Naklet seçeneğini ne zaman etkinleştirmeliyim?

**Satış Teslimatındaki Ertelenmiş Gelir Hesabına Naklet** seçeneğini, satış siparişi için sevk irsaliyesi naklettiğinizde genel muhasebe defterinde gelirin kabulünü isteyip istemediğinizi belirtmek için kullanırsınız. Bu seçenek genellikle bir satış siparişindeki sevk irsaliyesi ve fatura arasında uzun bir gecikme olduğunda veya dönemdeki tüm satış siparişlerini faturalamak mümkün olmadığında kullanılır. Genellikle, sevk irsaliyesini deftere naklettikten hemen sonra satış siparişi faturalarınızı deftere naklediyorsanız bu seçeneği devre dışı bırakırsınız. Böylece, bir satış siparişini faturaladığınızda hemen ters kaydedilecek ek genel muhasebe defteri nakilleri oluşturmanın önüne geçmiş olursunuz.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Ürün girişinde borcu tahakkuk ettir seçeneğini ne zaman etkinleştirmeliyim?

Çoğu kuruluşta, stoğu tutulan ürün veya stoğu tutulmayan ürününüz olup olmamasına bakılmaksızın, tüm madde modeli grupları için **Ürün girişinde borcu tahakkuk ettir** seçeneğinin etkinleştirilmesi istenir. Bu seçenek, ürün girişi fiyatına göre bir tahakkuku genel muhasebe defterine nakletmek için kullanılır. Genellikle bir satınalma siparişinin ürün girişinin deftere nakli ile faturanın deftere nakli arasında gecikme olduğundan çoğu kuruluş, Genel Kabul Görmüş Muhasebe Uygulamaları (GAAP) gibi yerel düzenlemelere uyum sağlamak için bilançoda borcu kabul etmelidir. Supply Chain Management mali kayıtlar için kayıt sisteminiz değilse, bu seçeneği devre dışı bırakmanız önerilir. Kuruluşunuz satınalma siparişlerinde tedarik kategorileri kullanıyorsa **Satınalma ilkeleri** sayfasındaki kategori ilkesi kuralı için **Girişte satın alma giderini tahakkuk ettir** seçeneğini etkinleştirerek tahakkuk şartını denetleyebilirsiniz.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Giriş kaydı henüz deftere nakledilmemişse, bir kullanıcının satınalma siparişi ürün girişini deftere nakletmesini nasıl önleyebilirim?

Madde model grubu için **Kayıt gereksinimleri** seçeneğini etkinleştirerek, satınalma siparişi kaydının henüz gerçekleşmediği durumlarda kullanıcıların satınalma siparişi ürün girişini deftere nakletmesini önleyebilirsiniz. Bu seçenek genellikle iki aşamalı alma sürecini kullanan kuruluşlarda veya aldığınız maddelerdeki parti veya seri numarasını kaydetmeniz gereken durumlarda kullanılır. **Kayıt gereksinimleri** seçeneği yalnızca satınalma siparişlerinde değil bir maddenin *tüm* stok girişlerinde geçerli olur. Örneğin, pozitif miktara sahip bir stok günlüğü ve üretim emri tamamlandı bildirimi günlüğü için geçerlidir.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Ürün girişi henüz deftere nakledilmemişse, kullanıcıların satınalma siparişi faturasını deftere nakletmesini nasıl önleyebilirim?

Madde model grubu için **Alma gereksinimleri** seçeneğini etkinleştirerek, satınalma siparişi ürün girişinin henüz gerçekleşmediği durumlarda kullanıcıların satınalma siparişi ürün faturasını deftere nakletmesini önleyebilirsiniz. Bu seçenek genellikle tahakkuk için girişlerin genel muhasebe defterine fiziksel olarak kabulünü gerektiren kuruluşlarda kullanılır. **Alma gereksinimleri** seçeneği yalnızca satınalma siparişlerinde değil bir maddenin *tüm* stok girişlerinde geçerli olur. Örneğin, pozitif miktara sahip bir stok günlüğü ve üretim emri tamamlandı bildirimi günlüğü için geçerlidir. Kuruluşunuz satınalma siparişlerinde tedarik kategorileri kullanıyorsa **Satınalma ilkeleri** sayfasındaki kategori ilkesi kuralı için **Alma gereksinimleri** seçeneğini etkinleştirerek giriş gereksinimini denetleyebilirsiniz.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Satış siparişi malzeme çekme listesi henüz deftere nakledilmediyse kullanıcıların satış siparişi sevk irsaliyesini deftere nakletmesini nasıl önleyebilirim?

Madde model grubu için **Malzeme çekme gereksinimleri** seçeneğini etkinleştirerek, satış siparişi malzeme çekme listesinin henüz gerçekleşmediği durumlarda kullanıcıların satış siparişi sevk irsaliyesini veya faturasını deftere nakletmesini önleyebilirsiniz. Bu seçenek genellikle ambarda fiziksel malzeme çekme işlemi gerçekleştiren (ör. malzeme çekme işlemi için ambar mobil aygıtını kullanan) kuruluşlarda kullanılır. **Malzeme çekme gereksinimleri** seçeneği yalnızca satış siparişlerinde değil bir maddenin *tüm* stok çıkışlarında geçerli olur. Örneğin, negatif miktara sahip bir stok günlüğü ve üretim emri malzeme çekme listesi günlüğü için geçerlidir.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Satış siparişi sevk irsaliyesi henüz deftere nakledilmediyse kullanıcıların satış siparişi faturasını deftere nakletmesini nasıl önleyebilirim?

Madde model grubu için **Kesinti gereksinimleri** seçeneğini etkinleştirerek, satış siparişi sevk irsaliyesinin henüz gerçekleşmediği durumlarda kullanıcıların satış siparişi faturasını deftere nakletmesini önleyebilirsiniz. Bu seçenek genellikle ambarda fiziksel bir sevk işlemi gerçekleştiren (ör. sevk işlemini yapmak için Warehouse Management mobil uygulamasını kullanan veya sevk edilen maddelere eklenecek bir belge oluşturan) kuruluşlarda kullanılır. **Kesinti gereksinimleri** seçeneği yalnızca satış siparişlerinde değil bir maddenin *tüm* stok çıkışlarında geçerli olur. Örneğin, negatif miktara sahip bir stok günlüğü ve üretim emri malzeme çekme listesi günlüğü için geçerlidir.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Kaydedilen maddelerin satılmasını engelleyebilir miyim?

Bir madde, Supply Chain Management'ta stoğunuza kaydedildiğinde miktar sistemde fiziksel olarak çıkışa uygundur. Kaydedilen ancak henüz teslim alınmamış maddelerin satış siparişlerinde veya üretim emirlerinde çıkış için *kullanılmaması* gerekiyorsa, iş sürecini yönetmek için stok durumu, stok durdurma, kalite emirleri, karantina emirleri veya rezervasyonları kullanabilirsiniz.

## <a name="production-costing"></a>Üretim maliyetlendirme

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Ham maddeler için ayrı mamul mallar için ayrı bir maliyetlendirme modeli kullanabilir miyim?

Evet, her madde için farklı maliyetlendirme modelleri kullanabilirsiniz. Üreticilerin ham maddeler için dönemsel bir maliyetlendirme modeli; yarı mamul ve mamul mallar içinse standart maliyet kullanması yaygın görülen bir durumdur.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Genel gideri makine maliyetlerimden nasıl ayırabilirim?

Genel gideri makine maliyetlerinizden ayırmak için iş gereksinimlerinize göre her bir makine için kaynaklar ve kaynak grupları oluşturmanız gerekir. Her kaynak veya kaynak grubu, makinenin maliyetini denetlemek için maliyet kategorilerine atanabilir. Her maliyet kategorisi bir maliyet grubuyla bağlantılı olabilir ve her maliyet grubu, maliyetlendirme tablosunda dolaylı maliyetlerin hesaplanmasında temel olarak kullanılabilir.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Maliyetlendirme tablosunda enerji tüketimi (ör. su, enerji veya gaz tüketimi) ile ilgili maliyeti nasıl ayırt edebilirim?

Enerji tüketimiyle ilişkili maliyetleri genellikle iki yöntemden biriyle ayırt edebilirsiniz:

- Ürün reçetenizde veya formülünüzde bir satır oluşturun. Genellikle, bu satır bir servis maddesi olarak oluşturulur ve ürettiğiniz miktara karşılık tükettiğiniz miktarın ölçü birimini belirtebilirsiniz. Bu şekilde, kullanıcı üretim sürecinde farklı bir tutarı tüketebilir. Maddeleri, **Otomatik tüketim kuralı** alanında seçtiğiniz değere göre otomatik olarak tüketebilirsiniz.
- Maliyetlendirme tablonuzda dolaylı maliyet oluşturun. Genellikle bu yaklaşım, üretim süreciniz genelinde enerji tüketiminin toplam maliyetini tahsis etmek için kullanılır. Örneğin, rotanızdaki malzeme veya iş gücünü temel alarak tüketimi ölçeklendirmek için maliyet grubunu ve içe alma temelini kullanabilirsiniz.

Raporlama, mutabakat ve operasyonel gereksinimlerinize göre en iyi seçeneği seçmeniz gerekir.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Ürün reçetesinde veya formülde kaynak ayrıntılarını yakalayabilir miyim?

Kaynak ayrıntıları yalnızca rota işleminde yakalanabilir. Kaynağı temsil etmesi için bir servis maddesi oluşturabilir ve mamul malın maliyet hesaplamasını artırmak için bir maliyet atayabilirsiniz ancak bu yaklaşımı genellikle önermeyiz. Bunun yerine, kaynak maliyetlerini izlemek için tek bir satırı bulunan basit bir rota oluşturmanızı ve operasyonu, üretim emrinin başlangıcında veya sonunda otomatik olarak tüketilecek şekilde yapılandırmanızı öneririz.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Maliyet el ile girilirse hesaplama ayrıntılarını görebilir miyim?

Hayır. Fiyatı **Madde fiyatı** sayfasına el ile girerseniz, **Hesaplama ayrıntılarını görüntüle** ve **Rapor hesaplama ayrıntıları** düğmeleri kullanılamaz. El ile girilen bir maliyet fiyatı için **Maliyet grubuna göre maliyet toplaması** düğmesini seçerseniz, özetlenen bir satır görüntülenir ve tüm maliyetler mamul maddede toplanır.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Maliyeti el ile girdiğimde sistem, üretim emrindeki farkları hesaplar mı?

Evet, standart maliyeti el ile girdiğinizde farkları hesaplar. Ancak, standart bir maliyeti hesaplamak yerine el ile girdiğinizde, üretim emrindeki tüm malzeme, rota ve dolaylı maliyet tüketimleri değiştirme farkı olarak kabul edilir. Ek malzeme veya iş gücü tüketimi gibi başka farklar varsa, bunlar da ürün reçetesinde fark olarak kaydedilir. Bu nedenle, ürün reçetesi, rota veya dolaylı maliyetleri olan maddeler için her zaman hesaplama çalıştırmanızı öneririz.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Bir alt üretim emrindeki farkları ana üretim emrine nasıl taşıyabilirim?

FIFO, LIFO veya ağırlıklı ortalama gibi dönemsel bir maliyetlendirme modeli kullanıyorsanız, alt üretimdeki maliyetler maddeler için seçtiğiniz buluşsal modelde tanınır. Fiili maliyetlendirme gerekiyorsa, hangi alt üretimin üst üretim emrine çıkış yaptığını göstermek için işaretleme ilkesini kullanabilirsiniz. Alternatif olarak, izleme boyutu grubunda **Parti** veya **Seri numarası** boyutu için **Mali stok** seçeneğini kullanabilirsiniz.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Otomatik tüketim kuralı tüketimi nasıl etkiler?

Bir ürün reçetesinde, formülde veya rota satırında otomatik tüketim kuralı, maddeyi veya iş gücünü tüketmek için kullanılan zamanlamayı ve tekniği denetler. *Başlangıç* seçeneğini seçerseniz üretim emrini başlattığınızda madde veya iş gücü otomatik olarak tüketilir. *Bitiş* seçeneğini seçerseniz üretim emrinin bittiğini bildirdiğinizde madde veya iş gücü otomatik olarak tüketilir. *El ile* seçeneğini seçerseniz, bir kullanıcının malzemeleri el ile çekmesi veya zamanı iş veya rota kartı günlüğüne kaydetmesi gerekir. Ürün reçeteleri ve formüllerde *Yerleşimde kullanılabilir* seçeneği de bulunur. Bu seçeneği belirlerseniz, maddeler üretim katı yerleşimine aktarıldıktan sonra otomatik olarak tüketilir.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Çok düzeyli ürün reçetelerim veya formüllerim varsa, maliyet hesaplamalarını nasıl çalıştırmalıyım?

Genel olarak, hesaplama için ürün reçetelerinizin veya formüllerinizin en alt düzeyinde başlamanızı öneririz. Maliyet hesaplamalarını toplu olarak çalıştırdığınızda filtre uygulanmasını kolaylaştırmak için, ürünleri ayırmak amacıyla hesaplama gruplarını kullanabilirsiniz. Maliyet hesaplamalarını toplu olarak çalıştırmaya başlamadan önce, *Ürün reçetesi düzeylerini yeniden hesapla* periyodik işini çalıştırmanızı öneririz. Her kuruluş, ürün karışımı üzerinde düşünmeli ve ürün ile ürün reçetesi veya formül yapılarının belirli ihtiyaçlarını karşılayan bir strateji tanımlamalıdır.

## <a name="transfer-order-costing"></a>Transfer emri maliyetlendirmesi

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Transfer emri maliyetine navlun tahsis etme yöntemi var mı?

Maliyetleri eklemek için transfer emrine masraf ekleyebilirsiniz. Masraflar kodu, eklediğiniz masrafın borcunu ve alacağını tanımlar. Öncelikle **Stok yönetimi** modülünde masraf kodları oluşturmanız gerekir. Bir transfer emrine masraf eklemek için masraf eklemek istediğiniz transfer emri satırında **Masraflar**'ı seçin.

## <a name="variances"></a>Farklar

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Tesise veya ambara göre farkları farklı şekilde işleyebilir miyim?

Tesise göre fark hesaplarını yapılandırma seçeneği yoktur. Serbest bırakılan bir ürün için standart maliyetlendirme kullandığınızda, **Deftere Nakil** sayfasındaki standart maliyet farkı deftere nakilleri için kullanılan ana hesabı seçebilirsiniz. Bir madde, bir madde grubu veya tüm maddeler için hesapları yönetmeyi seçebilirsiniz. Ayrıca bir maliyet grubunu, bir grup maliyet grubunu veya tüm maliyet gruplarını yapılandırabilirsiniz.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Diğer fark türlerindeki para birimi döviz kurlarının sonucu olan farkları ayırabilir miyim?

Bir fark, satınalma siparişi fiyatı ile bir maddenin standart maliyeti arasındaki döviz kuru farkının sonucuysa döviz kuru farkını diğer farklardan ayırmanın bir yolu yoktur.

## <a name="reporting"></a>Raporlama

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Kaç adet stok değeri rapor yapılandırması oluşturabilirim ve kullanabilirim?

Oluşturabileceğiniz stok değeri rapor yapılandırmalarının sayısıyla ilgili bir sınır yoktur. Belirli raporlama gereksinimlerinizi değerlendirmeniz ve bu gereksinimleri karşılamak için gereksinim duyduğunuz sayıda yapılandırma oluşturmanız gerekir. Raporu veya rapor depolama seçeneğini çalıştırmak için en az bir stok değeri raporu yapılandırmasına gerek vardır.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Her bir ambardaki maddenin maliyetini analiz etmek için stok değeri raporunu kullanabilir miyim?

Evet. Stok değeri rapor yapılandırmasındaki her **Ambar** boyutu için **Görünüm** veya **Toplam** seçeneğini etkinleştirebilirsiniz. Ancak, rapor yalnızca depolama boyutu grubu için **Mali stok** seçeneğinin etkin olduğu boyutların değerlerini gösterir. Diğer boyutlar için yalnızca boş sütunları gösterir. Daha fazla bilgi için bkz. [Stok değer raporu örnekleri ve mantığı](inventory-value-report-examples.md).

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Ağırlıklı ortalamaya göre belirli bir tarihten itibaren stok miktarını nasıl görüntüleyebilirim?

Belirli bir tarihe ait stok değerini gösteren **Ortalama birim maliyeti** sütununu içeren **Stok eskimesi** raporunu kullanabilirsiniz. Daha fazla bilgi için bkz. [Stok eskimesi raporu örnekleri ve mantığı](inventory-aging-report.md).

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Bir çıkış hareketine karşılık olarak hangi giriş hareketlerinin kapatıldığını nasıl görüntüleyebilirim?

**Stok hareketi** veya **Stok hareketi ayrıntıları** sayfasının Eylem bölmesindeki **Stok** sekmesinde bulunan **Kapatmalar**'ı veya **Maliyet gezgini**'ni seçerek bir stok hareketiyle ilgili kapatma işlemlerini görüntüleyebilirsiniz. Hareketle ilgili çıkışları görmek için bir giriş seçerseniz, maliyet gezgini ayrıntıları göstermez. Ayrıntılar yalnızca bir çıkış hareketi seçerseniz gösterilir.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Stok değeri raporu, pozitif fiziksel miktara ve negatif mali değere sahip maddeleri nasıl gösterir?

Stok değeri raporu, fiziksel ve mali tutarları ve miktarları kendi sütunlarına ayırır. Raporda gösterilen değerler, raporu çalıştırdığınızda seçtiğiniz tarih aralığı itibarıyla geçerli değerlerdir. Gösterilen özetleme düzeyi, seçtiğiniz ayarlara bağlıdır. Bir madde için fiziksel olarak alınan ve mali olarak çıkış yapılan hareketler varsa, miktarlar ve değerler bağımsız olarak toplanır. Ayrıntı düzeyini hareket olarak görüntülemeyi seçtiyseniz, her giriş ve çıkış satırı ayrı olarak gösterilir ve sırasıyla fiziksel ve mali miktarlar ve tutarlar gösterilir. Daha fazla bilgi için bkz. [Stok değer raporu örnekleri ve mantığı](inventory-value-report-examples.md).

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Depolama ve izleme boyutu gruplarının stok değeri raporu üzerindeki etkileri nelerdir?

Depolama veya izleme boyutu grubunda bir boyut için **Mali değer** seçeneğini etkinleştirirseniz, stok değeri raporu yapılandırmasında boyut için **Görünüm** veya **Toplam** seçeneğini belirleyebilirsiniz. **Mali değer** seçeneğinin işaretli olmadığı bir boyut için **Görünüm** veya **Toplam** seçeneğini belirlerseniz, rapor çıktısında sütun boş olacaktır. Depolama veya izleme boyutu grubunda bir boyut için **Mali değer** seçeneğini etkinleştirdiyseniz ve stok değeri raporu yapılandırmasında **Görünüm** veya **Toplam** seçeneğini seçmediyseniz sistem, seçili boyutların mali olarak izlendiği değerleri özetler.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Maliyetlendirme için Power BI katıştırılmış raporlarını özelleştirebilir miyim?

Evet. Doğru güvenlik izinlerine sahip kullanıcılar Supply Chain Management'taki tüm Power BI katıştırılmış raporları için rapor tasarım tuvalini güncelleştirebilir. Daha fazla bilgi için bkz. [Analiz çalışma alanlarında katıştırılmış raporları özelleştirme](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md).

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Fark analiz ekstresini nerede görüntüleyebilirim?

Fark analizi ekstresine, **Maliyet yönetimi \> Sorgular ve raporlar \> Stok muhasebesi – analiz raporları** veya **Maliyet yönetimi \> Sorgular ve raporlar \> Üretim muhasebesi – analiz raporları** bölümüne giderek erişebilirsiniz. Her iki seçenek de aynı raporu açar ve rapor da aynı davranışa sahiptir.

## <a name="item-prices-and-default-costs"></a>Madde fiyatları ve varsayılan maliyetler

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Her ürün çeşidinin maliyetini belirleyebilir miyim?

Evet. Ürün çeşidine göre fiyatlandırmayı etkinleştirmek için, **Serbest bırakılan ürün** sayfasının **Maliyeti yönet** hızlı sekmesindeki **Çeşide göre maliyet fiyatı kullan** seçeneğini etkinleştirebilirsiniz. (Bu seçenek yalnızca ana ürünler için kullanılabilir.) Ardından, **Yapılandırma**, **Boyut**, **Renk** veya **Stil** boyutunu göstermek isteyip istemediğinizi belirtmek için **Madde fiyatı** sayfasında (**Maliyetlendirme sürümü** sayfasından veya **Serbest bırakılan ürün** sayfasından açılabilir) **Boyutların görünümü**'nü seçebilirsiniz. Ayarları kaydetmek ve sayfayı her açışınızda seçili boyutları kullanmak için **Kurulumu kaydet** seçeneğini etkinleştirin ve **Tamam**'ı seçin. Yalnızca boyutların ürün boyutu grubunda etkin olduğu maddeler için boyutları girebilirsiniz.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Her ambar için maliyet belirleyebilir miyim?

Hayır, madde fiyatını ambara göre belirleyemezsiniz. Ancak, ambara göre satınalma fiyatları veya satış fiyatları için ticari sözleşmeleri belirleyebilirsiniz. İlk olarak, **Depolama boyutu grubu** sayfasındaki boyuta yönelik olarak **Satınalma fiyatları için** veya **Satış fiyatları için** seçeneklerinden birini seçin. Artık, ticari sözleşme günlüğü oluşturduğunuzda ve boyutların satırlarını açtığınızda, ızgarada hangi boyutun gösterileceğini seçmek için **Stok \> Boyutları görüntüle**'yi seçin. Ayarları kaydetmek ve sayfayı her açışınızda seçili boyutları kullanmak için **Kurulumu kaydet** seçeneğini etkinleştirin ve **Tamam**'ı seçin. Yalnızca boyutların ürün boyutu grubunda etkin olduğu maddeler için boyutları girebilirsiniz.

### <a name="what-are-price-charges"></a>Fiyat masrafları nedir?

Fiyat masrafları, madde fiyatının veya ticari sözleşmenin birim fiyatına sabit bir tutar ekleme yöntemi sunar. **Fiyat masrafları** alanına tutar girdiğinizde, **Masraf miktarı** alanına da bir değer girebilirsiniz. Fiyat masraflarına, belirttiğiniz masraf miktarı üzerinden amortisman uygulanır. Fiyat masraflarını maddenin birim fiyatına dahil etmek istiyorsanız, **Birim fiyata ekle** seçeneğini etkinleştirin. Bu seçenek standart maliyet için her zaman etkindir.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Birden çok para birimi cinsinden tedarik edilen maddeler için fiyatı nasıl yapılandırmalıyım?

**Serbest bırakılan ürün** sayfasındaki **Satınalma fiyatı** alanına varsayılan fiyat girerseniz, bu fiyatın açık olan tüzel kişiliğin genel muhasebe defteri para birimi cinsinden olduğu varsayılır. Benzer şekilde, **Fiyat türü** alanının *Satınalma* olarak ayarlandığı bir maliyet sürümünde satınalma fiyatı girerseniz, fiyatın tüzel kişiliğinizin muhasebe para biriminde olduğu varsayılır. Farklı para birimine sahip bir satıcı için satınalma siparişi oluşturduğunuzda sistem, genel muhasebe defterinizde **Muhasebe para birimi döviz kuru türü** alanında belirttiğiniz döviz kurunu kullanarak, para birimini muhasebe para birimi tutarından hareket para birimine otomatik olarak dönüştürür.

Bir ticari sözleşme günlüğü oluşturduğunuzda, her satırda fiyatı ifade ettiğiniz para birimini belirtebilirsiniz. Çoklu para birimleri, belirli satıcılar ve diğer etmenlerin birçok kombinasyonu için ticari sözleşmeler oluşturabilirsiniz. Seçtiğiniz para birimi için bir ticari sözleşme bulunan bir satınalma siparişi oluşturursanız sistem, eşleşen para birimine sahip ticari sözleşmeyi kullanır. Ürün girişleri veya fatura gibi hareketleri deftere naklettiğinizde tutar, genel muhasebe defterinde belirttiğiniz muhasebe para birimi döviz kurunu kullanarak genel muhasebe defterinin muhasebe para birimine dönüştürülür.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Birden çok para birimi cinsinden tedarik edilen maddeler için maliyetleri nasıl yapılandırmalıyım?

Maliyetler birden fazla para biriminde yapılandırılamaz. **Serbest bırakılan ürün** sayfasının **Maliyeti yönet** hızlı sekmesindeki **Fiyat** alanına girdiğiniz varsayılan maliyetler veya madde fiyatı için belirtilen maliyet, her zaman seçtiğiniz tüzel kişiliğin genel muhasebe para birimi cinsinden ifade edilir.

Kuruluşunuzda standart maliyetlendirme kullanılıyorsa, birden çok para birimi olduğunda maliyetlerin tanımlanması için bir strateji tanımlamanız gerekir. Ayrıca, deftere nakledilen farkların sayısını azaltmaya yardımcı olmak için maliyeti düzenli olarak güncelleştiren bir işlem tanımlamanız gerekir.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Satış fiyatlarını hesaplamak için Maliyet grubu sayfasındaki Kar ayarını kullanabilir miyim?

Evet, satış fiyatları maliyet hesaplaması kullanılarak hesaplandığında bir yüzde eklemek için **Maliyet grubu** sayfasındaki **Kar** ayarını kullanabilirsiniz. Daha fazla bilgi için bkz. [BOM hesaplamaları](bom-calculations.md).

## <a name="marking"></a>İşaretleme

### <a name="how-does-marking-affect-periodic-costing-models"></a>İşaretleme dönemsel maliyetlendirme modellerini nasıl etkiler?

FIFO, LIFO veya ağırlıklı ortalama gibi dönemsel bir maliyetlendirme modeli kullanıyorsanız ve bir çıkış hareketine karşılık olarak bir giriş hareketi işaretlediyseniz, stok kapanışı işlemi sırasında maddenin buluşsal modeli yoksayılır. Bunun yerine sistem, çıkışın maliyeti için girişin fiili maliyetini kullanır.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>İşaretleme kullandığımda, stok kapanışı sırasında ne olur?

Giriş ve çıkışları işaretlediğinizde, stok kapanışı birlikte işaretlenen hareketleri kapatır. Kapatma oluşturmak için işaretleme kullanıldığında, **Kapatma** sayfasındaki **İlke** alanı *İşaretleme* olarak ayarlanır. Bir hareket fiziksel veya mali olarak güncelleştirilmeden önce işaretlenmişse çıkış işleminde, cari ortalama maliyet yerine işaretli girişin maliyeti kullanılır. Hareketler mali güncellemeden sonra işaretlenmişse stok kapatma ve düzeltme işlemi, çıkış maliyetini giriş maliyetiyle eşleşecek şekilde düzeltir.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Standart maliyetlendirme veya hareketli ortalama kullandığımda, hareketleri el ile işaretleyebilir miyim?

Hayır, standart maliyetlendirme veya hareketli ortalama kullandığınızda, girişleri veya çıkışları el ile işaretleyemezsiniz. Hareketler (ör. doğrudan teslim veya şirketlerarası siparişler) otomatik olarak işaretleniyorsa işaretleme kaydı kalır ve kesin rezervasyon işlevi görür. Ancak, standart maliyetlendirme veya hareketli ortalama kullandığınızda kayıtların işaretlenmesi, maddelerin maliyeti üzerinde herhangi bir etkiye sahip değildir.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>İşaretleme kar ve zarar raporunu nasıl etkiler?

Bir stok girişine karşılık olarak çıkış hareketini işaretlediğinizde çıkışın maliyeti, seçili girişle eşleştirilir. Çıkışı fiziksel olarak ve mali olarak deftere naklettiğinizde deftere nakil işlemi, stok deftere nakil profilinde belirttiğiniz **Satılan malların maliyeti, teslim edilen** ve **Satılan malların maliyeti, faturalanan** hesaplarını etkiler. Bir hareket fiziksel veya mali güncelleştirmeden sonra işaretlenirse *Stok kapatma ve düzelme* işlemi, **Satılan malların maliyeti, faturalanan** hesabını düzelten ve **Birimlerin maliyeti, faturalanan** (stok) için belirttiğiniz hesaba mahsup eden eşleşen bir fişe sahip bir düzeltme oluşturur.

### <a name="how-does-marking-affect-master-planning"></a>İşaretleme master planlamayı nasıl etkiler?

**Master planlama parametreleri** sayfasındaki **Standart güncelleştirme** sekmesi, **İşaretlemeyi güncelleştir** adlı bir alan içerir. Burada belirlediğiniz seçenek, master planlama tarafından oluşturulan bir planlı siparişi kesinleştirdiğinizde kullanılır. Aşağıdaki seçenekler bulunur:

- *Hayır*: Sistem hiçbir işaretleme gerçekleştirmez.
- *Standart*: Sistem, ilişkilendirmeye göre çıkışlara karşılık olarak girişleri işaretler. Bir karşılama siparişine karşılık olarak bir gereksinim siparişi işaretlenir. Sipariş karşılamada belirli bir miktar kalırsa karşılama siparişi işaretlenmez.
- *Genişletilmiş*: Sistem, karşılama siparişinde herhangi bir miktarın açıkta kalmasına bakılmaksızın hem gereksinim siparişlerini hem de karşılama siparişlerini işaretler.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Negatif stok

### <a name="when-should-i-allow-physical-negative-inventory"></a>Fiziksel negatif stoğa hangi durumlarda izin vermem gerekir?

Genel olarak, ambarınızda somut bir maddeden 0 (sıfır) değerinden daha az miktarda bulunması mümkün olmadığından fiziksel negatif stoğa izin vermeniz önerilmez. Ancak, bazı sektörlerin ve kurumsal senaryoların iş süreçleri, stoğun fiziksel olarak negatif olmasına izin verilmesini gerektiren operasyonları kısıtlayabilir. Örneğin perakenciler, sistemin maddenin mevcut olmadığını gösterdiği bir durumda kasaya getirilen maddenin satışını önlemek istemeyebilir. Proses üretimi sektörü de buna başka bir örnektir. Bu üreticiler için tüketilen miktar formülde önerilen miktarı aşabilir. Alternatif olarak, tüketimde kesin bir miktar yerine tahmini bir miktar kullanılabilir. Bu nedenle tüketim, hazne gibi belirli bir yerleşimde miktarı aşar.

Mümkünse iş sürecinizi değerlendirmeli ve stoğun negatif olamayacağı şekilde geliştirmeye çalışmalısınız. Negatif stoğa izin vermeniz gerekiyorsa, negatif stoğu düzeltmek için net bir iş sürecinizin olması gerekir. Aksi takdirde bu durum, maliyetlendirmeyi olumsuz etkileyebilir.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Mali negatif stoğa hangi durumlarda izin vermem gerekir?

Genel olarak, birçok kuruluşun mali negatif stoğa izin vermesi önerilir. (Çoğu durumda, satınalma siparişi faturaları maddeleri sevk etmeden önce işlenmez.) Satış fiyatının bir satınalma siparişinin nihai maliyetini yansıtmasını gerektiren belirli iş süreçleriniz olduğunda bu seçeneği etkinleştirmelisiniz. Örneğin, bu gereksinim siparişe göre üretim yapılan sektörlerde veya bunun yasal olarak zorunlu olduğu belirli bölgelerde geçerli olabilir.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Stok negatif olduğunda çıkışlarımın maliyetine ne olur?

Maddenizin stoğu negatif olduğunda ve fiziksel olarak sahip olduğunuz miktardan fazla madde çıkışı yaptığınızda FIFO, LIFO veya ağırlıklı ortalama gibi dönemsel bir maliyetlendirme modeli kullanıyorsanız sistem, cari ortalamayı hesaplamak için varsayılan madde fiyatını kullanır. Madde için varsayılan fiyat belirtilmemişse sistem, stoğu 0 (sıfır) değeriyle çıkarır. Bu davranış, cari ortalamanıza veya hareketli ortalamanıza ilişkin gelecekteki hesaplamaların hatalı olmasına neden olabilir.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Eldeki stok yeterli değilse satış siparişlerinde veya üretim emirlerinde maddelerin çekilmesini, paketlenmesini veya satılmasını engelleyebilir miyim?

Evet. Maddelerin satış siparişlerinde ve üretim emirlerinde çekilmesini, paketlenmesini veya satılmasını önlemek üzere madde modeli grubu için **Fiziksel negatif** seçeneğini devre dışı bırakmanız önerilir.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Madde için herhangi bir satınalma siparişi faturalanmamışsa, aynı maddenin satış siparişinde faturalanmasını engelleyebilir miyim?

Evet. Madde için herhangi bir satınalma siparişi faturalanmamışsa aynı maddenin satış siparişinde faturalanmasını engellemek üzere madde modeli grubu için **Mali negatif** seçeneğini devre dışı bırakmanızı öneririz.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Negatif stok, brüt kar marjı gibi mali oranları nasıl etkiler?

Stoğunuzun negatif duruma geçmesine izin verdiğinizde, maddeleriniz için varsayılan fiyatın yapılandırılmadığı durumlar başta olmak üzere bilançonuzdaki stok değeri ile kar ve zarar raporunuzdaki satılan malların maliyeti gerçek değerinden daha az belirtilebilir. Bu nedenle, maliyet yanlış olduğundan brüt kar marjları gibi mali raporlama ve oranlar gerçek değerinden daha yüksek belirtilebilir. FIFO, LIFO veya ağırlıklı ortalama gibi dönemsel bir maliyetlendirme modeli kullanıyorsanız, negatif stok miktarları düzeltildikten sonra stok kapanışı ve düzeltme işlemini çalıştırdığınızda çıkışların değeri düzeltilebilir. Ancak, hareketli ortalama kullanıyorsanız, hareketlerin ayrı ayrı yeniden değerlenmesi mümkün değildir.

### <a name="how-should-i-correct-negative-inventory"></a>Negatif stoğu nasıl düzeltebilirim?

Kuruluşunuz veya iş gereksinimleriniz stoğunuzun negatif olmasına izin vermenizi gerektirdiğinde, negatif stokları sıklıkla izlemeniz ve düzeltmeniz önerilir. Dönemsel sayım gerçekleştirerek, düzeltmeyi deftere naklederek veya hareket günlüğünü deftere naklederek stok değerlerini düzeltebilirsiniz. Belirli bir genel muhasebe hesabında stoktaki beklenmeyen kazançları kabul etmeniz gerekiyorsa bir hareket günlüğü kullanmayı planlamanız gerekir. Aksi takdirde, dönemsel sayım veya stok düzeltme işlemini kullandığınızda sistem, stok düzeltmesini **Stok girişi** hesabına nakleder ve stok deftere nakil profilinde belirttiğiniz **Stok harcaması, kar** hesaplarına mahsup eder.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Stoğum negatif olduysa ve hareketli ortalama kullanıyorsam yeni bir madde oluşturmak zorunda mıyım?

Hayır. Kuruluşunuz stoğun fiziksel olarak negatif olmasına izin veriyor ve stok modeliniz olarak hareketli ortalama kullanıyorsanız sistem, maliyetin çıkışlarınıza nasıl atanacağını belirlemek için **Stok ve ambar yönetim parametreleri** sayfasında atanan geri dönüş maliyet sırasını kullanır. Genel olarak, stoğunuzun fiziksel olarak negatif duruma geçmesini engellemeniz önerilir. Daha fazla bilgi için bu konunun [Negatif stok](#negative-inventory) bölümündeki diğer sorulara bakın.

## <a name="not-stocked-products"></a>Stoğu tutulmayan ürünler

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Stoğu tutulmayan ürünler için satış siparişi malzeme çekme listelerini deftere nakledebilir miyim?

Stoğu tutulmayan bir madde modeli grubundaki maddeleri içeren bir satış siparişi için malzeme çekme listesi oluşturduğunuzda, stoğu tutulmayan maddeler için hiçbir satır görmezsiniz. Stoğu tutulmayan maddeleri işlemek için Warehouse Management mobil uygulamasını kullanamazsınız.

Stoğu tutulmayan bir madde modeli grubundaki maddeleri içeren bir satış siparişi için sevk irsaliyesi oluşturduğunuzda, belge oluşturmaya stoğu tutulmayan maddeleri dahil etmek için **Miktar** alanını *Çekilen miktar ve stoğu tutulmayan ürünler* olarak ayarlayın. *Tümü* seçeneğini belirlerseniz, sevk irsaliyesine yalnızca stoğu tutulan maddeler dahil edilir.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Stoğu tutulmayan ürün veya kategori (satış kategorisi veya tedarik kategorisi) kullanmalı mıyım?

Stoğu tutulmayan ürün ile kategori arasındaki seçim işinize özgü gereksinimlere bağlıdır. Stoğu tutulmayan ürünler genellikle, satınalma siparişleri ve satış siparişlerindeki miktarlar ve fiyatlar gibi varsayılan değerler üzerinde daha fazla kontrol sağlar. Bu nedenle, aynı ürün veya servisin birden çok kez satın alındığı veya satıldığı senaryolarda, stoğu tutulmayan ürünler tercih edilir. Kategoriler, fiyat, maddeler, açıklamalar vb.nin işlemler arasında tutarsız olduğu senaryolarda kullanışlıdır. Kategoriler, satılan veya satın alınan ürün türünü sınıflandırmak için herhangi bir üründe de kullanılabilir.

## <a name="service-items"></a>Servis maddeleri

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Servis maddesi ile stoğu tutulmayan ürün arasındaki fark nedir?

Servis maddesi bir ürün türüdür. Yeni serbest bırakılan bir ürün oluşturduğunuzda, **Ürün türü** alanını *Madde* veya *Servis* olarak ayarlayabilirsiniz. *Madde*, genel olarak maddenin maddi olduğunu belirtmek için seçilirken *Servis* maddenin maddi olmadığını belirtmek için seçilir.

Bir madde veya servis ürünü olup olmadığına bakılmaksızın servis bırakılan tüm ürünlerin stoğu tutulabilir veya tutulmayabilir. Stoğu tutulan veya stoğu tutulmayan ayarı, sunulan ürün için seçtiğiniz madde modeli grubu tarafından denetlenir. Stoğu tutulmayan bir madde grubu seçtiğinizde sistem, örneğin ilgili satış siparişi veya satınalma siparişi için stok hareketleri oluşturmaz.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Ürün reçetesine stoğu tutulmayan ürünler ekleyebilir miyim?

Hayır, **Stoğu tutulan** seçeneğinin devre dışı bırakıldığı bir madde model grubuna bağlı serbest bırakılan ürünü ürün reçetesine veya formüle ekleyemezsiniz. **Ürün türü** alanının *Madde* veya *Servis* olarak ayarlanıp ayarlanmaması fark etmez. Yalnızca stoğu tutulan maddeler ürün reçetesi veya formül satırlarına eklenebilir.

## <a name="costing-modelspecific-questions"></a>Maliyetlendirme modeline özel sorular

### <a name="which-costing-model-should-i-use"></a>Hangi maliyetlendirme modelini kullanmalıyım?

Seçmeniz gereken maliyetlendirme modelleri, iş gereksinimlerinize bağlıdır. Supply Chain Management'ta kullanılacak bir maliyetlendirme modeli seçmeden önce, yerel düzenlemelerinizde modele izin verildiğini doğrulamanız gerekir. Seçiminizi bölgenizdeki lisanslı bir muhasebeci ile doğrulamanız önerilir.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Kuruluşumda birden fazla maliyetlendirme modeli kullanabilir miyim?

Evet. Supply Chain Management'ta seçebileceğiniz madde modeli grubu veya maliyetlendirme modeli sayısı için bir sınır yoktur.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Her madde için maliyetlendirme modeli kullanabilir miyim?

Hayır. Serbest bırakılan her ürün için yalnızca bir maliyetlendirme modeli seçebilirsiniz. Bu davranış madde modeli grubu tarafından kontrol edilir. Stok değerlerini raporlamak için birden fazla maliyetlendirme modeli kullanmanız gerekiyorsa, Genel Stok Muhasebesi eklentisini kullanabilirsiniz.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Üretim yürütme işlemini kullanırken hangi maliyetlendirme metodolojisini kullanmalıyım?

Seçmeniz gereken maliyetlendirme modelleri, iş gereksinimlerinize bağlıdır. Kuruluşunuz üretim yürütme işlemini kullanırken herhangi bir maliyetlendirme modelini kullanmanın belirli bir avantajı veya dezavantajı yoktur.

### <a name="when-is-fefo-used"></a>FEFO ne zaman kullanılır?

İlk süresi dolan, ilk çıkar (FEFO) maliyetlendirme metodolojisi değildir. Bunun yerine, genellikle üretim kuruluşlarında kullanılan bir rezervasyon tekniğidir. **FEFO tarih denetimli** seçeneğini etkinleştirip **Çekme ölçütü** alanında bir değer seçerek madde modeli grubu için FEFO rezervasyonlarını etkinleştirebilirsiniz.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Belirli maliyetlendirme modellerinin performans avantajları var mı?

Genel olarak, bir madde için seçtiğiniz maliyetlendirme modelinin sistemin genel performansı üzerinde minimum düzeyde etkisi vardır. Ancak, seçtiğiniz stok maliyetlendirme modeli stok kapanışı veya yeniden hesaplama işlemini çalıştırmak için gereken süreyi etkileyebilir. Örneğin, standart maliyet veya hareketli ortalama kullandığınızda, bu model her bir stok işlemini güncelleştirip kapatma oluşturmadığından stok kapanışı sürecinin sistem üzerinden minimum düzeyde etkisi olur. Ancak, FIFO, LIFO veya ağırlıklı ortalama gibi dönemsel bir maliyetlendirme modeli, stok kapanışı sürecini tamamlamak için gereken süreyi artırabilir. Özellikle, *Stoğu kapat* işlemi için **Madde başına izin verilen maksimum tekrar sayısı** alanına yüksek bir değer girdiğinizde veya **İzin verilen minimum tutar** alanına düşük bir değer girdiğinizde kapanış işlemi daha da uzun sürebilir.

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Sabit giriş fiyatı seçeneğini ne zaman kullanmalıyım?

Bir madde için **Madde model grubu** sayfasındaki **Sabit giriş fiyatı** onay kutusunu işaretlediğinizde, sistem stok girişi için standart maliyet olarak giriş fiyatını kullanır. Bir ürün için yapılandırılan satınalma fiyatı ve varsayılan madde maliyeti fiyatı arasında fark varsa, bu fark **Sabit giriş fiyatı karı** veya **Sabit giriş fiyatı zararı** hesabına nakledilir ve **Sabit giriş fiyatı mahsup işlemi** hesabına mahsup edilir. (Tüm bu hesaplar **Deftere Nakil** sayfasında belirtilir.)

FIFO, LIFO veya ağırlıklı ortalama gibi dönemsel bir maliyetlendirme modeli kullandığınızda **Sabit giriş fiyatı** onay kutusunu seçmeniz ve giriş fiyatının varsayılan madde maliyetinden farklı olması durumunda satınalma fiyatı farkının genel muhasebe defterinde izlemeniz gerekir.

### <a name="moving-average"></a>Hareketli ortalama

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Hareketli ortalama ile kayan ortalama ile aynı mıdır?

Hareketli ortalama, kayan ortalama ve cari ortalama terimleri genellikle eş anlamlı olarak kullanılır. Bu terimler arasında Supply Chain Management'ta resmi maliyetlendirme modeli olan yalnızca hareketli ortalamadır. Cari ortalama resmi bir maliyetlendirme modeli olmasa da FIFO, LIFO veya ağırlıklı ortalama gibi dönemsel bir maliyetlendirme modeli kullandığınızda kullanılan tekniktir. Kayan ortalama terimi Supply Chain Management'ta kullanılmaz ve diğer sistemlerde farklı anlamlar ifade edebilir.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Hareketli ortalama kullandığımda, ürün giriş fiyatı ve fatura fiyatı arasındaki farkı nasıl dengeleyebilirim?

Hareketli ortalama kullandığınızda, fiziksel maliyet (giriş fiyatı) tüm çıkış hareketlerinin hareketli ortalamasını hesaplamak için kullanılır. Fiziksel maliyet (giriş fiyatı) ile mali maliyet (fatura fiyatı) arasında fark varsa sistem, **Stok deftere nakil profili** sayfasının **Stok** sekmesindeki **Hareketli ortalama için fiyat farkı** deftere nakil türünde belirtilen ana hesaba farkı otomatik olarak nakleder.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Hareketli ortalama için fiyat farkı genel muhasebe defterinin hangi bölümünde gösterilir?

Bir giriş için fiziksel güncelleştirme ile mali güncelleştirmenin deftere nakli arasında fiyat farkı olduğunda fark, **Stok deftere nakil profili** sayfasının **Stok** sekmesindeki **Hareketli ortalama için fiyat farkı** deftere nakil türünde belirtilen ana hesaba otomatik olarak nakledilir. Daha fazla bilgi için bkz. [Hareketli ortalama](moving-average.md).

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Hareketli ortalama kullandığımda, girişten önce bir çıkış varsa ne olur?

Genellikle, madde modeli grubu için fiziksel negatif stoğa izin vermeniz veya çıkışın geriye dönük tarihli olması nedeniyle girişten önce çıkış olabilir. Daha fazla bilgi için bu konudaki [Negatif stok](#negative-inventory) bölümüne bakın.

Hareketleri geriye dönük tarihlendiriyorsanız, bu senaryoyu önlemenin bir yolu olup olmadığını belirlemek için iş sürecinizi ve işlemlerinizi dikkatle değerlendirmeniz önerilir. Hareketli ortalamayı kullanan bir maddenin hareketini geriye dönük tarihlendiriyorsanız, sistem mevcut hareketli ortalamayı harekete atayacaktır. Sonraki çıkışlar düzeltilmez. Geriye dönük tarihli hareketleri olan hareketli ortalama hakkında daha fazla bilgi edinmek için bkz. [Hareketli ortalama](moving-average.md).

### <a name="standard-costing"></a>Standart maliyetlendirme

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Standart maliyetlendirme ve sabit giriş fiyatı arasındaki fark nedir?

Standart maliyetlendirme, bir madde fiyatı tanımlamanızı ve maliyeti bir maliyetlendirme sürümünde etkinleştirmenizi gerektirir. Bu maliyet tüm giriş ve çıkışlarda kullanılır. Stok girişleri için farklar, **Stok deftere nakil profili** sayfasının **Standart maliyet** sekmesinde belirttiğiniz standart maliyet farkı hesapları kullanılarak genel muhasebe defterine kaydedilir.

Ancak, sabit giriş fiyatı kullandığınızda, yalnızca giriş maliyeti sabittir ve sistem, **Serbest bırakılan ürün** sayfasının **Maliyetleri yönet** hızlı sekmesinde belirttiğiniz maliyeti kullanır. Varsayılan maliyet ile satınalma siparişi fiyatı arasındaki farklar, satınalma fiyatı farkının sabit giriş fiyatı kar ve zarar hesaplarına nakledilmesine neden olur. Çıkışlarda sabit giriş fiyatı kullanılmaz. Bunun yerine, çıkışlar deftere nakil sırasındaki cari ortalamaya göre değerlendirilir (işaretleme kullanmadığınız takdirde) ve stok kapanışını çalıştırdığınızda seçtiğiniz buluşsal modele göre yeniden değerlenir.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Standart maliyetlendirme ile FEFO rezervasyonlarını kullanabilir miyim?

Evet, standart maliyetlendirme seçeneğini belirlediğinizde bir madde modeli grubunda FEFO rezervasyonlarını kullanabilirsiniz. FEFO rezervasyonları maddelerin fiziksel olarak işlenmesinde kullanılan rezervasyon mantığını kontrol ederken, standart maliyetlendirme bir maddenin fiziksel ve mali maliyetini denetler.

### <a name="can-i-upload-pending-prices"></a>Bekleyen fiyatları karşıya yükleyebilir miyim?

Evet, bekleyen bir fiyatı karşıya yüklemek için Excel eklentisini veya Veri Yönetimi Çerçevesi'ni kullanabilirsiniz. Aşağıdaki varlıkları kullanmanızı öneririz:

- Bekleyen madde fiyatları (V2)
- Bekleyen rota maliyeti kategorisi birim maliyetleri
- Maliyetlendirme tablosu düğüm hesaplama etkenleri (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Bir maddenin standart maliyetini hangi sıklıkta güncelleştirebilirim?

Yeni standart maliyeti etkinleştirme sıklığıyla ilgili bir sınır yoktur. Son maliyetin etkinleştirildiği tarihteki bir madde için yeni bir maliyeti etkinleştirirseniz sistem, yeni hareketler veya güncelleştirmeler (mevcut hareketlerdeki güncelleştirmeler gibi) için en son etkinleştirilen maliyeti kullanır.

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Etkinleştirilmiş bir maliyeti devre dışı bırakabilir veya silebilir miyim?

Hayır, etkinleştirilmiş bir maliyeti devre dışı bırakamaz veya silemezsiniz. Maliyeti yanlış şekilde etkinleştirdiyseniz doğru maliyete sahip yeni bir maliyeti etkinleştirebilirsiniz.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Hesaplama grupları standart maliyetle kullanılır mı?

Seçtiğiniz madde modeli grubu ne olursa olsun, hesaplama grupları her maddeyle kullanılabilir. Hesaplama grupları, hesaplama çalıştırdığınız maddeler için kullanılması gereken ayarları belirlemek amacıyla maliyet toplama veya maliyet hesaplama işlemi sırasında kullanılır. Hesaplama grupları hakkında daha fazla bilgi için bkz. [BOM hesaplama grupları](bom-calculation-groups.md).

### <a name="when-should-i-use-a-planned-costing-version"></a>Planlanan maliyet sürümünü ne zaman kullanmalıyım?

Maliyet versiyonlarının *Standart maliyet* veya *Planlanan maliyet* olmak üzere iki türü bulunur. *Standart maliyet* türü, sistemde etkin olan maliyetler için kullanılır ve hareketlere nakledilir. *Planlanan maliyet* türü, maliyetler üzerinde simülasyon çalıştırmak için kullanılır ve hareketlerin maliyetini etkilemez.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Bir tüzel kişiden alınan toplam maliyet başka bir tüzel kişiye satış maliyeti olarak aktarılabilir mi?

Maliyetleri bir şirketten diğerine kopyalamanın otomatik bir yolu yoktur. Ayrıca, maliyetleri bir satınalma fiyatından satış fiyatına kopyalamanın da otomatik bir yolu yoktur. Kuruluşunuzun bu görevlerden birini tamamlaması gerekiyorsa verileri maliyetlendirme sürümünüzden dışarı aktarmak ve maliyetlendirme sürümünde satış fiyatı olarak ya da ticari sözleşme olarak başka bir şirkete yüklemek için Veri Yönetimi Çerçevesi'ni kullanmak isteyip istemediğinizi değerlendirebilirsiniz. Dosyaların el ile düzenlemesi gerekli olabilir.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Planlanan maliyetleri standart maliyetlendirme sürümüne kopyalamanın en iyi yöntemi hangisidir?

Madde fiyatları, maliyet kategorisi fiyatları veya dolaylı maliyetleri bir maliyetlendirme sürümünden diğerine kopyalamak için, **Maliyetlendirme sürümleri** sayfasındaki **Kopyala** düğmesini kullanabilirsiniz.
