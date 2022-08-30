---
title: Customer Service için Çok Yönlü Kanal modülüyle Commerce Sohbeti
description: Bu makalede, Microsoft Dynamics 365 Commerce'de Customer Service için Çok Yönlü Kanalla Commerce Sohbeti modülü açıklanmaktadır.
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: e4a004b929138f0a04c19d6a94278cfad6e83303
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346406"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Customer Service için Çok Yönlü Kanal modülüyle Commerce Sohbeti

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'de *Customer Service için Çok Yönlü Kanalla Commerce Sohbeti modülü* açıklanmaktadır.

Commerce 10.0.29 sürümünde, Commerce modülü kitaplığına yeni Customer Service için Çok Yönlü Kanalla Commerce Sohbeti modülü eklenmiştir. Commerce sohbet özelliği e-ticaret müşterilerine, müşteri sorgularını ele almaya, müşteri hizmetleri sağlamaya ve Commerce müşterilerinin satışlarını kolaylaştırmaya yardımcı olmak amacıyla canlı temsilci desteği içeren Dynamics 365 Customer Service için Çok Yönlü Kanal sohbet yeteneklerini sunar.

Commerce sohbet özelliği, perakendecilerin şu hedeflere ulaşmasına olanak tanır:

- Müşteri tutmayı iyileştirmeye yardımcı olmak için müşterilerle kişiselleştirilmiş etkileşimi artırma.
- İnsan temsilci ve self servis sohbet botlarını tümleştirerek müşteri hizmetlerini geliştirme.
- İnsan temsilcilerin gerçek zamanlı müşteri profili, sipariş ve operasyonel iyileştirme sağlayan satınalma verileri ve etkileşim aracılığıyla deneyim kazanmasına yardımcı olma.
- Satışları artırmaya yardımcı olmak için müşteri memnuniyetini artırma.

Aşağıdaki yetenekler Commerce sohbet özelliğinin bir parçası olarak sunulur:

- Customer Service için Çok Yönlü Kanalla Commerce Sohbeti
- Dynamics 365 Customer Service için Çok Yönlü Kanal'daki temsilci deneyimine **Commerce Çağrı Merkezinin** uygulama sekmesi olarak eklenmesi

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Customer Service için Çok Yönlü Kanal önkoşulları

Önkoşul olarak, Customer Service için Çok Yönlü Kanal Yönetim arabirim öğesinde sohbeti yapılandırmanız ve Commerce sohbet deneyimini yapılandırmak için bazı parametreleri elde etmeniz gerekir. Yönergeler için bkz: [Sohbet kanalı yapılandırma](/dynamics365/customer-service/set-up-chat-widget).

Customer Service için Çok Yönlü Kanal Yönetim arabirim öğesinde sohbeti yapılandırdıktan sonra, aşağıdaki örneğe benzer bir betik alırsınız.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Bu betiği kopyalayın çünkü sohbet modülünü yapılandırmak için içerdiği değerlere gereksinim duyacaksınız.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Customer Service için Çok Yönlü Kanalla Commerce Sohbeti zorunlu alanları

Aşağıdaki tabloda, Customer Service için Çok Yönlü Kanalla Commerce Sohbeti modülünü yapılandırmak için Customer Service için Çok Yönlü Kanal Yönetim arabirimi öğesinden alınan gerekli betik değerleri gösterilmektedir.

| Arabirim öğesi özelliği | Açıklama |
| ------------- |--------------|
| Betik kaynağı | Sohbet arabirim öğesi betiğindeki **src** değeri. |
| Veri uygulama kimliği | Sohbet arabirim öğesi betiğindeki **data-app-id** değeri. |
| Veri kuruluş kimliği | Sohbet arabirim öğesi betiğindeki **data-org-id** değeri. |
| Veri kuruluş URL'si | Sohbet arabirim öğesi betiğindeki **data-org-url** değeri. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>E-ticaret siteniz için Commerce sohbet deneyimini yapılandırma

E-ticaret siteniz için sohbet deneyimini uygulamanın önerilen yollarından biri Customer Service için Çok Yönlü Kanalla Commerce Sohbeti modülünü e-ticaret sitesi sayfalarında kullanılan paylaşılan başlık parçasına eklemektir.

Sohbet modülünü Commerce site oluşturucuda sitenizin başlık parçasına eklemek için aşağıdaki adımları izleyin.

1. Siteniz için site oluşturucuda **Parçalar**'a gidin.
1. **Yeni**'yi seçin.
1. **Parça seçin** iletişim kutusunda **Customer Service için Çok Yönlü Kanalla Commerce Sohbeti** modülünü seçin, parça için ad seçin ve **Tamam**'ı seçin.
1. Ana hat görünümünde **Msdyn365 cs sohbet bağlayıcısı** yuvasını seçin.
1. Sağdaki **Sohbet özellikleri** bölmesinde şu adımları izleyin:

    1. **Betik kaynağı** alanına Customer Service için Çok Yönlü Kanal betiğinden aldığınız **src** değerini girin.
    1. **Veri uygulaması kimliği** alanına Customer Service için Çok Yönlü Kanal betiğinden aldığınız **data-app-id** değerini girin.
    1. **Veri kuruluş kimliği** alanına Customer Service için Çok Yönlü Kanal betiğinden aldığınız **data-org-id** değerini girin.
    1. **Veri kuruluş URL'si** alanına Customer Service için Çok Yönlü Kanal betiğinden aldığınız **data-org-url** değerini girin.

    ![Commerce site oluşturucuda bir Commerce Sohbet modülü parçası oluşturma.](media/Commerce-chat-creating-new-fragment.png)

1. **Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Parçalar**'a gidin ve siteniz için başlık parçasını açın.
1. **Varsayılan kapsayıcı** yuvasında, üç nokta (**...**) düğmesini seçin ve **Parça ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda daha önce oluşturduğunuz sohbet parçasını ve sonra **Tamam**'ı seçin.
1. **Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Customer Service için Çok Yönlü Kanal için Commerce headquarters'ı uygulama sekmesi olarak ekleme

Customer Service için Çok Yönlü Kanal'da Commerce headquarters için bir uygulama sekmesi ekleyebilirsiniz. Canlı temsilciler, müşteri ve satış siparişi bilgilerine ilişkin bağlamsam bilgiler içeren Dynamics 365 Commerce Customer Service modülüne kolayca erişmek amacıyla Customer Service için Çok Yönlü Kanal temsilci deneyimi kullanıcı arabirimini kullanabilirler. Ayrıca, müşteri hizmetleri temsilcileri yeni siparişler oluşturabilir, iade başlatabilir ve sipariş durumu bilgilerini doğrulayabilir.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Bir iFrame modülünde Commerce headquarters yükleyen yeni bir uygulama sekmesi oluşturma 

Bir iFrame modülünde Commerce headquarters yükleyen yeni bir uygulama sekmesi oluşturmak için şu adımları izleyin.

1. [Power Apps Maker Portal](https://make.powerapps.com)'ı açın.
1. Soldaki gezinti bölmesinde **Uygulamalar**'ı seçin.
1. **Müşteri Hizmetleri Yönetim Merkezi**'ni seçin.
1. **Temsilci deneyimi**'ne gidin.
1. **Uygulama sekmesi şablonları** için **Yönet**'i seçin.
1. **Üçüncü taraf web sitesi** türünde yeni bir uygulama sekmesi oluşturun. Yönergeler için bkz. [Uygulama sekmesi şablonlarını yönetme](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter).
1. **Parametreler** altında **url** parametresinin **Değer** alanına şu URL'yi girin. `<YourOrganizationHeadquartersURL>` ve `<LegalEntityname>` uygun değerlerle değiştirilir. Customer Service için çok yönlü kanal sohbet bağlamında **{AccountNumber}** öğesini okur. Bu nedenle, **{AccountNumber}** değerini olduğu gibi bırakın.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. **Veri** parametresinin **değer** alanını boş bırakın.

![Dynamics 365 Omnichannel Customer Service'de uygulama sekmesi oluşturma.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Dynamics 365 Customer Service için Çok Yönlü Kanal'da müşteri temsilcileri için yeni uygulama sekmesi etkinleştirme

Dynamics 365 Customer Service için Çok Yönlü Kanal'da müşteri temsilcileri için yeni uygulama sekmesi etkinleştirmek için şu adımları izleyin.
    
1. [Power Apps Maker Portal](https://make.powerapps.com)'ı açın.
1. Soldaki gezinti bölmesinde **Uygulamalar**'ı seçin.
1. **Müşteri Hizmetleri Yönetim Merkezi**'ni seçin.
1. **Müşteri desteği \> İş akışları**'na gidin.
1. Temsilcileriniz için oluşturduğunuz iş akışını açın ve sonra **Gelişmiş ayarlar** altında **Oturumlar varsayılanı**'nı seçin.
1. **Uygulama Sekmeleri** altında **Mevcut Uygulama Sekmesi Ekle**'yi seçin ve daha önce oluşturduğunuz yeni uygulama sekmesini ekleyin. Bu adım, iFrame modülüne Commerce headquarters yükleyen bir uygulama sekmesinin bir temsilci e-ticaret web sitenizden gelen arama aldığında görüntülenmesini sağlar.

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Dynamics 365 Customer Service için Çok Yönlü Kanal'da bağlam değişkenleri ekleme

Dynamics 365 Customer Service için Çok Yönlü Kanal'da bağlam değişkenleri eklemek için şu adımları izleyin.

1. [Power Apps Maker Portal](https://make.powerapps.com)'ı açın.
1. Soldaki gezinti bölmesinde **Uygulamalar**'ı seçin.
1. **Müşteri Hizmetleri Yönetim Merkezi**'ni seçin.
1. **Müşteri desteği \> İş akışları**'na gidin.
1. Temsilcileriniz için oluşturduğunuz iş akışını açın ve sonra **Gelişmiş ayarlar** altında **Bağlam değişkeni** bölümüne gidin.
1. **Düzenle**'yi seçin ve ardından **metin** türünün bağlam değişkeni olarak **AccountNumber** ekleyin. Bu değişken Commerce headquarters'ın eşleşen hesap numaralarına sahip müşteri bilgilerini yüklemesine yardımcı olur.

> [!NOTE]
> E-ticaret kanalından oturum açmış kullanıcıların e-posta adreslerini ve adlarını okumak isterseniz, **AccountNumber** bağlam değişkenine ek olarak **metin** türünün bağlan değişkenleri olarak **E-posta** ve **Ad** ekleyebilirsiniz.
