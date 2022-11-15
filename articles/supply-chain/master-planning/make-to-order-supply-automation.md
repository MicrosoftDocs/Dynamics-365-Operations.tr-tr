---
title: Özel sipariş tedarik otomasyonu
description: Bu makalede, Siparişe göre tedarik otomasyonu özelliği ile eklenen çeşitli geliştirmelerin nasıl kurulacağı ve kullanılacağı açıklanır.
author: t-benebo
ms.date: 07/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-27
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d376c2f4d8514a4e6122e2e94455d57a39d2babf
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740207"
---
# <a name="make-to-order-supply-automation"></a>Özel sipariş tedarik otomasyonu

[!include [banner](../includes/banner.md)]

*Siparişe göre tedarik otomasyonu* özelliği Microsoft Dynamics 365 Supply Chain Management'a birkaç geliştirme ekler. Bu geliştirmeler şu görevleri gerçekleştirmenizi sağlar:

- Kullanıcı tanımlı bir dönem için kaynak kapasite yükünü görüntüleyin ve böylece kapasite yükünün uzun vadeli değerlendirmesini etkinleştirin.
- Her bir master plan için gecikme toleransını (negatif gün) denetleyerek esnekliği artırın.
- Ürünlerin son dakika verilen siparişler için kullanılabilir kalmasını sağlayın ve ilk olası tedariki kullanmak yerine, en son tarihli tedariki bir taleple ilişkilendirerek varolan tedarikin kullanımını en iyi duruma getirin.
- Sistemin son dakika talep değişikliklerine göre iyileştirme yapabilmesi için, kesinleştirme sonrasında üretim siparişleriyle ilgili bileşen atamalarını esnek tutun. Diğer bir deyişle, işaretlemeyi tek bir düzey ile sınırlayın.
- Her bir satış siparişi için karşılama ilkesini kontrol edin. Varsayılan ayarlar müşteri kurulumundan alınır.
- Şirketlerarası bilgi akışını geliştirin. Satınalma siparişleri; teslimat şekli, teslimat koşulları ve harici madde numarası ile ilgili alanları içerecek şekilde güncelleştirilir. Bu değişiklik ayrıntılı talep bilgilerinin tedarik şirketine akmasını sağlar.

Bu makalede, her geliştirmenin nasıl ayarlanacağı ve kullanılacağı açıklanmaktadır.

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Siparişe göre tedarik otomasyonu özelliğini açma

Bu makalede açıklanan özelliği kullanabilmeniz için, önce özelliği sisteminizde açmanız gerekir. Yöneticiler, özelliğin aşağıdaki şekilde listelendiği [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir:

- **Modül:** *Master Planlama*
- **Özellik adı:** *Siparişe göre tedarik otomasyonu*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Kapasite yükü sayfasında gösterilecek gün sayısını ayarlama

**Kapasite yükü** sayfası, bir kaynağın kullanılabilir kapasitesini gözden geçirmenizi sağlar. *Siparişe göre tedarik otomasyonu* özelliği, **Gün sayısı** alanı ekleyerek **Kapasite yükü** sayfasını geliştirir. **Genel Bakış** kılavuzunun gösterdiği gün sayısını sınırlandırmak için bu alanı kullanabilirsiniz. Ayarladığınız değer bellekte kaydedilir. Bu nedenle, sayfadan ayrılırsanız ve sonra daha sonra tekrar dönerseniz, **Genel Bakış** kılavuzu hala en son belirttiğiniz gün sayısını gösterir.

Belirli bir kaynağın kullanılabilir kapasitesini gözden geçirebilmek amacıyla **Kapasite yükü** sayfasını açmak için, aşağıdaki adımları izleyin.

1. **Kuruluş yönetimi \> Kaynaklar \> Kaynaklar**'a gidin.
1. Denetlenecek bir kaynak seçin.
1. Eylem Bölmesinde **Kaynak** sekmesinde **Görünüm** grubunda **Kapasite yükü** öğesini seçin.
1. **Genel Bakış** kılavuzunun gösterdiği gün sayısını sınırlandırmak için **Gün sayısı** filtresini kullanın.

Bir kaynak grubunun kullanılabilir kapasitesini gözden geçirebilmek amacıyla **Kapasite yükü** sayfasını açmak için, aşağıdaki adımları izleyin.

1. **Kuruluş yönetimi \> Kaynaklar \> Kaynak grupları**'na gidin.
1. Denetlenecek bir kaynak grubu seçin.
1. Eylem Bölmesinde **Kaynak grubu** sekmesinde **Görünüm** grubunda **Kapasite yükü** öğesini seçin.
1. **Genel Bakış** kılavuzunun gösterdiği gün sayısını sınırlandırmak için **Gün sayısı** filtresini kullanın.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Planlı siparişleri kesinleştirirken tek bir işaretleme düzeyi uygulama

*İşaretleme*, arz ve talebi bağlamak için kullanılır. Master planlamanın talebin nasıl olmasını beklediğini gösteren bir *ilişkilendirmeye* benzerdir. Ancak işaretleme, ilişkilendirmeden daha kalıcıdır. *Siparişe göre tedarik otomasyonu* özelliği, planlanan siparişler kesinleştirildiğinde, stok işaretlemesini tek bir düzeye sınırlama yeteneği ekler. Planlı bir sipariş kesinleştirilirken, **Kesinleştirme** iletişim kutusundaki **İşaretlemeyi güncelleştir** alanına aşağıdaki yeni seçenekleri ekler:

- *Tek düzeyli standart* – Tek düzeyli işaretleme kullanılır. Tek düzeyli işaretleme, ürün reçetesi (BOM) bileşenlerini değil yalnızca ana maddeyi işaretler. Bu nedenle, kesinleştirme sonrasında üretime yönelik bileşen atamasını esnek tutabilirsiniz. Tek düzeyli işaretleme, sistemin son dakikada gelen talep değişiklikleri için optimizasyon yapmasına olanak tanır. Tek düzeyli *standart* işaretlemede, gereksinim siparişleri karşılama emirlerine göre işaretlenir, ancak kalan miktarı olan karşılama siparişleri işaretlenmez.
- *Tek düzeyli genişletilmiş* – Tek düzeyli işaretleme kullanılır. Tek düzeyli *genişletilmiş* işaretlemede, gereksinim siparişleri karşılama emirlerine göre işaretlenir ve kalan miktar bulunmasından bağımsız olarak karşılama siparişleri her zaman işaretlenir.

Bu seçeneklere, **Kesinleştirme** iletişim kutusu için varsayılan seçimi tanımladığınız **Master planlama parametreleri** sayfasının **Standart güncelleştirme** sekmesindeki **İşaretlemeyi güncelleştir** alanından da ulaşılabilir.

Daha fazla bilgi için [Stok işaretleme](planning-optimization/marking.md) bölümüne bakın.

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>Master plan düzeyinde gecikme toleransı (negatif günler) ayarlama

*Siparişe göre tedarik otomasyonu* özelliği, master plan düzeyinde gecikme toleransını (negatif günler) yapılandırma yeteneğini ekler. Bu ayar, madde karşılama ve karşılama grubu düzeylerinde de mevcuttur. Negatif günler birden fazla düzeye atanırsa, hangi ayarın kullanılacağının kararını vermek için sistem aşağıdaki hiyerarşiyi uygular:

- **Master planlar** sayfasında negatif günler yapılandırılmışsa bu ayar plan çalıştığı zaman diğer tüm negatif günlerin ayarlarını geçersiz kılar.
- **Madde karşılama** sayfasında negatif günler yapılandırılmışsa bu ayar karşılama grubu ayarını geçersiz kılar.
- **Karşılama grupları** sayfasında yapılandırılan negatif günler yalnızca, ilgili madde veya master plan için negatif günler yapılandırılmamış ise geçerlidir.

Bir master plana ilişkin negatif günleri ayarlamak için aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Liste bölmesindeki master planlardan birini seçin veya yeni bir tane oluşturun.
1. **Gün cinsinden zaman dilimleri** hızlı sekmesinde, **Negatif günler** seçeneğini *Evet* olarak ayarlayın.
1. Yakındaki alanda, izin verilecek negatif gün sayısını girin.

Negatif günlerin nasıl kullanılacağı hakkında daha fazla bilgi için bkz. [Gecikme toleransı (negatif günler)](planning-optimization/delay-tolerance.md).

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>Master planlama sırasında kullanılan ilişkilendirme sırasını kontrol etme

Master planlama, hangi tedarikin hangi talebi kapsadığını belirlemek için bir *ilişkilendirme dizisi* kullanır. *Siparişe göre tedarik otomasyonu* özelliği, size ilişkilendirme sırası üzerinde daha fazla kontrol sağlayan yeni bir **En güncel tedariki kullan** seçeneği ekler. Yeni seçenek, ürünleri son dakika verilen siparişler için kullanılabilir tutmanızı ve ilk olası tedariki kullanmak yerine, en son tarihli tedariki bir taleple ilişkilendirerek varolan tedarikin kullanımını en iyi duruma getirmenizi sağlar.

Master plan, madde karşılama veya kapsam grubu düzeyinde ilişkilendirme sırasını ayarlayabilirsiniz. İlişkilendirme sırası birden fazla düzeyde ayarlanırsa, hangi ayarın kullanılacağının kararını vermek için sistem aşağıdaki hiyerarşiyi uygular:

- **Master planlar** sayfasında bir ilişkilendirme sırası ayarlanmışsa, bu ayar plan çalıştığı sırada diğer tüm diğer ilişkilendirme sırası ayarlarını geçersiz kılar.
- **Madde karşılama** sayfasında ilişkilendirme sırası ayarlanmışsa bu ayar karşılama grubu ayarını geçersiz kılar.
- **Karşılama grupları** sayfasında ayarlanan ilişkilendirme sırası, yalnızca ilgili bir madde veya master plan için ilişkilendirme sırası ayarları yapılandırılmamış ise geçerlidir.

Karşılama grubu düzeyinde bir ilişkilendirme ayarlamak için aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Kapsam \> Kapsam grupları**'na gidin.
1. Liste bölmesindeki gruplardan birini seçin veya yeni bir tane oluşturun.
1. **Genel** hızlı sekmesindeki **İlişkilendirme sırası** bölümünde, **Eldeki stoku tüket** ve **En güncel tedariki kullan** alanlarını kullanarak ilişkilendirme sırasını yapılandırın. Bu bölümün ilerleyen kısımlarında yer alanda tabloda, bu ayarların ilişkilendirme sırasını tanımlamak için nasıl birleştirildiği gösterilmektedir.

Madde karşılama düzeyinde bir ilişkilendirme ayarlamak için aşağıdaki adımları izleyin.

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Kılavuzda bir ürün seçin veya yeni bir tane oluşturun.
1. Eylem Bölmesi'nin **Plan** sekmesinde **Öğe kapsamı**'nı seçin.
1. **Madde karşılama** sayfası, her ambardaki madde için geçerli olan karşılama kurallarını tanımlamanızı sağlayan satırları sunar. Kılavuzdaki mevcut bir satırı seçin veya yeni bir tane oluşturun.
1. **Genel** sekmesinde, **İlişkilendirme sırasını geçersiz kıl** onay kutusunu seçin.
1. İlişkilendirme sıranızı yapılandırmak için **Eldeki stoku tüket** ve **En güncel tedariki kullan** alanlarını kullanın. Bu bölümün ilerleyen kısımlarında yer alanda tabloda, bu ayarların ilişkilendirme sırasını tanımlamak için nasıl birleştirildiği gösterilmektedir.

Master plan düzeyinde bir ilişkilendirme ayarlamak için aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Liste bölmesindeki master planlardan birini seçin veya yeni bir tane oluşturun.
1. **Genel** hızlı sekmesinde, **İlişkilendirme sırasını geçersiz kıl** seçeneğini *Evet* olarak ayarlayın.
1. İlişkilendirme sıranızı yapılandırmak için **Eldeki stoku tüket** ve **En güncel tedariki kullan** alanlarını kullanın. Bu bölümün ilerleyen kısımlarında yer alanda tabloda, bu ayarların ilişkilendirme sırasını tanımlamak için nasıl birleştirildiği gösterilmektedir.

Aşağıdaki tabloda, ilişkilendirme sıranızı oluşturmak için **Eldeki stoku tüket** ve **En güncel tedariki kullan** ayarlarının nasıl birleştirildiği gösterilmektedir.

| | En güncel tedariki kullan = Evet | En güncel tedariki kullan = Hayır |
|---|---|---|
| **Eldeki stoku tüket** = *Tüm diğer tedarikten önce* | <ol><li>Eldeki</li><li>Talep tarihini karşılayabilecek mevcut tedarik</li><li>Talep tarihini karşılayamayacak ancak yine de negatif günler içinde olan mevcut tedarik</li><li>Yeni tedarik oluşturma (planlı sipariş)</li></ol> | <ol><li>Eldeki</li><li>Talep tarihini karşılayabilecek mevcut tedarik</li><li>Talep tarihini karşılayamayacak ancak yine de negatif günler içinde olan mevcut tedarik</li><li>Yeni tedarik oluşturma (planlı sipariş)</li></ol> |
| **Eldeki stoku tüket** = *Tüm diğer tedarikten sonra* | <ol><li>Talep tarihini karşılayabilecek mevcut tedarik</li><li>Eldeki</li><li>Talep tarihini karşılayamayacak ancak yine de negatif günler içinde olan mevcut tedarik</li><li>Yeni tedarik oluşturma (planlı sipariş)</li></ol> | <ol><li>Talep tarihini karşılayabilecek mevcut tedarik</li><li>Talep tarihini karşılayamayacak ancak yine de negatif günler içinde olan mevcut tedarik</li><li>Eldeki</li><li>Yeni tedarik oluşturma (planlı sipariş)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Her satış siparişi için geçerli olan karşılama ilkesini gözden geçirme ve ayarlama

Sipariş karşılama ilkeleri, bir satış siparişini ambara serbest bırakmadan önce fiziksel olarak rezerve edilmesi gereken toplam sipariş fiyatı veya miktarının yüzdesini kontrol eder. Genel bir varsayılan karşılama ilkesi ayarlayabilir ve sonra bunu belirli müşteriler için geçersiz kılabilirsiniz. *Siparişe göre tedarik otomasyonu* özelliği, bir siparişe gerçekte hangi varsayılan ilkenin uygulandığını görüntüleme ve gerektikçe siparişe özel geçersiz kılmalar uygulama yeteneği ekler.

- Satış siparişleri için global olarak karşılama ilkesi varsayılanını ayarlamak üzere, **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin. Ardından, **Ambar Yönetimi** sekmesinde, **Satış siparişi karşılama ilkesi** alanını kullanmak istediğiniz ilkenin adına ayarlayın. 
- Satış siparişleri için müşteriye özel bir karşılama ilkesi ayarlamak üzere, **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin. Ardından, **Ambar** sekmesinde, **Sipariş karşılama ilkesi** alanını kullanmak istediğiniz ilkenin adına ayarlayın.

Herhangi bir sipariş için geçerli olan varsayılan ilkeyi görüntülemek ve siparişe özel bir geçersiz kılma uygulamak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Denetlemek veya düzenlemek istediğiniz satış siparişini açın veya seçin.
1. **Üstbilgi** görünümünü seçin.
1. **Ambar** hızlı sekmesinde, aşağıdaki alanları gerektiği gibi gözden geçirin ve düzenleyin:

    - **Sipariş karşılama ilkesi** – Seçili sipariş için kullanılacak karşılama ilkesini seçin. Varsayılan ilke geçersiz kılınır. **Varsayılan karşılama ilkesi** alanında gösterilen varsayılan karşılama ilkesini kullanmak için bu alanı boş bırakın.
    - **Varsayılan karşılama ilkesi** – Bu alan, **Sipariş karşılama ilkesi** alanı boş olduğunda uygulanan varsayılan karşılama ilkesini gösterir. Bu alan salt okunurdur. Boşsa, müşteriye özel veya genel bir varsayılan karşılama ilkesi tanımlanmamıştır.

    **Sipariş karşılama ilkesi** ve **Varsayılan karşılama ilkesi** alanları boşsa hiçbir karşılama ilkesi uygulanmaz. Ancak, diğer sınırlamalar yürürlükte olabilir ve satış siparişi serbest bırakılmadan önce rezervasyonların veya diğer koşulların karşılanmasını gerektirebilir.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>Tek bir satınalma siparişi satırındaki teslimat modunu ve koşullarını ayarlama

Tüm satınalma siparişlerinin sipariş başlığında, **Teslimat koşulları** ve **Teslimat modu** ayarları bulunur. *Siparişe göre tedarik otomasyonu* özelliği, bu ayarları her sipariş satırına ekler. Bu nedenle, gerektiğinde herhangi bir sipariş satırı veya tüm sipariş satırları için **Teslimat koşulları** ve/veya **Teslimat modu** değerinin geçersiz kılmalarını tanımlayabilirsiniz. Geçersiz kılma tanımlanmamış satırlarda, başlıktan alınan değer kullanılır. Sipariş başlığındaki bu alanlardan bir veya her ikisinin değerinde yapılan bir değişikliğin tüm satırları da güncelleştirip güncelleştirmeyeceğini belirtebilirsiniz.

Bir kullanıcı sipariş başlığındaki **Teslimat koşulları** ve/veya **Teslimat modu** değerini değiştirirse, satır ayarlarına ne olacağını belirtmek için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak atama \> Kurulum \> Tedarik ve kaynak atama parametrelerine** gidin.
1. **Genel** sekmesinde, **Varsayılan değerler ve parametreler** hızlı sekmesinde, **Sipariş satırlarını güncelleştir** bağlantısını seçin.
1. **Sipariş satırlarını güncelleştir** iletişim kutusunda, **Teslimat Koşullarını Güncelleştirme** ve **Teslimat Modunu Güncelleştirme** alanlarında aşağıdaki değerlerden birini seçin:

    - *Asla* – Sipariş başlığındaki ayarlar değiştirildikten sonra sipariş satırlarını asla güncelleştirmez.
    - *Her zaman* – Sipariş başlığındaki ayarlar değiştirildikten sonra tüm sipariş satırlarını güncelleştirir.
    - *İstem* – Kullanıcı sipariş başlığındaki bir veya her iki ayarı da değiştirirse, kullanıcının bir veya her iki ayardaki bu değişiklikle eşleşmesi için tüm satırları güncelleştirmek isteyip istemediğini soran bir iletişim kutusu açar.

Bir satınalma siparişi başlığındaki teslimat bilgilerini ayarlamak için, aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Denetlemek veya düzenlemek istediğiniz satın alma siparişini açın veya seçin.
1. **Üstbilgi** görünümünü seçin.
1. **Teslimat** hızlı sekmesinde, gereken şekilde **Teslimat modu** ve **Teslimat koşulları** alanlarını ayarlayın.
1. **Tedarik ve kaynak atama parametreleri** sayfasındaki ayarlara bağlı olarak, yaptığınız değişiklikleri tüm sipariş satırlarına uygulamak isteyip istemediğiniz sorulur.

Bir satınalma siparişi satırı için teslimat bilgileri geçersiz kılmalarını ayarlamak için, aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Denetlemek veya düzenlemek istediğiniz satın alma siparişini açın veya seçin.
1. **Satırlar** görünümünü seçin.
1. **Satınalma siparişi satırları** hızlı sekmesinde, düzenlenecek satırı seçin.
1. **Satır ayrıntıları** hızlı sekmesindeki **Teslimat** sekmesinde gereken şekilde **Teslimat modu** ve **Teslimat koşulları** alanlarını ayarlayın. Başlıktaki eşleştirme ayarlarını kullanmak için, bir veya her iki alanı temizleyin.

Şirketlerarası siparişler için, her satınalma siparişi satırındaki **Teslimat modu** ve **Teslimat koşulları** alanlarının değerleri satınalma siparişi ve ilgili satış siparişi arasında eşitlenir.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Şirketlerarası siparişler için harici madde kodlarını ve açıklamalarını eşitleme

Şirketlerarası siparişlerde *Siparişe göre tedarik otomasyonu* özelliği, satınalma siparişinin doğrudan teslime yönelik olup olmamasına bakılmaksızın, satınalma siparişi satırlarındaki harici madde kodlarının ve metin açıklamalarının ilgili şirketlerarası satış siparişi satırlarıyla eşitlenmesini sağlar. Özellik ayrıca, şirketlerarası satınalma siparişinde son harici müşteri hesabını belirtme yeteneğini de ekler. Sistem böylece otomatik olarak harici madde kodları ve metin açıklamalarını şirketlerarası satıcı kaydı (dahili) yerine harici müşteri kaydından alır.

Şirketlerarası satınalma siparişleri ve ilgili şirketlerarası satış siparişleri arasında harici madde kodlarını ve madde adlarını eşitlemek üzere bir şirketlerarası satıcı ayarlamak için, aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak \> Satıcılar \> Tüm satıcılar**'a gidin.
1. Ayarlamak istediğiniz şirketlerarası satıcıyı seçin.
1. Eylem Bölmesinde, **Genel** sekmesindeki **Ayarla** gurubunda **Şirketlerarası**'nı seçin.
1. **Şirketlerarası** sayfasının **Satınalma siparişi ilkeleri** sekmesindeki **Şirketlerarası satınalma siparişi -\> Şirketlerarası satış siparişi** bölümünde, **Harici madde kodu ve madde adı** onay kutusunu seçin.

Şirketlerarası satınalma siparişinde son harici müşteri hesabını belirtmek için aşağıdaki adımları izleyin. **Müşteri hesabı** alanı yalnızca şirketlerarası satınalma siparişleri için geçerlidir. Malları alacak olan müşterinin hesap numarasını belirtmek için bunu kullanın. Bu alan ayarlandığında satınalma siparişi satırları, satınalma siparişinde belirtilen şirketlerarası satıcı yerine, belirtilen müşteri hesabındaki harici madde açıklamalarını ve numaralarını alır. Müşteri hesabını daha sonra değiştirirseniz, harici madde açıklamaları ve kodları yeni hesabın değerleriyle eşleşecek şekilde güncelleştirilecektir. Her satırın harici madde açıklamaları ve kodları eşleşen şirketlerarası satış siparişiyle de eşitlenecektir.

1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Ayarlamak istediğiniz satın alma siparişini açın veya yeni bir sipariş oluşturun.
1. **Üstbilgi** görünümünü seçin.
1. **Referans** bölümünde, **Müşteri hesabı** alanını ilgili harici müşteri hesabına ayarlayın.

Bir şirketlerarası siparişin satınalma sipariş satırına yönelik harici madde kodlarını ve metin açıklamalarını belirtmek için, aşağıdaki adımları izleyin. Ayarladığınız değerler, satınalma siparişinin doğrudan teslim edilmeye yönelik olup olmamasından bağımsız olarak, ilgili şirketlerarası satış siparişi satırlarıyla eşitlenir.

1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Ayarlamak istediğiniz satın alma siparişini açın veya yeni bir sipariş oluşturun.
1. **Satırlar** görünümünü seçin.
1. **Satınalma siparişi satırları** hızlı sekmesinde, düzenlenecek satırı seçin.
1. **Satır ayrıntıları** hızlı sekmesindeki **Genel** sekmesinin **Sipariş satırı** bölümünde, **Metin** alanında, seçili sipariş satırında belirtilen maddenin harici açıklamasını girin. Bu değer ilgili şirketlerarası satış siparişi satırıyla eşitlenir.
1. **Referans** bölümündeki **Harici** alanında, seçili sipariş satırında belirtilen madde için harici bir madde kodu sağlayın. Bu değer ilgili şirketlerarası satış siparişi satırıyla eşitlenir.

Daha fazla bilgi içi bkz. [Harici müşteri için şirketlerarası satış siparişi oluşturma ve faturalama](../sales-marketing/intercompany-sales-order-for-external-customer.md).
