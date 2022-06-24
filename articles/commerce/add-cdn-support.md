---
title: İçerik teslim ağı (CDN) için destek ekleme
description: Bu makalede, Microsoft Dynamics 365 Commerce ortamınıza bir içerik teslim ağının (CDN) nasıl ekleneceği açıklanmaktadır.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a2ed8f66d447e1d9e890c0885fd20e9b55c66ac0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855888"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>İçerik teslim ağı (CDN) için destek ekleme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce ortamınıza bir içerik teslim ağının (CDN) nasıl ekleneceği açıklanmaktadır.

Dynamics 365 Commerce uygulamasında bir e-ticaret ortamı kurduğunuzda, bunu CDN hizmetiyle çalışacak şekilde konfigüre edebilirsiniz. 

Özel etki alanınız e-ticaret ortamınız için sağlama işlemi sırasında etkinleştirilebilir. Alternatif olarak, bir servis talebini, sağlama işlemi tamamlandıktan sonra ayarlamak için kullanabilirsiniz. E-ticaret ortamı için sağlama işlemi, ortamla ilişkilendirilmiş bir ana bilgisayar adı oluşturur. Bu ana bilgisayar adının aşağıdaki biçimi vardır; burada \<*e-commerce-tenant-name*\> ortamınızın adıdır:

&lt;e-ticaret-kiracı-adı&gt;.commerce.dynamics.com

Sağlama işlemi sırasında oluşturulan ana bilgisayar adı veya bitiş noktası, yalnızca. \*commerce.dynamics.com için bir güvenli yuva katmanı (SSL) sertifikasını destekler. Özel etki alanları için SSL'yi desteklemez. Bu nedenle, CDN'den özel etki alanları için SSL'yi sonlandırmalı ve CDN'den Commerce'in ürettiği ana bilgisayar adına veya bitiş noktasına iletme trafiğine son vermek zorundasınız. 

Ek olarak, Commerce *statikleri* (JavaScript veya geçişli stil sayfaları \[CSS\] dosyaları) Commerce tarafından üretilen bitiş noktasından (\*.commerce.dynamics.com) sunulur. Statikler, yalnızca Commerce tarafından oluşturulan ana bilgisayar adı veya bitiş noktası CDN'nin arkasına konulursa önbelleğe alınabilir.

## <a name="set-up-ssl"></a>SSL'u ayarla

Sağlanan özel etki alanı ile Commerce ortamınızı hazırladıktan sonra veya hizmet isteği kullanarak ortamınız için özel etki alanı sağladıktan sonra, DNS değişikliklerini planlamak için Commerce işe alım ekibiyle birlikte çalışmanız gerekir.

Daha önce belirtildiği gibi, oluşturulan ana bilgisayar adı veya bitiş noktası yalnızca \*.commerce.dynamics.com için bir SSL sertifikasını destekliyor. Özel etki alanları için SSL'yi desteklemez.

## <a name="cdn-services"></a>CDN hizmetleri

Herhangi bir CDN hizmeti, bir Commerce ortamıyla kullanılabilir. Burada iki örnek verilmiştir:

- **Microsoft Azure Ön kapı hizmeti** – Azure CDN çözümü. Azure ön kapı hizmeti hakkında daha fazla bilgi için [Azure ön kapı hizmeti belgelerine](/azure/frontdoor/) bakın.
- **Akamai dinamik sitesi Hızlandırıcısı** – daha fazla bilgi için bkz. [Dinamik Site Hızlandırıcısı](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN kurulumu

CDN kurulum işlemi aşağıdaki adımlardan oluşur:

1. Ön uç ana bilgisayar ekleyin.
1. Bir arka uç havuzu yapılandırın.
1. Yönlendirme için kural ayarlayın.

### <a name="add-a-front-end-host"></a>Ön uç ana bilgisayar ekleyin

Tüm CDN hizmetleri kullanılabilir ancak bu makaledeki örnek için Azure ön kapı hizmeti kullanılır. 

Azure ön kapı hizmeti'ni kurma hakkında bilgi için bkz. [Hızlı başlangıç: yüksek oranda kullanılabilir bir Global Web uygulaması için ön kapı oluşturun.](/azure/frontdoor/quickstart-create-front-door)

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Azure Front Door Service'te bir arka uç havuzu yapılandırın

Azure Front Door Service'te bir arka uç havuzu yapılandırmak için aşağıdaki adımları izleyin.

1. **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** öğesini, **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** ile aynı arka uç ana bilgisayar başlığına sahip özel bir ana bilgisayar olarak arka uç havuzuna ekleyin.
1. **Yük dengelemesi** altında, varsayılan değerleri bırakın.
1. Arka uç havuzu için sistem durumu denetimlerini devre dışı bırakın.

Aşağıdaki resimde, Azure Front Door Service'te arka uç ana bilgisayar adı girilmiş halde **Bir arka uç ekle** iletişim kutusu gösterilmektedir.

![Arka uç havuzu iletişim kutusu ekleme.](./media/CDN_BackendPool.png)

Aşağıdaki resimde, Azure Front Door Service'te varsayılan yük dengeleme değerleriyle birlikte **Bir arka uç havuzu ekle** iletişim kutusu gösterilmektedir.

![Arka uç havuzu iletişim kutusu ekleme devamı.](./media/CDN_BackendPool_2.png)

> [!NOTE]
> Commerce için kendi Azure Front Door Service'inizi kurarken **sistem durumu araştırmalarının** devre dışı olduğundan emin olun.


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


> [!WARNING]
> Kullanacağınız etki alanı zaten etkin ve yayında ise, sonraki adımlarınız için yardım almak üzere, [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/)'teki **Destek** kutucuğunda bir destek bileti oluşturun. Daha fazla bilgi için [Finans ve Operasyon uygulamaları veya Lifecycle Services (LCS) ile ilgili destek alma](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Etki alanınız yeniyse ve önceden varolan yayındaki bir etki alanı değilse, özel etki alanınızı Azure Front Door Service yapılandırmasına ekleyebilirsiniz. Bu, Azure Front Door örneği aracılığıyla web trafiğini sitenize yönlendirmeyi sağlar. Özel etki alanı eklemek için (örneğin `www.fabrikam.com`), etki alanı için kurallı bir ad (CNAME) yapılandırmalısınız.

Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **CNAME yapılandırması** iletişim kutusu gösterilmektedir.

![CNAME Yapılandırması iletişim kutusu.](./media/CNAME_Configuration.png)

Sertifikayı yönetmek için Azure ön kapı hizmetini kullanabilir veya özel etki alanı için kendi sertifikanızı kullanabilirsiniz.

Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **Özel alan HTTPS** iletişim kutusu gösterilmektedir.

![Özel etki alanı HTTPS iletişim kutusu.](./media/Custom_Domain_HTTPS.png)

Azure Front Door'unuza özel etki alanı eklemeyle ilgili ayrıntılı yönergeler için bkz. [Front Door'a özel etki alanı ekleme](/azure/frontdoor/front-door-custom-domain).

CDN'niz şimdi Commerce sitenizde kullanılabilecek şekilde doğru konfigüre edilmelidir.

## <a name="additional-resources"></a>Ek kaynaklar

[İçerik teslimi ağı uygulama seçenekleri](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]