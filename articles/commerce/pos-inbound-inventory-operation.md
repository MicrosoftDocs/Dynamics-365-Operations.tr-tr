---
title: POS'ta gelen stok işlemi
description: Bu konu satış noktası (POS) gelen stok operasyonunun yeteneklerini açıklar.
author: hhaines
manager: annbe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0f519ac3b5dd854d0c31b67382f46d0ab116ec7e
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071904"
---
# <a name="inbound-inventory-operation-in-pos"></a>POS'ta gelen stok işlemi

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Microsoft Dynamics 365 Commerce sürüm 10.0.10 ve sonraki sürümlerinde satış noktasındaki gelen ve giden operasyonlar (POS) malzeme çekme ve teslim alma operasyonunu değiştirir.

> [!NOTE]
> Sürüm 10.0.10 ve sonraki sürümlerde, satın alma siparişlerine ve transfer emirlerine karşı mağaza stoku alma ile ilgili olan POS uygulamasındaki tüm yeni özellikler **gelen operasyonlar** POS operasyonuna eklenir. Şu anda POS'ta malzeme çekme ve teslim alma operasyonunu kullanıyorsanız, bu operasyondan yeni gelen ve giden operasyonlarına geçmek için bir strateji geliştirmeniz önerilir. Malzeme çekme ve alma işlemi üründen kaldırılmayabilse de bir işlevsel veya performans açısından 10.0.9 sürümünden sonra başka yatırımlar olmayacak.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Ön koşul: Zaman uyumsuz belge çerçevesini konfigüre edin

Gelen operasyon, birçok mağaza veya şirket boyunca yüksek hacimde deftere nakil işlemi yapan kullanıcıların ve büyük stok belgelerinin bu belgeleri zaman aşımı veya hata yaşamdan Commerce Headquarters'a aktarmalarını sağlamak için performans iyileştirmeleri içerir. Bu geliştirmeler zaman uyumsuz bir belge çerçevesinin kullanımını gerektirir.

Zaman uyumsuz bir belge çerçevesi kullanıldığında, POS'tan Commerce Headquarters'a gelen belge değişikliklerini uygulayabilir ve daha sonra Commerce Headquarters'a işlem arka planda gerçekleşirken diğer görevlere taşıyabilirsiniz. Deftere Nakletme işleminin başarılı olduğundan emin olmak için, POS'daki **Gelen operasyon** belge listesi sayfasından belgenin durumunu denetleyebilirsiniz. POS uygulamasında, Commerce Headquarters'a nakledilebilecek tüm belgeleri görmek için gelen operasyon etkin belge listesini de kullanabilirsiniz. Belge başarısız olursa POS kullanıcıları bu belgede düzeltmeler yapabilir ve bunu Commerce Headquarters'da işlemeyi yeniden deneyebilir.

> [!IMPORTANT]
> Bir şirket POS'ta gelen operasyonu kullanmaya çalışmadan önce zaman uyumsuz belge çerçevesi konfigüre edilmelidir.

Zaman uyumsuz bir belge çerçevesini konfigüre etmek için aşağıdaki yordamları tamamlayın.

### <a name="create-and-configure-a-number-sequence"></a>Numara serileri oluşturma ve yapılandırma

1. **Kuruluş yönetim \> Numara serileri \> Numara serileri**'ne tıklayın.
2. **Numara serileri** sayfasında, bir numara serisi oluşturun.
3. **Numara serisi kodu** ve **ad** alanlarında kullanıcı tanımlı değerler girin.
4. **Referanslar** hızlı sekmesinde **Ekle**'yi seçin.
5. **Alan** alanında **Commerce parametreleri** seçin.
4. **Referans** alanında, **perakende belge işlemi tanımlayıcısı**'nı seçin.
5. **Genel** hızlı sekmesinde, **kurulum** bölümünde performans sorunu olmadığından emin olmak için **devamlı** seçeneğini **Hayır** olarak ayarlayın.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Belge işleme ve izleme görevleri için iki toplu iş oluşturun ve zamanlayın

Oluşturduğunuz toplu işler, başarısız olan veya zaman aşımına uğrayabilen belgeleri işlemek için kullanılır. Bunlar ayrıca, POS'tan işlenmekte olan etkin stok belgelerinin sayısı sistem tarafından yapılandırılmış bir değeri aştığında da kullanılır.

1. **Sistem Yönetimi \> Sorgular \> Toplu işler**'e gidin.
2. **Toplu iş** sayfasında, iki toplu iş oluşturun:

    - **RetailDocumentOperationMonitorBatch** sınıfını çalıştırmak üzere bir iş konfigüre edin.
    - **RetailDocumentOperationProcessingBatch** sınıfını çalıştırmak üzere bir iş konfigüre edin.

2. Yeni toplu işleri yinelenen bir temelde çalışacak şekilde zamanlayın. Örneğin, iş çizelgesini her beş dakikada bir çalışacak şekilde ayarlayın.

## <a name="prerequisite-add-inbound-operation-to-the-pos-screen-layout"></a>Önkoşul: POS ekran düzenine gelen işlem Ekle

Kuruluşunuzun gelen operasyon işlevini kullanabilmesi için önce bir veya daha fazla [POS ekran mizanpajlarından](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) **gelen operasyon** POS operasyonunu konfigüre etmelidir. Yeni operasyonu üretim ortamında dağıtmadan önce, bunu kapsamlı olarak test edin ve kullanıcılarınıza bunu kullanmaya eğittiğinizden emin olun.

## <a name="overview"></a>Genel Bakış

Gelen operasyonu POS kullanıcıları aşağıdaki görevleri yerine getirelim:

- Teyit edilen satınalma siparişi belgelerinden veya sevk transfer emri belgelerinden mağaza stoğunu teslim alın.
- Belge tam olarak alındıktan sonra yedi günlük bir dönem için geçmişe ait geçmiş stok girişleri hakkındaki bilgileri görüntüleyin.
- Yeni gelen transfer emri talepleri oluşturun.

POS uygulamasından gelen operasyon başladığında, bir liste sayfası görünümü görüntülenir. Bu görünüm, kullanıcının geçerli mağazanın alacağı planlanan stok satırlarına sahip açık satın alma emri ve transfer emri belgelerini gösterir. Belirli bir belge bulmak ve seçmek için, kullanıcılar listeyi kaydırabilecek veya arama özelliğini kullanabilir.

Gelen stok belgesi listesinde üç sekme vardır:

- **Etkin** – Bu sekme, tam veya kısmen açık olan ve henüz teslim alınması gereken satırlarda satır veya miktar içeren belgeleri gösterir.
- **Taslak** – Bu sekmede kullanıcının mağazanın oluşturulduğu yeni gelen transfer emri talepleri gösterilir. Ancak, belgeler yalnızca yerel olarak kaydedildi. Bunlar henüz işlenmek üzere Commerce Headquarters'a gönderilmemiş.
- **Tamam** – Bu sekmede, mağazanın son yedi gün içinde tam olarak aldığı satın alma emri veya transfer emri belgelerinin listesi gösterilir. Bu sekme yalnızca bilgi amaçlıdır. Belgelerle ilgili tüm bilgiler, mağazanın salt okunur verileri olduğunu öğrenin.

Sekmelerin herhangi birinde belge görüntülediğinizde, **durum** alanı belgenin bulunduğu aşamayı anlamanıza yardımcı olabilir.

- **Taslak** – Transfer emri belgesi yalnızca mağazanın kanal veritabanına kaydedildi. Transfer emri talebiyle ilgili hiçbir bilgi henüz Commerce Headquarters'a gönderilmedi.
- **Talep edilen** – Satın alma siparişi veya transfer emri Commerce Headquarters'da oluşturulmuş ve tamamen açık. Belgede henüz bir makbuz işlenmemiştir. Satınalma siparişi belge türündeki belgeler için, alma işlemi durum **istendi** olduğu zaman herhangi bir zamanda başlayabilir.
- **Kısmen sevk edildi** – Transfer emri belgesi, çıkış ambarı tarafından sevk edilmiş olarak deftere nakledilen bir veya daha fazla satır veya kısmi satır miktarları içerebilir. Sevk edilen bu satırlar gelen operasyonunu içe aktarmak için kullanılabilir.
- **Tam sevk edildi** - Transfer emrinin, çıkış ambarı tarafından sevk edilmiş olarak deftere nakledilen tüm satırları ve tam satır miktarları vardı. Tüm belge gelen operasyonunu içe aktarmak için kullanılabilir.
- **Kısmen alındı** – Satın alma siparişi veya transfer emri belgesindeki satırların veya satır miktarlarının bir kısmı mağaza tarafından teslim alındı, ancak bazı satırlar açık durumda kalır.
- **Tam alınan** – Satın alma siparişi veya transfer emri belgesindeki tüm satırlar ve miktarlar tam olarak teslim alındı. Belgelere yalnızca **Tamamlandı** sekmesinde erişilebilir ve mağaza kullanıcıları tarafından salt okunurdur.
- **Devam edenler** – Bu durum, aygıt kullanıcılarına belgenin başka bir kullanıcı tarafından etkin olarak çalıştığını bildirmek için kullanılır.
- **Duraklatıldı** – Alma işlemini geçici olarak durdurmak için **duraklatma alma** işlemi seçildikten sonra bu durum gösterilir.
- **HQ'da işleme** – Belge POS uygulamasından Commerce Headquarters'a gönderilmiştir, ancak henüz Commerce Headquarters 'a nakledilmemiştir. Belge, zaman uyumsuz belge deftere nakil işlemine geçiyor. Belge, Commerce Headquarters 'a başarıyla nakledildikten sonra, durumu **tam olarak alındı** veya **kısmen alındı** olarak güncelleştirilmelidir.
- **İşlem başarısız oldu** – Belge, Commerce Headquarters'a nakledildi ve reddedildi. **Ayrıntılar** bölmesi deftere nakil hatasının nedenini gösterir. Veri sorunlarını düzeltmek için belgenin düzenlenmesi ve daha sonra işlenmek üzere Commerce Headquarters'a yeniden gönderilmesi gerekir.

Listeden bir belge satırı seçtiğinizde **Ayrıntılar** bölmesi görüntülenir. Bu bölme, belge hakkında Sevkiyat ve tarih bilgileri gibi ek bilgiler gösterir. İlerleme çubuğu, kaç maddenin hala işlenmesi gerektiğini gösterir. Belge, Commerce Headquarters 'da başarılı şekilde işlenmediyse, **Ayrıntılar** bölmesi hatayla ilgili hata iletilerini de gösterir.

Belge listesi sayfası görünümünde, belge ayrıntılarını görüntülemek için uygulama çubuğunda **sipariş detayları**'nı seçebilirsiniz. Ayrıca, uygun belge satırlarında giriş işlemeyi etkinleştirebilirsiniz.

Belge listesi sayfası görünümünde, mağaza için yeni bir gelen transfer emri isteği de oluşturabilirsiniz. Belgeler **taslak** durumunda kalır ve bunlar işlenmek üzere Commerce Headquarters'a gönderilene kadar düzeltilebilir veya silinebilir. Bunlar Commerce Headquarters'a gönderildikten sonra, taşıma siparişi satırları artık POS uygulamasından değiştirilemez.

## <a name="receiving-process"></a>Alma işlemi

**Etkin** sekmede satın alma emri veya transfer emri belgesi seçildikten sonra, alma işlemine başlamak için **sipariş detayları** seçebilirsiniz.

Varsayılan olarak, **Şimdi alınıyor** görünümü gösterilir. Bu görünüm, barkod taraması için en iyi duruma getirilmiştir. Taranan maddelerin listesini oluşturmak için kullanılabilir, böylece bu maddeler alınabilecek şekilde yapılabilir. Teslim alma işlemine başlamak için madde barkodları taramaya başlayabilirsiniz.

Madde barkodları **şimdi alınıyor** görünümünde tarandıktan sonra, her taranan maddenin belgedeki geçerli bir maddeyle eşleştiğinden emin olmak için, uygulama maddeleri Seçili satınalma veya transfer emri belgesiyle karşılaştırarak doğrular. **Şimdi alınıyor** görünümünde, bir miktar barkoda gömülü olmadığı sürece, bir barkodun her taramanın bir birim miktarının alındığını temsil ettiği varsayılır. Bu görünümde bulunan ve giriş için tüm madde ve miktarların listesini oluşturmak için barkodlara art arda tarama yapabilirsiniz.

### <a name="example-scenario"></a>Örnek senaryo

Bir Kullanıcı, 10 birim 5657900266 barkodu içeren bir satınalma siparişi alır. Kullanıcı, **Şİmdi alınıyor** alanını, her tarama için bir birim olarak güncelleştirmek üzere barkod 10 kere tarama yapabilir. Kullanıcı taramaları tamamladığında, **Şimdi alınıyor** alanı 10 numaralı miktarın alındığını gösterecektir.

Alternatif olarak, madde miktarının büyük olduğu bir senaryoda, Kullanıcı, teslim alınan her madde için barkodunu taramak yerine el ile miktar girmeyi tercih edebilir. Bu durumda, Kullanıcı barkodunu **Şimdi alınıyor** listesine bir kez eklemek için bir seferde bir defa tarama yapabilir. Daha sonra Kullanıcı, **Şimdi alınıyor** görünümünde ilişkili satırı seçebilir ve sonra sayfanın sağ tarafında görüntülenen **Ayrıntılar** bölmesinde maddenin **teslim alma miktarı** alanını güncelleştirebilir.

**Şimdi alınıyor** görünümü barkod taraması için en iyi duruma getirilse de, kullanıcılar uygulama çubuğunda **Ürün al**'ı seçebilir ve öğe kodunu veya barkod verilerini bir iletişim kutusu aracılığıyla girebilir. Girilen madde doğrulandıktan sonra, kullanıcıdan giriş miktarını girmesi istenir.

**Şimdi alınıyor** görünümü, kullanıcıların hangi ürünleri aldığını görmeleri için odaklanmış bir yol sağlar. Alternatif olarak, **tam sipariş listesi** görünümü kullanılabilir. Bu görünüm, seçili satın alma veya transfer emri belgesiyle ilgili tüm belge satırı listesini gösterir. Kullanıcılar, listede el ile satırları el ile seçebilir ve sonra da **Ayrıntılar** bölmesinde, seçili satır için **Şimdi alnıyor** alanını güncelleştirebilir. **Tam sipariş listesi** görünümünde, kullanıcılar barkodları tarayabilir veya madde kodunu veya barkodu girmek için **ürün Al** işlevini, listeden eşleşen madde satırını seçmek zorunda kalmadan ise alınan miktarla ilgili verileri kullanabilir.

### <a name="over-receiving-validations"></a>Fazla alma doğrulamaları

Belge satırları alma işlemi sırasında geçerlilikler meydana gelir. Bunlar fazla teslimat için doğrulama içerirler. Bir Kullanıcı bir satın alma siparişinde sipariş edilen sayıdan daha fazla stok almayı denerse ancak fazla teslimat Konfigüre edilmezse veya teslim alınan miktar, satın alma siparişi satırı için konfigüre edilen fazla teslimat toleransını aşarsa, Kullanıcı hata alır fazlalık miktarı almasına izin verilmez.

Fazla alma, Transfer emri belgeleri için izin verilmez. Kullanıcılar transfer emri satırı için sevk edilmiş olandan fazlasını almayı denerse her zaman hata alır.

### <a name="receiving-location-controlled-items"></a>Yerleşim denetimli maddeleri alma

Alınan maddeler yerleşim denetimli ise, kullanıcılar alma sürecinde almak istedikleri yerleşimi seçebilirler. Bu işlemi daha etkili hale getirmek için mağaza ambarınız için varsayılan bir alma konumu konfigüre etmenizi öneririz. Varsayılan konum konfigüre edilmiş olsa bile, kullanıcılar gerektiğinde Seçili satırlardaki alma konumunu geçersiz kılabilir.

Operasyon, **yerleşim** depolama boyutunda **izin verilen boş giriş**'e karşılık gelir ve boş giriş konfigüre edilebilir ise bir yerleşim boyutu girilmesini gerektirmez. Bir madde için boş giriş yerleşimlerine izin verilmiyorsa POS uygulaması bir hata gösterir ve girişin deftere nakledilebilmesi için bir yerleşim girilmesini gerektirir.

### <a name="receive-all"></a>Tümünü al

Tüm belge satırları için **Şimdi alınıyor** miktarını bu satırlar için alınabilecek maksimum değere hızlı bir şekilde güncelleştirmek için, gerekirse uygulama çubuğunda **Tümünü Al** 'i seçebilirsiniz.

### <a name="cancel-receiving"></a>Teslim almayı iptal et

Yalnızca belgenin dışına geri dönmek istiyorsanız ve değişiklikleri kaydetmek istemiyorsanız, uygulama çubuğundaki **Almayı iptal et** işlevini kullanmalısınız. Örneğin, başlangıçta yanlış belgeyi seçtiniz ve önceki alma verilerinin kaydedilmesini istemezsiniz.

### <a name="pause-receiving"></a>Teslim almayı duraklat

Envanter alındıktan sonra, alma işlemine mola vermek istiyorsanız **Almayı duraklat** işlevini kullanabilirsiniz. Örneğin, POS'tan bir müşteri satışı veya makbuzun deftere naklini ertele ilgili başka bir operasyon gerçekleştirmek isteyebilirsiniz.

**Almayı Duraklat**'ı seçtiğinizde, belgenin durumu **duraklatıldı** olarak değiştirilir. Bu nedenle Kullanıcılar belgede veri girildiğini, ancak belgenin henüz kaydedilmemiş olmadığını bilir. Alma işlemini sürdürmeye hazır olduğunuzda, duraklatılan belgeyi seçin ve **sipariş ayrıntıları**'nı seçin. Daha önce kaydedilen **Şimdi alınıyor** miktarları korunur ve **tam sipariş listesi** görünümünden görüntülenebilir.

### <a name="finish-receiving"></a>Teslim almayı bitir

Ürünlere ait tüm **Şimdi alınıyor** miktarlarını girmeyi bitirdiğinizde, uygulama çubuğunda **Almayı bitir**'i seçmeniz gerekir.

Kullanıcılar bir satın alma siparişi girişini tamamladıklarında, bu işlev konfigüre edildiğinde, **makbuz numarası** alanına bir değer girmeleri istenir. Tipik olarak bu değer, satıcı sevk irsaliyesinin tanımlayıcısı ile eşdeğerdir. **Makbuz numarası** verileri, Commerce Headquarters'daki ürün giriş günlüğünde depolanır. Transfer emri girişleri için giriş numaraları yakalanmadı.

Zaman uyumsuz belge işleme kullanıldığında, makbuz zaman uyumsuz bir belge çerçevesi aracılığıyla gönderilir. Belgenin deftere nakledilmesi için gereken süre belgenin boyutuna (satır sayısı) ve sunucuda gerçekleşen genel işlem akışına bağlıdır. Genellikle bu işlem birkaç saniye içinde gerçekleşir. Belge deftere nakli başarısız olduysa, kullanıcıya, **Gelen operasyon** belge listesi (belge durumunun **işleme başarısız** olarak güncelleştirilecek) aracılığıyla bildirim gönderilir. Kullanıcı daha sonra hata iletilerini ve başarısızlık nedenini **Ayrıntılar** bölmesinde görüntülemek için, POS'ta başarısız olan belgeyi seçebilir. Hatalı bir belge deftere nakledilmemiş olarak kalır ve POS'ta **sipariş ayrıntıları**'nı seçerek kullanıcının belge satırlarına döndürülmesini gerektirir. Kullanıcının hataları temel alarak belgeyi düzeltmelerle güncelleştirmesi gerekir. Belge düzeltildikten sonra, uygulama çubuğunda **karşılamayı bitir**'i seçerek, Kullanıcı işlemi işlemeyi yeniden deneyebilir.

## <a name="create-an-inbound-transfer-order"></a>Gelen transfer emri oluştur

Kullanıcılar POS'tan yeni transfer emri belgeleri oluşturabilirler. İşlemi başlatmak için, ana **Gelen operasyon** belge listesi içindeyken uygulama çubuğunda **yeni**'yi seçin. Daha sonra mağaza konumunuza envanter sağlayacak ambar veya mağazadan **transfer** seçmeniz istenir. Değerler, mağaza yerine getirme grubunun konfigürasyonuyla tanımlanan seçimle sınırlıdır. Gelen bir transfer isteğinde, geçerli deponuzdan transfer emri için her zaman ambardan **transfer** olacak. O değer değiştirilemez.

**Sevk tarihi**, **teslim alma tarihi** ve **teslim alanı** kipinde, gereksinim duyduğunuz şekilde değer girebilirsiniz. Ayrıca, Transfer emri başlığıyla birlikte depolanan bir notu Commerce Headquarters'da belgeye ek olarak da ekleyebilirsiniz.

Başlık bilgileri oluşturulduktan sonra, ürünleri transfer emrine ekleyebilirsiniz. Madde ve istenen miktar ekleme sürecini başlatmak için **Ürün Ekle**'yi seçin. **Ayrıntılar** bölmesinde, günlük satırlarına satıra özel bir not da ekleyebilirsiniz. Bu notlar satır eki olarak depolanacak.

Gelen transfer emrine satırlar girildikten sonra, belge değişikliklerini yerel olarak kaydetmek için **Kaydet**'i seçmeniz veya daha fazla işlem yapmak için sipariş ayrıntılarını Commerce Headquarters'a göndermek amacıyla **talebi göndermek** için öğesini seçmelisiniz. **Kaydet**'i seçerseniz, taslak belge kanal veritabanında depolanır ve giden ambar belgeyi, **İstek gönder** aracılığıyla başarılı şekilde işlenene kadar çalıştıramaz. Yalnızca, isteği Commerce Headquarters 'a işlenmek üzere kaydetmeye hazır değilseniz **kaydet** 'i seçmelisiniz.

Belge yerel olarak kaydedilirse, **gelen operasyon** belgesi listesinin **Taslaklar** sekmesinde bulunabilir. Belge **taslak** durumundayken, **Düzenle** öğesini seçerek düzenleyebilirsiniz. Satırları gereksinim duyduğunuz şekilde güncelleştirebilir, ekleyebilir veya silebilirsiniz. Tüm belgeyi, **taslak** durumundayken, **Taslaklar** sekmesindeki **Sil**'i seçerek de silebilirsiniz.

Taslak belge başarıyla Commerce Headquarters'a gönderildikten sonra **etkin** sekmede görünür ve durumu **istenen** olur. Bu aşamada, gelen mağaza veya ambardaki kullanıcılar artık talep edilen gelen transfer emri belgesini düzenleyebilecek. Yalnızca giden ambardaki kullanıcılar belgeyi, POS uygulamasındaki **giden operasyonunu** seçerek düzenleyebilir. Düzenleme kilidi, gelen bir istek sahibinin, siparişi etkin olarak çekme ve sevk etme işlemlerinde transfer emrini aynı anda değiştirdiği için çakışma olmamasını sağlar. Transfer emri gönderildikten sonra gelen mağaza veya ambarda değişiklik gerekiyorsa çıkış sevkiyatıyla iletişim kurulması ve değişiklikleri girmeleri istenir.

Belge **istenen** duruma girdikten sonra **etkin** sekmesinde görünür. Ancak, henüz gelen mağaza veya ambar tarafından alınamaz. Giden ambar transfer emrinin bir kısmını veya tamamını sevk ettikten sonra, gelen mağaza veya ambar POS'ta alış irsaliyelerini deftere nakledebilir. Giden taraf, transfer emri belgelerini işlerken durumu **talep edilen**'den **Sevk edildi** veya **kısmen sevk edildi** durumuna göre güncelleştirilir. Belgeler **Sevk edidi** veya **kısmen sevk edildi** durumunda ise, gelen mağaza veya ambar gelen operasyon alma sürecini kullanarak kendilerine giriş yapabilir.

## <a name="related-topics"></a>İlgili konular

[POS'ta giden stok işlemi](pos-outbound-inventory-operation.md)
