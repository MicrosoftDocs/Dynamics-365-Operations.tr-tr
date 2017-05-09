---
title: "Elektronik raporlamaya genel bakış"
description: "Bu makale, Elektronik raporlama (ER) aracına genel bakış sağlar. Temel kavramlar, ER&quot;nin desteklediği senaryolar ve çözümün bir parçası olarak tasarlanan ve yayınlanan biçimlerin listesini içermektedir."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: b3e8174d07c9b9fd4210486c369c640fe07c49eb
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-overview"></a>Elektronik raporlamaya genel bakış

[!include[banner](../includes/banner.md)]


Bu makale, Elektronik raporlama (ER) aracına genel bakış sağlar. Temel kavramlar, ER'nin desteklediği senaryolar ve çözümün bir parçası olarak tasarlanan ve yayınlanan biçimlerin listesini içermektedir.

Elektronik raporlama (ER) çeşitli ülkelerin/bölgelerin yasal gereksinimlerine uygun olarak elektronik belgeler için biçimleri yapılandırmak amacıyla kullanabileceğiniz bir araçtır. ER, yaşam döngüleri boyunca bu biçimleri yönetmenizi sağlar. Örneğin, yeni mevzuat gerekliliklerini uygulayabilir ve devlet kurumları, bankalar ve diğer taraflarla elektronik olarak belge alışverişi yapmak için gerekli biçimde işletme belgeleri oluşturabilirsiniz. ER altyapısı geliştiricilerden ziyade iş kullanıcılarını hedefler. Çünkü kodu değil biçimleri yapılandırırsınız, elektronik belgeler için biçimler oluşturma ve ayarlama süreçleri daha hızlı ve kolaydır. ER şimdilik TEXT, XML ve OPENXML çalışma sayfası biçimlerini desteklemektedir. Ancak bir uzantı arabirimi daha fazla biçimi destekler.

## <a name="capabilities"></a>Beceriler
ER altyapısı aşağıdaki yeteneklere sahiptir:

-   Farklı etki alanlarında elektronik raporlama için tek bir ortak aracı temsil eder ve Microsoft Dynamics 365 for Operations için bir tür elektronik raporlama yapan 20'den fazla farklı altyapının yerini alır.
-   Rapor biçiminin şu anki Dynamics 365 for Operations uygulamasından yalıtılmasını sağlar. (Diğer bir deyişle, biçim Microsoft Dynamics 365 for Operations farklı sürümleri için geçerlidir.)
-   Özgün biçime dayalı özel bir biçim oluşturulmasını destekler. Yerelleştirme/özelleştirme gereklilikleri uygulandığından özgün biçimde değişiklikler olduğunda özelleştirilmiş biçimi otomatik olarak yükseltme yeteneğini içerir.
-   Microsoft ve Microsoft ortakları için elektronik raporlamada yerelleştirme gerekliliklerini desteklemek amacıyla birincil standart araç haline dönüşür.
-   Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla biçimleri iş ortakları ve müşterilere dağıtma yeteneğini destekler.

## <a name="concepts"></a>Kavramlar
### <a name="components"></a>Bileşenler

ER iki tür bileşeni destekler: **Veri modeli **ve **Biçim**.

#### <a name="data-model-components"></a>Veri modeli bileşenleri

Veri modeli bileşeni bir veri yapısının soyut temsilidir ve belirli iş etki alanını bu etki alanındaki raporlama gereksinimlerini karşılamak için yeterli ayrıntılarla açıklamak amacıyla kullanılır. Veri modeli bileşeni aşağıdaki bölümlerden oluşur:

-   Etki alanına özgü iş varlıkları kümesi olarak veri modeli ve bu varlıkların aralarındaki ilişkilerin hiyerarşik olarak tanımı
-   Seçilen Dynamics 365 for Operations veri kaynaklarını, veri bileşenine ilişkin veri akışı ve işletme veri popülasyonu kurallarını çalışma zamanında belirten bir veri modelinin tek tek öğelerine bağlayan model eşleme.

Bir iş varlık veri modeli (kayıt) kapsayıcı olarak temsil edilir. İş varlık özellikleri veri öğelerini (alanları) olarak temsil edilir. Her veri öğesinin benzersiz bir ad, etiket, açıklama ve değeri vardır. Her bir veri öğesinin değeri, dize, tamsayı, tarih, çetele türü, Boole vb. olarak tanınacak şekilde tasarlanabilir. Ayrıca başka bir kayıt veya kayıt listesi olabilir. Tek bir veri modeli bileşeni, etki alanına özgü iş varlıklarının bir çok hiyerarşisini ve çalışma zamanında belirli bir özel veri akışı raporunu destekleyen model eşlemelerini içerebilir. Hiyerarşiler eşleme modeli kökü olarak seçilen tek bir kayıt tarafından ayrıştırılır. Örneğin, ödeme etki alanının veri modeli aşağıdaki eşlemeleri destekliyor olabilir:

-   Şirket -&gt; Satıcı-&gt; AP etki alanının ödeme hareketleri
-   Müşteri -&gt; Şirket -&gt; AR etki alanının ödeme hareketleri

İş varlıklarının (Şirket ve Ödeme hareketleri gibi) bir kez tasarlandığını unutmayın. Daha sonra farklı eşleşmeler bunları yeniden kullanır. Model eşleme aşağıdaki özellikleri içerir:

-   Veri modeli için veri kaynakları olarak farklı Dynamics 365 for Operations veri türlerini kullanabilir. Örneğin tabloları, veri varlıklarını, yöntemleri veya çeteleleri kullanabilir.
-   Bazı verilerin çalışma zamanında belirtilmesi gerekiyorsa bir veri modeli için veri kaynağı olarak tanımlanabilen kullanıcı giriş parametrelerini destekler.
-   Dynamics 365 for Operations verilerinin gerekli gruplara dönüşümünü, veri filtreleme,sıralama ve toplamayı ve Microsoft Excel benzeri formüller aracılığıyla tasarlanan mantıksal hesaplanmış alanlara eklenmeyi destekler (daha fazla bilgi için bkz. [Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)).

[![Excel benzeri formül düzenleyici](./media/pic-formula-1024x615.png)](./media/pic-formula.png) Bir veri modeli bileşeni, raporlamayı Dynamics 365 for Operations veri kaynaklarının fiziksel uygulamalarından yalıtan raporlama amacıyla birleştirilmiş veri kaynağı olarak kullanılması gereken her bir iş etki alanı için tasarlanır ve raporlama biçiminin ilk tasarımını ve sonraki bakımını daha etkili kılan bir formda etki alanına özel iş kavramları ve işlevlerini temsil eder.

#### <a name="format-components"></a>Biçim bileşenleri

Biçim bileşeni çalışma zamanında oluşturulacak raporlama çıktısının planıdır. Plan aşağıdaki öğelerden oluşur:

-   Çalışma zamanında oluşturulan elektronik raporlama belgesinin yapısı ve içeriğini tanımlayan biçim
-   Bir dizi kullanıcı giriş parametresi ve seçilen model eşlemesini kullanan etki alanına özgü veri modeli olarak veri kaynakları
-   Çalışma zamanında veri akışı ve biçim çıktı oluşturma kurallarını belirten bir biçimin tek tek öğelerini barındıran biçim veri kaynaklarının bağlama kümesi olarak biçim eşleme
-   Çalışan bağlama bağlı olarak çalışma zamanında rapor oluşturulmasını kontrol eden yapılandırılabilir kurallar kümesi olarak biçim doğrulaması (örneğin, satıcının ödemelerine dair çıktı oluşumunu durduran ve banka hesap numarası gibi seçilen satıcının belirli öznitelikleri eksik olduğunda bir istisna oluşturan kural).

Biçim bileşeni aşağıdaki işlevleri destekler:

-   Raporlama çıktısının çeşitli biçimlerde tek tek dosyalar şeklinde oluşturulması: metin, XML veya çalışma sayfası
-   Birden fazla dosyanın ayrı ayrı oluşturulması ve bu dosyaların zip dosyalarına kapsüllenmesi

Biçim bileşeni, raporlama çıktısında kullanılabilen belirli dosyaları ekleme yeteneğini sağlar:

-   OPENXML çalışma biçiminde çıktı için şablon olarak kullanılabilen bir çalışma sayfasını içeren Excel çalışma kitapları
-   Önceden tanımlanmış dosyalar olarak biçim çıktısına dahil edilebilen diğer dosyalar

#### <a name="component-versioning"></a>Bileşen sürüm oluşturma

Sürüm Oluşturma ER bileşenleri için desteklenir. Aşağıdaki iş akışı ER bileşenlerindeki değişiklikleri yönetmek için sağlanır:

-   Başlangıçta oluşturulan sürüm **TASLAK** sürüm olarak işaretlenir. Bu sürüm düzenlenebilir ve test çalıştırmaları için kullanılabilir.
-   ** TASLAK** sürümü **TAMAMLANDI** sürümüne dönüştürülebilir. Bu sürüm yerel raporlama işlemlerinde kullanılabilir.
-   **TAMAMLANDI** sürümü **PAYLAŞIMLI** sürümüne dönüştürülebilir. Sürüm LCS üzerinde yayımlanır ve küresel raporlama işlemlerinde kullanılabilir.
-   **PAYLAŞILAN **sürümü **TAMAMLANDI** sürümüne dönüştürülebilir. Daha sonra bu sürüm silinebilir.

** TAMAMLANDI** veya **PAYLAŞILAN** durumuna sahip sürümler diğer veri değişimleri için kullanılabilir. Bu durumlara sahip bir bileşen bunlar üzerinden gerçekleştirilen eylemlere sahip olabilir.

-   Bunlar XML biçiminde sıralanabilir ve XML biçiminde bir dosya olarak Dynamics 365 for Operations'tan dışa aktarılabilir.
-   Bunlar bir XML dosyasından tekrar sıralanabilirler ve ER bileşeninin yeni bir sürümü olarak Dynamics 365 for Operations'ten içe aktarılabilirler.

#### <a name="component-date-effectivity"></a>Bileşen tarihi geçerlilik

ER bileşen sürümleri tarih etkilidir. **Yürürlük başlangıcı **tarihi, raporlama işlemleri için bileşenin geçerlilik kazandığı tarihi belirtmek amacıyla bir ER bileşeni için tanımlanabilir. Dynamics 365 for Operations oturum tarihi bir bileşen yürütme için geçerli olup olmadığını tanımlamak için kullanılır. Belirli bir tarih için birden fazla sürüm geçerliyse raporlama işlemleri için en son sürüm kullanılır.

#### <a name="component-access"></a>Bileşen erişim

ER biçimli bileşenlere erişilmesi ISO ülke/bölge kodu ayarlarına bağlıdır. Bu ayar bir biçim konfigürasyonunun seçilen sürümü için boş ise çalışma zamanında herhangi bir Dynamics 365 for Operations şirketinden biçim bileşenine erişilebilir. Bu ayar ISO ülke/bölge kodları içeriyorsa biçim bileşenine yalnızca biçim bileşeninin ISO ülke/bölge kodlarının biri için tanımlanan birincil adrese sahip Dynamics 365 for Operations şirketlerinden ulaşılabilir. Bir veri biçimi bileşeninin farklı sürümleri ISO ülke/bölge kodları için farklı ayarlara sahip olabilir.

#### <a name="configuration"></a>Yapılandırma

ER konfigürasyonu **Veri modeli **veya **Biçim** şeklinde belirli bir ER bileşeninin sarmalayıcısıdır. Bir konfigürasyon belirli bir ER bileşeninin farklı sürümlerini içerebilir. Her yapılandırma belirli yapılandırma sağlayıcı tarafından sahip olunan olarak işaretlenir. Bir konfigürasyon bileşeninin **TASLAK** sürümü, konfigürasyon sahibi Dynamics 365 for Operations'taki ER ayarlarında etkin sağlayıcı olarak seçilmişse düzenlenebilir. Her bir model konfigürasyonu **Veri modeli** bileşenini içerir. Yeni bir biçim konfigürasyonu belirli bir veri modeli konfigürasyonundan oluşturulabilir (türetilebilir). Oluşturulan biçim konfigürasyonu orijinal veri modeli konfigürasyonunun alt öğesi olarak konfigürasyon ağacında sunulur. Oluşturulan biçim konfigürasyonu bir **Biçim **bileşeni içerir. Orijinal model konfigürasyonunun **Veri modeli** bileşeni varsayılan veri kaynağı olarak alt biçim konfigürasyonunun **Biçim **bileşenine otomatik olarak eklenir. ER konfigürasyonu Dynamics 365 for Operations şirketleri için paylaşılır.

#### <a name="provider"></a>Sunucu

ER sağlayıcısı her bir ER konfigürasyonunun yazarını (sahibini) göstermek için kullanılan taraf tanımlayıcısıdır. ER, konfigürasyon sağlayıcıları listesini yönetmenizi sağlar. Elektronik belgeler için Dynamics 365 for Operations çözümünün parçası olarak sevk edilen biçim konfigürasyonlarının sahibi olarak **Microsoft** konfigürasyon sağlayıcısı işaretlenir.

#### <a name="repository"></a>Depo

ER havuzu ER konfigürasyonlarını depolar. Aşağıdaki ER havuzu türleri şu anda desteklenmektedir: **Operations kaynakları** ve **LCS projesi**. **Operations kaynakları** havuzu Microsoft tarafından bir ER konfigürasyon sağlayıcısı olarak Dynamics 365 for Operations çözümünün parçası olarak yayımlanan konfigürasyonlar listesine erişim sağlar. Bu konfigürasyonlar geçerli Dynamics 365 for Operations kurulumuna aktarılabilir ve elektronik raporlama için kullanılabilir. Bunlar ek yerelleştirmeler/özelleştirmeler için de kullanılabilir. **LCS projesi **havuzu, havuz kayıt aşamasında seçilen belirli bir LCS projesinin (LCS proje varlıkları kitaplığı) konfigürasyonlar listesine erişim sağlar. ER, belirli bir **LCS projesi** havuzu için geçerli Dynamics 365 for Operations kurulumundan paylaşılan konfigürasyonları karşıya yüklemenizi sağlar. Konfigürasyonları belirli bir **LCS projesi** deposundan geçerli Dynamics 365 for Operations kurulumuna da aktarabilirsiniz. Gerekli **LCS projesi** depoları her bir geçerli Dynamics 365 for Operations kurulumunun konfigürasyon sağlayıcısı için ayrı ayrı kaydedilebilir. Her depo belirli bir konfigürasyon sağlayıcısına ayrılabilir.

## <a name="supported-scenarios"></a>Desteklenen senaryolar
### <a name="building-a-data-model"></a>Bir veri modeli oluşturma

ER, belirli bir iş etki alanı için bir veri modeli oluşturmak amacıyla kullanabileceğiniz bir model tasarımcısı sağlar. Tüm etki alanına özgü iş varlıkları ve aralarındaki ilişkiler hiyerarşik olarak yapılandırılmış bir veri modelinde sunulabilir. Aşağıdaki çizim bu tür bir veri modeli örneğini (ödeme etki alanı veri modeli) gösterir. [![Veri modeli örneği](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Tasarım etki alanına özgü veri modeli** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="translating-data-model-content"></a>Veri modeli içeriği çevirme

Veri modeli içeriği (etiketler ve tanımlar) Dynamics 365 for Operations'ın desteklediği diğer dillere çevrilebilir. Aşağıdaki nedenlerden dolayı veri modeli içeriğini çevirmek isteyebilirsiniz:

-   Veri modelini biçim bileşenlerinin eşlemesi için kullanacak yabancı dil konuşan biçim tasarımcıları için tasarım zamanında daha anlaşılır yapmak için
-   O anda oturum açmış Dynamics 365 for Operations kullanıcısı tarafından tercih edilen dildeki yapılandırılmış doğrulama iletilerinin (hatalar ve uyarılar) yanı sıra çalıştırma zamanı parametreleri için komutları ve yardımları sunan daha kullanıcı dostu içerik oluşturmak için

Aşağıdaki çizim veri modeli içeriğinin İngilizceden Japoncaya nasıl çevrildiğine dair bir örneği göstermektedir. [![İngilizce veri modeli içeriği](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png) [![Japonca'ya çevrilmiş veri modeli içeriği](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Veri modeli eşlemelerini yapılandırma

ER, kullanıcılara belirli Dynamics 365 for Operations veri kaynakları için tasarlanan veri modellerini eşleme imkanı veren bir model eşleme tasarımcısı sağlar. Aşağıdaki çizim bu tür veri model eşleşmesinin bir örneğini göstermektedir (**SEPA Alacak Transferi** ödeme etki alanı veri modelinin model eşlemesi). [![Veri modeli eşleştirme örneği](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png) Bu senaryonun ayrıntıları hakkında bilgi edinmek için ER **model eşleme tanımla ve veri kaynakları seç** ve **ER seçili veri kaynaklarına veri modeli eşle** görev kılavuzlarını ( **7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Tasarlanmış model bileşenini model konfigürasyonu olarak depolama

ER, geçerli Dynamics 365 for Operations örneğinin model konfigürasyonu olarak ilgili veri eşleşmeleriyle birlikte tasarlanmış veri modelini saklayabilir. Aşağıdaki çizim bu tür bir veri modeli konfigürasyonu örneğini (ödeme etki alanı model konfigürasyonu) gösterir. [![Veri modeli yapılandırma örneği](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png) Bu senaryonun ayrıntıları hakkında bilgi edinmek için **Seçili veri kaynaklarına ER eşleştirmeye özgü veri modeli** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Temel olarak bir veri modelini kullanan bir biçim oluşturma

ER, model bileşenini temel olarak seçerek seçili bir iş etki alanı için belirli bir elektronik belge biçimini oluşturmak için kullanabileceğiniz bir biçim tasarımcısını destekler. Aynı ER biçimi tasarımcısı veri kaynağı olarak seçili etki alanı veri modeli eşlemesi için oluşturduğunuz bir biçimde eşleme yapmanızı sağlar. Aşağıdaki çizim bu tür biçim örneğini (İngiltere için **BACS** ödeme biçimini destekleyen biçim konfigürasyonu) göstermektedir. [![Veri modelini taban olarak içeren bir biçim örneği](./media/pic-format-1024x690.png)](./media/pic-format.png) Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Tasarım etki alanına özgü biçim** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>OPENXML çalışma sayfası biçiminde elektronik belgeler oluşturmak için bir konfigürasyon oluşturma

ER biçim tasarımcısı belirli bir elektronik belgeyi OPENXML çalışma sayfası biçiminde oluşturmak için kullanılabilir. Aşağıdaki çizim, bu biçim türüne bir örneği gösterir (OPENXML çalışma sayfasını seçilmiş ödeme günlüğü ayrıntıları ile yapılandırmak için bir biçim yapılandırması):[![res-ER-biçim-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) Bu senaryonun ayrıntıları ile aşina olmak için, **ER Raporlar için OPENXML biçiminde bir yapılandırma oluşturma** görev kılavuzunu oynatın (**7.5.4.3 Al/geliştirme BT hizmeti/çözüm bileşenleri (10677)** iş sürecinin parçası olarak). Bu görev kılavuzunun biçim şablonu aktarımı adımını tamamlamak için tasarlanan ER biçimi şablonu olarak aşağıda verilen Excel dosyasını kullanın: [Ödeme Raporu Şablonu (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Biçim konfigürasyonunda tasarlanmış bir biçim bileşeni depolama

ER, geçerli Dynamics 365 for Operations kurulumunun biçim konfigürasyonu olarak yapılandırılmış veri eşlemeleriyle birlikte tasarlanmış bir biçimi depolayabilir. Bu tür bir konfigürasyon biçimi örneği önceki çizimde gösterilmektedir (**BACS (UK)**, **Ödeme modeli **konfigürasyonunun alt öğesi). Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Tasarım etki alanına özgü biçim** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Oluşturulan biçimi dahili olarak kullanmaya başlamak için Dynamics 365 for Operations'ı yapılandırma

Dynamics 365 for Operations elektronik raporları oluşturmak için oluşturulan biçimi kullanmaya başlamak için yapılandırılabilir. Oluşturulmuş biçim konfigürasyonu başvurusu belirli bir etki alanı ayarları içinde tanımlanmalıdır. Örneğin, elektronik satıcı ödemeleri için BACS biçiminde ER biçim konfigürasyonu kullanmaya başlamak için biçim konfigürasyonu aşağıdaki çizimlerde gösterildiği gibi belirli ödeme yöntemlerinde referans olarak verilmelidir: 

[![BACS (UK) biçim konfigürasyonu](media/ger-bacs-uk-format-configuration.png) 

[![Ödeme yönteminde BACS (UK) biçimine başvurma](media/ger-bacs-uk-format-method.png) 

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Ödemeler için elektronik belge oluşturmak için biçim kullan** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

## <a name="handling-er-components"></a>ER bileşenlerini işleme
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER bileşenini harici olarak teklif etmek için LCS'de bir ER bileşeni yayınlama (yerelleştirme)

Oluşturulan bileşen sahibi (model veya biçim) LCS için bileşenin tamamlanmış sürümünü yayımlamak amacıyla ER kullanabilir. Geçerli ER konfigürasyon sağlayıcısı için **LCS projesi **türü depo gereklidir. Tamamlanmış bir bileşen sürümünün durumu **TAMAMLANDI**'dan **PAYLAŞILAN** olarak değiştirildiğinde, bu sürüm LCS'de yayımlanır. Bir bileşen LCS'de yayınlandığında bu bileşenin sahibi bu bileşeni desteklemek için hizmet sağlayıcısı olur. Örneğin, biçim bileşeni yasal olarak gerekli elektronik bir belge (örneğin, yerelleştirme senaryosuna uygun) oluşturmak için tasarlanmışsa, bu biçimin yasal değişikliklerle uyumlu tutulduğu ve yeni yasal gereksinimler ortaya çıktığında sağlayıcının bileşenin yeni sürümlerini çıkaracağı varsayılır. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Lifecycle Services'a bir yapılandırma yükleme **görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER bileşenini dahili olarak kullanmak üzere LCS'den içe aktarma

ER, ER bileşenlerini LCS'den geçerli Dynamics 365 for Operations kurulumuna aktarmanızı sağlar. **LCS projesi **türü bir depo gereklidir. ER bileşeni LCS'den geçerli Dynamics 365 for Operations kurulumuna aktarıldığında kurulumun sahibi aktarılan bileşenin sahibi (yazar) tarafından sağlanan hizmet tüketicisi olur. Örneğin, ülkeye/bölgeye özel bir biçimde Dynamics 365 for Operations'tan belirli bir elektronik belge oluşturmak için bir biçim bileşeni tasarlanmışsa (yerelleştirme senaryosu) hizmet tüketicisinin yasal gerekliliklerle uyum sağlamak için bu biçimin her türlü güncelleştirmesini yapabileceği varsayılır. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Lifecycle Services'tan bir yapılandırmayı içe aktarma** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Temel olarak başka bir biçim seçerek bir biçim oluşturma (özelleştirme)

ER, LCS'den aktarıla bir bileşenin güncel sürümünden (temel) yeni bir bileşen oluşturmanızı (türetmenizi) sağlar. Örneğin, bir kullanıcı özelleştirme senaryosunu desteklemek için bir elektronik belge için bazı özel gereklilikleri uygulamak amacıyla (örneğin ek alan veya kapsamlı bir tanım) yenir bir biçim türetmek ister. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Yeni temel sürüm benimsenerek biçimi yükselt** görev kılavuzunu (**7.5.4.3 Al/BT servisi geliştir/çözüm bileşenleri (10677)** iş işlemi parçası) oynatın.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Temel biçimin yeni sürümünü seçerek bir biçim yükseltme (rebase)

ER, türetilen bileşenin geçerli taslak sürümünde temel bileşenin en son sürümünün değişikliklerini otomatik olarak benimsemenizi sağlar. Bu işlem *yeniden temelleme*olarak bilinmektedir. Örneğin, LCS'den aktarılan biçimin en son sürümünde kullanılan yeni yasal değişiklik elektronik belgenin bu biçiminin özelleştirilmiş sürümüyle otomatik olarak birleştirilebilir. Otomatik olarak birleştirilemeyen herhangi bir değişiklik çakışma olarak kabul edilir. Bu çakışmalar uygun bileşen için tasarımcı aracında elle çözüm için sunulur. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Yeni temel sürüm benimsenerek biçimi yükselt** görev kılavuzunu (**7.5.4.3 Al/BT servisi geliştir/çözüm bileşenleri (10677)** iş işlemi parçası) oynatın.

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Dynamics 365 for Operations çözümüne teslim edilen ER konfigürasyonları listesi
| Etki alanına özgü veri modeli konfigürasyonları: Başlık | Etki alanı                | Veri modeline dayalı biçim konfigürasyonları: Başlık | Açıklama                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Denetim dosyası modeli                                 | Mali denetim       |                                                   |                                                                    |
|                                                  |                       | Denetim dosyası (NL)                                   | Hollanda için denetim dosyası biçimi                                  |
| BAS-modeli                                        | Vergi raporlama         |                                                   |                                                                    |
|                                                  |                       | BAS (AU)                                          | Avustralya için BAS biçimi                                           |
| İnşaat sektörü plan modeli               | Vergi raporlama         |                                                   |                                                                    |
|                                                  |                       | CIS aylık iade (İNG.)                           | İngiltere için CIS aylık iade biçimi                   |
| Tahsilat mektubu modeli                          | Elektronik faturalama  |                                                   |                                                                    |
|                                                  |                       | OIOUBL Tahsilat Mektubu (DK)                     | Danimarka için OIOUBL tahsilat mektup biçimi                        |
| Elektronik genel muhasebe modeli (MX)          | Vergi raporlama         |                                                   |                                                                    |
|                                                  |                       | Yardımcı Genel Muhasebe XML (MX)                         | Meksika için hesap raporu biçimi başına yardımcı genel muhasebe hareketleri |
|                                                  |                       | Hesap planı XML (MX)                         | Meksika için hesap raporu planı                          |
|                                                  |                       | Günlükler XML (MX)                                 | Meksika için günlük hareketler rapor biçimi                      |
|                                                  |                       | Mizan XML (MX)                            | Meksika için mizan raporu biçimi                             |
| Elster modeli                                     | Vergi raporlama         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | Almanya için Elster biçimi                                          |
| AB Satış listesi modeli                              | Ticari raporlama       |                                                   |                                                                    |
|                                                  |                       | AB satış listesi (DE)                                | Almanya için AB Satış listesi TXT biçimi                               |
|                                                  |                       | AB Satış listesi (DK)                                | Danimarka için AB Satış listesi TXT biçimi                               |
|                                                  |                       | AB Satış listesi (FR)                                | Fransa için AB Satış listesi XML biçimi                                |
|                                                  |                       | AB Satış listesi (NL)                                | Hollanda için AB Satış listesi biçimi                           |
|                                                  |                       | AB Satış listesi TXT (UK)                            | İngiltere için AB Satış listesi TXT biçimi                    |
|                                                  |                       | AB Satış listesi XML (UK)                            | İngiltere için AB Satış listesi XML biçimi                    |
|                                                  |                       | Rapor sütunlu AB Satış listesi                   | Rapor sütunlu AB Satış listesi                                    |
|                                                  |                       | Satır raporlu AB Satış listesi                      | Satır raporlu AB Satış listesi                                       |
| FEC hesap modeli (FR)                        | Vergi raporlama         |                                                   |                                                                    |
|                                                  |                       | FEC Muhasebe verileri XML (FR)                      | Fransa için FEC muhasebe verileri dışa aktarma XML biçimi                   |
| Almanca denetim dosyası                                | Mali denetim       |                                                   |                                                                    |
|                                                  |                       | Almanca denetim dosyası çıktısı                          | Almanya ve Avusturya için denetim dosyası çıktısı                          |
| Intrastat modeli                                  | Ticari raporlama       |                                                   |                                                                    |
|                                                  |                       | Intrastat (DE)                                    | Almanya için Intrastat biçimi                                       |
|                                                  |                       | Intrastat (DK)                                    | Danimarka için Intrastat biçimi                                       |
|                                                  |                       | Intrastat INTRACOM (FR)                           | Fransa için İntrastat INTRACOM biçimi                               |
|                                                  |                       | Intrastat SAISUNIC (FR)                           | Fransa için Intrastat SAISUNIC biçimi                               |
|                                                  |                       | Intrastat (NL)                                    | Hollanda için Intrastat biçimi                               |
|                                                  |                       | Intrastat (UK)                                    | İngiltere için Intrastat biçimi                            |
|                                                  |                       | Intrastat raporu                                  | Intrastat Excel kontrol raporu                                     |
| Müşteri faturası modeli                           | Elektronik faturalama  |                                                   |                                                                    |
|                                                  |                       | OIOUBL Proje kredi notu (DK)                   | Danimarka için OIOUBL Proje kredi notu biçimi                      |
|                                                  |                       | OIOUBL Proje faturası (DK)                       | Danimarka için OIOUBL Proje faturası biçimi                          |
|                                                  |                       | OIOUBL Satışlar kredi notu (DK)                     | Danimarka için OIOUBL Satış kredi notu biçimi                        |
|                                                  |                       | OIOUBL Satış faturası (DK)                         | Danimarka için OIOUBL Satış faturası biçimi                            |
| OB beyanname modeli                             | Vergi raporlama         |                                                   |                                                                    |
|                                                  |                       | OB beyannamesi (NL)                               | Hollanda için OB beyanname biçimi                          |
| Ödeme modeli                                    | Ödemeler              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | Danimarka için Betalingsservice ödeme biçimi                        |
|                                                  |                       | Kambiyo senedi havalesi (FR)                  | Fransa için kambiyo senedini havale biçimi                      |
|                                                  |                       | BTL91 (NL)                                        | Hollanda için BTL91 satıcı ödeme biçimi                    |
|                                                  |                       | CFONB Prelevements (FR)                           | Fransa için CFONB doğrudan borç ödeme biçimi                       |
|                                                  |                       | CFONB Virements (FR)                              | Fransa için CFONB yurtiçi satıcı ödeme biçimi                    |
|                                                  |                       | Nordea Satıcı (DK)                                | Danimarka için Nordea corporate netbank satıcı ödeme biçimi         |
|                                                  |                       | ANZ Doğrudan Kredi Hizmeti (AU)                    | Avustralya için ANZ Doğrudan Kredi Hizmeti Biçimi                 |
|                                                  |                       | CBA Doğrudan Kredi Hizmeti (AU)                    | Avustralya için CBA Doğrudan Kredi Hizmeti Biçimi                 |
|                                                  |                       | NAB Doğrudan Kredi Hizmeti (AU)                    | Avustralya için NAB Doğrudan Kredi Hizmeti Biçimi                 |
|                                                  |                       | STG Doğrudan Kredi Hizmeti (AU)                    | Avustralya için STG Doğrudan Kredi Hizmeti Biçimi                 |
|                                                  |                       | WBC Doğrudan Giriş Sistemi (AU)                      | Avustralya için WBC Doğrudan Giriş Sistemi Biçimi                   |
|                                                  |                       | DirectLink (NZ)                                   | Yeni Zelanda için DirectLink biçimi                              |
|                                                  |                       | JBA Ödeme dosyası (JP)                             | Japonya için JBA Ödeme biçimi                                       |
|                                                  |                       | ISO20022 Kredi transferi                          | Avrupa için SEPA Kredi aktarma biçimi                             |
|                                                  |                       | ISO20022 Kredi transferi (FR)                     | Fransa için SEPA Kredi aktarma biçimi                             |
|                                                  |                       | ISO20022 Kredi transferi (DE)                     | Almanya için SEPA Kredi aktarma biçimi                            |
|                                                  |                       | ISO20022 Kredi transferi (NL)                     | Hollanda için SEPA Kredi aktarma biçimi                    |
|                                                  |                       | ISO20022 Otomatik ödeme                             | Avrupa için SEPA otomatik ödeme biçimi                                |
|                                                  |                       | ISO20022 Otomatik ödeme (FR)                        | Fransa için SEPA otomatik ödeme biçimi                                |
|                                                  |                       | ISO20022 Otomatik ödeme (DE)                        | Almanya için SEPA otomatik ödeme biçimi                               |
|                                                  |                       | ISO20022 Otomatik ödeme (NL)                        | Hollanda için SEPA Otomatik ödeme biçimi                       |
|                                                  |                       | BACS (İNG.)                                         | İngiltere için BACS satıcı ödeme biçimi                  |
| Ters gider                                   | Vergi raporlama         |                                                   |                                                                    |
|                                                  |                       | Ters gider satış listesi                         | Ters gider satış listesi biçimi                                   |
| Hollanda XBRL tümleştirme modeli                     | XBRL raporlama        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL (NL)                                | Hollanda için Semansys XBRL dışa aktarma biçimi                    |
| GAF modeli (MY)                                   | Mali denetim       |                                                   |                                                                    |
|                                                  |                       | GAF dosyası (MY)                                     | Malezya için GAF biçimi                                         |
| Satıcı yaşlandırma raporu (CN)                         | Satıcı veri analizi |                                                   |                                                                    |
|                                                  |                       | Satıcı yaşlandırma raporu biçimi (CN)                   | Çin için Satıcı yaşlandırma raporu biçimi                               |
| Satıcı faturası bildirim modeli                 | Satıcı veri analizi |                                                   |                                                                    |
|                                                  |                       | Satıcı faturası bildirimi (IS)                   | İzlanda için Satıcı fatura bildirimi biçimi                      |
|                                                  |                       | Satıcı fatura bildirimi raporu (IS)            | İzlanda için Satıcı fatura bildirimi raporu                      |



<a name="see-also"></a>Ayrıca bkz.
--------

[Yerelleştirme gereksinimleri: Elektronik raporlama konfigürasyon oluştur](electronic-reporting-configuration.md)

[Elektronik raporlama yapılandırma yaşam döngüsünü yönetin](general-electronic-reporting-manage-configuration-lifecycle.md)




