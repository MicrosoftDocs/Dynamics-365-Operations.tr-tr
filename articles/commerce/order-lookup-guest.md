---
title: Konuk ödemeleri için sipariş aramayı etkinleştirme
description: Bu makalede, Microsoft Dynamics 365 Commerce'te konuk ödemeleri için sipariş aramanın nasıl etkinleştirileceği açıklanmaktadır.
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4f381f1ec0ea08f18db3cac474e8990906364504
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286904"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Konuk ödemeleri için sipariş aramayı etkinleştirme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te konuk ödemeleri için sipariş aramanın nasıl etkinleştirileceği açıklanmaktadır.

Konuk ödemeleri için sipariş arama özelliği, konuk kullanıcılar olarak satınalma yapan müşterilerin siparişlerini aramasını sağlar. Sipariş arama özelliği, müşteriler bir siparişteki ürünlerin karşılanma durumunu denetlemek, siparişin sevk edildiği adresi doğrulamak, bir ürünü yeniden sipariş etmek veya siparişin alınacağı mağazayı onaylamak gibi eylemler gerçekleştirmek istediğinde kullanışlıdır.

Kayıtlı kullanıcı olarak sipariş veren müşteriler, oturum açtıklarında sipariş ayrıntılarını görebilir ancak sipariş vermek için konuk ödemesini kullanan müşteriler göremez. Ancak konuk ödemeleri için sipariş arama özelliği etkinleştirildiğinde, müşterilerin konuk olarak verdikleri siparişleri aramak için kullanabilecekleri bir form sağlar. Bu formda müşteriler, sipariş onay kodunu ve (isteğe bağlı olarak) ödeme sırasında belirttikleri e-posta adresini girerler.

Ek olarak, müşteriyi siparişi için doğrudan sipariş ayrıntıları sayfasına götüren bir bağlantı veya düğme, siparişle ilgili herhangi bir işlem tabanlı e-postaya eklenebilir. Bu bağlantı veya düğme, hem kayıtlı kullanıcılar hem de konuk kullanıcılar tarafından verilen siparişler için çalışır.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>Commerce genel merkezinde gerekli özellikleri açma

Konuk ödemeleri için sipariş aramayı etkinleştirmek için Commerce genel merkezindeki **Çalışma Alanları \> Özellik yönetimi**'nde aşağıdaki özellikleri açmanız gerekir.

| Özellik | Amaç |
|---------|---------|
| Retail anonim kullanıcı arama emri ayrıntılarını etkinleştirme özelliği | Bu özellik, kimliği doğrulanmamış kullanıcılar için sipariş arama API'sini etkinleştirmenize ve kişisel verilerin nasıl görüntüleneceğini yapılandırmanızı sağlayan Commerce parametrelerindeki kullanıcı arabirimini ortaya çıkarır. |
| Daha güçlü bir kanal başvuru kimliği oluşturmayı etkinleştir | Bu özellik, bir sipariş arandığında sorgu dizesinde geçebilen daha güvenli 12 karakterli bir kanal referans kodu (sipariş onay kodu) oluşturur. |
| Tüm kanallar genelinde tutarlı bir kanal referans kimliği biçimi oluştur | Bu özellik; bir e-ticaret sitesi, perakende satış noktası (POS) veya bir çağrı merkezi aracılığıyla verilen siparişler için güvenli bir kanal referans kodu oluşturur. Bu özelliği açabilmeniz için **Daha güçlü bir kanal referans kodunun oluşturulmasını etkinleştirme** özelliğinin açık olması gerekir. |

**Perakende anonim kullanıcısı arama siparişi ayrıntılarını seçme özelliği**'ni açtıktan sonra, Commerce genel merkezinde kimliği doğrulanmamış sipariş aramasını destekleyen API'yi etkinleştirmeniz gerekir. **Retail ve Commerce \> Genel merkez kurulumu \> Parametreler \> Müşteri siparişleri**'ne gidin. **Müşteri siparişleri** sayfasındaki **Sipariş arama** hızlı sekmesinde, aşağıdaki şekilde gösterildiği gibi **Kimliği doğrulanmamış sipariş aramasını etkinleştir** seçeneğini **Evet** olarak ayarlayın.

## <a name="manage-the-display-of-personal-data"></a>Kişisel verilerin görünümünü yönetme

Commerce genel merkezindeki **Müşteri siparişleri** sayfasında **Sipariş arama** hızlı sekmesi, kişisel bilgilerin müşterilere gösterilip gösterilmeyeceğini denetlemenizi sağlayan bir **Konuk siparişi aramasına kişisel verileri dahil et** alanı içerir. Bu kişisel bilgiler müşterinin sevkiyat adresini ve müşterinin kredi kartı numarasının son dört basamağını içerir. Varsayılan olarak, kimliği doğrulanmamış sipariş arama etkinleştirildiğinde kişisel bilgiler müşterilere gösterilmez. Aşağıdaki tabloda kullanılabilir seçenekler açıklanmaktadır.

| Seçenek | Sonuç |
|--------|--------|
| Hiçbir Zaman | Varsayılan değer. Sipariş aramalarında hiçbir kişisel bilgi gösterilmez. Oturum açmış kayıtlı kullanıcılar, oturum açtıklarında oluşturdukları bir siparişi aradıklarında kişisel bilgilerini görebilir. |
| Yalnızca konuk siparişleri | Müşterilerin konuk olarak oluşturduğu siparişler için sipariş aramalarında kişisel bilgiler gösterilir. Sipariş, bir kayıtlı kullanıcı tarafından oluşturulduysa bu kullanıcının kişisel bilgilerini görmek için oturum açması gerekir. |
| Tüm siparişler | Kişisel bilgiler tüm sipariş aramalarında gösterilir. |

> [!NOTE]
> Bu seçenekler, müşterinin adresi ve müşterinin kredi kartı numarasının son dört basamağı gibi kişisel verilerin anonim konuk kullanıcılara ne zaman gösterileceğini belirler. Kayıtlı müşterilerin gizliliğinin korunmasına yardımcı olmak için **Yalnızca konuk siparişleri** seçeneğini belirlemenizi öneririz. Ancak en güvenli seçenek **Hiçbir Zaman**'dır.

**Kişisel verileri konuk siparişi aramasına dahil et** alanının değerini değiştirdikten sonra, **Retail ve Commerce \> Retail ve Commerce BT \> Dağıtım planı**'na giderek Commerce Headquarters'da 1070 işini (**Kanal yapılandırması**) çalıştırmanız gerekir.

## <a name="configure-the-order-lookup-module"></a>Sipariş arama modülünü yapılandırma

Commerce modülü kitaplığındaki sipariş arama modülü, konuk kullanıcıların siparişleri aramak için kullandıkları formu oluşturmak için kullanılır. Sipariş arama modülü, müşterinin oturum açmasını gerektirmeyen herhangi bir sayfanın gövde yuvasına dahil edilebilir. Modülün nasıl yapılandırılacağı hakkında bilgi için bkz. [Sipariş arama modülü](order-lookup-module.md).

## <a name="configure-the-order-details-page"></a>Sipariş ayrıntıları sayfasını yapılandırma

Konuk kullanıcıların sipariş ayrıntılarını görüntüleyebilmeleri için e-ticaret sitenizdeki sipariş ayrıntıları sayfasının oturum açmayı gerektirmeyen şekilde yapılandırılması gerekir. Sipariş ayrıntıları sayfanızın oturum açma gereksinimini kapatmak için sayfayı Commerce site oluşturucusunda açın, ağaç görünümünde **Varsayılan sayfa (gerekli)** yuvasını seçin ve sağdaki özellikler bölmesinin altındaki **Oturum açmayı gerektir?** onay kutusunun işaretini kaldırın.

## <a name="add-a-link-to-order-details-in-transactional-emails"></a>İşlem e-postalarındaki sipariş ayrıntılarına bağlantı ekleme

Siparişle ilgili e-postalarda, müşterileri sipariş bilgileri sayfasına götüren bir bağlantı veya düğme sağlayabilirsiniz. Bu bağlantıyı veya düğmeyi eklemek için e-ticaret sitenizdeki sipariş ayrıntıları sayfasına işaret eden bir HTML köprüsü oluşturun ve aşağıdaki örnekte gösterildiği gibi sipariş onay kimliği ve müşterinin e-posta adresini URL parametreleri olarak geçirin.

`<a href="https://[domain]/[orderdetailspage]?confirmationId=%orderconfirmationid%&propertyName=email&propertyValue=%customeremailaddress%" target="_blank">View my order status</a>`

## <a name="additional-resources"></a>Ek kaynaklar

[Sipariş arama modülü](order-lookup-module.md)

[E-posta bildirimi profili ayarlama](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
