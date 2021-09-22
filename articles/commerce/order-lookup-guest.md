---
title: Konuk ödemeleri için sipariş aramayı etkinleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te konuk ödemeleri için sipariş aramanın nasıl etkinleştirileceği açıklanmaktadır.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 0368f567898210f122047a9f298bcb28b7540de1
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472692"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Konuk ödemeleri için sipariş aramayı etkinleştirme

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te konuk ödemeleri için sipariş aramanın nasıl etkinleştirileceği açıklanmaktadır.

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

**Konuk siparişi aramasına kişisel verileri dahil et** alanının değerini değiştirdikten sonra, Commerce genel merkezinde **Retail ve Commerce \> Retail ve Commerce BT \> Dağıtım planı**'na giderek 1070 (**Kanal yapılandırması**) işini çalıştırmalısınız.

## <a name="configure-the-order-lookup-module"></a>Sipariş arama modülünü yapılandırma

Commerce modülü kitaplığındaki sipariş arama modülü, konuk kullanıcıların siparişleri aramak için kullandıkları formu oluşturmak için kullanılır. Sipariş arama modülü, müşterinin oturum açmasını gerektirmeyen herhangi bir sayfanın gövde yuvasına dahil edilebilir. Modülün nasıl yapılandırılacağı hakkında bilgi için bkz. [Sipariş arama modülü](order-lookup-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Sipariş arama modülü](order-lookup-module.md)

[E-posta bildirimi profili ayarlama](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
