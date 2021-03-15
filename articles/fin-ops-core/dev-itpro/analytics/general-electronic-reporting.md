---
title: Elektronik raporlamaya (ER) genel bakış
description: Bu konuda, Elektronik raporlama aracına dair genel bir bakış sunulmaktadır. Anahtar kavramlar, desteklenen senaryolar ve çözümün parçası olan biçimler açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33d399c6a9051097d3ea0c7990a37302395d9c77
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093938"
---
# <a name="electronic-reporting-er-overview"></a>Elektronik raporlamaya (ER) genel bakış

[!include [banner](../includes/banner.md)]

Bu konu, Elektronik raporlama (ER) aracına genel bakış sağlar. Temel kavramlar, ER'nin desteklediği senaryolar ve çözümün bir parçası olarak tasarlanan ve yayınlanan biçimlerin listesini içermektedir.

ER çeşitli ülkelerin/bölgelerin yasal gereksinimlerine uygun olarak hem gelen hem de giden elektronik belgeler için biçimleri yapılandırmak amacıyla kullanabileceğiniz bir araçtır. ER, yaşam döngüleri boyunca bu biçimleri yönetmenizi sağlar. Örneğin, yeni mevzuat gerekliliklerini uygulayabilir ve devlet kurumları, bankalar ve diğer taraflarla elektronik olarak belge alışverişi yapmak için gerekli biçimde işletme belgeleri oluşturursunuz.

ER altyapısı geliştiricilerden ziyade iş kullanıcılarını hedefler. Çünkü kod yerine biçimleri yapılandırırsınız, elektronik belgeler için biçimler oluşturmak ve ayarlamak için süreçler daha hızlı ve kolaydır.

ER şimdilik TEXT, XML, Microsoft Word belgesi ve OPENXML çalışma sayfası biçimlerini desteklemektedir. Ancak bir uzantı arabirimi ek biçimleri destekler.

## <a name="capabilities"></a>Beceriler

ER altyapısı aşağıdaki yeteneklere sahiptir:

- Farklı etki alanlarında elektronik raporlama için tek bir paylaşımlı aracı temsil eder ve Finance and Operations için bir tür elektronik raporlama yapan 20'den fazla farklı altyapının yerini alır.
- Rapor biçiminin şu anki uygulamadan yalıtılmasını sağlar. Diğer bir deyişle, biçim farklı sürümler için geçerlidir.
- Özgün biçime dayalı özel bir biçim oluşturulmasını destekler. Yerelleştirme/özelleştirme gereklilikleri yüzünden özgün biçim değişmiş olduğundan özelleştirilmiş biçimi otomatik olarak yükseltme yeteneğini de içerir.
- Microsoft ve Microsoft ortakları için elektronik raporlamada yerelleştirme gerekliliklerini desteklemek amacıyla birincil standart araç haline dönüşür.
- Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla biçimleri iş ortakları ve müşterilere dağıtma yeteneğini destekler.

## <a name="key-concepts"></a>Kilit kavramlar

### <a name="components"></a>Bileşenler

ER iki tür bileşeni destekler: **Veri modeli** ve **Biçim**.

#### <a name="data-model-and-model-mapping-components"></a>Veri modeli ve model eşleme bileşenleri

Bir veri modeli bileşeni, bir veri yapısının soyut bir temsilidir. Belirli bir iş etki alanını, bu etki alanı için raporlama gereksinimlerini tatmin edecek ayrıntıyla tanımlamak için kullanılır. Veri modeli bileşeni aşağıdaki bölümlerden oluşur:

- <a name="DataModelComponent"></a>Etki alanına özgü iş varlıkları kümesi olarak veri modeli ve bu varlıkların aralarındaki ilişkilerin hiyerarşik olarak tanımı.
- <a name="ModelMappingComponent"></a>Seçilen uygulama veri kaynaklarını, veri bileşenine ilişkin veri akışı ve işletme veri popülasyonu kurallarını çalışma zamanında belirten bir veri modelinin tek tek öğelerine bağlayan model eşleme.

Bir iş varlık veri modeli (kayıt) kapsayıcı olarak temsil edilir. İş varlık özellikleri veri öğelerini (alanları) olarak temsil edilir. Her veri öğesinin benzersiz bir ad, etiket, açıklama ve değeri vardır. Her bir veri öğesinin değeri, dize, tamsayı, tarih, çetele, Boole vb. olarak tanınacak şekilde tasarlanabilir. Ayrıca başka bir kayıt veya kayıt listesi olabilir.

Tek bir veri modeli bileşeni, birden fazla etki alanı iş varlığı hiyerarşisi içerebilir. Çalışma zamanında rapora özel veri akışı destekleyen bir model eşleştirmesi içerebilir. Hiyerarşiler eşleme modeli kökü olarak seçilen tek bir kayıt tarafından ayrıştırılır. Örneğin, ödeme etki alanının veri modeli aşağıdaki eşlemeleri destekliyor olabilir:

- Şirket \> Satıcı \> AP etki alanının ödeme hareketleri
- Müşteri \> Şirket \> AR etki alanının ödeme hareketleri

Şirket ve ödeme hareketleri gibi iş varlıklarının bir defa tasarlandığını unutmayın. Daha sonra farklı eşleşmeler bunları yeniden kullanır.

Giden elektronik belgeleri destekleyen bir model eşleştirmesi aşağıdaki özellikleri içerir:

- Veri modeli için veri kaynakları olarak farklı veri türlerini kullanabilir. Örneğin tabloları, veri varlıklarını, yöntemleri veya çeteleleri kullanabilir.
- Bazı verilerin çalışma zamanında belirtilmesi gerekiyorsa bir veri modeli için veri kaynağı olarak tanımlanabilen kullanıcı giriş parametrelerini destekler.
- Verinin gerekli gruplara dönüştürülmesini destekler. Veriyi filtrelemenize, sıralamanıza, toplamanıza ve Microsoft Excel formüllerine benzerlik gösteren, formüller aracılığıyla tasarlanmış mantıksal hesaplanan alanlar eklemenize olanak sağlar. Daha fazla bilgi için bkz. [Elektronik raporlamada (ER) formül tasarımcısı](general-electronic-reporting-formula-designer.md).

Gelen elektronik belgeleri destekleyen bir model eşleştirmesi aşağıdaki özellikleri içerir:

- Farklı güncelleştirilebilir veri öğelerini hedefler olarak kullanabilir. Bu veri öğeleri tablolar, veri varlıkları ve görünümler içerir. Veri, gelen elektronik raporlardan veriyi kullanarak güncelleştirilebilir. Birden çok hedef tek bir model eşlemede kullanılabilir.
- Bazı verilerin çalışma zamanında belirtilmesi gerekiyorsa bir veri modeli için veri kaynağı olarak tanımlanabilen kullanıcı giriş parametrelerini destekler.

Bir veri modeli bileşeni, raporlamayı veri kaynaklarının fiziksel uygulamasından ayırmak için raporlama için bir birleştirilmiş veri kaynağı olarak kullanılacak her bir iş etki alanı için tasarlanır. Etki alanına özel iş konseptlerini ve işlevlerini, bir raporlama biçiminin ilk tasarımını ve gelecekteki bakımını daha verimli hale getirecek bir biçimde temsil eder.

#### <a name="format-components-for-outgoing-electronic-documents"></a><a name="FormatComponentOutbound"></a>Giden elektronik belgeler için biçim bileşenleri

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

#### <a name="format-components-for-incoming-electronic-documents"></a><a name="FormatComponentInbound"></a>Gelen elektronik belgeler için biçim bileşenleri

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
- Bileşen bir XML dosyasından tekrar sıralanabilirler ve ER bileşeninin yeni bir sürümü olarak uygulamadan içe aktarılabilirler.

#### <a name="component-date-effectivity"></a>Bileşen tarihi geçerlilik

ER bileşen sürümleri tarih etkilidir. **Yürürlük başlangıcı** tarihini, raporlama işlemleri için bileşenin geçerlilik kazandığı tarihi belirtmek amacıyla bir ER bileşeni için ayarlayabilirsiniz. Uygulama oturum tarihi bir bileşenin yürütme için geçerli olup olmadığını tanımlamak için kullanılır. Belirli bir tarih için birden fazla sürüm geçerliyse raporlama işlemleri için en son sürüm kullanılır.

#### <a name="component-access"></a>Bileşen erişim

ER biçimli bileşenlere erişilmesi ISO ülke/bölge kodu ayarlarına bağlıdır. Bu ayar bir biçim konfigürasyonunun seçilen sürümü için boş ise çalışma zamanında herhangi bir şirketinden biçim bileşenine erişilebilir. Bu ayar ISO ülke/bölge kodları içeriyorsa biçim bileşenine yalnızca biçim bileşeninin ISO ülke/bölge kodlarının biri için tanımlanan birincil adrese sahip şirketlerinden ulaşılabilir.

Bir veri biçimi bileşeninin farklı sürümleri ISO ülke/bölge kodları için farklı ayarlara sahip olabilir.

#### <a name="configuration"></a><a name="Configuration"></a>Yapılandırma

Bir ER yapılandırması, belirli bir ER bileşeninin sarmalayıcısıdır. Bu bileşen bir veri modeli bileşeni ya da biçim bileşeni olabilir. Bir konfigürasyon bir ER bileşeninin farklı sürümlerini içerebilir. Her yapılandırma belirli bir yapılandırma sağlayıcı tarafından sahip olunan olarak işaretlenir. Bir yapılandırma bileşeninin **Taslak** sürümü, yapılandırma sahibi uygulamadaki ER ayarlarında etkin sağlayıcı olarak seçilmişse düzenlenebilir.

Her bir model konfigürasyonu veri modeli bileşenini içerir. Yeni bir biçim konfigürasyonu belirli bir veri modeli konfigürasyonundan kaynaklanarak oluşturulabilir (türetilebilir). Yapılandırma ağacında, oluşturulan biçim yapılandırması, orijinal veri modeli yapılandırmasının alt öğesi olarak belirir.

Oluşturulan biçim konfigürasyonu bir biçim bileşeni içerir. Orijinal model konfigürasyonunun veri modeli bileşeni varsayılan veri kaynağı olarak alt biçim konfigürasyonunun biçim bileşenine otomatik olarak eklenir.

ER yapılandırması uygulama şirketleri için paylaşılır.

#### <a name="provider"></a><a name="Provider"></a>Sağlayıcı

ER sağlayıcısı her bir ER konfigürasyonunun yazarını (sahibini) göstermek için kullanılan taraf tanımlayıcısıdır. ER, konfigürasyon sağlayıcıları listesini yönetmenizi sağlar. Elektronik belgeler için Finance and Operations çözümünün parçası olarak sevk edilen biçim konfigürasyonlarının sahibi olarak **Microsoft** konfigürasyon sağlayıcısı işaretlenir.

Yeni bir ER sağlayıcısını kaydetmeyi öğrenmek için **ER Bir yapılandırma sağlayıcısı oluşturmak ve bunu etkin olarak işaretlemek** (**7.5.4.3 Al/BT hizmeti geliştir/çözüm bileşenleri (10677)** iş işleminin parçası olan) görev kılavuzunu yürütün.

#### <a name="repository"></a><a name="Repository"></a>Depo

ER havuzu ER konfigürasyonlarını depolar. Aşağıdaki ER havuzu türleri şu anda desteklenir: 

- LCS paylaşımlı kitaplık
- LCS projesi
- Dosya sistemi
- RCS
- Operations kaynakları
- Genel depo

Bir **LCS paylaşımlı kitaplık** deposu Lifecycle Services (LCS) içindeki Paylaşılan varlık kitaplığındaki yapılandırmaların listesine erişim sağlar. Bu türde bir ER deposu, yalnızca Microsoft sağlayıcısı için kaydedilebilir. LCS Paylaşılan varlık kitaplığından ER yapılandırmalarının en güncel sürümlerini mevcut kuruluma aktarabilirsiniz.

**LCS projesi** havuzu, havuz kaydedildiğinde seçilen belirli bir LCS projesinin (LCS proje varlıkları kitaplığı) konfigürasyonlar listesine erişim sağlar. ER, belirli bir **LCS projesi** havuzu için geçerli kurulumdan paylaşılan konfigürasyonları karşıya yüklemenizi sağlar. Konfigürasyonları bir **LCS projesi** deposundan geçerli Finance and Operations uygulamalarınıza kurulumuna da aktarabilirsiniz.

Bir **Dosya sistemi** havuzu, AOS servisinin barındırıldığı makinede xml dosyaları olarak yerel dosya sisteminin belirli bir klasöründe bulunan yapılandırmalar listesine erişim sağlar. Gerekli klasör, havuz kayıt aşamasında seçilir. Yapılandırmaları bir **Dosya sistemi** deposundan geçerli kuruluma da aktarabilirsiniz. 

Bu havuz türünün aşağıdaki ortamlarda erişilebilir olduğunu unutmayın:

- Geliştirme amaçlarıyla dağıtılmış bulutta barındırılan ortamlar (iliştirilmiş paketlerin test modellerini içeren)
- Yerel depolanan ortamlar (şirket içi)

Daha fazla bilgi için bkz: [Elektronik raporlama (ER) yapılandırmalarını içe aktarma](./electronic-reporting-import-ger-configurations.md).

**RCS** örneği havuzu, havuz kayıt aşamasında seçilen [Yapılandırma servisi (RCS)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) belirli bir örneği konfigürasyonlar listesine erişim sağlar. ER, tamamlanmış veya paylaşılan yapılandırmaları seçilen RCS örneğinden geçerli örneğe aktarmanızı ve böylece elektronik raporlama için kullanmanızı sağlar.

Daha fazla bilgi için bkz: [RCS'den Elektronik raporlama (ER) yapılandırmalarını içe aktarma](./rcs-download-configurations.md).

**Genel bir depo** deposu, [yapılandırma hizmetindeki](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) genel depo içindeki yapılandırmalar listesine erişim sağlar . Bu türde bir ER deposu, yalnızca Microsoft sağlayıcısı için kaydedilebilir. Global depodan ER yapılandırmalarının en güncel sürümlerini mevcut kuruluma aktarabilirsiniz.

Daha fazla bilgi için bkz. [Yapılandırma Hizmeti Global deposundan Elektronik raporlama (ER) yapılandırmalarını içe aktarma](./er-download-configurations-global-repo.md).

**Operations kaynakları** havuzu Microsoft'un bir ER konfigürasyonu sağlayıcısı olarak ilk başta uygulama çözümünün parçası olarak yayımladığı konfigürasyonlar listesine erişim sağlar. Bu yapılandırmalar geçerli kuruluma aktarılabilir ve elektronik raporlama veya basit görev kılavuzları için kullanılabilir. Bunlar ek yerelleştirmeler ve özelleştirmeler için de kullanılabilir. Microsoft ER yapılandırmaları tarafından sağlanan en güncel sürümlerin LCS Paylaşımlı varlık kitaplığından, karşılık gelen ER deposu kullanılarak içe aktarılması gerekir.

Gerekli **LCS projesi**, **Dosya sistemi** ve **Düzenleyici Yapılandırma Servisleri (RCS)** depoları her bir geçerli kurulumun yapılandırma sağlayıcısı için ayrı ayrı kaydedilebilir. Her depo belirli bir konfigürasyon sağlayıcısına ayrılabilir.

## <a name="supported-scenarios"></a>Desteklenen senaryolar

### <a name="building-a-data-model"></a>Bir veri modeli oluşturma

ER, belirli bir iş etki alanı için bir veri modeli oluşturmak amacıyla kullanabileceğiniz bir model tasarımcısı sağlar. Tüm etki alanına özgü iş varlıkları ve aralarındaki ilişkiler hiyerarşik olarak yapılandırılmış bir veri modelinde sunulabilir. 

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Tasarım etki alanına özgü veri modeli** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş süreci) oynatın.

### <a name="translating-data-model-content"></a>Veri modeli içeriği çevirme

Veri modeli içeriği (etiketler ve tanımlar) uygulamaların desteklediği diğer dillere çevrilebilir. Aşağıdaki nedenlerden dolayı veri modeli içeriğini çevirmek isteyebilirsiniz:

- Veri modelini biçim bileşenlerinin eşlemesi için kullanacak yabancı dilleri konuşan biçim tasarımcıları için tasarım zamanında daha anlaşılır yapmak için.
- O anda oturum açmış kullanıcı tarafından tercih edilen dildeki yapılandırılmış doğrulama iletilerinin (hatalar ve uyarılar) yanı sıra çalıştırma zamanı parametreleri için komutları ve yardımları sunan daha kullanıcı dostu içerik oluşturmak için.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Giden belgeler için veri modeli eşlemeleri yapılandırmak

ER, kullanıcılara belirli uygulama veri kaynakları için tasarlanan veri modellerini eşleme imkanı veren bir model eşleme tasarımcısı sağlar. Veri, eşleşmeye bağlı olarak çalışma zamanında seçilen veri kaynaklarından modele alınacaktır. Veri modeli daha sonra giden elektronik belgeler oluşturan ER biçimlerinin soyut bir veri kaynağı kullanılır. 

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER model eşleme tanımla ve veri kaynakları seç** ve **ER seçili veri kaynaklarına veri modeli eşle** görev kılavuzlarını ( **7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Gelen belgeler için veri modeli eşlemeleri yapılandırmak

ER, kullanıcılara belirli hedefler için tasarlanan veri modellerini eşleme imkanı veren bir model eşleme tasarımcısı sağlar. Örneğin, veri modelleri güncelleştirilebilir veri bileşenlerine (tablolalar, veri varlıkları ve görünümler) eşlenebilir. Eşlemeye bağlı olarak, veriler çalışma zamanında, veri modelinden veriyi kullanarak güncelleştirilir. ER biçiminin soyut depolaması olarak veri modeli, gelen bir elektronik belgeden içe aktarılan verilerle doldurulur. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Tasarlanmış model bileşenini model konfigürasyonu olarak depolama

ER, geçerli örneğin model konfigürasyonu olarak ilgili veri eşleşmeleriyle birlikte tasarlanmış veri modelini saklayabilir. Aşağıdaki çizim, bu tür bir veri modeli konfigürasyonu örneğini (ödeme etki alanı model konfigürasyonu) gösterir.

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER seçili veri kaynaklarına veri modeli eşle** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Temel olarak bir veri modelini kullanan bir biçim oluşturma

ER, model bileşenini temel olarak seçerek seçili bir iş etki alanı için bir elektronik belge biçimini oluşturmak için kullanabileceğiniz bir biçim tasarımcısını destekler. Aynı ER biçimi tasarımcısı, veri kaynağı olarak seçili etki alanı veri modeli eşlemesi için oluşturduğunuz bir biçimde eşleme yapmanızı sağlar. 

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Tasarım etki alanına özgü biçim** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>OPENXML çalışma sayfası biçiminde elektronik belgeler oluşturmak için bir konfigürasyon oluşturma

ER biçim tasarımcısı, bir elektronik belgeyi OPENXML çalışma sayfası biçiminde oluşturmak için kullanılabilir. 

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **Raporlar için OPENXML biçiminde bir konfigürasyon oluştur** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın. Bir şablonun içe aktarılamsı görev kılavuzunun bir parçası olarak, [Ödeme Raporu Şablonu (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202) Excel dosyasını şablon olarak kullanın.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Bir Word belgesi biçiminde elektronik belgeler oluşturmak için bir konfigürasyon oluşturma

ER biçim tasarımcısı, bir elektronik belgeyi bir Word belgesi biçiminde oluşturmak için kullanılabilir. Aşağıdaki çizim, bu tür bir biçimin örneğini gösterir. Bu biçimin, rapor çıktısını OPENXML biçiminde oluşturmak için özgün olarak tasarlanmış olan mevcut ER yapılandırmasını yeniden kullandığını unutmayın.

Bu senaryonun ayrıntıları hakkında bilgi edinmek için ER Microsoft WORD biçiminde raporlar oluşturmak için bir yapılandırma tasarlama görev kılavuzunu (7.5.4.3 Al/BT hizmeti geliştir/çözüm bileşenleri (10677) iş işleminin parçası olarak) oynatın. Bir şablonu içe aktarmak için görev kılavuzu adımının bir parçası olarak, aşağıdaki Word dosyalarını ER biçimi için bir şablon olarak kullanın:

- [Ödeme Raporu Şablonu (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Ödeme Raporunun bağlı şablonu (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Gelen elektronik belgelerden veri aktarmak için bir yapılandırma oluşturmak

ER biçim tasarımcısı, XML ya da metin biçiminde veri içe aktarma için planlanan bir elektronik belgeyi tanımlamak için kullanılabilir. Tasarlanan biçim, gelen bir belgeyi ayrıştırmak için kullanılır. ER biçimi eşleme tasarımcısı, tasarlanan biçimin öğelerinin veri modeline bağlamasını tanımlamak için kullanılabilir. 

Bu senaryonun ayrıntıları hakkında bilgi edinmek için Harici bir dosyadan veri içe aktarmak için gerekli ER yapılandırmalarını oluşturma görev kılavuzunu (7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677) iş sürecinin parçası) oynatın. Bu kılavuzu oynatmak için aşağıdaki dosyaları kullanın:

- [ER veri modeli konfigürasyonu (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [ER biçim yapılandırma (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Gelen belgenin XML biçimnde örneği (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Gelen belgenin verisini yönetmek için çalışma sayfası örneği (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Biçim konfigürasyonunda tasarlanmış bir biçim bileşeni depolama

ER, geçerli kurulumun biçim konfigürasyonu olarak yapılandırılmış veri eşlemeleriyle birlikte tasarlanmış bir biçimi depolayabilir. Bu tür bir konfigürasyon biçimi örneği önceki çizimde gösterilmektedir (**BACS (UK)**, **Ödeme modeli** konfigürasyonunun alt öğesi). Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Tasarım etki alanına özgü biçim** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Oluşturulan biçimi dahili olarak kullanmaya başlamak için Finance'ı yapılandırma

Uygulama elektronik raporları oluşturmak için oluşturulan biçimi kullanmaya başlamak için yapılandırılabilir. Oluşturulmuş biçim konfigürasyonu başvurusu belirli bir etki alanı ayarları içinde tanımlanmalıdır. Örneğin, elektronik satıcı ödemeleri için BACS biçiminde ER biçim konfigürasyonu kullanmaya başlamak için biçim yapılandırması belirli ödeme yöntemlerinde referans olarak verilmelidir:

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Ödemeler için elektronik belge oluşturmak için biçim kullan** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

## <a name="handling-er-components"></a>ER bileşenlerini işleme

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER bileşenini harici olarak teklif etmek için LCS'de bir ER bileşeni yayınlama (yerelleştirme)

Oluşturulan bileşen sahibi (model veya biçim) LCS için bileşenin tamamlanmış sürümünü yayımlamak amacıyla ER kullanabilir. Geçerli ER konfigürasyon sağlayıcısı için **LCS projesi** türü depo gereklidir. Tamamlanmış bir bileşen sürümünün durumu **TAMAMLANDI**'dan **PAYLAŞILAN** olarak değiştirildiğinde, bu sürüm LCS'de yayımlanır. Bir bileşen LCS'de yayınlandığında bu bileşenin sahibi bu bileşeni desteklemek için hizmet sağlayıcısı olur. Örneğin, biçim bileşeni yasal olarak gerekli elektronik bir belge (örneğin, yerelleştirme senaryosuna uygun) oluşturmak için tasarlanmışsa, bu biçimin yasal değişikliklerle uyumlu tutulduğu ve yeni yasal gereksinimler ortaya çıktığında sağlayıcının bileşenin yeni sürümlerini çıkaracağı varsayılır. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Lifecycle Services'a bir yapılandırma yükleme** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER bileşenini dahili olarak kullanmak üzere LCS'den içe aktarma

ER, ER bileşenlerini LCS'den geçerli kuruluma aktarmanızı sağlar. **LCS projesi** türü bir depo gereklidir. ER bileşeni LCS'den geçerli kuruluma aktarıldığında kurulumun sahibi aktarılan bileşenin sahibi (yazar) tarafından sağlanan hizmet tüketicisi olur. Örneğin, ülkeye/bölgeye özel bir biçimde uygulamadan belirli bir elektronik belge oluşturmak için bir biçim bileşeni tasarlanmışsa (yerelleştirme senaryosu) hizmet tüketicisinin yasal gerekliliklerle uyum sağlamak için bu biçimin her türlü güncelleştirmesini yapabileceği varsayılır. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Lifecycle Services'tan bir yapılandırmayı içe aktarma** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın.

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Temel olarak başka bir biçim seçerek bir biçim oluşturma (özelleştirme)

ER, LCS'den aktarıla bir bileşenin güncel sürümünden (temel) yeni bir bileşen oluşturmanızı (türetmenizi) sağlar. Örneğin, bir kullanıcı özelleştirme senaryosunu desteklemek için bir elektronik belge için bazı özel gereklilikleri uygulamak amacıyla (örneğin ek alan veya kapsamlı bir tanım) yenir bir biçim türetmek ister. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Yeni temel sürüm benimsenerek biçimi yükselt** görev kılavuzunu (**7.5.4.3 Al/BT servisi geliştir/çözüm bileşenleri (10677)** iş işlemi parçası) oynatın.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Temel biçimin yeni sürümünü seçerek bir biçim yükseltme (rebase)

ER, türetilen bileşenin geçerli taslak sürümünde temel bileşenin en son sürümünün değişikliklerini otomatik olarak benimsemenizi sağlar. Bu işlem *yeniden temelleme* olarak bilinmektedir. Örneğin, LCS'den aktarılan biçimin en son sürümünde kullanılan yeni yasal değişiklik elektronik belgenin bu biçiminin özelleştirilmiş sürümüyle otomatik olarak birleştirilebilir. Otomatik olarak birleştirilemeyen her değişiklik bir çakışma olarak kabul edilir. Bu çakışmalar uygun bileşen için tasarımcı aracında elle çözüm için sunulur. Bu senaryonun ayrıntıları hakkında bilgi edinmek için **ER Bu biçimin yeni temel sürüm benimsenerek biçimi yükselt** görev kılavuzunu (**7.5.5.3 Al/Değiştirilmiş BT servisi geliştir/çözüm bileşeni (10683)** iş işlemi parçası) oynatın.

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>Finance'te yayınlanmış olan ER yapılandırmalarının listesi

Finance için ER yapılandırmalarının listesi sürekli olarak güncelleştirilmektedir. Şu anda desteklenen ER yapılandırmalarının listesini incelemek için [Genel depo](er-download-configurations-global-repo.md)'yu açın. **Kullanımdan kaldırma ayrıntıları** hızlı sekmesinde, kullanımdan kaldırılmış olan veya artık bakım sağlanmayan yapılandırmalar hakkındaki bilgileri inceleyebilirsiniz. 

![Yapılandırma deposu sayfasında Genel depo içerikleri](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlama (ER) yapılandırmaları oluşturma](electronic-reporting-configuration.md)
- [Elektronik raporlama (ER) yapılandırması yaşam döngüsünü yönetme](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]