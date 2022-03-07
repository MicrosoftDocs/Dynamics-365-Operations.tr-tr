---
title: Ürün hazır olma durumu
description: Bu konu, bir ürün için gerekli ana verilerin işlemlerde kullanılmadan önce tamamlandığından emin olmak için hazırlık denetimlerini nasıl kullanabileceğinizi açıklar.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 38ceef3d03fae83f7ac509fb05a4cd9603af2465
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266163"
---
# <a name="product-readiness"></a>Ürün hazır olma durumu

[!include [banner](../includes/banner.md)]

İşlemlerde kullanılmadan önce bir ürün için gerekli tüm ana verilerin belirtildiğinden emin olmak için hazırlık denetimlerini kullanabilirsiniz. Hazırlık denetimleri kullanıldığında, bir kullanıcı veya ekip önceden tanımlanmış belirli verileri doğrulamadan sorumlu hale getirilir. Bir ürün için açık hazırlık denetimi varsa, ürün serbest bırakılmaz veya işlemlerde kullanılamaz.

Bir mühendislik ürünü, varyantı veya sürümü için **Etkin** onay kutusu, yalnızca gerekli tüm veriler girildikten ve doğrulandıktan sonra ve tüm hazırlık denetimleri işlendikten sonra kullanılabilir. Bu noktada, ürün, sürüm veya varyant diğer şirketlere serbest bırakılabilir ve işlemlerde kullanılabilir. Yeni ürünler, yeni varyantlar ve yeni mühendislik sürümleri için hazırlık denetimleri oluşturabilirsiniz.

## <a name="types-of-readiness-checks"></a>Hazırlık denetimi türleri

Üç tür hazırlık denetimi vardır:

- **Sistem denetimi**: Sistem geçerli bir kayıt olup olmadığını doğrular. Örneğin, kayıt etkin bir ürün reçetesi olabilir.
- **El ile denetim**: Kullanıcı, kaydın geçerli olup olmadığını doğrular. Örneğin, hazırlık denetimi varsayılan sipariş ayarlarının doğrulanmasını gerektirebilir. Örneğin ürünün hala tasarlandığı ve bu nedenle stoğa alınmaması gibi bazı durumlarda, varsayılan sipariş ayarları gerekmez. Ancak ürün stokta tutulabileceğinden, aynı türden başka bir ürün için varsayılan sipariş ayarları gerekebilir. Kullanıcı, hazırlık denetiminin gerekli olup olmadığına nasıl doğru karar vereceğini bilmekle yükümlüdür.
- **Denetim listesi**: Kullanıcı bir denetim listesinden gelen bir dizi soruyu yanıtlar ve sistem, yanıtların beklentileri karşılayıp karşılamadığını belirler. Denetim listesi herhangi bir konuda olabilir. Örneğin, pazarlama malzemelerinin veya ürün belgelerinin tamamlanıp tamamlanmadığını belirlemek için kullanılabilir.

## <a name="how-readiness-checks-are-created-for-a-new-product-variant-or-version"></a>Yeni bir ürün, varyant veya sürüm için hazırlık denetimleri nasıl oluşturulur?

Yeni bir mühendislik **ürünü** oluşturduğunuzda sistem, mühendislik ürünü kategorisi için bir hazırlık denetimi ilkesinin ayarlanıp ayarlanmadığını belirler. (Hazırlık denetimi ilkeleri, serbest bırakılan ürün düzeyinde, serbest bırakılan varyant düzeyine ve mühendislik sürümü düzeyinde uygulanabilir.) Bir ilke ayarlandıysa aşağıdaki olaylar gerçekleşir:

- Geçerli ilkeye göre ürün için hazırlık denetimleri oluşturulur.
- Mühendislik sürümü, ürünün kullanılmasını engellemek için etkin değil olarak ayarlanır. İlgili ürünün tüm sürümleri etkin değil olarak ayarlanır.

Bir ürün için yeni bir **varyant** oluşturulursa sistem, mühendislik ürünü kategorisinde hazırlık denetimlerinin ayarlanıp ayarlanmadığını denetler. (Hazırlık deneitimleri, serbest bırakılmış varyant düzeyinde ve mühendislik sürümü düzeyinde uygulanabilir.) Hazırlık denetimi ayarlanyısa aşağıdaki olaylar gerçekleşir:

- Ürün için hazırlık denetimleri oluşturulur.
- Mühendislik sürümü, ürünün kullanılmasını engellemek için etkin değil olarak ayarlanır.

Bir ürün için yeni bir mühendislik **sürümü** oluşturulursa sistem, mühendislik ürünü kategorisinde hazırlık denetimlerinin ayarlanıp ayarlanmadığını denetler. (Hazırlık denetimleri mühendislik sürümü düzeyinde uygulanabilir.) Hazırlık denetimi ayarlanyısa aşağıdaki olaylar gerçekleşir:

- Ürün için hazırlık denetimleri oluşturulur.
- Mühendislik sürümü, ürünün kullanılmasını engellemek için etkin değil olarak ayarlanır.

## <a name="view-readiness-checks"></a>Hazırlık denetimlerini görüntüleme

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Bir ürün veya ürün sürümü için açık hazırlık denetimlerini görüntüleme

Bir ürün için açık hazırlık denetimlerini bulmak üzere, **Serbest bırakılan ürün ayrıntıları** sayfasını açın. Ardından, Eylem Bölmesi'nde, **Ürün** sekmesindeki **Hazırlık denetimleri** gurubunda **Hazırlık denetimi**'ni seçin.

Bir ürün sürümü için açık hazırlık denetimlerini bulmak üzere, serbest bırakılan bir ürünün **Mühendislik sürümleri** sayfasını açın ve bir sürüm seçin. Ardından, Eylem Bölmesi'nde, **Ürün** sekmesindeki **Denetim listesi** gurubunda **Hazırlık denetimi**'ni seçin.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Size atanmış olan açık hazırlık denetimlerini görüntüleme

Size atanan açık hazırlık denetimlerini görüntülemek için aşağıdaki adımlardan birini izleyin.

- **Mühendislik değişikliği yönetimi \> Ortak \> Ürün hazırlığı \> Açık hazırlık denetimlerim**'e gidin.
- **Ürün bilgileri yönetimi \> Çalışma Alanları \> Ayrık üretim için ürün hazırlığı**'na gidin.

Hazırlık denetiminin kime atandığını belirten kurulum, mühendislik ürünü kategorisi için yapılır. Hazırlık denetimleri bir kişiye veya takıma atanabilir. Bir takıma hazırlık denetimi atanmışsa, takımda hazırlık denetimini işlemesi gereken bir kişi vardır. Daha fazla bilgi için bkz. [Mühendislik sürümleri ve mühendislik ürünü kategorileri](engineering-versions-product-category.md).

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

Bir ürün için geçerli olan hazırlık denetimlerini yönetmek için ürün hazırlık ilkelerini kullanın. Hazırlık ilkesi mühendislik kategorisine atandığından, hazırlık ilkesindeki tüm denetimler mühendislik kategorisini temel alan tüm mühendislik ürünleri için geçerlidir. Daha fazla bilgi için bkz. [Mühendislik sürümleri ve mühendislik ürünü kategorileri](engineering-versions-product-category.md).

Her hazırlık ilkesi bir dizi hazırlık denetimi içerir. Bir mühendislik ürün kategorisine hazırlık ilkesi atandığında, bu mühendislik ürünü kategorisinden oluşturulan tüm ürünler, hazırlık ilkesinde belirtilen hazırlık denetimlerine sahip olur.

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
| Active | Hazırlık ilkelerinizi korumaya yardımcı olmak için bu seçeneği kullanın. Bunu, kullandığınız tüm hazırlık ilkeleri için *Evet* olarak ayarlayın. Kullanılmadığında etkin olmayan bir hazırlık ilkesini işaretlemek için *Hayır* olarak ayarlayın. Mühendislik ürünü kategorisine atanan bir hazırlık ilkesini devre dışı bırakamayacağınızı ve yalnızca etkin olmayan serbest bırakma ilkelerini silebileceğinizi unutmayın. |

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
| Soru formu | Denetim listesi için kullanılması gereken anketi seçin. Denetim listesi, hazırlık denetimin yapıldığı şirketteki yerel bir denetim listesidir. Sistem, denetim listesinin doğru yanıtlanıp yanıtlanmadığını değerlendirebilmelidir. Bu nedenle, doğru yanıtlara dayalı bir değerlendirme yapılacak şekilde denetim listesi ayarlanmalıdır. Anketlerin nasıl oluşturulacağı hakkında daha fazla bilgi için bkz. [Anketleri kullanma](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/using-questionnaires) ve ilgili konuları. |
| Otomatik onay | Hazırlık denetimi kayıtları, onay durumunu gösteren bir **Onaylandı** onay kutusu içerir. Atanan kullanıcı bunları tamamladıktan hemen sonra onaylanacak şekilde ayarlanacak denetimler için **Otomatik onay** onay kutusunu seçin. Ek bir adım olarak açık onay gerektirmesi için bu onay kutusunu temizleyin. |
| Zorunlu | Atanan kullanıcı tarafından tamamlanması gereken denetimler için bu onay kutusunu seçin. Zorunlu denetimler atlanamaz. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]