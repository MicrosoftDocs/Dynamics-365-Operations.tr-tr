---
title: POS'ta giden stok işlemi
description: Bu konu satış noktası (POS) giden stok operasyonunun yeteneklerini açıklar.
author: hhaines
manager: annbe
ms.date: 02/11/2020
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
ms.openlocfilehash: c3e50d20162340c599fb6719ae6f45654dba990a
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071903"
---
# <a name="outbound-inventory-operation-in-pos"></a>POS'ta giden stok işlemi

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Microsoft Dynamics 365 Commerce sürüm 10.0.10 ve sonraki sürümlerinde satış noktasındaki gelen ve giden operasyonlar (POS) malzeme çekme ve teslim alma operasyonunu değiştirir.

> [!NOTE]
> Sürüm 10.0.10 ve sonraki sürümlerde, satın alma siparişlerine ve transfer emirlerine karşı mağaza stoku alma ile ilgili olan POS uygulamasındaki tüm yeni özellikler gelen operasyonlar operasyonuna eklenir. Şu anda POS'ta malzeme çekme ve teslim alma operasyonunu kullanıyorsanız, bu operasyondan yeni gelen ve giden operasyonlarına geçmek için bir strateji geliştirmeniz önerilir. Malzeme çekme ve alma işlemi üründen kaldırılmayabilse de bir işlevsel veya performans açısından 10.0.9 sürümünden sonra başka yatırımlar olmayacak.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Ön koşul: Zaman uyumsuz belge çerçevesini konfigüre edin

Çıkış operasyonu, birçok mağaza veya şirket boyunca yüksek hacimde deftere nakil işlemi yapan kullanıcıların ve büyük stok belgelerinin bu belgeleri zaman aşımı veya hata yaşamdan Commerce Headquarters'a aktarmalarını sağlamak için performans iyileştirmeleri içerir. Bu geliştirmeler zaman uyumsuz bir belge çerçevesinin kullanımını gerektirir.

Zaman uyumsuz bir belge çerçevesi kullanıldığında, POS'tan Commerce Headquarters'a giden belge değişikliklerini uygulayabilir ve daha sonra Commerce Headquarters'a işlem arka planda gerçekleşirken diğer görevlere taşıyabilirsiniz. Deftere Nakletme işleminin başarılı olduğundan emin olmak için, POS'daki **giden operasyon** belge listesi sayfasından belgenin durumunu denetleyebilirsiniz. POS uygulamasında, Commerce Headquarters'a nakledilebilecek tüm belgeleri görmek için giden operasyon etkin belge listesini de kullanabilirsiniz. Belge başarısız olursa POS kullanıcıları bu belgede düzeltmeler yapabilir ve bunu Commerce Headquarters'da işlemeyi yeniden deneyebilir.

> [!IMPORTANT]
> Bir şirket POS'ta giden operasyonu kullanmaya çalışmadan önce zaman uyumsuz belge çerçevesi konfigüre edilmelidir.

Zaman uyumsuz bir belge çerçevesini konfigüre etmek için aşağıdaki yordamları tamamlayın.

### <a name="create-and-configure-a-number-sequence"></a>Numara serileri oluşturma ve yapılandırma

1. **Kuruluş yönetim \> Numara serileri \> Numara serileri**'ne tıklayın.
2. **Numara serileri** sayfasında, bir numara serisi oluşturun.
3. **Numara serisi kodu** ve **ad** alanlarında kullanıcı tanımlı değerler girin.
4. **Referanslar** hızlı sekmesinde **Ekle**'yi seçin.
5. **Alan** alanında **Commerce parametreleri** seçin.
6. **Referans** alanında, **perakende belge işlemi tanımlayıcısı**'nı seçin.
7. **Genel** hızlı sekmesinde, **kurulum** bölümünde performans sorunu olmadığından emin olmak için **devamlı** seçeneğini **Hayır** olarak ayarlayın.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Belge işleme ve izleme görevleri için iki toplu iş oluşturun ve zamanlayın

Oluşturduğunuz toplu işler, başarısız olan veya zaman aşımına uğrayabilen belgeleri işlemek için kullanılır. Bunlar ayrıca, POS'tan işlenmekte olan etkin stok belgelerinin sayısı sistem tarafından yapılandırılmış bir değeri aştığında da kullanılır.

1. **Sistem Yönetimi \> Sorgular \> Toplu işler**'e gidin.
2. **Toplu iş** sayfasında, iki toplu iş oluşturun:

    - **RetailDocumentOperationMonitorBatch** sınıfını çalıştırmak üzere bir iş konfigüre edin.
    - **RetailDocumentOperationProcessingBatch** sınıfını çalıştırmak üzere bir iş konfigüre edin.

3. Yeni toplu işleri yinelenen bir temelde çalışacak şekilde zamanlayın. Örneğin, iş çizelgesini her beş dakikada bir çalışacak şekilde ayarlayın.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Önkoşul: POS ekran düzenine giden işlem Ekle

Kuruluşunuzun giden operasyon işlevini kullanabilmesi için önce bir veya daha fazla [POS ekran mizanpajlarından](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) **giden operasyon** POS operasyonunu konfigüre etmelidir. Yeni operasyonu üretim ortamında dağıtmadan önce, bunu kapsamlı olarak test edin ve kullanıcılarınıza bunu kullanmaya eğittiğinizden emin olun.

## <a name="overview"></a>Genel Bakış

Çıkış operasyonu POS kullanıcıları aşağıdaki görevleri yerine getirelim:

- Kullanıcının mağazanın belirtilen çıkış ambarı olduğu durumlarda transfer emri belgeleri için sevk irsaliyeleri deftere nakledin.
- Mağaza tarafından deftere nakledilen geçmiş transfer emri sevkıyatları hakkındaki bilgileri görüntüleyin.
- Yeni giden transfer emri talepleri oluşturun.

POS uygulamasından giden operasyon başladığında, bir liste sayfası görünümü görüntülenir. Bu görünüm, kullanıcının geçerli mağazanın sevk etmek ve karşılamak üzere amaçlandığı stok satırlarına sahip açık transfer emri belgelerini gösterir. Bir belge seç belgesi bulmak için, kullanıcılar listeyi kaydırabilecek veya arama özelliğini kullanabilir.

Giden stok belgesi listesinde üç sekme vardır.

- **Etkin** – Bu sekme , **talep edilen** veya **kısmen sevk** edilen durumundaki transfer emirlerini gösterir. Siparişler, kullanıcının geçerli deposu tarafından sevk edilmek zorunda olan satırlardaki satırları veya miktarları içerir. Bu sekmede Ayrıca **HQ'da işlem** durumu olan siparişler gösterilir (yani, Commerce Headquarters 'dan başarılı bir şekilde deftere nakil işlemini bekliyor) veya **işlem başarısız oldu** (diğer bir deyişle, Commerce Headquarters 'a nakil işlemi başarısız olur ve kullanıcının siparişi teslim etmek için yeniden denemeniz gerekir).
- **Taslak** – Bu sekmede kullanıcının mağazanın oluşturulduğu yeni giden transfer emri talepleri gösterilir. Ancak, belgeler yalnızca yerel olarak kaydedildi. Bunlar henüz işlenmek üzere Commerce Headquarters'a gönderilmemiş.
- **Tamam** – Bu sekmede, mağazanın son yedi gün içinde tam olarak sevk ettiği transfer emri belgelerinin listesi gösterilir. Bu sekme yalnızca bilgi amaçlıdır. Belgelerle ilgili tüm bilgiler, mağazanın salt okunur verileri olduğunu öğrenin.

Sekmelerin herhangi birinde belge görüntülediğinizde, **durum** alanı belgenin bulunduğu aşamayı anlamanıza yardımcı olabilir.

- **Taslak** – Transfer emri belgesi yalnızca mağazanın kanal veritabanına kaydedildi. Transfer emri talebiyle ilgili hiçbir bilgi henüz Commerce Headquarters'a gönderilmedi.
- **Talep edilen** – satın alma siparişi veya transfer emri Commerce Headquarters'da oluşturulmuş ve tamamen açık. Kullanıcının geçerli deposu, belge bazında herhangi bir sevkiyatı henüz işlemiştir.
- **Kısmen sevk edildi** – Transfer emri belgesi, çıkış ambarı tarafından sevk edilmiş olarak deftere nakledilen bir veya daha fazla satır veya kısmi satır miktarları içerebilir. Sevk edilen bu satırlar gelen operasyonunu içe aktarmak için kullanılabilir.
- **Tam sevk edildi** - Transfer emrinin, çıkış ambarı tarafından sevk edilmiş olarak deftere nakledilen tüm satırları ve tam satır miktarları vardı.
- **Devam edenler** – Bu durum, aygıt kullanıcılarına belgenin başka bir kullanıcı tarafından etkin olarak çalıştığını bildirmek için kullanılır.
- **Duraklatıldı** – Alma işlemini geçici olarak durdurmak için **duraklatma alma** işlemi seçildikten sonra bu durum gösterilir.
- **HQ'da işleme** – Belge POS uygulamasından Commerce Headquarters'a gönderilmiştir, ancak henüz Commerce Headquarters 'a nakledilmemiştir. Belge, zaman uyumsuz belge deftere nakil işlemine geçiyor. Belge, Commerce Headquarters 'a başarıyla nakledildikten sonra, durumu **tam olarak alındı** veya **kısmen alındı** olarak güncelleştirilmelidir.
- **İşlem başarısız oldu** – Belge, Commerce Headquarters'a nakledildi ve reddedildi. **Ayrıntılar** bölmesi deftere nakil hatasının nedenini gösterir. Veri sorunlarını düzeltmek için belgenin düzenlenmesi ve daha sonra işlenmek üzere Commerce Headquarters'a yeniden gönderilmesi gerekir.

Listeden bir belge satırı seçtiğinizde **Ayrıntılar** bölmesi görüntülenir. Bu bölme, belge hakkında Sevkiyat ve tarih bilgileri gibi ek bilgiler gösterir. İlerleme çubuğu, kaç maddenin hala işlenmesi gerektiğini gösterir. Belge, Commerce Headquarters 'da başarılı şekilde işlenmediyse, **Ayrıntılar** bölmesi hatayla ilgili hata iletilerini de gösterir.

Belge listesi sayfası görünümünde, belge ayrıntılarını görüntülemek için uygulama çubuğunda **sipariş detayları**'nı seçebilirsiniz. Ayrıca, uygun belge satırlarında giriş işlemeyi etkinleştirebilirsiniz.

Belge listesi sayfası görünümünde, mağaza için yeni bir giden transfer emri de oluşturabilirsiniz.

## <a name="transfer-order-shipping-process"></a>Transfer emri gönderme işlemi

**Etkin** sekmede transfer emri belgesi seçildikten sonra, karşılama işlemine başlamak için **sipariş detayları** seçebilirsiniz. **Tam sipariş listesi** görünümü görüntülenir. Bu sayfa, maddeyi içeren tüm belge satırlarını gösterir. Ayrıca, sipariş edilen miktarın ayrıntılarını da gösterir.

Bir barkodun her taramasında, **şimdi sevk etme** alanındaki miktar bir birim olarak güncelleştirilir. Alternatif olarak, uygulama çubuğundaki **ürünü gönderi** seçip bir madde kodu girip miktarı girerek bir sevkiyat miktarı girebilirsiniz. Madde yerleşim denetimli ise, belge satırı için sevkiyat yerleşimini onaylar veya ayarlayabilirsiniz.

**Tam sipariş listesi** görünümünde, listeden bir satırı el ile seçebilir ve ardından **Ayrıntılar** bölmesindeki seçili satır için **şimdi sevkiyat** miktarını güncelleştirebilirsiniz.

### <a name="over-delivery-shipping-validations"></a>Fazla teslimat sevkiyat doğrulamaları

Belge satırları alma işlemi sırasında geçerlilikler meydana gelir. Bunlar fazla teslimat için doğrulama içerirler. Bir Kullanıcı bir satın alma siparişinde sipariş edilen sayıdan daha fazla stok almayı denerse ancak fazla teslimat Konfigüre edilmezse veya teslim alınan miktar, satın alma siparişi satırı için konfigüre edilen fazla teslimat toleransını aşarsa, Kullanıcı hata alır fazlalık miktarı almasına izin verilmez.

### <a name="shipping-location-controlled-items"></a>Yerleşim denetimli maddeleri gönderme

Sevk edilen maddeler yerleşim denetimli ise, kullanıcılar sevkiyat sürecinde stok vermek istedikleri yerleşimi seçebilirler. Bu işlemi daha etkili hale getirmek için mağaza ambarınız için varsayılan bir çıkış konumu konfigüre etmenizi öneririz. Varsayılan konum konfigüre edilmiş olsa bile, kullanıcılar gerektiğinde Seçili satırlardaki konu konumunu geçersiz kılabilir.

Operasyon, **yerleşim** depolama boyutunda **izin verilen boş giriş**'e karşılık gelir ve boş giriş konfigüre edilebilir ise bir yerleşim boyutu girilmesini gerektirmez. Bir madde için boş giriş yerleşimlerine izin verilmiyorsa POS uygulaması bir hata gösterir ve girişin deftere nakledilebilmesi için bir yerleşim girilmesini gerektirir.

### <a name="ship-all"></a>Tümünü sevk et

Tüm belge satırları için **Hemen gönderme** miktarını bu satırlar için yerine getirilebilecek maksimum değere hızlı bir şekilde güncelleştirmek için, gerekirse uygulama çubuğunda **Tümünü Gönder** 'i seçebilirsiniz.

### <a name="cancel-fulfillment"></a>Karşılamayı iptal et

Yalnızca belgenin dışına geri dönmek istiyorsanız ve değişiklikleri kaydetmek istemiyorsanız, uygulama çubuğundaki **karşılama iptali** işlevini kullanmalısınız. Örneğin, başlangıçta yanlış belgeyi seçtiniz ve önceki sevkiyat verilerinin kaydedilmesini istemezsiniz.

### <a name="pause-fulfillment"></a>Karşılamayı duraklat

Transfer emrini yerine getirdikten sonra, işlemden mola almak istiyorsanız **karşılamayı duraklat** işlevini kullanabilirsiniz. Örneğin, POS'tan bir müşteri satışı veya sevkiyatın deftere naklini ertele ilgili başka bir operasyon gerçekleştirmek isteyebilirsiniz.

**Karşılamayı Duraklat**'ı seçtiğinizde, belgenin durumu **duraklatıldı** olarak değiştirilir. Bu nedenle Kullanıcı belgede veri girildiğini, ancak belgenin henüz kaydedilmemiş olmadığını bilir. Karşılama işlemini sürdürmeye hazır olduğunuzda, duraklatılan belgeyi seçin ve **sipariş ayrıntıları**'nı seçin. Daha önce kaydedilen **Şimdi sevk** miktarları korunur ve **tam sipariş listesi** görünümünden görüntülenebilir.

### <a name="finish-fulfillment"></a>Karşılama işlemini bitir

Ürünlere ait tüm **Şimdi gnder** miktarlarını girmeyi bitirdiğinizde, uygulama çubuğunda **Karşılamayı bitir**'i seçmeniz gerekir.

Zaman uyumsuz belge işleme kullanıldığında, makbuz zaman uyumsuz bir belge çerçevesi aracılığıyla gönderilir. Belgenin deftere nakledilmesi için gereken süre belgenin boyutuna (satır sayısı) ve sunucuda gerçekleşen genel işlem akışına bağlıdır. Genellikle bu işlem birkaç saniye içinde gerçekleşir. Belge deftere nakli başarısız olduysa, kullanıcıya, **etkin** sekmesindeki **giden operasyon** belge listesi (belge durumunun **işleme başarısız** olarak güncelleştirilecek) aracılığıyla bildirim gönderilir. Kullanıcı daha sonra hata iletilerini ve başarısızlık nedenini **Ayrıntılar** bölmesinde görüntülemek için, POS'ta başarısız olan belgeyi seçebilir. Hatalı bir belge deftere nakledilmemiş olarak kalır ve POS'ta **sipariş ayrıntıları**'nı seçerek kullanıcının belge satırlarına döndürülmesini gerektirir. Kullanıcının hataları temel alarak belgeyi düzeltmelerle güncelleştirmesi gerekir. Belge düzeltildikten sonra, uygulama çubuğunda **karşılamayı bitir**'i seçerek, Kullanıcı işlemi işlemeyi yeniden deneyebilir.

## <a name="create-an-outbound-transfer-order"></a>Giden transfer emri oluştur

Kullanıcılar POS'tan yeni transfer emri belgeleri oluşturabilirler. İşlemi başlatmak için, ana **giden operasyon** belge listesi içindeyken uygulama çubuğunda **yeni**'yi seçin. Daha sonra geçerli deponuzun stok gönderecek ambar veya mağazaya **transfer** seçmeniz istenir. Değerler, mağaza yerine getirme grubunun konfigürasyonuyla tanımlanan seçimle sınırlıdır. Giden bir transfer isteğinde, geçerli deponuzdan transfer emri için her zaman ambardan **transfer** olacak. O değer değiştirilemez.

**Sevk tarihi**, **teslim alma tarihi** ve **teslim alanı** kipinde, gereksinim duyduğunuz şekilde değer girebilirsiniz. Ayrıca, Transfer emri başlığıyla birlikte depolanan bir notu Commerce Headquarters'da belgeye ek olarak da ekleyebilirsiniz.

Başlık bilgileri oluşturulduktan sonra, ürünleri transfer emrine ekleyebilirsiniz. Madde ve istenen miktar ekleme sürecini başlatmak için barkod tarama veya **Ürün Ekle**'yi seçin.

Giden transfer emrine satırlar girildikten sonra, belge değişikliklerini yerel olarak kaydetmek için **Kaydet**'i seçmeniz veya daha fazla işlem yapmak için sipariş ayrıntılarını Commerce Headquarters'a göndermek amacıyla **talebi göndermek** için öğesini seçmelisiniz. **Kaydet**'i seçerseniz, taslak belge kanal veritabanında depolanır ve giden ambar belgeyi, **İstek gönder** aracılığıyla başarılı şekilde işlenene kadar çalıştıramaz. Yalnızca, isteği Commerce Headquarters 'a işlenmek üzere kaydetmeye hazır değilseniz **kaydet** 'i seçmelisiniz.

Belge yerel olarak kaydedilirse, **gelen operasyon** belgesi listesinin **Taslaklar** sekmesinde bulunabilir. Belge **taslak** durumundayken, **Düzenle** öğesini seçerek düzenleyebilirsiniz. Satırları gereksinim duyduğunuz şekilde güncelleştirebilir, ekleyebilir veya silebilirsiniz. Tüm belgeyi, **taslak** durumundayken, **Taslaklar** sekmesindeki **Sil**'i seçerek de silebilirsiniz.

Taslak belge başarıyla Commerce Headquarters'a gönderildikten sonra **etkin** sekmede görünür ve durumu **istenen** olur. Bu aşamada, yalnızca giden ambardaki kullanıcılar belgeyi, POS uygulamasındaki **giden operasyonunu** seçerek düzenleyebilir. Gelen ambardaki kullanıcılar transfer emrini **gelen operasyon** belge listesinin **etkin** sekmesinde görüntüleyebilir, ancak düzenleyemez veya silemez. Düzenleme kilidi, gelen bir istek sahibinin, siparişi etkin olarak çekme ve sevk etme işlemlerinde transfer emrini aynı anda değiştirdiği için çakışma olmamasını sağlar. Transfer emri gönderildikten sonra gelen mağaza veya ambarda değişiklik gerekiyorsa çıkış sevkiyatıyla iletişim kurulması ve değişiklikleri girmeleri istenir.

Belge **istenen** duruma girdikten sonra, çıkış ambarı tarafından işlem için yerine getirilmesi hazırdır. Sevkiyat giden operasyonu kullanılarak işlenirken, Transfer emri belgelerinin durumu **talep edilen** **tamamıyla sevk edilen** veya **kısmen sevk edilen** durumuna göre güncelleştirilir. Belgeler **tam olarak sevk edilen** veya **kısmen sevk edildi** durumunda ise, gelen mağaza veya ambar gelen operasyon alma sürecini kullanarak kendilerine giriş yapabilir.

Tam olarak sevk edilen transfer emirleri, **giden operasyon** belgesi listesinin **tam** sekmesine kopyalanır. Burada, giden mağaza veya ambardaki kullanıcılar, salt okunur modda yedi gün süreyle görünür durumda kalırlar.

## <a name="related-topics"></a>İlgili konular

[POS'ta gelen stok işlemi](pos-inbound-inventory-operation.md)