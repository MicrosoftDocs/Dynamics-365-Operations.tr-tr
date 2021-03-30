---
title: Hesap yönetimi sayfaları ve modülleri
description: Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarını ve modüllerini kapsamaktadır.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206643"
---
# <a name="account-management-pages-and-modules"></a>Hesap yönetimi sayfaları ve modülleri

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarını ve modüllerini kapsamaktadır.

Hesap yönetimi, Dynamics 365 Commerce'teki Kullanıcı hesabı ile ilgili bilgileri yönetmek için kullanılan bir grup sayfayı gösterir. Hesap yönetimi sayfaları, hesap yönetimi giriş sayfası, kullanıcı profili sayfası, kullanıcı adresi sayfası, sipariş geçmişi sayfası, sipariş ayrıntıları sayfası, bağlılık programı sayfası ve istek listesi sayfasını içerir.

### <a name="account-management-landing-page"></a>Hesap yönetimi giriş sayfası

Hesap yönetimi giriş sayfası aşağıdaki modülleri kullanır:

- **Konteyner** - Tüm hesap yönetimi giriş sayfası modülleri bir kapsayıcı içinde yer almalıdır. 
- **Hesap karşılama kutucuğu** – bu modül, hesap yönetimi sayfasında hoş geldiniz iletisi sağlamak için kullanılır. Başlığa ilişkin özellikleri içerir.
- **Hesap genel kutucuğu** -bu modül, "Sipariş geçmişi" veya "Profilim" sayfaları gibi hesap yönetimi sayfalarına başlık ve bağlantı sağlamak için kullanılabilir. Genel döşeme modülü herhangi bir sayfa için bir kutucuğu yapılandırmak amacıyla kullanılabilir. Fabrikam'da, bu modül hesap yönetimi giriş sayfasındaki "Sipariş geçmişi" ve "Profilim" sayfa bağlantıları için kullanılır.
- **Hesap istek listesi kutucuğu** – bu modül, müşterinin istek listesindeki maddelerin özetini sağlamak için kullanılır. Örneğin, "İstek listenizde 10 öğe var" olabilir. Başlık, başlık için özellikleri ve "Ayrıntıları görüntüle" bağlantısı özelliklerini içerir. "Ayrıntıları Görüntüle" bağlantısı istek listesi sayfasına yeniden yönlendirilecek şekilde yapılandırılmalıdır. 
- **Hesap adresi kutucuğu** – bu modül, Kullanıcı adreslerinin özetini sağlamak için kullanılır. Örneğin, "Hesabınıza 2 adres eklendi" durumu olabilir. Başlık, başlık için özellikleri ve "Ayrıntıları görüntüle" bağlantısı özelliklerini içerir. "Ayrıntıları Görüntüle" bağlantısı kullanıcı adresi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.
- **Hesap bağlılık kutucuğu** – Bu modül, bağlılık programı bilgilerini görüntülemek ve bağlamak için kullanılır. Bu kutucuğun iki durumu vardır: bir durum, bir üye değilse, bağlılık programına katılma bağlantılarını gösterir. Diğer durum, kullanıcının zaten üye olduğunda bağlılık programı ayrıntıları sayfasını görüntülemek için bağlantıları gösterir. Özellikler başlığı, "Kaydol" bağlantısı ve "Bağlılık programını görüntüle" bağlantısını içerir. "Bağlılık programını görüntüle" bağlantısı bağlılık sayfasına yeniden yönlendirilecek şekilde yapılandırılmalıdır. "Üye olun" bağlantısı, kullanıcıların bağlılık programına katılabilecek bir sayfaya yeniden yönlendirilecek şekilde yapılandırılmalıdır. 

### <a name="order-history-page"></a>Sipariş geçmişi sayfası

Sipariş geçmişi sayfası, kullanıcının verdiği tüm son siparişleri göstermek için sipariş geçmişi modülünü kullanır.

### <a name="order-details-page"></a>Sipariş ayrıntıları sayfası

Sipariş Ayrıntıları sayfası her sipariş için ayrıntılı bilgi sağlar ve sipariş geçmişi sayfasından erişilir. Sipariş ayrıntılarını almak için satış kodu veya işlem kodunun gerekli olmasını gerektiren sipariş ayrıntıları modülünü kullanır.

### <a name="user-profile-page"></a>Kullanıcı profil sayfası

Kullanıcı profili sayfası kullanıcının adı ve e-posta adresi gibi kullanıcı hesabı ayrıntılarını gösterir. Kullanıcı profili ayrıntılarını ve Kullanıcı profili düzenleme modüllerini kullanır. Ancak e-posta adresi kaldırılamaz, düzenlenebilir. Kullanıcı profili sayfası, kullanıcının öneri listelerinin kişiselleştirmesi gibi belirli özellikleri kabul etmesini veya devre dışı olmasını etkinleştiren Kullanıcı tercihlerini de gösterir. 

### <a name="user-address-page"></a>Kullanıcı adresi sayfası

Kullanıcı adresi sayfası, kullanıcı hesabıyla ilişkili adreslerin listesini gösterir. Kullanıcı bu adresleri kullanıma alma sırasında sağladı veya doğrudan bu sayfaya ekledi. Kullanıcı Adres modülü, adres ekleme ve düzenleme, birincil adresi belirleme ve varolan adresleri sayfada işleme seçeneğini kullanır.

### <a name="wish-list-page"></a>İstek listesi sayfası

İstek listesi sayfası, müşterinin istek listesine eklenen maddeleri gösterir. Liste öğelerini oluşturmak için, istek listesi modülünü kullanır.

### <a name="loyalty-page"></a>Bağlılık programı sayfası

Bağlılık programı sayfası müşterilerin, eğer halihazırda üyelerse, bağlılık programı ayrıntılarını görmelerini sağlar. Ayrıca, son hareketlerde kazanılan ve bunlar tarafından kullanılan puanları de görüntüleyebilirler. Sayfa bağlılık programı ayrıntılarını gösterimi için bağlılık programı Ayrıntılar modülünü kullanır. 

Bağlılık programı programına katılmak için, bağlılık programı kayıt ve bağlılık programı şartları modülleriyle bir pazarlama sayfası oluşturulabilir. Kullanıcı bir bağlılık programı üyesi değilse, bu modüller kullanıcının kaydolmasını sağlayacaktır.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Kapsayıcı modülü](add-container-module.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Alışveriş sepeti modülü](add-cart-module.md)

[Ödeme yapma modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]