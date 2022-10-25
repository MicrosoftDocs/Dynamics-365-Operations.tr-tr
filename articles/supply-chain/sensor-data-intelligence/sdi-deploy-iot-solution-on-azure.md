---
title: Azure'da IoT çözümü dağıtma
description: Sensör Veri Yönetim Bilgileri, Microsoft Azure'a bağlı sensörlerden gelen verileri kullanır. Bu makalede, Azure aboneliğinizde bir Nesnelerin İnterneti (IoT) çözümünün nasıl dağıtılacağı açıklanmaktadır.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5f0f49c0f7daaacb85b75dc11b9f015b6aa4e997
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689734"
---
# <a name="deploy-an-iot-solution-on-azure"></a>Azure'da IoT çözümü dağıtma

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Sensör Veri Yönetim Bilgileri, Microsoft Azure'a bağlı sensörlerden gelen verileri kullanır. Azure'un sensörlerinizden veri almasını ve bunları Dynamics 365 Supply Chain Management ile paylaşmasını sağlamak için Azure aboneliğinizde bir Nesnelerin İnterneti (IoT) çözümü dağıtmanız gerekir. Aşağıdaki mimari diyagram, çözüme ve bileşenlerine genel bir bakış sağlar.

![Sensör Veri Yönetim Bilgileri mimari diyagramı.](media/sdi-architecture.png "Sensör Veri Yönetim Bilgileri mimari diyagramı")

## <a name="video-instructions"></a>Video yönergeleri

Aşağıdaki videoda [Algılayıcı Veri Zekası özelliğinin nasıl açılacağı](sdi-enable-feature.md) ve gerekli Azure kaynaklarının nasıl dağıtılacağı gösterilmektedir. Aynı yönergeler, bu makalenin diğer bölümünde metin şeklinde sunulmuştur.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58g3I]

## <a name="procedure"></a>Prosedür

Gerekli kaynakları Azure'da dağıtmak için aşağıdaki adımları izleyin.

1. Supply Chain Management ortamınızda yönetici olarak oturum açın.
1. **Sistem yönetimi \> Kurulum \> Sensör Veri Yönetim Bilgileri \> Azure kaynaklarını dağıtma ve bağlama**'ya giderek dağıtım sihirbazını açın.
1. **Hoş Geldiniz** sayfasında, bilgileri okuyun ve ardından **İleri**'yi seçin.
1. **Örnek IoT çözümünü Azure'a dağıtma** sayfasında, bilgileri okuyun ve ardından **Yönergeler** bölümünde **Dağıt**'ı seçin.
1. Yeni bir tarayıcı sekmesi açılır ve Azure kaynaklarını dağıtabilmeniz için Azure portalına yönlendirilirsiniz. İstenirse Azure aboneliğinizin kimlik bilgilerinizi kullanarak oturum açın.
1. **Özel dağıtım** sayfasında, **Abonelik** alanında, aboneliğinizi seçin.
1. Kaynak grubu alanı altında, dağıtacağınız Azure bileşenleri için bir **Kaynak grubu** oluşturmak üzere **Yeni oluştur**'u seçin.
1. Görüntülenen açılan iletişim kutusundaki **Ad** alanına yeni kaynak grubu için bir ad girin (örneğin, *IoT-demo*). Daha sonra **Tamam**'ı seçin.
1. Aşağıdaki alanları ayarlayın:

    - **Kaynak grubu**: Yeni oluşturduğunuz kaynak grubunu seçin.
    - **Bölge**: İdeal olarak Supply Chain Management ortamınızın dağıtıldığı bölge olmak üzere bir bölge seçin. Azure bölgelerinin farklı fiyatlandırmalara sahip olduğunu unutmayın. [Sensör Veri Yönetim Bilgileri fiyat hesaplayıcısını](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68) kullanarak bölgeniz için tahmini maliyetleri görüntüleyebilirsiniz.
    - **Supply Chain Management ortam URL'si**: Supply Chain Management ortamınızın URL'sini girin.
    - **Mevcut Azure IoT Hub'ı yeniden kullanma**: Bu onay kutusunu boş bırakın.

1. **İleri: Gözden Geçir + Oluştur**'u seçin.
1. **Özel dağıtım** sayfasında, doğrulamanın geçtiğini doğrulayın ve ardından **Oluştur**'u seçin.
1. **Dağıtım devam ediyor** sayfası, dağıtımınızın ilerlemesini izler. Dağıtım işlemi 30 dakika sürebilir. **Dağıtım devam ediyor** sayfası dağıtımın tamamlandığını gösterdiğinde, grupta dağıtılan kaynakların listesini gösteren bir sayfa açmak için kaynak grubu adının bağlantısını seçin.
1. Kaynak listesinde, **Tür** alanının *Yönetilen Kimlik* olarak ayarlandığı kaydı bulun. **Ad** sütununda, kaynağın ayrıntılar sayfasını açmak için adı seçin.
1. **İstemci Kimliği** alanındaki değeri kopyalayın (örneğin, **Panoya kopyala** düğmesini seçerek).
1. Supply Chain Management'ın çalıştığı tarayıcı sekmesine geri dönün *fakat Azure portalının sekmesini kapatmayın*. **Örnek IoT çözümünü Azure'a dağıtma** sihirbazı sayfası hala açık olmalıdır. 
1. **Sonraki**'yi seçin.
1. **Azure kaynaklarını bağlayın** sayfasında, **Azure AD Uygulama istemci kimliği** alanına, kopyaladığınız **İstemci Kimliği** değerini yapıştırın.
1. Azure portalının açık olduğu tarayıcı sekmesine geri dönün, *ancak Supply Chain Management sekmesini kapatmayın*. Kaynağın ayrıntılar sayfası hala açık olmalıdır.
1. Yeni kaynak grubundaki kaynakların listesine dönmek için tarayıcının **Geri** düğmesini seçin.
1. Kaynak listesinde, **Tür** alanının *Redis için Azure Cache* olarak ayarlandığı kaydı bulun. **Ad** sütununda, kaynağın ayrıntılar sayfasını açmak için adı seçin.
1. Sol gezinti bölmesinde **Erişim anahtarları**'nı seçin.
1. **Erişim anahtarları** sayfasında, **Birincil bağlantı dizesi (StackExchange.Redis)** için gösterilen değeri kopyalayın (örneğin, **Panoya kopyala** düğmesini seçerek).
1. Supply Chain Management'ın çalıştığı tarayıcı sekmesine geri dönün. **Azure kaynaklarını bağlayın** sayfası hala açık olmalıdır.
1. **Redis ölçüm deposu bağlantı dizesi** alanına, kopyaladığınız **Birincil bağlantı dizesi (StackExchange.Redis)** değerini yapıştırın.
1. **Bitir**'i seçin.

Sensör Veri Yönetim Bilgileri için Azure kaynakları artık Azure aboneliğinizde dağıtılır.

> [!NOTE]
> İstediğiniz zaman, **Sensör Veri Yönetim Bilgileri parametreleri** sayfasını açarak Supply Chain Management'a kaydedilen bağlantı bilgilerini görüntüleyebilir veya düzenleyebilirsiniz. Daha fazla bilgi için bkz. [Sensör Veri Yönetim Bilgileri parametreleri](sdi-parameters.md).
