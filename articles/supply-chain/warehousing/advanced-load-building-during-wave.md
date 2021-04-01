---
title: Dalga sırasında gelişmiş yük oluşturma
description: Bu konu, dalga yürütme sırasında varolan dalgalara otomatik olarak sevkiyat atayan gelişmiş dalga yükü Binası hakkında bilgi sağlar. Bu nedenle, yükleme planlama ekranını kullanmak zorunda kalmadan, kamyonları temsil eden anlamlı yüklemeler oluşturabilirsiniz.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate, WHSWaveTableListPage, TMSLoadBuildTemplateApply, TMSLoadBuildTemplates, TMSLoadBuildTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 1b75d5cec991b2863e7e0213257ac63d5ab566a6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233211"
---
# <a name="advanced-load-building-during-wave"></a>Dalga sırasında gelişmiş yük oluşturma

[!include [banner](../includes/banner.md)]

Dalga yürütme sırasında varolan dalgalara otomatik olarak sevkiyat atayan gelişmiş dalga yükü birikmesi. Bu nedenle, yükleme planlama ekranını kullanmak zorunda kalmadan, kamyonları temsil eden anlamlı yüklemeler oluşturabilirsiniz. Bu yetenek, bir kamyon/römorktaki malların sevkiyatını izlemek ve planlamak, ancak bunların her gün bunları el ile oluşturmak istemediğinizde, yükleme kavramını kullanmak isteyen işletmeler için yararlıdır.

Dalga işleme sırasında, sistem genellikle, yükleme atanmamış her sevkiyat için yeni bir yük oluşturur. Ancak, gelişmiş dalga yükü oluşturma özelliği açıldığında, sistem her atanmamış sevkiyatı varolan bir yüklemeye atar (uygun bir yükleme varsa) ve yeni yüklemeler yalnızca gerekli olduklarında oluşturulur. Gelişmiş dalga yükü oluşturma, tanımladığınız ölçütlere göre yeni yükleri otomatik olarak oluşturur.

Özelliği kullanmak için sistemi aşağıdaki şekilde ayarlamanız gerekir:

- Yeni **buildyükleri** yöntemini içeren *dalga şablonları* oluşturun. Bu yöntem, bu şablonları kullanan dalgalar için gelişmiş dalga yükü oluşturmayı kullanılabilir yapar.
- Her biri belirli bir dalga şablonu ve yöntemine bağlı olan *yükleme oluşturma şablonlarını* kurun. Yapı şablonlarını yükle hangi yük (varolan veya yeni) bekleyen yükleme satırlarının ekleneceğini denetler. Yükleme şablonu, ekipman ve yükleme satırındaki diğer alan değerleri gibi ölçütlere dayalı olarak sevk irsaliyelerini birleştirebilir veya ayırabilirsiniz.
- Tek bir yüklemede birleştirilmemelidir olması gereken maddeleri kontrol etmek için *yük karıştırma gruplarını* tanımlayın. Ayrıca kısıtlamanın bir uyarı mı, hata mı yoksa yükleme şablonu hacimsel kısıtlamasının değerlendirilmesi gerekip gerekmeyeceğini da belirtirsiniz.

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a>Sisteminizde gelişmiş dalga yükü oluşturmayı açın

İleri düzeyde dalga yükü oluşturma kullanabilmeniz için iki özelliğin sisteminizde etkinleştirilmesi gerekir. Yöneticiler bu özelliklerin durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellikler aşağıdaki şekilde listelenir:

- Dalga yükü oluşturma özelliği:

    - **Modül:** *Ambar yönetimi*
    - **Özellik adı:** *Dalga yükleme oluşturma özelliği*

- Kuruluş genelindeki dalga adım kodu:

    - **Modül:** *Ambar yönetimi*
    - **Özellik adı:** *Kuruluş genelindeki dalga adım kodu:*

### <a name="make-sample-data-available"></a>Örnek verilerini kullanılabilir hale getirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak bu tanıtım üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

Bu gösteriyi, üretim sisteminde çalışırken bu özelliği kullanmaya yönelik kılavuz olarak da kullanabilirsiniz. Ancak, bu durumda kendi değerlerinizi değiştirmeniz gerekir ve standart tanıtım verilerinin sağladığı bazı gerekli kayıt türleri kaybolabilir.

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a>Senaryo kurulumunun yeterli kullanılabilir stok içerdiğinden emin olun

**USMF** demo verileriyle çalışıyorsanız, ilk olarak, ilgili her konumda yeterli stok olmasını sağlamak için sisteminizin ayarlandığından emin olmanız gerekir. Bu gösteri için, aşağıdaki stoğun ambar *62*'da mevcut olması beklendir:

- **Madde A0001:** 10 parça
- **Madde A0002:** 10 parça
- **Madde M9200:** 10 beher

**M9200 madde** ambara eklenmelidir. Madde envanterini eklemek için aşağıdaki alt kısımlarda bulunan yordamları tamamlayın.

#### <a name="create-a-new-license-plate-id"></a>Yeni lisans levhası kimliği oluştur

1. **Ambar yönetimi** \> **Kurulum** \> **Ambar** \> **Lisans plakaları** öğesine gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni satırda, **Lisans levhası** alanına *LP6203* girin.
1. **Kaydet**'i seçin.

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a>Site 6'da madde M9200 için standart maliyet oluştur

1. **Ürün bilgileri yönetimi** \> **Ürünler** \> **Serbest bırakılmış ürünler**'e gidin.
1. **M9200** üzerinde arama yapın.
1. Maddenin satırını seçin ve sonra eylem bölmesinde **maliyetleri Yönet** sekmesinde, **ayarlama** grubunda **Madde fiyatı**'nı seçin.
1. **Madde fiyatı** sayfasında, **bekleyen fiyatlar** sekmesini seçin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Maliyetlendirme tipi:** *Planlanan maliyet*
    - **Fiyat türü:** *Maliyet*
    - **Sürüm:** *10*
    - **Tesis:** *6*
    - **Fiyat:** *1,60*

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem bölmesinde, **bekleyen fiyatları etkinleştir**'i seçin.
1. Tesis *6* için yeni maliyet fiyatının eklendiğini doğrulamak için **etkin fiyatlar** sekmesini seçin.

#### <a name="create-inventory-in-warehouse-62"></a>62. Ambarda stok oluştur

1. **Stok yönetimi** \> **Günlük girişleri** \> **Maddeler** \> **Stok ayarlama**'ya gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Stok günlüğü oluştur** iletişim kutusunda, **ambar** alanındaki **özet** hızlı sekmesinde, *62* girin. Tüm diğer alanlar için varsayılan değerleri kabul edin.
1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. **Stok Ayarlama** sayfası açılır. **Günlük Satırları** hızlı sekmesinde, satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın. Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **Madde numarası:** *M9200*
    - **Konum:** *bulk-003*
    - **Miktar:** değeri *10* olarak değiştirin.

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem bölmesinde, hataları denetlemek için **Doğrula** 'yı seçin.
1. **Günlüğü denetle** iletişim kutusunda, çeki başlatmak için **Tamam** 'ı seçin. Çek tamamlandığında bir ileti alırsınız.
1. Eylem bölmesinde, stok ayarı yapmak için **Deftere naklet**'i seçin.
1. **Günlüğü deftere naklet** iletişim kutusunda, nakletmeyi başlatmak için **Tamam** 'ı seçin. Nakletme tamamlandığında bir ileti alırsınız.

## <a name="set-up-advanced-wave-load-building"></a>Gelişmiş dalga yük oluşturmayı ayarla

### <a name="regenerate-wave-process-methods"></a>Dalga işlemi yöntemlerini yeniden oluştur

Yükleme oluşturma yöntemini (**buildLoads**) kullanılabilir hale getirmek için dalga işlemi yöntemlerini yeniden oluşturmanız gerekebilir.

1. **Ambar yönetimi** \> **Kurulum** \> **Dalgalar** \> **Dalga işleme yöntemleri**'na gidin.
2. **buildLoads**'un listede olduğunu doğrulayın. Yoksa, eklemek Için eylem bölmesindeki **yöntemleri yeniden üret**'i seçin.

### <a name="set-up-wave-templates"></a>Dalga şablonu ayarlama

Gelişmiş dalga yükü binanın avantajlarından yararlanmak için, her ilgili [dalga şablonuna](tasks/configure-wave-processing.md) **buildLoads** yöntemini eklemeniz gerekir.

1. **Ambar yönetimi** \> **Kurulum** \> **Dalgalar** \> **Dalga şablonları**'na gidin.
1. Dalga şablonu seçin.

    **USMF** demo verileriyle çalışıyorsanız, **62 sevkiyat varsayılan** şablonunu seçin.

1. Eylem bölmesinde, sayfayı düzenleme moduna yerleştirecek **Düzenle** seçin.
1. **Yöntemler** Hızlı sekmesinde, **kalan Yöntemler** kılavuzunda, **buildLoads** yöntemini seçin.
1. **buildLoads** yöntemini **Seçili yöntemler** kılavuzuna taşımak için Sağ ok seçin.
1. **buildLoads** yöntemine bir **dalga adım kodu** atamak için , önce **dalga adım kodları** sayfasında bir kod oluşturmanız gerekir. İstediğiniz herhangi bir değeri kullanabilirsiniz, ancak daha sonra gereksinim duyacağınız bir not aldığınızdan emin olun. **WSC2112** kodu oluşturmak için şu adımları izleyin.

    1. **buildLoads** yönteminin satırında, **Dalga adımı kodu** alanındaki aşağı oku farenin sağ düğmesiyle tıklayıp **Ayrıntıları göster** seçeneini seçin.
    1. **Dalga adımı kodları** sayfasında, eylem bölmesinde, **yeni** 'yi seçin.
    1. **Dalga adım kodu** alanına, *WSC2112* girin.
    1. **Dalga adım açıklaması** alanına, *WSC2112* girin.
    1. **Dalga adımı türü** alanında *yapı yükle*'yi seçin.

1. **Kaydet**'i seçip sayfayı kapatın.
1. **buildLoads** yönteminin satırında, **dalga adımı kodu** alanında, az önce oluşturduğunuz kodu seçin (**WSC2112**).
1. Eylem bölmesinde, **Kaydet**'i seçin.

> [!NOTE]
> Dalga adımı kodları, kullanıcıların, dalga yöntemlerinin belirli örneklerini ilgili bir şablona bağlamak için ayarlayıp kullanabileceği kodlardır. Şablonlar, stok yenileme, konteyner kullanımı, etiket yazdırma, yük oluşturma ve sıralama şablonlarını içerir.
>
> Dalga adımı kodları kullanılmadığı zaman, kullanıcıların dalga yöntemi örneğinden belirli bir şablona başvuruda bulunmak için serbest metin girmeleri gerekir. Serbest metin hataya açıktır çünkü kullanıcılar bir dalga şablonunda belirli bir dalga adımı yöntemi için ekledikleri dalga adımı metninin, hedef şablondaki dalga adımı metniyle tam olarak eşleştiğinden emin olmalıdır.
>
> Belirli bir dalga adımı türü için dalga adımı kodları ayrı bir sayfada ayarlanır. Dalga adımı kodu gerektiren bir dalga şablonunda bulunan her bir dalga adımı yöntemi örneği için, dalga adımı kodunun açılan listede seçilmesi gerekir. Açılır listedeki seçim serbest metin girişinin yerini alır ve insan hatası riskini ve etkisini azaltmaya yardımcı olur. Kurulum kodları, bir dalga şablonundaki dalga adımı yöntemini yöntem için hedef şablona bağlamak amacıyla kullanılır.

### <a name="set-up-load-mix-groups"></a>Yük karışımı grupları ayarlama

Karışım gruplarını yükle tek bir yüklemede birleştirilebilecek öğe türleri için kurallar oluşturur. İhtiyaç duyduğunuz kadar yük karışım grupları ayarlayabilirsiniz. Ancak, gelişmiş dalga yükleme oluşturmayı kullanmak için, en az bir tane olmalıdır. Yük karışım grubu oluşturmak için bu adımları izleyin.

1. **Ambar Yönetimi** \> **Kurulum** \> **YÜk** \> **Yük karışım grupları**'na gidin.
1. Eylem bölmesinde, bir yük grubu oluşturmak için **Yeni**'yi seçin.
1. **Yük karışım grubu kimliği** alanına, yeni grubu için açıklayıcı bir ad girin.

    **USMF** demo verileriyle çalışıyorsanız, aşağıdaki değerleri ayarlayın:

    - **Yük Karışım grubu kodu:** *TV*
    - **Açıklama:** *TV*

1. Eylem bölmesinde, **Yük karışımını grup ölçütü** Hızlı sekmesi 'ni kullanılabilir hale getirmek için **Kaydet** 'i seçin.
1. **Karışım grubu ölçütünü Yükle** hızlı sekmesinde, kılavuza satır eklemek için **yeni** 'yi seçin.
1. Yeni satırda, her bir alanda istenen değerleri ayarlayın. Bu değerler, yükleme karışımı için dikkate alınan madde gruplarını belirler.

    **USMF** demo verileriyle çalışıyorsanız, *madde grubu* alanında **TV & videosu** 'ni seçin.

1. Eylem bölmesinde, **Yük karışımını grup kısıtlamaları** Hızlı sekmesi 'ni kullanılabilir hale getirmek için **Kaydet** 'i seçin.
1. **Yük karışım grubu kısıtlamaları** hızlı sekmesinde, kılavuza satır eklemek için **yeni** 'yi seçin.
1. Yeni satırda, her bir alanda istenen değerleri ayarlayın.

    **USMF** demo verileriyle çalışıyorsanız, aşağıdaki değerleri ayarlayın:

    - **Madde grubu:** *CarAudio*
    - **Yükleme yapısı eylemi:** *Kısıtla* (Bu değer, **CarAudio** madde grubuna ait olan maddelerin **TV & video** madde grubuna ait olan öğelerle aynı yük üzerinde olmasını engeller.)

1. Yük karıştırma grubu için gereksinim duyduğunuz tüm ölçütleri ve sınırlamaları ekleyinceye kadar kurallarla çalışmaya devam edin.

**USMF** demo verileriyle çalışıyorsanız, şimdi bu kurulumu bitirdiniz.

### <a name="set-up-load-build-templates"></a>Yükleme oluşturma şablonlarını ayarla

İhtiyaç duyduğunuz kadar yük olşuturma şablonları ayarlayabilirsiniz. Ancak, gelişmiş dalga yükleme oluşturmayı kullanmak için, en az bir tane olmalıdır. Yük oluşturma şablonu oluşturmak için şu adımları izleyin.

1. **Ambar Yönetimi** \> **Kurulum** \> **Yük** \> **Dalga yük oluşturma şablonları**'na gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın.

    | Alan | Tanım | USMF demo verilerinde değer |
    |---|---|---|
    | Numara serisi | Şablonun değerlendirileceği sipariş. | *1* |
    | Yük oluşturma şablonu adı | Yük oluşturma şablonunun benzersiz tanımlayıcısı girin. Bu kurulumda daha önce oluşturduğunuz veya güncelleştirdiğiniz şablonun adını girmelisiniz. | *62 sevkiyat varsayılanı* |
    | Dalga adım kodu | Şablonu bir dalga yöntemine bağlamak için kullanılan dalga adım kodu girin. Dalga şablonunu Bu kurulumda daha önce ayarladığınızda **buildLoads** yöntemi için seçtiğiniz kodu girmeniz gerekir. | *WSC2112* |
    | Yük şablonu kodu | Yeni yükler oluşturulurken ve mevcut yüklere atama yapılırken eşleştirme için kullanılacak yük şablonu Yükleme şablonu, tüm yükleme için izin verilen maksimum ağırlık ve hacmi tanımlar. | *Standart Yük Şablonu* |
    | Equipment | Mevcut yükler atanırken eşleştirme yapmak ve oluşturulan yeni yüklerin doldurulması için kullanılan ekipman. | Bu alanı boş bırakın. |
    | Yük karıştırma grubu kodu | Yükte maddeye izin verilmesi durumunda kullanılana yük karıştırma grubunu seçin. Karışım gruplarını yükle tek bir yüklemede birleştirilebilecek öğe türleri için kurallar oluşturur. Bu kurulumda daha önce oluşturduğunuz karışım gruplarından birini seçmelisiniz. | *TV* |
    | Açık yükleri kullan | Mevcut açık yüklerin eklenip eklenmemesi gerektiğini seçin. Aşağıdaki seçenekler bulunur:<ul><li>**Yok** – Açık yükleri varolan yüklerin hiçbirine eklemeyin.</li><li>**Herhangi biri** - Herhangi biri seçilirse satır için geçerli olan mevcut yüklere ekler.</li><li>**Atandı** – Açık yükleri dalgaya atanan yüklemeye ekler.</li></ul> | *Herhangi* |
    | Yük oluştur | Herhangi bir yük ölçütle eşleşmezse yeni yüklemeler oluşturulup oluşturulmayacağını belirtir. | Seçili (= *Evet*) |
    | Sevkiyat satırı bölünmeye izin ver | Yük şablonunun maksimum kapasitesini aşması durumunda yük satırının birden çok yüke bölünmesine izin verilip verilmeyeceğini belirtin. | Temizlendi (= *Hayır*) |
    | Hacimleri doğrula | Etkin olduğunda yük oluşturma, yük şablonun maksimum değerlerine uyulmasını sağlamak için her yük satırı eklendiğinde ağırlığı ve hacmi kontrol eder. | Temizlendi (= *Hayır*) |

1. Eylem bölmesinde, **Düzenle sorgusu** seçeneğini kullanılabilir hale getirmek için **Kaydet** 'i seçin.
1. Eylem Bölmesinde, Sorguyu düzenleme iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.
1. İletişim kutusundaki **Sıralama** sekmesinde **Ekle**'yi seçerek kılavuza bir satır ekleyin:
1. Yeni satırda, kullanmak istediğiniz sıralama kurallarını tanımlayın. Örneğin, arama sonuçlarını sıra numarasına göre artan sırada sıralamak için aşağıdaki değerleri ayarlayın:

    - **Tablo:** *ayrıntıları yükle*
    - **Türetilmiş tablo:** *ayrıntıları yükle*
    - **Alan:** *Sipariş numarası*
    - **Arama yönü:** *Azalan*

1. Değişikliklerinizi kaydedip iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. **Kesme ölçütü** hızlı sekmesinde, yüklerinizin nasıl bölüneceğini kontrol eden kurallar ayarlayın. Genellikle, **Rota**, **Tur** veya **Çalıştır** gibi yükleme satırına genişletilmiş özel alanları kesebilirsiniz. Örneğin, her sipariş numarası için bir yükleme oluşturmak üzere, aşağıdaki değerlere sahip bir satır için **Kesme ölçütü** onay kutusunu işaretleyin:

    - **Referans tablosu adı:** *Yükleme ayrıntıları*
    - **Referans alan adı:** *Sipariş numarası*

## <a name="scenario"></a>Senaryo

Bu senaryo, bir satış siparişi işlendiği sırada bu konuda daha önce açıklanan ayarların Ambar işlemlerini nasıl etkilediğini gösterir. Bu senaryo, **USMF** demo verilerini bu kurulum yönergelerinde sağlanan diğer gösteri değerleriyle birlikte kullanır.

### <a name="create-sales-orders"></a>Satış siparişleri oluşturma

1. **Satış ve pazarlama** \> **Satış siparişleri** \> **Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Satış siparişleri oluştur** iletişim kutusunu açmak için **Yeni**'i seçin.
1. İletişim kutusunda aşağıdaki değerleri ayarlayın.

    - **Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını *ABD-007* olarak ayarlayın.
    - **Genel** hızlı sekmesinde, **Ambar** alanının ayarını *62* yapın.

1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişiniz açılır. **Satış siparişi satırları** hızlı sekmesi 'ndeki kılavuza yeni, boş bir satır dahil etmelidir. Bu yeni satırda, **Madde numarası** alanını *A0001* olarak ve **miktar** alanını *1* olarak ayarlayın.
1. Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.
1. **Rezervasyon** sayfasında, eylem bölmesinde, **Lot ayır** 'yi seçin.
1. Satış siparişine dönmek için sayfanın sağ üst köşesindeki **Kapat** düğmesini (**X**) seçin.
1. Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin. Mevcut yüklemede bu sipariş numarasına sahip yükleme satırları bulunduğundan, sistem bir sevkiyat ve bunu yeni bir yük ile ekler.

    Satış siparişi için oluşturulan iş, dalga ve sevkiyat kimliklerini gösteren bilgi iletileri alırsınız.

1. Satış satırında yükleme, Sevkiyat ve iş ayrıntılarını onaylamak için, satırı seçin ve ardından kılavuzun üzerindeki **ambar** menüsünde **Yük detayları**, **Sevkiyat detayları** veya **iş ayrıntıları**'nı seçin.
1. Oluşturduğunuz satış siparişinde, **Satış siparişi satırları** hızlı sekmesinde, başka bir satır eklemek için **Satır ekle**'yi seçin.
1. Bu yeni satırda, **Madde numarası** alanını *A0002* olarak ve **miktar** alanını *1* olarak ayarlayın.
1. Satırı rezerve etmek ve ambara serbest bırakmak için 6-9 arası satırları yineleyin. Sistem, eklediğiniz satır için **yeni** bir sevkiyat oluşturur. Ancak, gelişmiş dalga yükleme oluşturmayı kullandığınızdan, sistem o Sevkiyat ve yükleme hattını varolan dalgaya ekler. Gelişmiş dalga yükü oluşturmayı kullanmıyorsanız, sistem sevkiyat için yeni bir yük oluşturur.
1. Oluşturduğunuz satış siparişinde, **Satış siparişi satırları** hızlı sekmesinde, başka bir satır eklemek için **Satır ekle**'yi seçin.
1. Bu yeni satırda, **Madde numarası** alanını *M9200* olarak ve **miktar** alanını *1* olarak ayarlayın.
1. Satırı rezerve etmek ve ambara serbest bırakmak için 6-9 arası satırları yineleyin. Önceden olduğu gibi sistem, eklediğiniz satır için **yeni** bir sevkiyat oluşturur. Ancak, madde **CarAudio** madde grubundan olduğundan, **Yük karıştırma grubu için ayarladığınız sınırlamaları geçemezse**. Bu nedenle, **Yeni bir yüklemeye eklenir**. Yükleme oluştur şablonunda bir yük karışımı grubu belirtilmezse, bu sevkiyat ilk yüklemeye eklenmiş olmalıdır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]