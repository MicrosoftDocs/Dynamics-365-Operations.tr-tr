---
title: Stok Görünürlüğü uygulaması
description: Bu konuda, Stok Görünürlüğü uygulamasının nasıl kullanılacağı açıklanmaktadır.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0457190f2fc8cd0ed39e109e6720509b77b83566
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678531"
---
# <a name="use-the-inventory-visibility-app"></a>Stok Görünürlüğü uygulamasını kullanma

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Bu konuda, Stok Görünürlüğü uygulamasının nasıl kullanılacağı açıklanmaktadır.

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

**Stok özeti**, *Eldeki Stok Toplamı* varlığı için özelleştirilmiş bir görünümdür. Tüm boyutlarla birlikte ürünler için bir stok özeti sağlar. Stok özeti verileri, Stok Görünürlüğü'nden periyodik olarak eşitlenir. **Stok özeti** sekmesindeki verileri görüntüleyebilmeniz için **Özellik Yönetimi** sekmesinde *OnHandMostSpecificBackgroundService* özelliğini açmanız gerekir.

Dataverse'in sağladığı **Gelişmiş filtre**'yi kullanarak sizin için önemli olan satırları gösteren bir kişisel görünüm oluşturabilirsiniz. Gelişmiş filtre seçenekleri, basitten karmaşığa doğru geniş aralıklı görünümler oluşturmanıza olanak tanır. Ayrıca filtrelere gruplanmış ve iç içe koşullar eklemenize de olanak tanır. **Gelişmiş filtre**'nin nasıl kullanılacağı hakkında daha fazla bilgi edinmek için bkz. [Gelişmiş ızgara filtrelerini kullanarak kişisel görünümleri düzenleme veya oluşturma](/powerapps/user/grid-filters-advanced).

Özelleştirilmiş görünümün üst kısmında üç alan bulunur: **Varsayılan boyut**, **Özel boyut** ve **Ölçü**. Hangi sütunların görünür olduğunu denetlemek için bu alanları kullanabilirsiniz.

Geçerli sonucu filtrelemek veya sıralamak için sütun başlığını seçebilirsiniz.

Özelleştirilmiş görünümün alt kısmında "50 kayıt (29 seçili)" veya "50 kayıt" gibi bilgiler gösterilir. Bu bilgi, **Gelişmiş filtre** sonucundan şu anda yüklenen kayıtları ifade eder. "29 seçili" metni, yüklenen kayıtlar için sütun başlığı filtresi kullanılarak seçilen kayıtların sayısını ifade eder.

Görünümün altında, Dataverse'ten daha fazla kayıt yüklemek için kullanabileceğiniz bir **Daha fazla yükle** düğmesi vardır. Yüklenen varsayılan kayıt sayısı 50'dir. **Daha fazla yükle**'yi seçtiğinizde, sonraki 1.000 kullanılabilir kayıt görünüme yüklenir. **Daha fazlasını yükle** düğmesindeki sayı, o anda yüklü olan kayıtları ve **Gelişmiş Filtre** sonucu için toplam kayıt sayısını gösterir.

![Stok Özeti](media/inventory-visibility-onhand-list.png "Stok Özeti")
