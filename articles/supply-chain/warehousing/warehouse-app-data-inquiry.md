---
title: Warehouse Management mobil uygulaması sapmalarını kullanarak verileri sorgulama
description: Bu makalede, veri sorgulama mobil cihaz menü öğelerinin nasıl yapılandırılacağı ve sapmaların bir parçası olarak nasıl kullanılacağı açıklanır.
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cc013e962b4da803764f16e451b1d433666e75c2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336620"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Warehouse Management mobil uygulaması sapmalarını kullanarak verileri sorgulama

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Özelliğe giriş

Warehouse Management mobil uygulaması, barkod tarama yeteneği sağlayarak size ambar süreçlerinizin bir parçası olarak veri yakalamak için kolay ve doğru bir yol sağlar. Ancak, barkodlar bazen hasar görür ve okunamaz hale gelir veya gerekli veri bilgileri iş süreci akışlarınızda bir barkod olarak mevcut olmayabilir. Bu durumlarda, verilerin el ile girilmesi uzun sürebilir ve hatalı verilerin yakalanmasına bile neden olabilir. Sonuç olarak etkililik ve servis düzeyi düşebilir.

Çalışanlar esnek bir veri sorgulama işlemi kullanarak, katıştırılmış Warehouse Management mobil uygulama akışlarının bir parçası olarak gerekli bilgileri kolayca arayabilir ve yalnızca ilgili verilerin gösterilmesi için filtre seçeneklerini uygulayabilir. Bu nedenle, el ile seçim daha hızlı ve daha doğrudur.

Örneğin, satın alma siparişi teslim alma akışında, gelen stokla eşleşmesi için bir satınalma siparişi numarası gereklidir. Bu işlemin bir parçası olarak, menü öğelerini, ilgili satınalma siparişi numaralarının kart listesi görünümünü sağlayacak şekilde kolayca yapılandırabilirsiniz. Bu şekilde, seçmek için üzerine git hızlı yaklaşımını kullanarak alma akışını devam ettirebilirsiniz. Bu makalede örnek senaryolar sağlanır, ancak işlevler tüm Warehouse Management mobil uygulama akışlarınız içinde de kullanılabilir.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>Veri sorgulama akışı özelliğini açma ve özelliğin önkoşulları

Bu makalede açıklanan işlevleri kullanabilmeniz için, gerekli özellikleri etkinleştirmek üzere aşağıdaki yordamı tamamlamanız gerekir.

1. **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin. (**Özellik yönetimi** çalışma alanını kullanma hakkında daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Supply Chain Management 10.0.28 veya öncesi bir sürümü kullanıyorsanız listelenen özelliği aşağıdaki şekilde açın:

    - **Modül:** *Ambar yönetimi*
    - **Özellik adı:** *Ambar uygulaması adım yönergeleri*

    Bu özellik, *Warehouse Management uygulaması veri sorgusu akışı* özelliği için bir önkoşuldur. Supply Chain Management 10.0.29 sürümü itibarıyla zorunludur ve kapatılamaz. *Ambar uygulaması adım yönergeleri* özelliği hakkında daha fazla bilgi için , [Warehouse Management mobil uygulaması ile ilgili adım başlıklarını ve yönergeleri özelleştirme](mobile-app-titles-instructions.md) konusuna bakın.

1. Özelliği, aşağıdaki şekilde açın:

    - **Modül:** *Ambar yönetimi*
    - **Özellik adı:** *Warehouse Management uygulama sapmaları*

    Bu özellik, *Warehouse Management uygulaması veri sorgusu akışı* özelliği için bir önkoşuldur. Supply Chain Management sürüm 10.0.29 itibariyle, varsayılan olarak açıktır. *Warehouse Management uygulama sapmaları* özelliği hakkında daha fazla bilgi için bkz. [Mobil aygıt menü öğelerindeki adımlar için sapmaları yapılandırma](warehouse-app-detours.md).

1. *Warehouse Management uygulama sapmaları* özelliği zaten açık değilse **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Ambar uygulaması alan adları**'na gidip **Varsayılan kurulum oluştur**'u seçerek Warehouse Management mobil uygulamasında alan adlarını güncelleştirin. Warehouse Management mobil uygulamasını kullandığınız her yasal varlık (şirket) için bu adımı yineleyin. - Daha fazla bilgi için bkz. [Ambar Yönetimi mobil uygulaması için alanları yapılandırma](configure-app-field-names-priorities-warehouse.md).
1. Özelliği, aşağıdaki şekilde açın:

    - **Modül:** *Ambar yönetimi*
    - **Özellik adı:** *Warehouse Management uygulaması veri sorgusu akışı*

    Bu özellik, bu makalede açıklanan özelliktir.

## <a name="example-scenarios"></a>Örnek senaryolar

Bu makalede, satınalma girişi akışını iyileştirmek üzere *Warehouse management uygulaması veri sorgulama akışı* özelliğini nasıl kullanabileceğinizi göstermek için örnek senaryolar kullanılmıştır. Senaryolar, *Satın alma teslim alma* adı verilen bir akışı içeren standart örnek verileri kullanır. Bu akış, çalışanların hangi satın alma siparişi numarasına göre teslim alacaklarını tanımlamalarını isteyerek başlar. Çalışanların satın alma siparişini daha kolay belirlemesine yardımcı olmak için, aşağıdaki yeni sorgu seçeneklerini [sapma](warehouse-app-detours.md) olarak ekleyerek akışın ilk sayfasını geliştirebilirsiniz:

- **Satıcıya göre PO ara** – Çalışanların satıcı adı veya satıcı adının bir bölümünü girmesini isteyen bir sayfa açar. Joker karakterler kullanılabilir. Örneğin bir çalışan, adında *Tailspin* içeren bir satıcıdan bugün gelecek bir teslimat bekliyorsa, bu metni içeren açık satınalma siparişleri için bir dizi kartı görüntülemek üzere **Tail\*** ifadesini girebilir. Her kartta her satınalma siparişi hakkında bilgi sağlayan çeşitli alanlar vardır. Satıcı adının yanı sıra, kartları satıcı hesap numarasını, teslimat tarihini ve belge durumunu gösterecek şekilde tasarlayabilirsiniz.
- **Bugünün PO'larını ara** – Çalışanların veri girmesini istemeyen ancak bunun yerine önceden yapılandırılmış filtreleri gösteren (bugünün tarihi gibi) bir sayfa açar. Böylece sayfa, filtreyle eşleşen bir dizi kart gösterir. Çalışanlar, stok maddelerini kaydetmek istedikleri satınalma siparişi için bir kart seçerek devam eder.
- **PO'ları maddeye göre ara** Çalışanların gelen stokta bulunan bir maddenin barkodunu taramasını isteyen bir sayfa açar. Böylece akış, taranan madde numarasının satırlarını içeren tüm açık satınalma siparişlerini listeler. Bir barkodun okunamadığı durumları kapsamak için bu sayfaya, çalışanların belirli bir satın alma siparişi içinde madde numaraları aramasına izin veren başka bir sapma araması ekleyebilirsiniz.

Her durumda çalışan, bir kart seçip bir satınalma siparişini tanımlar ve ardından seçilen satınalma siparişi numarasını gösteren ilk sayfaya geri döndürülür. Çalışan, gelen stok madde kaydı akışına devam edebilir.

## <a name="enable-sample-data"></a>Örnek verileri etkinleştirme

Bu makalede açıklanan örnek senaryolarla çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce *USMF* tüzel kişiliğini (şirket) seçmeniz gerekir.

## <a name="configure-the-mobile-device-menu-items"></a>Mobil cihaz menü öğelerini yapılandırma

Akışın ilk sayfasına eklemek zorunda olduğunuz yeni sorgu seçeneklerinin her birini oluşturmak için, bunları mobil aygıt menü öğesi olarak ayarlamalısınız. Daha sonra, sorgu seçeneklerini *Satın alma teslim alma* akışında sapma olarak kullanılabilir hale getirirsiniz.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>"Satıcıya göre PO ara" menü öğesini oluşturma

Aşağıdaki adımları izleyerek, **Satıcıya göre PO ara** menü öğesini oluşturun.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem bölmesinde, mobil cihaz menü öğesi eklemek için **Yeni**'yi seçin.
1. Yeni menü öğesinde aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Satıcıya göre PO ara*
    - **Başlık:** *Satıcıya göre PO ara*
    - **Mod:** *Dolaylı*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Faaliyet kodu:** *Veri sorgulama*
    - **İşlem kılavuzunu kullan:** *Evet* (Bu değer otomatik olarak seçilir.)
    - **Tablo adı:** *PurchTable* (Bu tablodan satınalma siparişi numaralarını aramak istiyorsunuz.)

1. Eylem bölmesinde, seçili temel tabloyu temel alan bir sorgu tanımlamak için (bu örnekte, satınalma siparişleri tablosu) **Sorguyu düzenle**'yi seçin.
1. Sorgu düzenleyicisinde, **Aralık** sekmesinde, kılavuza aşağıdaki satırları ekleyin.

    | Tablo | Türetilen tablo | Alan | Ölçütler |
    |---|---|---|---|
    | Satın alma siparişleri | Satın alma siparişleri | Satınalma siparişi durumu | Açık sipariş |
    | Satın alma siparişleri | Satın alma siparişleri | Teslimat tarihi | (dayRange(-10,10)) |
    | Satın alma siparişleri | Satın alma siparişleri | Satıcı adı | |

1. **Tamam**'ı seçin.

    Bu örnekte, yeni menü öğesi, geçmiş 10 gün ile sonraki 10 gün arasında varması beklenen açık satınalma siparişlerini bulmak için yapılandırılmıştır.

    Sorguda, **Satıcı adı** için *Ölçüt* sütunu boş bırakılmıştır. Böylece çalışanlar, Warehouse Management mobil uygulamasını kullanırken bu değeri belirtebilecektir.

    Listenin nasıl sıralanacağını belirtmek istiyorsanız, sıralamayı **Sıralama** sekmesinde ayarlayabilirsiniz.

1. Sorguyu tanımlamanın yanı sıra, sorgulama listesi sayfasındaki kartlar üzerinde hangi alanların gösterileceğini de seçmeniz gerekir. Bu nedenle, Eylem Bölmesinde **Alan listesi** öğesini seçin.
1. **Alan listesi** sayfasında, aşağıdaki değerleri ayarlayın:

    - **Görüntüleme alanı 1:** *PurchId* (Bu alan her bir kartın başlığı olarak gösterilir.)
    - **Görüntüleme alanı 2:** *PurchStatus*
    - **Görüntüleme alanı 3:** *PurchName*
    - **Görüntüleme alanı 4:** *OrderAccount*
    - **Görüntüleme alanı 5:** *DeliveryDate*
    - **Görüntüleme alanı 6:** *displayDocumentStatus()* (Bu değer, sondaki "()" işaretinin belirttiği üzere bir görüntüleme yöntemidir.)

1. Eylem bölmesinde, **Kaydet**'i seçin. Ardından sayfayı kapatın.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>"Bugünün PO'larını ara" menü öğesini oluşturma

Aşağıdaki adımları izleyerek, **Bugünün PO'larını ara** menü öğesini oluşturun.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem bölmesinde, mobil cihaz menü öğesi eklemek için **Yeni**'yi seçin.
1. Yeni öğe için aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Bugünün PO'larını ara*
    - **Başlık:** *Bugünün PO'larını ara*
    - **Mod:** *Dolaylı*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Faaliyet kodu:** *Veri sorgulama*
    - **İşlem kılavuzunu kullan:** *Evet* (Bu değer otomatik olarak seçilir.)
    - **Tablo adı:** *PurchTable* (Bu tablodan satınalma siparişi numaralarını aramak istiyorsunuz.)

1. Eylem bölmesinde, seçili temel tabloyu temel alan bir sorgu tanımlamak için (bu örnekte, satınalma siparişleri tablosu) **Sorguyu düzenle**'yi seçin.
1. Sorgu düzenleyicisinde, **Aralık** sekmesinde, kılavuza aşağıdaki satırları ekleyin.

    | Tablo | Türetilen tablo | Alan | Ölçütler |
    |---|---|---|---|
    | Satın alma siparişi | Satın alma siparişi | Satınalma siparişi durumu | Açık sipariş |
    | Satın alma siparişi | Satın alma siparişi | Teslimat tarihi | (Day(0)) |

1. **Tamam**'ı seçin.

    Bu örnekte, yeni menü öğesi bugün gelmesi beklenen açık satınalma siparişlerini bulmak için yapılandırılır.

    Listenin nasıl sıralanacağını belirtmek istiyorsanız, sıralamayı **Sıralama** sekmesinde ayarlayabilirsiniz.

1. Sorguyu tanımlamanın yanı sıra, sorgulama listesi sayfasındaki kartlar üzerinde hangi alanların gösterileceğini de seçmeniz gerekir. Bu nedenle, Eylem Bölmesinde **Alan listesi** öğesini seçin.
1. **Alan listesi** sayfasında, aşağıdaki değerleri ayarlayın:

    - **Görüntüleme alanı 1:** *PurchName* (Bu alan her bir kartın başlığı olarak gösterilir.)
    - **Görüntüleme alanı 2:** *PurchName*
    - **Görüntüleme alanı 3:** *PurchStatus*
    - **Görüntüleme alanı 4:** *DlvMode*
    - **Görüntüleme alanı 5:** *DlvTerm*
    - **Görüntüleme alanı 6:** *OrderAccount*
    - **Görüntüleme alanı 7:** *VendorName()* (Bu değer, sondaki "()" işaretinin belirttiği üzere bir görüntüleme yöntemidir.)

1. Eylem bölmesinde, **Kaydet**'i seçin. Ardından sayfayı kapatın.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>"Öğeye göre PO ara" menü öğesini oluşturma

Aşağıdaki adımları izleyerek, **Öğeye göre PO ara** menü öğesini oluşturun.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem bölmesinde, mobil cihaz menü öğesi eklemek için **Yeni**'yi seçin.
1. Yeni öğe için aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Öğeye göre PO ara*
    - **Başlık:** *Öğeye göre PO ara*
    - **Mod:** *Dolaylı*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Faaliyet kodu:** *Veri sorgulama*
    - **İşlem kılavuzunu kullan:** *Evet* (Bu değer otomatik olarak seçilir.)
    - **Tablo adı:** *PurchLine* (Satır verileri aracılığıyla madde numarası temelinde satınalma siparişi numaraları aramak istiyorsunuz.)

1. Eylem bölmesinde, seçili temel tabloya dayalı bir sorgu tanımlamak için **Sorgu düzenle**'yi seçin (Bu örnekte, satınalma sipariş satırları tablosu, ancak *PurchTable* ile birleştirerek üstbilgiyle ilişkili değerlerden herhangi birini kullanabilirsiniz).
1. Sorgu düzenleyicisinde, **Aralık** sekmesinde, kılavuza aşağıdaki satırları ekleyin.

    | Tablo | Türetilen tablo | Alan | Ölçütler |
    |---|---|---|---|
    | Satın alma siparişi satırları | Satın alma siparişi satırları | Satır durumu | Açık sipariş |
    | Satın alma siparişi satırları | Satın alma siparişi satırları | Teslimat tarihi | (dayRange(-10,10)) |
    | Satın alma siparişi satırları | Satın alma siparişi satırları | Madde numarası | |

1. **Tamam**'ı seçin.

    Bu örnekte, yeni menü öğesi, geçmiş 10 gün ile sonraki 10 gün arasında varması beklenen açık satınalma siparişi satırlarını bulmak için yapılandırılmıştır.

    Sorguda, **Öğe numarası** için *Ölçüt* sütunu boş bırakılmıştır. Böylece çalışanlar, Warehouse Management mobil uygulamasını kullanırken bu değeri belirtebilecektir.

    Listenin nasıl sıralanacağını belirtmek istiyorsanız, sıralamayı **Sıralama** sekmesinde ayarlayabilirsiniz.

1. Sorguyu tanımlamanın yanı sıra, sorgulama listesi sayfasındaki kartlar üzerinde hangi alanların gösterileceğini de seçmeniz gerekir. Bu nedenle, Eylem Bölmesinde **Alan listesi** öğesini seçin.
1. **Alan listesi** sayfasında, aşağıdaki değerleri ayarlayın:

    - **Görüntüleme alanı 1:** *PurchId* (Bu değer her bir kartın başlığı olarak kullanılır.)
    - **Görüntüleme alanı 2:** *VendAccount*
    - **Görüntüleme alanı 3:** *PurchQty*
    - **Görüntüleme alanı 4:** *PurchUnit*
    - **Görüntüleme alanı 5:** *PurchStatus*

1. Eylem bölmesinde, **Kaydet**'i seçin. Ardından sayfayı kapatın.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>Yeni mobil cihaz menü öğelerini menüye ekleme

Üç yeni mobil cihaz menü öğesi artık mobil cihaz menüsüne eklenmek üzere hazırdır. Menü öğelerinin sapma işleminin bir parçası olarak kullanılabilmesi için bu görevin tamamlanması gerekir. Bu örnekte, yeni bir alt menü oluşturacak ve yeni menü öğelerini bu alt menüye ekleyeceksiniz.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni kaydın üst bilgisinde aşağıdaki değerleri ayarlayın:

    - **Ad:** *Sorgu*
    - **Açıklama:** *Sorgu*

1. **Kullanılabilir menüler ve menü öğeleri** listesinde, yeni oluşturduğunuz mobil cihaz menü öğelerinden ilkini seçin. Ardından, ilgili öğeyi **Menü yapısı** listesine taşımak için sağ ok düğmesini seçin.
1. Diğer iki yeni menü öğesi için önceki adımı tekrarlayın.
1. Soldaki liste bölmesinde, **Ana** menüyü seçin.
1. **Kullanılabilir menüler ve menü öğeleri** listesinde, **Menüler** bölümüne gidin ve yeni **Sorgu** menünüzü seçin. Ardından, ilgili öğeyi **Menü yapısı** listesine taşımak için sağ ok düğmesini seçin.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Mobil cihaz adımlarınızda sapmaları yapılandırma

Kurulumu tamamlamak için şimdi, üç yeni mobil cihaz menü öğesini *Satın alma teslim alma* akışındaki varolan satınalma siparişi tanımlama adımına eklemek için **Mobil cihaz adımları** sayfasındaki sapma yapılandırmasını kullanmalısınız.

1. **Ambar yönetimi \> Kurulum > Mobil cihaz \> Mobil cihaz adımları**'na gidin.
1. **Filtre** alanına, *PONum* yazın. Ardından açılan listede *Adım Kimliği: "PONum"* öğesini seçin.
1. Bulunan kayıt kılavuzda seçiliyken, eylem bölmesinde **Adım yapılandırması ekle**'yi seçin. Açılan iletişim kutusunda, **Menü öğesi** alanını *Satın Alma Teslim Alma* olarak ayarlayın. Ardından iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni adım yapılandırmasının ayrıntılar sayfasında (**Satın Alma Teslim Alma: PONum**), **Kullanılabilir sapmalar (menü öğeleri)** hızlı sekmesinde, araç çubuğundan **Ekle**'yi seçin.
1. **Sapma ekle** iletişim kutusunda, daha önce oluşturduğunuz **Satıcıya göre PO ara** menü öğesini bulup seçin.
1. İletişim kutusunu kapatmak ve seçili menü öğesini sapmalar listesine eklemek için **Tamam**'ı seçin.
1. Yeni sapmayı seçin ve ardından araç çubuğunda **Gönderilecek alanları seç**'i seçin.
1. **Gönderilecek alanları seç** iletişim kutusunda, herhangi bir veriyi sapma menü öğesine geçirmek istemediğiniz için **Satınalma teslim alma menü öğesinden gönder** bölümüne hiçbir şey eklemeyin. Ancak, **Satıcıya göre PO ara menü öğesinden geri getir** bölümünde, zaten eklenmiş olan boş satır için aşağıdaki değeri ayarlayın:

    - **Satıcıya göre PO ara menü öğesinden kopyala:** *Satınalma siparişi*
    - **Satınalma Teslim Alma menü öğesine yapıştır:** *Satınalma siparişi*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Diğer iki yeni menü öğesi için (**Bugünün PO'larını ara** ve **Öğeye göre PO ara**) 4-9 arasındaki adımları yineleyin. **Satıcıya göre PO ara** menü öğesinde olduğu gibi, bu sapmalara hiçbir veri göndermek istemez ancak bir satınalma siparişi numarası döndürmek istersiniz.
1. Sayfayı kapatın.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Sapmanın bir parçası olarak veri sorgulamasına sahip olan bir satınalma teslim alma akışı deneyin

Yeni mobil uygulama kurulumunu sınamak için aşağıdaki adımları izleyin.

1. Ambar 51 için satırları olan çeşitli satınalma siparişleri oluşturun.
1. Ambar Yönetimi mobil uygulaması çalıştıran bir mobil cihaza veya emülatöre gidin ve kullanıcı kimliği olarak *51* ve parola olarak *1* kullanarak ambar 51'de oturum açın.
1. Mobil uygulama menüsünde, **Gelen** ve **Satınalma teslim alma**'yı seçin.

    Üç yeni menü öğesini de içeren aşağıdaki sayfayı görmelisiniz.

    ![PO numarası kullanarak satın almayı teslim alma.](media/wma-purchase-receive-po-num-with-detours.png "PO numarası kullanarak satın almayı teslim alma")

1. Farklı yetenekleri deneyin ve listedeki kartlardan birini seçerek bir satın alma siparişi numarasını geri gönderin.

    ![Satıcıya göre PO aramasını kullanarak satın alma teslim alma, örnek 1.](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Satıcıya göre PO aramasını kullanarak satın alma teslim alma, örnek 1")

    ![Satıcıya göre PO aramasını kullanarak satın alma teslim alma, örnek 2.](media/wma-purchase-receive-lookup-po-vendor-detours.png "Satıcıya göre PO aramasını kullanarak satın alma teslim alma, örnek 2")

> [!TIP]
> **Satın alma teslim alma** menü öğesinden bir arama yaparak teslim alma akışını çalıştırmak yerine, bir sorgu akışından (**Ana \> Sorgu \> Satıcıya göre PO ara)** başlayabilir ve listedeki kartlardan birini seçerek istenen akışı çalıştırmak için bir sapma çağırabilirsiniz. Bu yaklaşımı kullanmak için, **Adım Kimliği** değeri *GenericDataInquiryList* olan **Mobil cihaz adımları** sayfasında bir sapma tanımlayabilirsiniz. Bu akış bir sapma akışı olduğundan, daha fazla sapma çağıramazsınız. Bu nedenle, madde numarası giriş ekranına geldiğinizde örneğin, sistem yalnızca tek bir sapma düzeyini desteklediğinden burada arama kullanılamaz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
