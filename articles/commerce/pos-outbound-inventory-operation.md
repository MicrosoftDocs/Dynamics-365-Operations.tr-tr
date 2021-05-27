---
title: POS'ta giden stok işlemi
description: Bu konu satış noktası (POS) giden stok operasyonunun yeteneklerini açıklar.
author: hhaines
ms.date: 07/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 5a2c596293e632bb6c06af56f413fcee9e867563
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022743"
---
# <a name="outbound-inventory-operation-in-pos"></a>POS'ta giden stok işlemi

[!include [banner](includes/banner.md)]


Microsoft Dynamics 365 Commerce sürüm 10.0.10 ve sonraki sürümlerinde satış noktasındaki gelen ve giden operasyonlar (POS) malzeme çekme ve teslim alma operasyonunu değiştirir.

> [!NOTE]
> Sürüm 10.0.10 ve sonraki sürümlerde, satın alma siparişlerine ve transfer emirlerine karşı mağaza stoku alma ile ilgili olan POS uygulamasındaki tüm yeni özellikler gelen operasyonlar operasyonuna eklenir. Şu anda POS'ta malzeme çekme ve teslim alma operasyonunu kullanıyorsanız, bu operasyondan yeni gelen ve giden operasyonlarına geçmek için bir strateji geliştirmeniz önerilir. Malzeme çekme ve alma işlemi üründen kaldırılmayabilse de bir işlevsel veya performans açısından 10.0.9 sürümünden sonra başka yatırımlar olmayacak.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Ön koşul: Zaman uyumsuz belge çerçevesini konfigüre edin

Çıkış operasyonu, birçok mağaza veya şirket boyunca yüksek hacimde deftere nakil işlemi yapan kullanıcıların ve büyük stok belgelerinin bu belgeleri zaman aşımı veya hata yaşamdan Commerce Headquarters'a (HQ) aktarmalarını sağlamak için performans iyileştirmeleri içerir. Bu geliştirmeler zaman uyumsuz bir belge çerçevesinin kullanımını gerektirir.

Zaman uyumsuz bir belge çerçevesi kullanıldığında, POS'tan Commerce Headquarters'a (HQ) giden belge değişikliklerini uygulayabilir ve daha sonra Commerce Headquarters'a (HQ) işlem arka planda gerçekleşirken diğer görevlere taşıyabilirsiniz. Deftere Nakletme işleminin başarılı olduğundan emin olmak için, POS'daki **giden operasyon** belge listesi sayfasından belgenin durumunu denetleyebilirsiniz. POS uygulamasında, Commerce Headquarters'a (HQ) nakledilebilecek tüm belgeleri görmek için giden operasyon etkin belge listesini de kullanabilirsiniz. Belge başarısız olursa POS kullanıcıları bu belgede düzeltmeler yapabilir ve bunu Commerce Headquarters'da (HQ) işlemeyi yeniden deneyebilir.

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

> [!NOTE]
> Commerce sürüm 10.0.13 ve sonrasında, toplu işleri toplu iş çerçevesi aracılığıyla yapılandırmak zorunda değilsiniz. Toplu işler **Retail ve Commerce > Retail ve Commerce BT** menüsünden yapılandırılabilir. Toplu işleri yapılandırmak için **Perakende belge işlemi izleyicisi** ve **Perakende belge işlemi işleme** menü seçeneklerini kullanın

Oluşturduğunuz toplu işler, başarısız olan veya zaman aşımına uğrayabilen belgeleri işlemek için kullanılır. Bunlar ayrıca, POS'tan işlenmekte olan etkin stok belgelerinin sayısı sistem tarafından yapılandırılmış bir değeri aştığında da kullanılır.

1. **Sistem Yönetimi \> Sorgular \> Toplu işler**'e gidin.
2. **Toplu iş** sayfasında, iki toplu iş oluşturun:

    - **RetailDocumentOperationMonitorBatch** sınıfını çalıştırmak üzere bir iş konfigüre edin.
    - **RetailDocumentOperationProcessingBatch** sınıfını çalıştırmak üzere bir iş konfigüre edin.

3. Yeni toplu işleri yinelenen bir temelde çalışacak şekilde zamanlayın. Örneğin, iş çizelgesini her beş dakikada bir çalışacak şekilde ayarlayın.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Önkoşul: POS ekran düzenine giden işlem Ekle

Kuruluşunuzun giden operasyon işlevini kullanabilmesi için önce bir veya daha fazla [POS ekran mizanpajlarından](/dynamics365/unified-operations/retail/pos-screen-layouts) **giden operasyon** POS operasyonunu konfigüre etmelidir. Yeni operasyonu üretim ortamında dağıtmadan önce, bunu kapsamlı olarak test edin ve kullanıcılarınıza bunu kullanmaya eğittiğinizden emin olun.

## <a name="overview"></a>Genel Bakış

Çıkış operasyonu POS kullanıcıları aşağıdaki görevleri yerine getirelim:

- Kullanıcının mağazanın belirtilen çıkış ambarı olduğu durumlarda transfer emri belgeleri için sevk irsaliyeleri deftere nakledin.
- Mağaza tarafından deftere nakledilen geçmiş transfer emri sevkıyatları hakkındaki bilgileri görüntüleyin.
- Yeni giden transfer emri talepleri oluşturun.

POS uygulamasından giden operasyon başladığında, bir liste sayfası görünümü görüntülenir. Bu görünüm, kullanıcının geçerli mağazanın sevk etmek ve karşılamak üzere amaçlandığı stok satırlarına sahip açık transfer emri belgelerini gösterir. Bir belge seç belgesi bulmak için, kullanıcılar listeyi kaydırabilecek veya arama özelliğini kullanabilir.

Giden stok belgesi listesinde üç sekme vardır.

- **Etkin** – Bu sekme , **talep edilen** veya **kısmen sevk** edilen durumundaki transfer emirlerini gösterir. Siparişler, kullanıcının geçerli deposu tarafından sevk edilmek zorunda olan satırlardaki satırları veya miktarları içerir. Bu sekmede Ayrıca **HQ'da işlem** durumu olan siparişler gösterilir (yani, Commerce Headquarters'dan [HQ] başarılı bir şekilde deftere nakil işlemini bekliyor) veya **işlem başarısız oldu** (diğer bir deyişle, Commerce Headquarters'a (HQ) nakil işlemi başarısız olur ve kullanıcının siparişi teslim etmek için yeniden denemeniz gerekir).
- **Taslak** – Bu sekmede kullanıcının mağazanın oluşturulduğu yeni giden transfer emri talepleri gösterilir. Ancak, belgeler yalnızca yerel olarak kaydedildi. Bunlar henüz işlenmek üzere Commerce Headquarters'a (HQ) gönderilmemiş.
- **Tamam** – Bu sekmede, mağazanın son yedi gün içinde tam olarak sevk ettiği transfer emri belgelerinin listesi gösterilir. Bu sekme yalnızca bilgi amaçlıdır. Belgelerle ilgili tüm bilgiler, mağazanın salt okunur verileri olduğunu öğrenin.

Sekmelerin herhangi birinde belge görüntülediğinizde, **durum** alanı belgenin bulunduğu aşamayı anlamanıza yardımcı olabilir.

- **Taslak** – Transfer emri belgesi yalnızca mağazanın kanal veritabanına kaydedildi. Transfer emri talebiyle ilgili hiçbir bilgi henüz Commerce Headquarters'a (HQ) gönderilmedi.
- **Talep edildi** – Satın alma siparişi veya transfer emri Commerce Headquarters'da (HQ) oluşturulmuş ve tamamen açık. Kullanıcının geçerli deposu, belge bazında herhangi bir sevkiyatı henüz işlemiştir.
- **Kısmen sevk edildi** – Transfer emri belgesi, çıkış ambarı tarafından sevk edilmiş olarak deftere nakledilen bir veya daha fazla satır veya kısmi satır miktarları içerebilir. Sevk edilen bu satırlar gelen operasyonunu içe aktarmak için kullanılabilir.
- **Tam sevk edildi** - Transfer emrinin, çıkış ambarı tarafından sevk edilmiş olarak deftere nakledilen tüm satırları ve tam satır miktarları vardı.
- **Devam edenler** – Bu durum, aygıt kullanıcılarına belgenin başka bir kullanıcı tarafından etkin olarak çalıştığını bildirmek için kullanılır.
- **Duraklatıldı** – Alma işlemini geçici olarak durdurmak için **duraklatma alma** işlemi seçildikten sonra bu durum gösterilir.
- **HQ'da işleniyor** – Belge POS uygulamasından Commerce Headquarters'a (HQ) gönderilmiştir, ancak henüz Commerce Headquarters'a (HQ) nakledilmemiştir. Belge, zaman uyumsuz belge deftere nakil işlemine geçiyor. Belge, Commerce Headquarters'a (HQ) başarıyla nakledildikten sonra, durumu **tam olarak alındı** veya **kısmen alındı** olarak güncelleştirilmelidir.
- **İşlem başarısız oldu** – Belge, Commerce Headquarters'a (HQ) nakledildi ve reddedildi. **Ayrıntılar** bölmesi deftere nakil hatasının nedenini gösterir. Veri sorunlarını düzeltmek için belgenin düzenlenmesi ve daha sonra işlenmek üzere Commerce Headquarters'a (HQ) yeniden gönderilmesi gerekir.

Listeden bir belge satırı seçtiğinizde **Ayrıntılar** bölmesi görüntülenir. Bu bölme, belge hakkında Sevkiyat ve tarih bilgileri gibi ek bilgiler gösterir. İlerleme çubuğu, kaç maddenin hala işlenmesi gerektiğini gösterir. Belge, Commerce Headquarters'da (HQ) başarılı şekilde işlenmediyse, **Ayrıntılar** bölmesi hatayla ilgili hata iletilerini de gösterir.

Belge listesi sayfası görünümünde, belge ayrıntılarını görüntülemek için uygulama çubuğunda **sipariş detayları**'nı seçebilirsiniz. Ayrıca, uygun belge satırlarında giriş işlemeyi etkinleştirebilirsiniz.

Belge listesi sayfası görünümünde, mağaza için yeni bir giden transfer emri de oluşturabilirsiniz.

## <a name="transfer-order-shipping-process"></a>Transfer emri gönderme işlemi

**Etkin** sekmede transfer emri belgesi seçildikten sonra, karşılama işlemine başlamak için **sipariş detayları** seçebilirsiniz. **Tam sipariş listesi** görünümü görüntülenir. Bu sayfa, maddeyi içeren tüm belge satırlarını gösterir. Ayrıca, sipariş edilen miktarın ayrıntılarını da gösterir.

Bir barkodun her taramasında, **şimdi sevk etme** alanındaki miktar bir birim olarak güncelleştirilir. Alternatif olarak, uygulama çubuğundaki **ürünü gönderi** seçip bir madde kodu girip miktarı girerek bir sevkiyat miktarı girebilirsiniz. Madde yerleşim denetimli ise, belge satırı için sevkiyat yerleşimini onaylar veya ayarlayabilirsiniz.

**Tam sipariş listesi** görünümünde, listeden bir satırı el ile seçebilir ve ardından **Ayrıntılar** bölmesindeki seçili satır için **şimdi sevkiyat** miktarını güncelleştirebilirsiniz.

### <a name="over-delivery-shipping-validations"></a>Fazla teslimat sevkiyat doğrulamaları

Belge satırları alma işlemi sırasında geçerlilikler meydana gelir. Bunlar fazla teslimat için doğrulama içerirler. Bir Kullanıcı bir satın alma siparişinde sipariş edilen sayıdan daha fazla stok almayı denerse ancak fazla teslimat Konfigüre edilmezse veya teslim alınan miktar, satın alma siparişi satırı için konfigüre edilen fazla teslimat toleransını aşarsa, Kullanıcı hata alır fazlalık miktarı almasına izin verilmez.

### <a name="underdelivery-close-lines"></a>Eksik teslimat kapatma satırları

Commerce 10.0.12 sürümünde, giden ambar istenen tam miktarı sevk edemeyeceğini belirlerse, POS kullanıcılarının giden sipariş sevkiyatı sırasında kalan miktarları kapatmasına veya iptal etmesine olanak veren işlevler eklenmiştir. Miktarlar da daha sonra kapatılabilir veya iptal edilebilir. Bu yeteneği kullanmak için şirketin transfer emirlerinin eksik teslimatına izin verecek şekilde yapılandırılmış olması gerekir. Ek olarak, transfer emri satırı için eksik teslimat yüzdesi tanımlanmalıdır.

Şirketi transfer emirlerinin eksik teslimatına izin verecek şekilde yapılandırmak için Commerce Headquarters'da (HQ) **Stok yönetimi \> Kurulum \> Stok ve ambar yönetim parametreleri** öğesine gidin. **Stok ve ambar yönetim parametreleri** sayfasındaki **Transfer emirleri** sekmesinde, **Eksik teslimatı kabul et** parametresini açın. Daha sonra, parametre değişikliklerini depolama kanalınızla eşitlemek için **1070** dağıtım zamanlayıcısı işini çalıştırın.

Transfer emri satırı için eksik teslimat yüzdeleri, Commerce Headquarters'da ürün yapılandırmasının bir parçası olarak ürünlerde önceden tanımlanabilir. Alternatif olarak, Commerce Headquarters (HQ) aracılığıyla belirli bir transfer emri satırında bunlar ayarlanabilir veya bunların üzerine yazılabilir.

Bir kuruluş transfer emrinin eksik teslimatını yapılandırmayı tamamladıktan sonra, POS kullanıcıları **Giden işlem** işlevi aracılığıyla bir giden transfer emri satırını seçtiklerinde, **Ayrıntılar** bölmesinde yeni bir **Kalan miktarı kapat** seçeneği görür. Kullanıcı, **Karşılamayı bitir** işlemini kullanarak sevkiyatı tamamladığında, kalan sevk edilmemiş miktarı iptal etmek Için Commerce Headquarters'a (HQ) bir talep gönderebilirler. Kullanıcı kalan miktarı kapatırsa Commerce, iptal edilen miktarın transfer emri satırında tanımlanan eksik teslimat yüzdesi toleransı dahilinde olduğunu bir doğrulama işlemiyle doğrular. Eksik teslimat toleransı aşılırsa bir hata iletisi gösterilir ve kullanıcı önceden sevk edilen ve "şimdi sevk et" miktarı eşleşinceye veya eksik teslimat toleransını aşıncaya kadar kalan miktarı kapatamaz.

Sevkiyat Commerce Headquarters (HQ) ile eşitlendikten sonra, POS'taki transfer emri satırının **Şimdi sevk et** alanında tanımlanan miktarlar Commerce Headquarters'da (HQ) sevk edildi durumuna güncelleştirilir. Önceden "kalan sevk" miktarları (daha sonra sevk edilecek miktarlar) olarak kabul edilen sevk edilmemiş miktarlar, bunun yerine iptal edilen miktarlar olarak kabul edilir. Transfer emri satırının "kalan sevk" miktarı **0** (sıfır) olarak, satır ise tamamen sevk edildi olarak ayarlanır.

### <a name="shipping-location-controlled-items"></a>Yerleşim denetimli maddeleri gönderme

Sevk edilen maddeler yerleşim denetimli ise, kullanıcılar sevkiyat sürecinde stok vermek istedikleri yerleşimi seçebilirler. Bu işlemi daha etkili hale getirmek için mağaza ambarınız için varsayılan bir çıkış konumu konfigüre etmenizi öneririz. Varsayılan konum konfigüre edilmiş olsa bile, kullanıcılar gerektiğinde Seçili satırlardaki konu konumunu geçersiz kılabilir.

Operasyon, **yerleşim** depolama boyutunda **izin verilen boş giriş**'e karşılık gelir ve boş giriş konfigüre edilebilir ise bir yerleşim boyutu girilmesini gerektirmez. Bir madde için boş giriş yerleşimlerine izin verilmiyorsa POS uygulaması bir hata gösterir ve girişin deftere nakledilebilmesi için bir yerleşim girilmesini gerektirir.

### <a name="ship-all"></a>Tümünü sevk et

Tüm belge satırları için **Hemen gönderme** miktarını bu satırlar için yerine getirilebilecek maksimum değere hızlı bir şekilde güncelleştirmek için, gerekirse uygulama çubuğunda **Tümünü Gönder** 'i seçebilirsiniz.

### <a name="cancel-fulfillment"></a>Karşılamayı iptal et

Belgenin dışına geri dönmek istiyorsanız ve değişiklikleri kaydetmek istemiyorsanız, uygulama çubuğundaki **Karşılamayı iptal et** işlevini kullanın. Örneğin, başlangıçta yanlış belgeyi seçtiniz ve önceki sevkiyat verilerinin kaydedilmesini istemezsiniz.

### <a name="pause-fulfillment"></a>Karşılamayı duraklat

Transfer emrini yerine getirdikten sonra, işlemden mola almak istiyorsanız **karşılamayı duraklat** işlevini kullanabilirsiniz. Örneğin, POS'tan bir müşteri satışı veya sevkiyatın Commerce Headquarters'a (HQ) naklini erteleme ile ilgili başka bir işlem gerçekleştirmek isteyebilirsiniz.

**Karşılamayı Duraklat**'ı seçtiğinizde, belgenin durumu **duraklatıldı** olarak değiştirilir. Bu nedenle Kullanıcı belgede veri girildiğini, ancak belgenin henüz kaydedilmemiş olmadığını bilir. Karşılama işlemini sürdürmeye hazır olduğunuzda, duraklatılan belgeyi seçin ve **sipariş ayrıntıları**'nı seçin. Daha önce kaydedilen **Şimdi sevk** miktarları korunur ve **tam sipariş listesi** görünümünden görüntülenebilir.

### <a name="review"></a>Gözden geçir

Karşılamanın Commerce Headquarters'a (HQ) nihai uygulanmasından önce, giden belgeyi doğrulamak için **İnceleme** işlevini kullanabilirsiniz. Bu işlev, işlem hatasına neden olabilecek potansiyel eksik veya yanlış veriler için sizi uyarır ve karşılama isteğini göndermeden önce size sorunları çözme fırsatı sağlar. Uygulama çubuğunda **İnceleme** işlevini etkinleştirmek için Commerce Headquarters'daki (HQ) Özellik yönetimi özelliği aracılığıyla **POS gelen ve giden stok operasyonları özelliğinde doğrulamayı etkinleştir** özelliğini etkinleştirin.

**İnceleme** işlevi bir giden belgedeki aşağıdaki sorunları doğrular:
- **Fazla gönderme** - Şimdi gönderme miktarı sipariş edilen miktardan fazla. Bu sorunun önem derecesi, Commerce Headquarters'daki (HQ) fazla teslimat yapılandırması tarafından belirlenir.
- **Eksik gönderme** - Şimdi gönderme miktarı sipariş edilen miktardan az. Bu sorunun önem derecesi, Commerce Headquarters'daki (HQ) eksik teslimat yapılandırması tarafından belirlenir.
- **Seri numarası** – Seri numarasının stoka kaydedilmesini gerektiren serileştirilmiş bir kalem için seri numarası sağlanmamış veya mevcut değil.
- **Konum ayarlanmadı** – Konum denetimli bir kalem için konumun boş olmasına izin verilmediği durumda konum belirtilmemiştir.
- **Silinen satırlar** – Siparişte, POS uygulaması tarafından bilinmeyen bir Commerce Headquarters (HQ) kullanıcısı tarafından silinen satırlar vardır.

**Commerce parametreleri** > **Stok** > **Mağaza stoğu operasyonları** bölümünde **Otomatik doğrulamayı etkinleştir** parametresini **Evet** olarak ayarlarsanız **Almayı bitir** işlevini seçtiğinizde doğrulama otomatik olarak gerçekleştirilir.

### <a name="finish-fulfillment"></a>Karşılama işlemini bitir

Ürünlere ait tüm **Şimdi gnder** miktarlarını girmeyi bitirdiğinizde, uygulama çubuğunda **Karşılamayı bitir**'i seçmeniz gerekir.

Zaman uyumsuz belge işleme kullanıldığında, makbuz zaman uyumsuz bir belge çerçevesi aracılığıyla gönderilir. Belgenin deftere nakledilmesi için gereken süre belgenin boyutuna (satır sayısı) ve sunucuda gerçekleşen genel işlem akışına bağlıdır. Genellikle bu işlem birkaç saniye içinde gerçekleşir. Belge deftere nakli başarısız olduysa, kullanıcıya, **etkin** sekmesindeki **giden operasyon** belge listesi (belge durumunun **işleme başarısız** olarak güncelleştirilecek) aracılığıyla bildirim gönderilir. Kullanıcı daha sonra hata iletilerini ve başarısızlık nedenini **Ayrıntılar** bölmesinde görüntülemek için, POS'ta başarısız olan belgeyi seçebilir. Hatalı bir belge deftere nakledilmemiş olarak kalır ve POS'ta **sipariş ayrıntıları**'nı seçerek kullanıcının belge satırlarına döndürülmesini gerektirir. Kullanıcının hataları temel alarak belgeyi düzeltmelerle güncelleştirmesi gerekir. Belge düzeltildikten sonra, uygulama çubuğunda **karşılamayı bitir**'i seçerek, Kullanıcı işlemi işlemeyi yeniden deneyebilir.

## <a name="create-an-outbound-transfer-order"></a>Giden transfer emri oluştur

Kullanıcılar POS'tan yeni transfer emri belgeleri oluşturabilirler. İşlemi başlatmak için, ana **giden operasyon** belge listesi içindeyken uygulama çubuğunda **yeni**'yi seçin. Daha sonra geçerli deponuzun stok gönderecek ambar veya mağazaya **transfer** seçmeniz istenir. Değerler, mağaza yerine getirme grubunun konfigürasyonuyla tanımlanan seçimle sınırlıdır. Giden bir transfer isteğinde, geçerli deponuzdan transfer emri için her zaman ambardan **transfer** olacak. O değer değiştirilemez.

**Sevk tarihi**, **teslim alma tarihi** ve **teslim alanı** kipinde, gereksinim duyduğunuz şekilde değer girebilirsiniz. Ayrıca, Transfer emri başlığıyla birlikte depolanan bir notu Commerce Headquarters'da (HQ) belgeye ek olarak da ekleyebilirsiniz.

Başlık bilgileri oluşturulduktan sonra, ürünleri transfer emrine ekleyebilirsiniz. Madde ve istenen miktar ekleme sürecini başlatmak için barkod tarama veya **Ürün Ekle**'yi seçin.

Giden transfer emrine satırlar girildikten sonra, belge değişikliklerini yerel olarak kaydetmek için **Kaydet**'i seçmeniz veya daha fazla işlem yapmak için sipariş ayrıntılarını Commerce Headquarters'a (HQ) göndermek amacıyla **talebi göndermek** için öğesini seçmelisiniz. **Kaydet**'i seçerseniz, taslak belge kanal veritabanında depolanır ve giden ambar belgeyi, **İstek gönder** aracılığıyla başarılı şekilde işlenene kadar çalıştıramaz. Yalnızca, isteği Commerce Headquarters'a (HQ) işlenmek üzere kaydetmeye hazır değilseniz **kaydet** 'i seçmelisiniz.

Belge yerel olarak kaydedilirse, **gelen operasyon** belgesi listesinin **Taslaklar** sekmesinde bulunabilir. Belge **taslak** durumundayken, **Düzenle** öğesini seçerek düzenleyebilirsiniz. Satırları gereksinim duyduğunuz şekilde güncelleştirebilir, ekleyebilir veya silebilirsiniz. Tüm belgeyi, **taslak** durumundayken, **Taslaklar** sekmesindeki **Sil**'i seçerek de silebilirsiniz.

Taslak belge başarıyla Commerce Headquarters'a (HQ) gönderildikten sonra **etkin** sekmede görünür ve durumu **istenen** olur. Bu aşamada, yalnızca giden ambardaki kullanıcılar belgeyi, POS uygulamasındaki **giden operasyonunu** seçerek düzenleyebilir. Gelen ambardaki kullanıcılar transfer emrini **gelen operasyon** belge listesinin **etkin** sekmesinde görüntüleyebilir, ancak düzenleyemez veya silemez. Düzenleme kilidi, gelen bir istek sahibinin, siparişi etkin olarak çekme ve sevk etme işlemlerinde transfer emrini aynı anda değiştirdiği için çakışma olmamasını sağlar. Transfer emri gönderildikten sonra gelen mağaza veya ambarda değişiklik gerekiyorsa çıkış sevkiyatıyla iletişim kurulması ve değişiklikleri girmeleri istenir.

Belge **istenen** duruma girdikten sonra, çıkış ambarı tarafından işlem için yerine getirilmesi hazırdır. Sevkiyat giden operasyonu kullanılarak işlenirken, Transfer emri belgelerinin durumu **talep edilen** **tamamıyla sevk edilen** veya **kısmen sevk edilen** durumuna göre güncelleştirilir. Belgeler **tam olarak sevk edilen** veya **kısmen sevk edildi** durumunda ise, gelen mağaza veya ambar gelen operasyon alma sürecini kullanarak kendilerine giriş yapabilir.

Tam olarak sevk edilen transfer emirleri, **giden operasyon** belgesi listesinin **tam** sekmesine kopyalanır. Burada, giden mağaza veya ambardaki kullanıcılar, salt okunur modda yedi gün süreyle görünür durumda kalırlar.

## <a name="related-topics"></a>İlgili konular

[POS'ta gelen stok işlemi](pos-inbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]