---
title: Talep tahmini kurulumu
description: Bu konu başlığı, talep tahmini için hazırlamak üzere gerçekleştirmeniz gereken kurulum görevlerini açıklar.
author: ChristianRytt
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f53171361b655ab4ae05894d098203df0af8d60
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920785"
---
# <a name="demand-forecasting-setup"></a>Talep tahmini kurulumu

[!include [banner](../includes/banner.md)]

Bu konuda, talep tahmininin nasıl ayarlanacağı açıklanmaktadır.  

## <a name="item-allocation-keys"></a>Madde dağıtım anahtarları

Madde tahsisat anahtarları madde grupları oluşturur. Talep tahmini, bir öğe ve boyutları için, yalnızca o öğe bir madde tahsisat anahtarının parçasıysa hesaplanır. Bu kural, büyük öğe sayılarını gruplamak için uygulanır, böylece talep tahminleri daha hızlı oluşturulabilir. Tahminler yalnızca geçmiş veriler temel alınarak oluşturulur.

Tahmin oluşturma sırasında madde tahsisat anahtarı kullanılıyorsa, bir madde ve boyutları sadece bir madde tahsisat anahtarının parçası olmalıdır.

Madde tahsisat anahtarları oluşturmak ve bunlara bir stok tutma birimi (SKU) eklemek için aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Talep tahmini \> Madde tahsisat anahtarları**'na gidin.
1. Liste bölmesinden madde tahsisat anahtarı seçin veya Eylem Bölmesinden **Yeni**'yi seçerek yeni bir anahtar oluşturun. Yeni veya seçilen anahtarın üst bilgisinde, aşağıdaki alanları ayarlayın:

    - **Madde tahsisat anahtarı** – Anahtar için benzersiz bir ad girin.
    - **Ad**: Anahtar için açıklayıcı bir ad girin.

1. Seçili madde ayırma anahtarına madde eklemek veya maddeleri kaldırmak için aşağıdaki adımlardan birini izleyin:

    - **Madde tahsisatı** Hızlı Sekmesinde, gerektiğinde madde eklemek veya kaldırmak için araç çubuğundaki **Yeni** ve **Sil** düğmelerini kullanın. Her satır için madde numarasını seçin ve diğer sütunlara istediğiniz boyut değerlerini atayın. Kılavuzda gösterilen boyut sütunları kümesini değiştirmek için Araç çubuğunda **Boyutları görüntüle**'yi seçin. (Talep tahminleri oluşturulduğunda **Yüzde** sütunundaki değer yoksayılır.)
    - Anahtara çok sayıda madde eklemek istiyorsanız seçili anahtara birden çok madde bulabileceğiniz ve atayabileceğiniz bir sayfa açmak için Eylem Bölmesi'nde **Madde ata**'yı seçin.

> [!IMPORTANT]
> Her madde tahsisat anahtarına yalnızca ilgili maddeleri dahil etmeye dikkat edin. Microsoft Azure Machine Learning'i kullandığınızda, gereksiz maddeler artan maliyetlere yol açabilir.

## <a name="intercompany-planning-groups"></a>Şirketlerarası planlama grupları

Talep tahmini, şirketler arası tahminler oluşturabilir. Dynamics 365 Supply Chain Management'ta, birlikte planlanan şirketler aynı şirketlerarası planlama grubunda gruplandırılır. Her şirket için talep tahmininde hangi madde tahsisat anahtarlarının düşünülmesi gerektiğini belirlemek için bir madde tahsisat anahtarını şirketlerarası planlama grubu üyesi ile ilişkilendirin.

> [!IMPORTANT]
> Planlamayı En İyi Duruma Getirme, şu anda şirketlerarası planlama gruplarını desteklemiyor. Planlamayı En İyi Duruma Getirme'nin kullanıldığı şirketlerarası planlama yapmak için ilgili tüm şirketler için ana planları içeren ana planlama toplu işleri ayarlayın.

Şirketlerarası planlama gruplarınızı ayarlamak için aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Şirketlerarası planlama grupları**'na gidin.
1. Liste bölmesinden bir planlama grubu seçin veya Eylem Bölmesinden **Yeni**'yi seçerek yeni bir grup oluşturun. Yeni veya seçilen grubun üst bilgisinde, aşağıdaki alanları ayarlayın:

    - **Ad**: Planlama grubu için benzersiz bir ad girin.
    - **Açıklama**: Planlama grubu için kısa açıklama girin.

1.  **Şirketlerarası planlama grubu üyeleri** Hızlı Sekmesinde, grubun parçası olması gereken her şirket (tüzel kişilik) için bir satır eklemek üzere araç çubuğundaki düğmeleri kullanın. Her satır için aşağıdaki alanları ayarlayın:

    - **Tüzel kişilik** – Seçili grubun üyesi olan bir şirketin (tüzel kişilik) adını seçin.
    - **Planlama sırası** – Şirketin diğer şirketlere göre işlenmesi gereken sırayı atayın. Önce düşük değerler işlenir. Bir şirkete olan talep diğer şirketleri etkilediğinde bu sıra önemli olabilir. Bu durumlarda, talebi sağlayan şirket en son işlenmelidir.
    - **Ana plan** – Geçerli şirket için tetikleyecek ana planı seçin.
    - **Statik plana otomatik kopyalama** – Planın sonucunu statik plana kopyalamak için bu onay kutusunu seçin.
    - **Dinamik plana otomatik kopyalama** – Planın sonucunu dinamik plana kopyalamak için bu onay kutusunu seçin.

1. Varsayılan olarak, şirketlerarası planlama grubu üyelerine hiçbir madde tahsisat anahtarı atanmamışsa, tüm şirketlerden tüm madde tahsisat anahtarlarına atanan tüm maddeler için bir talep tahmini hesaplanır. Şirketler ve madde tahsisat anahtarları için ek filtreleme seçenekleri **İstatistiksel temel tahmin oluştur** iletişim kutusunda kullanılabilir (**Master planlama \> Tahmin \> Tale tahmini \> İstatistiksel temel tahmin oluştur**). Seçili şirketlerarası planlama grubundaki bir şirkete madde tahsisat anahtarları atamak için şirketi seçin ve **şirketlerarası planlama grubu üyeleri** Hızlı Sekmesinde araç çubuğunda **Madde tahsisat anahtarları**'nı seçin.

> [!IMPORTANT]
> Her şirketlerarası planlama grubuna yalnızca ilgili madde tahsisat anahtarlarını dahil etmeye dikkat edin. Azure Machine Learning'i kullandığınızda, gereksiz maddeler artan maliyetlere yol açabilir.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a>Talep tahmini parametrelerini ayarlama

Talep tahminlerinin sisteminizde nasıl çalışacağını denetleyen çeşitli seçenekleri ayarlamak için **Talep tahmini parametreleri** sayfasını kullanın.

### <a name="open-the-demand-forecasting-parameters-page"></a>Talep tahmini parametreleri sayfasını açma

Talep tahmin parametrelerini ayarlamak için **Master planlama \> Kurulum \> Talep tahmini \> Talep tahmini parametreleri**'ne gidin. Talep tahmini şirketler arası gerçekleştirildiği için, ayar geneldir. Başka bir deyişle, tüm tüzel kişiler (şirketler) için geçerlidir.

### <a name="general-settings"></a>Genel ayarlar

Talep tahminine yönelik genel ayarları tanımlamak için **Talep tahmini parametreleri** sayfasının **Genel** sekmesini kullanın.

#### <a name="demand-forecast-unit"></a>Talep tahmin birimi

Talep tahmini, tahmini miktar cinsinden oluşturur. Bu yüzden, miktarın ifade edileceği ölçü birimi **Talep tahmin birimi** alanında belirtilmelidir. Bu alan, her ürün için normal stok birimlerinden bağımsız olarak tüm talep tahminleri için kullanılacak birimi tanımlar. Tutarlı bir tahmin birimi kullanarak toplama ve yüzde dağılımının anlamlı olmasını sağlamaya yardımcı olursunuz. Toplam ve yüzde dağılımı hakkında daha fazla bilgi için bkz. [Temel tahmine manüel ayarlar yapma](manual-adjustments-baseline-forecast.md).

Talep tahminine dahil edilen SKU'lar için kullanılan her ölçü birimi konusunda, burada seçtiğiniz ölçü birimi ve genel tahmin ölçü birimi için bir dönüştürme kuralı olduğundan emin olun. Bir tahmin oluşturduğunuzda, ölçü birimi dönüştürmesi olmayan maddelerin listesi günlüğe kaydedilir. Bu nedenle, kurulumu kolayca düzeltebilirsiniz. Ölçü birimleri ve bunlar arasında dönüştürme hakkında daha fazla bilgi için bkz. [Ölçü birimlerini yönetme](../pim/tasks/manage-unit-measure.md).

#### <a name="transaction-types"></a>Hareket tipleri

İstatistiksel temel tahmin oluşturulduğunda kullanılan hareket tiplerini seçmek için **Hareket türleri** Hızlı Sekmesindeki alanları kullanın.

Talep tahmini bağımlı ve bağımsız talebi tahmin etmek için kullanılabilir. Örneğin, yalnızca **Satış siparişi** seçeneği *Evet* olarak ayarlanırsa ve talep tahmini için kabul edilen tüm öğeler satılan öğeler ise, sistem bağımsız talebi hesaplar. Ancak, kritik alt bileşenler madde tahsisat anahtarlarına eklenebilir ve talep tahminine eklenebilir. Bu durumda, **Üretim satırı** seçeneği *Evet* olarak ayarlanırsa bağımlı bir tahmin hesaplanır.

Madde tahsisat anahtarları sekmesini kullanarak bir veya daha fazla belirli **Madde tahsisat anahtarı** için hareket türlerini geçersiz kılabilirsiniz. Bu sekme benzer alanlar sağlar.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Temel tahminin nasıl oluşturulacağına ilişkin seçimi yapın

**Tahmin oluşturma stratejisi** alanı, temel tahmin oluşturmak için kullanılan yöntemi seçmenizi sağlar. Üç yöntem mevcuttur:

- *Geçmiş talebin üzerine kopyala* – Yalnızca geçmiş verileri kopyalayarak tahminler oluşturun.
- *Azure Machine Learning Hizmeti* – Azure Machine Learning Hizmeti'ni kullanan bir tahmin modeli kullanın. Azure Machine Learning Hizmeti, Azure için geçerli makine öğrenimi çözümüdür. Bu nedenle, bir tahmin modeli kullanmak istiyorsanız bunu kullanmanızı öneririz.
- *Azure Machine Learning* – Azure Machine Learning Studio (klasik) kullanan bir tahmin modeli kullanın. Azure Machine Learning Studio (klasik) kullanım dışı bırakıldı ve yakında Azure'dan kaldırılacak. Bu nedenle, talep tahminini ilk kez ayarlıyorsanız *Azure Machine Learning Hizmeti*'ni seçmenizi öneririz. Şu anda Azure Machine Learning Studio (klasik) kullanıyorsanız en kısa sürede Azure Machine Learning Hizmeti'ne geçmeyi planlamalısınız.

 **Madde tahsisat anahtarları** sekmesini kullanarak bir veya daha fazla belirli madde tahsisat anahtarı için tahmin oluşturma yöntemini geçersiz kılabilirsiniz. Bu sekme benzer alanlar sağlar.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Varsayılan tahmin algoritması parametrelerini genel olarak geçersiz kılma

Varsayılan tahmin algoritması parametreleri ve değerleri **Talep tahmini parametreleri** sayfasında atanır (**Master Planlama \> Kurulum \> Talep tahmini \> Talep tahmini parametreleri**). Ancak, **Talep tahmini parametreleri** sayfasının **Genel** sekmesindeki **Tahmin algoritması parametreleri** Hızlı Sekmesini kullanarak bunları genel olarak geçersiz kılabilirsiniz. (**Talep tahmini parametreleri** sayfasındaki **Madde tahsisat anahtarları** sekmesini kullanarak da belirli tahsisat anahtarları için bunları geçersiz kılabilirsiniz.)

Gerekli parametre geçersiz kılma koleksiyonunu oluşturmak için araç çubuğundaki **Ekle** ve **Kaldır** düğmelerini kullanın. Listedeki her parametre için **Ad** alanında bir değer seçin ve **Değer** alanına uygun bir değer girin. Burada listelenmeyen tüm parametreler, değerlerini **Talep tahmini parametreleri** sayfasındaki ayarlardan alır. Standart parametre kümesinin nasıl kullanılacağı ve bunlar için değerlerin nasıl seçileceği hakkında daha fazla bilgi için [Talep tahmini modelleri için varsayılan parametreler ve değerler](#model-parameters) bölümüne bakın.

### <a name="set-forecast-dimensions"></a>Tahmin boyutlarını ayarlama

Bir tahmin boyutu tahminin tanımlandığı ayrıntı düzeyini gösterir. Şirket, saha ve madde tahsisat anahtarı gerekli tahmin boyutlarıdır. Ayrıca ambar, stok durumu, müşteri grubu, müşteri hesabı, ülke/bölge, eyalet ve/veya madde düzeyinde ve tüm madde boyut düzeylerinde tahminler oluşturabilirsiniz. **Talep tahmini parametreleri** sayfasındaki **Tahmin boyutları**'nı kullanarak talep tahmini oluşturulurken kullanılacak tahmin boyutlarını da seçebilirsiniz.

Herhangi bir anda, talep tahmini için kullanılan boyutların listesine tahmin boyutlarını ekleyebilirsiniz. Ayrıca tahmin boyutlarını listeden kaldırabilirsiniz. Ancak, bir tahmin boyutu ekler veya kaldırırsanız, manüel ayarlar kaybolur.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Belirli madde tahsisat anahtarları için geçersiz kılmaları ayarlama

Tüm maddeler talep tahmini perspektifinden aynı şekilde çalışmaz. Bu nedenle, **Genel** sekmesinde tanımlanan ayarların çoğu için ayırma anahtarına özgü geçersiz kılmalar oluşturabilirsiniz. İstisna, talep tahmin birimidir. Belirli bir madde tahsisat anahtarının geçersiz kılmalarını ayarlamak için şu adımları izleyin.

1. **Talep tahmini parametreleri** sayfasında, **Madde tahsisat anahtarları** sekmesinde, araç çubuğu düğmelerini kullanarak madde tahsisat anahtarlarını soldaki kılavuza ekleyin veya istediğiniz gibi kaldırın. Ardından, geçersiz kılmaları ayarlamak istediğiniz tahsisat anahtarını seçin.
1. **Hareket türleri** Hızlı Sekmesinde, seçili tahsisat anahtarına ait ürünler için istatistiksel temel tahmini oluşturmak üzere kullanmak istediğiniz hareket türlerini etkinleştirin. Ayarlar, **Genel** sekmesinde çalıştıkları gibi çalışır ancak yalnızca seçili madde tahsisat anahtarına uygulanır. Buradaki tüm ayarlar (hem *Evet* değerleri hem de *Hayır* değerleri) **Genel** sekmesindeki tüm **Hareket türleri** ayarlarını geçersiz kılar.
1. **Tahmin algoritması parametreleri** Hızlı Sekmesinde, seçili tahsisat anahtarına ait ürünler için tahmin oluşturma stratejisini ve tahmin algoritması parametre geçersiz kılmalarını seçin. Bu ayarlar **Genel** sekmesinde çalıştıkları gibi çalışır ancak yalnızca seçili madde tahsisat anahtarına uygulanır. Gerekli parametre geçersiz kılma koleksiyonunu tanımlamak için araç çubuğundaki **Ekle** ve **Kaldır** düğmelerini kullanın. Listedeki her parametre için **Ad** alanında bir değer seçin ve **Değer** alanına uygun bir değer girin. Standart parametre kümesinin nasıl kullanılacağı ve bunlar için değerlerin nasıl seçileceği hakkında daha fazla bilgi için [Talep tahmini modelleri için varsayılan parametreler ve değerler](#model-parameters) bölümüne bakın.

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Azure Machine Learning Hizmeti bağlantısını ayarlama

**Azure Machine Learning Hizmeti** bağlantısını ayarlamak için Azure Machine Learning Hizmeti sekmesini kullanın. Bu çözüm, temel tahmini oluşturmak için seçeneklerden biridir. Bu sekmedeki ayarlar yalnızca **Tahmin oluşturma stratejisi** alanı, *Azure Machine Learning Hizmeti* olarak ayarlandığında etkilidir.

Azure Machine Learning Hizmeti'ni ayarlamak ve buradaki ayarları kullanarak hizmet bağlanma hakkında daha fazla bilgi için [Azure Machine Learning Hizmeti'ni Ayarlama](#setup-amls) bölümüne bakın.

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Azure Machine Learning Studio (klasik) bağlantısını ayarlama

> [!IMPORTANT]
> Azure Machine Learning Studio (klasik) kullanım dışı bırakıldı. Bu nedenle, artık Azure'da bunun için yeni çalışma alanları oluşturamazsınız. Benzer işlevsellik ve daha fazlasını sağlayan Azure Machine Learning Hizmeti ile değiştirilmiştir. Halihazırda Azure Machine Learning kullanmıyorsanız Azure Machine Learning Hizmeti'ni kullanmaya başlamalısınız. Azure Machine Learning Studio (klasik) için oluşturulmuş bir çalışma alanınız varsa özellik Azure'dan tamamen kaldırılana kadar kullanmaya devam edebilirsiniz. Ancak Azure Machine Learning Hizmeti'ne en kısa sürede güncelleştirmenizi öneririz. Uygulama, Azure Machine Learning Studio'nun (klasik) kullanım dışı olduğu konusunda sizi uyarmaya devam etse de, tahmin sonucu etkilenmez. Yeni Azure Machine Learning Hizmeti ve nasıl ayarlanacağı hakkında daha fazla bilgi için [Azure Machine Learning Hizmeti'ni Ayarlama](#setup-amls) bölümüne bakın.
>
> Eski Azure Machine Learning Studio (klasik) çalışma alanınız kullanılabilir olduğu sürece Supply Chain Management ile yeni ve eski makine öğrenimi çözümlerini kullanmak arasında serbestçe geçiş yapabilirsiniz.

Zaten kullanılabilir bir Azure Machine Learning Studio (klasik) çalışma alanınız varsa bunu Supply Chain Management'a bağlayarak tahminler oluşturmak için kullanabilirsiniz. **Talep tahmini parametreleri** sayfasındaki **Azure Machine Learning** sekmesini kullanarak bu bağlantıyı kurabilirsiniz. Bu sekmedeki ayarlar yalnızca **Tahmin oluşturma stratejisi** alanı, *Azure Machine Learning* olarak ayarlandığında etkilidir. Azure Machine Learning Studio (klasik) çalışma alanınız için aşağıdaki ayrıntıları girin:

- Ağ hizmeti uygulama programlama arabirimi (API) anahtarı
- Ağ hizmeti sonlanım noktası URL'si
- Azure depolama hesap adı
- Azure depolama hesap anahtarı

> [!NOTE]
> Yalnızca özel bir depolama hesabı kullanıyorsanız Azure depolama hesap adı ve anahtarı gerekir. Şirket içi sürümünü kullanıyorsanız Machine Learning hizmetinin geçmiş verilere ulaşabilmesi için Azure üzerinde özel bir depolama hesabınızın olması gerekir.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a>Talep tahmin modelleri için varsayılan parametreler ve değerler

Tahmin planlama modellerinizi oluşturmak için makine öğrenimini kullandığınızda, *algoritma parametrelerini tahmin etmek* için değerler ayarlayarak makine öğrenimi seçeneklerini kontrol edersiniz. Bu değerler Supply Chain Management'tan Azure Machine Learning'e gönderilir. Hangi tür değerlerin sağlanacağını ve her birinin hangi değerlere sahip olması gerektiğini kontrol etmek için **Tahmin algoritması parametreleri** sayfasını kullanın.

Talep tahmin modelleri için kullanılan varsayılan parametreleri ve değerleri ayarlamak için **Master Planlama \> Kurulum \> Talep tahmini \> Tahmin algoritma parametreleri** bölümüne gidin. Standart bir parametre kümesi sağlanır. Her parametrede, aşağıdaki alanlar bulunur:

- **Ad** – Azure tarafından kullanılan parametrenin adı. Genellikle, Azure Machine Learning'deki denemeyi özelleştirmediyseniz bu adı değiştirmemelisiniz.
- **Açıklama** – Parametre için ortak bir ad. Bu ad, parametreyi sistemdeki diğer yerlerde (örneğin, **Talep tahmini parametreleri** sayfasında) tanımlamak için kullanılır.
- **Değer** – Parametrenin varsayılan değeri. Girmeniz gereken değer, düzenlediğiniz parametreye bağlıdır. 
- **Açıklama** – Parametrenin kısa bir açıklaması ve nasıl kullanılacağı. Bu açıklama genellikle **Değer** alanı için geçerli değerler hakkında tavsiyeler içerir.

Aşağıdaki parametreler varsayılan olarak sağlanır. (Bu standart listeye geri dönmeniz gerekiyorsa Eylem Bölmesi'nde **Geri Yükle**'yi seçin.)

- **Güven düzeyi yüzdesi**: Güven aralığı, talep tahmini için iyi tahminler görevi gören bir değer aralığıdır. Yüzde 95'lik bir güven düzeyi yüzdesi, gelecekteki talep tahmininin güven aralığı sınırlarının dışına çıkma konusunda yüzde 5'lik bir risk bulunduğunu gösterir.
- **Mevsimliği zorla** –  Modelin belirli bir mevsimsellik türü kullanması için zorlanıp zorlanmayacağını belirtir. Bu parametre, yalnızca ARIMA ve ETS için geçerlidir. Seçenekler: *OTOMATİK (varsayılan)*, *YOK*, *TOPLAMSAL*, *ÇARPIMSAL*.
- **Tahmin modeli** – Hangi tahmin modelinin kullanılacağını belirtir. Seçenekler: *ARIMA*, *ETS*, *STL*, *ETS+ARIMA*, *ETS+STL*, *TÜMÜ*. En uygun modeli seçmek için *TÜMÜ* seçeneğini kullanın.
- **Maksimum tahmin edilen değer**: Tahminler için kullanılacak maksimum değeri belirtir. Biçim: +1E[n] veya sayısal sabit değer.
- **Minimum tahmin edilen değer**: Tahminler için kullanılacak minimum değeri belirtir. Biçim: -1E[n] veya sayısal sabit değer.
- **Eksik değer değiştirme**: Geçmiş verilerindeki boşlukların nasıl doldurulacağını belirtir. Seçenekler: *(sayısal değer)*, *ORTALAMA*, *ÖNCEKİ*, *DOĞRUSAL İLİŞKİLENDİR*, *POLİNOM İLİŞKİLENDİR*.
- **Eksik değer değiştirme kapsamı**: Değer değiştirmenin yalnızca her bir ayrıntı düzeyi özniteliğinin tarih aralığına mı yoksa tüm veri kümesine mi uygulanacağını belirtir. Sistemin geçmiş verilerdeki boşlukları doldururken kullandığı tarih aralığını belirlemek için aşağıdaki seçenekler kullanılabilir:

    - *GENEL* – Sistem, tüm parçalı yapı özniteliklerinin tüm tarih aralığını kullanır.
    - *HISTORY_DATE_RANGE* – Sistem, **İstatistiksel temel tahmin oluştur** iletişim kutusundaki **Geçmiş dönem** bölümündeki **Başlangıç tarihi** ve **Bitiş tarihi** alanlarıyla tanımlanan belirli bir tarih aralığı kullanır.
    - *GRANULARITY_ATTRIBUTE* – Sistem, şu anda işlenen parçalı yapı özniteliğinin tarih aralığını kullanır.

    > [!NOTE]
    > Ayrıntı düzeyi özniteliği, tahminin yapıldığı tahmin boyutlarının bir birleşimidir. **Talep tahmin parametreleri** sayfasında tahmin boyutlarını tanımlayabilirsiniz.

- **Mevsimsellikle ilgili ipucu**: Mevsimsel veriler için tahmin doğruluğunu iyileştirmek amacıyla tahmin modeline bir ipucu sağlar. Biçim: bir talep deseninin kendisini tekrarlayacağı demet sayısını temsil eden tamsayı. Örneğin, her 6 ayda bir yinelenen veriler için *6* girin.
- **Test kümesi boyut yüzdesi**: Tahmin doğruluğu hesaplamada test kümesi olarak kullanılacak geçmiş verilerin yüzdesi.

**Master Planlama \> Kurulum \> Talep tahmini \> Talep tahmin parametreleri** bölümüne giderek bu parametrelerin değerlerini geçersiz kılabilirsiniz. **Talep tahmini parametreleri** sayfasında, parametreleri aşağıdaki şekillerde geçersiz kılabilirsiniz:

- Parametreleri genel olarak geçersiz kılmak için **Genel** sekmesini kullanın.
- Belirli madde tahsisat anahtarlarının parametrelerini geçersiz kılmak için **Madde tahsisat anahtarları** sekmesini kullanın. Bir madde tahsisat anahtarı için geçersiz kılınan parametreler sadece o madde tahsisat anahtarı ile ilişkilendirilen öğelerin tahminini etkiler.

> [!NOTE]
> **Tahmin algoritması parametreleri** sayfasında, Eylem Bölmesindeki düğmeleri kullanarak listeye parametre ekleyebilir veya listeden parametreleri kaldırabilirsiniz. Ancak, genellikle, Azure Machine Learning'deki denemeyi özelleştirmediyseniz bu yaklaşımı kullanmamalısınız.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a>Azure Machine Learning Hizmeti'ni ayarlama

Supply Chain Management, kendi Azure aboneliğinizde ayarlamanız ve çalıştırmanız gereken Azure Machine Learning Hizmeti'ni kullanarak talep tahminlerini hesaplar. Bu bölümde, Azure'da Azure Machine Learning Hizmeti'nin nasıl ayarlanacağı ve ardından Supply Chain Management ortamınıza nasıl bağlanacağı açıklanmaktadır.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Özellik yönetiminde Azure Machine Learning Hizmeti'ni etkinleştirme

Talep tahmini için Azure Machine Learning Hizmeti'ni kullanabilmeniz için önce, tümleştirmeyi etkinleştirmek için Supply Chain Management'taki bir özelliği etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Master planlama*
- **Özellik adı:** *Talep tahmini için Azure Machine Learning Hizmeti*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a>Azure'da makine öğrenimini ayarlama

Azure'un tahminlerinizi işlemek için makine öğrenimini kullanmasını sağlamak için bu amaçla bir Azure Machine Learning çalışma alanı ayarlamanız gerekir. İki seçeneğiniz vardır:

- Microsoft tarafından sağlanan bir komut dosyasını çalıştırarak çalışma alanını ayarlamak için [Seçenek 1: Machine Learning çalışma alanı bölümünüzü otomatik olarak ayarlamak üzere bir komut dosyası çalıştırma](#ml-workspace-script) bölümündeki yönergeleri izleyin ve ardından [Supply Chain Management'ta Azure Machine Learning Hizmeti bağlantı parametrelerini ayarlama](#demand-forecast-parameters) bölümüne geçin.
- Çalışma alanınızı el ile ayarlamak için [Seçenek 2: Makine öğrenimi çalışma alanınızı el ile ayarlama](#ml-workspace-manual) bölümündeki yönergeleri izleyin ve ardından [Supply Chain Management'ta Azure Machine Learning Hizmeti bağlantı parametrelerini ayarlama](#demand-forecast-parameters) bölümüne geçin. Bu seçenek daha fazla zaman alır ancak size daha fazla kontrol sağlar.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a>Seçenek 1: Machine Learning çalışma alanınızı otomatik olarak ayarlamak için bir komut dosyası çalıştırma

Bu bölümde, Microsoft tarafından sağlanan otomatik bir komut dosyası kullanarak Machine Learning çalışma alanınızı nasıl kuracağınız açıklanmaktadır. İsterseniz [Seçenek 2: Machine Learning çalışma alanınızı el ile ayarlama](#ml-workspace-manual) bölümündeki yönergeleri izleyerek tüm kaynakları el ile ayarlayabilirsiniz. Her iki seçeneği de tamamlamanız gerekmez.

1. GitHub'da, [Azure Machine Learning ile Dynamics 365 Supply Chain Management talep tahmini için şablonlar](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) deposunu açın ve şu dosyaları indirin:

    - quick_setup.ps1
    - sampleInput.csv
    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Bir PowerShell penceresi açın ve önceki adımda indirdiğiniz **quick_setup.ps1** komut dosyasını çalıştırın. Ekrandaki yönergeleri izleyin. Komut dosyası gerekli çalışma alanını, depolamayı, varsayılan veri deposu ve işlem kaynaklarını ayarlar. Ancak, yine de bu yordamın kalan adımlarını izleyerek gerekli işlem hatlarını oluşturmanız gerekir. (Ardışık düzenler, Supply Chain Management'tan komut dosyalarını tahmin etmeye başlamak için bir yol sağlar.)
1. Azure Machine Learning Studio'da, 1. adımda indirdiğiniz **sampleInput.csv** dosyasını *demplan-azureml* adlı kapsayıcıya yükleyin. (Bu kapsayıcıyı quick_setup.ps1 komut dosyası oluşturdu.) Bu dosya ardışı düzeni yayımlamak ve bir test tahmini oluşturmak için gereklidir. Yönergeler için bkz. [Bir blok blobunu yükleme](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).
1. Azure Machine Learning Studio'da, gezginden **Notebooks**'u seçin.
1. **Dosyalar** yapısında aşağıdaki konumu bulun: **Users/\[geçerli kullanıcı\]/src**.
1. 1. adımda indirdiğiniz kalan dört dosyayı önceki adımda bulduğunuz konuma yükleyin.
1. Yeni yüklediğiniz **api_trigger.py** dosyasını seçin ve çalıştırın. API aracılığıyla tetiklenebilecek bir ardışık düzen oluşturur.
1. Çalışma alanınız artık ayarlandı. [Supply Chain Management'ta Azure Machine Learning Hizmeti bağlantı parametrelerini ayarlama](#demand-forecast-parameters) bölümüne geçin.

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a>Seçenek 2: Machine Learning çalışma alanınızı el ile ayarlama

Bu bölümde, Machine Learning çalışma alanınızı el ile nasıl ayarlayacağınız açıklanmaktadır. Bu bölümdeki yordamları, yalnızca [Seçenek 1: Machine Learning çalışma alanınızı ayarlamak için bir komut dosyası çalıştırma](#ml-workspace-script) bölümünde açıklandığı gibi otomatik kurulum komut dosyasını çalıştırmamaya karar verdiyseniz tamamlamanız gerekir.

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a>Adım 1: Yeni çalışma alanı oluşturun

Yeni bir Machine Learning çalışma alanı oluşturmak için aşağıdaki yordamı kullanın.

1. Azure portalınızda oturum açın.
1. **Machine Learning** hizmetini açın.
1. **Oluştur** sihirbazını açmak için araç çubuğunda **Oluştur**'u seçin.
1. Ekrandaki yönergeleri izleyerek sihirbazı tamamlayın. Çalışırken aşağıdaki noktaları aklınızda bulundurun:

    - Bu listedeki diğer noktalar farklı ayarlar önermediği sürece varsayılan ayarları kullanın.
    - Supply Chain Management örneğinizin dağıtıldığı bölgeyle eşleşen coğrafi bölgeyi seçtiğinizden emin olun. Aksi takdirde, verilerinizin bir kısmı bölge sınırlarından geçebilir. Daha fazla bilgi için bu konunun sonraki kısımlarında yer alan [gizlilik bildirimi](#privacy) bölümüne bakın.
    - Kaynak grupları, depolama hesapları, kapsayıcı kayıtları, Azure anahtar kasaları ve ağ kaynakları gibi ayrılmış kaynakları kullanın.
    - Sihirbazın **Azure Machine Learning Hizmeti bağlantı parametrelerini ayarlama** sayfasında, bir depolama hesabı adı sağlamanız gerekir. Talep tahminine ayrılmış bir hesap kullanın. Talep tahmini giriş ve çıkış verileri bu depolama hesabında depolanır.

Daha fazla bilgi için bkz. [Çalışma alanı oluşturma](/azure/machine-learning/quickstart-create-resources#create-the-workspace).

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a>2. Adım: Depolama alanını yapılandırın

Depolama alanınızı ayarlamak için aşağıdaki yordamı kullanın:

1. GitHub'da, [Azure Machine Learning ile Dynamics 365 Supply Chain Management talep tahmini için şablonlar](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) deposunu açın ve **sampleInput.csv** dosyasını indirin.
1. [Adım 1: Yeni bir çalışma alanı oluşturma](#create-workspace) bölümünde oluşturduğunuz depolama hesabını açın.
1. *demplan-azureml* adlı bir kapsayıcı oluşturmak için [Kapsayıcı oluşturma](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) bölümündeki yönergeleri izleyin.
1. 1. adımda indirdiğiniz **sampleInput.csv** dosyasını yeni oluşturduğunuz kapsayıcıya yükleyin. Bu dosya ardışı düzeni yayımlamak ve bir test tahmini oluşturmak için gereklidir. Yönergeler için bkz. [Bir blok blobunu yükleme](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).

##### <a name="step-3-configure-a-default-datastore"></a>3. Adım: Varsayılan bir veri deposu yapılandırın

Varsayılan veri deponuzu ayarlamak için aşağıdaki yordamı kullanın.

1. Azure Machine Learning Studio'da gezginde **Veri Depoları**'nı seçin.
1. [Adım 2: Depolamayı yapılandırma](#config-storage) bölümünde oluşturduğunuz *demplan-azureml* Blob depolama kapsayıcısını gösteren *Azure Blob Depolama* türünde yeni bir veri deposu oluşturun. (Yeni veri deposunun kimlik doğrulama türü *Hesap anahtarı* ise oluşturulan depolama hesabı için bir hesap anahtarı sağlayın. Yönergeler için bkz. [Depolama hesabı erişim anahtarlarını yönetme](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal).
1. Ayrıntılarını açıp **Varsayılan veri deposu olarak ayarla**'yı seçerek yeni veri deponuzu varsayılan veri deposu yapın.

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a>Adım 4: İşlem kaynaklarını yapılandırın

Tahmin oluşturma komut dosyalarınızı çalıştırmak üzere Azure Machine Learning Studio'da bir işlem kaynağı ayarlamak için aşağıdaki yordamı kullanın.

1. [Adım 1: Yeni çalışma alanı oluşturun](#create-workspace) bölümünde oluşturduğunuz Machine Learning çalışma alanının ayrıntılar sayfasını açın. **Studio web URL'i** değerini bulun ve açmak için bağlantıyı seçin.
1. Gezinti bölmesinden, **Bilgi İşlem**'i seçin.
1. **İşlem örnekleri** sekmesinde, yeni bir işlem örneği oluşturmanıza yardımcı olacak bir sihirbaz açmak için **Yeni**'yi seçin. Ekrandaki yönergeleri izleyin. İşlem örneği, talep tahmin ardışık düzeni oluşturmak için kullanılır (Ardışık düzen yayımlandıktan sonra silinebilir.) Varsayılan ayarları kullanın.
1. **İşlem kümeleri** sekmesinde, yeni bir işlem kümesi oluşturmanıza yardımcı olacak bir sihirbaz açmak için **Yeni**'yi seçin. Ekrandaki yönergeleri izleyin. İşlem kümesi, talep tahminleri oluşturmak için kullanılacaktır. Ayarları, çalıştırmanın performansını ve maksimum paralelleştirme düzeyini etkiler. Aşağıdaki alanları ayarlayın ancak diğer tüm alanlar için varsayılan ayarları kullanın:

    - **Ad** – *e2ecpucluster* girin.
    - **Sanal makine boyutu** – Bu ayarı, talep tahmini için giriş olarak kullanmayı planladığınız veri hacmine göre ayarlayın. Düğüm sayısı 11'i geçmemelidir çünkü talep tahmini oluşturmayı tetiklemek için bir düğüm gereklidir ve daha sonra bir tahmin oluşturmak için kullanılabilecek maksimum düğüm sayısı 10'dur. ([Adım 5: Ardışık düzen oluşturun](#create-pipelines) bölümündeki parameters.py dosyasında düğüm sayısını da ayarlayacaksınız.) Her düğümde, tahmin komut dosyalarını paralel olarak çalıştıran birkaç alt işlem olacaktır. İşinizdeki toplam çalışan sayısı, *Bir düğümün sahip olduğu çekirdek sayısı* x *Düğüm sayısı* şeklindedir. Örneğin, işlem kümenizde *Standart\_D4* (sekiz çekirdek) türü ve en fazla 11 düğüm varsa ve `nodes_count` değeri parameters.py dosyasında *10* olarak ayarlanmışsa etkili paralellik düzeyi 80'dir.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a>5. Adım: Ardışık düzen oluşturun

Ardışık düzenler, Supply Chain Management'tan komut dosyalarını tahmin etmeye başlamak için bir yol sağlar. Gerekli ardışık düzenleri oluşturmak için aşağıdaki yordamı kullanın.

1. GitHub'da, [Azure Machine Learning ile Dynamics 365 Supply Chain Management talep tahmini için şablonlar](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) deposunu açın ve şu dosyaları indirin:

    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Azure Machine Learning Studio'da, gezginden **Notebooks**'u seçin.
1. **Dosyalar** yapısında aşağıdaki konumu bulun: **Users/\[geçerli kullanıcı\]/src**.
1. 1. adımda indirdiğiniz dört dosyayı önceki adımda bulduğunuz konuma yükleyin.
1. Azure'da, yeni yüklediğiniz **parameters.py** dosyasını açın ve gözden geçirin. `nodes_count` değerinin, [Adım 4: İşlem kaynaklarını yapılandırın](#config-compute-resources) bölümünde işlem kümesi için yapılandırdığınız değerden bir küçük olduğundan emin olun. `nodes_count` değeri, işlem kümesindeki düğüm sayısından büyük veya buna eşitse ardışık düzen çalıştırması başlatılabilir. Ancak daha sonra gerekli kaynakları beklerken yanıt vermeyi durdurur. Düğüm sayısı hakkında daha fazla bilgi için [Adım 4: İşlem kaynaklarını yapılandırın](#config-compute-resources) bölümüne bakın.
1. Yeni yüklediğiniz **api_trigger.py** dosyasını seçin ve çalıştırın. API aracılığıyla tetiklenebilecek bir ardışık düzen oluşturur.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a>Yeni bir Active Directory uygulaması ayarlama

Hizmet sorumlusu kullanarak talep tahminine ayrılmış kaynaklarla kimlik doğrulaması yapmak için bir Active Directory uygulaması gerekir. Bu nedenle, uygulamanın tahmini oluşturmak için gereken en düşük ayrıcalık düzeyine sahip olması gerekir.

1. Azure portalınızda oturum açın.
1. Kiracının Azure Active Directory'sine (Azure AD) yeni bir uygulama kaydedin. Talimatlar için bkz. [kaynaklara erişebilen bir Azure AD uygulaması ve hizmet sorumlusu oluşturmak için portalı kullanma](/azure/active-directory/develop/howto-create-service-principal-portal).
1. Sihirbazı tamamlarken ekrandaki yönergeleri izleyin. Varsayılan ayarları kullanın.
1. Yeni Active Directory uygulamanıza [Azure'da Machine Learning'i ayarlama](#ml-workspace) bölümünde oluşturduğunuz aşağıdaki kaynaklara erişim izni verin. Yönergeler için bkz. [Azure portal kullanarak Azure rollerini atama](/azure/role-based-access-control/role-assignments-portal?tabs=current). Bu adım, sistemin tahmin verilerini içeri ve dışarı aktarmasını ve Supply Chain Management'tan makine öğrenimi ardışık düzeni çalıştırmalarını tetiklemesini sağlar.

    - Machine Learning çalışma alanına katkıda bulunan rolü
    - Ayrılmış depolama hesabına katkıda bulunan rolü
    - Ayrılmış depolama hesabına Depolama Blobu Veri Katkıda Bulunan rolü

1. Oluşturduğunuz uygulamanın **Sertifikalar ve gizli diziler** bölümünde, uygulama için bir gizli dizi oluşturun. Yönergeler için bkz. [Bir gizli anahtar ekleme](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).
1. Uygulama kimliğini ve gizli dizisini not edin. Supply Chain Management'taki **Talep tahmin parametreleri** sayfasını ayarladığınızda, bu uygulamanın ayrıntılarına daha sonra ihtiyacınız olacaktır.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a>Supply Chain Management'ta Azure Machine Learning Hizmeti bağlantı parametrelerini ayarlama

Supply Chain Management ortamınızı Azure'da yeni ayarladığınız Machine Learning hizmetine bağlamak için aşağıdaki yordamı kullanın.

1. Supply Chain Management'ta oturun açın.
1. **Master planlama \> Kurulum \> Talep tahmini \> Talep tahmini parametreleri**'ne gidin.
1.  **Genel** sekmesinde, **Tahmin oluşturma stratejisi** alanının *Azure Machine Learning Hizmeti* olarak ayarlı olduğundan emin olun.
1. **Madde tahsisat anahtarları** sekmesinde, **Talep tahmini** için *Azure Machine Learning Hizmeti*'ni kullanması gereken her tahsisat anahtarı için Tahmin oluşturma stratejisi alanının Azure Machine Learning Hizmeti olarak ayarlı olduğundan emin olun.
1. **Azure Machine Learning Hizmeti** sekmesinde, aşağıdaki alanları ayarlayın:

    - **Kiracı Kimliği** – Azure kiracınızın kimliğini girin. Supply Chain Management, Azure Machine Learning Hizmeti ile kimlik doğrulaması yapmak için bu kimliği kullanır. Kiracı kimliğinizi Azure portal'daki Azure AD **Genel Bakış** sayfasında bulabilirsiniz.
    - **Hizmet sorumlusu uygulama kimliği** – [Active Directory Uygulaması](#aad-app) bölümünde oluşturduğunuz uygulamanın uygulama kimliği girin. Bu değer, Azure Machine Learning Hizmeti'ne API isteklerini yetkilendirmek için kullanılır.
    - **Hizmet sorumlusu gizli dizisi** – [Active Directory Uygulaması](#aad-app) bölümünde oluşturduğunuz uygulama için hizmet sorumlusu uygulama gizli dizisini girin. Bu değer, Azure Depolama ve Azure Machine Learning çalışma alanına karşı yetkili işlemler gerçekleştirmek üzere oluşturduğunuz güvenlik sorumlusunun erişim belirtecini almak için kullanılır.
    - **Depolama hesabı adı** – Azure çalışma alanınızda kurulum sihirbazını çalıştırdığınızda belirttiğiniz Azure depolama hesabı adını girin. (Daha fazla bilgi için [Azure'da makine öğrenimini ayarlama](#ml-workspace) bölümüne bakın.)
    - **Ardışık düzen uç noktası adresi** – Azure Machine Learning Hizmeti'niz için ardışık düzen REST uç noktasının URL'sini girin. [Azure'da makine öğrenimini ayarlarken](#ml-workspace) bu ardışık düzeni son adım olarak oluşturdunuz. Ardışık düzen URL'sini almak için Azure portalınızda oturum açın, gezintide **Ardışık Düzenler**'i seçin. **Ardışık Düzen** sekmesinde, **TriggerDemandForecastGeneration** adlı ardışık düzen uç noktasını seçin. Ardından gösterilen REST uç noktasını kopyalayın.

    ![Talep tahmini parametreleri sayfasının Azure Machine Learning Hizmeti sekmesindeki parametreler.](media/azure-ml-service-parameters.png "Talep tahmini parametreleri sayfasının Azure Machine Learning Hizmeti sekmesindeki parametreler")

## <a name="privacy-notice"></a><a name="privacy"></a>Gizlilik bildirimi

Tahmin oluşturma stratejiniz olarak *Azure Machine Learning Hizmeti*'ni seçtiğinizde, Supply Chain Management toplanan miktarlar, ürün adları ve bunların ürün boyutları, sevkiyat ve teslim alma konumları, müşteri tanımlayıcıları ve ayrıca tahmin parametreleri gibi müşteri verilerinizi geçmiş talep için gelecekteki talepleri tahmin etmek amacıyla Machine Learning çalışma alanınızın ve bağlı depolama hesabının bulunduğu coğrafi bölgeye otomatik olarak gönderir. Azure Machine Learning Hizmeti, Supply Chain Management'ın dağıtıldığı coğrafi bölgeden farklı bir coğrafi bölgede olabilir. Bazı kullanıcılar, **Talep tahmini parametreleri** sayfasında tahmin oluşturma stratejisini seçerek bu işlevselliğin etkinleştirilip etkinleştirilmediğini denetleyebilir. 

## <a name="additional-resources"></a>Ek kaynaklar

- [Talep tahminine genel bakış](introduction-demand-forecasting.md)
- [İstatistik temel tahmini oluşturma](generate-statistical-baseline-forecast.md)
- [Temel tahminde manüel ayarlamalar yapma](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
