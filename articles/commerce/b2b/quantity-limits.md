---
title: B2B e-ticaret siteleri için ürün miktarı sınırlarını ayarlama
description: Bu konu, işletmeler arası (B2B) e-ticaret siteleri için ürün miktarı sınırlarının nasıl ayarlanacağını açıklar.
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
ms.openlocfilehash: 2c8adaad2afee3b735c69a501d7949a807f4e770
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323392"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>B2B e-ticaret siteleri için ürün miktarı sınırlarını ayarlama

[!include [banner](../../includes/banner.md)]

Bu konu, işletmeler arası (B2B) e-ticaret siteleri için ürün miktarı sınırlarının nasıl ayarlanacağını açıklar.

Çoğu ürünün, gruplandırmasını tanımlayan ölçü birimi vardır. Gruplandırma ürünlerin nasıl satılabilir olduğunu etkiler. Bazı ürünlerde miktar için ek bir gruplama olabilir. Bu gruplandırma, ürünlerin ayrı birimler veya katları olarak satılıp satılmayacağını ve izlenmesi gereken minimum veya maksimum sipariş miktarı sınırı olup olmadığını belirler.

Miktar sınırlaması özelliği, Microsoft Dynamics 365 Commerce'te (varsayılan sipariş ayarları veya Commerce site oluşturucu site ayarlarında) konfigüre edilen minimum, maksimum, çoklu ve standart miktarların bir e-ticaret sitesine yerleştirilen müşteri siparişleri için geçerli olmasını sağlar. Ürün miktarı sınırları şu anda satış noktası (POS) ve çağrı merkezleri için desteklenmez.

Pek çok perakendeci, çeşitli ürün ve yerine getirme gereksinimlerini karşılamak için müşteri siparişleri (özel siparişler olarak da adlandırılır) seçeneği veya özel siparişler sağlar. Burada bazı tipik senaryolar vardır:

- Bir müşteri belirli çeşitlerin çarpımlarının katları olarak satılmasını istiyor.
- Bir müşteri, ürünleri, müşterinin satın aldığı mağazadan başka bir konumda bulunan bir mağazadan teslim almak istiyor. Ancak, mağazaların ambalaj standartları çevrimiçi satış dağıtımı için ambalaj standartlarından farklıdır.
- Müşteri, satın alınabilecek kalemler için maksimum miktar sınırı olan bir sınırlı sürümde ürün satın almak istiyor.

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>Commerce Headquarters'da varsayılan sipariş ayarları özelliğini açma

Ürün miktar sınırlarını ayarlamadan önce, Commerce Headquarters'da varsayılan sipariş ayarları özelliği açık olmalıdır.

Varsayılan sipariş ayarları özelliğini etkinleştirmek için bu adımları izleyin.

1. **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. **Müşteri siparişinde Site ve Varsayılan sipariş ayarlarını destekle** özelliğini bulup seçin.
1. Sağ bölmenin alt kısmında **Şimdi etkinleştir**'i seçin. 

## <a name="define-quantity-settings"></a>Miktar ayarlarını tanımlama 

Miktar ayarlarını **Varsayılan sipariş ayarları** sayfasında tanımlayabilirsiniz.

Miktar ayarlarını tanımlamak için aşağıdaki adımları izleyin. 

1. Ürün **Perakende ve Ticaret \> Ürünler ve kategoriler \> Kategoriye göre serbest bırakılmış ürünler**'e gidin.
1. Sevk edilen ürünleri seçin.
1. Eylem Bölmesinde **Stoğu yönet** sekmesinde, **Sipariş ayarları** grubunda, **Varsayılan sipariş ayarları**'nı seçin. 
1. **Varsayılan sipariş ayarları** sayfasında, **Satış siparişi** hızlı sekmesinde, **Satış miktarı** bölümünde ürün satış miktarlarını ayarlayın:

    - **Çoklu** – Ürünün katları olarak satın alınabileceği miktar.
    - **Minimum Sipariş Miktarı** - Satın alınması gereken minimum ürün sayısı.
    - **Maksimum Sipariş Miktarı** - Satın alınabilecek maksimum ürün sayısı.
    - **Standart Sipariş Miktarı** – Ürün seçildiğinde otomatik olarak girilen varsayılan miktar.

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>Commerce site oluşturucuda B2B sipariş miktarı sınırları özelliğini açma

Commerce site oluşturucuda B2B sipariş miktarı sınırları özelliğini açmak için bu adımları izleyin.

1. **Site ayarları \> Uzantılar**'a gidin
1. **Sipariş Miktarı Sınırlarını Etkinleştir** altında, açılır menüden **B2B müşterileri için etkin**'i seçin. 

> [!NOTE] 
> Güncelleştirilen site oluşturucu ayarları yalnızca app.settings.json dosyası güncelleştirildikten sonra etkinleşir. Daha fazla bilgi için bkz. [SDK ve Modül kitaplığı güncelleştirmeleri](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Ek kaynaklar

[B2B e-ticaret sitesi ayarlama](set-up-b2b-site.md)

[Müşteri hiyerarşileri kullanarak B2B iş ortaklarını yönetme](partners-customer-hierarchies.md)

[B2B e-ticaret sitelerindeki iş ortağı kullanıcılarını yönetme](manage-b2b-users.md)

[B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
