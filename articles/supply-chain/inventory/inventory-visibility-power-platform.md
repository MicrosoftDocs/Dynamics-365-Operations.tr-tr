---
title: Stok Görünürlüğü uygulaması
description: Bu makalede, Stok Görünürlüğü uygulamasının nasıl kullanılacağı açıklanmaktadır.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a360b8beaad2bf6916c22765131e37f90e40282b
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306188"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility uygulamasını kullanma

[!include [banner](../includes/banner.md)]


Bu makalede, Stok Görünürlüğü uygulamasının nasıl kullanılacağı açıklanmaktadır.

Stok görünürlüğü, görselleştirme için bir model temelli uygulama sağlar. Uygulama üç sayfa içerir: **Yapılandırma**, **Operasyonel görünürlük** ve **Stok özeti**. Aşağıdaki özelliklere sahiptir:

- Eldeki yapılandırma ve geçici rezervasyon yapılandırması için bir kullanıcı arabirimi (UI) sağlar.
- Çeşitli boyut birleşimlerinde gerçek zamanlı eldeki stok sorgularını destekler.
- Rezervasyon taleplerini deftere nakletmek için bir kullanıcı arabirimi sağlar.
- Tüm boyutlarla birlikte ürünler için eldeki stokların özelleştirilmiş görünümünü sağlar.

## <a name="prerequisites"></a>Önkoşullar

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

**Eldeki Sorgu** sekmesini seçtiğinizde sistem, Stok Görünürlüğü hizmetini sorgulamak için gereken taşıyıcı belirteci alabilmesi için kimlik bilgilerinizi ister. Taşıyıcı belirtecini, **BearerToken** alanına yapıştırabilir ve iletişim kutusunu kapatabilirsiniz. Ardından, eldeki sorgu isteğini deftere nakledebilirsiniz.

Taşıyıcı belirteci geçerli değilse veya süresi dolmuşsa **BearerToken** alanına yeni bir tane yapıştırmanız gerekir. **İstemci Kimliği**, **Kiracı Kimliği**, **İstemci Gizli Anahtarı**'nın doğru değerlerini girin ve ardından **Yenile**'yi seçin. Sistem otomatik olarak yeni ve geçerli bir taşıyıcı belirteci alır.

Eldeki sorgusunu deftere nakletmek için sorguyu istek gövdesine girin. [Nakletme yöntemini kullanarak sorgulama](inventory-visibility-api.md#query-with-post-method) içinde açıklanan modeli kullanın.

![Eldeki sorgu ayarları](media/inventory-visibility-query-settings.png "Eldeki sorgu ayarları")

### <a name="reservation-posting"></a>Rezervasyonun deftere nakli

Rezervasyon isteğini deftere nakletmek için **Rezervasyonun Deftere Nakli** sekmesini kullanın. Rezervasyon isteğini deftere nakletmeden önce *OnHandReservation* özelliğini açmalısınız. Bu özellik hakkında daha fazla bilgi için bkz. [Stok Görünürlüğü rezervasyonları](inventory-visibility-reservations.md).

Rezervasyon isteğini deftere nakletmek için talep gövdesine bir değer girmelisiniz. [Rezervasyon olayı oluşturma](inventory-visibility-api.md#create-one-reservation-event) bölümünde açıklanan modeli kullanın. Ardından **Deftere Naklet**'i seçin. İstek yanıtı ayrıntılarını görüntülemek için **Ayrıntıları göster**'i seçin. Ayrıca yanıt ayrıntılarından `reservationId` değerini de alabilirsiniz.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Stok özeti

**Stok özeti** sayfası tüm boyutlarla birlikte ürünler için bir stok özeti sağlar. *Eldeki Stok Toplamı* varlığı için özelleştirilmiş bir görünümdür. Stok özeti verileri, Stok Görünürlüğü'nden periyodik olarak eşitlenir.

### <a name="enable-the-inventory-summary-and-set-the-synchronization-frequency"></a>Stok özetini etkinleştirin ve eşitleme sıklığını ayarlayın

**Stok özeti** sayfasını etkşnleştirmek ve eşitleme sıklığını ayarlamak için şu adımları izleyin:

1. **Yapılandırma** sayfasını açın.
1. **Özellik Yönetimi ve Ayarlar** sekmesini açın.
1. **OnHandMostSpecificBackgroundService** özelliğinin düğmesini *Evet* olarak ayarlayın.
1. Özellik etkinleştirildiğinde **Hizmet Yapılandırması** bölümü kullanılabilir hale gelir ve **OnHandMostSpecificBackgroundService** özelliğini yapılandırma için bir satır içerir. Bu ayar, stok özeti verilerinin eşitlendiği sıklığı seçmenize olanak tanır. Eşitlemeler arasındaki zamanı değiştirmek için (en az 5 dakika olabilir) **Değer** sütunundaki **Yukarı** ve **Aşağı** düğmelerini kullanın. Sonra **Kaydet**'i seçin.
1. Tüm değişiklikleri kaydetmek için **Yapılandırmayı güncelleştir**'i seçin.

![OnHandMostSpecificBackgroundService Ayarı](media/inventory-visibility-ohms-freq.PNG "OnHandMostSpecificBackgroundService Ayarı")

> [!NOTE]
> *OnHandMostSpecificBackgroundService* özelliği yalnızca özelliği açtıktan sonra oluşan eldeki ürün değişikliklerini izler. Özelliği açtığınızdan bu yana değiştirilemeyen ürünlere ait veriler, stok hizmeti önbelleğinden Dataverse ortamına eşitlenmez. **Stok özeti** sayfanız beklediğiniz eldeki ürün bilgilerinin tümünü göstermiyorsa **Stok Yönetimi > Periyodik görevler > Stok görünürlüğü tümleştirmesi**'ne gidin, toplu işi devre dışı bırakın ve yeniden etkinleştirin. Bu işlemi, ilk gönderimi yapacak ve tüm veriler sonraki 15 dakika içinde *Stok Eldeki Toplam* varlığıyla eşitlenecektir. Bu özelliği kullanmak istiyorsanız herhangi bir eldeki miktar değişikliği oluşturmadan ve **Stok Görünürlüğü tümleştirmesi** toplu işlemini etkinleştirmeden önce bunu etkinleştirmenizi öneririz.

### <a name="work-with-the-inventory-summary"></a>Stok özeti ile çalışma

Dataverse'in sağladığı **Gelişmiş filtre**'yi kullanarak sizin için önemli olan satırları gösteren bir kişisel görünüm oluşturabilirsiniz. Gelişmiş filtre seçenekleri, basitten karmaşığa doğru geniş aralıklı görünümler oluşturmanıza olanak tanır. Ayrıca filtrelere gruplanmış ve iç içe koşullar eklemenize de olanak tanır. **Gelişmiş filtre**'nin nasıl kullanılacağı hakkında daha fazla bilgi edinmek için bkz. [Gelişmiş ızgara filtrelerini kullanarak kişisel görünümleri düzenleme veya oluşturma](/powerapps/user/grid-filters-advanced).

Özelleştirilmiş görünümün üst kısmında üç alan bulunur: **Varsayılan boyut**, **Özel boyut** ve **Ölçü**. Hangi sütunların görünür olduğunu denetlemek için bu alanları kullanabilirsiniz.

Geçerli sonucu filtrelemek veya sıralamak için sütun başlığını seçebilirsiniz.

Özelleştirilmiş görünümün alt kısmında "50 kayıt (29 seçili)" veya "50 kayıt" gibi bilgiler gösterilir. Bu bilgi, **Gelişmiş filtre** sonucundan şu anda yüklenen kayıtları ifade eder. "29 seçili" metni, yüklenen kayıtlar için sütun başlığı filtresi kullanılarak seçilen kayıtların sayısını ifade eder.

Görünümün altında, Dataverse'ten daha fazla kayıt yüklemek için kullanabileceğiniz bir **Daha fazla yükle** düğmesi vardır. Yüklenen varsayılan kayıt sayısı 50'dir. **Daha fazla yükle**'yi seçtiğinizde, sonraki 1.000 kullanılabilir kayıt görünüme yüklenir. **Daha fazlasını yükle** düğmesindeki sayı, o anda yüklü olan kayıtları ve **Gelişmiş Filtre** sonucu için toplam kayıt sayısını gösterir.

![Stok Özeti](media/inventory-visibility-onhand-list.png "Stok Özeti")
