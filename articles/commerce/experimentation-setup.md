---
title: Deneme ayarlama
description: Bu makalede, üçüncü taraf bir hizmette deneme ayarlamanın nasıl yapılacağı anlatılmaktadır.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946210"
---
# <a name="set-up-an-experiment"></a>Deneme ayarlama

[Bir varsayım tanımladıktan ve hangi başarı ölçümlerini kullanmak istediğinizi belirledikten](experimentation-identify.md) sonra üçüncü taraf hizmette denemenizi ayarlamanız gerekir. Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir. Ek adımlar ayrı makalelerde ele alınmıştır.

[ ![Deneme kullanıcı yolculuğu - Ayarlama.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Üçüncü taraf hizmetinde denemenizi ayarlama
Artık denemenizi çalıştırmak ve izlemek için üçüncü taraf hizmetinizi seçmiş ve deneme bağlayıcısını ayarlamanız olmanız gerekir. Bu önkoşullar [Dynamics 365 Commerce'ta deneme](experimentation-overview.md) bölümünde listelenir.

Üçüncü taraf hizmetinde denemenizi oluşturmak için gereken adımları izleyin. Bağlayıcı doğru yapılandırılırsa, üçüncü taraf hizmetinde ayarladığınız tüm denemelerin listesi, yaklaşık 5 dakika içinde Commerce site oluşturucuda görünür.

## <a name="set-up-your-success-metrics"></a>Başarı ölçümlerinizi ayarlama
Her deneme varyasyonların etkisini ölçmek ve varsayımı doğrulamak için ölçümlere gereksinim duyar. Dynamics 365 Commerce'taki canlı telemetri olaylarını kullanarak üçüncü taraf hizmetindeki ölçümlerin hesaplanmasını sağlamak için aşağıdaki adımları izleyin.

Kullanıma hazır modüllerin başarı ölçümlerini ayarlamak için aşağıdaki adımları izleyin.

1. Commerce site oluşturucuda sol gezinti bölmesinde **Sayfalar** sekmesini seçin ve sonra ölçümleri toplamak istediğiniz sayfayı seçin. 
1. İzlemek istediğiniz sayfanın veya modülün sağ özellik bölmesindeki **İzlenecek olay kimlikleri** bölümüne gidin.
1. **Görüntüle**'yi seçin. Tüm tıklama olayı kimliklerinin listesi görüntülenir. İzlemek istediğiniz olayı kopyalayın ve ardından olay anahtarını üçüncü taraf hizmetinde belirtilen konuma yapıştırın. Birden fazla olaya gereksinim duyarsanız, anahtarları tek tek kopyalayın. 
1. Sayfa görüntülemeler için site oluşturucuda `.PageView` ifadesinin ekli olduğu sayfa adının SHA-256 karma değerini kullanın. Örneğin, `Homepage.PageView` için olay kimliği  `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9` olur.
1. Üçüncü taraf hizmetinde, ölçümleri izlemek için diğer adımları uygulayın.

Özel modül tıklamaları için tıklama olaylarını eklemek üzere aşağıdaki adımları izleyin:

1. Aşağıdaki işlevi kullanarak modül için bir **TelemetryContent** nesnesi hazırlayın. Bu işlev sayfa adı, modül adı ve SDK tarafından sağlanan varsayılan telemetri nesnesini giriş olarak alır.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Aşağıda bir örnek verilmiştir: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Yakalanması gereken bilgiler içeren yük verilerini oluşturun. Düğmeler ve diğer statik denetimler için "Hemen alışveriş yapın" veya "Arama yapın" gibi **etext** dahil edebilirsiniz. Ürün kartına tıklama gibi, tıklamalar içeren bileşenler için ürünün kayıt kimliği olan **recid** değerini veya ürün kimliğini gönderebilirsiniz.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    Statik denetimlere örnek olarak, düğme metin dizesini aşağıda gösterildiği gibi aktarın:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    Ürün tıklamalarına örnek olarak, aşağıda gösterildiği gibi ürün RecordID değerini aktarın:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Olayı kaydetmek için **OnClick** işlevini çağırın.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Aşağıda bir örnek verilmiştir:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Önceki adım
[Varsayım tanımlama ve deneme için ölçümleri belirleme](experimentation-identify.md) 


## <a name="next-step"></a>Sonraki adım
[Deneme bağlama ve düzenleme](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
