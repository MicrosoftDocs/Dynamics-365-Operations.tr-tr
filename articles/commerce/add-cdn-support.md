---
title: İçerik teslim ağı (CDN) için destek ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce ortamınıza bir içerik teslim ağının (CDN) nasıl ekleneceği açıklanmaktadır.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf5a0da2803f985e6c0c04dd9916977397173d11
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001634"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>İçerik teslim ağı (CDN) için destek ekleme


[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce ortamınıza bir içerik teslim ağının (CDN) nasıl ekleneceği açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce uygulamasında bir e-ticaret ortamı kurduğunuzda, bunu CDN hizmetiyle çalışacak şekilde konfigüre edebilirsiniz. 

Özel etki alanınız e-ticaret ortamınız için sağlama işlemi sırasında etkinleştirilebilir. Alternatif olarak, bir servis talebini, sağlama işlemi tamamlandıktan sonra ayarlamak için kullanabilirsiniz. E-ticaret ortamı için sağlama işlemi, ortamla ilişkilendirilmiş bir ana bilgisayar adı oluşturur. Bu ana bilgisayar adının aşağıdaki biçimi vardır; burada *e-ticaret-kiracı-adı* ortamınızın adıdır:

&lt;e-ticaret-kiracı-adı&gt;.commerce.dynamics.com

Sağlama işlemi sırasında oluşturulan ana bilgisayar adı veya bitiş noktası, yalnızca. \*commerce.dynamics.com için bir güvenli yuva katmanı (SSL) sertifikasını destekler. Özel etki alanları için SSL'yi desteklemez. Bu nedenle, CDN'den özel etki alanları için SSL'yi sonlandırmalı ve CDN'den Commerce'in ürettiği ana bilgisayar adına veya bitiş noktasına iletme trafiğine son vermek zorundasınız. 

Ek olarak, Commerce *statikleri* (JavaScript veya geçişli stil sayfaları \[CSS\] dosyaları) Commerce tarafından üretilen bitiş noktasından (\*.commerce.dynamics.com) sunulur. Statikler, yalnızca Commerce tarafından oluşturulan ana bilgisayar adı veya bitiş noktası CDN'nin arkasına konulursa önbelleğe alınabilir.

## <a name="set-up-ssl"></a>SSL'yi ayarlama

SSL'nin ayarlandığını ve bu tür önbelleğe alınmış olduğunu garantilemek için, CDN'nizi, ortamınız için ticaret tarafından üretilen ana bilgisayar adıyla ilişkilendirilmiş olacak şekilde konfigüre etmelisiniz. Ayrıca, yalnızca statiği için aşağıdaki kalıbı da önbelleğe almalısınız: 

/\_msdyn365/\_scnr/\*

Sağlanan özel etki alanı ile Commerce ortamınızı hazırladıktan sonra veya hizmet isteği kullanarak ortamınız için özel etki alanı sağlamadıktan sonra, özel etki alanınızı Commerce'in oluşturduğu ana bilgisayar adına veya bitiş noktasına getirin.

Daha önce belirtildiği gibi, oluşturulan ana bilgisayar adı veya bitiş noktası yalnızca \*.commerce.dynamics.com için bir SSL sertifikasını destekliyor. Özel etki alanları için SSL'yi desteklemez.

## <a name="cdn-services"></a>CDN hizmetleri

Herhangi bir CDN hizmeti, bir Commerce ortamıyla kullanılabilir. Burada iki örnek verilmiştir:

- **Microsoft Azure Ön kapı hizmeti** – Azure CDN çözümü. Azure ön kapı hizmeti hakkında daha fazla bilgi için [Azure ön kapı hizmeti belgelerine](https://docs.microsoft.com/azure/frontdoor/) bakın.
- **Akamai dinamik sitesi Hızlandırıcısı** – daha fazla bilgi için bkz. [Dinamik Site Hızlandırıcısı](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN kurulumu

CDN kurulum işlemi aşağıdaki adımlardan oluşur:

1. Ön uç ana bilgisayar ekleyin.
1. Bir arka uç havuzu yapılandırın.
1. Rota ve ön belleğe alma kurallarını ayarla.

### <a name="add-a-front-end-host"></a>Ön uç ana bilgisayar ekleyin

Tüm CDN hizmetleri kullanılabilir, ancak bu konudaki örnek için Azure ön kapı hizmeti kullanılır. 

Azure ön kapı hizmeti'ni kurma hakkında bilgi için bkz. [Hızlı başlangıç: yüksek oranda kullanılabilir bir Global Web uygulaması için ön kapı oluşturun.](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door)

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a>Azure ön kapı hizmeti'nde bir arka uç havuzu konfigüre et

Azure ön kapı hizmeti'nde bir arka uç havuzu konfigüre etmek için aşağıdaki adımları izleyin.

1. Arka uç havuzuna boş arka uç ana bilgisayar üstbilgisi olan özel bir ana bilgisayar olarak **&lt;ecom-kiracı-adı&gt;.commerce.dynamics.com** ekleyin.
1. **Sistem durumu araştırmaları** altında, **yol** alanında **/KeepAlive** girin.
1. **Aralıklar (saniye)** alanına, **255** girin.
1. **Yük dengelemesi** altında, varsayılan değerleri bırakın.

Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **bir arka uç Havuzu Ekle** iletişim kutusu gösterilmektedir.

![Arka uç havuzu iletişim kutusu Ekle](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Azure ön kapı hizmeti'nde kuralları ayarla

Azure ön kapı hizmeti'nde bir yönlendirme kuralı ayarlamak için, aşağıdaki adımları izleyin.

1. Rota kuralı ekleyin.
1. **Ad** alanına, **varsayılan** yazın.
1. **Kabul edilen iletişim kuralı** alanında, **http ve https**'yi seçin.
1. **Ön uç ana bilgisayarlar** alanında, **dynamics-ecom-tenant-name.azurefd.net** girin.
1. **Eşleştirilecek desenler** altında, üst alana şunu girin: **/\***.
1. **Rota Ayrıntıları** altında, **rota türü** seçeneğini **ileri** olarak ayarlayın.
1. **Arka uç havuzu** alanında, **ecom-arka uç**'yi seçin.
1. **İletme Protokolü** alan grubunda, **isteği eşleştir** seçeneğini seçin. 
1. **URL yeniden yazma** seçeneğini **devre dışı** olarak ayarlayın.
1. **Önbelleğe alma** seçeneğini **devre dışı** olarak ayarlayın.

Azure ön kapı hizmeti'nde bir önbelleğe alma kuralı ayarlamak için, aşağıdaki adımları izleyin.

1. Önbelleğe alma kuralı ekleyin.
1. **Ad** alanına, **statikler** yazın.
1. **Kabul edilen iletişim kuralı** alanında, **http ve https**'yi seçin.
1. **Ön uç ana bilgisayarlar** alanında, **dynamics-ecom-tenant-name.azurefd.net** girin.
1. **Eşleştirilecek desenler** altında, üst alana şunu girin: **/\_msdyn365/\_scnr/\***.
1. **Rota Ayrıntıları** altında, **rota türü** seçeneğini **ileri** olarak ayarlayın.
1. **Arka uç havuzu** alanında, **ecom-arka uç**'yi seçin.
1. **İletme Protokolü** alan grubunda, **isteği eşleştir** seçeneğini seçin.
1. **URL yeniden yazma** seçeneğini **devre dışı** olarak ayarlayın.
1. **Önbelleğe alma** seçeneğini **devre dışı** olarak ayarlayın.
1. **Sorgu dizesi önbelleğe alma davranışı** alanında, **her benzersiz URL 'yi önbelleğe al** 'ı seçin.
1. **Dinamik sıkıştırma** alan grubunda, **etkin** seçeneğini belirleyin.

Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **bir kural Ekle** iletişim kutusu gösterilmektedir.

![Kural Ekle iletişim kutusu](./media/CDN_CachingRule.png)

Bu başlangıç konfigürasyonu dağıtıldıktan sonra, özel etki alanınızı Azure ön kapı hizmeti yapılandırmasına eklemeniz gerekir. Özel etki alanı eklemek için (örneğin `www.fabrikam.com`), etki alanı için kurallı bir ad (CNAME) yapılandırmalısınız.

Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **CNAME yapılandırması** iletişim kutusu gösterilmektedir.

![CNAME Konfigürasyon iletişim kutusu](./media/CNAME_Configuration.png)

> [!NOTE]
> Kullanacağınız etki alanı zaten etkin ve canlı ise, test ayarlamak için bu etki alanını Azure ön kapı hizmeti ile etkinleştirme desteği ile iletişime geçin.

Sertifikayı yönetmek için Azure ön kapı hizmetini kullanabilir veya özel etki alanı için kendi sertifikanızı kullanabilirsiniz.

Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **Özel alan HTTPS** iletişim kutusu gösterilmektedir.

![Özel etki alanı HTTPS iletişim kutusu](./media/Custom_Domain_HTTPS.png)

CDN'niz şimdi Commerce sitenizde kullanılabilecek şekilde doğru konfigüre edilmelidir.

## <a name="additional-resources"></a>Ek kaynaklar

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[Yeni e-Ticaret sitesini dağıtma](deploy-ecommerce-site.md)

[e-Ticaret sitesi oluşturma](create-ecommerce-site.md)

[Çevrimiçi siteyi bir kanalla ilişkilendirme](associate-site-online-store.md)

[Robots.txt dosyalarını yönetme](manage-robots-txt-files.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)
