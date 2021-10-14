---
title: Ürün hazırlığı
description: Bu konuda, bir ürün için gerekli ana verilerin işlemlerde kullanılmadan önce tamamlandığından emin olmak için hazırlık denetimlerini nasıl kullanabileceğiniz açıklanmaktadır.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4286f72f9aed1b4dd91e7c45203cfab2af43f3c2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571965"
---
# <a name="product-readiness"></a>Ürün hazırlığı

[!include [banner](../includes/banner.md)]

İşlemlerde kullanılmadan önce bir ürün için gerekli tüm ana verilerin belirtildiğinden emin olmaya yardımcı olmak üzere hazırlık denetimlerini kullanabilirsiniz. Hazırlık denetimleri kullanıldığında, bir kullanıcı veya ekip önceden tanımlanmış belirli verileri doğrulamadan sorumlu hale getirilir.

Bir mühendislik ürünü, varyantı veya sürümü için gerekli tüm veriler girildikten ve doğrulandıktan sonra ve tüm hazırlık denetimleri işlendikten sonra **Etkin** onay kutusunu işaretleyebilirsiniz. Ürün, sürüm veya varyant için bir veya birden fazla onay işlenmediyse **Etkin** onay kutusunu işaretlemeyi denediğinizde tüm onayların tamamlanmadığına dair bir istem uyarısı alırsınız.

Yeni mühendislik ürünleri, varyantları ve sürümleri için hazırlık denetimleri oluşturabilirsiniz. Hazırlık denetimlerini standart (mühendislik dışı) ürünlere de uygulayabilirsiniz (ayrıca bkz. [Standart ürünler üzerinde hazırlık denetimleri](#standard-products)). 

Tüm hazırlık denetimleri tamamlanmasa bile standart ürünleri hareketlerde kullanabilirsiniz. Bir ürünün hareketlerde kullanılmasını engellemeniz gerekirse yaşam döngüsü durumunu kullanın. Ürünün hareketlerde kullanılmasını engelleyen bir yaşam döngüsü durumu atayabilir ve ardından tüm hazırlık denetimleri tamamlandıktan sonra gerekli hareketlere izin veren yeni bir yaşam döngüsü durumu atayabilirsiniz.

## <a name="types-of-readiness-checks"></a>Hazırlık denetimi türleri

Üç tür hazırlık denetimi vardır:

- **Sistem denetimi**: Sistem geçerli bir kayıt olup olmadığını doğrular. Örneğin, kayıt etkin bir ürün reçetesi olabilir.
- **El ile denetim**: Kullanıcı, kaydın geçerli olup olmadığını doğrular. Örneğin, hazırlık denetimi varsayılan sipariş ayarlarının doğrulanmasını gerektirebilir. Örneğin ürünün hala tasarlandığı ve bu nedenle stoğa alınmaması gibi bazı durumlarda, varsayılan sipariş ayarları gerekmez. Ancak ürün stokta tutulabileceğinden, aynı türden başka bir ürün için varsayılan sipariş ayarları gerekebilir. Kullanıcı, hazırlık denetiminin gerekli olup olmadığına nasıl doğru karar vereceğini bilmekle yükümlüdür.
- **Denetim listesi**: Kullanıcı bir denetim listesinden gelen bir dizi soruyu yanıtlar ve sistem, yanıtların beklentileri karşılayıp karşılamadığını belirler. Denetim listesi herhangi bir konuda olabilir. Örneğin, pazarlama malzemelerinin veya ürün belgelerinin tamamlanıp tamamlanmadığını belirlemek için kullanılabilir.

<a name="checks-engineering"></a>

## <a name="how-readiness-checks-are-created-for-a-new-engineering-product-variant-or-version"></a>Yeni bir mühendislik ürünü, varyant veya sürüm için hazırlık denetimleri nasıl oluşturulur?

Hazırlık denetimi ilkeleri, serbest bırakılan ürün düzeyinde, serbest bırakılan varyant düzeyine ve mühendislik sürümü düzeyinde uygulanabilir.

Yeni bir *mühendislik ürünü* oluşturduğunuzda, sistem [hazırlık denetimi ilkesinin buna uygulanıp uygulanmayacağını](#assign-policy) belirler. Hazırlık denetimi ilkesi uygulanırsa, aşağıdaki olaylar oluşur:

- Geçerli ilkeye göre ürün için hazırlık denetimleri oluşturulur.
- Mühendislik sürümü, ürünün kullanılmasını engellemek için etkin değil olarak ayarlanır. Ürünün tüm mühendislik sürümleri etkin değil olarak ayarlanır.

Bir ürün için yeni bir *varyant* oluşturulursa sistem hazırlık denetimi ilkesinin bu ürün için geçerli olup olmadığını denetler. (Hazırlık deneitimleri, serbest bırakılmış varyant düzeyinde ve mühendislik sürümü düzeyinde uygulanabilir.) İlke geçerliyse aşağıdaki olaylar gerçekleşir:

- Geçerli ilkeye göre ürün için hazırlık denetimleri oluşturulur.
- Mühendislik sürümü ve varyantı ürünün kullanılmasını engellemek için etkin değil olarak ayarlanır.

Bir ürün için yeni bir mühendislik *sürümü* oluşturulursa sistem hazırlık denetimi ilkesinin bu ürün için geçerli olup olmadığını denetler. (Hazırlık deneitimleri, smühendislik sürümü düzeyinde uygulanabilir.) İlke geçerliyse aşağıdaki olaylar gerçekleşir:

- Geçerli ilkeye göre ürün için hazırlık denetimleri oluşturulur.
- Mühendislik sürümü, ürünün kullanılmasını engellemek için etkin değil olarak ayarlanır.

> [!NOTE]
> Hazırlık denetimlerini standart (mühendislik dışı) ürünlere de uygulayabilirsiniz. Daha fazla bilgi için, bu konunun sonraki bölümlerinde yer alan [Standart ürünler üzerinde hazırlık denetimleri](#standard-products) bölümüne bakın.

## <a name="view-readiness-checks"></a>Hazırlık denetimlerini görüntüleme

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Bir ürün veya ürün sürümü için açık hazırlık denetimlerini görüntüleme

Bir ürün için açık hazırlık denetimlerini bulmak üzere, **Serbest bırakılan ürün ayrıntıları** sayfasını açın. Ardından, Eylem Bölmesi'nde, **Ürün** sekmesindeki **Hazırlık denetimleri** gurubunda **Hazırlık denetimi**'ni seçin.

Bir ürün sürümü için açık hazırlık denetimlerini bulmak üzere, serbest bırakılan bir ürünün **Mühendislik sürümleri** sayfasını açın ve bir sürüm seçin. Ardından, Eylem Bölmesi'nde, **Ürün** sekmesindeki **Denetim listesi** gurubunda **Hazırlık denetimi**'ni seçin.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Size atanmış olan açık hazırlık denetimlerini görüntüleme

Size atanan açık hazırlık denetimlerini görüntülemek için aşağıdaki adımlardan birini izleyin.

- **Mühendislik değişikliği yönetimi \> Ortak \> Ürün hazırlığı \> Açık hazırlık denetimlerim**'e gidin.
- **Ürün bilgileri yönetimi \> Çalışma Alanları \> Ayrık üretim için ürün hazırlığı**'na gidin.

Hazırlık denetiminin kime atandığını belirten kurulum, hazırlık ilkesi için yapılır. Hazırlık denetimleri bir kişiye veya takıma atanabilir. Bir takıma hazırlık denetimi atanmışsa, takımda hazırlık denetimini işlemesi gereken bir kişi vardır.

## <a name="process-open-readiness-checks"></a>Açık hazırlık denetimlerini işleme

### <a name="process-system-and-manual-readiness-checks"></a>Sistemi ve el ile hazırlık denetimlerini işleme

**Hazırlık denetimleri** sayfasını açtıktan sonra, Eylem bölmesindeki **İlgili bilgileri görüntüle**'yi seçerek sistem ve el ile hazırlık denetimlerinin konusunu görüntüleyebilirsiniz. Daha sonra hazırlık denetimi verilerini tamamlayabilir ve/veya doğrulayabilirsiniz. Açık hazırlık denetimleri *Beklemede* **Durum** değerine sahiptir. Bu durum, hazırlık denetiminin yine de işlenmesi gerektiğini gösterir. Bir hazırlık denetimini işlemek için aşağıdaki adımlardan birini uygulayın:

- Eylem Bölmesinde, hazırlık denetimini gözden geçirmek ve tamamlamak için **Denetle/tamamla**'yı seçin. Bitirdikten sonra **Durum** alanı *Geçti* olarak güncelleştirilir.
- Eylem Bölmesinde, zorunlu olmayan bir hazırlık denetimini atlamak istiyorsanız **Atla**'yı seçin. Örneğin, fiyat hesaplamaları için bir hazırlık denetimi ayarladınız. Ancak, ürün hala tasarım aşamasındayken bu denetimi atlamaya karar verdiniz. Bu durumda, **Durum** alanı *Atlandı* olarak güncelleştirilir.

Hazırlık ilkesinin yapılandırmasına bağlı olarak, hazırlık denetimi için **Durum** alanı *Geçti* olarak güncelleştirildiğinde, hazırlık denetimini onaylamak için fazladan bir adım gerekebilir. Bu durumda, hazırlık denetimini tamamlamak için **Onay**'ı seçin. Hazırlık denetimi atlandığında bu onay adımı her zaman zorunludur.

Yeni bir ürün, varyant veya sürüm için tüm açık hazırlık denetimleri gerektiği gibi işlendiğinde ve onaylandığında, madde otomatik olarak etkin hale gelir ve bu nedenle kullanıma hazırdır.

### <a name="process-checklist-readiness-checks"></a>İşleme denetim listesi hazırlık denetimleri

Denetim listesini açmak için **Hazırlık denetimleri** sayfasını açın ve ardından Eylem Bölmesinde **Denetim listesini başlat**'ı seçin. Denetim listesini tamamladığınızda sistem, anketteki ayarlara bağlı olarak hazırlık denetiminin geçip geçmediğini doğrular. Denetim geçerse **Durum** alanı *Geçti* olarak güncelleştirilir. Hazırlık denetimi zorunlu değilse atlayabilirsiniz. Bu durumda, **Durum** alanı *Atlandı* olarak güncelleştirilir.

Hazırlık ilkesinin yapılandırmasına bağlı olarak, hazırlık denetimi için **Durum** alanı *Geçti* olarak güncelleştirildiğinde, hazırlık denetimini onaylamak için fazladan bir adım gerekebilir. Bu durumda, hazırlık denetimini tamamlamak için **Onay**'ı seçin. Hazırlık denetimi atlandığında bu onay adımı her zaman zorunludur.

Yeni bir ürün, varyant veya sürüm için tüm açık hazırlık denetimleri gerektiği gibi işlendiğinde ve onaylandığında, madde otomatik olarak etkin hale gelir ve bu nedenle kullanıma hazırdır.

## <a name="create-and-manage-product-readiness-policies"></a>Ürün hazırlık ilkelerini oluşturma ve yönetme

Bir ürün için geçerli olan hazırlık denetimlerini yönetmek için ürün hazırlık ilkelerini kullanın. Her hazırlık ilkesi bir dizi hazırlık denetimi içerir. Bir mühendislik ürün kategorisine hazırlık ilkesi atandığında, bu mühendislik ürünü kategorisinden oluşturulan tüm ürünler, hazırlık ilkesinde belirtilen hazırlık denetimlerine sahip olur.

Ürün hazırlık ilkeleriyle çalışmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Ürün hazırlık ilkeleri**'ne gidin. Ardından şu adımlardan birini izleyin.

- Yeni ilke oluşturmak için Eylem bölmesinden **Yeni**'yi seçin ve sonra alanları aşağıdaki alt bölümlerde açıklandığı gibi ayarlayın.
- Mevcut ilkeyi düzenlemek için liste bölmesinden ilkeyi seçin ve Eylem bölmesinden **Düzenle**'yi seçin ve sonra alanları aşağıdaki alt kısımlarda açıklandığı gibi ayarlayın.
- Var olan bir ilkeyi silmek için liste bölmesinden seçin, Eylem Bölmesinde **Düzenle**'yi seçin ve ardından **Genel** hızlı sekmesinde **Etkin** seçeneğini *Hayır* olarak ayarlayın. Eylem Bölmesi'nde **Sil**'i seçin.

### <a name="header"></a>Üst bilgi

Ürün hazırlık ilkesinin üst bilgisinde aşağıdaki alanları ayarlayın.

| Alan | Tanım |
|---|---|
| Kuruluş adı | İlke için bir ad girin. |
| Tanım | İlke için açıklama girin. |

### <a name="general-fasttab"></a>Genel FastTab

Ürün hazırlık ilkesinin **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın.

| Alan | Tanım |
|---|---|
| Ürün türü | İlkenin *Madde* veya *Hizmet* türündeki ürünler için geçerli olup olmadığını seçin. Kaydı kaydettikten sonra bu ayarı değiştiremezseniz. |
| Active | Hazırlık ilkelerinizi korumaya yardımcı olmak için bu seçeneği kullanın. Bunu, kullandığınız tüm hazırlık ilkeleri için *Evet* olarak ayarlayın. Kullanılmadığında etkin olmayan bir hazırlık ilkesini işaretlemek için *Hayır* olarak ayarlayın. Mühendislik ürünü kategorisine veya paylaşılan bir ürüne atanan bir hazırlık ilkesini devre dışı bırakamayacağınızı ve yalnızca etkin olmayan serbest bırakma ilkelerini silebileceğinizi unutmayın. |

### <a name="readiness-control-fasttab"></a>Hazırlık denetimi hızlı sekmesi

İlkeye eklemek istediğiniz her hazırlık denetimi türü için **Hazırlık denetimi** hızlı sekmesine bir satır ekleyin. Satırları istediğiniz gibi eklemek ve kaldırmak için hızlı sekme araç çubuğundaki şu düğmeleri kullanın:

- **Denetim ekle**: İlkeye standart bir hazırlık denetimi ekleyin. Bu düğmeyi seçtiğinizde, **Ekle** iletişim kutusu görüntülenir. Burada, kullanılabilir denetimler listesinden seçim yapabilirsiniz.
- **Mevcut anket ekle**: Kılavuza boş bir satır ekleyin. Daha sonra, aşağıdaki tablodaki alanları ayarlayarak mevcut bir anket atayabilirsiniz.
- **Kopyala**: Seçilen satırın bir kopyasını kılavuza ekleyin.
- **Sil**: Seçilen satırı kılavuzdan silin.

Eklediğiniz her satır için aşağıdaki alanları ayarlayın.

| Alan | Tanım |
| --- | --- |
| İşlem alanı | Denetimin ilişkili olduğu alanı seçin. |
| Türü | Denetimin sistem denetimi mi, el ile denetim mi yoksa denetim listesi mi (anket) olduğunu seçin. |
| Kuruluş adı | Denetim bir denetim listesiyse ad girin. Sistem denetimleri ve el ile denetimler için bu alan otomatik olarak ayarlanır. |
| Tanım | Denetim bir denetim listesiyse, bir açıklama girin. Sistem denetimleri ve el ile denetimler için bu alan otomatik olarak ayarlanır ve açıklama, denetimin odak noktasını açıklar. |
| Denetimleri şurada uygula | Satırın, yeni serbest bırakılan bir ürüne, serbest bırakılan varyanta veya serbest bırakılan sürüme yanıt olarak hazırlık denetimleri oluşturup oluşturmayacağını seçin. |
| Şurada yürüt: | Satırın oluşturduğu hazırlık denetimlerinin tüm şirketler için mi yoksa tek bir şirket için mi geçerli olacağını seçin. |
| Şirket | **Şuraya yürüt** alanını *Tek şirket* olarak ayarlarsanız şirketi seçin. |
| Sahip türü | Satırın oluşturduğu hazır denetimlerin bir kişiye mi yoksa bir takıma mı atanması gerektiğini seçin. |
| Sahip | Satırın oluşturduğu hazırlık denetimlerinin atanması gereken kişi veya takımı seçin. |
| Soru formu | Denetim listesi için kullanılması gereken anketi seçin. Denetim listesi, hazırlık denetimin yapıldığı şirketteki yerel bir denetim listesidir. Sistem, denetim listesinin doğru yanıtlanıp yanıtlanmadığını değerlendirebilmelidir. Bu nedenle, doğru yanıtlara dayalı bir değerlendirme yapılacak şekilde denetim listesi ayarlanmalıdır. Anketlerin nasıl oluşturulacağı hakkında daha fazla bilgi için bkz. [Anketleri kullanma](/dynamicsax-2012/appuser-itpro/using-questionnaires) ve ilgili konuları. |
| Otomatik onay | Hazırlık denetimi kayıtları, onay durumunu gösteren bir **Onaylandı** onay kutusu içerir. Atanan kullanıcı bunları tamamladıktan hemen sonra onaylanacak şekilde ayarlanacak denetimler için **Otomatik onay** onay kutusunu seçin. Ek bir adım olarak açık onay gerektirmesi için bu onay kutusunu temizleyin. |
| Zorunlu | Atanan kullanıcı tarafından tamamlanması gereken denetimler için bu onay kutusunu seçin. Zorunlu denetimler atlanamaz. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>Standart ve mühendislik ürünlerine hazırlık politikaları atama

Mühendislik kategorisine dayalı yeni bir ürün oluşturduğunuzda, hem *piyasaya sürülen* bir ürün hem de ilgili bir *paylaşılan ürün* oluşturursunuz. Piyasaya sürülen bir ürün için hazırlık ilkelerinin çözümlenme şekli, *Ürün hazırlık denetimleri* özelliğini açıp çalıştırmadığınıza bağlıdır. (Daha fazla bilgi için, bu konunun sonraki bölümlerinde yer alan [Standart ürünler üzerinde hazırlık denetimleri](#standard-products) bölümüne bakın.)

- Sisteminizde *Ürün hazırlık denetimleri* özelliği *kapalı* olduğunda, hazırlık ilkesi ayarlanır ve yalnızca [mühendislik kategorisi](engineering-versions-product-category.md) kayıtlarında gösterilir. Sistem, piyasaya sürülen bir ürün için hangi ilkenin geçerli olduğunu öğrenmek için, ilgili mühendislik kategorisi için **Ürün hazırlık ilkesi** alanını denetler. İlgili mühendislik kategorisini (paylaşılan ürünü değil) düzenleyerek mevcut bir ürünün hazırlık ilkesini değiştirebilirsiniz.
- *Ürün hazırlık denetimleri* özelliği *açık* olduğunda, **Ürün** sayfasına (paylaşılan ürünlerin ayarlandığı) ve **Serbest bırakılan ürün** sayfasına  (değerin salt okunur olduğu ve ilgili paylaşılan üründen alındığı) bir **Ürün hazırlık ilkesi** alanı ekler. Sistem, ilgili paylaşılan ürünü denetleyerek serbest bırakılmış bir ürün için hazırlık ilkesini bulur. Yeni bir mühendislik ürünü oluşturmak için bir mühendislik kategorisi kullandığınızda, sistem hem paylaşılan bir ürün hem de piyasaya sürülen bir ürün oluşturur ve mühendislik kategorisi için **Ürün hazırlık ilkesi** ayarını yeni paylaşılan ürüne kopyalar. İlgili paylaşılan ürünü (sunulan mühendislik kategorisini değil) düzenleyerek mevcut bir ürünün hazırlık ilkesini değiştirebilirsiniz.

Bir paylaşılan ürüne hazırlık ilkesi atamak için aşağıdaki adımları izleyin.

1. **Ürün bilgileri \> Ürünler \> Ürünler** öğesine gidin.
1. Hazırlık ilkesi atamak istediğiniz ürünü açın veya oluşturun.
1. **Genel** Hızlı Sekmesinde, **Ürün hazırlık ilkesi** alanını ürün için geçerli olması gereken ilkenin adına ayarlayın.

Bir mühendislik kategorisine hazırlık ilkesi atamak için aşağıdaki adımları izleyin.

1. **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik ürünü kategorisi ayrıntıları**'na gidin.
1. Hazırlık ilkesi atamak istediğiniz mühendislik kategorisini açın veya oluşturun.
1. **Ürün hazırlık politikası** Hızlı Sekmesinde, **Ürün hazırlık ilkesi** alanını mühendislik kategorisi için geçerli olması gereken ilkenin adına ayarlayın.

<a name="standard-products"></a>

## <a name="readiness-checks-on-standard-products"></a>Standart ürünlerde hazırlık kontrolleri

Özellik yönetiminde ürün hazırlık denetimleri özelliğini açarak standart (mühendislik dışı) ürünler için *ürün hazırlık denetimlerini* etkinleştirebilirsiniz. Bu özellik, standart ürünleri desteklemek için hazırlık denetimi sisteminde birkaç küçük değişiklik yapar.

### <a name="enable-readiness-checks-on-standard-products"></a>Standart ürünlerde hazırlık kontrollerini etkinleştirin

Sisteminizin standart ürünlerde hazırlık denetimleri yapmasını sağlamak için aşağıdaki adımları izleyin.

- [Mühendislik değişikliği yönetimine genel bakış](product-engineering-overview.md) bölümünde açıklandığı gibi sisteminizde Mühendislik değişikliği yönetimini etkinleştirin.
- *Ürün hazırlık denetimleri* adlı özelliği açmak için [Özellik yönetimini](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanın.

<!-- KFM: This section requires confirmation before publishing

### How readiness checks are created for standard products

When you create a new non-engineering *released product*, the system determines whether a readiness check policy has been set up for the related shared product. If a policy has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

If a new *variant* is created for a product, the system checks whether readiness checks have been set up on the related shared product. If a readiness check has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

For engineering products, readiness checks are created in the same way that they are created when the *Product readiness checks* feature is turned off. For more information, see the [How readiness checks are created for a new engineering product, variant, or version](#checks-engineering) section earlier in this topic.

-->

### <a name="create-readiness-policies-for-standard-products"></a>Standart ürünler için hazırlık ilkeleri oluşturma

Standart ürünler için, mühendislik ürünleri için yaptığınız gibi hazırlık ilkeleri oluşturursunuz. Bu konunun önceki bölümlerindeki bilgilere bakın.

### <a name="assign-readiness-policies-to-standard-products"></a>Standart ürünler için hazırlık ilkeleri atama

Standart bir ürüne hazırlık ilkesi atamak için, ilgili paylaşılan ürünü açın ve **Ürün hazırlık ilkesi** alanını uygulanması gereken ilkenin adına ayarlayın. Daha fazla bilgi için, bu konunun önceki bölümlerinde yer alan [Standart ve mühendislik ürünlerine hazırlık ilkeleri atama](#assign-policy) bölümüne bakın.

### <a name="view-and-process-readiness-checks-on-standard-products"></a>Standart ürünlerde hazırlık kontrollerini görüntüleme ve işleme

Bu özellik açıldığında, standart ürünler için hazırlık denetimlerini tıpkı mühendislik ürünü için yaptığınız gibi görüntüler ve işlersiniz. Bu konunun önceki bölümlerindeki bilgilere bakın.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
