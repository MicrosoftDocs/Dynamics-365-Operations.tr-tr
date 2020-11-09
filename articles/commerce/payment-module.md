---
title: Ödeme modülü
description: Bu konu ödeme modülünü kapsamaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 894ac35973927c193d6e9c54e326daefb8a3f4a5
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055393"
---
# <a name="payment-module"></a>Ödeme modülü

[!include [banner](includes/banner.md)]

Bu konu ödeme modülünü kapsamaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.

## <a name="overview"></a>Genel bakış

Ödeme modülü, müşteriye bir kredi kartı veya banka kartı kullanarak sipariş ödemesi yapma olanağı tanır. Bu modül için ödeme tümleştirmesi, Adyen için Dynamics 365 Ödeme Bağlayıcısı tarafından sağlanır. Ödeme bağlayıcısını kurma ve yapılandırma hakkında daha fazla bilgi için bkz. [Adyen için Dynamics 365 Ödeme Bağlayıcısı](dev-itpro/adyen-connector.md).

Ödeme modülü, Adyen aracılığıyla HTML satır içi çerçevesinde (iframe) sunulan ödeme bilgilerini barındırır. Ödeme modülü, Adyen ödeme bilgilerini almak için Commerce Scale Unit ile etkileşime girer. Commerce Scale Unit etkileşiminin bir parçası olarak, ödeme modülü, fatura adres bilgilerinin iframe'de veya ayrı bir modül olarak sunulmasını sağlar. Fabrikam temasında, fatura adresi ayrı bir modülde gösterilir. Adres satırları sevkiyat adresinin satırlarına benzeyecek şekilde işlenebileceğinden, bu yaklaşım daha fazla biçimlendirme esnekliği sağlar.

Ayrıca ödeme modülü de oturum açmış müşterilerin ödeme bilgilerini kaydetmesine olanak tanır. Ödeme bilgileri ve faturalama adresi, Adyen ödeme bağlayıcısı aracılığıyla kaydedilir ve yönetilir.

Ödeme modülü, bağlılık programı puanları veya hediye kartı tarafından henüz kapsanmayan sipariş giderlerini kapsar. Bir siparişin toplamı bağlılık programı veya hediye kartı kredileri tarafından karşılanacaksa, ödeme modülü gizlenir ve müşteri siparişi bu modül olmadan verebilir.

Adyen ödeme bağlayıcısı güçlü müşteri kimlik doğrulamasını (SCA) da destekler. Avrupa Birliği (AB) Ödeme Hizmetleri Yönergesi 2.0 (PSD2.0), çevrimiçi alışverişçilerin elektronik ödeme yöntemi kullandıklarında çevrimiçi alışveriş deneyimlerinin dışında kimlik doğrulamasının yapılmasını gerektirir. Ödeme akışı sırasında, müşteriler kendi bankacılık sitesine yönlendirilir. Ardından, kimlik doğrulamasından sonra yeniden Commerce ödeme akışına yönlendirilir. Bu yeniden yönlendirme sırasında, bir müşterinin ödeme akışına girdiği bilgiler (örneğin, sevkiyat adresi, teslimat seçenekleri, hediye kartı bilgileri ve bağlılık programı bilgileri) kalır. Bu özelliği etkinleştirmeden önce, SCA için ödeme bağlayıcısının Commerce Headquarters'da yapılandırılması gerekir. Daha fazla bilgi için bkz. [Adyen kullanarak Güçlü Müşteri Kimlik Doğrulaması](adyen_redirect.md).

> [!NOTE]
> Adyen ödeme Bağlayıcısı için, ödeme modülündeki iFrame modülü ancak, adyen URL'sini sitenizin izin verilenler listesine eklediğinizde oluşturulabilir. Bu adımı tamamlamak için, **\*.adyen.com** öğesini sitenizin içerik güvenlik ilkesinin **child-src** , **connect-src** , **img-src** , **script-src** ve **Style-src** yönergelerine ekleyin. Daha fazla bilgi için bkz. [İçerik Güvenlik İlkesini yönetme](manage-csp.md). 

Aşağıdaki resimde, ödeme sayfasındaki hediye kartı, bağlılık ve ödeme modülleri gösterilmektedir.

![Ödeme sayfasındaki hediye kartı, bağlılık ve ödeme modüllerini gösteren örnek](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>Ödeme modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Başlık | Başlık metni | Ödeme modülü için isteğe bağlı bir başlık. |
| iframe yüksekliği. | Piksel | Piksel cinsinden iframe yüksekliği. Yükseklik gerektiği gibi ayarlanabilir. |
| Fatura adresini göster | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, faturalama adresi ödeme modülü iframe içinde Adyen tarafından sunulur. **Yanlış** olarak ayarlanırsa, faturalama adresi Adyen tarafından işlenmez ve Commerce kullanıcısının ödeme sayfasında fatura adresini göstermek için bir modül yapılandırması gerekir. |
| Ödeme stilini geçersiz kıl | Geçişli Stil Sayfaları (CSS) kodu | Ödeme modülü bir iframe içinde barındırıldığından, sınırlı stil oluşturma yeteneği vardır. Bu özelliği kullanarak bazı stil özellikleri elde edebilirsiniz. Site stillerini geçersiz kılmak için CSS kodunu bu özelliğin değeri olarak yapıştırmanız gerekir. Site oluşturucu CSS geçersiz kılmaları ve stilleri bu modüle uygulanamaz. |

## <a name="billing-address"></a>Fatura adresi

Ödeme modülü müşterilerinin ödeme bilgileri için faturalama adresi sağlamasına olanak tanır. Ayrıca, fatura adresi olarak sevkiyat adresini kullanma olanağı sunarak ödeme akışının daha kolay ve hızlı olmasını sağlar. **Fatura adresini göster** özelliği **Yanlış** olarak ayarlanırsa, ödeme modülü ödeme sayfasında yapılandırılmalıdır.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Bir ödeme sayfasına ödeme modülü ekleme ve gerekli özellikleri ayarlama

Ödeme modülü yalnızca bir ödeme modülüne eklenebilir. Bir ödeme sayfası için ödeme modülü yapılandırmayla ilgili daha fazla bilgi için bkz. [Ödeme modülü](add-checkout-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Sepet modülü](add-cart-module.md)

[Sepet simgesi modülü](cart-icon-module.md)

[Ödeme modülü](add-checkout-module.md)

[Sevkiyat adresi modülü](ship-address-module.md)

[Teslimat seçenekleri modülü](delivery-options-module.md)

[Sipariş ayrıntıları modülü](order-confirmation-module.md)

[Hediye kartı modülü](add-giftcard.md)

[Adyen için Dynamics 365 Ödeme Bağlayıcısı](dev-itpro/adyen-connector.md)

[Adyen bağlayıcısı kullanan Güçlü Müşteri Kimlik Doğrulaması](adyen_redirect.md)
