---
title: B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma
description: Bu konuda, B2B e-ticaret siteleri için müşteri hesabı ödeme yönteminin nasıl yapılandırılacağı açıklanmaktadır.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 628f3b3b2d86154190dfdcc82b8b391c2facce103f607519514c65b5fba26653
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738065"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma

[!include [banner](../../includes/banner.md)]

Bu konuda, B2B e-ticaret siteleri için müşteri hesabı ödeme yönteminin nasıl yapılandırılacağı açıklanmaktadır.

Perakendeciler, e-ticaret kanalında sattıkları ürünler ve hizmetler karşılığında çeşitli türlerde ödemeler kabul edebilirler. Perakendecinin kabul edeceği ödeme türlerinin her biri, sistem ayarlandığında Microsoft Dynamics 365 Commerce'te yapılandırılmalıdır. Müşteri hesabı (veya "açık hesap") ödeme yöntemi, B2B e-ticaret sitelerinde desteklenmelidir. 

## <a name="prerequisites"></a>Önkoşullar

1. Müşteri hesabı ödeme yöntemini Commerce Headquarters'a ekleyin.
2. Müşteri hesabı ödeme yöntemini e-ticaret kanalıyla ilişkilendirin.
3. Commerce Headquarters'da **Perakende ve Ticaret \> Müşteriler \> Tüm müşteriler \> Ödeme varsayılanları** bölümünde müşteri için **Açık hesaba izin ver**'in etkinleştirildiğinden emin olun. Ayrıca, Commerce Headquarters'da **Perakende ve Ticaret \> Müşteriler \> Tüm müşteriler \>Kredi ve Tahsilatlar**'da **Kredi limiti** parametrelerinin müşteri için uygun şekilde ayarlandığından emin olun. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Commerce site oluşturucusunda müşteri hesabı ödeme yöntemini etkinleştirme 

Commerce site oluşturucuda müşteri hesabı ödeme yöntemini etkinleştirmek için aşağıdaki adımları izleyin.

1. **Site Ayarları \> Uzantılar**'a gidin.
1. **Müşteri hesabı ödemelerini etkinleştir** özelliğini **B2B müşterileri için etkin** olarak ayarlayın. 
1. **kaydet ve yayınla** yı seçin.

> [!NOTE]
> Yeni site ayarları yalnızca app.settings.json dosyası güncelleştirildikten sonra etkinleşir. Daha fazla bilgi için bkz. [SDK ve Modül kitaplığı güncelleştirmeleri](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>B2B e-ticaret siteleri için ödeme sayfasında müşteri hesabı ödeme yöntemini etkinleştirme

B2B e-ticaret sitesinin ödeme sayfasında müşteri hesabı ödeme yöntemini etkinleştirmek için şu adımları izleyin.

1. Commerce site oluşturucusunda, B2B e-ticaret sitesinin ödeme modüllerini içeren ödeme sayfasını veya parçasını bulun ve düzenleyin.
1. **Ödeme bölümü kapsayıcısı** alanında, **Modül Ekle**'yi seçin ve **Müşteri hesabı ödemesi** modülü ekleyin.
1. Üç noktayı (**...**) seçip gerektiği gibi **Yukarı Taşı** veya **Aşağı Taşı**'yı seçerek **Müşteri hesabı ödemesi** modülunu konumlandırın.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Müşteri hesabı ödeme yönteminin etkinleştirildiğini ve yayınlandığını onaylayın

Müşteri hesabı ödeme yönteminin etkinleştirildiğini onaylamak için şu adımları izleyin.

1. E-ticaret sitesinde oturum açın.
1. Sepete ürün ekleyin.
1. Ödeme sayfasına gidin. Yeni **Müşteri Hesabı** ödeme yöntemini görürsünüz.

## <a name="additional-resources"></a>Ek kaynaklar

[B2B e-ticaret sitesi ayarlama](set-up-b2b-site.md)

[B2B kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma](org-model.md)

[B2B e-ticaret sitelerindeki iş ortağı kullanıcılarını yönetme](manage-b2b-users.md)

[B2B e-ticaret siteleri için ürün miktarı sınırlarını ayarlama](quantity-limits.md)

[SDK ve Modül kitaplığı güncelleştirmeleri](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]