---
title: Kalite denetimi
description: Bu konuda, Kalite denetimi özelliğiyle ilgili bilgiler verilir. Bu özellik, ambar çalışanlarının kalemleri giriş noktası alanına alırken kalite açısından hızlı bir şekilde denetlemesine olanak tanır.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dfb71f74732d65409003c4f6f74145442a1efa3f
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439696"
---
# <a name="quality-check"></a>Kalite denetimi

[!include [banner](../includes/banner.md)]

*Kalite denetimi* özelliği, ambar çalışanlarının kalemleri giriş noktası alanına alırken kalite açısından hızlı bir şekilde denetlemesine olanak tanır. Bu rastgele denetimler, çalışanlar ambalajı veya bir öğenin kolayca tanınabilen bölümlerini denetlediğinde yararlıdır. Özellik, çalışanların stoku yerine koyma konumuna yerleştirmeden önce hatalı veya hasarlı olup olmadığını görmesini sağlamak amacıyla hızlı bir şekilde kontrol etmesini sağlar.

Bu özellik standart kalite denetimi işleminin bir alternatifidir. Daha fazla esneklik ve daha hızlı işlem sunar.

Bu özelliği kullandığınızda, varış ve kalite denetimi aşağıdaki şekilde gerçekleştirilir:

1. Bir sevkiyat geldiğinde, bir ambar çalışanı varış kaydını yapar. Çalışan aynı zamanda, konumu kaydetmek için plakayı tarar.
1. Çalışan hızlı bir kalite denetimi yapar ve bu plaka için sonuçları (başarılı veya başarısız) kaydeder.
1. Aşağıdaki eylemlerden biri gerçekleşir:

    - Plaka kalite denetiminden geçerse kabul edilir ve her zamanki gibi bir teslim alma konumuna yönlendirilir.
    - Kalite denetimi başarısız olursa, plaka reddedilir ve bu plaka için varolan yerine koyma işi, daha fazla inceleme için alternatif bir konuma yönlendirilir. Yeni bir kalite emri oluşturulur. Başarısız olan kalite denetiminden oluşturulan kalite emrini görüntülemek için **Stok Yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.

Bu işlem, taranan tüm plakaların hemen kalite denetimi konumuna yönlendirilmesi için de ayarlanabilir.

## <a name="turn-on-the-quality-check-feature"></a>Kalite denetimi özelliğini açma

*Kalite denetimi* özelliğini kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Kalite denetimi*

## <a name="set-up-the-feature-for-the-example-scenario"></a>Örnek senaryo için özelliği ayarlama

Bu bölümde, *Kalite denetimi* özelliğinin nasıl ayarlanacağı ve bu konunun ilerleyen kısımlarında sağlanan örnek senaryo için örnek verilerin nasıl hazırlanacağı gösterilmektedir.

### <a name="make-sample-data-available"></a>Örnek verilerini kullanılabilir hale getirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak [örnek senaryo](#example-scenario) üzerinden çalışmak için standart [demo verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

### <a name="quality-check-template"></a><a name="quality-template"></a>Kalite denetimi şablonu

Kalite denetimi şablonu, teslim alma sırasında kalite için hızlı rastgele denetim kurallarını tanımlar.

1. **Ambar yönetimi \> Kurulum \> İş \> Kalite denetimi şablonu**'na gidin.
1. Kılavuza şablon eklemek için **Yeni**'yi seçin.
1. Yeni şabonu tanımlamak için aşağıdaki değerleri ayarlayın:

    - **Kalite denetim şablonu adı:** *Giriş noktası denetimi*

        Bu şablon için geçerli olan ilkeleri tanımlayan bir ad girin.

    - **Kabul ilkesi:** *Kullanıcıya sor*

        Kullanıcılara, işi işlerken stok kalitesini kabul etmeleri veya reddetmeleri için istemde bulunulup bulunulmayacağını ya da kalitenin otomatik reddedilip edilmeyeceğini belirtin. Kullanılabilir seçenekler *Otomatik olarak reddet* ve *Kullanıcıya sor* şeklindedir.

    - **Kalite işleme ilkesi:** *Kalite emri oluştur*

        Stok kalitesini reddederken kullanılacak ilkeyi seçin. Aşağıdaki seçenekler bulunur:

        - *Yalnızca iş oluştur* – Yalnızca stok hareketlerini kolaylaştırmak için iş oluşturun.
        - *Kalite emri oluştur* – Kalite testlerini kolaylaştırmak için bir kalite emri oluşturun.

    - **Test grubu:** *Kutu*

        Oluşturulan kalite emrinde kullanılacak test grubunu belirtin. Test grupları **Stok yönetimi** modülünde ayarlanır.

        Test grubu için **Bozma metni** seçeneğini kapalı bırakın. Bu seçenek, test grubu içindeki testler kapsamında örneklerin imha edilip edilmeyeceğini tanımlar. Bozucu bir test kullanılırsa bir kalem için kalite emri oluşturulduğunda sistem bir stok hareketi oluşturur. Yeni stok hareketi test miktar için stok azaltması öngörür. Kalite emri doğrulama adımı yoluyla tamamlandığında stok azaltma işlemi gerçekleşir. Stok hareketi kalite emri olarak tanımlanır.

### <a name="work-class--quality-check"></a><a name="work-class"></a>İş sınıfı – Kalite denetimi

İş sınıfları, ambar çalışanları tarafından bir mobil cihazda işlenebilecek iş emri satırlarının türünü yönetmek ve/veya sınırlamak için kullanılır.

1. **Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.
1. Yeni iş sınıfı oluşturmak için **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **İş sınıfı kodu:** *QC Check*

        İş sınıfını tanımlayan bir ad girin.

    - **Açıklama:** *QC Check*

        İş sınıfının ne için kullanıldığını gösteren kısa bir açıklama girin.

    - **İş emri türü:** *Kalite denetiminde kalite*

        İş sınıfı tarafından oluşturulan iş emri türünü seçin. Kalite denetimi işi ayarladığınızda, her zaman *Kalite denetiminde kalite*'yi seçin.

1. **Geçerli yerine koyma konumu türleri** hızlı sekmesinde, **Konum türü** alanını boş bırakın.

    Bir konum türü seçerseniz kalemler çekildikten sonra koyulacakları konumları sınırlamış olursunuz. Bu alan, konum yönergesi konumu çözümlemeye çalışırken ya da bir ambar çalışanı el ile mobil cihaz menü öğesi konumunu belirtirken kullanılır.

İş sınıfları ve bunların nasıl oluşturulacağı hakkında daha fazla bilgi için bkz. [İş sınıfı oluşturma](tasks/create-work-class.md).

### <a name="work-template"></a>İş şablonu

İş şablonları, ambarda gerçekleştirilmesi gereken iş operasyonlarını tanımlamanıza olanak sağlar. Genellikle, ambar iş operasyonları bir eylemler çiftinden oluşur: Bir ambar çalışanı eldeki stoku bir konumdan çeker ve çekilen stoku başka bir konuma indirir. Kalite denetimi için iş şablonu, kalite denetimleri yapmaya yönelik iş işlemlerini tanımlar.

#### <a name="purchase-orders"></a>Satın alma siparişleri

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. Başlıkta, **İş emri türü** alanını *Satın alma siparişi* olarak ayarlayın.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. Kalite denetimi adımı içerecek bir iş şablonu seçin. **Genel bakış** bölümünde, **İş şablonu** alanında, *51 SAS Girişi* öğesini seçin.
1. **İş şablonu ayrıntıları** bölümünde, kılavuzun mevcut iki satırı olduğuna dikkat edin: *Malzeme çekme* için bir ve *Yerine koyma* için bir adet.
1. **İş şablonu ayrıntıları** bölümünde, kılavuza kalite denetimi satırı eklemek için **Yeni**'yi seçin. Yeni satır için **Satır numarası** alanının *3* olarak ayarlandığına dikkat edin.
1. Yeni satırda aşağıdaki değerleri ayarlayın. Kalan alanlar için varsayılan değerleri kabul edin.

    - **İş türü:** *Kalite denetimi*
    - **İş sınıfı kodu:** *Purchase*
    - **Kalite denetim şablonu adı:** *Giriş noktası denetimi*

        İş sınıfı için benzersiz kimlik seçin. Mobil cihazdaki menü öğelerini ve bu menü öğelerinin işleyebildiği iş türlerini konfigüre etmek için bu değeri kullanın.

1. Eylem Bölmesinde, şimdiye kadarki çalışmanızı kaydetmek için **Kaydet**'i seçin.

    "Geçersiz - Kalite denetiminin malzeme çekme işleminden hemen sonra gelmesi gerekir" şeklinde bir bilgi iletisi alırsınız. Bu nedenle, az önce eklediğiniz satırın **Satır numarası** değerini değiştirmeniz gerekir.

1. Yeni satırın **Satır numarası** değerini değiştirmek için şu adımları izleyin:

    1. **İş şablonu ayrıntıları** bölümünde, **İş türü** alanının *Kalite denetimi* olarak ayarlandığı satırı seçin.
    2. *Kalite denetimi* satırını *Malzeme çekme* satırından sonra olacak şekilde taşımak için **Yukarı taşı** veya **Aşağı taşı** düğmesini seçin.

1. Eylem bölmesinde, **Kaydet**'i seçin.

#### <a name="quality-in-quality-check"></a>Kalite denetiminde kalite

Daha sonra, kalite denetimi için bir iş şablonu oluşturun.

1. **İş şablonları** sayfasının başlığında, **İş emri türü** alanının değerini *Kalite denetiminde kalite* olarak değiştirin.
1. Eylem Bölmesinde, **Genel bakış** bölümünde kılavuzuna satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **İş şablonu:** *51 Kalite Denetimi*

        Şablon için bir ad girin.

    - **İş şablonu açıklaması:** *51 Kalite Denetimi*

1. Eylem Bölmesinde, **İş şablonu ayrıntıları** bölümünü kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. Yeni şablon **Genel bakış** bölümünde hala seçiliyken, kılavuza bir satır eklemek için **İş şablonu ayrıntıları** bölümünde **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Çekme*
    - **İş sınıfı kodu:** *QC Check*

        Kalite denetimi işi için daha önce oluşturduğunuz [iş sınıfının](#work-class) adını seçin.

1. **İş şablonu ayrıntıları** bölümünde, başka bir satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Yerine koyma*
    - **İş sınıfı kodu:** *QC Check*

        Kalite denetimi işi için daha önce oluşturduğunuz [iş sınıfının](#work-class) adını seçin.

1. Eylem bölmesinde, **Kaydet**'i seçin.

İş şablonları hakkında daha fazla bilgi için bkz. [İş şablonları ve konum yönergelerini kullanarak ambar işini denetleme](control-warehouse-location-directives.md)

### <a name="location-directive--quality-failures"></a>Konum yönergesi – Kalite başarısızlıkları

Konum yönergeleri stok hareketi için çekme ve indirme konumlarını belirlemeye yardımcı olan kurallardır. Örneğin, bir satış siparişi hareketinde, kalemlerin nereden çekileceğini ve nereye indirileceğini bir konum yönergesi belirler. Başarısız kalite denetimlerinin nasıl işleneceğini tanımlamak için bir konum yönergesi kuralı yapılandırmalısınız.

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. Sol bölmede, **İş emri türü** alanını, ilgili türdeki konum yönergeleriyle çalışacak şekilde *Satın alma siparişleri* olarak ayarlayın.
1. Eylem Bölmesinde, kalite denetimleri için konum yönergesi oluşturmak üzere **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** Varsayılan değeri kabul edin.
    - **Ad:** *51 Kalite*

1. **Yerleşim yönergeleri** hızlı sekmesinde aşağıdaki değerleri ayarlayın. Kalan alanlar için varsayılan değerleri kabul edin.

    - **İş türü:** *Yerine koyma*
    - **Tesis:** *5*
    - **Ambar:** *51*

1. Eylem Bölmesinde, **Kaydet**'i seçerek yönergenizi kaydedin ve **Satırlar** hızlı sekmesini kullanılabilir hale getirin.
1. **Satırlar** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın. Kalan alanlar için varsayılan değerleri kabul edin.

    - **Başlangıç miktarı:** *1*
    - **Son miktar:** *1000000*

1. Eylem Bölmesinde, **Kaydet**'i seçerek yeni satırı kaydedin ve **Konum yönergesi eylemleri** hızlı sekmesini kullanılabilir hale getirin.
1. Yeni satır **Satırlar** hızlı sekmesinde seçili durumdayken, kılavuza bir satır eklemek için **Konum yönergesi eylemleri** hızlı sekmesinde **Yeni**'yi seçin; böylece satır için bir eylem ayarlayabilirsiniz.
1. Yeni satırda, **Ad** alanını *Kalite* olarak ayarlayın. Kalan alanlar için varsayılan değerleri kabul edin.
1. **Konum yönergesi eylemleri** hızlı sekmesinde **Sorguyu düzenle** düğmesini kullanılabilir hale getirmek için Eylem Bölmesindeki **Kaydet**'i seçin.
1. Yeni eklediğiniz satır **Konum yönergesi eylemleri** hızlı sekmesinde seçiliyken, eylem sorgusunu düzenleyebileceğiniz bir iletişim kutusu açmak için **Sorguyu düzenle**'yi seçin.
1. **Aralık** sekmesinde, sorguya satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** *Yerleşimler*
    - **Türetilmiş tablo:** *Yerleşimler*
    - **Alan:** *Yerleşim*
    - **Ölçüt:** *QMS*

    *QMS* konumu, kalite için bir ambar konumudur.

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Ambar *51* için satın alma siparişi konum yönergelerinin sırasını değiştirmeniz gerekir. Kalite konumu yönergesine yeni *51 Kalite* konumu kaydedin, sayfayı yenileyin ve listeden konum yönergesini seçin. Sonra, ambar *51* için konum yönergesini aşağıdaki sıraya koymak için Eylem Bölmesindeki **Yukarı taşı** ve **Aşağı taşı** düğmelerini kullanın. (**Yukarı taşı** veya **Aşağı taşı** düğmelerini seçmeden önce listeden bir konum yönergesi seçmelisiniz.)

    1. 51 Kalite
    2. 51 SAS Doğrudan
    3. 51 QMS

### <a name="mobile-device-menu-items"></a>Mobil cihaz menü öğeleri

Mobil cihazların **Kalite Denetimi** işlevini gerçekleştirebilmesi için bir menü öğesini yapılandırın.

#### <a name="purchase-putaway"></a>Satın alma yerine koyma

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Listeden, **Satın alma yerine koyma** menü öğesini seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **İş sınıfları** bölümünde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **İş sınıfı kodu:** *QC Check*

        Kalite denetimi işi için daha önce oluşturduğunuz [iş sınıfının](#work-class) adını girin.

    - **İş emri türü:** *Kalite denetiminde kalite*

1. Eylem bölmesinde, **Kaydet**'i seçin.

#### <a name="purchase-order-line-receiving"></a>Satınalma siparişi satırı teslim alma

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Menü madde adı:** *Satınalma siparişi satın alma*
    - **Başlık:** *Satınalma siparişi satın alma*
    - **Mod:** *İş*
    - **Varolan çalışmayı kullan:** *Hayır*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın. Kalan alanlar için varsayılan değerleri kabul edin.

    - **İş oluşturma işlemi:** *Satın alma siparişi satırı teslim alma ve yerine koyma*
    - **Plaka oluştur:** *Evet*
    - **İş şablonu:** *51 SAS Girişi*

1. Eylem bölmesinde, **Kaydet**'i seçin.

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Mobil cihaz menüsüne menü öğesi ekleme

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.
1. Sol bölmede, **Gelen** menüsünü seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Mevcut menüler ve menü öğeleri** sütununda, yeni **SAS satırı alma** menüsü öğesini bulup seçin.
1. **SAS satırı alma**'yı **Menü yapısı** sütununa taşımak için sağ ok düğmesini seçin.
1. **Menü yapısı** sütununda, **SAS satırı alma**'yı seçin ve ardından menü öğesini mobil cihaz menüsünde istediğiniz konuma taşımak için yukarı ok veya aşağı ok düğmesini seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="example-scenario"></a><a name="example-scenario"></a>Örnek senaryo

Daha önce açıklanan örnek verilerin tümünü kullanılabilir hale getirip ayarladıktan sonra, bu senaryoda, *Kalite denetimi* özelliğini deneyebilirsiniz. Bu senaryoda gösterilen değerler, standart demo verileriyle çalıştığınızı, **USMF** tüzel kişiliğini seçmiş olduğunuzu ve bu konunun önceki bölümlerinde açıklanan örnek kayıtları hazırladığınızı varsayar. Bu senaryo aynı zamanda özelliğin bir üretim ayarında nasıl kullanılabileceğini gösteren bir örnek işlevi de görür.

### <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma

1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Satıcı hesabı:** *104*
    - **Ambar:** *51*

1. İletişim kutusunu kapatmak ve yeni satın alma siparişini açmak için **Tamam**'ı seçin.
1. **Satın alma siparişi satırları** hızlı sekmesine, kılavuzda yeni, boş bir satır bulunur. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *M9203*
    - **Miktar:** *3*
    - **Birim:** *PL*

1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="process-quality-check-receiving"></a>İşlem kalite denetimi alma

Satın alma siparişi oluşturulduktan sonra, **SAS satırı teslim alma** menü öğesi ve *Kalite denetimi* özelliğinin işlevleri kullanılarak teslim edilebilir.

#### <a name="receive-pallet-1"></a>Palet 1'i alma

1. Ambar uygulamasında ambar *51*'deki bir kullanıcı olarak oturum açın. (Kullanıcı kimliği olarak *51*, parola olarak *1* girin.)
1. **Gelen \> SAS satırı teslim alma** bölümüne gidin.
1. **PONUM** alanına satın alma siparişi numaranızı girin.
1. Satın alma siparişi numarasını doğrulayın.
1. **LINENUM** alanına, alınmakta olan satın alma siparişinin numarasını girin. Bu senaryoda siparişin yalnızca bir satırı bulunduğundan, her teslim alma alma adımı için **LINENUM** alanına *1* girin.
1. Satır numarasını onaylayın.
1. **Miktar** alanına teslim alınacak miktarı girin. Bu senaryoda satın alma siparişi üç palet (*PL*) için olduğundan ve üç teslim alma adımı olduğundan her teslim alma adımı için **Miktar** alanına *1* girin.
1. Onaylanan miktar.

    Açılan **Kalite denetimi** sayfasında hiç giriş alanı yok. Yalnızca en altta bulunan onay (onay işareti) düğmesi ve en üstteki Menü düğmesi (**≡**) var. (Menü düğmesine bazen hamburger veya hamburger düğmesi denir.) Kalite denetimi işlemini hızlandırmak için palet kalite denetimini geçtiğinde kullanıcının yalnızca **Kalite denetimi** sayfasını onaylaması yeterlidir.

    ![Kalite denetimi sayfası](media/quality-check.png "Kalite denetimi sayfası")

1. Palet1'i kalite denetimini geçirmek için satır 1'den onay düğmesini seçin.

    Açılan **Satın alma siparişleri: Yerine koyma** sayfası, yerine koyma işinin ayrıntılarını gösterir:

    - **KONUM:** Sistem tarafından belirlenen konum

        Bu konum, satın alma siparişi teslim alma için belirlenmiş yerine koyma konumudur.

    - **LP:** Sistem tarafından oluşturulan plaka kimliği
    - **Madde:** *M9203*
    - **Miktar:** *1 PL: 100 beher*

    Kalem açıklaması da gösterilir.

1. Yerine koyma işini onaylayın.

    Satın alma siparişi satırı teslim alma **Görev** sayfasında, "İş Tamamlanadı" iletisi alırsınız. Bir sonraki paleti almaya başlamak için **LINENUM** alanı kullanılabilir.

#### <a name="receive-pallet-2"></a>Palet 2'yi alma

Bu senaryo için palet 2 reddedilecektir.

1. **LINENUM** alanına *1* girip satır numarasını onaylayın.
1. **Miktar** alanı artık kullanılabilirdir. *1* girin ve miktarı onaylayın.

    **Kalite denetimi** sayfası görüntülenir. Bu giriş için palet, kalite açısından reddedilecek ve *QMS* kalite konumuna yerleştirilecek.

1. Sayfanın üst kısmındaki Menü düğmesini (**≡**) seçin ve ardından menüden **Reddet**'i seçin.
1. Görüntülenen **Görev** sayfasında, paletin daha fazla inceleme için gönderileceği *Yerine koyma* konumu konumu olarak **QMS** girin.

    Açılan **Kalite denetiminde kalite: Yerine koyma** sayfası, yerine koyma işinin ayrıntılarını gösterir:

    - **KONUM:** *QMS*

        Bu konum, reddedilen kalite teslim alma için belirlenmiş yerine koyma konumudur.

    - **LP:** Sistem tarafından oluşturulan plaka kimliği
    - **Madde:** *M9203*
    - **Miktar:** *1 PL: 100 beher*

    Kalem açıklaması da gösterilir.

1. Yerine koyma işini onaylayın.

    Satın alma siparişi satırı teslim alma **Görev** sayfasında, "İş Tamamlanadı" iletisi alırsınız. Bir sonraki paleti almaya başlamak için **LINENUM** alanı kullanılabilir.

Kalite denetimini tamamladınız ve reddedilmiş palet için bir kalite emri oluşturdunuz. Oluşturulan emri görüntülemek için **Stok Yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.

Kalite emri testleri artık işlenebilir. Kalite testi bu konuda ele alınmamaktadır.

Kalite yönetimi hakkında daha fazla bilgi için bkz. [Kalite yönetimine genel bakış](../inventory/enable-quality-management.md)

#### <a name="receive-pallet-3"></a>Palet 3'ü alma

Bu senaryo için palet 3 kabul edilecektir.

1. **LINENUM** alanına *1* girip satır numarasını onaylayın.
1. **Miktar** alanı artık kullanılabilirdir. *1* girin ve miktarı onaylayın.

    **Kalite denetimi** sayfası görüntülenir. Bu giriş için palet, kalite açısından kabul edilecek ve toplu yerine koyma konumuna yerleştirilecek.

1. Kalite denetiminden geçirmek için onay düğmesini seçin.

    Açılan **Satın alma siparişleri: Yerine koyma** sayfası, yerine koyma işinin ayrıntılarını gösterir:

    - **KONUM:** Sistem tarafından belirlenen konum

        Bu konum, satın alma siparişi teslim alma için belirlenmiş yerine koyma konumudur.

    - **LP:** Sistem tarafından oluşturulan plaka kimliği
    - **Madde:** *M9203*
    - **Miktar:** *1 PL: 100 beher*

    Kalem açıklaması da gösterilir.

1. Yerine koyma işini onaylayın.

    Satın alma siparişi satırı teslim alma **Görev** sayfasında, "İş Tamamlanadı" iletisi alırsınız. Bir sonraki paleti almaya başlamak için **LINENUM** alanı kullanılabilir.

1. Sayfanın üst kısmındaki Menü düğmesini (**≡**) seçin ve ardından menüden **İptal**'i seçerek menüye dönün.

Artık mobil uygulamayı kapatabilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]