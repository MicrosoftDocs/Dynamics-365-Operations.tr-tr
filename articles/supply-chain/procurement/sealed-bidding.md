---
title: RFQ'lar için kapalı teklif
description: Bu konuda, satıcının teklifinin satın alma personeli tarafından açılana kadar satıcı teklifi yanıtlarının gizli kalması için kapalı tekliflerin nasıl ayarlanacağı açıklanmaktadır.
author: yanansong
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 02cbe9d6a6d157208d73ed756efae24df2a082de
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500646"
---
# <a name="sealed-bidding-for-rfqs"></a>RFQ'lar için kapalı teklif

[!include [banner](../includes/banner.md)]

Kapalı teklif, satıcının teklif yanıtlarını, satın alma personeli tarafından açılana kadar gizli tutar. Teklif talebi (RFQ) ile ilgili tüm teklifler, teklifin sona ermesinin üzerine mührü açılacak şekilde ilk olarak kullanılabilir. Teklifin mührü açılmadan önce, teklife yalnızca ayrılmış kullanıcı rollerine sahip olan ve satıcıyı temsil eden kullanıcılar erişebilir.

> [!IMPORTANT]
> Formlar değiştirildiğinde veya genişletildiğinde ya da yeni formlar veya iş mantığı oluşturulduğunda, Microsoft'un kapalı teklif için sağladığı koruma ortadan kalkabilir. Değişiklikleri, uzantıları, yeni formları veya iş mantığını kullanma riski ya da bu gibi değişiklikler, uzantılar, yeni formlar veya iş mantığı nedeniyle kapalı teklif özelliğini kullanamama riski size aittir.  Microsoft, formlar için değişiklikler veya uzantılardan ya da oluşturduğunuz yeni formlar veya iş mantığından ya da sizin için içerik oluşturan üçüncü taraflardan kaynaklanan zararlardan sorumlu değildir. Microsoft, sizin veya sizin adınıza üçüncü taraflar tarafından yapılan değişiklikler, uzantılar, yeni formlar ya da iş mantığı için teknik veya başka türlü destek sağlamaz. Kapalı teklif ile ilgili geçerli tüm yasalara veya düzenlemelere uymaktan yalnızca siz sorumlusunuz.

## <a name="how-bids-are-kept-secure"></a>Tekliflerin güvenliğini sağlama

Kapalı teklif, teklif şifreleme anahtarını (KEK) şifrelemek için asimetrik şifrelemeyi ve gerçek teklifi şifrelemek için simetrik şifrelemeyi kullanır. Sistem, kapalı teklifleri şifrelemek için kullanılan şifreleme anahtarlarını oluşturmak ve yönetmek için Microsoft Azure Key Vault ile tümleşir. Her teklifin kendi şifreleme anahtarı vardır. Bu şifreleme, Dynamics 365 Supply Chain Management çalıştıran kuruluşun sahibi olduğu bir anahtar kasasında güvende tutulur. Sistem, şifreleme ve şifre çözme gerektiğinde anahtar kasasına isteğe bağlı olarak erişir.

## <a name="setup-and-configuration"></a>Kurulum ve yapılandırma

Bu bölümde, kapalı teklif gerektiren RFQ'ları göndermeden önce olması gereken önkoşullar açıklanmaktadır.

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>1. Adım: Mühürlü teklife kullanıcı erişimini ayarlama

Kapalı teklif kullandığınızda, yalnızca bir satıcı için ilgili kişi olarak ayarlanmış kullanıcılar, o satıcı için teklif verme süresi sona erene kadar teklifleri görüntüleyebilir, düzenleyebilir ve gönderebilir. Bu kullanıcılar **Satıcı (harici)** rolüne sahip olmalı ve satıcı hesabı için ilgili kişi olarak ayarlanmalıdır. İlgili kişinin ayrıca [Satıcı işbirliğini ayarlama ve koruma](set-up-maintain-vendor-collaboration.md) bölümünde açıklandığı gibi satıcı işbirliği yapma iznine sahip olması gerekir.

Uygun izinleri olan ve satıcı ilgili kişisi olarak ayarlanmış kullanıcılar, bir satıcının kapalı tekliflerine erişebileceğinden bu kullanıcıların kimler olduklarının izlenmesi önemlidir. Kullanıcıları ve güvenlik rollerini ayarlayan sistem yöneticisi, kapalı tekliflere erişimi teklifleri gerçekten görmelerine izin verilen kullanıcılarla sınırlamaktan sorumludur.

### <a name="step-2-enable-the-sealed-bidding-feature"></a>2. Adım: Kapalı teklif özelliğini etkinleştirme

Bu özelliği ayarlamaya veya kullanmaya başlamadan önce, bu özelliğin sisteminizde kullanılabilir olduğundan emin olmanız gerekir. Yöneticiler özellik durumunu denetlemek ve açmak için **[Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** çalışma alanını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Satınalma ve kaynaklandırma*
- **Özellik adı:** *RFQ'lar için kapalı teklif*

### <a name="step-3-set-up-azure-key-vault"></a>3. Adım: Azure Key Vault'u ayarlama

Supply Chain Management, tüm kapalı teklifleri korumak ve bunları uygun zamana kadar gizli tutmak için şifreleme anahtarları kullanır. Gerekli anahtarları oluşturmak ve yönetmek için Key Vault'un özelliklerinden yararlanır. Bu nedenle, sistemi etkinleştirmek için Supply Chain Management'tan bir anahtar kasasına bağlantı ayarlamanız gerekir.

> [!IMPORTANT]
> Anahtar kasası, kuruluşunuzun sahibi olduğu bir Azure aboneliğinde (Supply Chain Management'ı çalıştırdığınız abonelik değil) oluşturulmalıdır.

Her teklif kendi gizli anahtarını alır. Bu anahtar, kullanıcı teklifi her görüntülediğinde, güncelleştirdiğinde veya mührü açtığında kullanılır.

Satıcı, satıcı işbirliği arabiriminde **Teklif ver**'i seçtiğinde Key Vault gizli anahtarı almak için kullanılan anahtarı oluşturur. Anahtarın süresi, tedarik yöneticisinin Supply Chain Management'taki **Tedarik ve Kaynak Atama Parametreleri** sayfasında belirlediği sabit bir süreden sonra sona erer. Anahtarın süresi dolduktan sonra kimse teklifi görüntüleyemez, düzenleyemez veya teklifin mührünü açamaz. Bu nedenle, anahtarın bitiş tarihini, teklif verme sürecinin tamamlanması için yeterli zaman olacak şekilde yapılandırmak önemlidir.

Sonraki üç adımda, Key Vault bağlantısını ayarlarsınız. Öncelikle, kapalı teklif ile kullanmak için bir anahtar kasası ayarlarsınız. Ardından, Supply Chain Management'ı anahtar kasasıyla iletişim kuracak şekilde yapılandırırsınız. Son olarak, anahtarın bitiş zamanını ayarlarsınız.

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>4. Adım: Kapalı teklifle kullanmak için bir anahtar kasası ayarlama

Anahtar kasanızı ayarlamak için aşağıdaki adımları izleyin. Adımların sırası önemlidir.

1. Supply Chain Management'ı çalıştırdığınız abonelikten ayrı bir Azure aboneliğini zaten ayarlamadıysanız bunu ayarlayabilirsiniz.
1. Ayrı Azure depolama alanınızda bir anahtar kasası ayarlayın. Daha fazla bilgi için bkz. [Azure Key Vault depolamayı yönetme](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage).
1. Anahtar kasanız için istemci olarak çalışmak üzere Supply Chain Management uygulamanızı ayarlayın. Daha fazla bilgi için bkz. [Azure Key Vault İstemcisini ayarlama](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client).

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>5. Adım: Supply Chain Management'ta Key Vault parametrelerini yapılandırma

Supply Chain Management'ı kapalı teklif verme sırasında anahtar kasasıyla iletişim kuracak şekilde yapılandırmak için aşağıdaki adımları izleyin.

1. Supply Chain Management'ta oturum açın ve **Sistem yönetimi \> Kurulum \> Key Vault parametreleri**'ne gidin.
1. Kayıt oluşturmak için **Yeni**'yi seçin ve bunun için aşağıdaki alanları ayarlayın:

    - **Ad**: Ad girin.
    - **Açıklama**: Açıklama girin.
    - **Key Vault URL'si**: Anahtar kasanızın varsayılan URL'sini girin.
    - **Key Vault istemcisi**: Kimlik doğrulaması için bir anahtar kasasıyla ilişkili Active Directory uygulamasının etkileşimli istemci kimliğini girin.
    - **Key Vault gizli anahtarı**: Sertifika için gizli anahtar başvurusunu girin.
    - **Kapalı teklif için etkinleştirildi**: Bu seçeneği *Evet* olarak ayarlayın.

![Key Vault parametreleri sayfası](media/sealed-bidding-key-vault-param.png "Key Vault parametreleri sayfası")

> [!NOTE]
> Kapalı teklif için aynı anda yalnızca bir anahtar kasası yapılandırmasını etkinleştirebilirsiniz. Mevcut anahtar kasası yapılandırmasını devre dışı bırakmadan önce, onu kullanan tüm kapalı tekliflerin mührünün açık olduğundan emin olmanız gerekir. *Kapalı* türdeki tüm RFQ dosyalarını inceleyin ve bunlar için tüm yanıtların mühürsüz olduğundan emin olun.

### <a name="step-6-set-the-key-expiration-time"></a>6. Adım: Anahtarın bitiş zamanını ayarlama

Her yeni teklif için oluşturulan anahtara uygulanan bitiş tarihini ayarlamak için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak atama parametreleri \> Kurulum \> Tedarik ve kaynak atama parametrelerine**'ne gidin.
1. **Teklif talebi** sekmesindeki **Denkleştirme gün sayısı** alanına, RFQ döneminin sürmesi gereken gün sayısını girin. Bir RFQ oluşturulduğunda, RFQ için varsayılan bitiş tarihini tanımlamak için girdiğiniz gün sayısı sistem tarihine eklenir.
1. **Şifreleme anahtarı bitiş tarihi denkleştirme** alanında, her şifreleme anahtarı verildikten sonra geçerli olması gereken gün sayısını girin. Şifreleme anahtarı bitiş tarihi dolduktan sonra, onu kullanan hiç kimse kapalı teklifi görüntüleyemez, düzenleyemez veya teklifin mührünü açamaz.

> [!TIP]
> **Şifreleme anahtarı bitiş tarihi denkleştirme** alanının değeri, **Denkleştirme gün sayısı** alanının değerinden az olmamalıdır.

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>7. Adım: Varsayılan teklif türünü ayarlama

Her RFQ dosyasının bir teklif türü vardır. Teklif türü, RFQ dosyasının açık veya kapalı teklif sağladığını tanımlar.

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>Talep türü bulunmayan RFQ dosyaları

Oluşturulduklarında bir talep türü atanmamış yeni RFQ dosyalarına atanan varsayılan teklif türünü ayarlamak için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak atama parametreleri \> Kurulum \> Tedarik ve kaynak atama parametrelerine**'ne gidin.
1. **Teklif talebi** sekmesinde, **Teklif türü** alanını *Kapalı* olarak ayarlayın.

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>Talep türü bulunan RFQ dosyaları

Oluşturulduklarında bir talep türü atanmış yeni RFQ dosyalarına atanan varsayılan teklif türünü ayarlamak için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak atama \> Kurulum \> Teklif Talebi \> Talep türü**'ne gidin.
1. Yeni bir talep türü oluşturun veya *Kapalı* teklif türünü kullanmak istediğiniz var olan bir talep türü seçin.
1. **Teklif türü** alanını *Kapalı* olarak ayarlayın.
1. Kapalı teklif uygulamak istediğiniz her ek talep türü için bu adımları tekrarlayın.

> [!TIP]
> Yeni bir RFQ oluşturulduğunda bir talep türünün atanması gerekmez. Bir talep türü atanmışsa RFQ için varsayılan teklif türü bunu alabilir. Aksi takdirde, Tedarik ve kaynak atama parametrelerinde tanımlanan varsayılan talep türü kullanılabilir.

## <a name="the-sealed-bidding-process"></a>Kapalı teklif işlemi

Kapalı teklif, [Teklif taleplerine (RFQ'lar) genel bakış](request-quotations.md)'ta açıklananla neredeyse aynı işlemi izler. Aralarındaki temel fark, teklif verilerinin ve eklerinin teklifin mührü açılana kadar şifreli tutulmasıdır.

> [!IMPORTANT]
> [Soru formları](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) şifreli değildir ve hassas bilgileri toplamak için kullanılmamalıdır

Bu işlemin ana hattı aşağıda verilmiştir:

1. RFQ oluşturup bir veya daha fazla satıcıya gönderirsiniz.
1. Satıcılar kapalı tekliflerini göndererek yanıtlarlar.
1. Teklif girişinin bitiş tarihinden sonra tekliflerin mührünü açarsınız.
1. Teklifler görünür hale gelir ve bunları değerlendirip karşılaştırabilirsiniz.
1. Teklif kabul edildikten sonra, bir satınalma siparişi ve satınalma sözleşmesi oluşturun veya bir satınalma talebini güncelleştirin.

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>Kapalı teklif kullanan bir RFQ dosyası oluşturma

Kapalı teklif için RFQ dosyası oluşturma işlemi, kapalı olmayan teklif işlemi ile neredeyse aynıdır. Her iki türde RFQ dosyaları oluşturmak hakkında bilgi için bkz. [Teklif talebi oluşturma](tasks/create-request-quotation.md). Bu bölümde, bir kapalı teklif için RFQ oluştururken dikkate almanız gereken bazı önemli noktalar vurgulanmaktadır.

Kapalı teklif için RFQ dosyalarının **Teklif türü**, *Kapalı* olmalıdır. Bu değeri bir RFQ dosyasına atamanın üç yolu vardır:

- Dosyayı oluşturduktan sonra değeri doğrudan RFQ dosyasında belirleyin.
- Tedarik ve kaynak atama parametrelerinde tüm RFQ dosyaları için varsayılan teklif türü olarak kapalı teklifi tanımlayın. (Bu konunun önceki [Varsayılan teklif türünü ayarlama](#set-default-bid-type) bölümüne bakın.)
- Yeni bir RFQ dosyası oluşturduğunuzda, kapalı teklif için ayarlanmış bir talep türü seçin. ([Varsayılan teklif türünü ayarlama](#set-default-bid-type) bölümüne bakın.)

Kapalı teklif için RFQ dosyasının **Bitiş tarihi ve saati** değeri, gönderilen tekliflerin mührünün ne zaman açılabileceğini belirler. Her satırdaki **Bitiş tarihi ve saati** değeri, başlıktaki değerle eşleşir.

RFQ dosyası gönderildikten sonra teklif türünü değiştiremezsiniz.

### <a name="vendors-respond-to-an-rfq"></a>RFQ'ya satıcıların yanıtı

Kapalı teklifi yanıtlayan satıcılar, [Satıcı teklifi çalışma alanında RFQ'larla çalışma](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace) bölümünde açıklandığı şekilde açık teklifleri yanıtlamak için kullandıkları yordamla aynı yordamı kullanırlar. Hem açık tekliflerle hem de kapalı tekliflerle nasıl çalışılacağına ilişkin ayrıntılı talimatlar için bkz. [RFQ tekliflerini girip karşılaştırma ve işi verme](tasks/enter-compare-rfq-bids-award-contracts.md). Kapalı tekliflerin işlenmesi ile açık tekliflerin işlenmesi arasındaki tek fark, teklif verme süresi sona erene kadar tedarik profesyonellerinin satıcının kapalı teklifini açamamasıdır. Satıcının kapalı teklifini yalnızca satıcının ilgili kişisi açabilir.

> [!IMPORTANT]
> Kapalı teklif için satıcılar, ekleri yalnızca PDF formatında yükleyebilir. Başka biçimler kabul edilmez.

Kayıtlı bir satıcı kullanıcısı, bir kapalı teklif RFQ'sunda **Teklif ver**'i seçtikten sonra, teklif verilerini girebilir ve bu veriler güvende tutulur. Satıcılar, bir teklif hazırlarken çalışmalarını kaydedebilir, gerektiği sıklıkta teklife geri dönebilir ve ardından hazır olduğunda teklifi gönderebilir. Satıcılar, tekliflerini gönderdikten sonra görüntüleyebilir. Satıcılar tekliflerini gönderdikten sonra değiştirmeleri gerekirse teklif süresi sona erinceye kadar diledikleri zaman tekliflerini geri çağırabilir, güncelleştirebilir ve yeniden gönderebilir.

Kapalı teklif sırasında aşağıdaki koşullar geçerlidir:

- Kapalı teklif sırasında sistem *Teklif talebi* günlüğü oluşturur.
- Satıcı bir teklif gönderdiğinde, kapalı fiyatı olan ve satır içermeyen RFQ günlükleri oluşturulur.
- Dosyanın mührü açıldıktan sonra, fiyat ve tutarı olan RFQ günlükleri oluşturulur. Bu günlüğe **Tüm teklif talepleri** sayfasında **Teklif talebi günlükleri**'ni seçerek erişebilirsiniz.
- Sistem, bir kapalı teklif üzerinde kullanıcıların gerçekleştirdiği her bir eylemin günlüğünü depolar. Bu eylemler, teklifin görüntülenmesini, düzenlenmesini ve kaydedilmesini içerir. Bu günlük, hem satıcı hem de teklife erişimi olan tedarik profesyonelleri tarafından görülebilir.
- Teklif ilerledikçe, tedarik profesyonelleri teklifin durumunu görüntüleyebilir. Durum *Satıcı güncelleştiriyor* veya *Satıcı tarafından gönderildi* olur.
- Kapalı teklifin içindeki satırların durumu, teklifin mührü açılana kadar *Gönderildi* olarak kalır.
- Satıcı bir teklifi reddetmeyi seçerse teklifin **Yanıt ilerlemesi** durumu *Satıcı tarafından reddedildi* olur. Bu durum, tedarik profesyoneli tarafından görülebilir.
- Soru formlarındaki yanıtlar, veritabanındaki şifrelenmiş formda **depolanmaz**. Bu nedenle, bunlar mühürlenmez. Ancak dosyanın mührü açılana kadar RFQ kullanıcı arabiriminde görünmez.

### <a name="all-sealed-bid-activities-are-logged"></a>Tüm kapalı teklif etkinlikleri kaydedilir

Bir teklif için tüm kullanıcı etkinlikleri ve eylemleri ayrıntılı bir günlükte kaydedilir. Etkinlik günlüğü, kuruluşların bir teklifi kullanım ömrü boyunca kimin güncelleştirdiğini ve güncelleştirmelerin neler olduğunu belirlemesini sağlar. Ayrıca kuruluşların bir kapalı teklifle yalnızca yetkili kişilerin eriştiğini onaylamasını sağlar. Etkinlik günlüğü her teklifin **Etkinlik** sayfasında kullanılabilir.

### <a name="review-rfq-activity"></a>RFQ etkinliğini inceleme

Teklifle yapılan tüm etkileşimler günlüğe kaydedilir ve **Etkinlik** sayfasında görüntülenebilir. Aşağıdaki şekilde bir örneği gösterilmiştir.

![Etkinlik sayfası örneği](media/sealed-bidding-rfq-activity.png "Etkinlik sayfası örneği")

Satıcılar, **Teklif Talebi Kapalı teklifi** sayfasında **Etkinlik**'i seçerek **Etkinlik** sayfasına erişebilir. Tedarik personeli, **Teklif Talebi** sayfasında **Etkinlik**'i seçerek erişebilir. Etkinlik günlüğü, satıcılar ve teklife erişimi olan tedarik personeli için tam görünürlük sağlar. Bu nedenle, herhangi bir yetkisiz erişimi ortaya çıkarabilir.

### <a name="unseal-sealed-bids"></a>Kapalı tekliflerin mührünü açma

Kapalı teklif RFQ dosyası için yapılandırılan **Bitiş tarihi ve saati** değeri geçtiğinde, **Mührü Aç** düğmesi kullanılabilir hale gelir. Seçili RFQ dosyası için tüm tekliflerin mührünü açmak üzere **Mührü Aç**'ı seçin. Tüm teklif verileri ve ekleri daha sonra görünür hale gelir. Böylece dosyaya verilen yanıtlar yönetilebilir. Ek olarak, gönderilen teklif verilerini içeren günlükler oluşturulur.

Mührü açma olayı günlüğe kaydedilir ve **Etkinlik** sayfasında görüntülenebilir.

### <a name="process-accepted-bids"></a>Kabul edilen teklifleri işleme

Önceden kapalı olan teklifleri karşılaştırma ve onaylama işlemi, açık teklifler için olan işlemle aynıdır. Kapalı teklifleri puanlama, karşılaştırma, reddetme ve kabul etme hakkında bilgi için bkz. [RFQ tekliflerini girip karşılaştırma ve işi verme](tasks/enter-compare-rfq-bids-award-contracts.md).

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>RFQ etkinlik günlüğü hiçbir zaman silinemez

Yöneticiler ve Microsoft Desteği de dahil olmak üzere hiç kimse RFQ etkinlik günlüğünü düzenleyemez veya silemez. Bu kısıtlama, kapalı teklif işleminin adilliğinin sağlanmasına yardımcı olur. Ayrıca doğru denetim kaydının tutulmasını sağlamaya da yardımcı olur.
