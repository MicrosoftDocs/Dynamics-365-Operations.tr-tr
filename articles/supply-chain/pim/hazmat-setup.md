---
title: Tehlikeli malzemeleri ayarlama
description: Bu konuda, maddeleri tehlikeli malzeme olarak sınıflandırmak için gerekli verilerin nasıl ayarlanacağı açıklanmaktadır. Tehlikeli malzeme olarak sınıflandırılmış bir madde içeren bir satış siparişi oluşturduğunuzda sistem, satış siparişi sevk edilirken bu sipariş için tehlikeli malzeme belgeleri hazırlar.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b049559b64045e80a40afd99bac30a9cfe1d0580
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439483"
---
# <a name="set-up-hazardous-materials"></a>Tehlikeli malzemeleri ayarlama

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tehlikeli malzeme işlevlerini kullanmak için önce maddeleri tehlikeli malzeme olarak sınıflandırmak için gerekli verileri ayarlamanız gerekir. Ardından, tehlikeli malzeme olarak sınıflandırılmış bir madde içeren bir satış siparişi oluşturduğunuzda sistem, satış siparişi sevk edilirken bu sipariş için tehlikeli malzeme belgeleri hazırlar.

## <a name="turn-on-the-hazardous-materials-feature-for-your-system"></a>Sisteminiz için tehlikeli malzeme özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ürün bilgileri yönetimi*
- **Özellik adı:** *Tehlikeli malzeme ürün bilgileri ve sevkiyat belgeleri*

## <a name="hazardous-material-regulations"></a>Tehlikeli malzeme yönetmelikleri

Tehlikeli malzeme işlemlerini kullanmak için önce bir yönetmelik oluşturmanız gerekir. Yönetmelikler, maddenin yazılı sevkiyat metninin nasıl oluşturulacağını tanımlar. Yönetmelikler, ilişkili teslimat şekillerini de belirler.

Bazı ortak yönetmelikler şunlardır:

- **ADR** – Tehlikeli malların uluslararası karayollarında taşınmasıyla ilgili düzenlemeler
- **CFR 49** – ABD'de tehlikeli malların taşınmasına yönelik düzenlemeler
- **IMDG** – Uluslararası Denizcilik Tehlikeli Maddeler (IMDG) kodu
- **IATA** – Uluslararası Hava Taşımacılığı Birliği (IATA) tehlikeli mal düzenlemeleri

Bu yönetmelikler, bir maddenin sevkiyat metnini yazdırdığınızda gösterilmesi gereken bilgileri belirlemeye yardımcı olur. Uymanız gereken sayıda yönetmelik tanımlayabilirsiniz.

> [!IMPORTANT]
> Tehlikeli malzemelerle ilgili bilgi kodları ayarlama işlevi şirketinizi yönetmeliklerle uyumlu hale getirmez. Bu, yalnızca şirketiniz için süreçleri oluşturmanıza yardımcı olan bir araçtır.

Genellikle, belirli bir taşıma şekli (ör. deniz yolu, kara yolu veya hava yolu) için bir yönetmelik mevcuttur. Bu nedenle, her yönetmelikle bir teslimat şeklini ilişkilendirebilirsiniz. Teslimat şekli, Ambar yönetiminde belirli belgeler yazdırılırken kullanılır. Ambar yönetiminde, her sevkiyat **Taşıma** modülünde ayarlanan bir sevkiyat taşıyıcısı ve taşıyıcı hizmet ile bağlantılıdır. Teslimat şekli, sevkiyat taşıyıcısı ve taşıyıcı hizmetiyle ilişkilidir. Bir rapor çalıştırdığınızda serbest bırakılmış maddeyle ilişkili sevkiyat yazılı metnini bulmak için teslimat şekli kullanılır.

Bu ayar verileri, tüzel kişiliklere (şirketler) özgü değildir. Bu nedenle, tüm tüzel kişilikleriniz arasında paylaşılan ortak tehlikeli malzeme bilgileri kümesine sahip olabilirsiniz.

Her yönetmelik için, bir malzeme listesi tanımlayıp bunu serbest bırakılan maddelerle ilişkili bir şablon listesi olarak kullanabilirsiniz. Her yönetmelik için, bir yazdırma ayarı da tanımlayabilirsiniz. Yazdırma ayarı, maddenin sevkiyat metninin nasıl oluşturulduğunu tanımlamanızı sağlar. Yazdırma ayarı, serbest bırakılan bir madde için sevkiyat yazılı metnini oluşturmak amacıyla kullanılır.

Tehlikeli malzeme yönetmeliklerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme yönetmeliği**'ne gidin. **Tehlikeli malzeme yönetmeliği** sayfasında, istediğiniz sayıda yönetmelik oluşturup her birini aşağıdaki alt bölümlerde açıklanan alanları kullanarak yapılandırabilirsiniz.

### <a name="hazardous-material-regulation-header"></a>Tehlikeli malzeme yönetmeliği üst bilgisi

Her yönetmeliğin kodu ve açıklaması vardır. Aşağıdaki tabloda, üst bilgide kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Düzenleme kodu | Tehlikeli malzeme düzenleme kaydını tanımlayacak kodu girin. |
| Tanım | Tehlikeli malzeme yönetmeliği açıklamasını girin. |

### <a name="print-setup-fasttab"></a>Yazdırma ayarı hızlı sekmesi

Her yönetmelikte istediğiniz sayıda yazdırma ayarı olabilir. Yazdırma ayarları, **Yazdırma ayarı** hızlı sekmesinde tanımlanır. Aşağıdaki tabloda, her yazdırma ayarında kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Seri | Sevkiyat metninde alanlara başvuru yapılacak sırayı tanımlayın. |
| Alanı yazdır | Sevkiyat metnine dahil edilecek alanı seçin. Tehlikeli malzemeyle ilgili tüm alanlar yazdırma için kullanılabilir değildir. Yalnızca çeşitli yönetmeliklerdeki sevkiyat metinlerini tanımlamak için kullanılan ortak alanlar kullanılabilir. İlk yazdırma alanını alan *0* (sıfır) **Sıra** değerine sahip bir alan ayırıcı olarak tanımlamanız gerekir. Böylece diğer alanlar arasında ayırıcı olarak kullanılabilir. Alan ayırıcı için yalnızca bir başvuru gereklidir.<p>Aşağıdaki değerler kullanılabilir:</p><ul></li><li>**Alan ayırıcısı**: Bu yazdırma alanı metin için alan ayırıcısı olarak kullanılır. Sırada yalnızca bir alan ayırıcı gereklidir. Genellikle bu yazdırma alanının **Sıra** değerini *0* (sıfır) olarak belirlemeniz gerekir. Sistem bir alan ayırıcısı arayıp listede bulduğu ilk ayırıcıyı kullanır. Dizede kullanılan metin değeri, **Yazdırmaya başla** alanından gelir.</li><li>**Kimlik**: Bu yazdırma alanı, yazılı metne [kimlik kodunu ve/veya açıklamasını](#identification) yerleştirir.</li><li>**Sınıf**: Bu yazdırma alanı, yazılı metne [sınıf kodunu ve/veya açıklamasını](#classes) yerleştirir.</li><li>**Bölüm**: Bu yazdırma alanı, yazılı metne [bölüm kodunu ve/veya açıklamasını](#divisions) yerleştirir.</li><li>**Ambalaj grubu**: Bu yazdırma alanı, yazılı metne [ambalaj grubu kodunu ve/veya açıklamasını](#packing-group) yerleştirir.</li><li>**Tünel kodu ve/veya açıklaması**: Bu yazdırma alanı, yazılı metne [tünel kodunu ve/veya açıklamasını](#tunnel) yerleştirir.</li><li>**Uygun sevkiyat adı**: Bu yazdırma alanı, yazılı metne [uygun sevkiyat adını](hazmat-items.md#hazmat-description) yerleştirir.</li><li>**Teknik ad**: Bu yazdırma alanı, yazılı metne [teknik adı ve/veya açıklamasını](#technical-name) yerleştirir.</li><li>**Taşıma kategorisi**: Bu yazdırma alanı, yazılı metne [taşıma kategorisini ve/veya açıklamasını](#transport-category) yerleştirir.</li><li>**İstifleme**: Bu yazdırma alanı, yazılı metne [istifleme kodunu ve/veya açıklamasını](#stowage) yerleştirir.</li><li>**Sabit metin**: Bu yazdırma alanına, bu sıra için **Sabit metin** alanında tanımlanan metin girilir.</li><li>**Etiket kodu ve/veya açıklaması**: Bu yazdırma alanı, yazılı metne [etiket kodunu ve/veya açıklamasını](#label) yerleştirir.</li><li>**Hava taşıtı ambalajı**: Bu yazdırma alanı, yazılı metne [hava taşıtı ambalaj talimatları kodunu ve/veya açıklamasını](#packing-instruction) yerleştirir.</li><li>**Sınırlı miktar:** Bu yazdırma alanı, maddenin [sınırlı miktar uygulanan madde](hazmat-items.md#material-management) olarak işaretlenip işaretlenmediğini denetler ve işaretlenmişse bu satır için **Sabit metin** alanında tanımlanan metni girer.</li><li>**Ambalaj açıklaması**: Bu yazdırma alanı, yazılı metne [ambalaj açıklamasını](#packing-description) yerleştirir.</li></ul> |
| Önce yazdır | **Yazdırma alanı** ayarı tarafından tanımlanan içerikten önce yazdırılması gereken metni girin. |
| Sonra yazdır | **Yazdırma alanı** ayarı tarafından tanımlanan içerikten sonra yazdırılması gereken metni girin. |
| Öncekiyle yazdır | Alan ayırıcının önceki alanla bu alan arasında yazdırılmasını önlemek için bu onay kutusunu seçin. İsteğe bağlı veya başka bir yazdırma alanına dahil olan yazdırma alanları için bu onay kutusunu kullanın. |
| Sabit metin | **Yazdırma alanı** alanını **Sabit metin** veya **Sınırlı miktar** olarak ayarlarsanız yazdırılması gereken metni girin. |
| Yazdırmaya dahil et | Bu satır için seçili yazdırma alanındaki hangi değer veya değerlerin yazdırılacağını seçin. Kodu, açıklamayı veya hem kodu hem de açıklamayı yazdırabilirsiniz. |

### <a name="mode-of-delivery-fasttab"></a>Teslimat şekli hızlı sekmesi

Yönetmelik, ortak bir tablodur ve tüzel kişiliğe özgü değildir. Ancak, teslimat şekilleri tüzel kişiliğe özgüdür. Bu nedenle, bir teslimat şekli ayarladığınızda yönetmelik, tüzel kişilik ve teslimat şekli arasındaki ilişkiyi seçmeniz gerekir.

Aşağıdaki tabloda, **Teslimat şekli** hızlı sekmesinde kullanılabilecek alanlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Şirket | Bu yönetmelikle ilişkilendirilecek tüzel kişiliği seçin. |
| Teslimat şekli | Seçtiğiniz tüzel kişiliğe bağlı olarak, yönetmelikle ilişkilendirilmesi gereken teslimat şeklini seçin. |

### <a name="country-fasttab"></a>Ülke hızlı sekmesi

Başvuru amacıyla, yönetmeliğin geçerli olduğu ülkeleri veya bölgeleri listeleyebilirsiniz. Ancak, sevkiyat raporları çalıştırıldığında yönetmeliği belirlemek için yalnızca teslimat şekli kullanılır. Ambar sevkiyatını incelediğinizde teslimat şekline doğrudan bağlantı olmaz. Sevkiyat, sevkiyat taşıyıcısı ve taşıyıcı hizmetiyle ilişkilendirilebilir. Taşıyıcı hizmeti tanımladığınızda, bunu bir teslimat şekliyle ilişkilendirmeniz gerekir. Bu ilişki, konşimento gibi sevkiyat raporlarında maddeyle ilgili sevkiyat yazılı metnini bulmak için kullanılır.

Aşağıdaki tabloda, **Ülke** hızlı sekmesinde kullanılabilecek alan açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Ülke/bölge | Yönetmelikle ilişkilendirilecek bir ülke/bölge seçin. |

## <a name="material-codes"></a><a name="hazmat-codes"></a>Malzeme kodları

Malzeme kodları, serbest bırakılan ürüne dahil edilmiş olabilecek belirli bir tehlikeli bileşenle ilgili ayarları belirler. Her malzeme kodu, belirli bir tehlikeli malzeme yönetmeliğine aittir ve tanımı söz konusu yönetmelikle uyumlu olmalıdır. Serbest bırakılan bir ürüne **Malzeme kodu** alanını kullanarak malzeme kodu uyguladığınızda, malzeme kodunun tüm tehlikeli malzeme ayarları otomatik olarak söz konusu ürüne uygulanır. Bu sayede, serbest bırakılan ürünleri ayarlama işlemi hızlanır ve hata ihtimali azalır.

Tehlikeli malzeme tanımlarınızı yönetmek için aşağıdaki adımları izleyin.

1. **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme yönetmeliği**'ne gidin.
2. Tehlikeli malzeme tanımını ayarlamak istediğiniz yönetmeliği seçin.
3. Eylem Bölmesindeki **Ayar** sekmesinde, **Tehlikeli malzemeler**'i seçin.
4. **Malzeme kodu** alanına, tehlikeli malzeme tanımı için bir malzeme kodu girin. Malzeme kodunu serbest bırakılan bir ürüne uyguladığınızda bu değeri seçersiniz.

    **Yönetmelik kodu** alanı salt okunurdur ve 2. adımda seçtiğiniz yönetmeliği gösterir.

5. Seçtiğiniz yönetmelik için geçerli olan her bir tehlikeli malzemeyi oluşturmak ve ayarlamak için bu sayfadaki kalan alanları kullanın. Kullanılabilir alanlar, bağımsız serbest bırakılan ürünler için kullanılabilen tehlikeli malzeme alanlarının bir alt kümesidir. Daha fazla bilgi için bkz. [Ürün, sipariş, sevkiyat ve yüklerdeki tehlikeli malzemeler](hazmat-items.md)

## <a name="hazardous-material-classification-groups"></a><a name="classification-groups"></a>Tehlikeli malzeme sınıflandırma grupları

Her tehlikeli malzeme sınıflandırma grubu, bir şablon oluşturan alan değerleri grubunu tanımlar. Daha sonra bu şablonu, serbest bırakılan bir ürün için tehlikeli malzeme bilgilerini ayarlarken kullanabilirsiniz.

Tehlikeli malzeme sınıflandırma grubunun kodunu serbest bırakılan bir maddeye atadığınızda, bu sınıflandırma grubuyla ilişkili bilgiler maddenin uygun alanlarına kopyalanır. Bu sayede, genellikle birlikte kullandığınız bir dizi ilgili alan değeri oluşturarak ayarlama işlemlerini basitleştirebilirsiniz.

Bu ayar verileri, tüzel kişiliğe özgü değildir. Bu nedenle, tüm tüzel kişilikleriniz arasında paylaşılan ortak tehlikeli malzeme bilgileri kümesine sahip olabilirsiniz.

Tehlikeli malzeme sınıflandırma grupları ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme sınıflandırma grubu**'na gidin. **Tehlikeli malzeme sınıflandırma grubu** sayfasında, istediğiniz sayıda grup oluşturup her birini aşağıdaki tabloda açıklanan alanları kullanarak yapılandırabilirsiniz.

| Alan | Tanım |
|---|---|
| Grup kodu | Grubu tanımlamak için bir kod girin. |
| Tanım | Grubun açıklamasını girin. |
| Sınıf kodu | Grup ile tehlikeli malzeme [sınıf kodunu](#classes) ilişkilendirin. |
| Bölüm kodu | Grup ile tehlikeli malzeme [bölüm kodunu](#divisions) ilişkilendirin. |
| Paketleme grubu kodu | Grup ile [ambalaj grubu kodunu](#packing-group) ilişkilendirin. |
| Taşıma kategorisi kodu | Grup ile [taşıma kategorisi kodunu](#transport-category) ilişkilendirin. |
| Çarpan | Geçerli yönetmeliklere göre, seçili tehlikeli malzeme sınıfı ve bölümü için geçerli olan tehlikeli malzeme çarpanını girin. Bu çarpan, yüke veya sevkiyata dahil edilen toplam *tehlikeli malzeme puanını* hesaplayan formülün içinde kullanılır. Tehlikeli malzeme puanları ve bu çarpan ile ilgili daha fazla bilgi için bkz. [Malzeme yönetimi hızlı sekmesi](hazmat-items.md#material-management). |

## <a name="hazardous-material-classes"></a><a name="classes"></a>Tehlikeli malzeme sınıfları

Tehlikeli malzeme sınıfı, genellikle uyduğunuz yönetmelikte sağlanan sınıf listesiyle eşleştirilir. Örneğin, CFR 49 ABD yönetmeliği "3. sınıfı" alev alabilen ve yanabilen sıvılar" olarak listeler. Sınıflamanız gereken malzemelerle ilgili sınıfları ayarlayabilirsiniz.

Her sınıf, yönetmelikle ilgili malzeme listesindeki bir malzeme ayarına atanır. Ürünün tehlikeli yapısını açıklamak için serbest bırakılan her maddeye gereken şekilde sınıf atarsınız.

Bu ayar verileri, tüzel kişiliğe özgü değildir. Bu nedenle, tüm tüzel kişilikleriniz arasında paylaşılan ortak tehlikeli malzeme bilgileri kümesine sahip olabilirsiniz.

Tehlikeli malzeme sınıfları bölümler, gruplar ve uyumluluk gruplarıyla aşağıdaki şekilde birlikte kullanılır:

- Serbest bırakılan bir maddeye tehlikeli malzeme sınıfı atadığınızda [tehlikeli malzeme bölümü](#divisions) de atamanız gerekir.
- Madde ayarlamayla ilgili kod şablonu oluşturmak için tehlikeli malzeme sınıflarını [tehlikeli malzeme sınıflandırma grupları](#classification-groups) ile birlikte kullanabilirsiniz.
- Hangi tehlikeli malzeme sınıflarının ve bölümlerinin birlikte sevk edilebileceğini belirlemek için [tehlikeli malzeme uyumluluk gruplarını](#compatibility-groups) kullanabilirsiniz.

Tehlikeli malzeme sınıflarını ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme sınıfı**'na gidin. **Tehlikeli malzeme sınıfı** sayfasında, istediğiniz sayıda sınıf oluşturup her birini aşağıdaki tabloda açıklanan alanları kullanarak yapılandırabilirsiniz.

| Alan | Tanım |
|---|---|
| Sınıf kodu | Bu sınıfı tanımlamak için bir kod girin. Bu kodu madde için tanımlarsınız. Böylece, serbest bırakılan maddeye tehlikeli malzeme sınıfı atadığınızda bu sınıf arama listelerinde kullanılır. |
| Tanım | Sınıfın açıklamasını girin. |

## <a name="hazardous-material-divisions"></a><a name="divisions"></a>Tehlikeli malzeme bölümleri

Tehlikeli malzeme bölümü, tehlikeli malzeme sınıfının bir alt kümesidir. Tehlikeli malzeme içeren tüm ürünlere hem bölüm hem de sınıf atamanız gerekir.

Bölümü olmayan sınıflar için kodu *0* olan bir bölüm oluşturun. Örneğin, IATA yönetmeliği 7. sınıf radyoaktif malzemelerin alt bölümü yoktur. Bu sayede, sınıfı atadığınızda serbest bırakılan ürünle ilişkilendirebileceğiniz bir *0* bölmesi oluşturmuş olursunuz.

Bu ayar verileri, tüzel kişiliğe özgü değildir. Bu nedenle, tüm tüzel kişilikleriniz arasında paylaşılan ortak tehlikeli malzeme bilgileri kümesine sahip olabilirsiniz.

Tehlikeli malzeme bölümleri sınıflar, gruplar ve uyumluluk gruplarıyla aşağıdaki şekillerde birlikte kullanılır:

- Serbest bırakılan maddeye tehlikeli malzeme bölümü atadığınızda [tehlikeli malzeme sınıfı](#classes) da atamanız gerekir.
- Madde ayarlamayla ilgili kod şablonu oluşturmak için tehlikeli malzeme bölümlerini [tehlikeli malzeme sınıflandırma grupları](#classification-groups) ile birlikte kullanabilirsiniz.
- Hangi tehlikeli malzeme sınıflarının ve bölümlerinin birlikte sevk edilebileceğini belirlemek için [tehlikeli malzeme uyumluluk gruplarını](#compatibility-groups) kullanabilirsiniz.

Tehlikeli malzeme bölümlerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme bölümü**'ne gidin. **Tehlikeli malzeme bölümü** sayfasında, istediğiniz sayıda bölüm oluşturup her birini aşağıdaki tabloda açıklanan alanları kullanarak yapılandırabilirsiniz.

| Alan | Tanım |
|---|---|
| Bölüm | Bölüm için başvuru numarası olarak kullanılacak bir kod girin. |
| Tanım | Bölümün açıklamasını girin. |
| Sınıf | Bölümün ait olduğu sınıfı arayıp atayın. |

## <a name="hazardous-material-compatibility-groups"></a><a name="compatibility-groups"></a>Tehlikeli malzeme uyumluluk grupları

Hangi tehlikeli malzeme sınıflarının ve bölümlerinin birlikte sevk edilebileceğini belirlemek için tehlikeli malzeme uyumluluk gruplarını kullanabilirsiniz. Operatörler ambar yükü veya sevkiyat oluştururken uyumluluk denetimi gerçekleştirebilir. Yükte veya sevkiyatta aynı uyumluluk grubuna ait olmayan maddeler varsa uyarı verilir.

Bu ayar verileri, tüzel kişiliğe özgü değildir. Bu nedenle, tüm tüzel kişilikleriniz arasında paylaşılan ortak tehlikeli malzeme bilgileri kümesine sahip olabilirsiniz.

Tehlikeli malzeme uyumluluk grupları ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme uyumluluk grubu**'na gidin. **Tehlikeli malzeme uyumluluk grubu** sayfasında, istediğiniz sayıda uyumluluk grubu oluşturup her birini aşağıdaki alt bölümlerde açıklanan alanları kullanarak yapılandırabilirsiniz.

### <a name="hazardous-material-compatibility-group-header"></a>Tehlikeli malzeme uyumluluk grubu üst bilgisi

Her uyumluluk grubunun bir kodu ve açıklaması vardır. Aşağıdaki tabloda, üst bilgide kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Uyumluluk grubu | Uyumluluk grubunu tanımlamak için bir kod girin |
| Tanım | Uyumluluk grubunun açıklamasını girin. |

### <a name="compatibility-group-details"></a>Uyumluluk grubu ayrıntıları

Her uyumluluk grubu, birlikte sevk edilebilecek tehlikeli malzeme sınıflarının ve bölümlerinin listesini oluşturur.

| Alan | Tanım |
|---|---|
| Sınıf | Gruptaki diğer tüm sınıflarla uyumlu bir tehlikeli bir malzeme sınıfı seçin. |
| Bölüm | Seçili sınıfa ait bir tehlikeli malzeme bölümü seçin. |

## <a name="hazardous-material-specification-values"></a>Tehlikeli malzeme belirtim değerleri

Microsoft Dynamics 365 Supply Chain Management, çeşitli tehlikeli malzeme belirtim türleri sunar. Her türde, her bir ilgili alan için merkezi değer kümesini belirlemeniz gerekir. Kullanıcılar, tehlikeli malzeme tanımlarını veya serbest bırakılan ürünleri yapılandırırken bu değerler arasından seçim yapabilir. Supply Chain Management, değerleri oluşturabileceğiniz sayfa koleksiyonunu sunar. Her sayfa tek bir belirtim türüne ayrılmıştır. Kullanılabilir her belirtimin açıklamasını ve değerleri belirleme hakkındaki bilgileri görmek için aşağıdaki alt bölümleri inceleyin.

Tehlikeli malzeme belirtimlerinin arasında belirli bir malzemenin taşıma sırasında nasıl depolanması gerektiğini belirten _istifleme kodu_ yer alır. Bu bölümdeki bilgileri kullanarak, istifleme kodları için merkezi bir koleksiyon oluşturursunuz. Daha sonra kullanıcılar, serbest bırakılan bir ürün için istifleme kodunu ayarlarken bu koleksiyon, kullanıcılara açılır liste şeklinde gösterilir.

Bu tehlikeli malzeme belirtim değerleri tüzel kişiliklere özgü olmadığından tüm tüzel kişilikleriniz arasında paylaşılan ortak değerler kümesine sahip olabilirsiniz.

Her belirtim için, belirli bir yönetmelikte belirtilen şekliyle ortak ayarlar koleksiyonu oluştururken [malzeme kodlarını](#hazmat-codes) kullanırsınız. Ardından uygun kodu, gerektiği şekilde serbest bırakılan her bir ürüne uygulayabilirsiniz. Serbest bırakılan belirli bir ürüne tehlikeli malzeme kodunu uygulama ve burada açıklanan belirtimler için söz konusu ürünün tekil ayarlarını yapılandırma hakkında daha fazla bilgi edinmek isterseniz [Ürün, sipariş, sevkiyat ve yüklerdeki tehlikeli malzemeler](hazmat-items.md) konusuna bakın.

### <a name="hazardous-material-emergency-response"></a>Tehlikeli madde acil durum yanıtı

*Tehlikeli malzeme acil durum yanıtı* belirtimi, belirli bir tehlikeli malzeme içeren bir ürün taşınırken bir sorun yaşanırsa yapılması gerekenleri belirtir.

Bu belirtimin değerlerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme acil durum yanıtı**'na gidin. **Tehlikeli malzeme acil durum yanıtı** sayfasında istediğiniz sayıda değer oluşturabilir ve her birini sınıflandırma kodu ve kısa açıklama ile yapılandırabilirsiniz.

### <a name="hazardous-material-identification"></a><a name="identification"></a>Tehlikeli madde tanımlayıcısı

*Tehlikeli malzeme kimliği* belirtimi, tehlikeli malzemenin sınıfını ve yapısını tanımlar. Bu değer, genellikle Birleşmiş Milletler (BM) standardına dayalı bir koddur. Her sınıf, bir kod ve açıklama ile tanımlanır ve taşıma yöntemleri için limit belirleyebilir. Örneğin, yanıcı bir maddeyi veya malzemeyi tanımlamak için *FL* kodunu ve *Yanıcı* açıklamasını kullanan bir tehlikeli malzeme sınıfı oluşturursunuz. Ayrıca bu sınıftakilerin hava yoluyla taşınmaması gerektiğini belirtirsiniz.

Bu belirtimin değerlerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme kimliği**'ne gidin. **Tehlikeli malzeme kimliği** sayfasında, istediğiniz sayıda değer oluşturup her birini aşağıdaki tabloda açıklanan alanları kullanarak yapılandırabilirsiniz.

| Alan | Tanım |
|---|---|
| Kimlik | Bu tehlikeli malzeme sınıfını tanımlayan başvuru numarası olarak kullanılacak bir kod girin. |
| Tanım | Bu sınıfın açıklamasını girin. |
| Hava nakliyesini kısıtla | Bu tehlikeli malzeme sınıfının hava yoluyla taşınamayacağını belirtmek için bu onay kutusunu seçin. |
| Deniz nakliyesini kısıtla | Bu tehlikeli malzeme sınıfının deniz yoluyla taşınamayacağını belirtmek için bu onay kutusunu seçin. |

### <a name="hazardous-material-label"></a><a name="label"></a>Tehlikeli madde etiketi

*Tehlikeli malzeme etiketi* belirtimi, ilgili serbest bırakılan ürünlere uygulanması gereken tehlikeli mallar etiketini tanımlar. Etiketler, ürüne nasıl işlem yapılması gerektiğini açıklar. Örneğin, zehirli gaz içeren bir ürününüz olduğunu düşünelim. Bu durumda, zehirli gaz etiketini temsil eden bir etiket kodu oluşturursunuz. Ayrıca iş sürecinizi, ürünleri sevk ederken bu değeri arayacak şekilde oluşturursunuz.

Bu belirtimin değerlerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme etiketi**'ne gidin. **Tehlikeli malzeme etiketi** sayfasında istediğiniz sayıda etiket oluşturabilir ve her birini tanımlama kodu ve kısa açıklama ile yapılandırabilirsiniz.

### <a name="hazardous-material-packing-descriptions"></a><a name="packing-description"></a>Tehlikeli madde paketleme açıklaması

*Tehlikeli malzeme ambalaj açıklamaları* belirtimi, tehlikeli bir maddenin nasıl ambalajlanması gerektiğini gösterir. Örneğin, belirli bir çelik varille veya başka tür özel ambalajlarla ambalajlanması gerekebilir.

Bu belirtimin değerlerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme ambalaj açıklamaları**'na gidin. **Tehlikeli malzeme ambalaj açıklamaları** sayfasında istediğiniz sayıda ambalaj açıklaması oluşturabilir ve her birini tanımlama kodu ve kısa açıklama ile yapılandırabilirsiniz.

### <a name="hazardous-material-packing-group"></a><a name="packing-group"></a>Tehlikeli madde paketleme grubu

*Tehlikeli malzeme ambalaj grubu* belirtimi, tehlikeli maddenin ambalaj grubunu tanımlar. Ambalaj grubu, taşıma veya sevkiyat sırasında tehlikeli malzeme içeren maddelerin nasıl ambalajlanması gerektiğini belirtmek için bir kod ve açıklama tanımlamanızı sağlar. Ambalaj grubu maddeye **Madde tehlikeli malzemeleri** sayfası üzerinden atanır.

Bu belirtimin değerlerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme ambalaj grubu**'na gidin. **Tehlikeli malzeme ambalaj grubu** sayfasında istediğiniz sayıda ambalaj grubu oluşturabilir ve her birini tanımlama kodu ve kısa açıklama ile yapılandırabilirsiniz.

### <a name="hazardous-material-packing-instruction"></a><a name="packing-instruction"></a>Tehlikeli madde paketleme talimatı

*Tehlikeli malzeme ambalaj talimatı* belirtimi, belirli bir tehlikeli maddenin hava yoluyla taşınmaya hazırlandığı sırada uyulması gereken ambalaj talimatlarını tanımlar.

Bu belirtimin değerlerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme ambalaj talimatları**'na gidin. **Tehlikeli malzeme ambalaj talimatları** sayfasında istediğiniz sayıda ambalaj talimatı tanımlayıcı oluşturabilir ve her birini tanımlama kodu ve kısa açıklama ile yapılandırabilirsiniz.

### <a name="hazardous-material-stowage"></a><a name="stowage"></a>Tehlikeli madde istiflemesi

*Tehlikeli malzeme istiflemesi* belirtimi, ürünün deniz yoluyla taşınması durumunda gemide nasıl depolanması gerektiğini belirtir.

Bu belirtimin değerlerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme istiflemesi**'ne gidin. **Tehlikeli malzeme istifleme** sayfasında istediğiniz sayıda istifleme tanımlayıcısı oluşturabilir ve her birini tanımlama kodu ve kısa açıklama ile yapılandırabilirsiniz.

### <a name="hazardous-material-transport-category"></a><a name="transport-category"></a>Tehlikeli madde taşıma kategorisi

*Tehlikeli malzeme taşıma kategorisi* genel olarak raporlardaki benzer tehlikeli ürünleri gruplamak için kullanılır. Örneğin, taşıma kategorileri ambar sevkiyat kaydından yazdırabileceğiniz **Sevkiyat özeti** raporunda kullanılır.

Bu belirtimin değerlerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme taşıma kategorisi**'ne gidin. **Tehlikeli malzeme taşıma kategorisi** sayfasında istediğiniz sayıda taşıma kategorisi oluşturabilir ve her birini görünen ad ve kısa açıklama ile yapılandırabilirsiniz.

### <a name="hazardous-material-technical-name"></a><a name="technical-name"></a>Tehlikeli madde teknik adı

*Tehlikeli malzeme teknik adı* belirtimi, her bir malzemeyi açıklamak için yaygın olarak veya şirket içinde kullanılan adı belirtmek için kullanılabilir.

Bu belirtimin değerlerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme teknik adı**'na gidin. **Tehlikeli malzeme teknik adı** sayfasında istediğiniz sayıda teknik ad oluşturabilir ve her birini görünen ad ve kısa açıklama ile yapılandırabilirsiniz.

### <a name="hazardous-material-tunnel"></a><a name="tunnel"></a>Tehlikeli madde tüneli

*Tehlikeli malzeme tüneli* belirtimi, kullanılması gereken tünel türlerini tanımlayarak tehlikeli malzemenin taşınabileceği tünel türlerini sınırlar. Tünel kategorileri, tehlikeli taşıma için uygun yönetmelikler tarafından belirlenir. Bu belirtim genellikle yalnızca kara yoluyla taşıma için geçerlidir.

Bu belirtimin değerlerini ayarlamak için **Ürün bilgileri yönetimi \> Ayar \> Tehlikeli malzeme sevkiyat belgeleri \> Tehlikeli malzeme tüneli**'ine gidin. **Tehlikeli malzeme tüneli** sayfasında istediğiniz sayıda tünel tanımlayıcısı oluşturabilir ve her birini tanımlama kodu ve kısa açıklama ile yapılandırabilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]