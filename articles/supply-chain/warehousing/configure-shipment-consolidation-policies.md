---
title: Sevkiyat konsolidasyon ilkelerini yapılandırma
description: Bu konu, varsayılan ve özel sevkiyat konsolidasyon ilkelerinin nasıl ayarlanacağını açıklar.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: a9215672f4ace591bf7d964c8fbd3ad483bacca5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360436"
---
# <a name="configure-shipment-consolidation-policies"></a>Sevkiyat konsolidasyon ilkelerini yapılandırma

[!include [banner](../includes/banner.md)]

Otomatik ve el ile gerçekleştirilen ambara serbest bırakma sırasında, sevkiyat konsolidasyon ilkelerini kullanan sevkiyat konsolidasyon süreci otomatik sevkiyat konsolidasyon işlemine olanak sağlar. Bu özelliği açtıktan sonra, başlangıç ilkelerinizi yapılandırmanız gerekir. Herhangi bir ilke yapılandırılmazsa, her satış satırı tek bir yükleme satırına sahip olan ayrı bir sevkiyat oluşturacaktır.

Bu konuda sunulan senaryolar, varsayılan ve özel sevkiyat konsolidasyon ilkelerinin nasıl ayarlanacağını gösterir.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Sevkiyat konsolidasyon ilkeleri özelliğini açma

> [!IMPORTANT]
> Bu konuda açıklanan [ilk senaryoda](#scenario-1), ilk olarak önceki sevkiyat konsolidasyon özelliğini kullanacak şekilde bir ambar ayarlarsınız. Daha sonra, sevkiyat konsolidasyon ilkelerinin kullanılabilmesini sağlayabilirsiniz. Böylece, yükseltme senaryosunun nasıl çalıştığını görebilirsiniz. İlk senaryo üzerinden gitmek için demo veri ortamı kullanmayı planlıyorsanız senaryoyu yapmadan önce özelliği açmayın.

*Sevkiyat konsolidasyon ilkeleri* özelliğini kullanabilmeniz için önce sisteminizde bu özelliği açmanız gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Sevkiyatı konsolide etme*

## <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu konudaki her senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur. Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a>Senaryo 1: Varsayılan sevkiyat konsolidasyon ilkelerini yapılandırma

*Sevkiyat konsolidasyon ilkeleri* özelliğini açtıktan sonra minimum varsayılan ilke sayısını yapılandırmak zorunda olduğunuz iki durum vardır:

- Zaten veri içeren bir ortamı yükseltirsiniz.
- Tamamıyla yeni bir ortam ayarlarsınız.

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a>Ambarların zaten çapraz sipariş konsolidasyonu için yapılandırıldığı bir ortamı yükseltme

Bu yordamı başlattığınızda, temel çapraz sipariş konsolidasyonu özelliğinin zaten kullanıldığı bir ortamın benzetimini yapmak için *Sevkiyat konsolidasyon ilkeleri* özelliğinin kapatılmış olması gerekir. Daha sonra, özelliği açmak için özellik yönetimini kullanacaksınız. Böylece yükseltme işleminden sonra sevkiyat konsolidasyonu ilkelerinin nasıl ayarlanacağını öğrenebilirsiniz.

Ambarların zaten çapraz sipariş konsolidasyonu için yapılandırıldığı bir ortamda varsayılan sevkiyat konsolidasyon ilkelerini ayarlamak için bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar  \> Ambarlar**'a gidin.
1. Listede, istediğiniz ambar kaydını bulun ve açın (örneğin, **USMF** tanıtım verilerindeki ambar *24*).
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Ambar** hızlı sekmesinde, **Ambara serbest bırakmada sevkiyatı konsolide et** seçeneğini *Evet* olarak ayarlayın.
1. Konsolidasyonun gerekli olduğu tüm diğer ambarlar için 2 ile 4 arasındaki adımları yineleyin.
1. Sayfayı kapatın.
1. *Sevkiyat konsolidasyon ilkeleri* özelliğini açmak için [özellik yönetimini](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanın. **Özellik yönetimi** çalışma alanında, bu özellik *Sevkiyatı konsolide etme* olarak adlandırılır.
1. **Ambar yönetimi \> Kurulum \> Ambara serbest bırakma \> Sevkiyat konsolidasyon ilkeleri** seçeneğine gidin. Özelliği açtıktan sonra, yeni **Sevkiyat konsolidasyonu ilkeleri** menü öğesini görmek için tarayıcınızı yenilemeniz gerekebilir.
1. Eylem Bölmesi'nde, aşağıdaki ilkeleri oluşturmak için **Varsayılan kurulum oluştur**'u seçin:

    - *Satış siparişleri* ilke türü için bir **CrossOrder** ilkesi (önceki konsolidasyon özelliğini kullanacak şekilde ayarlanmış en az bir ambarınız olması koşuluyla)
    - *Satış siparişleri* ilke türü için bir **Varsayılan** ilke
    - *Transfer çıkışı* ilke türü için bir **Varsayılan** ilke
    - *Transfer çıkışı* ilke türü için bir **CrossOrder** ilkesi (önceki konsolidasyon özelliğini kullanacak şekilde ayarlanmış en az bir ambarınız olması koşuluyla)

    > [!NOTE]
    > - Her iki **CrossOrder** ilkesi, sipariş numarası alanı dışında, daha önceki mantıkla aynı alan kümesini dikkate alır. (Bu alan; ambar, taşıma teslimat şekli ve adres gibi faktörlere bağlı olarak, satırları sevkiyatlar halinde konsolide etmek için kullanılır.)
    > - Her iki **Varsayılan** ilkesi, sipariş numarası alanı dahil, daha önceki mantıkla aynı alan kümesini dikkate alır. (Bu alan; sipariş numarası, ambar, taşıma teslimat şekli ve adres gibi faktörlere bağlı olarak, satırları sevkiyatlar halinde konsolide etmek için kullanılır.)

1. *Satış siparişleri* ilke türü için **CrossOrder** ilkesini seçin ve sonra, Eylem Bölmesi'nde **Sorguyu düzenle**'yi seçin.
1. Sorgu düzenleyici iletişim kutusunda, **Ambara serbest bırakmada sevkiyatı konsolide et** seçeneğinin *Evet* olarak ayarlandığı ambarların listelendiğine dikkat edin. Bu nedenle, bunlar sorguya dahil edilir.

### <a name="create-default-policies-for-a-new-environment"></a>Yeni ortam için varsayılan ilkeler oluşturma

Yepyeni bir ortamda varsayılan sevkiyat konsolidasyon ilkelerini ayarlamak için bu adımları izleyin.

1. Daha önce açmadıysanız *Sevkiyat konsolidasyon ilkeleri* özelliğini açmak için [özellik yönetimini](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanın. **Özellik yönetimi** çalışma alanında, bu özellik *Sevkiyatı konsolide etme* olarak adlandırılır.
1. **Ambar yönetimi \> Kurulum \> Ambara serbest bırakma \> Sevkiyat konsolidasyon ilkeleri** seçeneğine gidin.
1. Eylem Bölmesi'nde, aşağıdaki ilkeleri oluşturmak için **Varsayılan kurulum oluştur**'u seçin:

    - *Satış siparişleri* ilke türü için bir **Varsayılan** ilke
    - *Transfer çıkışı* ilke türü için bir **Varsayılan** ilke

    > [!NOTE]
    > Her iki **Varsayılan** ilkesi, sipariş numarası alanı dahil, daha önceki mantıkla aynı alan kümesini dikkate alır. (Bu alan; sipariş numarası, ambar, taşıma teslimat şekli ve adres gibi faktörlere bağlı olarak, satırları sevkiyatlar halinde konsolide etmek için kullanılır.)

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a>Senaryo 2: Özel sevkiyat konsolidasyon ilkelerini yapılandırma

Bu senaryo, özel sevkiyat konsolidasyon ilkelerinin nasıl ayarlanacağını gösterir. Özel ilkeler, sevkiyat konsolidasyonunun çeşitli koşullara bağlı olduğu karmaşık iş gereksinimlerini destekleyebilir. Bu senaryoda daha sonra yer alan her örnek ilke için iş örneğinin kısa bir açıklaması dahil edilir. Bu örnek ilkeler sorgular için piramit benzeri bir değerlendirme sağlayan bir sırada ayarlanmalıdır. (Başka bir deyişle, en fazla koşula sahip ilkeler en yüksek önceliğe sahip olacak şekilde değerlendirilmelidir.)

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a>Özelliği açma ve bu senaryo için ana verileri hazırlama

Bu senaryodaki alıştırmalara devam etmeden önce, aşağıdaki alt kısımlarda açıklandığı gibi, özelliği etkinleştirmeniz ve filtre uygulamak için gereken ana verileri hazırlamanız gerekir. (Bu önkoşullar, [Sevkiyat konsolidasyonu ilkelerinin nasıl kullanılacağına ilişkin örnek senaryolar](#example-scenarios) bölümünde listelenen senaryolar için de geçerlidir.)

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a>Özelliği açma ve varsayılan ilkeleri oluşturma

Henüz açmadıysanız özelliği açmak ve [senaryo 1](#scenario-1)'de açıklanan varsayılan konsolidasyon ilkelerini oluşturmak için özellik yönetimini kullanın.

#### <a name="create-two-new-product-filter-codes"></a>İki yeni ürün filtre kodu oluşturma

1. **Ambar yönetimi \> Kurulum \> Ürün filtreleri \> Ürün filtreleri** öğesine gidin ve iki ürün filtresi ekleyin:

    - Ürün filtresi 1:

        - **Filtre kodu:** *Yanıcı*
        - **Filtre başlığı:** *Kod 4*

    - Ürün filtresi 2:

        - **Filtre kodu:** *Patlayıcı*
        - **Filtre başlığı:** *Kod 4*

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. *M9200* madde numarasına sahip ürünü açın. (Seçtiğiniz ürün, gelişmiş ambar \[WMS\] işlemleri için etkinleştirilmiş olmalıdır ve bu ürün, **USMF** tanıtım verilerinde WMS işlemleri için önceden etkinleştirilir.)
1. **Ambar** hızlı sekmesinde, **Kod 4** alanını *Yanıcı* olarak ayarlayın.
1. Sayfayı kapatın.
1. *M9201* madde numarasına sahip ürünü açın. (Bu ürün, **USMF** tanıtım verilerindeki WMS işlemleri için de önceden etkinleştirilir.)
1. **Ambar** hızlı sekmesinde, **Kod 4** alanını *Patlayıcı* olarak ayarlayın.
1. Sayfayı kapatın.

#### <a name="create-a-new-transportation-mode-of-delivery"></a>Yeni bir taşıma teslimat şekli oluşturma

1. **Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Mod** öğesine gidin.
1. Konsolidasyon sorgularında kullanılacak bir taşıma şekli oluşturun ve bunu *Hava yolları* olarak adlandırın.
1. **Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Sevkiyat taşıyıcıları** seçeneğine gidin.
1. Aşağıdaki ayarlara sahip bir taşıyıcı oluşturun:

    - **Sevkiyat taşıyıcısı:** *Hava yolları*
    - **Ad:** *Hava yolları*
    - **Mod:** *Hava yolları*

1. Yeni taşıyıcı için **Hizmetler** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Taşıyıcı hizmeti:** *Hava*
    - **Taşıma yöntemi:** *Hava*

1. Eylem bölmesinde, **Kaydet**'i seçin.

    > [!NOTE]
    > Yeni taşıyıcıyı kaydettiğinizde, **Hizmetler** kılavuzundaki yeni satır için **Teslimat şekli** alanı otomatik olarak *Airwa-Air* olarak ayarlanır. Bir satış siparişi için *Airwa-Air* teslimat şeklini kullandığınızda, ilgili sevkiyatlar için *Hava yolları* taşıma şekli kullanılır.

#### <a name="create-an-order-pool"></a>Sipariş havuzu oluşturma

1. **Satış ve pazarlama \> Kurulum \> Satış siparişleri \> Sipariş havuzları** öğesine gidin.
1. Konsolidasyon sorgusu için kullanılacak bir sipariş havuzu oluşturun. Bu sipariş havuzunda aşağıdaki ayarlar olmalıdır:

    - **Havuz:** Başka bir havuz tarafından kullanılmayan bir tamsayı girin.
    - **Ad:** *ShipCons*

1. **Satış ve pazarlama \> Müşteriler \> Tüm müşteriler** öğesine gidin.
1. Hesap numarası *US-003* olan müşteriyi açın.
1. **Satış siparişi varsayılanları** hızlı sekmesinde, yeni oluşturduğunuz sipariş havuzu için **Satış siparişi havuzu** alanını ayarlayın.
1. Sayfayı kapatın ve hesap numarası *US-004* olan müşteri için 4. ve 5. adımları yineleyin.

### <a name="create-example-policy-1"></a>Örnek ilke 1'i oluşturma

Bu örnekte, aşağıdaki iş örneği için kullanılabilecek bir *Müşteri+Mod* ilkesi oluşturacaksınız:

- İlke belirli bir müşteri hesabı (*US-001*) ve belirli bir teslimat şekli (*Airwa-Air*) için sorgu oluşturacaktır.
- Açık sevkiyatlarla konsolidasyon kapalıdır.
- Konsolidasyon, her sipariş kodu için gerçekleştirilir. (Başka bir deyişle, her sipariş, ambar vb. için ayrı sevkiyatlar olacaktır.)

Bu iş örneğine ait sevkiyat konsolidasyon ilkesini oluşturmak için bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambara serbest bırakma \> Sevkiyat konsolidasyon ilkeleri** seçeneğine gidin.
1. **İlke türü** alanını *Satış siparişleri* olarak ayarlayın.
1. Eylem Bölmesi'nde, aşağıdaki ayarlara sahip bir ilke oluşturmak için **Yeni**'yi seçin:

    - **İlke adı:** *CustomerMode*
    - **İlke açıklaması:** *Müşteri hesabı ve teslimat şekli*

1. **Açık sevkiyatlarla konsolide et** seçeneğini *Hayır* ayarında bırakın.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Konsolidasyon alanları** hızlı sekmesinde bulunan **Kalan alanlar** listesinde, **Alan adı** alanının *Teslimat şekli* olarak ayarlandığı satırı seçin.
1. **Ekle** düğmesini ![sağ ok.](media/forward-button.png) seçerek alanı **Seçili alanlar** listesine taşıyın.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyici iletişim kutusundaki **Aralık** sekmesinde bulunan kılavuzda, **Alan** alanının *Müşteri hesabı* olarak ayarlandığı satırı bulun ve bu satır için **Ölçüt** alanını *US-001* olarak ayarlayın.
1. Kılavuza aşağıdaki ayarlara sahip bir satır eklemek için **Ekle**'yi seçin:

    - **Tablo:** *Sipariş satırları*
    - **Türetilen tablo:** *Sipariş satırları*
    - **Alan:** *Teslimat şekli*
    - **Ölçüt:** *Airwa-Air*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.

> [!NOTE]
> Bu iş örneği için *Airwa-Air* teslimat şeklini kullanan *US-001* müşterisinin sipariş satırları, siparişler genelinde konsolide edilmeyecektir. Diğer tüm teslimat şekillerinin sevkiyatları bu müşteri için konsolide edildiğinde, bu ilkenin bir sırada ilk olarak kullanılması amaçlanmıştır.

### <a name="create-example-policy-2"></a>Örnek ilke 2'yi oluşturma

Bu örnekte, aşağıdaki iş örneği için kullanılabilecek bir *Tehlikeli mallar* ilkesi oluşturacaksınız:

- İlke belirli bir filtre kodu (*tehlikeli*) ve belirli bir teslimat şekli (*Airwa-Air*) için sorgu oluşturacaktır.
- Açık sevkiyatlarla konsolidasyon açıktır.
- Konsolidasyon, siparişler genelinde gerçekleştirilir. (Başka bir deyişle, her hesap, ambar vb. için ayrı sevkiyatlar olacaktır ancak bunlar yalnızca sorguda belirtilen madde grubu içindedir.)

Bu iş örneğine ait sevkiyat konsolidasyon ilkesini oluşturmak için bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambara serbest bırakma \> Sevkiyat konsolidasyon ilkeleri** seçeneğine gidin.
1. **İlke türü** alanını *Satış siparişleri* olarak ayarlayın.
1. Eylem Bölmesi'nde, aşağıdaki ayarlara sahip bir ilke oluşturmak için **Yeni**'yi seçin:

    - **İlke adı:** *Madde türü*
    - **İlke açıklaması:** *Aynı madde türünü siparişler genelinde konsolide etme*

1. **Açık sevkiyatlarla konsolide et** seçeneğini *Evet* olarak ayarlayın.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Konsolidasyon alanları** hızlı sekmesinde bulunan **Kalan alanlar** listesinde, **Alan adı** alanının *Teslimat şekli* olarak ayarlandığı satırı seçin.
1. **Ekle** düğmesini ![sağ ok.](media/forward-button.png) seçerek alanı **Seçili alanlar** listesine taşıyın.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyici iletişim kutusunda, **Birleşimler** sekmesinde, ağaçtaki **Tablolar \> Yük ayrıntıları** öğesini genişletin ve seçin.
1. **Tablo birleşimi ekle**'yi seçin.
1. Görüntülenen ilişkiler kılavuzunda, **İlişki** alanının *Ambar madde numarası (madde numarası)* olarak ayarlandığı satırı bulun ve seçin ve **Seç**'i belirleyin. 
1. Kılavuza aşağıdaki ayarlara sahip bir satır eklemek için **Aralık** sekmesinde **Ekle**'yi seçin:

    - **Tablo:** *Ambar madde numarası*
    - **Türetilmiş tablo:** *Ambar madde numarası*
    - **Alan:** *Kod 4*
    - **Ölçüt:** *Yanıcı*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.

> [!NOTE]
> Bu iş örneğinde, maddelerin belirli bir filtre koduna sahip olduğu tüm sipariş satırları (yani **Kod 4** alanının *Yanıcı* olarak ayarlandığı filtre kodu), siparişler genelinde aynı türde diğer maddelerle konsolide edilir. Aynı hesap, ambar ve madde grubu için açık bir sevkiyat varsa yeni satırlar buna iliştirilir.

### <a name="create-example-policy-3"></a>Örnek ilke 3'ü oluşturma

Bu örnekte, aşağıdaki iş örneği için kullanılabilecek bir *Müşteri gereksinimleri* ilkesi oluşturacaksınız:

- İlke belirli bir müşteri hesabını sorgulayacak.
- Açık sevkiyatlarla konsolidasyon açıktır.
- Konsolidasyon, siparişler genelinde gerçekleştirilir ancak müşteri talepleri temel alınarak yapılır. (Başka bir deyişle, aynı müşteri talep numarası ve ambara dayalı olarak birden çok sipariş sevkiyatlar halinde gruplandırılır.)

Bu iş örneğine ait sevkiyat konsolidasyon ilkesini oluşturmak için bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambara serbest bırakma \> Sevkiyat konsolidasyon ilkeleri** seçeneğine gidin.
1. **İlke türü** alanını *Satış siparişleri* olarak ayarlayın.
1. Eylem Bölmesi'nde, aşağıdaki ayarlara sahip bir ilke oluşturmak için **Yeni**'yi seçin:

    - **İlke adı:** *CustomerOrderNo*
    - **İlke açıklaması:** *Müşteri PO'sunu temel alan satırları konsolide etme*

1. **Açık sevkiyatlarla konsolide et** seçeneğini *Evet* olarak ayarlayın.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Konsolidasyon alanları** hızlı sekmesinde bulunan **Kalan alanlar** listesinde, **Alan adı** alanının *Müşteri gereksinimi* olarak ayarlandığı satırı seçin.
1. **Ekle** düğmesini ![sağ ok.](media/forward-button.png) seçerek alanı **Seçili alanlar** listesine taşıyın.
1. **Kalan alanlar** listesinde, **Alan adı** alanının *Teslimat şekli* olarak ayarlandığı satırı seçin.
1. **Ekle** düğmesini ![sağ ok.](media/forward-button.png) seçerek alanı **Seçili alanlar** listesine taşıyın.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyici iletişim kutusundaki **Aralık** sekmesinde, **Alan** alanının *Müşteri hesabı* olarak ayarlandığı satırı bulun ve bu satır için **Ölçüt** alanını *US-001* olarak ayarlayın.
1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.

> [!NOTE]
> Bu iş örneği için satış siparişlerinin aynı müşteri talep numarasına sahip olduğu sipariş satırları, satış sipariş numarasından bağımsız olarak tek bir sevkiyatta konsolide edilecektir. (Müşteri talep numarası müşterinin satın alma siparişi \[PO\] numarası olarak kullanılır.) Aynı hesap, ambar ve müşteri talebi için açık bir sevkiyat varsa yeni satırlar buna iliştirilir. Müşteri bir günde birkaç kez aynı PO numarasına sahip ek sipariş satırları gönderirse ve tüm satırların tek bir sevkiyat olarak gruplandırılmasını isterse bu ilke kullanılabilir. (Başka bir deyişle, tek bir konşimento ve bir sevk irsaliyesi olacaktır.)

### <a name="create-example-policy-4"></a>Örnek ilke 4'ü oluşturma

Bu örnekte, aşağıdaki iş örneği için kullanılabilecek bir *Konsolidasyona izin veren müşteriler* ilkesi oluşturacaksınız:

- İlke, konsolide edilen sevkiyatları kabul eden müşterileri tanımlamak üzere belirli bir sipariş havuzunu sorgulayacaktır.
- Açık sevkiyatlarla konsolidasyon kapalıdır.
- Konsolidasyon, varsayılan CrossOrder ilkesi (önceki **Ambara serbest bırakmada sevkiyatı konsolide et** onay kutusunu çoğaltmak için) tarafından seçilen alanları kullanan siparişler genelinde yapılır.

- Farklı bir sipariş havuzu seçerek satış siparişindeki kuralı geçersiz kılabilirsiniz.

Bu iş örneğine ait sevkiyat konsolidasyon ilkesini oluşturmak için bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambara serbest bırakma \> Sevkiyat konsolidasyon ilkeleri** seçeneğine gidin.
1. **İlke türü** alanını *Satış siparişleri* olarak ayarlayın.
1. Eylem Bölmesi'nde, aşağıdaki ayarlara sahip bir ilke oluşturmak için **Yeni**'yi seçin:

    - **İlke adı:** *Sipariş havuzu*
    - **İlke açıklaması:** *Sipariş havuzuna dayalı olarak siparişleri konsolide etme*

1. **Açık sevkiyatlarla konsolide et** seçeneğini *Hayır* ayarında bırakın.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Konsolidasyon alanları** hızlı sekmesinde bulunan **Kalan alanlar** listesinde, **Alan adı** alanının *Teslimat şekli* olarak ayarlandığı satırı seçin.
1. **Ekle** düğmesini ![sağ ok.](media/forward-button.png) seçerek alanı **Seçili alanlar** listesine taşıyın.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyici iletişim kutusunda, kılavuza aşağıdaki ayarlara sahip bir satır eklemek için **Aralık** sekmesinde **Ekle**'yi seçin:

    - **Tablo:** *Satış siparişleri*
    - **Türetilmiş tablo:** *Satış siparişleri*
    - **Alan:** *Havuz*
    - **Ölçüt:** *ShipCons*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.

> [!NOTE]
> Bu iş örneği için satış siparişlerinin aynı sipariş havuzuna ait olduğu tüm sipariş satırları, aynı hesap, ambar ve taşıma teslimat şekli açısından satış siparişleri genelinde tek bir sevkiyat olarak konsolide edilir. Sipariş havuzu yerine, bir müşteri grubunu ayırmak ve varsayılan olarak satış siparişi başlığını kullanmak için başka bir alan kullanabilirsiniz. Konsolidasyon gereksinimini ambar değil de müşteri yönlendiriyorsa bu yaklaşımı kullanabilirsiniz. (Önceki konsolidasyon mantığında, ambar konsolidasyon gereksinimini yönlendiriyordu.)

### <a name="create-example-policy-5"></a>Örnek ilke 5'i oluşturma

Bu örnekte, aşağıdaki iş örneği için kullanılabilecek bir *Konsolidasyona izin veren ambarlar* ilkesi oluşturacaksınız:

- İlke, sevkiyatları konsolide edebilen ambarları tanımlamak üzere belirli bir sipariş havuzunu sorgulayacaktır.
- Açık sevkiyatlarla konsolidasyon kapalıdır.
- Konsolidasyon, varsayılan CrossOrder ilkesi (önceki **Ambara serbest bırakmada sevkiyatı konsolide et** onay kutusunu çoğaltmak için) tarafından seçilen alanları kullanan siparişler genelinde yapılır.

Genellikle bu iş örneği, [senaryo 1](#scenario-1)'de oluşturduğunuz varsayılan ilkeler kullanılarak ele alınabilir. Ancak, bu adımları izleyerek benzer ilkeleri el ile de oluşturabilirsiniz.

1. **Ambar yönetimi \> Kurulum \> Ambara serbest bırakma \> Sevkiyat konsolidasyon ilkeleri** seçeneğine gidin.
1. **İlke türü** alanını *Satış siparişleri* olarak ayarlayın.
1. Eylem Bölmesi'nde, aşağıdaki ayarlara sahip bir ilke oluşturmak için **Yeni**'yi seçin:

    - **İlke adı:** *Çapraz sipariş*
    - **İlke açıklaması:** *Belirli ambarlar için çapraz sipariş konsolidasyonu*

1. **Açık sevkiyatlarla konsolide et** seçeneğini *Hayır* ayarında bırakın.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Konsolidasyon alanları** hızlı sekmesinde bulunan **Kalan alanlar** alanında, **Alan adı** alanının *Teslimat şekli* olarak ayarlandığı satırı seçin.
1. **Ekle** düğmesini ![sağ ok.](media/forward-button.png) seçerek alanı **Seçili alanlar** listesine taşıyın.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyici iletişim kutusundaki **Aralık** sekmesinde, **Alan** alanının *Ambar* olarak ayarlandığı satırı bulun ve bu satır için **Ölçüt** alanını *61-63* olarak ayarlayın.
1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.

### <a name="set-the-order"></a>Sıralamayı ayarlama

Tüm ilkeleriniz oluşturulduğunda, bunların uygulanacağı sırayı oluşturmanız gerekir. En çok koşula sahip olan ilkelerin en yüksek öncelikle ele alındığı piramit benzeri bir yaklaşım kullanmak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambara serbest bırakma \> Sevkiyat konsolidasyon ilkeleri** seçeneğine gidin.
1. **İlke türü** alanını *Satış siparişleri* olarak ayarlayın.
1. Sol sütunda listelenen her bir ilkeyi seçin ve sonra ilkeleri aşağıdaki sırada düzenlemek için Eylem Bölmesi'nde **Yukarı taşı** ve **Aşağı taşı** düğmelerini kullanın:

    1. CustomerMode
    1. Madde türü
    1. CustomerOrderNo
    1. Sipariş havuzu
    1. Çapraz sipariş
    1. Varsayılan

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> Sevkiyat konsolidasyon ilkelerinin nasıl kullanılacağına ilişkin örnek senaryolar

Aşağıdaki senaryolar, bu konuyu okurken oluşturduğunuz sevkiyat konsolidasyon ilkelerini nasıl kullanabileceğinizi gösterir. Her bir senaryo otomatik ve el ile gerçekleştirilen ambara serbest bırakma sırasında, sevkiyat konsolidasyon ilkelerini kullanan sevkiyat konsolidasyon sürecinde size yol gösterir:

- Senaryo 1: [Satış siparişlerinin otomatik serbest bırakılması kullanılarak ambara serbest bırakıldıklarında sevkiyatları konsolide etme](../warehousing/consolidate-shipments-automatic.md)
- Senaryo 2: [Sevkiyat konsolidasyonu ilkesi, Ambara serbest bırakma sayfasından geçersiz kılındığında sevkiyatları konsolide etme](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Senaryo 3: [Yük planlama çalışma ekranından Ambara serbest bırakma kullanılarak sevkiyatları konsolide etme](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Senaryo 4: [Sevkiyat konsolidasyonu çalışma ekranı kullanılarak sevkiyatları konsolide etme](../warehousing/consolidate-shipments-manual-workbench.md)
- Senaryo 5: [Sevkiyatları konsolide etme sayfası kullanılarak sevkiyatları manuel olarak konsolide etme](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Ek kaynaklar

- [Sevkiyat konsolidasyonu ilkeleri](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]