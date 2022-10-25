---
title: Konum yönergeleriyle çalışma
description: Bu makale, konum yönergeleriyle nasıl çalışılacağını açıklamaktadır. Yerleşim yönergeleri stok hareketi için çekme ve yerine koyma yerleşimlerini belirlemeye yardımcı olan kullanıcı tanımlı kurallardır.
author: Mirzaab
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ef8ec0732cd3bd50bca8d334c43d0354e9e3316
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689679"
---
# <a name="work-with-location-directives"></a>Konum yönergeleriyle çalışma

[!include [banner](../includes/banner.md)]

Konum yönergeleri stok hareketi için çekme ve indirme konumlarını belirlemeye yardımcı olan kurallardır. Örneğin, bir satış siparişi hareketinde, öğelerin nereden çekileceğini ve nereye indirileceğini bir konum yönergesi belirler. Konum yönergeleri bir başlıktan ve ilişkili satırlardan oluşur. Belirli *iş emri türleri* için oluşturulurlar.

> [!NOTE]
> Bu makale, **Ambar yönetimi** modülündeki özellikler için geçerlidir. [Stok yönetimi](../inventory/inventory-home-page.md) modülündeki özellikler için geçerli değildir.

Yerleşim yönergelerini şu görevleri gerçekleştirmek için kullanabilirsiniz:

- Gelen maddeleri yerine koyma.
- Giden hareketler için maddeleri çekme ve hazırlama.
- Üretim için hammadde çekme ve yerine koyma.
- Yerleşimlerde stok yenileme.

## <a name="prerequisites"></a>Önkoşullar

Bir yerleşim yönergesi oluşturmadan önce, önkoşulların karşılandığından emin olmak için aşağıdaki adımları izlemeniz gerekir.

1. Gerekli lisans anahtarının açık olduğundan emin olun. **Sistem Yönetimi \> Kurulum \> Lisansı yapılandırması**'na gidin, **Ticaret** lisansı anahtarını genişletin ve **Ambar ve Taşıma yönetimi** yapılandırma anahtarını seçin. Bu adım için yönetici erişimi gerektiğini unutmayın.
1. **Ambar yönetimi \> Kurulum \> Ambar  \> Ambarlar**'a gidin.
1. Ambar oluşturun.
1. **Ambar** hızlı sekmesinde **Ambar yönetimi işlemlerini kullan** seçeneğini *Evet* olarak ayarlayın.
1. Yerleşimler, yerleşim türleri, yerleşim profilleri ve yerleşim biçimleri oluşturun. Daha fazla bilgi için bkz. [WMS özellikli ambarda yerleşimler yapılandırma](./tasks/configure-locations-wms-enabled-warehouse.md).
1. Tesisler, bölgeler ve bölge grupları oluşturun. Daha fazla bilgi için bkz. [Ambar kurulumu](../../commerce/channels-setup-warehouse.md) ve [WMS özellikli ambarda yerleşimler yapılandırma](./tasks/configure-locations-wms-enabled-warehouse.md).

## <a name="turn-the-location-directive-scopes-feature-on-or-off"></a><a name="scopes-feature"></a>Konum yönergesi kapsamları özelliğini açma veya kapatma

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until 10.0.31 GA -->

*Konum yönergesi kapsamları* özelliği, konum yönergelerini tasarlarken size daha fazla özgürlük sağlar ve gereksiz yapılandırmaları azaltmaya yardımcı olur. Önceki **Çoklu SKU** seçeneğinin yerini alan bir **Kapsamlar** seçeneği ekler. **Çoklu SKU** seçeneği *Evet* veya *Hayır* olarak ayarlanabilirken, **Kapsamlar** seçeneği yalnızca bu iki ayarı (*Tek öğe* ve *Birden fazla öğe* değerleri aracılığıyla) değil, aynı zamanda iki ayar daha (*Tek öğe veya sipariş* ve *Tümü* değerleri yoluyla) sağlar. Bu ayarlar hakkında daha fazla bilgi için bkz. [Konum yönergeleri FastTab](#location-directives-tab).

Etkinleştirildiğinde, **Kapsam** seçeneği **Çoklu SKU** seçeneğinin yerini alır ve mevcut yapılandırmalarla %100 uyumludur.

Bu özelliği kullanmanız için sisteminizde açmanız gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek veya devre dışı bırakmak için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanında bu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Yerleşim yönergesi kapsamları*

## <a name="work-order-types-for-location-directives"></a>Konum yönergeleri için iş emri türleri

Konum yönergeleri için ayarlanabilecek alanların çoğu tüm çalışma emri türleri için ortaktır. Ancak, diğer alanlar belirli iş emri türlerine özgüdür.

![Konum yönergeleri iş emri türleri.](media/Location_Directives_Work_Order_Types.png "Konum yönergeleri iş emri türleri")

> [!NOTE]
> *İptal edilen iş* ve *Döngü sayımı* olmak üzere iki iş emri türü yalnızca sistem tarafından kullanılır. Bu iş emri türleri için konum yönergeleri oluşturulamaz.

Aşağıdaki alt bölümlerdeki tablolarda, bir konum yönergesi ayarladığınızda kullanılabilen ortak ve iş emri türüne özgü alanlar listelenir.

### <a name="fields-that-are-common-to-all-work-order-types"></a>Tüm iş emri türleri için ortak olan alanlar

Aşağıdaki tabloda, tüm iş emri türleri için ortak olan alanlar listelenmiştir.

| Hızlı sekme | Alan |
|---|---|
| Konum yönergeleri | İş türü |
| Konum yönergeleri | Tesis |
| Konum yönergeleri | Ambar |
| Konum yönergeleri | Yönerge kodu |
| Konum yönergeleri | Kapsam *veya* Çoklu SKU |
| Satırlar | Numara serisi |
| Satırlar | Başlangıç miktarı |
| Satırlar | Son miktar |
| Hatlar | Birim |
| Hatlar | Miktarı bul |
| Hatlar | Birime göre kısıtla |
| Hatlar | Yukarı yuvarlama birimi |
| Hatlar | Paketleme miktarını bul |
| Hatlar | Bölmeye izin ver |
| Konum Yönergesi Eylemleri | Numara serisi |
| Konum Yönergesi Eylemleri | Kuruluş adı |
| Konum Yönergesi Eylemleri | Sabit yerleşim kullanımı |
| Konum Yönergesi Eylemleri | Negatif stoğa izin ver |
| Konum Yönergesi Eylemleri | Toplu iş etkinleştirildi |
| Konum Yönergesi Eylemleri | Strateji |

### <a name="fields-that-are-specific-to-work-order-types"></a><a name="fields-specific-types"></a>İş emri türlerine özgü olan alanlar

Aşağıdaki tabloda, iş emri türlerine özgü olan alanlar listelenmiştir.

| Hızlı sekme | Alan | İş siparişi türü |
|---|---|---|
| Konum yönergeleri | Şuna göre bul: | Satın alma siparişleri |
| Konum yönergeleri | Geçerli elden çıkarma kodu | Satın alma siparişleri |
| Konum yönergeleri | Elden çıkarma kodu | Satın alma siparişleri |
| Konum yönergeleri | Geçerli elden çıkarma kodu | Yerine konan mamul mallar |
| Konum yönergeleri | Elden çıkarma kodu | Yerine konan mamul mallar |
| Konum yönergeleri | Geçerli elden çıkarma kodu | Sipariş iadeleri |
| Konum yönergeleri | Elden çıkarma kodu | Sipariş iadeleri |
| Konum yönergeleri | Geçerli elden çıkarma kodu | Kanban yerine koyma |
| Konum yönergeleri | Geçerli elden çıkarma kodu | Kanban çekme |
| Hatlar | Anlık stok yenileme şablonu | Satış siparişleri |
| Hatlar | Anlık stok yenileme şablonu | Hammadde çekme |
| Hatlar | Anlık stok yenileme şablonu | Transfer sorunu |
| Hatlar | Anlık stok yenileme şablonu | Kanban çekme |

## <a name="open-the-location-directives-page"></a>Konum yönergeleri sayfasını açma

**Konum yönergeleri** sayfasını açmak için **Ambar yönetimi \> Kurulum \> Yerleşim yönergeleri**'ne gidin.

Buradan, Eylem bölmesindeki komutları kullanarak konum yönergelerinizi görüntüleyebilir, oluşturabilir ve düzenleyebilirsiniz. Sayfada bulunan tüm alanların nasıl kullanılacağı hakkında bilgi için bu makalenin geri kalan bölümlerine bakın.

## <a name="action-pane"></a>Eylem Bölmesi

**Konum yönergeleri** sayfasındaki Eylem bölmesi, yönergeleri oluşturmak, düzenlemek ve silmek için kullanabileceğiniz düğmeler (**Düzenle**, **Yeni** ve **Sil**) içerir. Ayrıca, konum yönergesinin işlendiği sırayı ayarlamanıza ve konum yönergesini uygulama ölçütlerini tanımlayan bir sorguyu yapılandırmanıza olanak tanıyan aşağıdaki düğmeler de bulunur:

- **Yukarı taşı**: Seçili konum yönergesini sırada yukarı taşıyın. Örneğin, bunu 4 numaralı sıradan 3 numaralı sıraya taşıyabilirsiniz.
- **Aşağı taşı**: Seçili konum yönergesini sırada aşağı taşıyın. Örneğin, bunu 4 numaralı sıradan 5 numaralı sıraya taşıyabilirsiniz.
- **Kopyala** – Geçerli konum yönergesinin tam kopyasını oluşturabileceğiniz bir iletişim kutusu açar.
- **Sorguyu düzenle**: Seçili konum yönergesinin altında işlenmesi gereken koşulları tanımlayabileceğiniz bir iletişim kutusu açar. Örneğin, bunun yalnızca belirli bir ambara uygulanmasını isteyebilirsiniz.
- **Kabul testleri** – Konum yönergelerinizin farklı başlangıç koşulları altında nasıl davranacağını belirlemek için otomatik testler ayarlayabileceğiniz bir sayfa açar. Bu şekilde, yönergelerinizi oluştururken ve sürdürürken hızlı bir şekilde kolayca doğrulayabilirsiniz. Daha fazla bilgi için bkz. [Kabul testleri ile konum yönergelerini test etme](location-directive-acceptance-tests.md).

## <a name="location-directives-header"></a>Konum yönergeleri başlığı

Konum yönergesi başlığı, sıra numarası ve konum yönergesinin tanımlayıcı adı için aşağıdaki alanları içerir:

- **Sıra numarası**: Bu alan, sistemin seçili iş emri türü için her bir konum yönergesini uygulamaya çalıştığı sırayı gösterir. Önce düşük sayılar uygulanır. Sırayı, Eylem bölmesindeki **Yukarı Taşı** ve **Aşağı Taşı** düğmelerini kullanarak değiştirebilirsiniz.
- **Ad**: Konum yönergesi için açıklayıcı bir ad girin. Bu ad, yönergenin genel amacını tanımlamaya yardımcı olmalıdır. Örneğin, *Ambar 24'teki satış siparişi malzeme çekme* girin.

## <a name="location-directives-fasttab"></a><a name="location-directives-tab"></a>Konum yönergeleri hızlı sekmesi

**Konum yönergeleri** hızlı sekmesindeki alanlar, liste bölmesindeki **İş emri türü** alanında seçilen iş emri türüne özgüdür.

- **İş türü**: Yapılması gereken iş türünü seçin. Kullanılabilir değerler, **Çalışma siparişi türü** alanında seçtiğiniz stok hareketi türüne bağlıdır. Aşağıdaki değerlerden birini seçin:

    - **Yerine koyma**: Yerleşim yönergesi teslim alma, üretim veya stok ayarlamaları aracılığıyla sisteme gelen stoğu yerleştirmek veya yerini belirlemek için ideal konumu bulmaya çalışır. Bir yerine bir aşama veya bir bölmesi kapı son sevkiyat yerleşimine tanımlamak için de kullanılabilir.
    - **Çekme**: Yerleşim yönergesi, stoğu fiziksel olarak rezerve etmek için (iş oluştur) ideal konumları bulmaya çalışır. Çekme, iş tamamlanmamış olsa bile tamamlanabilir (çekme iş satırı kapatılabilir). Kullanıcı fiziksel malzeme çekmeyi tamamlayabilir. Sistemde, bu eylem bir çekme adımıdır. Kullanıcı daha sonra bir mobil cihazdan iptal edebilir ve işi sonra tamamlayabilir. Bununla birlikte, son yerleştirme tamamlandığında iş bağlığı önce kapatılır.

    > [!IMPORTANT]
    > **İş türü** alanındaki diğer değerler, konum yönergeleri için uygun değildir. Yalnızca alan seçili iş emri türüyle eşleşmek üzere filtrelenmediği için görünürler.

- **Tesis**: Bu alan zorunludur çünkü konum yönergesinin geçerli olacağı tesisi ve ambarı belirlemesi gerekir.
- **Ambar**: Bu alan zorunludur çünkü konum yönergesinin geçerli olacağı tesisi ve ambarı belirlemesi gerekir.
- **Yönerge kodu**: Bir iş şablonu veya stok yenileme şablonu için yönerge kodunu seçin. **Yönerge kodu** sayfasında, iş şablonlarını veya stok yenileme şablonlarını yerleşim yönergelerine bağlamak için kullanılabilecek yeni kodlar oluşturabilirsiniz. Yönerge kodları ayrıca, herhangi bir iş şablonu satırı ve konum yönergesi (bölme kapısı veya hazırlama konumu gibi) arasındaki bağlantıyı oluşturmak için de kullanılabilir.

    > [!TIP]
    > Yönerge kodu ayarlanırsa, iş oluşturulması gerektiğinde sistem, arama yönergelerini sıra numarasına göre aramaz. Bunun yerine, yönerge koduna göre arama yapılır. Bu şekilde, iş şablonundaki (örneğin malzemelerin hazırlanması gibi) belirli bir adım için hangi konum yönergesinin kullanılabileceği konusunda daha spesifik olabilirsiniz.

- **Kapsam** – Konum yönergesinin uygulanacağı senaryoları belirlemek için bu seçeneği kullanın. Bu seçenek **Çoklu SKU** seçeneğinin yerini alır ve yalnızca sisteminizde *Konum yönergesi kapsamları* özelliğini açar. (Daha fazla bilgi için bkz. [Konum yönergesi kapsamları özelliğini açma veya kapatma](#scopes-feature).)

    | Kapsam ayarı | Bir öğeli tek bir sipariş | Aynı öğeyle birden fazla sipariş | Birden fazla öğeyle tek bir sipariş | Birden fazla öğeyle birden fazla sipariş |
    |---|---|---|---|---|
    | Tek madde | Evet | Evet | No. | No. |
    | Birden çok madde | No. | No. | Evet | Evet |
    | Tek madde veya sipariş | Evet | Evet | Evet | No. |
    | Tümü | Evet | Evet | Evet | Evet |

    Aşağıdaki tabloda kapsamların ne zaman kullanılabilir olduğu ve **Sorgu düzenle** işlevine izin verip vermedikleri açıklanır.

    | Kapsam | Destekli iş türü | Destekli iş emri türleri | Sorgu düzenlemeye izin ver |
    |---|---|---|---|
    | Tek madde | Tümü | Tümü | Evet |
    | Birden çok madde | Tümü | Tümü | No. |
    | Tek madde veya sipariş | Yerleştirmeler | Ortak ürün ve yan ürün yerine koyma, mamul mallar yerine koyma, kanban yerine koyma, satın alma siparişleri, kalite emirleri, stok yenileme, iade siparişleri, satış siparişleri, transfer sorunu ve transfer alış irsaliyesi | Evet |
    | Tümü | Yerleştirmeler | Tümü | No. |

    > [!NOTE]
    > - Hem birden fazla öğeyi hem de tek bir öğeyi yerine koyarken, her iki senaryoyu kapsayan konum yönergelerinin mevcut olduğundan emin olmalısınız. Hassas ayarlama gerektiren senaryoları kapsamak için bir veya daha fazla *Tek öğe veya sipariş* konum yönergesi ve ardından kalan senaryoları kapsamak için bir veya daha fazla *Tümü* konum yönergesi ayarlayabilirsiniz.
    > - *Tek öğe* ve *Birden fazla öğe* kapsamları yerleştirmeler için kullanılabilse de bu yaklaşım genellikle gereksiz yapılandırmalara yol açar. Bunun yerine *Tek öğe veya sipariş* ve *Tümü* kapsamlarını kullanmayı düşünün, çünkü bu yaklaşım daha temiz bir kurulum üretir.

- **Birden fazla SKU** – Konum yönergesinin uygulanacağı senaryoyu belirlemek için bu seçeneği kullanın. Sisteminizde *Konum yönergesi kapsamları* özelliği etkinse bu ayar **Kapsam** ayarı ile değiştirilir. (Daha fazla bilgi için bkz. [Konum yönergesi kapsamları özelliğini açma veya kapatma](#scopes-feature).) Bir konumda birden fazla stok tutma biriminin (SKU'lar) kullanılmasını sağlamak için bu seçeneği *Evet* olarak ayarlayın. Örneğin, bölme kapısı konumu için birden çok SKU etkinleştirilmiş olmalıdır. Birden çok SKU'yu etkinleştirirseniz yerine koyma konumunuz beklendiği gibi çalışma sırasında belirtilir. Ancak, yerine koyma konumu yalnızca çoklu madde yerine koymayı işleyebilir (iş, çekilmesi ve yerine koyulması gereken farklı SKU'lar içeriyorsa). Tek bir SKU yerine koymayı işleyemez. Bu seçeneği *Hayır* olarak ayarlarsanız, yerine koyma konumunuz, yerine koyma işleminde yalnızca bir çeşit SKU varsa belirtilir.

    > [!IMPORTANT]
    > Hem çoklu madde, hem de tekli SKU yerine koyma yapabilmek için aynı yapıya ve kuruluma sahip iki satır belirtmeniz gerekir ancak **Birden fazla SKU** seçeneğini bir satır için *Evet* ve diğeri için *Hayır* olarak ayarlamalısınız. Bu nedenle, yerine koyma işlemleri için iki eş konum yönergesine ihtiyacınız vardır, iş kimliğinde tekli SKU veya çoklu SKU arasında ayrım yapmıyorsanız bile. Genellikle, bu konum yönergelerinin her ikisini birden ayarlamadıysanız, uygulanan Konum yönergesinden beklenmeyen iş süreci konumları gelecektir. Çoklu SKU'ları içeren siparişleri işleyebilmeniz gerekiyorsa *malzeme çekme* **İş türü** olan konum yönergeleri için benzer bir kurulum kullanmalısınız.

    Birden fazla madde numarası işleyen iş satırları için **Çoklu SKU** seçeneğini kullanın. (Madde numarası iş ayrıntılarında boş olacak ve Ambar Yönetimi mobil uygulamasındaki işleme sayfalarında **Çoklu** şeklinde gösterilecektir.)

    Tipik bir örnek senaryoda, bir iş şablonu birden fazla malzeme çekme/yerine koyma çifti içerecek şekilde ayarlanır. Bu durumda, **İş türü** *Yerine Koyma* olan satırlarda kullanılmak üzere belirli bir hazırlama konumunu aramak isteyebilirsiniz.

    > [!NOTE]
    > **Birden fazla SKU** seçeneği *Evet* olarak ayarlanmışsa, Eylem bölmesinde **Sorguyu düzenle**'yi seçemezsiniz çünkü sorgu birden fazla madde olduğunda madde düzeyinde değerlendirilemez. İstenen konum yönergesinin seçildiğinden emin olmak için iş şablonunda o yönerge kodunun atandığı yerine koyma satırlarıyla ilişkili konum yönergesi seçimine yol göstermek için **Yönerge kodu** alanını kullanın.

    Tek maddeyle veya karışık madde işlemleriyle çalışmadığınız sürece, *Yerine Koyma* iş türü için iki konum yönergesi tanımlamanız önemlidir: **Çoklu SKU** seçeneğinin *Evet* olarak ayarlandığı konum ve *Hayır* olarak ayarlandığı konum.

- **Geçerli değerlendirme kodu**: Yerleşim yönergesi değerlendirme kodunun, ürün teslim almada uygulanan değerlendirme koduyla eşleşmesi gerekip gerekmediğini veya yerleşim yönergesinin herhangi bir değerlendirme kodu temel alınarak seçilip seçilemeyeceğini belirtin. *Tam eşleşmeyi* seçerseniz ve **Değerlendirme kodu** alanı boşsa, bu yerleşim yönergesi için yalnızca boş değerlendirme kodları dikkate alınır.

    > [!NOTE]
    > Bu alan yalnızca stok yenilemeye izin verilen seçili iş emri türleri için kullanılabilir. Listenin tamamı için bu makalenin önceki bölümlerindeki [İş emri türlerine özel olan alanlar](#fields-specific-types) kısmına bakın.

- **Bulma ölçütü**: Yerine koyma miktarının plakadaki miktarın tamamı mı yoksa maddeye göre mi olacağını belirtin. Bir plakadaki tüm içeriğin bir konuma yerleştirilmesini ve sistemin içeriği **ANS** (plaka teslim alma), **Karma plaka** teslim alma ve **Küme** teslim alma işlemleri için çeşitli konumlara bölmenizi önermemesini sağlamak için bu alanı kullanın. (Bu **Küme** teslim alma işlemi, [Küme yerine koyma özelliği](putaway-clusters.md)'nin açık olmasını gerektiriyor.) Konum yönergesi sorgusunun, satırların ve konum yönergesi eylemlerinin davranışı seçtiğiniz değere göre değişir. **Satırlar** hızlı sekmesi yalnızca, **Bulma ölçütü** *Madde* olarak ayarlandığında kullanılır.

    > [!NOTE]
    > Bu alan yalnızca stok yenilemeye izin verilen seçili iş emri türleri için kullanılabilir. Listenin tamamı için [İş emri türlerine özel olan alanlar](#fields-specific-types) kısmına bakın.

- **Değerlendirme kodu**: Bu alan, iş emri türü *Satın alma siparişleri*, *Bitmiş mal yerine koyma* veya *İade siparişleri* olan ve iş türü *Yerine koyma* olan iş emri türüne sahip konum yönergeleri için kullanılır. Ambar Yönetimi mobil uygulamasında bir çalışanın seçtiği değerlendirme koduna bağlı olarak, akışta belirli bir konum yönergesini kullanmasını gösteren bir yol göstermesi için bunu kullanın. Örneğin, stoğa iade etmeden önce iade edilen malları bir denetleme konumuna yönlendirebilirsiniz. Bir değerlendirme kodu stok durumuna bağlanabilir. Bu şekilde, teslim alma sürecinin bir parçası olarak stok durumunu değiştirmek için kullanılabilir. Örneğin, stok durumunu *QA* olarak ayarlayan *QA* adlı bir değerlendirme kodunuz vardır. Daha sonra, bu stoğu karantina konumuna taşımak için ayrı bir konum yönergesine sahip olabilirsiniz.

    > [!NOTE]
    > Bu alan yalnızca stok yenilemeye izin verilen seçili iş emri türleri için kullanılabilir. Listenin tamamı için [İş emri türlerine özel olan alanlar](#fields-specific-types) kısmına bakın.

## <a name="lines-fasttab"></a>Satırlar hızlı sekmesi

**Konum yönergesi eylemleri** hızlı sekmesinde belirtilen ilgili eylemleri uygulama koşullarını oluşturmak için **Satırlar** hızlı sekmesini kullanın. Her satır için eylemlerin uygulanacağı bir minimum miktar ve maksimum miktar belirtebilirsiniz. Ayrıca, eylemlerin belirli bir stok birimi için geçerli olacağını da belirtebilirsiniz.

- **Sıra numarası**: Seçilen iş türü için konum yönergesinin hangi sırada işlenmesi gerektiğini girin. Sırayı, araç çubuğundaki **Yukarı taşı** ve **Aşağı taşı** düğmelerini kullanarak dilediğiniz gibi değiştirebilirsiniz.
- **Başlangıç miktarı**: Satırın geçerli olduğu miktar aralığının başlangıcını belirtin. **Birim** alanında, miktar için ölçü birimini belirtin.
- **Bitiş miktarı**: Satırın geçerli olduğu miktar aralığının bitişini belirtin. **Birim** alanında, miktar için ölçü birimini belirtin.
- **Birim**: Maddelerin ölçü birimini seçin. Yönergenin uygulanması gereken minimum miktarı ve maksimum miktarı belirtebilirsiniz ve o yönergenin belli bir stok birimine yönelik olması gerektiğini belirtebilirsiniz. **Birim** alanı *yalnızca* miktar değerlendirmesi için kullanılır. Bir yerleşim yönergesi satırının uygulanıp uygulanmayacağını belirlemek için sistem, o satırda belirtilen birimdeki miktarı kullanarak değerlendirir. Bir konum yönergesi satırına ulaştığında, sistem talep birimini, satırda belirtilen birime dönüştürmeye çalışır. Ölçü birimi dönüştürme yoksa sistem sonraki satıra geçer.
- **Miktarı bul**: Bu alan yalnızca ambardaki maddeleri yerine koyma veya bulma girişimleri sırasında kullanılır. (Bu nedenle yalnızca **İş türü** alanı *Koyma* olarak ayarlandığında geçerlidir.) Bir miktarın **Başlangıç miktarı** ile **Bitiş miktarı** aralığında olup olmadığını değerlendirmek için kullanılan miktarı belirtmek üzere aşağıdaki değerlerden birini seçin:

    - **Plaka miktarı**: Alınmakta olan plakadaki miktarı kullanın.
    - **Bırakılmamış miktar**: Hareket sırasında kullanılan miktarı kullanın. Örneğin, bir ambarda 1.000 miktarını alıp her birinin 100 miktarı olan 10 plakaya bölebilirsiniz. Bu durumda, 100 plaka miktarı yerine 1.000 miktar maddeyi kullanabilirsiniz.
    - **Kalan miktar**: İşlenmekte olan satın alma siparişi satırında hala teslim alınması gereken miktarı kullanın.
    - **Beklenen miktar**: Teslim alınan madde ne olursa olsun, satın alma siparişi satırının toplam miktarını kullanın.

- **Birime göre kısıtla**: Bu onay kutusu, konum yönergesi satırını bir ölçü birimine veya birden fazla ölçü birimlerine göre özel hale getirir. Yerleşim yönergesi satırları için geçerli seçim ölçütü olarak kabul edilen ölçü birimlerini sınırlandırmak için bunu seçin. Bu işlev yalnızca **İş türü** alanının *Malzeme çekme* olarak ayarlandığı konum yönergeleri için kullanılabilir.

    Örneğin, miktar ayırdığınızda paletleri yalnızca belirli bir konum kümesinden ayırmak isteyebilirsiniz. Bu durumda satırlar, konum yönergesi için bir paletten az olan miktarın seçilmemesi için bu diziyi paletlere göre kısıtlar.

    **Birime göre kısıtla** onay kutusunun iş satırları üzerinde uygulanan birim veya birimleri denetlemediğini unutmayın. Birim kısıtlaması yalnızca birim sırası grubu aracılığıyla kullanılabilir duruma getirilen birimlere uygulanır. Örneğin, bir madde hem *paletler* birimi hem de *parça* birimini içeren bir birim sırası grubuyla ilişkilendirilir. 1 palet = 100 adet olacak şekilde bir ölçü birimi tanımlanır ve yerleşim yönergesi yalnızca paletler için **Birime göre kısıtla** işlevini kullanır. Ayrıca, iş başlığı oluşturmayı 50 adete sınırlayan bir iş şablonu tanımlanmıştır. Bu durumda, 50 adetlik iş satırları oluşturulur. Kısıtlama için ölçü birimini belirtmek üzere aşağıdaki adımları izleyin:

    1. **Satırlar** hızlı sekmesinde, araç çubuğundaki **Birimle sınırla**'yı seçin. (Bu düğme yalnızca satırdaki **Birime göre kısıtla** onay kutusu seçildikten sonra kullanılabilir duruma gelir; ardından **Kaydet**'i seçin.)
    1. **Birimle sınırla** sayfasında, **Birim** alanında, çekme ve yerine koyma işlemleri için sınırlamak istediğiniz ölçü birimini seçin.

- **Birime yuvarla**: Bu alan, **Birimle sınırla** onay kutusu ile birlikte çalışır. Örneğin, **Birimle sınırla** ve **Birime yukarı yuvarla**, konum yönergesinde seçiliyse hammadde çekmeye yönelik yönergede oluşturulan işin, bir işleme biriminin katına yukarı yuvarlanacağı anlamına gelir (**Birimle sınırla**'da belirtildiği üzere).

    > [!NOTE]
    > Bu **Birime yukarı yuvarla** ayarı, yalnızca *Ham malzeme çekme* iş emri türü için ve **İş türü** alanının *Çekme* olarak ayarlandığı konum yönergeleri için geçerlidir.

- **Ambalaj Miktarını Bul**: Bir satış siparişi, transfer emri veya üretim emrinde ambalaj miktarı belirtirseniz bu onay kutusu, sistemi yalnızca en az ambalaj miktarına sahip olan konumları seçebileceği şekilde sınırlamanıza olanak tanır.

    > [!NOTE]
    > Bu işlev, yalnızca *Çekme* türündeki konum yönergeleriyle çalışır.

- **Bölmeye İzin Ver**: Bir konum yönergesinin alınan miktarı veya birden çok ambar konumu arasında rezerve edilen miktarın bölmesine izin verilip verilmeyeceğini veya işin oluşturulması için tüm miktarın tek bir konum veya rezerve edilen edilmesi gerekip gerekmediğini belirtin.
- **Anında stok yenileme şablonu**: Maddeler tahsis edilmemişse stok yenilemeyi hemen başlatmak için stok yenileme şablonuna bağlantı oluşturmak için bunu kullanın. Bu alan boş bırakılırsa, yerleşim yönergesindeki tüm satırlar işlenene kadar madde stok yenilemesi başlatılmaz.

    > [!NOTE]
    > Bu alan yalnızca stok yenilemeye izin verilen seçili iş emri türleri için kullanılabilir. Listenin tamamı için [İş emri türlerine özel olan alanlar](#fields-specific-types) kısmına bakın.

## <a name="location-directive-actions-fasttab"></a>Konum yönergesi eylemleri hızlı sekmesi

Her satır için birden fazla konum yönergesi eylemi tanımlayabilirsiniz. Bir kez daha, bir sıra numarası eylemlerin karar sırasını belirlemek için kullanılır. Bu düzeyde, ambardaki en iyi konumun nasıl bulunacağını tanımlamak için bir sorgu ayarlayabilirsiniz. Ayrıca ideal bir konum bulmak için önceden tanımlanmış **Strateji** değerlerini de kullanabilirsiniz.

- **Sıra numarası**: Bu alan, seçilen iş türü için eylemlerin hangi sırada işlendiğini gösterir. Sırayı, araç çubuğundaki **Yukarı Taşı** ve **Aşağı Taşı** düğmelerini kullanarak değiştirebilirsiniz.
- **Ad**: Konum yönergesi eyleminin adını girin. Gerçekleştirilecek eylemin addan ayrılması için net bir ad verin.
- **Sabit konum kullanımı**: Konum yönergesinin hangi konumları göz önünde bulundurduğunu belirtin. Aşağıdaki değerlerden birini seçin:

    - **Sabit ve sabit olmayan yerleşimler** - Yerleşim yönergesi tüm yerleşimleri kabul eder.
    - **Ürün için yalnızca sabit yerleşimler** - Yerleşim yönergesi ürünler için yalnızca sabit yerleşimleri kabul edecektir.
    - **Ürün çeşidi için yalnızca sabit yerleşimler** - Yerleşim yönergesi ürün çeşitleri için yalnızca sabit yerleşimleri kabul edecektir.

- **Negatif stoğa izin ver**: Konum yönergelerinde belirtilen ambar konumunda eksi stoğa izin vermek için bu onay kutusunu seçin.
- **Toplu İş Etkin**: Etkin toplu iş öğeleri için toplu iş stratejileri kullanmak için bu onay kutusunu seçin. Toplu iş numarası ile izlenen maddeleri çekmek üzere konum yönergelerini kullanan işlemler için bu onay kutusunu seçmeniz önemlidir. Bu şekilde, toplu iş numarası izlenen maddeleri tutan konumların araması dahil edilir. Bu onay kutusu işaretliyse ve **Strateji** alanı *Hiçbiri* olarak ayarlanmışsa , sistem sonraki eylem satırına geçer.
- **Strateji**: Her bir konum yönergesi satırı ile ilişkili eylemleri tanımlamanın daha hızlı ve kolay olması için önceden tanımlanmış stratejilerden birini seçebilirsiniz:

    - **Hiçbiri** – Strateji kullanılmaz.
    - **Paketleme miktarını eşleştir** - Bu strateji çekme yerleşiminin belirtilen paketleme miktarına sahip olup olmadığını doğrular. Bu strateji yalnızca **İş türü** alanı *Çekme* olarak ayarlandığında geçerlidir.
    - **Birleştir** - Bu strateji, benzer maddeler kullanılabilir olduğunda maddeleri belirli bir yerleşimde birleştirmek için kullanılır. Bu strateji yalnızca **İş türü** alanı *Koyma* olarak ayarlandığında geçerlidir. Koyma eylemi için normal bir kurulum, ilk eylem satırında birleştirme yapmaya çalışır ve ardından ikinci eylem satırında birleştirme olmadan koyma işlemini gerçekleştirmeyi dener. Ürünleri birleştirmek, sonraki çekmeleri daha verimli hale getirir.
    - **FEFO toplu iş rezervasyonu**: Bu strateji ilk sona eren ilk çıkar (FEFO) toplu iş rezervasyonlarını kullanır. Stok toplu iş bitiş tarihi kullanarak konumlandırıldığında ve toplu iş rezervasyonu için tahsis edildiğinde kullanın. Bu stratejiyi yalnızca toplu iş etkinleştirilmiş maddelerde kullanabilirsiniz. Yalnızca **İş türü** alanı *Çekme* olarak ayarlandığında geçerlidir.
    - **Tam LP ve FEFO toplu işine yukarı yuvarla**: Bu strateji, *FEFO toplu iş rezervasyonu* ile *Tam LP'ye yukarı yuvarla* stratejilerinin öğelerini içerir. Yalnızca toplu iş için etkin maddeler ve iş türü *Çekme* olan konum yönergeleri için geçerlidir. Satır, *FEFO toplu iş rezervasyonu* stratejisini kullanmak için toplu olarak etkinleştirilmiş olmalıdır ve *Tam LP'ye yukarı yuvarla* stratejisi yalnızca stok yenileme için kullanılabilir. Bu strateji stoklama limiti ile birlikte yapılandırılırsa seçili koyma işi konumunun aşırı yüklenmesine ve stoklama limitlerinin yoksayılmasına neden olabilir.
    - **Tam LP'ye yuvarla** - Bu strateji stok miktarını, çekilecek maddelere atanan plaka (LP) miktarıyla eşleşecek şekilde yuvarlamak için kullanılır. Bu stratejiyi yalnızca *Çekme* türündeki stok yenileme konum yönergeleri için kullanabilirsiniz. Bu strateji stoklama limiti ile birlikte yapılandırılırsa seçili koyma işi konumunun aşırı yüklenmesine ve stoklama limitlerinin yoksayılmasına neden olabilir.
    - **Plaka rehberli**: Çekme ve koyma işlerini oluşturmak için siparişi ambara serbest bıraktığınızda bu stratejiyi kullanın. Çoklu plakalar için bu yaklaşımı kullanabilirsiniz. Bu strateji, transfer emri satırlarıyla ilişkilendirilmiş olan istenen plakaları tutan konumlara göre ayırma ve çekme işi oluşturmayı dener. Ancak, bu eylemler tamamlanamadığı halde malzeme çekme işi oluşturmak istiyorsanız konum yönergesi eylemleri için başka bir stratejiye geri dönmelisiniz. İş süreci gereksinimlerinize bağlı olarak, ambarın başka bir alanında stok aramak da isteyebilirsiniz.
    - **Gelen iş olmadan boş yerleşim**- Bu stratejiyi boş yerleşimleri bulmak için kullanın. Fiziksel stoğu yoksa ve gelen iş beklenmiyorsa yerleşim boş olarak değerlendirilir. Bu stratejiyi yalnızca *Yerine Koyma* iş türüne sahip konum yönergeleri için kullanabilirsiniz.
    - **Konum yaşlandırma FIFO**: Hem toplu olarak izlenen maddeleri, hem de toplu olarak izlenmeyen maddeleri sevk etmek için stoğun ambara girdiği tarihi temel alan İlk giren ilk çıkar (FIFO) stratejisini kullanabilirsiniz. Bu yetenek özellikle, tasnif için bitiş tarihi bulunmayan, toplu olarak izlenmeyen stok için yararlı olabilir. FIFO stratejisi, en eski yaşlandırma tarihini içeren konumu bulur ve ardından bu yaşlandırma tarihine göre malzeme çekme işlemini tahsis eder.
    - **Konum yaşlandırma LIFO**: Hem toplu olarak izlenen maddeleri, hem de toplu olarak izlenmeyen maddeleri sevk etmek için stoğun ambara girdiği tarihi temel alan Son giren son çıkar (LIFO) stratejisini kullanabilirsiniz. Bu yetenek özellikle, tasnif için bitiş tarihi bulunmayan, toplu olarak izlenmeyen stok için yararlı olabilir. LIFO stratejisi, en yeni yaşlandırma tarihini içeren konumu bulur ve ardından bu yaşlandırma tarihine göre malzeme çekme işlemini tahsis eder.

## <a name="example-using-location-directives"></a>Örnek: Konum yönergelerini kullanma

Bu örnekte, konum yönergesinin, alış noktasında kaydedilen stok öğeleri için bir ambar içinde serbest kapasite bulmasının gerektiği bir satınalma siparişi işlemini ele alacağız. İlk olarak, mevcut eldeki stok ile birleştirerek ambar içinde boş kapasite bulmanız gerekir. Konsolidasyon mümkün değilse, bu durumda boş bir yer bulmanız gerekir.

Bu senaryo için iki konum yönergesi eylemi tanımlamanız gerek. Sıradaki ilk eylemin *Konsolide Et* stratejisini ve ikinci eylemin *Gelen iş olmayan boş yer* stratejisini kullanması gerekir. Bir taşma senaryosunu idare etmek için üçüncü bir eylem tanımlamadığınız takdirde, ambarda daha fazla kapasite olmadığında iki sonucun meydana gelmesi olasıdır: iş hiçbir konum tanımlanmasa da oluşturulabilir veya iş oluşturma işlemi başarısız olabilir. Sonuç **Konum yönergesi hataları** sayfasındaki ayara göre belirlenir; burada her bir iş siparişi türü için **Konum yönergesi hatasında işi durdur** seçeneğini seçip seçmemeye karar verebilirsiniz.

## <a name="next-step"></a>Sonraki adım

Yerleşim yönergeleri oluşturduktan sonra, her yönerge kodunu iş oluşturma için bir iş şablonu koduyla ilişkilendirebilirsiniz. Daha fazla bilgi için bkz. [İş şablonları ve yerleşim yönergeleri kullanarak ambar işini denetleme](./control-warehouse-location-directives.md).

## <a name="additional-resources"></a>Ek kaynaklar

- Video: [Ambar yönetimi yapılandırmasının ayrıntıları](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Yardım makalesi: [İş şablonları ve konum yönergeleri ile ambar işini denetleme](control-warehouse-location-directives.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
