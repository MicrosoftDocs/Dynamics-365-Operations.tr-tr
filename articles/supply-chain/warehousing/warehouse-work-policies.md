---
title: İş ilkeleri
description: Bu konuda, iş ilkelerinin nasıl ayarlanacağını açıklanmaktadır.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 08c04caeace7b8ced40915ace1561d817426cba3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439709"
---
# <a name="work-policies"></a>İş ilkeleri

[!include [banner](../includes/banner.md)]

Bu konu, sistemin ve ambar uygulamasının iş ilkelerini destekleyecek şekilde nasıl ayarlanacağını açıklar. Bu işlevi, satın alma veya transfer emirleri aldığınızda ya da üretim sürecini tamamladığınızda, yerine koyma işi oluşturmadan stoku hızlı bir şekilde kaydetmek için kullanabilirsiniz. Bu konu genel bilgileri sağlar. Plaka alma ile ilgili ayrıntılı bilgi için bkz. [Ambar uygulaması üzerinden plaka alma](warehousing-mobile-device-app-license-plate-receiving.md).

İş ilkesi, üretilen bir kalem tamamlandı olarak bildirildiğinde veya ambar uygulaması kullanılarak mal alındığında ambar işi oluşturulup oluşturulmayacağını denetler. Her iş ilkesini, uygulandığı koşulları tanımlayarak ayarlayabilirsiniz: iş emri türleri ve süreçleri, stok konumu ve (isteğe bağlı olarak) ürünler. Örneğin, A *0001* ürününün satın alma siparişi ambar *24*'te *RECV* konumuna alınmalıdır. Daha sonra, ürün, *RECV* konumunda başka bir işlemde kullanılır. Bu durumda, bir çalışan *A0001* ürününün *RECV* konumuna alındığını bildirdiğinde yerine koyma işi oluşturmayı önleyecek bir iş ilkesi ayarlayabilirsiniz.

> [!NOTE]
> - Bir iş ilkesinin etkin olması için **İş ilkeleri** sayfasının **Stok konumları** hızlı sekmesinde en az bir konum tanımlamanız gerekir. 
> - Birden fazla iş ilkesi için aynı konumu belirtemezsiniz.
> - Mobil cihaz menüsü öğelerinin **yazdırma etiketi** seçeneği, iş oluşturulmadıysa plaka etiketi yazdırmayacaktır.

## <a name="activate-the-features-in-your-system"></a>Sisteminizde özellikleri etkinleştirme

Bu konuda açıklanan tüm işlevleri sisteminizde kullanılabilir hale getirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'nde aşağıdaki iki özelliği etkinleştirin:

- Plaka teslim alma geliştirmeleri
- Gelen iş için iş ilkesi geliştirmeleri

## <a name="the-work-policies-page"></a>İş ilkeleri sayfası

İş ilkelerini ayarlamak için **Ambar Yönetimi \> Kurulum \> İş \> Çalışma ilkeleri**'ne gidin. Sonra, her hızlı sekmede, alanları aşağıdaki alt kısımlarda açıklandığı gibi ayarlayın.

### <a name="the-work-order-types-fasttab"></a>İş emri türleri hızlı sekmesi

**İş emri türleri** hızlı sekmesinde, tüm iş emri türlerini ve çalışma ilkesinin geçerli olduğu ilgili iş süreçlerini ekleyin. İş ilkeleri için aşağıdaki iş emri türleri ve ilgili iş süreçleri desteklenir.

| İş siparişi türü | İş süreci |
|---|---|
| Hammadde çekme| İlgili tüm süreçler |
| Yerine konan ortak ürün ve yan ürün | İlgili tüm süreçler |
| Memul mal yerine koyma | İlgili tüm süreçler |
| Transfer alış irsaliyesi | Plaka alma (ve yerine koyma) |
| Satın alma siparişleri | <ul><li>Plaka alma (ve yerine koyma)</li><li>Yük kalemi teslim alma (ve yerine koyma)</li><li>Satın alma siparişi satırı teslim alma (ve yerine koyma)</li><li>Satın alma siparişi kalemini teslim alma (ve yerine koyma)</li></ul> |

Bir iş ilkesini aynı iş emri türündeki birkaç iş sürecinde geçerli olacak şekilde ayarlamak için kılavuza her çalışma işlemine yönelik ayrı bir satır ekleyin.

Kılavuzdaki her satır için **İş oluşturma yöntemi** alanını aşağıdaki değerlerden birine ayarlayın:

- **Hiçbir zaman**: İş ilkesi seçili iş emri türü için ambar işinin ve ilgili iş sürecinin oluşturulmasını önler.
- **Çapraz sevk**: İş ilkesi, **Çapraz sevk ilkesi adı** alanında seçtiğiniz ilkeyi kullanarak çapraz sevk işi oluşturur.

### <a name="the-inventory-locations-fasttab"></a>Stok konumları hızlı sekmesi

**Stok konumları** hızlı sekmesinde, bu iş ilkesinin uygulanacağı tüm konumları ekleyin. İş ilkesi ile ilişkilendirilmiş bir konum yoksa iş ilkesi herhangi bir sürece uygulanmaz.

Birden fazla iş ilkesi için aynı konumu belirtemezsiniz.

**Plaka izlemeyi kullan** seçeneği kapalı olduğunda bir konum profiline atanmış ambar konumu kullanılabilir. Bu durumda, çalışanlar eldeki stoku doğrudan kaydeder.

### <a name="the-products-fasttab"></a>Ürünler hızlı sekmesi

**Ürünler** sekmesinde, ilkenin hangi ürünlere uygulanacağını denetlemek için **Ürün seçimi** alanını ayarlayın:

- **Tümü**: İlke tüm ürünler için geçerli olur.
- **Seçili**: İlke yalnızca kılavuzda listelenen ürünler için geçerli olur. Kılavuza ürün eklemek veya kılavuzdan ürün kaldırmak için **Ürünler** hızlı sekmesindeki araç çubuğunu kullanın.

## <a name="default-and-custom-to-locations"></a>Varsayılan ve özel "hedef" konumlar

> [!NOTE]
> Bu bölümde açıklanan işlevselliğin sisteminizde kullanılabilmesini sağlamak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ndeki gelen *Plaka alma geliştirmeleri* ve *Gelen iş için iş ilkesi geliştirmeleri*'ni açmanız gerekir.

Daha önce sistem, yalnızca her ambar için tanımlanan varsayılan konumda almayı destekler. Ancak, aşağıdaki iş oluşturma süreçlerini kullanan mobil cihaz menü öğeleri artık **Varsayılan verileri kullan** seçeneğini sağlar. Bu seçenek, bir veya daha fazla menü öğesine özel bir "hedef" konum atamanıza olanak tanır. (Bu seçenek bazı menü öğesi türleri için zaten kullanılabilir.)

- Plaka alma (ve yerine koyma)
- Yük kalemi teslim alma (ve yerine koyma)
- Satın alma siparişi satırı teslim alma (ve yerine koyma)
- Satın alma siparişi kalemini teslim alma (ve yerine koyma)

Bir menü öğesinin **Hedef konum** ayarı, o menü öğesi kullanılarak işlenen tüm siparişler için ambarın varsayılan alma konumunu geçersiz kılar.

Bir mobil cihaz menü öğesini özel bir konumda almayı destekleyecek şekilde ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Bu bölümün önceki kısımlarında listelenen iş oluşturma süreçlerinden birini kullanan bir menü öğesi seçin veya oluşturun.
1. **Genel** hızlı sekmesinde, **Varsayılan verileri kullan** seçeneğini **Evet** olarak ayarlayın.
1. Eylem Bölmesinde **Varsayılan veriler**'i seçin.
1. **Varsayılan veriler** sayfasında, aşağıdaki değerleri ayarlayın:

    - **Varsayılan veri alanı:** Bu alanı *Hedef konum* olarak ayarlayın.
    - **Ambar:** Bu menü öğesiyle kullanılacak hedef ambarı seçin.
    - **Konum:** Bu alan, seçili ambar için kullanılabilir olan tüm konum kimliklerini listeler. Ancak, bu alanın ayarı aslında herhangi bir etkiye sahip değildir. Bu nedenle boş bırakabilirsiniz. Bununla birlikte, **Sabit kodlu değer** alanına girmeniz gereken kimliği onaylamak için listeyi kullanabilirsiniz.
    - **Sabit kodlu değer:** Bu menü öğesi için geçerli olan giriş konumunun konum kimliğini girin.

> [!TIP]
> Bir iş ilkesi, yalnızca tüm alma konumları ilgili iş ilkesi kurulumunda listeleniyorsa uygulanabilir. Bu gereksinim, varsayılan ambar teslim alma konumu veya özel "hedef" konum olup olmadığına bakılmaksızın uygulanır.

## <a name="example-scenario-warehouse-receiving"></a>Örnek senaryo: Ambar teslim alma

*Satınalma sipariş kalemi teslim alma (ve yerine koyma)* süreci tarafından alınan tüm ürünler, *FL-001* konumunda kayıtlı olmalıdır ve bunlar ambar *24*' te kullanılabilir olmalıdır. Ancak, iş oluşturulmamalıdır. Başka bir süreç (diğer mobil cihaz menü öğelerini kullanan) tarafından teslim alınan ürünler varsayılan ambar teslim alma konumuna (*RECV*) kaydedilmelidir ve her zamanki gibi iş oluşturulması gerekir. (Bu senaryo varsayılan teslim alma kurulumunu göstermez.)

Bu senaryo için aşağıdaki öğeler gereklidir:

- Tüm ürünler için *FL-001* konumuna *Satın alma sipariş kalemi teslim alma (ve yerine koyma)* süreci iş ilkesi
- Varsayılan verileri olan ve **Hedef konum** alanı *FL-001* olarak ayarlanmış bir mobil cihaz menü öğesi

### <a name="prerequisites"></a>Önkoşullar

Bu senaryoda açıklanan işlevselliğin sisteminizde kullanılabilmesini sağlamak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ndeki gelen *Plaka alma geliştirmeleri* ve *Gelen iş için iş ilkesi geliştirmeleri*'ni açmanız gerekir.

Bu senaryo stamdart demo verilerini kullanır. Bu nedenle, burada sunulan değerleri kullanarak bu senaryoyla çalışmak istiyorsanız demo verilerinin yüklenmiş olduğu bir sistemde çalışmanız gerekir. Ayrıca, **USMF** hukuk varlığını seçmelisiniz.

### <a name="set-up-a-work-policy"></a>İş ilkesi ayarlama

1. **Ambar yönetimi \> Kurulum \> İş \> İş ilkeleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **İş ilkesi adı** alanında, *Satın alma kalemi yerine koyma işi yok* girin.
1. **Kaydet**'i seçin.
1. **İş emri türleri** hızlı sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:

    - **İş emri türü:** *Satın alma siparişleri*
    - **İş süreci:** *Satın alma sipariş kalemi teslim alma (ve yerine koyma)*
    - **İş oluşturma yöntemi:** *Hiçbir zaman*
    - **Çapraz sevk ilkesi adı:** Bu alanı boş bırakın.

1. **Stok konumları** hızlı sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:

    - **Ambar:** *24*
    - **Konum:** *FL-001*

1. **Ürünler** hızlı sekmesinde, **Ürün seçimi** alanını *Tümü* olarak ayarlayın.
1. **Kaydet**'i seçin.

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a>Teslim alma konumunu değiştirmek için bir mobil cihaz menü öğesi ayarlama

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Sol bölmede, varolan **Satın alma teslimi** menü öğesini seçin.
1. **Genel** hızlı sekmesinde, **Varsayılan verileri kullan** seçeneğini *Evet* olarak ayarlayın.
1. **Kaydet**'i seçin.
1. Eylem Bölmesinde **Varsayılan veriler**'i seçin.
1. **Varsayılan veriler** sayfasında, Eylem Bölmesinde kılavuza satır eklemek için **Yeni**'yi seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:

    - **Varsayılan veri alanı:** *Hedef konum*
    - **Ambar:** *24*
    - **Konum:** Bu alanı boş bırakın.
    - **Sabit kodlu değer:** *FL-001*

1. **Kaydet**'i seçin.

### <a name="receive-a-purchase-order-without-creating-work"></a>İş oluşturmadan bir satın alma siparişi teslim alma

Bu bölümdeki örnekte, bir satın alma siparişi kaleminin ambar için ayarlanan varsayılan teslim alma konumundan farklı bir konumda iş oluşturulmadan nasıl teslim alınacağı gösterilmiştir. Bu örnekte, bu senaryoda daha önce oluşturduğunuz iş ilkesi ve mobil cihaz öğesi kullanılmaktadır.

#### <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma

1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Satıcı hesabı:** *US-101*
    - **Tesis:** *2*
    - **Ambar:** *24*

1. İletişim kutusunu kapatmak ve yeni satın alma siparişini açmak için **Tamam**'ı seçin.
1. **Satın alma siparişi satırları** hızlı sekmesinde, boş satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *1*

1. **Kaydet**'i seçin.
1. Satın alma siparişi numarasını not edin.

#### <a name="receive-a-purchase-order"></a>Satın alma siparişi teslim alma

1. Mobil cihazda, kullanıcı kimliği olarak *24* ve parola olarak *1* girerek ambar *24*'te oturum açın.
1. **Gelen**'i seçin.
1. **Satın alma teslim alma** öğesini seçin. **Konum** alanı *FL-001* olarak ayarlanmalıdır.
1. Önceki yordamda oluşturduğunuz satın alma siparişinin satın alma siparişi numarasını girin.
1. **Kalem numarası** alanına *A0001* girin.
1. **Tamam**'ı seçin.
1. **Miktar** alanına *1* yazın.
1. **Tamam**'ı seçin.

Satın alma siparişi artık teslim alındı, ancak ilişkilendirilmiş iş yok. Eldeki stok güncelleştirildi ve *FL-001* konumunda *A0001* kaleminden *1* adet bulunuyor.

## <a name="example-scenario-manufacturing"></a>Örnek senaryo: Üretim

Aşağıdaki örnekte, *PRD-001* ve *PRD-002* olmak üzere iki üretim emri bulunmaktadır. Üretim emri *PRD-001*, *SC1* ürününün *001* konumuna tamamlandı olarak bildirildiği *Derleme* adlı bir işleme sahiptir. Üretim emri *PRD-002*, *Boyama* adlı bir işleme sahiptir ve *001* konumundan *SC* 1 ürününü kullanır. Üretim emri *PRD-002* de *001* konumundan *RM* 1 hammaddesini kullanır. *RM1* hammaddesi, *BULK-001* ambar konumunda depolanır ve hammadde çekmeye yönelik ambar işi tarafından *001* konumuna çekilir. Malzeme çekme işi *PRD-002* üretimi serbest bırakıldığında oluşturulur.

[![Ambar iş ilkeleri](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)

Bu senaryo için bir ambar işi ilkesi yapılandırmayı planlarken, aşağıdaki hususları göz önünde bulundurmalısınız:

- Yerine konan mamul mallar için ambar işi, *SC1* ürününü *PRD-001* üretim emrinden *001* konumuna tamamlandı olarak bildirdiğinizde gerekli değildir. Bunun nedeni *PRD-002* üretim emrinin *Boyama* işleminin *SC* 1 ürününün aynı konumda kullanmasıdır.
- Hammadde çekme için ambar işi *RM* 1 hammaddesini *BULK-001* ambar konumundan *001* konumuna taşımak için gereklidir.

Bu noktalara göre, ayarlayabileceğiniz iş ilkesine bir örneği aşağıda bulabilirsiniz:

- **İş ilkesi adı:** *Yerine koyma işi yok*
- **İş emri türleri:** *Mamul mal yerine koyma* ve *Ortak ürün ve yan ürün yerine koyma*
- **Stok konumları:** Ambar *51* ve konum *001*
- **Ürünler:** *SC1*

Aşağıdaki örnek senaryo bu senaryo için ambar iş ilkesini ayarlama konusunda adım adım yönergeler sağlar.

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Örnek senaryo: Plaka denetimli olmayan bir konuma tamamlandı olarak bildirme

Bu senaryo, bir üretim emrinin plaka denetimli olmayan bir konuma tamamlandı olarak bildirildiği bir örneği göstermektedir.

Bu senaryo stamdart demo verilerini kullanır. Bu nedenle, burada sunulan değerleri kullanarak bu senaryoyla çalışmak istiyorsanız demo verilerinin yüklenmiş olduğu bir sistemde çalışmanız gerekir. Ayrıca, **USMF** hukuk varlığını seçmelisiniz.

### <a name="set-up-a-warehouse-work-policy"></a>Ambar iş ilkesi ayarlama

Ambar işlemi her zaman ambar çalışmasını içermezler. Bir çalışma ilkesi tanımlayarak, hammadde çekme ve tamamlanmış malların yerine koyması işlerinin oluşturulmasını, çeşitli bir ürün dizisi veya belirtilen konumlar için engelleyebilirsiniz.

1. **Ambar yönetimi \> Kurulum \> İş \> İş ilkeleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **İş ilkesi adı** alanında, *Yerine koyma işi yok* girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **İş emri türleri** hızlı sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:

    - **İş emri türü:** *Mamul malları yerine koyma*
    - **İş süreci:** *Tüm ilgili iş süreçleri*
    - **İş oluşturma yöntemi:** *Hiçbir zaman*
    - **Çapraz sevk ilkesi adı:** Bu alanı boş bırakın.

1. Kılavuza ikinci bir satır eklemek için **Ekle**'yi tekrar seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:

    - **İş emri türü:** *Ortak ürün ve yan ürün yerine koyma*
    - **İş süreci:** *Tüm ilgili iş süreçleri*
    - **İş oluşturma yöntemi:** *Hiçbir zaman*
    - **Çapraz sevk ilkesi adı:** Bu alanı boş bırakın.

1. **Stok konumları** hızlı sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:

    - **Ambar:** *51*
    - **Konum:** *001*

1. **Ürünler** hızlı sekmesinde, **Ürün seçimi** alanını *Seçili* olarak ayarlayın.
1. **Ürünler** hızlı sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda, **Kalem numarası** alanını *L0101* olarak ayarlayın.
1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="set-up-an-output-location"></a>Bir çıkış konumu ayarlama

1. **Kuruluş yönetimi \> Kaynaklar \> Kaynak grupları**'na gidin.
1. Sol bölmeden **5102** kaynak grubunu seçin.
1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Çıkış ambarı:** *51*
    - **Çıkış konumu:** *001*

1. Eylem bölmesinde, **Kaydet**'i seçin.

> [!NOTE]
> *001* konumu, plaka denetimli bir konum değildir. Konum için geçerli bir çalışma ilkesi bulunuyorsa sadece, plaka denetimli olmayan bir çıkış konumu ayarlayabilirsiniz.

### <a name="create-a-production-order-and-report-it-as-finished"></a>Bir üretim emri oluşturun ve bunu tamamlandı olarak rapor edin

1. **Üretim denetimi \> Üretim emirleri \> Tüm üretim emirleri**'ne gidin.
1. Eylem Bölmesinde **Yeni üretim emri**'ni seçin.
1. **Üretim emri oluştur** iletişim kutusunda, **Kalem numarası** alanını *L0101* olarak ayarlayın.
1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Oluştur**'u seçin.

    **Tüm üretim emirleri** sayfasındaki kılavuza yeni bir üretim emri eklenir.

    Yeni üretim emrini seçili durumda tutun.

1. Eylem Bölmesinde, **Üretim emri** sekmesinde **İşlem** grubunda **Tahmin**'i seçin.
1. **Tahmin** iletişim kutusunda tahmini okuyun ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Eylem Bölmesinde, **Üretim emri** sekmesinde **İşlem** grubunda **Başlat**'ı seçin.
1. **Başlat** iletişim kutusunda, **Genel** sekmesinde, **Otomatik BOM kullanımı** alanını *Hiçbir zaman* olarak ayarlayın.
1. Ayarınızı kaydedip iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Eylem Bölmesinde, **Üretim emri** sekmesinde **İşlem** grubunda **Tamamlandı olarak bildir**'i seçin.
1. **Tamamlandı olarak bildir** iletişim kutusunda, **Genel** sekmesinde **Hatayı kabul et** seçeneğini *Evet* olarak ayarlayın.
1. Ayarınızı kaydedip iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Eylem Bölmesinde **Ambar** sekmesindeki **Genel** grubunda **İş ayrıntıları**'nı seçin.

Üretim emri, tamamlandı olarak bildirildiğinde, yerine koyma için hiçbir iş üretilmez. Bu davramış, Ürün *L0101*, konum *001*'e tamamlandı olarak bildirildiğinde işin oluşturulmasının engellenmesi için tanımlanan bir iş ilkesi bulunmasından kaynaklanır.

## <a name="more-information"></a>Daha fazla bilgi

Mobil cihaz menü öğeleri hakkında daha fazla bilgi için bkz. [Ambar işi için mobil cihazları ayarlama](configure-mobile-devices-warehouse.md).

Plaka alma ve iş ilkeleri ile ilgili ayrıntılı bilgi için bkz. [Ambar uygulaması üzerinden plaka alma](warehousing-mobile-device-app-license-plate-receiving.md).

Giriş yük yönetimi hakkında daha fazla bilgi için bkz. [Satınalma siparişleri için gelen yüklerin ambarda işlenmesi.](inbound-load-handling.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]