---
title: Dynamics 365 Commerce uygulamasında etki alanları
description: Bu konuda, etki alanlarının Microsoft Dynamics 365 Commerce uygulamasında nasıl yönetildiği açıklanmaktadır.
author: BrShoo
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 0a494a36d1d8fa55521c416efd4262d860e1a708
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022848"
---
# <a name="domains-in-dynamics-365-commerce"></a>Dynamics 365 Commerce uygulamasında etki alanları

[!include [banner](includes/banner.md)]

Bu konuda, etki alanlarının Microsoft Dynamics 365 Commerce uygulamasında nasıl yönetildiği açıklanmaktadır.

Etki alanları, bir web tarayıcısında Dynamics 365 Commerce sitelerinde gezinmek için kullanılan web adresleridir. Etki alanının yönetimini seçilen bir etki alanı adı sunucusu (DNS) sağlayıcısıyla denetleyebilirsiniz. Dynamics 365 Commerce site oluşturucusunda yayımlandığında bir siteye nasıl erişileceğini koordine etmek için etki alanlarına başvurulur. Bu konuda, Commerce site geliştirme ve başlatma yaşam döngüsü boyunca etki alanlarının nasıl yönetildiği ve başvurulduğu incelenir.

## <a name="provisioning-and-supported-host-names"></a>Hazırlama ve desteklenen ana bilgisayar adları

[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) içinde bir e-ticaret ortamı hazırlanırken, dağıtılmış e-ticaret ortamıyla ilişkilendirilecek etki alanlarını girmek için e-ticaret hazırlama ekranındaki **Desteklenen ana bilgisayar adları** kutusu kullanılır. Bu etki alanları, e-ticaret web sitelerinin barındırıldığı müşteri tarafındaki etki alanı adı sunucusu (DNS) adları olacaktır. Bu aşamada bir etki alanı girildiğinde, etki alanının trafiği Dynamics 365 Commerce uygulamasına yönlendirilmeye başlamaz. Etki alanının trafiği, yalnızca DNS CNAME kaydı etki alanı ile Commerce uç noktasını kullanacak şekilde güncelleştirildiğinde Commerce uç noktasına yönlendirilir.

> [!NOTE]
> **Desteklenen ana bilgisayar adları** kutusuna, noktalı virgüllerle ayırarak birden fazla etki alanı girilebilir.

Aşağıdaki resimde, **desteklenen ana bilgisayar adları kutusu** vurgulanmış olarak LCS e-Commerce hazırlama ekranı gösterilmektedir. 

![Vurgulanmış olarak **Desteklenen ana bilgisayar adları** kutusunun bulunduğu LCS e-Commerce hazırlama ekranı](./media/Domains_ProvisioningeCommerceScreen_publish.png)

Hazırlama işlemi oluşturulmaya başlandıysa, ortama ek etki alanları eklemek için bir servis isteği oluşturabilirsiniz. LCS içinde bir servis talebi oluşturmak için, ortamınızda **Destek \> Destek sorunları** bölümüne gidin ve **Bir olay gönderin** öğesini seçin.

## <a name="commerce-generated-urls"></a>Commerce tarafından oluşturulan URL'Ler

Bir Dynamics 365 Commerce e-ticaret ortamı hazırlanırken Commerce, ortam için çalışma adresi olacak bir URL oluşturur. Bu URL'ye, ortam hazırlandıktan sonra LCS'de gösterilen e-ticaret site bağlantısında başvurulur. Commerce tarafından oluşturulan bir URL, Commerce ortamı için e-ticaret kiracı adının LCS'de girildiği `https://<e-commerce tenant name>.commerce.dynamics.com` adresi şeklindedir.

Üretim sitesi ana bilgisayar adlarını, bir korumalı alan ortamında da kullanabilirsiniz. Bu seçenek, bir siteyi bir korumalı alan ortamından üretime kopyalayacaksanız ideal bir seçenektir.

## <a name="site-setup"></a>Site kurulumu

E-ticaret ortamınız hazırlandıktan sonra, sitenizi çalışma URL'siyle ilişkilendirmek için Commerce site oluşturucusunda sitenizi kurmanız gerekir.

Site oluşturucusunda ilk kez bir site kurarken, **Sitenizi kurun** iletişim kutusu açılır.

Aşağıdaki şekilde, site oluşturucusuna ilk kez eriştiğinizde "varsayılan" adlı bir site için **Sitenizi kurun** iletişim kutusu gösterilmektedir.

![**Sitenizi kurun** iletişim kutusu](./media/Domains_SetupyoursiteScreen.png)

**Bir etki alanı seçin** kutusu, LCS içindeki siteniz için sağlanan desteklenen ana bilgisayar adlarından birini site oluşturucusundaki sitenize ilişkilendirmenizi sağlar.

**Yol** kutusu boş bırakılabilir veya çalışma URL'nize yansıyacak başka bir yol dizesi eklenebilir. **Yol** kutusunu boş bırakmak, temel Commerce tarafından oluşturulan URL'yi, site oluşturucusunda kurulan siteyle ilişkilendirir. Yollar her site/etki alanı çifti için benzersiz olmalıdır. Seçili site ve etki alanı içinde, ortamdaki yalnızca bir site boş yolu kullanabilir veya benzersiz bir yol dizesiyle ilişkilendirilir. Site kurulumu sırasında **Yol** alanına eklenen tüm dizeler, web tarayıcısında siteye erişmek için kullanılan, Commerce tarafından üretilen temel URL'nin bir alt yolu olur.

> [!NOTE]
> Yol, site oluşturucusunun **Site ayarları \> Kanallar** yapılandırması bölümüne bir kanal eklerken **Eşleşme yolu** olarak da bilinir.

Örneğin, "xyz" adlı bir e-ticaret kiracısında site oluşturucusunda "Fabrikam" adlı bir siteniz varsa ve siteyi boş bir yolla ayarlarsanız, Commerce tarafından olarak oluşturulan temel URL'ye doğrudan giderek, bir web tarayıcısındaki yayınlanan site içeriğine erişebilirsiniz:

`https://xyz.commerce.dynamics.com`

Alternatif olarak, aynı sitenin kurulumu sırasında "fabrikam" yolunu eklediyseniz, aşağıdaki URL'yi kullanarak bir web tarayıcısında yayınlanan site içeriğine erişebilirsiniz:

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a>Sayfalar ve URL'Ler

Siteniz bir yolla oluşturulduktan sonra, site oluşturucusundaki sayfalarla ilişkilendirilmiş tüm URL'Ler, sitenin çalıştığı URL'de (Commerce tarafından oluşturulan URL'de veya Commerce tarafından oluşturulan URL ve yol) oluşturulur. **Yeni URL** iletişim kutusundaki listeden bir sayfa seçip bu sayfanın URL yolunu girerek, site oluşturucusunda yeni bir URL oluşturmak (**URL'ler /> + Yeni**) URL'yi seçili sayfayla ilişkilendirir. URL yolu değeri sayfaya erişmek için sitenin çalışma URL'sine eklenir ve site oluşturucusundaki **URL'ler** sayfasının URL listesinde `./<URL path>` olarak etiketlenir.

Aşağıdaki şekilde, URL yolunun vurgulandığı bir örnek bulunan site oluşturucusundaki **Yeni URL** iletişim kutusu gösterilir. 

![Site oluşturucusundaki **Yeni URL** iletişim kutusu](./media/Domains_PageSetup2a.png)

Aşağıdaki şekilde, listede URL yolunun vurgulandığı bir örnek bulunan site oluşturucusundaki **URL'ler** sayfası gösterilir.

![İlke akışında kullanıcı akışı seçeneğini çalıştır](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Site oluşturucusundaki etki alanları

Desteklenen ana bilgisayar adları değerleri, bir siteyi kurarken etki alanı olarak ilişkilendirilebilir. Etki alanı olarak desteklenen bir ana bilgisayar adı değeri seçerken, site oluşturucusunda başvurulan etki alanının görüntülendiğini görürsünüz. Bu etki alanı yalnızca Commerce ortamı içinde bulunan bir başvurudur, o etki alanının canlı trafiği henüz Dynamics 365 Commerce uygulamasına yönlendirilmez.

Site oluşturucusunda sitelerle çalışırken, iki farklı etki alanı ile kurulmuş iki siteniz varsa, bir tarayıcıda yayınlanan site içeriğine erişmek için, çalışma URL'nize **?domain=** özniteliğini ekleyebilirsiniz.

Örneğin, "xyz" ortamı hazırlandı ve site oluşturucusunda iki site oluşturulup ilişkilendirildi: Biri `www.fabrikam.com` etki alanına sahip ve diğeri `www.constoso.com` etki alanına sahip. Her site boş bir yol kullanarak kuruldu. Daha sonra bu iki siteye, **?domain=** özniteliğini kullanarak bir web tarayıcısından aşağıdaki gibi erişilebilir:
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

Birden çok etki alanı bulunan bir ortamda bir etki alanı sorgusu dizesi verilmediğinde, Commerce, verdiğiniz ilk etki alanını kullanır. Örneğin, site kurulumu sırasında ilk olarak "fabrikam" yolu sağlanmışsa, `https://xyz.commerce.dynamics.com` URL'si `www.fabrikam.com` için yayımlanan sitenin içerik sitesine erişmek amacıyla kullanılabilir.

## <a name="traffic-forwarding-in-production"></a>Üretimde trafiği yönlendirme

commerce.dynamics.com uç noktasının kendisi üzerindeki etki alanı sorgulama dizesi parametrelerini kullanarak birden çok etki alanı benzetimi yapabilirsiniz. Ancak, üretimde canlıya geçmeniz gerektiğinde, özel etki alanınıza ilişkin trafiği `<e-commerce tenant name>.commerce.dynamics.com` uç noktasına yönlendirmelisiniz.

`<e-commerce tenant name>.commerce.dynamics.com` uç noktası özel etki alanı güvenli yuva katmanlarını (SSL'ler) desteklemediğinden, front door hizmeti veya içerik teslim ağı (CDN) kullanarak özel etki alanları kurmanız gerekir. 

Bir front door hizmeti veya CDN kullanarak özel etki alanları ayarlamak için iki seçeneğiniz vardır:

- Ön uç trafiği yönetmek ve Commerce ortamınıza bağlamak için, Azure Front Door gibi bir front door hizmeti kurun. Bu, etki alanı ve sertifika yönetimi ve daha ayrıntılı güvenlik ilkeleri üzerinde daha fazla denetim sağlar.
- Commerce tarafından sağlanan Azure Front Door örneğini kullanın. Bu, etki alanı doğrulaması için Dynamics 365 Commerce ekibi ile eşgüdümlü eylemi ve üretim etki alanınız için SSL sertifikaları elde etmeyi gerektirir.

CDN hizmetinin doğrudan nasıl kurulacağı hakkında bilgi için, bkz. [İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md).

Commerce tarafından sağlanan Azure Front Door örneğini kullanmak için, Commerce katılım ekibinden CDN kurulum için bir servis isteği oluşturmanız gerekir. 

- Şirket adınızı, üretim etki alanınızı, ortam kimliğini ve üretim e-ticaret kiracı adını sağlamanız gerekir. 
- Bunun var olan bir etki alanı (halen etkin bir site için kullanılan) veya yeni bir etki alanı olup olmadığı onaylamanız gerekir. 
- Yeni bir etki alanı için, etki alanı doğrulaması ve SSL sertifikası tek bir adımda elde edilebilir. 
- Var olan bir web sitesine hizmet veren bir etki alanı için, etki alanı doğrulaması ve SSL sertifikası oluşturmak için çok adımlı bir işlem gerekir. Bu işlemde; birden çok sıralı adım içerdiği için, bir etki alanının canlıya geçmesi 7 çalışma günlük hizmet düzeyi anlaşması (SLA) vardır.

LCS içinde bir servis talebi oluşturmak için, ortamınızda **Destek \> Destek sorunları** bölümüne gidin ve **Bir olay gönderin** öğesini seçin.

> [!NOTE]
> SSL bulunan özel etki alanları yalnızca üretim ortamlarında desteklenir. Korumalı alan ve kullanıcı kabul testleri (UAT) gibi üretim dışı ortamlarda, web tarayıcısında yayınlanan içeriğe erişmek için Commerce tarafından oluşturulan URL'yi kullanın.

## <a name="ssl-certificate-process"></a>SSL sertifikası işlemi

Bir servis talebi oluşturulduğu zaman, Commerce ekibi aşağıdaki adımları sizinle koordine edecektir.

Yeni etki alanları için:
- Commerce ekibi, Azure Front Door örneğini (Commerce barındırmalı) kurar.
- Böylece Commerce ekibi özel etki alanınızı işaret etmek için CNAME kaydını sağlar.
- CNAME kaydı güncelleştirildikten sonra, Commerce tarafından barındırılan Azure Front Door örneği etki alanı sahipliğini doğrulayabilir ve SSL sertifikasını alabilir.

Var olan/etkin etki alanları için:
- Commerce ekibi, etki alanı DNS sağlayıcınızı sağlamak üzere `afdverify.<custom-domain>` CNAME kaydının eklenmesi konusunda sizi yönlendirecektir.
- Tamamlandığında, Commerce ekibi etki alanını Azure Front Door örneğine ekler ve etki alanı için DNS'ye eklenecek ek DNS TXT kayıtlarını sağlar.
- TXT kayıtları tamamlandıktan sonra, Commerce ekibi SSL sertifikasının kurulacağı etki alanı için Azure Front Door güncelleştirmelerini tamamlayacaktır.

## <a name="apex-domains"></a>Zirve etki alanları

Commerce tarafından sağlanan Azure Front Door örneği zirve etki alanlarını (alt etki alanı içermeyen kök etki alanları) desteklemez. Zirve etki alanları çözümlemek için bir IP adresi gerektirir ve Commerce Azure Front Door örneği yalnızca sanal uç noktalarda bulunur. Zirve bir etki alanı kullanmak için iki seçeneğiniz vardır:

- **Seçenek 1:** Zirve etki alanını bir "www" etki alanına yönlendirmek için DNS sağlayıcınızı kullanın. Örneğin, `www.fabrikam.com` Commerce tarafından barındırılan Azure Front Door örneğine işaret eden CNAME kaydının olduğu `www.fabrikam.com` adresine yönlendirilir.

- **Seçenek 2:** Zirve etki alanını barındırmak için kendi kendinize bir CDN/Front Door örneği kurun.

> [!NOTE]
> Azure Front Door kullanıyorsanız, aynı abonelikte bir Azure DNS'yi de ayarlamanız gerekir. Azure DNS'de barındırılan zirve etki alanı, bir diğer ad kaydı olarak Azure Front Door hizmetine işaret edebilir. Bu, zirve etki alanlarının her zaman bir IP adresine işaret etmesi gerektiğinden geçici bir çözümdür.

  ## <a name="additional-resources"></a>Ek kaynaklar

  [Yeni bir e-ticaret kiracısını dağıtma](deploy-ecommerce-site.md)

  [Çevrimiçi mağaza kanalı ayarlama](./channel-setup-online.md)

  [E-ticaret sitesi oluşturma](create-ecommerce-site.md)

  [Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme](associate-site-online-store.md)

  [robots.txt dosyalarını yönetme](manage-robots-txt-files.md)

  [URL yeniden yönlendirmelerini toplu olarak yükleme](upload-bulk-redirects.md)

  [Commerce'ta B2C kiracısı ayarlama](set-up-B2C-tenant.md)

  [Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)

  [Commerce ortamında birden fazla B2C kiracısı yapılandırma](configure-multi-B2C-tenants.md)

  [İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

  [Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]