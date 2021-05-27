---
title: Varış yeri maliyetlerini tahmin etme ve yönetme
description: Sistem, varış yeri maliyetiniz için bir tahmin belirlemek üzere otomatik maliyet kurulumunuzu kullanır. Bu konuda, daha doğru bir tahmin sunmak için çeşitli senaryoları nasıl tanımlayabileceğiniz açıklanmaktadır.
author: sherry-zheng
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 174b80adbe61c455983307c6065b75704ce93ce9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021268"
---
# <a name="estimate-and-manage-landed-costs"></a>Varış yeri maliyetlerini tahmin etme ve yönetme

[!include [banner](../../includes/banner.md)]

Sistem, varış yeri maliyetiniz için bir tahmin belirlemek üzere [otomatik maliyet kurulumunuzu](auto-cost-setup.md) kullanır. Ayrıca, daha doğru bir tahmin sunmak için çeşitli senaryolar tanımlayabilirsiniz. Bu senaryolar depolanır. Böylece, bunları daha sonra gözden geçirebilir ve bir rapordaki fiili değerlerle karşılaştırabilirsiniz. Madde fiyatını da güncelleştirebilirsiniz.

## <a name="set-up-cost-estimates"></a>Maliyet tahminlerini ayarlama

### <a name="set-up-cost-templates"></a>Maliyet şablonlarını ayarla

Maliyet şablonları, tahmini alan kullanıcıların bilmeyebileceği varsayılan ayarları oluşturur. Şablonlar, kullanıcıların doğru bir tahmin elde etmek için belirtmesi gereken seçimleri en aza indirerek tahmin sürecindeki karmaşıklığı azaltmaya yardımcı olabilir. Standart maliyet modelini kullanıyorsanız malların maliyetini ayarlarken maliyet şablonlarını kullanabilirsiniz.

Maliyet şablonlarını ayarlamak için **Varış yeri maliyeti \> Maliyetlendirme kurulumu \> Maliyet şablonları**'na gidin. **Maliyet şablonları** sayfasında, soldaki liste bölmesi tüm geçerli maliyet şablonlarını gösterir. Şablon oluşturmak, silmek ve düzenlemek için Eylem Bölmesindeki düğmeleri kullanabilirsiniz.

Aşağıdaki tabloda, her şablonda kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Maliyet şablonu | Maliyet şablonu için benzersiz bir ad girin. Ad genellikle şablonun faktörünü veya maliyet çarpanını açıklar. |
| Tanım | Maliyet şablonu için açıklama girin. |
| Sevkiyat şirketi | Şablon kullanıldığında uygulanması gereken sevkiyat şirketini seçin. |
| Teslimat şekli | Şablon kullanıldığında uygulanması gereken deniz veya hava gibi teslimat şeklini seçin. Bu alan, maliyet tahmininde mallarla ilişkili otomatik maliyetlerin belirlenmesine yardımcı olur. |
| Sevkiyat konteyneri türü | Şablon kullanıldığında uygulanması gereken sevkiyat konteyneri türünü seçin. Bu alan, maliyet tahmininde mallarla ilişkili otomatik maliyetlerin belirlenmesine yardımcı olur. |
| Gümrük müşaviri | Şablon kullanıldığında uygulanması gereken gümrük müşaviri (satıcı). Bu alan, maliyet tahminiyle ilişkili otomatik maliyetlerin belirlenmesine yardımcı olur. |
| Faktör | Şablon kullanıldığında maliyet tahminine otomatik olarak uygulanması gereken çarpanı (yüzde) girin. Örneğin, hesaplanan maliyet tahminine yüzde 10 eklemek için *1,10* girin. |

### <a name="create-a-cost-estimate"></a>Maliyet tahmini oluşturma

Seçili maliyet şablonlarını, seçili madde kümesini ve yolculuğun diğer ayrıntılarını temel alan yeni bir maliyet tahmini oluşturmak için **Maliyet tahmini** iletişim kutusunu kullanın. Bu ayarlar daha sonra malların tahmini varış yeri maliyetlerini belirlemek için kullanılır. Bu maliyet tahminleri öncelikle standart maliyet maddeleri ile çalışmak için kullanılır. Tahmini varış yeri maliyetlerini stoktaki malların standart maliyetine ekleyerek mallar bir seyahate eklendiğinde daha küçük fark işlemleri ortaya çıkmalıdır çünkü standart maliyet bu varış yeri maliyetlerinin tahminlerini yansıtacaktır.

**Maliyet tahmini** iletişim kutusunu açmak için **Varış yeri maliyeti \> Periyodik görevler \> Maliyet tahmini**'ne gidin. Ardından, aşağıdaki alt bölümlerde açıklanan alanları ayarlayın. Son olarak tahmini oluşturmak için **Tamam**'ı seçin. Daha sonra **Maliyet tahmini** sayfası **(Varış yeri maliyeti \> Sorgular \> Maliyet tahminleri)** görünür ve bu konuda daha sonra açıklanacağı üzere yeni tahmininizi gösterir.

### <a name="settings-on-the-parameters-tab"></a>Parametreler sekmesindeki ayarlar

Aşağıdaki tablo, **Maliyet tahmini** iletişim kutusunun **Parametreler** sekmesinde kullanılabilen alanları tanımlar.


| Alan | Tanım |
|---|---|
| Maliyet şablonu | Maliyet şablonu seçin. Seçili şablonla ilişkili ayarlar, uygulanan otomatik maliyetleri belirlemek için kullanılır. |
| Tahmin tarihi | Varsayılan olarak bu alan bugünün tarihine ayarlanır ancak değeri değiştirebilirsiniz. Belirtilen tarih, uygun satış fiyatlarını, satın alma fiyatlarını, otomatik maliyetleri ve sevkiyat ücreti kullanılıyorsa döviz kurunu seçmek için kullanılır. |
| Ölçüm | Maliyetler bir ölçüme bağlı olabilir. Örneğin, hava taşımacılığı kullanıldığında hacimsel fiyatlandırma uygulanabilir. Maliyet bir ölçüme bağlıysa bu ölçümün değerini girin. Aksi takdirde, ölçüm kullanılarak herhangi bir değerlendirmenin gerçekleşmediğinden emin değilseniz bu alanı *1* olarak ayarlamanızı öneririz. Ondalık bir değer girin. Birim, ilgili otomatik maliyet kaydında tanımlanan birimdir. |
| Yolculuk şablonu | [Yolculuk şablonu](multi-leg-journey-setup.md) seçin. Bu alan, uygulanması gereken doğru otomatik maliyetleri belirlemek için kullanılır. |
| Çıkış limanı | Maddelerin sevk için alınacağı çıkış limanı. Bu alan, seçili yolculuk şablonu temel alınarak ayarlanır. |
| Varış limanı | Maddelerin sevk edileceği varış limanı. Bu alan, seçili yolculuk şablonu temel alınarak ayarlanır. |
| Para Birimi | Maddelerin satın alınacağı para birimini seçin. |
| Konteynerler | Genellikle birden çok konteyner kullanılıyorsa konteyner sayısını belirtin. Sistem daha sonra maliyetleri tahmin ettiğinde birden fazla konteyner için maliyetleri kullanır. |
| Folyolar | Genellikle birden çok folyo kullanılıyorsa miktarı belirtin. (Miktar genellikle *1*'dir.) |
| Tesis | Malların teslim edileceği tesisi belirtin. |

### <a name="settings-on-the-items-tab"></a>Maddeler sekmesindeki ayarlar

**Maddeler** sekmesinde, tahmine istediğiniz kadar madde ekleyebilirsiniz. Kılavuza madde eklemek veya maddeleri kaldırmak için araç çubuğunu kullanın. Kılavuza boyut sütunları ekleyebileceğiniz veya sütunları kaldırabileceğiniz bir iletişim kutusu açmak için araç çubuğunda **Stok \> Görüntüleme boyutları**'nı seçin.

Aşağıdaki tabloda, her maddede kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Madde kodu | Fiyatını belirlemek için maddeyi seçin. (Madde henüz sistemde yoksa işlevsiz bir madde oluşturun, isteğe bağlı olarak bunu bir seyahat maddesi maliyet grubuna ekleyin ve fiyatı boş bırakın veya fiyat oluşturun ya da değiştirin.) |
| Satıcı hesabı | Bu maddenin tahmini için kullanılacak satıcıyı seçin. Maddeye varsayılan satıcı atanmışsa bu alan otomatik olarak ayarlanır. |
| Miktar | Satın alacağınız miktarı seçin. |
| Maliyet fiyatı | Sistem, başlangıç fiyatını bulmak için fiyatlandırma kurallarını kullanır ancak gerekirse bu fiyatı geçersiz kılabilirsiniz. |
| Satış fiyatı | Malların beklenen satış fiyatını girin. |
| Ölçüm | Malların ölçümü için ondalık değer girin. Birim, ilgili piyasaya sürülecek ürün için ayarlanan birimdir. |
| Madde ağırlığını/hacmini güncelleştir | Piyasaya sürülen ürünün ağırlık veya hacim ölçümünü, bu satır için girilen **Ölçüm** değeriyle eşleşecek şekilde güncelleştirmek için bu onay kutusunu işaretleyin. |
| (Diğer boyutlar) | Göstermeyi seçtiğiniz boyutlara bağlı olarak her madde hakkında ek bilgi sütunları görebilirsiniz. |

Bir maddenin birim ve/veya ağırlık ayrıntılarını görüntülemek veya ayarlamak için kılavuzdan maddeyi seçin ve sayfanın altındaki alanları kullanın.

## <a name="manage-estimated-costs"></a>Tahmini maliyetleri yönetme

Oluşturduğunuz maliyet tahminlerini görüntülemek ve düzenlemek için **Varış yeri maliyeti \> Sorgular \> Maliyet tahminleri**'ne gidin. **Maliyet tahminleri** sayfasında, soldaki liste bölmesi tüm geçerli maliyet tahminlerini gösterir. Seçili bir tahminle çalışmak için Eylem Bölmesindeki düğmeleri kullanabilirsiniz. **Maliyet tahminleri** sayfasından yeni bir maliyet tahmini oluşturamayacağınızı unutmayın. Bunun yerine, bu konuda daha önce açıklandığı gibi **Maliyet tahmini** iletişim kutusunu **(Varış yeri maliyeti \> Periyodik görevler \> Maliyet tahmini)** kullanın.

**Maliyet tahminleri** sayfası, her tahmini maliyetin nasıl türetildiğini gösterir. Ayrıca, her madde için tahmini varış yeri maliyetini de gösterir. Çeşitli mallarla ilişkili maliyet fiyatını ve/veya para birimini değiştirerek maliyet tahminini değiştirebilirsiniz. Ayrıca, ilişkili seyahat maliyetlerini hem seyahat seviyesinde hem de konteyner düzeyinde değiştirebilirsiniz. Maliyetleri değiştirmek için bu sayfayı kullandığınızda, maliyet tahminindeki maddelerin tahmini maliyetlerini yeniden hesaplamanız istenir. Hazır olduğunuzda, maliyet şablonundaki maddelerin maliyet fiyatını güncelleştirmek için tahminleri kullanabilirsiniz.

### <a name="information-on-the-header"></a>Başlık hakkındaki bilgiler

**Maliyet tahminleri** sayfasının üst kısmında, önceki bölümde açıklandığı gibi seçili maliyet tahminini oluşturmak için kullanılan ayarlar gösterilir. 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>Satırlar hızlı sekmesindeki ayarlar ve düğmeler

**Satırlar** hızlı sekmesi, geçerli tahmine dahil edilen her öğeyi listeler. Aşağıdaki tabloda, her satırda kullanılabilecek alan açıklanmıştır.

| Alan | Tanım |
|---|---|
| Satıcı hesabı | Maddeyle ilişkili satıcı hesabı. |
| Madde kodu | Madde numarası. |
| Miktar | Maliyeti belirlemek için kullanılan madde sayısı. |
| Maliyet fiyatı | Ticaret anlaşmasına göre maliyet fiyatı. Bu değer yerel para biriminde gösterilir. |
| Ölçüm | Ayrı bir ölçüm. Birim, ilgili piyasaya sürülecek ürün için tanımlanan birimdir. |
| Tahmini varış yeri maliyeti | Toplam miktar için tahmini varış yeri maliyeti. |
| Birim başına | Tahmini varış yeri maliyetinin miktara bölümü. |
| (Diğer boyutlar) | Göstermeyi seçtiğiniz boyutlara bağlı olarak her madde hakkında ek bilgi sütunları görebilirsiniz. |

Aşağıdaki tabloda, **Satırlar** hızlı sekmesindeki araç çubuğunda yer alan düğmeler açıklanmaktadır.

| Düğme | Tanım |
|---|---|
| Ekle | Maliyet tahminine madde ekleyin. Madde ekledikten sonra, Eylem Bölmesinde **Yeniden Hesapla**'yı seçmelisiniz. |
| Kaldır | Maddeleri maliyet tahmininden kaldırın. Maddeleri kaldırdıktan sonra, Eylem Bölmesinde **Yeniden Hesapla**'yı seçmelisiniz. |
| Seyahat maliyetleri | Madde için çeşitli seyahat maliyetlerini görüntüleyebileceğiniz ve düzenleyebileceğiniz bir sayfa açın. |
| Stok \> Görüntüleme boyutları | Kılavuza boyut sütunları ekleyebileceğiniz veya sütunları kaldırabileceğiniz bir iletişim kutusu açın. |

### <a name="settings-on-the-general-fasttab"></a>Genel hızlı sekmesindeki ayarlar

**Genel** hızlı sekmesi, **Satırlar** hızlı sekmesinde seçili olan maddeyle ilgili ayrıntıları gösterir. Bu bilgilerin çoğu **Satırlar** hızlı sekmesinden yinelenir ve her iki yerde de düzenlenebilir. Ancak ek ayrıntılara da buradan ulaşabilirsiniz. Ek alanların değerleri, ilgili piyasaya sürülen ürünün kurulumuna bağlıdır.

### <a name="settings-on-the-dimension-fasttab"></a>Boyut hızlı sekmesindeki ayarlar

**Boyut** hızlı sekmesi, **Satırlar** hızlı sekmesinde seçili madde için kullanılabilir tüm stok boyutlarının değerlerini, orada göstermeyi seçtiğiniz boyutlara bakılmaksızın gösterir. Burada gösterilen tüm değerler ilgili maliyet tahmini şablonundan gelir. Bunlar maliyet tahmini şablonunda isteğe bağlıdır.

### <a name="buttons-on-the-action-pane"></a>Eylem Bölmesindeki düğmeler

Seçili maliyet tahminiyle çalışmak için **Maliyet tahminleri** sayfasının Eylem Bölmesindeki düğmeleri kullanabilirsiniz. Aşağıdaki tabloda, kullanılabilecek düğmeler açıklanmıştır.

| Eylem | Tanım |
|---|---|
| Maliyet Sorgusu | Seyahat için tüm maliyetleri görüntüleyin. Maliyetleri gerektiği gibi tek tek madde düzeyinde görüntüleyebilirsiniz. |
| Standart maliyeti güncelleştir | <p>**Varış yeri maliyeti parametreleri** sayfasında tanımlanan varsayılan maliyet sürümünü kullanarak standart maliyeti güncelleştirin. Bu sürümü geçersiz kılabilirsiniz.</p><p>**Not:** Bir maddenin birkaç madde boyutu varsa (örneğin, çeşitli boyutlar, renkler ve yapılandırmalar) ancak bu boyutlar tahmin için seçilmemişse sistem her kombinasyon için bekleyen bir fiyat oluşturur.</p><p>**Önemli:** Fiyat dökümü oluşturulur ve varış yeri maliyeti başına standart maliyet farkını belirlemek için kullanılır.</p> |
| Seyahat maliyetleri | Sevkiyattaki tüm malların seyahat maliyetlerini görüntüleyin ve düzenleyin. |
| Yeniden hesapla | Seyahat maliyetleri güncellendikten, eklendikten veya kaldırıldıktan sonra tahmini varış yeri maliyetlerini güncelleştirin. |
| Kilitle | Daha fazla değişiklik yapılmaması için maliyet tahmini kaydını kilitleyin. |

## <a name="item-cost-price-update"></a>Madde maliyet fiyatı güncelleştirmesi

**Madde maliyet fiyatı güncelleştirmesi** periyodik görevi, görevi çalıştırdığınızda ayarladığınız filtrelerle eşleşen tüm maliyet tahminlerini güncelleştirir. Etkisi, tek bir tahmin için Eylem Bölmesinde **Standart maliyeti güncelleştir**'in seçilmesinin yarattığı etkiye benzerdir. Ancak bu durumda, güncelleştirme işlemi, eşleşen tüm tahminler için geçerlidir.

Periyodik görevi çalıştırmak için aşağıdaki adımları uygulayın.

1. **Varış yeri maliyeti \> Periyodik görevler \> Madde maliyet fiyatı güncelleştirmesi**'ne gidin.
1. **Maliyet fiyatını tahminden güncelleştir** iletişim kutusunda, güncelleştirmenin kapsamını sınırlamak için aşağıdaki alanları gerektiği gibi ayarlayın:

    - **Sürüm**: Yalnızca belirtilen maliyet sürümünü kullanan tahminleri güncelleştirin.
    - **Tesis**: Yalnızca belirtilen tesisi kullanan tahminleri güncelleştirin.
    - **Maliyet şablonu**: Yalnızca belirtilen şablonu kullanan tahminleri güncelleştirin.
    - **Varış limanı**: Yalnızca belirtilen "varış" limanını kullanan tahminleri güncelleştirin.
    - **Tahmin tarihi**: Yalnızca belirtilen tarihe sahip tahminleri güncelleştirin.

1. Periyodik görevler için **Dahil edilecek kayıtlar** ve **Arka planda çalıştır** hızlı sekmesindeki seçenekleri her zamanki gibi ayarlayın.
1. Görevi çalıştırmak için **Tamam**'ı seçin.

> [!NOTE]
> Bu periyodik görev yalnızca aşağıdaki bilgilerin kullanılabilir olması koşuluyla başarıyla yürütülür:
>
> - İlgili her ürünün tanımlanmış bir **Brüt derinliği**, **Brüt genişliği** ve **Brüt yüksekliği** olmalıdır.
> - İlgili her satıcının tanımlanmış bir **Çıkış limanı** olmalıdır.
