---
title: Hesap yönetimi sayfaları ve modülleri
description: Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarını ve modüllerini kapsamaktadır.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785405"
---
# <a name="account-management-pages-and-modules"></a>Hesap yönetimi sayfaları ve modülleri

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarını ve modüllerini kapsamaktadır.

## <a name="overview"></a>Genel Bakış

Hesap yönetimi, Dynamics 365 Commerce'teki Kullanıcı hesabı ile ilgili bilgileri yönetmek için kullanılan bir grup sayfayı gösterir. Hesap yönetimi sayfaları, hesap yönetimi giriş sayfası, kullanıcı profili sayfası, kullanıcı adresi sayfası, sipariş geçmişi sayfası, sipariş ayrıntıları sayfası, bağlılık programı sayfası ve istek listesi sayfasını içerir.

### <a name="account-management-landing-page"></a>Hesap yönetimi giriş sayfası

Hesap yönetimi giriş sayfası aşağıdaki modülleri kullanır:

- **İçerik yerleşimi** – bu modül hesap yönetimi giriş sayfasındaki tüm modülleri tutan bir konteyner modülüdür.
- **Hesap karşılama öğesi** – bu modül, hesap yönetimi sayfasında hoş geldiniz iletisi sağlamak için kullanılır. Başlık ve döşeme boyutu özelliklerini içerir. **Döşeme boyutu** özelliği, içerik yerleştirme modülündeki modülün genişliğini tanımlar. Değerler **1** ile **12**arasında değişir (burada **12**, içerik yerleşimi konteynerin tam genişliğini gösterir).
- **Hesap düzeni yerleşim maddesi** – bu modül, Kullanıcı hesabı tarafından verilen sipariş sayısının özetini sağlamak için kullanılır. Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir. "Ayrıntıları görüntüle" bağlantısı sipariş geçmişi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.
- **Hesap profili yerleştirme öğesi** – bu modül, Kullanıcı profilinin özetini sağlamak için kullanılır. Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir. "Ayrıntıları görüntüle" bağlantısı kullanıcı profili sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.
- **Hesap istek listesi maddesi** – bu modül, müşterinin istek listesindeki maddelerin özetini sağlamak için kullanılır. Örneğin, "İstek listenizde 10 öğe var" olabilir. Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir. "Ayrıntıları görüntüle" bağlantısı istek listesi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.
- **Hesap adresi öğesi** – bu modül, Kullanıcı adreslerinin özetini sağlamak için kullanılır. Örneğin, "Hesabınıza 2 adres eklendi" durumu olabilir. Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir. "Ayrıntıları görüntüle" bağlantısı kullanıcı adresi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.
- **Hesap bağlılık maddesi** – Bu modül, bağlılık programı bilgilerini göstermek ve bağlamak için kullanılır. Başlık, döşeme boyutu, "ayrıntıları göster" ve "üye ol" bağlantısı özelliklerini içerir. "Ayrıntıları görüntüle" bağlantısı bağlılık sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir. "Üye olun" bağlantısı, kullanıcıların bağlılık programına katılabilecek bir sayfaya yeniden yönlendirilecek şekilde konfigüre edilmelidir.

### <a name="order-history-page"></a>Sipariş geçmişi sayfası

Sipariş geçmişi sayfası, kullanıcının verdiği tüm son siparişleri göstermek için sipariş geçmişi modülünü kullanır.

### <a name="order-details-page"></a>Sipariş ayrıntıları sayfası

Sipariş Ayrıntıları sayfası her sipariş için ayrıntılı bilgi sağlar ve sipariş geçmişi sayfasından erişilir. Sipariş ayrıntılarını almak için satış kodu veya işlem kodunun gerekli olmasını gerektiren sipariş ayrıntıları modülünü kullanır.

### <a name="user-profile-page"></a>Kullanıcı profil sayfası

Kullanıcı profili sayfası kullanıcının adı ve e-posta adresi gibi kullanıcı hesabı ayrıntılarını gösterir. Kullanıcı profili modülünü kullanır. Ancak e-posta adresi kaldırılamaz, düzenlenebilir.

### <a name="user-address-page"></a>Kullanıcı adresi sayfası

Kullanıcı adresi sayfası, kullanıcı hesabıyla ilişkili adreslerin listesini gösterir. Kullanıcı bu adresleri kullanıma alma sırasında sağladı veya doğrudan bu sayfaya ekledi. Kullanıcı Adres modülü, adres ekleme ve düzenleme, birincil adresi belirleme ve varolan adresleri sayfada işleme seçeneğini kullanır.

### <a name="wish-list-page"></a>İstek listesi sayfası

İstek listesi sayfası, müşterinin istek listesine eklenen maddeleri gösterir. Liste öğelerini oluşturmak için, istek listesi modülünü kullanır.

### <a name="loyalty-page"></a>Bağlılık programı sayfası

Bağlılık programı, müşterilerinin bir bağlılık programına katılmasına veya zaten bağlılık programı üyesi olduklarında Program ayrıntılarını görüntülemesine olanak tanır. Ayrıca, son hareketlerde kazanılan ve bunlar tarafından kullanılan puanları de görüntüleyebilirler.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
