---
title: Elektronik raporlama (ER)
description: Bu konu, Elektronik raporlama (ER) aracına genel bakış sağlar. Temel kavramlar, ER'nin desteklediği senaryolar ve çözümün bir parçası olarak tasarlanan ve yayınlanan biçimlerin listesini içermektedir.
author: NickSelin
manager: AnnBe
ms.date: 03/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc544211891c19104b2b3cb704b55a074784d608
ms.sourcegitcommit: b95bc0f81bd3bb3d9ec4c61f64f93b5c2bef9e05
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/28/2019
ms.locfileid: "902972"
---
# <a name="electronic-reporting-er"></a>Elektronik raporlama (ER)

[!include [banner](../includes/banner.md)]

Bu konu, Elektronik raporlama (ER) aracına genel bakış sağlar. Temel kavramlar, ER'nin desteklediği senaryolar ve çözümün bir parçası olarak tasarlanan ve yayınlanan biçimlerin listesini içermektedir.

ER çeşitli ülkelerin/bölgelerin yasal gereksinimlerine uygun olarak hem gelen hem de giden elektronik belgeler için biçimleri yapılandırmak amacıyla kullanabileceğiniz bir araçtır. ER, yaşam döngüleri boyunca bu biçimleri yönetmenizi sağlar. Örneğin, yeni mevzuat gerekliliklerini uygulayabilir ve devlet kurumları, bankalar ve diğer taraflarla elektronik olarak belge alışverişi yapmak için gerekli biçimde işletme belgeleri oluşturursunuz.

ER altyapısı geliştiricilerden ziyade iş kullanıcılarını hedefler. Çünkü kod yerine biçimleri yapılandırırsınız, elektronik belgeler için biçimler oluşturmak ve ayarlamak için süreçler daha hızlı ve kolaydır.

ER şimdilik TEXT, XML, Microsoft Word belgesi ve OPENXML çalışma sayfası biçimlerini desteklemektedir. Ancak bir uzantı arabirimi ek biçimleri destekler.

## <a name="capabilities"></a>Beceriler
ER altyapısı aşağıdaki yeteneklere sahiptir:

- Farklı etki alanlarında elektronik raporlama için tek bir paylaşımlı aracı temsil eder ve Microsoft Dynamics 365 for Finance and Operations için bir tür elektronik raporlama yapan 20'den fazla farklı altyapının yerini alır.
- Rapor biçiminin şu anki Finance and Operations uygulamasından yalıtılmasını sağlar. Diğer bir deyişle, biçim Finance and Operations farklı sürümleri için geçerlidir.
- Özgün biçime dayalı özel bir biçim oluşturulmasını destekler. Yerelleştirme/özelleştirme gereklilikleri yüzünden özgün biçim değişmiş olduğundan özelleştirilmiş biçimi otomatik olarak yükseltme yeteneğini de içerir.
- Microsoft ve Microsoft ortakları için elektronik raporlamada yerelleştirme gerekliliklerini desteklemek amacıyla birincil standart araç haline dönüşür.
- Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla biçimleri iş ortakları ve müşterilere dağıtma yeteneğini destekler.

## <a name="key-concepts"></a>Kilit kavramlar
### <a name="components"></a>Bileşenler

ER iki tür bileşeni destekler: **Veri modeli** ve **Biçim**.

#### <a name="data-model-components"></a>Veri modeli bileşenleri

Bir veri modeli bileşeni, bir veri yapısının soyut bir temsilidir. Belirli bir iş etki alanını, bu etki alanı için raporlama gereksinimlerini tatmin edecek ayrıntıyla tanımlamak için kullanılır. Veri modeli bileşeni aşağıdaki bölümlerden oluşur:

- Etki alanına özgü iş varlıkları kümesi olarak veri modeli ve bu varlıkların aralarındaki ilişkilerin hiyerarşik olarak tanımı.
- Seçilen Finance and Operations veri kaynaklarını, veri bileşenine ilişkin veri akışı ve işletme veri popülasyonu kurallarını çalışma zamanında belirten bir veri modelinin tek tek öğelerine bağlayan model eşleme.

Bir iş varlık veri modeli (kayıt) kapsayıcı olarak temsil edilir. İş varlık özellikleri veri öğelerini (alanları) olarak temsil edilir. Her veri öğesinin benzersiz bir ad, etiket, açıklama ve değeri vardır. Her bir veri öğesinin değeri, dize, tamsayı, tarih, çetele, Boole vb. olarak tanınacak şekilde tasarlanabilir. Ayrıca başka bir kayıt veya kayıt listesi olabilir.

Tek bir veri modeli bileşeni, birden fazla etki alanı iş varlığı hiyerarşisi içerebilir. Çalışma zamanında rapora özel veri akışı destekleyen bir model eşleştirmesi içerebilir. Hiyerarşiler eşleme modeli kökü olarak seçilen tek bir kayıt tarafından ayrıştırılır. Örneğin, ödeme etki alanının veri modeli aşağıdaki eşlemeleri destekliyor olabilir:

- Şirket \> Satıcı \> AP etki alanının ödeme hareketleri
- Müşteri \> Şirket \> AR etki alanının ödeme hareketleri

Şirket ve ödeme hareketleri gibi iş varlıklarının bir defa tasarlandığını unutmayın. Daha sonra farklı eşleşmeler bunları yeniden kullanır.

Giden elektronik belgeleri destekleyen bir model eşleştirmesi aşağıdaki özellikleri içerir:

- Veri modeli için veri kaynakları olarak farklı Finance and Operations veri türlerini kullanabilir. Örneğin tabloları, veri varlıklarını, yöntemleri veya çeteleleri kullanabilir.
- Bazı verilerin çalışma zamanında belirtilmesi gerekiyorsa bir veri modeli için veri kaynağı olarak tanımlanabilen kullanıcı giriş parametrelerini destekler.
- Finance and Operations verisinin gerekli gruplara dönüştürülmesini destekler. Veriyi filtrelemenize, sıralamanıza, toplamanıza ve Microsoft Excel formüllerine benzerlik gösteren, formüller aracılığıyla tasarlanmış mantıksal hesaplanan alanları mantıksal olarak hesaplanmış alanlar eklemenize, aşağıda gösterildiği gibi olanak sağlar. Daha fazla bilgi için [Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md) konusuna bakın.

[![Formül tasarımcısı](./media/ER-overview-01.png)](./media/ER-overview-01.png)

Gelen elektronik belgeleri destekleyen bir model eşleştirmesi aşağıdaki özellikleri içerir:

- Farklı güncelleştirilebilir veri öğelerini hedefler olarak kullanabilir. Bu veri öğeleri tablolar, veri varlıkları ve görünümler içerir. Veri, gelen elektronik raporlardan veriyi kullanarak güncelleştirilebilir. Birden çok hedef tek bir model eşlemede kullanılabilir.
- Bazı verilerin çalışma zamanında belirtilmesi gerekiyorsa bir veri modeli için veri kaynağı olarak tanımlanabilen kullanıcı giriş parametrelerini destekler.

Bir veri modeli bileşeni, raporlamayı veri kaynaklarının fiziksel uygulamasından ayırmak için raporlama için bir birleştirilmiş veri kaynağı olarak kullanılacak her bir iş etki alanı için tasarlanır. Etki alanına özel iş konseptlerini ve işlevlerini, bir raporlama biçiminin ilk tasarımını ve gelecekteki bakımını daha verimli hale getirecek bir biçimde temsil eder.

#### <a name="format-components-for-outgoing-electronic-documents"></a>Giden elektronik belgeler için biçim bileşenleri

Biçim bileşeni çalışma zamanında oluşturulacak raporlama çıktısının planıdır. Plan aşağıdaki öğelerden oluşur:

- Çalışma zamanında oluşturulan giden elektronik belgenin yapısı ve içeriğini tanımlayan biçim.
- Bir dizi kullanıcı giriş parametresi ve seçilen model eşlemesini kullanan etki alanına özgü veri modeli olarak veri kaynakları.
- Çalışma zamanında veri akışı ve biçim çıktı oluşturma kurallarını belirten bir biçimi için tek tek öğelerini barındıran biçim veri kaynaklarının bağlama kümesi olarak biçim eşleme.
- Bir biçim doğrulaması bağlamında çalışan bağlı olarak çalışma zamanında rapor oluşturmayı denetleyen yapılandırılabilir kurallar kümesi olarak. Örneğin, bir satıcının ödemelerinin çıktı oluşturmasını durduran bir kural olabilir ve seçilen satıcının, örneğin banka hesap numarası gibi belirli öznitelikleri eksik olduğunda bir özel durum ilan edebilir.

Biçim bileşeni aşağıdaki işlevleri destekler:

- Raporlama çıktısının çeşitli biçimlerde tek tek dosyalar şeklinde oluşturulması: örneğin metin, XML, Microsoft Word belgesi veya çalışma sayfası.
- Birden fazla dosyanın ayrı ayrı oluşturulması ve bu dosyaların zip dosyalarına kapsüllenmesi.

Biçim bileşeni, raporlama çıktısında kullanılabilen belirli dosyaları eklemenize olanak sağlar:

- OPENXML çalışma biçiminde çıktı için şablon olarak kullanılabilen bir çalışma sayfasını içeren Excel çalışma kitapları
- Word dosyaları, Microsoft Word belgesi biçiminde çıktı için bir şablon olarak kullanılabilecek bir belge içerebilirler.
- Önceden tanımlanmış dosyalar olarak biçim çıktısına dahil edilebilen diğer dosyalar

Aşağıdaki görsel, verinin bu biçimler için nasıl aktığını gösterir.

[![Giden biçim bileşenleri için veri akışı](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Biçim yapılandırmasının eşleşmesini, tek bir ER biçim yapılandırmasını çalıştırmak ve giden bir elektronik belge oluşturmak için tanımlamanız gerekir.

#### <a name="format-components-for-incoming-electronic-documents"></a>Gelen elektronik belgeler için biçim bileşenleri
Bir biçim bileşeni, çalışma zamanında içe aktarılan gelen belgenin planıdır. Plan aşağıdaki öğelerden oluşur:

- Çalışma zamanında içe aktarılan veriyi içeren gelen elektronik belgenin yapısını ve içeriğini tanımlayan bir biçim. Bir biçim bileşeni, bir gelen belgeyi metin ve XML gibi çeşitli biçimlerde ayrıştırmak için kullanılır.
- Etki alanına özel bir veri modelinin öğelerine ayrı ayrı biçim öğeleri bağlayan bir biçim eşlemesi. Çalışma zamanında, veri modelindeki öğeler, bir gelen belgedeki verileri içe aktarmak için veri akışını ve kuralları belirtir ve daha sonra veriyi bir veri modelinde depolar.
- Bir biçim doğrulaması bağlamında çalışan bağlı olarak çalışma zamanında veri içe aktarmayı denetleyen yapılandırılabilir kurallar kümesi olarak. Örneğin, bir satıcının ödemelerini içeren bir banka ekstresinin veri içe aktarması durduran bir kural olabilir ve satıcının satıcı kimlik saptama kodu gibi belirli öznitelikleri eksik olduğunda bir özel durum ilan edebilir.

Aşağıdaki görsel, verinin bu biçimler için nasıl aktığını gösterir.

[![Gelen biçim bileşenleri için veri akışı](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Gelen bir elektronik belgeden veri içe aktarmak için tek bir ER biçim yapılandırması çalıştırmak için bir biçim yapılandırmasının arzulanan eşlemesini ve ayrıca bir model eşlemesinin tümleştirme noktasını tanımlamanız gerekir. Aynı model eşlemesini ve hedefleri, farklı türde gelen belgeler için farklı biçimlerle birlikte kullanabilirsiniz.

#### <a name="component-versioning"></a>Bileşen sürüm oluşturma

Sürüm Oluşturma ER bileşenleri için desteklenir. Aşağıdaki iş akışı ER bileşenlerindeki değişiklikleri yönetmek için sağlanır:

1. Başlangıçta oluşturulan sürüm **Taslak** sürüm olarak işaretlenir. Bu sürüm düzenlenebilir ve test çalıştırmaları için kullanılabilir.
2. **Taslak** sürümü **Tamamlandı** sürümüne dönüştürülebilir. Bu sürüm yerel raporlama işlemlerinde kullanılabilir.
3. **Tamamlandı** sürümü **Paylaşımlı** sürümüne dönüştürülebilir. Sürüm LCS üzerinde yayımlanır ve küresel raporlama işlemlerinde kullanılabilir.
4. **Paylaşılan** sürümü **Devam ettirilmeyen** sürümüne dönüştürülebilir. Daha sonra bu sürüm silinebilir.

**Tamamlandı** veya **Paylaşılan** durumuna sahip sürümler diğer veri değişimleri için kullanılabilir. Aşağıdaki eylemler, şu durumlara sahip bir bileşen üzerinde gerçekleştirilebilir:

- Bileşen, XML biçiminde sıralanabilir ve XML biçiminde bir dosya olarak dışa aktarılabilir.
- Bileşen bir XML dosyasından tekrar sıralanabilirler ve ER bileşeninin yeni bir sürümü olarak Finance and Operations'ten içe aktarılabilirler.

#### <a name="component-date-effectivity"></a>Bileşen tarihi geçerlilik

ER bileşen sürümleri tarih etkilidir. **Yürürlük başlangıcı** tarihini, raporlama işlemleri için bileşenin geçerlilik kazandığı tarihi belirtmek amacıyla bir ER bileşeni için ayarlayabilirsiniz. Finance and Operations oturum tarihi bir bileşen yürütme için geçerli olup olmadığını tanımlamak için kullanılır. Belirli bir tarih için birden fazla sürüm geçerliyse raporlama işlemleri için en son sürüm kullanılır.

#### <a name="component-access"></a>Bileşen erişim

ER biçimli bileşenlere erişilmesi ISO ülke/bölge kodu ayarlarına bağlıdır. Bu ayar bir biçim konfigürasyonunun seçilen sürümü için boş ise çalışma zamanında herhangi bir şirketinden biçim bileşenine erişilebilir. Bu ayar ISO ülke/bölge kodları içeriyorsa biçim bileşenine yalnızca biçim bileşeninin ISO ülke/bölge kodlarının biri için tanımlanan birincil adrese sahip şirketlerinden ulaşılabilir.

Bir veri biçimi bileşeninin farklı sürümleri ISO ülke/bölge kodları için farklı ayarlara sahip olabilir.

#### <a name="configuration"></a>Yapılandırma

Bir ER yapılandırması, belirli bir ER bileşeninin sarmalayıcısıdır. Bu bileşen bir veri modeli bileşeni ya da biçim bileşeni olabilir. Bir konfigürasyon bir ER bileşeninin farklı sürümlerini içerebilir. Her yapılandırma belirli bir yapılandırma sağlayıcı tarafından sahip olunan olarak işaretlenir. Bir konfigürasyon bileşeninin **Taslak** sürümü, konfigürasyon sahibi Finance and Operations'taki ER ayarlarında etkin sağlayıcı olarak seçilmişse düzenlenebilir.

Her bir model konfigürasyonu veri modeli bileşenini içerir. Yeni bir biçim konfigürasyonu belirli bir veri modeli konfigürasyonundan kaynaklanarak oluşturulabilir (türetilebilir). Yapılandırma ağacında, oluşturulan biçim yapılandırması, orijinal veri modeli yapılandırmasının alt öğesi olarak belirir.

Oluşturulan biçim konfigürasyonu bir biçim bileşeni içerir. Orijinal model konfigürasyonunun veri modeli bileşeni varsayılan veri kaynağı olarak alt biçim konfigürasyonunun biçim bileşenine otomatik olarak eklenir.

ER konfigürasyonu Finance and Operations şirketleri için paylaşılır.

#### <a name="provider"></a>Sunucu

ER sağlayıcısı her bir ER konfigürasyonunun yazarını (sahibini) göstermek için kullanılan taraf tanımlayıcısıdır. ER, konfigürasyon sağlayıcıları listesini yönetmenizi sağlar. Elektronik belgeler için Finance and Operations çözümünün parçası olarak sevk edilen biçim konfigürasyonlarının sahibi olarak **Microsoft** konfigürasyon sağlayıcısı işaretlenir.

Yeni bir ER sağlayıcısını kaydetmeyi öğrenmek için **ER Bir yapılandırma sağlayıcısı oluşturmak ve bunu etkin olarak işaretlemek** (**7.5.4.3 Al/BT hizmeti geliştir/çözüm bileşenleri (10677)** iş işleminin parçası olan) görev kılavuzunu yürütün.

#### <a name="repository"></a>Depo

ER havuzu ER konfigürasyonlarını depolar. Aşağıdaki ER havuzu türleri şu anda desteklenir: 

- LCS paylaşımlı kitaplık
- LCS projesi
- Dosya sistemi
- Düzenleyici Yapılandırma Hizmeti (RCS)
- İşlem kaynakları


Bir **LCS paylaşımlı kitaplık** deposu Lifecycle Services (LCS) içindeki Paylaşılan varlık kitaplığındaki yapılandırmaların listesine erişim sağlar. Bu türde bir ER deposu, yalnızca Microsoft sağlayıcısı için kaydedilebilir. LCS Paylaşılan varlık kitaplığından ER yapılandırmalarının en güncel sürümlerini mevcut Finance and Operations kurulumuna içe aktarabilirsiniz.

**LCS projesi** havuzu, havuz kayıt aşamasında seçilen belirli bir LCS projesinin (LCS proje varlıkları kitaplığı) konfigürasyonlar listesine erişim sağlar. ER, belirli bir **LCS projesi** havuzu için geçerli Finance and Operations kurulumundan paylaşılan konfigürasyonları karşıya yüklemenizi sağlar. Konfigürasyonları bir **LCS projesi** deposundan geçerli Finance and Operations kurulumuna da aktarabilirsiniz.

Bir **Dosya sistemi** havuzu, AOS servisinin barındırıldığı makinede xml dosyaları olarak yerel dosya sisteminin belirli bir klasöründe bulunan yapılandırmalar listesine erişim sağlar. Gerekli klasör, havuz kayıt aşamasında seçilir. Konfigürasyonları bir **Dosya sistemi** deposundan geçerli Finance and Operations kurulumuna da aktarabilirsiniz. 

Bu havuz türünün aşağıdaki Dynamics 365 for Finance and Operations ortamlarında erişilebilir olduğunu unutmayın:

- Geliştirme amaçlarıyla dağıtılmış bulutta barındırılan ortamlar (iliştirilmiş paketlerin test modellerini içeren)
- Yerel depolanan ortamlar (şirket içi)

Daha fazla bilgi için bkz: [Elektronik raporlama (ER) yapılandırmalarını içe aktarma](./electronic-reporting-import-ger-configurations.md).

**RCS örneği** havuzu, havuz kayıt aşamasında seçilen belirli bir RCS örneği konfigürasyonlar listesine erişim sağlar. ER, tamamlanmış veya paylaşılan yapılandırmaları seçilen RCS örneğinden geçerli Finance and Operations örneklerini içe aktarmanıza ve böylece elektronik raporlama için kullanmanızı sağlar.

Daha fazla bilgi için bkz. [Düzenleyici Yapılandırma Hizmeti'nden (RCS) Elektronik raporlama (ER) yapılandırmalarını içe aktarma](./rcs-download-configurations.md).

**Operations kaynakları** havuzu Microsoft'un bir ER konfigürasyonu sağlayıcısı olarak ilk başta Finance and Operations çözümünün parçası olarak yayımladığı konfigürasyonlar listesine erişim sağlar. Bu yapılandırmalar geçerli Finance and Operations kurulumuna aktarılabilir ve elektronik raporlama veya basit görev kılavuzları için kullanılabilir. Bunlar ek yerelleştirmeler ve özelleştirmeler için de kullanılabilir. Microsoft ER yapılandırmaları tarafından sağlanan en güncel sürümlerin LCS Paylaşımlı varlık kitaplığından, karşılık gelen ER deposu kullanılarak içe aktarılması gerekir.

Gerekli **LCS projesi**, **Dosya sistemi** ve **Düzenleyici Yapılandırma Servisleri (RCS)** depoları her bir geçerli Finance and Operations kurulumunun konfigürasyon sağlayıcısı için ayrı ayrı kaydedilebilir. Her depo belirli bir konfigürasyon sağlayıcısına ayrılabilir.

## <a name="supported-scenarios"></a>Desteklenen senaryolar
### <a name="building-a-data-model"></a>Bir veri modeli oluşturma

ER, belirli bir iş etki alanı için bir veri modeli oluşturmak amacıyla kullanabileceğiniz bir model tasarımcısı sağlar. Tüm etki alanına özgü iş varlıkları ve aralarındaki ilişkiler hiyerarşik olarak yapılandırılmış bir veri modelinde sunulabilir. Aşağıdaki çizim, bu tür bir veri modeli örneğini (ödeme etki alanı veri modeli) gösterir.

[![Ödeme etki alanı veri modeli](./media/ER-overview-04.png)](./media/ER-overview-04.png)

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Tasarım etki alanına özgü veri modeli** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş süreci) oynatın.

### <a name="translating-data-model-content"></a>Veri modeli içeriği çevirme

Veri modeli içeriği (etiketler ve tanımlar) Finance and Operations'ın desteklediği diğer dillere çevrilebilir. Aşağıdaki nedenlerden dolayı veri modeli içeriğini çevirmek isteyebilirsiniz:

- Veri modelini biçim bileşenlerinin eşlemesi için kullanacak yabancı dilleri konuşan biçim tasarımcıları için tasarım zamanında daha anlaşılır yapmak için.
- O anda oturum açmış kullanıcı tarafından tercih edilen dildeki yapılandırılmış doğrulama iletilerinin (hatalar ve uyarılar) yanı sıra çalıştırma zamanı parametreleri için komutları ve yardımları sunan daha kullanıcı dostu içerik oluşturmak için.

Aşağıdaki çizim, veri modeli içeriğinin İngilizceden Japoncaya nerede çevrildiğine dair bir örneği göstermektedir.

[![İngilizce veri modeli içeriği](./media/ER-overview-05.png)](./media/ER-overview-05.png)

[![Japonca'ya çevrilen veri modeli içeriği](./media/ER-overview-06.png)](./media/ER-overview-06.png)

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Giden belgeler için veri modeli eşlemeleri yapılandırmak

ER, kullanıcılara belirli Finance and Operations veri kaynakları için tasarlanan veri modellerini eşleme imkanı veren bir model eşleme tasarımcısı sağlar. Veri, eşleşmeye bağlı olarak çalışma zamanında seçilen veri kaynaklarından modele alınacaktır. Veri modeli daha sonra giden elektronik belgeler oluşturan ER biçimlerinin soyut bir veri kaynağı kullanılır. Aşağıdaki çizim, bu tür veri model eşleşmesinin bir örneğini göstermektedir (**SEPA Alacak Transferi** ödeme etki alanı veri modelinin model eşlemesi).

[![Veri modeli eşleme örneği ](./media/ER-overview-07.png)](./media/ER-overview-07.png)

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER model eşleme tanımla ve veri kaynakları seç** ve **ER seçili veri kaynaklarına veri modeli eşle** görev kılavuzlarını ( **7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Gelen belgeler için veri modeli eşlemeleri yapılandırmak
ER, kullanıcılara belirli hedefler için tasarlanan veri modellerini eşleme imkanı veren bir model eşleme tasarımcısı sağlar. Örneğin, veri modelleri Finance and Operations güncelleştirilebilir veri bileşenlerine (tablolalar, veri varlıkları ve görünümler) eşlenebilir. Eşlemeye bağlı olarak, Finance and Operations verisi çalışma zamanında, veri modelinden veriyi kullanarak güncelleştirilir. ER biçiminin soyut depolaması olarak veri modeli, gelen bir elektronik belgeden içe aktarılan verilerle doldurulur. Aşağıdaki çizim, bu tür bir veri modeli eşlemesinin örneğini gösterir. Bu örnekte ödeme etki alanı veri modelinin **NETS için içe aktarma eşleme** modeli eşlemesi, Norveç için NETS banka biçimindeki banka ekstrelerinin içe aktarılması için kullanılır.

[![NET veri modeli örneği için içe aktarma eşlemesi](./media/ER-overview-08.png)](./media/ER-overview-08.png)

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Tasarlanmış model bileşenini model konfigürasyonu olarak depolama

ER, geçerli Finance and Operations örneğinin model konfigürasyonu olarak ilgili veri eşleşmeleriyle birlikte tasarlanmış veri modelini saklayabilir. Aşağıdaki çizim, bu tür bir veri modeli konfigürasyonu örneğini (ödeme etki alanı model konfigürasyonu) gösterir.

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER seçili veri kaynaklarına veri modeli eşle** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Temel olarak bir veri modelini kullanan bir biçim oluşturma

ER, model bileşenini temel olarak seçerek seçili bir iş etki alanı için bir elektronik belge biçimini oluşturmak için kullanabileceğiniz bir biçim tasarımcısını destekler. Aynı ER biçimi tasarımcısı, veri kaynağı olarak seçili etki alanı veri modeli eşlemesi için oluşturduğunuz bir biçimde eşleme yapmanızı sağlar. Aşağıdaki çizim, bu tür biçim örneğini (İngiltere için **BACS** ödeme biçimini destekleyen biçim konfigürasyonu) göstermektedir.

[![Temel olarak bir veri modeline sahip biçim örneği](./media/ER-overview-09.png)](./media/ER-overview-09.png)

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Tasarım etki alanına özgü biçim** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>OPENXML çalışma sayfası biçiminde elektronik belgeler oluşturmak için bir konfigürasyon oluşturma

ER biçim tasarımcısı, bir elektronik belgeyi OPENXML çalışma sayfası biçiminde oluşturmak için kullanılabilir. Aşağıdaki çizim, bu tür bir biçim (Seçili ödeme günlüğü ayrıntılarını içeren OPENXML çalışma sayfası oluşturmak için biçim konfigürasyonu) örneğini göstermektedir.

[![ER biçimi Excel resmi](./media/ER-overview-10.png)](./media/ER-overview-10.png)

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **Raporlar için OPENXML biçiminde bir konfigürasyon oluştur** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın. Bir şablonun içe aktarılamsı görev kılavuzunun bir parçası olarak, [Ödeme Raporu Şablonu (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202) Excel dosyasını şablon olarak kullanın.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Bir Word belgesi biçiminde elektronik belgeler oluşturmak için bir konfigürasyon oluşturma
ER biçim tasarımcısı, bir elektronik belgeyi bir Word belgesi biçiminde oluşturmak için kullanılabilir. Aşağıdaki çizim, bu tür bir biçimin örneğini gösterir. Bu biçimin, rapor çıktısını OPENXML biçiminde oluşturmak için özgün olarak tasarlanmış olan mevcut ER yapılandırmasını yeniden kullandığını unutmayın.

[![ER biçimi Word resmi](./media/ER-overview-11.png)](./media/ER-overview-11.png)

Bu senaryonun ayrıntıları hakkında bilgi edinmek için ER Microsoft WORD biçiminde raporlar oluşturmak için bir yapılandırma tasarlama görev kılavuzunu (7.5.4.3 Al/BT hizmeti geliştir/çözüm bileşenleri (10677) iş işleminin parçası olarak) oynatın. Bir şablonu içe aktarmak için görev kılavuzu adımının bir parçası olarak, aşağıdaki Word dosyalarını ER biçimi için bir şablon olarak kullanın:

- [Ödeme Raporu Şablonu (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Ödeme Raporunun bağlı şablonu (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Gelen elektronik belgelerden veri aktarmak için bir yapılandırma oluşturmak
ER biçim tasarımcısı, XML ya da metin biçiminde veri içe aktarma için planlanan bir elektronik belgeyi tanımlamak için kullanılabilir. Tasarlanan biçim, gelen bir belgeyi ayrıştırmak için kullanılır. ER biçimi eşleme tasarımcısı, tasarlanan biçimin öğelerinin veri modeline bağlamasını tanımlamak için kullanılabilir. Aşağıdaki çizimler, bu tür bir biçim ve biçim eşlemesinin örneğini gösterir. Bu örnekte, satıcı ödeme ayrıntılarını metin biçiminde içeren NETS banka ekstreleri içe aktarılır.

[![ER Biçim tasarımcısı](./media/ER-overview-12.png)](./media/ER-overview-12.png)

[![ER model eşleme tasarımcısı](./media/ER-overview-13.png)](./media/ER-overview-13.png)

Bu senaryonun ayrıntıları hakkında bilgi edinmek için Harici bir dosyadan veri içe aktarmak için gerekli ER yapılandırmalarını oluşturma görev kılavuzunu (7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677) iş sürecinin parçası) oynatın. Bu kılavuzu oynatmak için aşağıdaki dosyaları kullanın:

- [ER veri modeli konfigürasyonu (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [ER biçim yapılandırma (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Gelen belgenin XML biçimnde örneği (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Gelen belgenin verisini yönetmek için çalışma sayfası örneği (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Biçim konfigürasyonunda tasarlanmış bir biçim bileşeni depolama

ER, geçerli Finance and Operations kurulumunun biçim konfigürasyonu olarak yapılandırılmış veri eşlemeleriyle birlikte tasarlanmış bir biçimi depolayabilir. Bu tür bir konfigürasyon biçimi örneği önceki çizimde gösterilmektedir (**BACS (UK)**, **Ödeme modeli** konfigürasyonunun alt öğesi). Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Tasarım etki alanına özgü biçim** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="configuring-finance-and-operations-to-start-to-use-a-created-format-internally"></a>Oluşturulan biçimi dahili olarak kullanmaya başlamak için Finance and Operations'ı yapılandırma

Finance and Operations elektronik raporları oluşturmak için oluşturulan biçimi kullanmaya başlamak için yapılandırılabilir. Oluşturulmuş biçim konfigürasyonu başvurusu belirli bir etki alanı ayarları içinde tanımlanmalıdır. Örneğin, elektronik satıcı ödemeleri için BACS biçiminde ER biçim konfigürasyonu kullanmaya başlamak için biçim konfigürasyonu aşağıdaki çizimlerde gösterildiği gibi belirli ödeme yöntemlerinde referans olarak verilmelidir:

[![BACS (UK) biçim konfigürasyonu](./media/ER-overview-14.png)](./media/ER-overview-14.png)

[![Ödeme yönteminde BACS (UK) biçimine başvurma](./media/ER-overview-15.png)](./media/ER-overview-15.png)

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Ödemeler için elektronik belge oluşturmak için biçim kullan** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

## <a name="handling-er-components"></a>ER bileşenlerini işleme
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER bileşenini harici olarak teklif etmek için LCS'de bir ER bileşeni yayınlama (yerelleştirme)

Oluşturulan bileşen sahibi (model veya biçim) LCS için bileşenin tamamlanmış sürümünü yayımlamak amacıyla ER kullanabilir. Geçerli ER konfigürasyon sağlayıcısı için **LCS projesi** türü depo gereklidir. Tamamlanmış bir bileşen sürümünün durumu **TAMAMLANDI**'dan **PAYLAŞILAN** olarak değiştirildiğinde, bu sürüm LCS'de yayımlanır. Bir bileşen LCS'de yayınlandığında bu bileşenin sahibi bu bileşeni desteklemek için hizmet sağlayıcısı olur. Örneğin, biçim bileşeni yasal olarak gerekli elektronik bir belge (örneğin, yerelleştirme senaryosuna uygun) oluşturmak için tasarlanmışsa, bu biçimin yasal değişikliklerle uyumlu tutulduğu ve yeni yasal gereksinimler ortaya çıktığında sağlayıcının bileşenin yeni sürümlerini çıkaracağı varsayılır. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Lifecycle Services'a bir yapılandırma yükleme** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER bileşenini dahili olarak kullanmak üzere LCS'den içe aktarma

ER, ER bileşenlerini LCS'den geçerli Finance and Operations kurulumuna aktarmanızı sağlar. **LCS projesi** türü bir depo gereklidir. ER bileşeni LCS'den geçerli Finance and Operations kurulumuna aktarıldığında kurulumun sahibi aktarılan bileşenin sahibi (yazar) tarafından sağlanan hizmet tüketicisi olur. Örneğin, ülkeye/bölgeye özel bir biçimde Finance and Operations'tan belirli bir elektronik belge oluşturmak için bir biçim bileşeni tasarlanmışsa (yerelleştirme senaryosu) hizmet tüketicisinin yasal gerekliliklerle uyum sağlamak için bu biçimin her türlü güncelleştirmesini yapabileceği varsayılır. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Lifecycle Services'tan bir yapılandırmayı içe aktarma** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Temel olarak başka bir biçim seçerek bir biçim oluşturma (özelleştirme)

ER, LCS'den aktarıla bir bileşenin güncel sürümünden (temel) yeni bir bileşen oluşturmanızı (türetmenizi) sağlar. Örneğin, bir kullanıcı özelleştirme senaryosunu desteklemek için bir elektronik belge için bazı özel gereklilikleri uygulamak amacıyla (örneğin ek alan veya kapsamlı bir tanım) yenir bir biçim türetmek ister. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Yeni temel sürüm benimsenerek biçimi yükselt** görev kılavuzunu (**7.5.4.3 Al/BT servisi geliştir/çözüm bileşenleri (10677)** iş işlemi parçası) oynatın.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Temel biçimin yeni sürümünü seçerek bir biçim yükseltme (rebase)

ER, türetilen bileşenin geçerli taslak sürümünde temel bileşenin en son sürümünün değişikliklerini otomatik olarak benimsemenizi sağlar. Bu işlem *yeniden temelleme*olarak bilinmektedir. Örneğin, LCS'den aktarılan biçimin en son sürümünde kullanılan yeni yasal değişiklik elektronik belgenin bu biçiminin özelleştirilmiş sürümüyle otomatik olarak birleştirilebilir. Otomatik olarak birleştirilemeyen her değişiklik bir çakışma olarak kabul edilir. Bu çakışmalar uygun bileşen için tasarımcı aracında elle çözüm için sunulur. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Bu biçimin yeni temel sürüm benimsenerek biçimi yükselt** görev kılavuzunu (**7.5.5.3 Al/Değiştirilmiş BT servisi geliştir/çözüm bileşeni (10683)** iş işlemi parçası) oynatın.

## <a name="list-of-er-configurations-that-are-delivered-in-the-finance-and-operations-solution"></a>Finance and Operations çözümüne teslim edilen ER konfigürasyonları listesi

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

## <a name="additional-resources"></a>Ek kaynaklar

- [Yerelleştirme gereksinimleri: Elektronik raporlama konfigürasyon oluştur](electronic-reporting-configuration.md)
- [Elektronik raporlama yapılandırma yaşam döngüsünü yönetin](general-electronic-reporting-manage-configuration-lifecycle.md)
