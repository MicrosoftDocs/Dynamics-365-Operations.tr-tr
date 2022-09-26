---
title: Stok Görünürlüğü uygulaması
description: Bu makalede, Stok Görünürlüğü uygulamasının nasıl kullanılacağı açıklanmaktadır.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 674adb70cc4372a8c5ca8c75ed3ef840d8ec7b79
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520877"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility uygulamasını kullanma

[!include [banner](../includes/banner.md)]

Bu makalede, Stok Görünürlüğü uygulamasının nasıl kullanılacağı açıklanmaktadır.

Stok görünürlüğü, görselleştirme için bir model temelli uygulama sağlar. Uygulama üç sayfa içerir: **Yapılandırma**, **Operasyonel görünürlük** ve **Stok özeti**. Aşağıdaki özelliklere sahiptir:

- Eldeki yapılandırma ve geçici rezervasyon yapılandırması için bir kullanıcı arabirimi (UI) sağlar.
- Çeşitli boyut birleşimlerinde gerçek zamanlı eldeki stok sorgularını destekler.
- Rezervasyon taleplerini deftere nakletmek için bir kullanıcı arabirimi sağlar.
- Tüm boyutlarla birlikte ürünler için eldeki stokların görünümünü sağlar.
- Önceden tanımlı boyutlarla birlikte ürünler için eldeki stok listesinin görünümünü sağlar.


## <a name="prerequisites"></a>Ön Koşullar

Başlamadan önce, Stok Görünürlüğü Eklentisini [Stok Görünürlüğü'nü yükleme ve ayarlama](inventory-visibility-setup.md) bölümünde açıklandığı gibi yükleyin ve ayarlayın.

## <a name="open-the-inventory-visibility-app"></a>Stok Görünürlüğü uygulamasını açma

Stok Görünürlüğü uygulamasını açmak için Power Apps ortamınızda oturum açıp **Stok Görünürlüğü**'nü açın.

## <a name="configuration"></a><a name="configuration"></a>Konfigürasyon

Stok Görünürlüğü uygulamasının **Yapılandırma** sayfası eldeki yapılandırmasını ve geçici rezervasyon yapılandırmasını ayarlamanıza yardımcı olur. Eklenti yüklendikten sonra varsayılan yapılandırma, Microsoft Dynamics 365 Supply Chain Management (`fno` veri kaynağı) için varsayılan kurulumu içerir. Varsayılan ayarı inceleyebilirsiniz. Bundan sonra, iş gereksinimlerinize ve harici sisteminizin stok deftere nakil gereksinimlerine göre yapılandırmayı, stok değişikliklerinin birden çok sistem arasında deftere nakledilme, düzenlenme ve sorgulanma şeklini standartlaştırmak için değiştirebilirsiniz.

Çözümün nasıl yapılandırılacağıyla ilgili tüm ayrıntılar için bkz. [Stok Görünürlüğünü Yapılandırma](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Operasyonel görünürlük

**Operasyonel Görünürlük** sayfası, çeşitli boyut birleşimlerine göre gerçek zamanlı eldeki stok sorgusunun sonuçlarını sağlar. *OnHandReservation* özelliği açıldığında, **Operasyonel Görünürlük** sayfasından da rezervasyon isteklerini deftere nakledebilirsiniz.

### <a name="on-hand-query"></a>Eldeki sorgu

**Eldeki Sorgu** sekmesi, gerçek zamanlı eldeki stok sorgusunun sonuçlarını gösterir.

**Operasyonel Görünürlük** sayfasının **Eldeki Sorgu** sekmesini açtığınızda sistem, Stok Görünürlüğü hizmetini sorgulamak için gereken taşıyıcı belirteci alabilmesi için kimlik bilgilerinizi ister. Taşıyıcı belirtecini, **BearerToken** alanına yapıştırabilir ve iletişim kutusunu kapatabilirsiniz. Ardından, eldeki sorgu isteğini deftere nakledebilirsiniz.

Taşıyıcı belirteci geçerli değilse veya süresi dolmuşsa **BearerToken** alanına yeni bir tane yapıştırmanız gerekir. **İstemci Kimliği**, **Kiracı Kimliği**, **İstemci Gizli Anahtarı**'nın doğru değerlerini girin ve ardından **Yenile**'yi seçin. Sistem otomatik olarak yeni ve geçerli bir taşıyıcı belirteci alır.

Eldeki sorgusunu deftere nakletmek için sorguyu istek gövdesine girin. [Nakletme yöntemini kullanarak sorgulama](inventory-visibility-api.md#query-with-post-method) içinde açıklanan modeli kullanın.

![Eldeki sorgu ayarları](media/inventory-visibility-query-settings.png "Eldeki sorgu ayarları")

### <a name="reservation-posting"></a>Rezervasyonun deftere nakli

Rezervasyon isteğini deftere nakletmek için **Operasyonel Görünürlük** sayfasının **Rezervasyonun Deftere Nakli** sekmesini kullanın. Rezervasyon isteğini deftere nakletmeden önce *OnHandReservation* özelliğini açmalısınız. Bu özellik ve etkinleştirme hakkında daha fazla bilgi için bkz. [Stok Görünürlüğü rezervasyonları](inventory-visibility-reservations.md).

Rezervasyon isteğini deftere nakletmek için talep gövdesine bir değer girmelisiniz. [Rezervasyon olayı oluşturma](inventory-visibility-api.md#create-one-reservation-event) bölümünde açıklanan modeli kullanın. Ardından **Deftere Naklet**'i seçin. İstek yanıtı ayrıntılarını görüntülemek için **Ayrıntıları göster**'i seçin. Ayrıca yanıt ayrıntılarından `reservationId` değerini de alabilirsiniz.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Stok özeti

**Stok özeti** sayfası tüm boyutlarla birlikte ürünler için bir stok özeti sağlar. *Eldeki Stok Toplamı* varlığı için özelleştirilmiş bir görünümdür. Stok özeti verileri, Stok Görünürlüğü'nden periyodik olarak eşitlenir.

**Stok özeti** sayfasını etkşnleştirmek ve eşitleme sıklığını ayarlamak için şu adımları izleyin:

1. **Yapılandırma** sayfasını açın.
1. **Özellik Yönetimi ve Ayarlar** sekmesini açın.
1. **OnHandMostSpecificBackgroundService** özelliğinin düğmesini *Evet* olarak ayarlayın.
1. Özellik etkinleştirildiğinde **Hizmet Yapılandırması** bölümü kullanılabilir hale gelir ve **OnHandMostSpecificBackgroundService** özelliğini yapılandırma için bir satır içerir. Bu ayar, stok özeti verilerinin eşitlendiği sıklığı seçmenize olanak tanır. Eşitlemeler arasındaki zamanı değiştirmek için (en az 5 dakika olabilir) **Değer** sütunundaki **Yukarı** ve **Aşağı** düğmelerini kullanın. Sonra **Kaydet**'i seçin.

    ![OnHandMostSpecificBackgroundService Ayarı](media/inventory-visibility-ohms-freq.png "OnHandMostSpecificBackgroundService Ayarı")

1. Tüm değişiklikleri kaydetmek için **Yapılandırmayı güncelleştir**'i seçin.


> [!NOTE]
> *OnHandMostSpecificBackgroundService* özelliği yalnızca özelliği açtıktan sonra oluşan eldeki stok değişikliklerini izler. Özelliği açtığınızdan bu yana değiştirilemeyen ürünlere ait veriler, stok hizmeti önbelleğinden Dataverse ortamına eşitlenmez. **Stok özeti** sayfanız beklediğiniz eldeki ürün bilgilerinin tümünü göstermiyorsa Supply Chain Management'ı açın, **Stok Yönetimi > Periyodik görevler > Stok görünürlüğü tümleştirmesi**'ne gidin, toplu işi devre dışı bırakın ve yeniden etkinleştirin. Bu işlemi, ilk gönderimi yapacak ve tüm veriler sonraki 15 dakika içinde *Stok Eldeki Toplam* varlığıyla eşitlenecektir. *OnHandMostSpecificBackgroundService* özelliğini kullanmak istiyorsanız herhangi bir eldeki miktar değişikliği oluşturmadan ve **Stok Görünürlüğü tümleştirmesi** toplu işlemini etkinleştirmeden önce bunu etkinleştirmenizi öneririz.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-the-inventory-visibility-onhand-query"></a>Kolaylaştırılmış eldeki sorguyu önceden yükleme

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management, geçerli eldeki stoklarınız hakkında büyük bilgileri depolar ve bunu çok çeşitli amaçlarla kullanabilir hale getirir. Ancak, birçok günlük işlem ve üçüncü taraf tümleştirme bu ayrıntıların yalnızca küçük bir alt kümesini gerektirir ve sistemin tümü için sorgulanmaları, birleştirme ve aktarma zamanı alan büyük veri kümelerine neden olabilir. Bu nedenle, stok görünürlüğü, en iyi duruma getirilmiş bilgileri sürekli kullanılabilir hale getirmek için düzenli olarak eldeki stok verilerinin rahat bir kümesini alıp depolayabilir. Depolanan eldeki stok ayrıntıları, yalnızca en ilgili bilgilerin dahil edilmesini sağlamak amacıyla konfigüre edilebilir iş ölçütlerine göre filtrelenir. Filtre uygulanan eldeki stok listeleri stok görünürlüğü hizmetinde yerel olarak depolandığından ve düzenli olarak güncelleştirildiklerinden, Hızlı erişimi, isteğe bağlı veri aktarma ve harici sistemlerle kolay tümleşiklik desteği vardır.

> [!NOTE]
> Bu özelliğin geçerli önizleme sürümü yalnızca, site ve konum içeren önceden yüklenmiş sonuçlar sağlayabilir. Özelliğin son sürümünün, sonuçlarla önceden yüklemek üzere başka boyutları seçmenizi sağlamak beklenir.

**Stok Görünürlüğü Özetini Önceden Yükle** sayfası, *Eldeki Dizin Sorgu Önyükleme Sonuçları* varlığı için bir görünüm sağlar. *Stok özet* varlığından farklı olarak, *Eldeki Dizin Sorgu Önyükleme Sonuçları* varlığı, ürünler için seçili boyutlarla birlikte bir eldeki stok listesi sağlar. Stok Görünürlüğü, önceden yüklenmiş özet verileri her 15 dakikada bir eşitler.

**Stok Görünürlük Özetini Önceden Yükleme** sekmesindeki verileri görüntülemek için **Yapılandırma** sayfasının **Özellik Yönetimi** sekmesindeki *OnHandIndexQueryPreloadBackgroundService* özelliğini etkinleştirmeniz ve ardından **Yapılandırmayı güncelleştir**'i seçmeniz gerekir (ayrıca bkz. [Stok Görünürlüğünü Yapılandırma](inventory-visibility-configuration.md)).

> [!NOTE]
> *OnhandMostSpecificBackgroudService* özelliğinde olduğu üzere *OnHandIndexQueryPreloadBackgroundService* özelliği de yalnızca özelliği etkinleştirdikten sonra gerçekleşen eldeki stok değişikliklerini izler. Özelliği açtığınızdan bu yana değiştirilemeyen ürünlere ait veriler, stok hizmeti önbelleğinden Dataverse ortamına eşitlenmez. **Stok özeti** sayfanız beklediğiniz eldeki ürün bilgilerinin tümünü göstermiyorsa **Stok Yönetimi > Periyodik görevler > Stok görünürlüğü tümleştirmesi**'ne gidin, toplu işi devre dışı bırakın ve yeniden etkinleştirin. Bu işlemi, ilk gönderimi yapacak ve tüm veriler sonraki 15 dakika içinde *Eldeki Dizin Sorgusu Önceden Yükleme Sorguları* varlığıyla eşitlenecektir. Bu özelliği kullanmak istiyorsanız herhangi bir eldeki miktar değişikliği oluşturmadan ve **Stok Görünürlüğü tümleştirmesi** toplu işlemini etkinleştirmeden önce bunu etkinleştirmenizi öneririz.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>Stok özetlerini filtreleyin ve göz atın

Dataverse'in sağladığı **Gelişmiş filtre**'yi kullanarak sizin için önemli olan satırları gösteren bir kişisel görünüm oluşturabilirsiniz. Gelişmiş filtre seçenekleri, basitten karmaşığa doğru geniş aralıklı görünümler oluşturmanıza olanak tanır. Ayrıca filtrelere gruplanmış ve iç içe koşullar eklemenize de olanak tanır. Gelişmiş filtrenin nasıl kullanılacağı hakkında daha fazla bilgi edinmek için bkz. [Gelişmiş ızgara filtrelerini kullanarak kişisel görünümleri düzenleme veya oluşturma](/powerapps/user/grid-filters-advanced).

**Stok özeti** sayfası, hangi sütunların görünür olduğunu kontrol etmek için kullanabileceğiniz kılavuzun üzerinde üç alan sağlar (**Varsayılan boyut**, **Özel boyut** ve **Ölçüm**). Ayrıca bu sütuna göre geçerli sonucu filtrelemek veya sıralamak için sütun başlığını seçebilirsiniz. Aşağıdaki ekran görüntüsünde, **Stok özeti** sayfasında bulunan boyut, filtre uygulama, sonuç sayısı ve "daha fazla yükle" alanları vurgulanır.

![Stok özeti sayfası.](media/inventory-visibility-onhand-list.png "Stok özeti sayfası")

Özet verileri yüklemek için kullanılan boyutları önceden tanımlamış olacağından, **Stok Görünürlüğü özetini ön yükleme** sayfası, boyutla ilgili sütunları görüntüler. *Boyutlar özelleştirilemez &mdash;sistem yalnızca önceden yüklenmiş eldeki listeler için tesis ve yerleşim boyutlarını destekler.* **Stok Görünürlüğü özetini önceden yükle** sayfası, boyutların zaten seçili olması dışında, **Stok özeti** sayfasında olanlarla benzerlik gösteren filtreler sağlar. Aşağıdaki ekran görüntüsünde, **Stok Görünürlüğü özetini önceden yükle** sayfasındaki kullanılabilir filtreleme alanları vurgulanır.

![Stok Görünürlüğü özetini önceden yükle sayfası.](media/inventory-visibility-preload-onhand-list.png "Stok Görünürlüğü özetini önceden yükle sayfası")

**Stok Görünürlüğü özetini önceden yükle** ve **Stok özeti** sayfalarının altında, "50 kayıt (29'u seçili)" ya da "50 kayıt" gibi bilgiler yer alır. Bu bilgi, **Gelişmiş filtre** sonucundan şu anda yüklenen kayıtları ifade eder. "29 seçili" metni, yüklenen kayıtlar için sütun başlığı filtresi kullanılarak seçilen kayıtların sayısını ifade eder. Ayrıca Dataverse'ten daha fazla kayıt yüklemek için kullanabileceğiniz bir **Daha fazla yükle** düğmesi vardır. Yüklenen varsayılan kayıt sayısı 50'dir. **Daha fazla yükle**'yi seçtiğinizde, sonraki 1.000 kullanılabilir kayıt görünüme yüklenir. **Daha fazlasını yükle** düğmesindeki sayı, o anda yüklü olan kayıtları ve **Gelişmiş Filtre** sonucu için toplam kayıt sayısını gösterir.
