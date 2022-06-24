---
title: Ödeme modülü
description: Bu makale ödeme modülünü kapsamaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
ms.date: 04/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a89ca5dd4f46611e75faccd3213028750fa48d35
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850287"
---
# <a name="payment-module"></a>Ödeme modülü

[!include [banner](includes/banner.md)]

Bu makale ödeme modülünü kapsamaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.

Ödeme modülü, müşteriye bir kredi kartı veya banka kartı kullanarak sipariş ödemesi yapma olanağı tanır. Bu modül için ödeme tümleştirmesi, Adyen için Dynamics 365 Ödeme Bağlayıcısı tarafından sağlanır. Ödeme bağlayıcısını kurma ve yapılandırma hakkında daha fazla bilgi için bkz. [Adyen için Dynamics 365 Ödeme Bağlayıcısı](dev-itpro/adyen-connector.md).  

Commerce sürüm 10.0.14 itibariyle, müşterilerin PayPal'i kullanarak siparişlere ödeme yapmasına olanak tanımak amacıyla ödeme modülü de PayPal için Dynamics 365 ödeme konnektörü ile tümleştirilmiştir. Paypal için kurma ve Dynamics 365 Payment Connector'ı yapılandırma hakkında daha fazla bilgi için bkz. [Paypal için Dynamics 365 Ödeme Bağlayıcısı](paypal.md). 

## <a name="dynamics-365-payment-connector-for-adyen"></a>Adyen için Dynamics 365 Ödeme Bağlayıcısı 

Ödeme modülü, Adyen aracılığıyla HTML satır içi çerçevesinde (iframe) sunulan ödeme bilgilerini barındırır. Ödeme modülü, Adyen ödeme bilgilerini almak için Commerce Scale Unit ile etkileşime girer. Commerce Scale Unit etkileşiminin bir parçası olarak, ödeme modülü, fatura adres bilgilerinin Adyen yoluyla iframe'de veya ayrı bir modül olarak sunulmasını sağlar. Fabrikam temasında, fatura adresi ayrı bir modülde gösterilir. Adres satırları sevkiyat adresinin satırlarına benzeyecek şekilde işlenebileceğinden, bu yaklaşım daha fazla biçimlendirme esnekliği sağlar.

Ayrıca ödeme modülü de oturum açmış müşterilerin ödeme bilgilerini kaydetmesine olanak tanır. Ödeme bilgileri ve faturalama adresi, Adyen ödeme bağlayıcısı aracılığıyla kaydedilir ve yönetilir.

Ödeme modülü, bağlılık programı puanları veya hediye kartı tarafından henüz kapsanmayan sipariş giderlerini kapsar. Bir siparişin toplamı bağlılık programı veya hediye kartı kredileri tarafından karşılanacaksa, ödeme modülü gizlenir ve müşteri siparişi bu modül olmadan verebilir.

Adyen ödeme bağlayıcısı güçlü müşteri kimlik doğrulamasını (SCA) da destekler. Avrupa Birliği (AB) Revize Ödeme Hizmetleri Yönergesi (PSD2), çevrimiçi alışverişçilerin elektronik ödeme yöntemi kullandıklarında çevrimiçi alışveriş deneyimlerinin dışında kimlik doğrulamasının yapılmasını gerektirir. Kullanıma alma akışı sırasında, müşteriler bankacılık sitesine yönlendirilir ve bunları kimlik doğrulamasından sonra Commerce ödeme sağlama akışına yeniden yönlendirilir. Bu yeniden yönlendirme sırasında, bir müşterinin ödeme akışına girdiği bilgiler (örneğin, sevkiyat adresi, teslimat seçenekleri, hediye kartı bilgileri ve bağlılık programı bilgileri) kalır. Adyen ödeme bağlayıcısı özelliği etkinleştirmeden önce, SCA için ödeme bağlayıcısının Commerce Headquarters'da yapılandırılması gerekir. Daha fazla bilgi için bkz. [Adyen kullanarak Güçlü Müşteri Kimlik Doğrulaması](adyen_redirect.md). Bu özellik, Commerce sürüm 10.0.12'te etkinleştirildi.

> [!NOTE]
> Adyen ödeme Bağlayıcısı için, ödeme modülündeki iframe modülü ancak, adyen URL'sini sitenizin izin verilenler listesine eklediğinizde oluşturulabilir. Bu adımı tamamlamak için, **\*.adyen.com** öğesini sitenizin içerik güvenlik ilkesinin **child-src**, **connect-src**, **img-src**, **script-src** ve **Style-src** yönergelerine ekleyin. Daha fazla bilgi için bkz. [İçerik Güvenlik İlkesini yönetme](manage-csp.md). 

Aşağıdaki resimde, Adyen ödeme sayfasındaki hediye kartı, bağlılık ve ödeme modülleri gösterilmektedir.

![Ödeme sayfasındaki hediye kartı, bağlılık programı, Adyen ve ödeme modüllerini gösteren örnek.](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>PayPal için Dynamics 365 Payment Connector

Commerce Release 10.0.14 itibariyle, PayPal için Dynamics 365 ödeme Bağlayıcısı ile ödeme modülü de tümleşiktir. Ödeme bağlayıcısını kurma ve yapılandırma hakkında daha fazla bilgi için bkz. [Paypal için Dynamics 365 Ödeme Bağlayıcısı](paypal.md).
 
Kullanıma alma sayfasında, adyen ve PayPal bağlayıcılarının her ikisi birden yapılandırılmış olabilir. Ödeme modülü, hangi bağlayıcının çalışması gerektiğini belirlemeye yardımcı olan ek özelliklerle geliştirilmiştir. Ayrıntılar için **Desteklenen ödeme tipleri**'ne bakın ve **Birincil ödeme** aşağıdaki tabloda modülü özelliklerine bakın.
  
Ödeme modülü PayPal ödeme bağlayıcısını kullanacak şekilde konfigüre edildiğinde, kullanıma alma sayfasında bir PayPal düğmesi görüntülenir. Müşteri tarafından çağrıldığında, ödeme modülü PayPal bilgilerini içeren bir iframe'i işler. Müşteri, hareketini tamamlamak için oturum açabilir ve bu iframe içinde PayPal bilgilerini sunabilir. Bir müşteri PayPal ile ödeme yapmayı seçtiğinde, siparişteki kalan bakiye PayPal aracılığıyla ücretlendirilecektir.

Tüm faturalama ile ilgili bilgiler, iframe içinde PayPal tarafından işlendiğinden, PayPal ödeme Bağlayıcısı bir faturalama adresi modülü gerektirmiyor. Ancak sevkiyat adresi ve teslim seçenekleri modülleri gereklidir.

Aşağıdaki şekil, biri bir kullanıma alma sayfasında bulunan, diğeri de bir adyen ödeme Bağlayıcısı ve diğeri PayPal ödeme Bağlayıcısı ile konfigüre edilen iki ödeme modülü örneği göstermektedir.
![Ödeme sayfasındaki Adyen ve Paypal modüllerini gösteren örnek.](./media/ecommerce-paypal.png)

Aşağıdaki çizimde, PayPal düğmesi kullanılarak çağrılan PayPal iframe dosyasının bir örneği gösterilmektedir. 
![Kullanıma alma sayfasında Paypal iframe örneği.](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Ödeme modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Başlık | Başlık metni | Ödeme modülü için isteğe bağlı bir başlık. |
| iframe yüksekliği. | Piksel | Piksel cinsinden iframe yüksekliği. Yükseklik gerektiği gibi ayarlanabilir. |
| Fatura adresini göster | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, faturalama adresi ödeme modülü iframe içinde Adyen tarafından sunulur. **Yanlış** olarak ayarlanırsa, faturalama adresi Adyen tarafından işlenmez ve Commerce kullanıcısının ödeme sayfasında fatura adresini göstermek için bir modül yapılandırması gerekir. PayPal ödeme Bağlayıcısı için, faturalama adresi PayPal içinde tam olarak işlendiğinden, bu alanın bir etkisi olmaz. |
| Ödeme stilini geçersiz kıl | Geçişli Stil Sayfaları (CSS) kodu | Ödeme modülü bir iframe içinde barındırıldığından, sınırlı stil oluşturma yeteneği vardır. Bu özelliği kullanarak bazı stil özellikleri elde edebilirsiniz. Site stillerini geçersiz kılmak için CSS kodunu bu özelliğin değeri olarak yapıştırmanız gerekir. Site oluşturucu CSS geçersiz kılmaları ve stilleri bu modüle uygulanamaz. |
|Desteklenen ödeme türleri| Dize| Birden fazla ödeme Bağlayıcısı konfigüre edilmiş ise, Commerce Headquarters ödeme Bağlayıcısı konfigürasyonlarında tanımlandığı şekilde desteklenen ödeme tipi dizesini sağlamanız gerekir (aşağıdaki resme bakın). Boş bırakılırsa, varsayılan olarak adyen ödeme Bağlayıcısı 'nı alır. Commerce sürüm 10.0.14'e eklendi.|
|Birincil ödemedir|  **Doğru** veya **yanlış** | Değer **doğru** ise , kullanıma alma sayfasındaki birincil ödeme bağlayıcısından alınan tüm hata iletileri oluşturulur. Adyen ve PayPal ödeme bağlayıcıları yapılandırılırsa, adyen ile **doğru** değerini Commerce sürüm 10.0.14'e eklenmiş olarak ayarlayın.|
|Bağlayıcı kimliğini kullan| **Doğru** veya **yanlış** | Site için birden fazla ödeme bağlayıcısı yapılandırılırsa, bu özelliği kullanın. **Doğru** ise, bağlayıcılar ödeme bağıntısı için bağlayıcı kodunu kullanmalıdır.|
|iFrame için tarayıcıda ayarlanmış dil kodunu kullan|  **Doğru** veya **yanlış** | (Yalnızca Adyen) **Doğru** ise Adyen iFrame, site için yapılandırılan Commerce kanalının dil kodunu kullanmak yerine, dili site kullanıcısının tarayıcı bağlamına göre işler. Commerce sürüm 10.0.27'e eklendi.|

Aşağıdaki çizimde, Commerce Headquarters 'da ödeme Bağlayıcısı konfigürasyonunda "PayPal" olarak ayarlanan **Desteklenen ödeme tipleri** değerinin bir örneği gösterilmektedir.
![Commerce Headquarters'da desteklenen ödeme tipleri örneği.](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Fatura adresi

Bir faturalama adresi modülü, Adyen ödeme Bağlayıcısı fatura adres satırları sitenin geri kalanının görünümüyle aynı kadar uygun değilse, kullanıma alma sayfasında kullanılabilir. 

Ödeme modülü bir Adyen ödeme Bağlayıcısı ile tümleştirildiği zaman kullanıma alma sayfasında faturalama adresi modülünü kullanmak için varsayılan Adyen faturalama adresi yerine adanmış faturalama adresi modülü kullanılabilmesi için **fatura adresini göster** özelliğini **yanlış** olarak ayarlayın. Bu durumda, site yazarı, kullanıma alma sayfasına bir faturalama adresi modülü içermelidir. Adyen ödeme Bağlayıcısı, site kullanıcısı için adım sayısını en aza indirmek için sevkiyat adresini faturalama adresi olarak kullanabilme becerisine da izin verir.

Ödeme modüllerine benzer şekilde, Commerce sürüm 10.0.14 faturalama adres modülüne **desteklenen bir ödeme tipleri** özelliği eklenmiştir. Bu özelliğin değeri, ödeme modülünde birlikte çalışabildiklerinden emin olmak için belirtilen değerle özdeş olmalıdır. Adyen ödeme bağlayıcısı için, hem ödeme modülü hem de faturalama adresi modülü bu değeri boş bırakır (varsayılan il). PayPal bağlayıcısı için adanmış bir faturalama adresi modülü gerekli değildir. Diğer ödeme türü bağlayıcılar için, dize Commerce Headquarters'da konfigüre edilmiş olarak sağlanmalıdır.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Bir ödeme sayfasına ödeme modülü ekleme ve gerekli özellikleri ayarlama

Ödeme modülü yalnızca bir ödeme modülüne eklenebilir. Bir ödeme sayfası için ödeme modülü yapılandırmayla ilgili daha fazla bilgi için bkz. [Ödeme modülü](add-checkout-module.md).

## <a name="configure-the-adyen-and-paypal-payment-connectors-when-both-are-used"></a>Her ikisi de kullanıldığında, Adyen ve PayPal ödeme bağlayıcılarını konfigüre edin

Siteniz için hem Adyen hem de PayPal ödeme bağlayıcıları kullanılacaksa her bir bağlayıcı için ödeme modüllerini kullanıma alma modülüne eklemek ve sonra her modülün özelliklerini konfigüre etmek için Commerce site oluşturucuda aşağıdaki adımları izleyin.

1. PayPal ödeme modülünün özellikler bölmesinde şu adımları izleyin:

    1. **Desteklenen ödeme tipleri** özelliği alanında **PayPal** girin.
    1. **Birincil ödeme** özelliği için onay kutusunu temizleyin.
    1. **Bağlayıcı kodu kullan** özelliği için onay kutusunu işaretleyin.

1. Adyen ödeme modülünün özellikler bölmesinde şu adımları izleyin:

    1. **Desteklenen ödeme tipleri** özelliği alanını boş bırakın.
    1. **Birincil ödeme** özelliği için onay kutusunu seçin.
    1. **Bağlayıcı kodu kullan** özelliği için onay kutusunu işaretleyin.

> [!NOTE]
> Adyen ve PayPal bağlayıcılarını birlikte kullanılacak şekilde konfigüre ettiğinizde, **Adyen için Dynamics 365 Ödeme Bağlayıcısı** konfigürasyonu, çevrimiçi kanalın **Ödeme Hesapları** bağlayıcısı konfigürasyonunun Commerce Headquarters'ta ilk konumunda olmalıdır. Bağlayıcı sırasını onaylamak veya değiştirmek için, **Çevrimiçi mağazalar**'a gidin ve siteniz için kanalı seçin. Ardından, **Kurulum** sekmesinde, **Ödeme Hesapları** hızlı sekmesinde, **Bağlayıcı** altında, **Adyen için Dynamics 365 Ödeme Bağlayıcısı** konfigürasyonunun ilk konumda olduğundan (yani en üst satırda olduğundan) ve **PayPal için Dynamics 365 Ödeme Bağlayıcısı** konfigürasyonunun ikinci satırda olduğundan emin olun. Yeniden sıralamak için gereken bağlayıcıları ekleyin veya kaldırın.

## <a name="additional-resources"></a>Ek kaynaklar

[Alışveriş sepeti modülü](add-cart-module.md)

[Sepet simgesi modülü](cart-icon-module.md)

[Ödeme yapma modülü](add-checkout-module.md)

[Sevkiyat adresi modülü](ship-address-module.md)

[Teslimat seçenekleri modülü](delivery-options-module.md)

[Malzeme çekme bilgileri modülü](pickup-info-module.md)

[Sipariş ayrıntıları modülü](order-confirmation-module.md)

[Hediye kartı modülü](add-giftcard.md)

[Adyen için Dynamics 365 Ödeme Bağlayıcısı](dev-itpro/adyen-connector.md)

[PayPal için Dynamics 365 Payment Connector](paypal.md)

[Adyen bağlayıcısı kullanan Güçlü Müşteri Kimlik Doğrulaması](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
