---
title: Stok tahminleri
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta stok tahminleri oluşturmak için kullanılabilen tedarik ve talep tahmini işlevleri açıklanmaktadır.
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: abc827139c71f7942335cd2b7e2c7502f7fc1cfe
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469408"
---
# <a name="inventory-forecasts"></a>Stok tahminleri

[!include [banner](../includes/banner.md)]

Bu konuda stok tahminlerinin nasıl görüntüleneceği ve oluşturulacağı açıklanmaktadır. Maddeler, madde grupları, madde tahsisat anahtarları, müşteri hesapları, müşteri grupları, satıcı hesapları ve satıcı grupları için tedarik ve talep tahmin satırları oluşturabilir ve görüntüleyebilirsiniz.

Her tahmin satırı için kullanılan tahmin modelini seçebilirsiniz. Daha sonra madde veya madde grubunu ve miktar veya hareket tutarını belirtebilirsiniz. Aynı zamanda tahmin miktarının tahsisi için bir zaman planlaması da ayarlayabilirsiniz.

Tedarik ve talep tahmin satırları bir madde ve model birleşimi için stok tahmini oluşturur. Bu stok tahmini, aynı madde için girilen tedarik talebi ile ilgili olarak bir bakiyeyi temsil eder. Bu değer düzenlenemez. Stok tahmini, stok yönetimi ekibinin tahmin edilen dönem içinde bir maddenin eldeki stokunda beklenen değişiklikleri incelemesine yardımcı olur.

Talep ve/veya tedarik değerlerinizi girdikten sonra, malzeme ve kapasite için brüt gereksinimleri hesaplamak ve planlanmış siparişler oluşturmak üzere tahmin planlamayı çalıştırabilirsiniz.

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>Tahmin satırlarını görüntüleme ve el ile girme

Ürünlerle ilgili tahmin satırlarını el ile oluşturmak için bu prosedürü kullanın.

Tahmin satırlarını oluşturmanın başka yolları da vardır:

- [İstatistik temel tahmini oluşturma](generate-statistical-baseline-forecast.md).
- [Talep tahminleri için geçmiş verilerini içe aktarma](import-historical-data.md).
- [Microsoft Azure Machine Learning web servisi kullanarak tahmin oluşturma](demand-forecasting-setup.md).
- [Veri yönetimi çerçevesi (ForecastDemandForecastEntryStaging ve ForecastSupplyForecastEntryStaging veri varlıkları) kullanarak talep veya tedarik tahmin satırlarını içe aktarma](../../dev-itpro/data-entities/data-entities-data-packages.md).

Adım 1'deki tabloda gösterildiği gibi, kullanılan sayfalara erişmek için farklı yollar vardır.

1. Tahmin oluşturmak istediğiniz varlık türüne ve oluşturmak istediğiniz tahmin türüne bağlı olarak, aşağıdaki tabloda açıklandığı gibi bir tedarik, talep veya stok tahmin sayfası açın.

    | Varlık | Yönergeler |
    |---|---|
    | Serbest bırakılan ürünler | <ol><li>**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</li><li>Adına tahmin oluşturulacak ürünü seçin.</li><li>Eylem Bölmesinde, **Plan** sekmesinde, **Tahmin** grubunda, çalışmak istediğiniz tahmin türüne bağlı olarak **Talep tahmini**, **Tedarik tahmini** veya **Stok tahmini**'ni seçin.</li></ol> |
    | Serbest bırakılan ürün çeşitleri | <ol><li>**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürün çeşitleri**'ne gidin.</li><li>Adına tahmin oluşturulacak çeşidi seçin.</li><li>Eylem Bölmesinde, **Plan** sekmesinde, **Tahmin** grubunda, çalışmak istediğiniz tahmin türüne bağlı olarak **Talep tahmini**, **Tedarik tahmini** veya **Stok tahmini**'ni seçin.</li></ol> |
    | Madde grupları | <ol><li>**Stok yönetimi \> Kurulum \> Stok \> Madde grupları**'na gidin.</li><li>Adına tahmin oluşturulacak madde grubunu seçin.</li><li>Eylem Bölmesinde, çalışmak istediğiniz tahmin türüne bağlı olarak **Tahmin \> Talep**, **Tahmin \> Tedarik** veya **Tahmin \> Stok tahmini**'ni seçin.</li></ol> |
    | Madde dağıtım anahtarları | <ol><li>**Stok yönetimi \> Kurulum \> Tahmin** öğelerini seçin.</li><li>Adına tahmin oluşturulacak tahsisat anahtarını seçin.</li><li>Eylem bölmesinde, **Talep tahmini**'ni seçin.</li></ol> |
    | Müşteriler | <ol><li>**Master planlama \> Tahmin \> El ile tahmin girişi \> Müşteriler**'e gidin.</li><li>Adına tahmin oluşturulacak müşteriyi seçin.</li><li>Eylem bölmesinde, **Talep tahminini belirle**'yi seçin.</li></ol> |
    | Müşteri grupları | <ol><li>**Master planlama \> Tahmin \> El ile tahmin girişi \> Müşteri grupları**'na gidin.</li><li>Adına tahmin oluşturulacak müşteri grubunu seçin.</li><li>Eylem bölmesinde, **Talep tahminini belirle**'yi seçin.</li></ol> |
    | Satıcılar | <ol><li>**Master planlama \> Tahmin \> El ile tahmin girişi \> Satıcılar**'a gidin.</li><li>Adına tahmin oluşturulacak satıcıyı seçin.</li><li>**Tedarik tahmini** sayfasını açmak için Eylem bölmesinde, **Giriş**'i seçin.</li></ol> |
    | Satıcı grupları | <ol><li>**Master planlama \> Tahmin \> El ile tahmin girişi \> Satıcı grupları**'na gidin.</li><li>Adına tahmin oluşturulacak satıcı grubunu seçin.</li><li>**Tedarik tahmini** sayfasını açmak için Eylem bölmesinde, **Giriş**'i seçin.</li></ol> | 
    | Tüm satırlar | <ul><li>Üzerinde çalışmak istediğiniz tahmin türüne bağlı olarak **Master planlama \> Tahmin \> Talep tahmin satırları** veya **Master planlama \> Tahmin \> Tedarik tahmin satırları**'na gidin.</li></ul> |

    Seçiminize bağlı olarak, **Tedarik tahmini** veya **Talep tahmini** sayfası görüntülenir. Siz sayfayı açmadan önce seçtiğiniz kayıtla ilgili varolan tüm tahmin satırlarını gösterir.

1. Eylem Bölmesi'nde, sayfanın üst bölümünde ızgaraya tahmin satırı eklemek için **Yeni**'yi seçin.
1. Yeni satırda, **Model** alanında, kullanılacak tahmin modelini seçin. Daha sonra; madde, madde grubu, müşteri veya satıcı hesabı ya da grubu, madde miktarı veya toplam hareket tutarı gibi diğer ayrıntıları gerektiği şekilde girin. **Tedarik tahmini** ve **Talep tahmini** sayfalarında kullanılabilen alanlar hakkında ayrıntılı bilgi için bu konunun sonraki bölümlerine bakın.
1. Tahmini dönem içinde dağıtmak için **Genel bakış** sekmesinde araç çubuğunda **Tahmin ayır**'ı seçin.
1. **Tahsisat** ızgarasında, tahmin miktarlarını dağıtmak için kullanılan zaman dilimi ve zaman aralıklarını gözden geçirin.

## <a name="supply-forecast-lines"></a>Tedarik tahmini satırları

Tedarik tahmini, satın alınması gereken maddeler için bir plan oluşturmanıza olanak sağlar. Bu, satın alma ve kaynaklandırma yetkililerine neler sipariş vermeleri beklendiğini söyler.

Madde, madde grubu, madde tahsisat anahtarı, satıcı ve satıcı grubuna göre bir tedarik tahmini girebilirsiniz. Çeşitli varlıklar ve kayıtlar için **Tedarik tahmini** sayfası açma yöntemleri hakkında bilgi için bu bölgenin önceki kısımlarında yer alan [Tahmin satırlarını görüntüleme ve elle girme](#manual-entry) bölümüne bakın.

**Tedarik tahmini** sayfasının üst kısmı, tedarik tahmin satırı ızgarası ve seçili bir tahmin satırı hakkında daha fazla bilgi görüntülemek ve ayarlamak için kullanabileceğiniz bir sekmeler kümesi sağlar. Sayfanın alt kısmı bir **Tahsisat** ızgarası sağlar.

Aşağıdaki alt bölümler, her bir sekmede kullanılabilen tüm alanları ve sayfanın Eylem Bölmesinde ve **Genel bakış** sekmesindeki araç çubuğunda bulunan tüm komutları açıklar.

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>Tedarik tahmin sayfasındaki Eylem Bölmesi komutları

Aşağıdaki tabloda, **Tedarik tahmini** sayfasındaki Eylem Bölmesinde yer alan komutlar açıklanmaktadır.

| Command | Tanım |
|---|---|
| Kaydet | Geçerli ayarlarınızı kaydedin. |
| Düzenle | Düzenlenecek sayfadaki ayarları etkinleştirin. |
| Yeni | Üst ızgaraya bir tahmin satırı ekleyin. |
| Dil | Seçili tahmin satırını üst ızgaradan kaldırın. |
| Tahmini bakiyeler | Geçerli mali yıl için seçili satırın model kimliği için hesaplanan tahmin bakiyelerini görüntüleyin. Bakiyeler, döneme göre bölünür (ay). |
| Nakit akışı tahminleri | Genel muhasebeye tahsis edilen tahmin işlemlerini görüntüleyin. Daha fazla bilgi için bkz. [Nakit akışı tahminleri](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Stok \> Görüntüleme boyutları | **Genel bakış** sekmesindeki ızgarada gösterilmesi gereken stok boyutlarını seçin. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>Tedarik tahmini sayfasının Genel bakış sekmesindeki araç çubuğu komutları

Aşağıdaki tabloda, **Tedarik tahmini** sayfasındaki **Genel bakış** sekmesinde bulunan araç çubuğundaki komutlar açıklanmaktadır.

| Command | Tanım |
|---|---|
| Tahmini tahsis et | Bir tahsisat yöntemi kullanıyorsanız, tahmin hareketi için ayrı çizelge satırları oluşturun. Daha sonra satırın miktarı, tüm zaman dilimi için tarihe (seçilen zaman aralıklarına göre), miktara ve tutara göre dağıtılır. (Bu konunun sonraki bölümlerinde yer alan [Tahmini tahsis et](#allocate-forecast) bölümüne bakın.) |
| Toplu güncelleştirme | **Tahmin işlemlerini düzenle** sayfasını açın. (Bu bölümün ileriki kısımlarında yer alan [Tahmin hareketlerinin toplu güncelleştirme ](#bulk-update) bölümünü inceleyin.) |
| Stok tahmini | Seçili madde/model kombinasyonu için filtre uygulanan **Stok tahmini** sayfası görünümünü açın. (Bu bölümün ileriki kısımlarında yer alan [Stok tahmini](#inventory-forecast) bölümünü inceleyin.) |
| Madde gereksinimi oluştur | Projeyle ilgili tahmin hareketleri için madde gereksinimleri ve satış siparişi veya madde günlüğü satırları oluşturabileceğiniz iletişim kutusunu açın. Bu komut hem tedarik tahmin satırları hem de talep tahmin satırları için kullanılabilir olmakla birlikte, **Tedarik tahmini** sayfasında kullanılamaz. |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>Tedarik tahmini sayfasındaki Genel bakış sekmesi

Aşağıdaki tabloda, **Tedarik tahmini** sayfasının **Genel bakış** sekmesindeki alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| **Model** | İşlemin ilişkili olduğu tahmin modeli. |
| **Date** | Hareketin başlangıç tarihi. |
| **Satıcı hesabı** | İşlemin ilişkili olduğu satıcı hesabı. |
| **Satıcı grubu** | İşlemin ilişkili olduğu satıcı grubu. |
| **Madde numarası** | Maddenin tanımlayıcısı. |
| **Madde grubu** | Hareketin ilişkili olduğu madde grubu. |
| **Madde dağıtım anahtarı** | Tahminle ilişkili madde tahsis anahtarı. |
| **FA miktarı** | Belirtilen fiili ağırlık birimi cinsinden tahmin miktarı. |
| **FA birimi** | Maddenin satın alındığı fiili ağırlık birimi. Değer, madde kurulumundan otomatik olarak alınır. |
| **Miktar** | Belirtilen satın alma birimi cinsinden tahmin miktarı. |
| **Birim** | Maddenin satın alındığı birim. Değer, madde kurulumundan otomatik olarak alınır. Ancak, birim dönüştürmeleri ayarlanmışsa bunu değiştirebilirsiniz. |
| **Tutar** | İskontolar hariç, tahmin hareketinin tahmine katkıda bulunduğu brüt tutar. |
| **Para Birimi** | Tahmin işlemi için kullanılan para birimi kodu. Otomatik olarak girilen varsayılan para birimi, ancak farklı bir para birimi seçebilirsiniz. |
| (Diğer boyutlar) | Ek boyutlar, ızgarada sütunlar olarak gösterilebilir. Görüntülenen ek boyutları seçmek için Eylem Bölmesinde **Görüntüleme boyutları**'nı seçin. |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>Tedarik tahmini sayfasındaki Genel sekmesi

**Genel** sekmesinde, **Genel bakış** sekmesinde seçili olan satır hakkında daha fazla bilgi gösterilir. Bu bilgilerden bazıları **Genel bakış** sekmesinden yinelenir. Aşağıdaki tabloda, **Genel** sekmesinde benzersiz olan alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Rapor al | Hareketi raporlamaya dahil etmek için bu seçeneği *Evet* olarak belirleyin. |
| Yorumlar | Tahmin hareketiyle ilgili yorumlarınızı girin. |
| Active | Hareketi bütçe raporlamaya dahil etmek için bu onay kutusunu işaretleyin. |
| Nakit akış tahminlerine dahil et | Tahmin hareketini genel muhasebeye tahsis etmek için bu onay kutusunu seçin. Bu onay kutusunun ayarı, hareketleri raporlamak için değiştirilemez. |
| Satış vergi grubu | Tahmin hareketi için vergiyi belirtmek amacıyla kullanılan vergi grubu. |
| Madde satış vergisi grubu | Tahmin hareketi için vergiyi belirtmek amacıyla kullanılan madde vergisi grubu. |
| Yöntem | <p>Tahmin işlemini tahsis etmek için kullanılan yöntemi seçin:</p><ul><li>**Hiçbiri** – Tahsisat yoktur.</li><li>**Dönem** – Her dönem için aynı miktarı tahmin edin. Bu değeri seçerseniz, **Beher** alanında bir miktar ve **Birim** alanında bir zaman birimi belirleyin.</li><li>**Anahtar** – Tahmini, **Dönem anahtarı** alanında belirttiğiniz dönem tahsis anahtarına göre tahsis edin. Periyodik değişikliği hesaba katmak istediğinizde bu yöntemi kullanabilirsiniz.</li></ol>|
| Birim miktar | <p>Tahminin geleceğe uzandığı zaman aralıklarının sayısını girin. Bu alan yalnızca **Yöntem** alanında *Dönem* seçildiğinde kullanılabilir.</p><p>Örneğin, **Yöntem** alanında *Dönem* seçeneğini belirlediğinizde, **Beher** alanına *1* girin, **Birim** alanından *Aylar* seçeneğini belirleyin. **Bitiş** alanında, bir yıl sonraya ait bir bitiş tarihi belirtin. Bu durumda, gelecek yılın her ayı için, başlık satırında belirtilen madde ve miktara dayanan bir tahmin satırı oluşturulur.</p> |
| Birim | Zaman aralığının birimini seçin: *Gün*, *Ay* veya *Sene*. Tahsis işlemi, **Beher** alanında belirttiğiniz gün, ay veya yıl sayısına karşılık gelir.|
| Dönem anahtarı | Dönem tahsis anahtarını belirleyin. |
| Son | **Beher** ve **Birim** alanlarını kullandığınızda bitiş tarihini belirleyin. |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>Tedarik tahmini sayfasındaki Madde sekmesi

**Madde** sekmesinde **Genel bakış** sekmesinde seçili olan satır hakkında daha fazla madde bilgisi görüntülenir.

**Madde** sekmesinin en üstündeki ızgara, **Genel bakış** sekmesinde gösterilen madde bilgilerini de yineler. Ayrıca, **Birim** alanında belirtilen birim sayısı için satınalma fiyatını gösteren **Birim fiyatı** alanını da içerir. Birim fiyatı madde kurulumundan otomatik olarak alınır ancak bunu değiştirebilirsiniz.

Izgaranın altındaki alanlar daha fazla madde ayrıntısı sağlar. Bu bilgilerden bazıları, **Genel bakış** sekmesinden yinelenir. Aşağıdaki tabloda, **Madde** sekmesinde benzersiz olan alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Fiyata esas miktar | Satın alma fiyatının uygulandığı birim sayısını belirtin. Bu değer Maddeler tablosundan otomatik olarak alınır ancak bunu değiştirebilirsiniz. |
| Satınalmadaki masraflar | Satın alma fiyatlarındaki sabit giderler. Bu giderler miktardan bağımsızdır. |
| İskonto yüzdesi | Yüzde olarak iskonto. |
| İskonto tutarı | Satış birimi başına tutar olarak iskonto. |
| Brüt tutar | İskonto uygulanmamış olan tutar. |
| Miktar | Maddenin stok birimleri olarak hareket miktarı. |
| Alt ürün reçetesi | Özel alt ürün reçetesinin ürün reçetesi numarası. |
| Alt rota | Özel alt rotanın rota numarası. |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>Tedarik tahmini sayfasındaki Mali boyutlar sekmesi

**Mali boyutlar** sekmesi, **Genel bakış** sekmesinde seçili satırla ilgili tüm mali boyut değerlerini gösterir.

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>Tedarik tahmini sayfasındaki Stok boyutları sekmesi

**Stok boyutları** sekmesi, **Genel bakış** sekmesinde seçili satırla ilgili tüm stok boyutu değerlerini gösterir.

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>Tedarik tahmini sayfasındaki Tahsisat ızgarası

Bir madde tahsisat anahtarı kullanıyorsanız veya bir ya da daha fazla gelecek dönem için madde tahmini girdiyseniz, **Genel bakış** sekmesindeki araç çubuğunda **Tahmin tahsisatı**'nı seçerek tahmini tahsis edebilirsiniz. Miktar daha sonra, **Tahsisat** ızgarasındaki satırlar tarafından belirtilen şekilde dağıtılır.

## <a name="demand-forecast-lines"></a>Talep tahmin satırları

Talep tahmini, müşteri talebi girmenize veya oluşturmanıza olanak tanır. Satış ve pazarlama yetkililerinin, yaklaşan tahmin döneminde, beklenen taleple ilgili olarak master planlama yetkililerini bilgilendirmesine yardımcı olur.

Madde, madde grubu, madde tahsisat anahtarı, müşteri ve müşteri grubuna göre bir talep tahmini girebilirsiniz. Çeşitli varlıklar ve kayıtlar için **Talep tahmini** sayfası açma yöntemleri hakkında bilgi için bu bölgenin önceki kısımlarında yer alan [Tahmin satırlarını görüntüleme ve elle girme](#manual-entry) bölümüne bakın.

**Talep tahmini** sayfasının üst kısmı, talep tahmin satırı ızgarası ve seçili bir tahmin satırı hakkında daha fazla bilgi görüntülemek ve ayarlamak için kullanabileceğiniz bir sekmeler kümesi sağlar. Sayfanın alt kısmı bir **Tahsisat** ızgarası sağlar.

Aşağıdaki alt bölümler, her bir sekmede kullanılabilen tüm alanları ve sayfanın Eylem Bölmesinde ve **Genel bakış** sekmesindeki araç çubuğunda bulunan tüm komutları açıklar.

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>Talep tahmin sayfasındaki Eylem Bölmesi komutları

Aşağıdaki tabloda, **Talep tahmini** sayfasındaki Eylem Bölmesinde yer alan komutlar açıklanmaktadır.

| Command | Tanım |
|---|---|
| Kaydet | Geçerli ayarlarınızı kaydedin. |
| Düzenle | Düzenlenecek sayfadaki ayarları etkinleştirin. |
| Yeni | Üst ızgaraya bir tahmin satırı ekleyin. |
| Dil | Seçili tahmin satırını üst ızgaradan kaldırın. |
| Tahmini bakiyeler | Geçerli mali yıl için seçili satırın model kimliği için hesaplanan tahmin bakiyelerini görüntüleyin. Bakiyeler, döneme göre bölünür (ay). |
| Nakit akışı tahmini | Genel muhasebeye tahsis edilmesi gereken tahmin işlemlerini görüntüleyin. Daha fazla bilgi için bkz. [Nakit akışı tahminleri](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Boyutları görüntüle | **Genel bakış** sekmesindeki ızgarada gösterilmesi gereken ürün, depolama ve izleme boyutlarını seçin. |
| Genel muhasebe önizlemesi | Seçili işlem için genel muhasebe girişlerini görüntüleyin. |
| Teklif satırlarını transfer et | Teklif satırlarını seçilen projeye transfer edin. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>Talep tahmini sayfasının Genel bakış sekmesindeki araç çubuğu komutları

Aşağıdaki tabloda, **Talep tahmini** sayfasındaki **Genel bakış** sekmesinde bulunan araç çubuğundaki komutlar açıklanmaktadır.

| Command | Tanım |
|---|---|
| Tahmini tahsis et | Bir tahsisat yöntemi kullanıyorsanız, tahmin hareketi için ayrı çizelge satırları oluşturun. Daha sonra satırın miktarı, tüm zaman dilimi için tarihe (seçilen zaman aralıklarına göre), miktara ve tutara göre dağıtılır. (Bu konunun sonraki bölümlerinde yer alan [Tahmini tahsis et](#allocate-forecast) bölümüne bakın.)|
| Toplu güncelleştirme | **Tahmin işlemlerini düzenle** sayfasını açın. (Bu bölümün ileriki kısımlarında yer alan [Tahmin hareketlerinin toplu güncelleştirme ](#bulk-update) bölümünü inceleyin.) |
| Stok tahmini | Seçili madde/model kombinasyonu için filtre uygulanan **Stok tahmini** sayfası görünümünü açın. (Bu bölümün ileriki kısımlarında yer alan [Stok tahmini](#inventory-forecast) bölümünü inceleyin.) |
| Madde gereksinimi oluştur | Projeyle ilgili tahmin hareketleri için madde gereksinimleri ve satış siparişi veya madde günlüğü satırları oluşturabileceğiniz iletişim kutusunu açın. |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>Talep tahmini sayfasındaki Genel bakış sekmesi

Aşağıdaki tabloda, **Talep tahmini** sayfasının **Genel bakış** sekmesindeki alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| **Görev adı** | Tahmin satırını oluşturmak için kullanılmış olan toplu iş görevinin adı. |
| **Model** | İşlemin ilişkili olduğu tahmin modeli. |
| **Date** | Hareketin başlangıç tarihi. |
| **Müşteri hesabı** | İşlemin ilişkili olduğu müşteri hesabı. |
| **Müşteri grubu** | İşlemin ilişkili olduğu müşteri grubu. |
| **Madde numarası** | Maddenin tanımlayıcısı. |
| **Ürün adı** | Maddenin açıklamasıdır. |
| **Madde dağıtım anahtarı** | Stok tahmini tahsisi sırasında kullanılan madde tahsis anahtarı. |
| **Satış miktarı** | Belirtilen satış birimi olarak işlem miktarı. |
| **Birim** | Maddenin satıldığı birim. |
| **Tutar** | İskontolar hariç, tahmin hareketinin tahmine katkıda bulunduğu brüt tutar. |
| **Satış fiyatı** | **Fiyat birimi** alanında belirtilen birim sayısı için satış fiyatı. Değer, madde kurulumundan otomatik olarak alınır ancak bunu değiştirebilirsiniz. |
| **Satış para birimi** | Tahmin işlemi için kullanılan para birimi kodu. Otomatik olarak girilen varsayılan para birimi, ancak farklı bir para birimi seçebilirsiniz. |
| **FA miktarı** | Belirtilen fiili ağırlık birimi cinsinden tahmin miktarı. |
| **FA birimi** | Maddenin satıldığı fiili ağırlık birimi. Değer, madde kurulumundan otomatik olarak alınır. |
| (Diğer boyutlar) | Ek ürün, depolama ve izleme boyutları, ızgarada sütunlar olarak gösterilebilir. Görüntülenen ek boyutları seçmek için Eylem Bölmesinde **Görüntüleme boyutları**'nı seçin. |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>Talep tahmini sayfasındaki Genel sekmesi

**Genel** sekmesinde, **Genel bakış** sekmesinde seçili olan satır hakkında daha fazla bilgi gösterilir. Bu bilgilerden bazıları **Genel bakış** sekmesinden yinelenir. Aşağıdaki tabloda, **Genel** sekmesinde benzersiz olan alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Talep tahmini sıra numarası | Talep tahmin satırının benzersiz numarası. Bu numara, **Master planlama parametreleri** sayfasındaki talep tahminleri için seçilen numara serisi kullanılarak oluşturulur. |
| Madde grubu | Hareketin ilişkili olduğu madde grubu. |
| Rapor al | Hareketi raporlamaya dahil etmek için bu seçeneği *Evet* olarak belirleyin. |
| Yorumlar | Tahmin hareketiyle ilgili yorumlarınızı girin. |
| Active | Hareketi bütçe raporlamaya dahil etmek için bu onay kutusunu işaretleyin. Bu onay kutusunun ayarı, hareketleri raporlamak için değiştirilemez. |
| Nakit akış tahminlerine dahil et | Tahmin hareketini genel muhasebeye tahsis etmek için bu onay kutusunu seçin. Bu onay kutusunun ayarı, hareketleri raporlamak için değiştirilemez. Daha fazla bilgi için bkz. [Nakit akışı tahminleri](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Satış vergi grubu | Tahmin hareketi için vergiyi belirtmek amacıyla kullanılan vergi grubu. |
| Madde satış vergisi grubu | Tahmin hareketi için vergiyi belirtmek amacıyla kullanılan madde vergisi grubu. |
| Yöntem | <p>Tahmin işlemini tahsis etmek için kullanılan yöntemi seçin:</p><ul><li>**Hiçbiri** – Tahsisat yoktur.</li><li>**Dönem** – Her dönem için aynı miktarı tahmin edin. Bu değeri seçerseniz, **Beher** alanında bir miktar ve **Birim** alanında bir zaman birimi belirleyin.</li><li>**Anahtar** – Tahmini, **Dönem anahtarı** alanında belirttiğiniz dönem tahsis anahtarına göre tahsis edin. Periyodik değişikliği hesaba katmak istediğinizde bu yöntemi kullanabilirsiniz.</li><ul>|
| Birim miktar | <p>Tahminin geleceğe uzandığı zaman aralıklarının sayısını girin. Bu alan yalnızca **Yöntem** alanında *Dönem* seçildiğinde kullanılabilir.</p><p>Örneğin, **Yöntem** alanında *Dönem* seçeneğini belirlediğinizde, **Beher** alanına *1* girin, **Birim** alanından *Aylar* seçeneğini belirleyin. **Bitiş** alanında, bir yıl sonraya ait bir bitiş tarihi belirtin. Bu durumda, gelecek yılın her ayı için, başlık satırında belirtilen madde ve miktara dayanan bir tahmin satırı oluşturulur. |
| Birim | Zaman aralığının birimini seçin: *Gün*, *Ay* veya *Sene*. Tahsis işlemi, **Beher** alanında belirttiğiniz gün, ay veya yıl sayısına karşılık gelir.|
| Dönem anahtarı | Tahmini tahsis etmek için kullanılan dönem tahsisat anahtarını belirtin. Daha fazla bilgi için bkz. [Bütçe planlama verileri tahsisatı](../../finance/budgeting/budget-planning-data-allocation.md). |
| Son | **Beher** ve **Birim** alanlarını kullandığınızda bitiş tarihini belirleyin. |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>Talep tahmini sayfasındaki Madde sekmesi

**Madde** sekmesinde, **Genel bakış** sekmesinde seçili olan satır hakkında daha fazla madde bilgisi gösterilir. Bu bilgilerden bazıları **Genel bakış** sekmesinden yinelenir. Aşağıdaki tabloda, **Madde** sekmesinde benzersiz olan alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Fiyata esas miktar | Satış fiyatının geçerli olduğu satış birimlerinin sayısı. Bu değer Maddeler tablosundan otomatik olarak alınır ancak bunu değiştirebilirsiniz. |
| Satış masrafları | Satış fiyatlarındaki sabit giderler. Bu giderler miktardan bağımsızdır. |
| Maliyet fiyatı | Stok birimi başına geçerli tahmin hareketinin maliyeti. Değer, Maddeler tablosundan alınır ancak bunu değiştirebilirsiniz. |
| İskonto yüzdesi | Yüzde olarak iskonto. |
| İskonto tutarı | Satış birimi başına tutar olarak iskonto. |
| Brüt tutar | İskonto uygulanmamış olan tutar. |
| Stok miktarı | Maddenin stok birimleri olarak hareket miktarı. |
| Özel ürün reçetesi kullan | Özel ürün reçetesinin ürün reçetesi numarası. |
| Özel rota kullan | Özel alt rotanın rota numarası. |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>Talep tahmini sayfasındaki Proje sekmesi

**Proje** sekmesinde, **Genel bakış** sekmesinde seçili olan satır hakkında daha fazla proje bilgisi gösterilir. Bu bilgilerden bazıları **Genel bakış**, **Genel** veya **Madde** sekmelerinden yinelenir. Aşağıdaki tabloda, **Proje** sekmesinde benzersiz olan alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Proje tarihi | Talep tahmini işleminin tarihi. |
| Proje kodu | Geçerli işlem tarafından başvurulan projenin tanımlayıcısı. |
| Finansman kaynağı | Talep tahminiyle ilişkili finansman kaynağı. |
| Faaliyet numarası | Talep tahmini hareketiyle ilişkili etkinlik. |
| Kategori | Geçerli hareketin maliyet kategorisi. |
| Satır özelliği | Hareketin bağlı olduğu durum. |
| Hareket Kodu | Talep tahmini işleminin sistem tanımlayıcısı. |
| Maliyet tutarı | Talep tahmini işleminin tutarı. |
| Birim fiyat | Birim başına fiyat. |
| Değiştiren | Seçili işlemi en son değiştiren çalışanın tanımlayıcısı. |
| Fatura tarihi | Beklenen fatura tarihini girin. |
| Eleme tarihi | Eleme tarihini görüntüleyin veya değiştirin. Tahmin oluşturulduğunda, eleme tarihi projenin bitiş tarihine ayarlanır. Projenin bitiş tarihi yoksa, proje tarihi geçerli olur. Bu alan sabit fiyatlı projeler ve yatırım projeleri için geçerlidir. |
| Maliyet ödemesi tarihi | Satınalma ödemesinin beklenen tarihini girin. |
| Satış ödemesi tarihi | Satış ödemesinin beklenen tarihi girin. |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>Talep tahmini sayfasındaki Mali boyutlar sekmesi

**Mali boyutlar** sekmesi, **Genel bakış** sekmesinde seçili satırla ilgili tüm mali boyut değerlerini gösterir.

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>Talep tahmini sayfasındaki Stok boyutları sekmesi

**Stok boyutları** sekmesi, **Genel bakış** sekmesinde seçili satırla ilgili tüm stok boyutu değerlerini gösterir.

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>Talep tahmini sayfasındaki Tahsisat ızgarası

Bir madde tahsisat anahtarı kullanıyorsanız veya bir ya da daha fazla gelecek dönem için madde tahmini girdiyseniz, **Genel bakış** sekmesindeki araç çubuğunda **Tahmin tahsisatı**'nı seçerek tahmini tahsis edebilirsiniz. Miktar daha sonra, **Tahsisat** ızgarasındaki satırlar tarafından belirtilen şekilde dağıtılır. (Bu konunun sonraki bölümlerinde yer alan [Tahmini tahsis et](#allocate-forecast) bölümüne bakın.)

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>Stok tahmini

Tedarik ve talep tahmin satırları sayfalarının, aynı madde/model kombinasyonu için filtre uygulanan **Stok tahmini** sayfası görünümünü açan bir **Stok tahmini** düğmesi vardır. Stok tahmini, aynı madde için girilen tedarik talebi ile ilgili olarak bir bakiyeyi temsil eder. Bu değer düzenlenemez. Stok tahmini, stok yönetimi ekibinin tahmin edilen dönem içinde bir maddenin eldeki stokunda beklenen değişiklikleri incelemesine yardımcı olur.

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>Stok tahmini sayfasındaki Eylem Bölmesi

Aşağıdaki tabloda, **Stok tahmini** sayfasındaki Eylem Bölmesinde yer alan komutlar açıklanmaktadır.

| Eylem | Tanım |
|---|---|
| Tedarik tahmini | Aynı madde/model/tarih kombinasyonu için filtre uygulanan **Tedarik tahmini** sayfası görünümünü açın. |
| Talep tahmini | Aynı madde/model/tarih kombinasyonu için filtre uygulanan **Talep tahmini** sayfası görünümünü açın. |
| Stok \> Görüntüleme boyutları | **Genel bakış** ızgarasında gösterilmesi gereken ürün, depolama ve izleme boyutlarını seçin. |

### <a name="the-grid-on-the-inventory-forecast-page"></a>Stok tahmini sayfasındaki ızgara

Aşağıdaki tabloda **Stok tahmini** sayfasındaki kılavuzdaki alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| **Model** | İşlemin ilişkili olduğu tahmin modeli. |
| **Madde numarası** | Maddenin tanımlayıcısı. |
| **Bütçe tarihi** | Tahmin işleminin tarihi. |
| **Tahmin türü** | İşlemin kaynağı (*Talep tahmini* veya *Tedarik tahmini*). |
| **FA miktarı** | Fiili ağırlık birimi cinsinden tahmin miktarı. |
| **Miktar** | Stok birimi cinsinden tahmin miktarı. |
| **Kümülatif FA** | Aynı madde için birden fazla tahmin satırı biriktirildiğinde, fiili ağırlık birimi cinsinden birikmiş tahmin miktarı. |
| **Alt ürün reçetesi** | Özel alt ürün reçetesinin ürün reçetesi numarası. |
| **Alt rota** | Özel alt rotanın rota numarası. |
| (Diğer boyutlar) | Ek boyutlar, ızgarada sütunlar olarak gösterilebilir. Görüntülenen ek boyutları seçmek için Eylem Bölmesinde **Stok \> Görüntüleme boyutları**'nı seçin. |

## <a name="allocate-forecast"></a><a name="allocate-forecast"></a>Tahmini tahsis et

Seçili tahmin hareketi satırlarını işlemek için aşağıdaki prosedürü kullanın. Tahmin tahsis ettiğinizde, miktar daha sonra **Tahsisat** ızgarasındaki satırlarla gösterildiği gibi dağıtılır.

1. Tahmin oluşturduğunuz varlığın türüne ve oluşturmak istediğiniz tahminin türüne bağlı olarak [Tahmin satırlarını görüntüleme ve el ile girme](#manual-entry) bölümünde açıklandığı gibi bir tedarik veya talep tahmini sayfası açın.
1. Tedarik veya talep tahmini satırları sayfasında bir tahmin satırı seçin ve ardından **Genel Bakış** sekmesindeki araç çubuğunda **Tahmini tahsis et**'i seçin.
1. **Tahmini tahsis et** iletişim kutusunda, aşağıdaki tabloda açıklanan alanları ayarlayın. (**Yöntem** alanında seçtiğiniz değer kullanılabilen diğer alanları belirler.)

    | Alan | Tanım |
    |---|---|
    | Yöntem | <p>Tahmin işlemini tahsis etmek için kullanılan yöntemi seçin:</p><ul><li>**Hiçbiri** – Tahsisat yoktur.</li><li>**Dönem** – Her dönem için aynı miktarı tahmin edin. Bu değeri seçerseniz, **Beher** alanında bir miktar ve **Birim** alanında bir zaman birimi belirleyin.</li><li>**Anahtar** – Tahmini, **Dönem anahtarı** alanında belirttiğiniz dönem tahsis anahtarına göre tahsis edin. Mevsimsel varyasyonları hesaba katmak istediğinizde bu yöntemi kullanabilirsiniz.</li><ul>|
    | Birim miktar | <p>Tahminin geleceğe uzandığı zaman aralıklarının sayısını girin. Bu alan yalnızca **Yöntem** alanında *Dönem* seçildiğinde kullanılabilir.</p><p>Örneğin, **Yöntem** alanında *Dönem* seçeneğini belirlediğinizde, **Beher** alanına *1* girin, **Birim** alanından *Aylar* seçeneğini belirleyin. Ardından, **Bitiş** alanında bir yıl sonraki bir bitiş tarihi belirtirsiniz. Bu durumda, gelecek yılın her ayı için, başlık satırında belirtilen madde ve miktara dayanan bir tahmin satırı oluşturulur. |
    | Birim | Zaman aralığının birimini seçin: *Gün*, *Ay* veya *Sene*. Tahsis işlemi, **Beher** alanında belirttiğiniz gün, ay veya yıl sayısına karşılık gelir.|
    | Dönem anahtarı | Tahmini tahsis etmek için kullanılan dönem tahsisat anahtarını belirtin. Daha fazla bilgi için bkz. [Bütçe planlama verileri tahsisatı](../../finance/budgeting/budget-planning-data-allocation.md). |
    | Son | Ayarlarınız için geçerli olan bitiş tarihini **Başına** ve **Birim** alanlarında belirtin. |

1. Ayarlarınızı onaylamak için **Tamam**'ı seçin.
1. Sonuçları aynı satır için **Tahsisat** sekmesinde inceleyebilirsiniz.

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>Tahmin hareketlerini toplu güncelleştirme

Mevcut tahmin işlemi satırlarını işlemek için bu prosedürü kullanın. Tahmin işlemi satırlarını kopyalayabilir, düzenleyebilir ve silebilirsiniz.

1. Tedarik veya talep tahmin satırları sayfasında **Toplu güncelleştirme**'yi seçin.
1. İletişim kutusunda **Filtre**'yi seçin.
1. **Aralık** sekmesinde, kopyalamak, düzenlemek veya silmek istediğiniz tahmin verilerinin kaynağını tanımlayan ölçütleri seçin. Bu veriler tahmin modeli, madde numarası ve müşteri hesabını içerebilir.
1. Seçiminizi onaylamak için **Tamam**'ı seçin.

    Veriler seçildikten sonra, **Tahmin işlemlerini düzenle** iletişim kutusunu kullanarak bunu nasıl kopyalamak, düzenlemek veya silmek istediğinizi belirleyebilirsiniz.

    > [!NOTE]
    > Filtre uygulama adımı, **Toplu düzenleme** işlevinin kullanımıyla ilgili bir önkoşuldur. Bunu atlarsanız, program **tüm** tahmin satırlarını seçer ve güncelleştirir. Bu nedenle, yanlışlıkla tekrarlanan öğe veya kaldırma işlemlerine neden olabilirsiniz.

1. **Yönetim** bölümünde, seçili tahmin hareketlerini kopyalamak mı, güncelleştirmek mi yoksa silmek mi istediğinizi seçin.
1. Tahmine ait parametreleri silmek için **Alanda değişiklikler** bölümünü kullanın. Parametrenin onay kutusunu seçip ardından kullanılabilir seçenekler arasından seçiminizi yapın. Örneğin, **Model** onay kutusunu seçin ve ardından tahmin modeli numarasını seçin. Mevcut tahmin satırları, seçili tahmin modeline kopyalanır.
1. Tahminin başlangıç ve bitiş tarihlerini ileriye veya geriye taşımak için **Dönem değişikliği** bölümünü kullanın. Onay kutusunu seçin ve ardından tahmin tarihlerinin nasıl taşınacağını tanımlamak üzere miktar ve dönem alanlarını kullanın. Başlangıç tarihini ileri taşımak için eksi bir miktar girebilirsiniz (diğer bir deyişle, tarihi daha erken yaparsınız).

    Örneğin, tahmin hareketinin başlangıç tarihini altı ay geciktirmek için, onay kutusunu seçin, miktar olarak *6* girin ve dönem olarak *Ay*'ı seçin.

1. Gerçek tahmin verilerini güncelleştirmek için **Doğru alan** bölümünü kullanın. **Alan** alanında, değiştirmek istediğiniz ölçütü seçin. **Faktör** alanında, seçtiğiniz ölçüte uygulanacak çarpım faktörünü girin veya bir toplama ya da çıkarma sabiti girin. Örneğin, ölçüt olarak *Miktar*'ı seçin ve madde miktarını 1,5 ile çarpmak için *1,5* faktörünü girin. Alternatif olarak madde miktarını 25 birim azaltmak için *-25* sabitini girin.
1. Tahmin satırlarının mali boyutlarını güncelleştirmek için **Mali boyutlar** bölümünü kullanın. Değiştirmek istediğiniz mali boyutları seçin ve seçili boyutlara uygulamak için bir değer girin.
1. Değişiklerinizi uygulamak için **Tamam**'ı seçin.

## <a name="use-forecasts-with-master-planning"></a>Tahminleri master planlama ile kullanma

Talep tahmininizi ve/veya tedarik tahminini girdikten sonra, Master planlama çalıştırıldığında beklenen talep ve/veya tedarikle ilgili dikkate alınacak tahminleri master planlama sırasında ekleyebilirsiniz. Tahminler master planlamaya dahil edildiğinde, malzeme ve kapasite için brüt gereksinimler hesaplanır ve planlı siparişler oluşturulur.

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>Bir stok tahminini dahil etmek için bir master plan ayarlama

Master planınızı bir stok tahmini içerecek şekilde yapılandırmak için bu adımları izleyin.

1. **Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Var olan bir planı seçin veya yeni bir plan oluşturun.
1. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Tahmin modeli**: Uygulanacak tahmin modelini seçin. Geçerli master plan için bir tedarik önerisi oluşturulduğunda, bu model dikkate alınır.
    - **Tedarik tahminini dahil et**: Geçerli master plana tedarik tahmini eklemek için bu seçeneği *Evet* olarak ayarlayın. *Hayır* olarak ayarlarsanız tedarik tahmini hareketleri master plana dahil edilmeyecektir.
    - **Talep tahminini dahil et**: Geçerli master plana talep tahmini eklemek için bu seçeneği *Evet* olarak ayarlayın. *Hayır* olarak ayarlarsanız talep tahmini hareketleri master plana dahil edilmeyecektir.
    - **Tahmin gereksinimlerini azaltmak için kullanılan yöntem**: Tahmin gereksinimlerini azaltmak için kullanılacak yöntemi seçin. Daha fazla bilgi için bkz. [Tahmin azaltma anahtarları](planning-optimization/demand-forecast.md#reduction-keys).

1. **Gün olarak zaman dilimleri** hızlı sekmesinde, tahminin dahil edildiği dönemi belirtmek için aşağıdaki alanları ayarlayabilirsiniz:

    - **Tahmin planı**: Ayrı kapsam gruplarından kaynaklanan tahmin planı zaman dilimini geçersiz kılmak için bu seçeneği *Evet* olarak ayarlayın. Geçerli master plan için ayrı kapsam gruplarındaki değerleri kullanmak için *Hayır* olarak ayarlayın.
    - **Tahmin zaman dönemi**: **Tahmin planı** seçeneğini *Evet* olarak ayarlarsanız, talep tahmininin uygulanması gereken gün sayısını (bugünün tarihinden itibaren) belirtin.

    > [!IMPORTANT]
    > **Tahmin planı** seçeneği Planlamayı En İyi Duruma Getirme'de henüz desteklenmemektedir.

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>Bir stok tahmini içeren bir master plan çalıştırma

Stok tahmini içeren bir master plan çalıştırmak için bu adımları izleyin.

1. **Master planlama \> Çalışma alanları \> Master planlama**'ya gidin.
1. **Master plan** alanında, önceki yordamda ayarladığınız master planı girin veya seçin.
1. **Master planlama** kutucuğunda **Çalıştır**'ı seçin.
1. **Master planlama** iletişim kutusunda, **İşlem süresini izle** seçeneğini *Evet* olarak ayarlayın.
1. **İş parçacığı sayısı** alanına bir rakam girin.
1. **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin.
1. Standart sorgu düzenleyicisi iletişim kutusu görüntülenir. **Aralık** sekmesinde **Alan** alanının *Madde numarası* olarak ayarlandığı satırı seçin.
1. **Ölçüt** alanında, plana dahil edilecek madde numarasını seçin.
1. **Tamam**'ı seçin.

Hesaplanan gereksinimleri görüntülemek için **Brüt gereksinim** sayfasını açın. Örneğin, **Serbest bırakılan ürünler** sayfasında, Eylem Bölmesinde, **Plan** sekmesinde, **Gereksinimler** grubunda **Brüt gereksinim**'i seçin.

Oluşturulan planlı siparişleri görüntülemek için **Master planlama \> Yaygın \> Planlı siparişler**'e gidin ve uygun tahmin planını seçin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Talep tahminine genel bakış](introduction-demand-forecasting.md)
- [Talep tahmini kurulumu](demand-forecasting-setup.md)
- [İstatistik temel tahmini oluşturma](generate-statistical-baseline-forecast.md)
- [Temel tahminde manüel ayarlamalar yapma](manual-adjustments-baseline-forecast.md)
- [Talep tahminleri ile master planlama](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
