---
title: Elektronik raporlamaya (ER) genel bakış
description: Bu makalede, Elektronik raporlama (ER) aracına dair genel bir bakış sağlanmaktadır. Anahtar kavramlar, desteklenen senaryolar ve çözümün parçası olan biçimler açıklanmaktadır.
author: NickSelin
ms.date: 11/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "58941"
- intro-internal
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f3853e0c1da0a5abb3f92171370cc4aeabbd829
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109595"
---
# <a name="electronic-reporting-er-overview"></a>Elektronik raporlamaya (ER) genel bakış

[!include [banner](../includes/banner.md)]

Bu makalede, Elektronik raporlama (ER) aracına dair genel bakış sağlanmaktadır. Temel kavramlar, ER'nin desteklediği senaryolar ve çözümün bir parçası olarak tasarlanan ve yayınlanan biçimlerin listesini içermektedir.

ER, düzenleyici elektronik raporlama ve ödemeler oluşturmanıza ve sürdürmenize yardımcı olan yapılandırılabilir bir araçtır. Aşağıdaki üç konsepte dayanmaktadır:

- Kodlama yerine yapılandırma:

    - Yapılandırma, bir işletme kullanıcısı tarafından yapılabilir ve geliştirici gerektirmez.
    - Veri modeli işletme terimleriyle tanımlanır.
    - Görsel düzenleyiciler, ER yapılandırmasının tüm bileşenlerini oluşturmak için kullanılır.
    - Veri dönüştürme için kullanılan dil Microsoft Excel‘de kullanılan dile benzerdir.

- Birden çok Dynamics 365 Finance sürümü için tek bir yapılandırma:

    - İşletme terimleriyle tanımlanan etki alanına özgü bir veri modelini yönetin.
    - Sürüme bağımlı veri modeli eşlemelerinde uygulama sürümü ayrıntılarını ayırın.
    - Veri modeline bağlı olarak, geçerli sürümün birden çok sürümü için bir biçim yapılandırmasını koruyun.

- Kolay veya otomatik yükseltme:

    - ER yapılandırmalarının sürümünü oluşturma işlemi desteklenir.
    - Microsoft Dynamics Lifecycle Services (LCS) Varlıklar kitaplığı, sürüm değişimi amacıyla, ER yapılandırmaları için bir depo olarak kullanılabilir.
    - Özgün ER yapılandırmalarını temel alan yerelleştirmeler alt sürümler olarak tanıtılabilir.
    - ER yapılandırma ağacı, sürümler için bağımlılıkları kontrol etmeye yardımcı olan bir araç olarak sağlanır.
    - Yerelleştirmedeki farklılıklar veya delta yapılandırma kaydedilerek özgün ER yapılandırmasının yeni bir sürümüne otomatik yükseltmeyi etkinleştirir.
    - Yerelleştirme sürümlerinin otomatik olarak yükseltilmesi sırasında keşfedilen çakışmalar el ile kolayca çözülebilir.

ER, elektronik biçim yapıları tanımlamanıza ve ardından veriler ve algoritmalar kullanarak yapıların nasıl doldurulması gerektiğini açıklamanıza olanak tanır. Veri dönüştürme için Excel diline benzeyen bir formül dili kullanabilirsiniz. Veritabanından biçime eşlemeyi daha yönetilebilir, yeniden kullanılabilir ve biçim değişikliklerinden bağımsız hale getirmek için bir ara veri modeli konsepti kullanıma sunulmuştur. Bu konsept, uygulama ayrıntılarının biçim eşlemesinden gizlenmesini ve tek bir veri modelinin birden çok biçim eşlemesi için yeniden kullanılmasını sağlar.

ER'yi, çeşitli ülke ve bölgelerin yasal gereksinimlerine uygun olarak hem gelen hem de giden elektronik belgelerin biçimlerini yapılandırmak için kullanabilirsiniz. ER, yaşam döngüleri boyunca bu biçimleri yönetmenizi sağlar. Örneğin, yeni mevzuat gerekliliklerini uygulayabilir ve devlet kurumları, bankalar ve diğer taraflarla elektronik olarak belge alışverişi yapmak için gerekli biçimde işletme belgeleri oluşturursunuz.

ER altyapısı geliştiricilerden ziyade iş kullanıcılarını hedefler. Çünkü kod yerine biçimleri yapılandırırsınız, elektronik belgeler için biçimler oluşturmak ve ayarlamak için süreçler daha hızlı ve kolaydır.

ER şu anda TEXT, XML, JSON, PDF, Microsoft Word, Microsoft Excel, and OPENXML çalışma sayfası biçimlerini destekler.

## <a name="capabilities"></a>Beceriler

ER altyapısı aşağıdaki yeteneklere sahiptir:

- Farklı etki alanlarında elektronik raporlama için tek bir paylaşımlı aracı temsil eder ve finans ve operasyon için bir tür elektronik raporlama yapan 20'den fazla farklı altyapının yerini alır.
- Rapor biçiminin şu anki uygulamadan yalıtılmasını sağlar. Diğer bir deyişle, biçim farklı sürümler için geçerlidir.
- Özgün biçime dayalı özel bir biçim oluşturulmasını destekler. Yerelleştirme/özelleştirme gereklilikleri yüzünden özgün biçim değişmiş olduğundan özelleştirilmiş biçimi otomatik olarak yükseltme yeteneğini de içerir.
- Microsoft ve Microsoft ortakları için elektronik raporlamada yerelleştirme gerekliliklerini desteklemek amacıyla birincil standart araç haline dönüşür.
- Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla biçimleri iş ortakları ve müşterilere dağıtma yeteneğini destekler.

## <a name="key-concepts"></a>Kilit kavramlar

### <a name="main-data-flow"></a>Ana veri akışı

[![ER ana veri akışı.](./media/ger-main-data-flow.jpg)](./media/ger-main-data-flow.jpg)

### <a name="components"></a>Bileşenler

ER, aşağıdaki bileşen türlerini destekler:

- Veri modeli
- Model eşleme
- Biçim
- Meta veriler

Daha fazla bilgi için bkz: [Elektronik raporlama bileşenleri](er-overview-components.md).


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

ER sağlayıcısı her bir ER konfigürasyonunun yazarını (sahibini) göstermek için kullanılan taraf tanımlayıcısıdır. ER, konfigürasyon sağlayıcıları listesini yönetmenizi sağlar. Elektronik belgeler için finans ve operasyon çözümünün parçası olarak sevk edilen biçim konfigürasyonlarının sahibi olarak **Microsoft** yapılandırma sağlayıcısı işaretlenir.

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

**LCS projesi** havuzu, havuz kaydedildiğinde seçilen belirli bir LCS projesinin (LCS proje varlıkları kitaplığı) konfigürasyonlar listesine erişim sağlar. ER, belirli bir **LCS projesi** havuzu için geçerli kurulumdan paylaşılan konfigürasyonları karşıya yüklemenizi sağlar. Yapılandırmaları bir **LCS projesi** deposundan geçerli finans ve operasyon uygulamalarının kurulumuna da aktarabilirsiniz.

Bir **Dosya sistemi** havuzu, AOS servisinin barındırıldığı makinede xml dosyaları olarak yerel dosya sisteminin belirli bir klasöründe bulunan yapılandırmalar listesine erişim sağlar. Gerekli klasör, havuz kayıt aşamasında seçilir. Yapılandırmaları bir **Dosya sistemi** deposundan geçerli kuruluma da aktarabilirsiniz. 

Bu havuz türünün aşağıdaki ortamlarda erişilebilir olduğunu unutmayın:

- Geliştirme amaçlarıyla dağıtılmış bulutta barındırılan ortamlar (iliştirilmiş paketlerin test modellerini içeren)
- Yerel depolanan ortamlar (şirket içi)

Daha fazla bilgi için bkz: [Elektronik raporlama (ER) yapılandırmalarını içe aktarma](./electronic-reporting-import-ger-configurations.md).

**RCS** örneği havuzu, havuz kayıt aşamasında seçilen [Yapılandırma servisi (RCS)](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) belirli bir örneği konfigürasyonlar listesine erişim sağlar. ER, tamamlanmış veya paylaşılan yapılandırmaları seçilen RCS örneğinden geçerli örneğe aktarmanızı ve böylece elektronik raporlama için kullanmanızı sağlar.

Daha fazla bilgi için bkz: [RCS'den Elektronik raporlama (ER) yapılandırmalarını içe aktarma](./rcs-download-configurations.md).

**Genel bir depo** deposu, [yapılandırma hizmetindeki](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) genel depo içindeki yapılandırmalar listesine erişim sağlar . Bu türde bir ER deposu, yalnızca Microsoft sağlayıcısı için kaydedilebilir. Global depodan ER yapılandırmalarının en güncel sürümlerini mevcut kuruluma aktarabilirsiniz.

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

Bu senaryonun ayrıntıları hakkında bilgi edinmek için **Raporlar için OPENXML biçiminde bir konfigürasyon oluştur** görev kılavuzunu (**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası) oynatın. Bir şablonun içe aktarılamsı görev kılavuzunun bir parçası olarak, [Ödeme Raporu Şablonu (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx) Excel dosyasını şablon olarak kullanın.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Bir Word belgesi biçiminde elektronik belgeler oluşturmak için bir konfigürasyon oluşturma

ER biçim tasarımcısı, bir elektronik belgeyi bir Word belgesi biçiminde oluşturmak için kullanılabilir. Aşağıdaki çizim, bu tür bir biçimin örneğini gösterir. Bu biçimin, rapor çıktısını OPENXML biçiminde oluşturmak için özgün olarak tasarlanmış olan mevcut ER yapılandırmasını yeniden kullandığını unutmayın.

Bu senaryonun ayrıntıları hakkında bilgi edinmek için ER Microsoft WORD biçiminde raporlar oluşturmak için bir yapılandırma tasarlama görev kılavuzunu (7.5.4.3 Al/BT hizmeti geliştir/çözüm bileşenleri (10677) iş işleminin parçası olarak) oynatın. Bir şablonu içe aktarmak için görev kılavuzu adımının bir parçası olarak, aşağıdaki Word dosyalarını ER biçimi için bir şablon olarak kullanın:

- [Ödeme Raporu Şablonu (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Ödeme Raporunun bağlı şablonu (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Gelen elektronik belgelerden veri aktarmak için bir yapılandırma oluşturmak

ER biçim tasarımcısı, XML ya da metin biçiminde veri içe aktarma için planlanan bir elektronik belgeyi tanımlamak için kullanılabilir. Tasarlanan biçim, gelen bir belgeyi ayrıştırmak için kullanılır. ER biçimi eşleme tasarımcısı, tasarlanan biçimin öğelerinin veri modeline bağlamasını tanımlamak için kullanılabilir. 

Bu senaryonun ayrıntıları hakkında bilgi edinmek için Harici bir dosyadan veri içe aktarmak için gerekli ER yapılandırmalarını oluşturma görev kılavuzunu (7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677) iş sürecinin parçası) oynatın. Bu kılavuzu oynatmak için aşağıdaki dosyaları kullanın:

- [ER veri modeli konfigürasyonu (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [ER biçim yapılandırma (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [Gelen belgenin XML biçimnde örneği (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [Gelen belgenin verisini yönetmek için çalışma sayfası örneği (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

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

![Yapılandırma deposu sayfasında Genel depo içerikleri.](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlama (ER) yapılandırmaları oluşturma](electronic-reporting-configuration.md)
- [Elektronik raporlama (ER) yapılandırması yaşam döngüsünü yönetme](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

