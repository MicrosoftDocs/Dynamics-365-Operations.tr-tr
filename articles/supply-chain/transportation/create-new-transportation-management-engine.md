---
title: Yeni bir taşıma yönetimi altyapısı oluşturma
description: Bu konu, Dynamics 365 Supply Chain Management uygulamasında yeni bir taşıma yönetim altyapısının nasıl oluşturulacağını açıklar.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be52c6afb66e88b36f3b2cdf5af14e17b3d3005f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678136"
---
# <a name="create-a-new-transportation-management-engine"></a>Yeni bir taşıma yönetimi altyapısı oluşturma

[!include [banner](../includes/banner.md)]

Bu konu, Dynamics 365 Supply Chain Management uygulamasında yeni bir taşıma yönetim altyapısının nasıl oluşturulacağını açıklar. 

Nakliye yönetimi (TMS) motorları, Nakliye yönetimindeki nakliye oranlarının oluşturulması ve işlenmesi için kullanılan mantığı tanımlar. Supply Chain Management; oran, yoldaki saatler ve aktarma sırasında kesilecek bölge sayısı gibi farklı parametreleri hesaplayan birkaç farklı altyapı türü sağlar. Bu makalede, yeni bir TMS altyapısı oluşturmak ve dağıtmak ve daha sonra işlemdeki altyapıyı ayarlamak için Supply Chain Management geliştirme araçlarıyla birlikte Microsoft Visual Studio geliştirme ortamının nasıl kullanılacağı açıklanır. Altyapılar hakkında daha fazla bilgi için bkz. [Nakliye yönetimi motorları](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>Yeni TMS altyapısı oluşturma

Bu bölümde, TMS altyapı uygulaması bulunan bir sınıf kitaplığının nasıl oluşturulacağı ve bir Supply Chain Management modelinden nasıl referans bulunduğu açıklanmaktadır.

1. Yeni altyapılarınızı dağıtmak için, alt yapıları içeren bir modeliniz olmalıdır. **Dynamics 365** &gt; **Model Yönetimi** menüsünde yeni bir model oluşturmak için **Model oluştur** öğesine tıklayın. **Model oluştur** sihirbazının ilk sayfasında , modeli **TMSEngines** olarak adlandırın. 

   [![Model oluşturma.](./media/012.png)](./media/012.png)

2. Sonraki sayfada **Yeni paket oluştur**'u seçin. 

   [![Yeni paket oluşturma](./media/021.png)](./media/021.png)

3. Sonraki sayfada, başvurulacak **ApplicationSuite** modelini seçin. (**ApplicationPlatform** modeli önceden seçilmiştir.) 

   [![Referans olarak kullanılacak modeli seçme.](./media/032.png)](./media/032.png)

4. Yeni bir modelin oluşturulmasını onaylamak için bir sonraki sayfada **Son**'u tıklatın. 

   [![Model oluşturmayı tamamlama.](./media/042.png)](./media/042.png)

5. Yeni bir çözümde, yeni bir Supply Chain Management projesi oluşturun ve **TMSThirdParty** olarak adlandırın. Proje özelliklerinden, projenin modelini **TMSEngines**'a ayarlayın.
6. Çözümünüze yeni bir C\# sınıfı kitaplığı ekleyin ve bunu **ThirdPartyTMSEngines** olarak adlandırın.
7. ThirdPartyTMSEngines projesinde, Supply Chain Management'a özel derlemelere referanslar ekleyin:
   -   Referans alınacak X++ türlerine izin veren uygulama derlemeleri. Bu derlemeler, aşağıdaki konumlarda bulunabilir. \[Paketler kökü\], C:\\Paketler gibi tüm dağıtılan derlemelerin yerleştirildiği konumun yoludur.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Data, LINQ ve yardımcı işlevlere erişimi etkinleştiren çerçeve derlemeleri. Tüm bu derlemeler, \[Paketler kökü\]\\ bölmesinde bulunabilir.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   Çekirdek TMS derlemesi (alt yapıları içerir) ve TMS taban derlemesi (yardımcılar, sabitler, veri aktarım sınıfı tanımları, vb. içerir). Bu derlemeler, aşağıdaki konumlarda bulunabilir.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. ThirdPartyTMSEngines projesinde otomatik olarak oluşturulan C\# sınıfını, **SampleRatingEngine** olarak yeniden adlandırın.
9. Altyapıyı uygulayın. Bu örnekte bir oran altyapısı oluşturulmamız nedeniyle, oran alt yapıları için temel sınıftan devraldık. Temel sınıf, oran motoru arabiriminin çoğunu kullanır (**TMSFwkIRateEngine**). Yalnızca oran yöntemini uygulamamız gerekir. Bu örneğin basit kalmasını sağlamak için, bu yöntem 100 sabit kodlu bir oran kaydedecek şekilde yapılır. **TMSFwkIAccessorialEngine** gibi altyapı arabirimlerinden herhangi birini uygulayan altyapılar oluşturabilirsiniz. Tüm altyapı arabirimleri, X++ içinde tanımlanmıştır.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Çözümü oluşturun.
11. TMSThirdParty projesine yeni bir referans ekleyin. Referans, ThirdPartyTMSEngines projesine işaret etmelidir. Bitirdiğinizde, çözümünüz aşağıdaki gibi görünmelidir. 

    [![TMSThirdParty projesine başvuru içeren çözüm.](./media/052.png)](./media/052.png)

12. Çözümü oluşturun. Yeni kitaplığın, Uygulama Gezgini'nde **Referanslar** düğümünde göründüğünü doğrulayın. 

    [![Uygulama Gezgini'ndeki referans düğümünün yeni kitaplığı.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>TMS altyapısını paket olarak dağıtma

Üçüncü taraf TMS altyapılarını dağıtmanın bir yolu dağıtım paketidir. Üretim ortamında bu yaklaşım önerilir. Geliştirme ortamında, "Supply Chain Management'ta bir TMS altyapısı ayarlama" başlıklı sonraki kısımda anlatıldığı gibi birleştirmeleri el ile kopyalayabilirsiniz. Altyapıyı paket olarak dağıtmak için şu adımları izleyin.

1. **Dynamics 365** &gt; **Dağıt** menüsünde <strong>Dağıtım Paketi Oluştur</strong>'a tıklayın.
2. **Dağıtım Paketi Oluştur** iletişim kutusunda, TMSEngines modelini seçin ve paket dosyalarınızın depolanacağı yolu girin. 

   [![TMSEngines modelini seçme.](./media/071.png)](./media/071.png)

3. Artık paketi hedef ortama dağıtabilirsiniz. Öğretici için, bkz [Dağıtılabilir bir paketi yükleme](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>Supply Chain Management'ta TMS altyapısı ayarlama

Bu bölümde, TMS altyapısı kullanmak için Supply Chain Management'ın nasıl kurulacağını açıklar ve oluşturduğumuz alt yapının sevkiyat değerlendirme işleminde nasıl kullanıldığını gösterir. Bu bölümdeki örnek, USMF demo veri şirketi kullanır.

1. "Yeni bir TMS altyapısı oluşturma" bölümünde açıklandığı gibi yeni bir altyapı oluşturun.
2. Çözümünüzü oluşturun.
3. Elde edilen derlemeyi, Supply Chain Management sunucusunun \[AOSWebRoot\] bölmesi ikili konumuna kopyalayın. **Not:** Bu adım yalnızca geliştirme ortamında ilgilidir. Üretim ortamında bir dağıtım paketi üzerinden dağıtmanız gerekir. Yönergeler için, önceki "TMS altyapısını paket olarak dağıtma" başlıklı bölüme bakın.
4. Supply Chain Management'ta, **Oran alt yapıları** sayfasında yeni bir derecelendirme altyapısı oluşturun. Altyapı, uygulanan altyapı sınıf kitaplığını ve altyapı sınıfını oluşturarak üretilen altyapı derlemesini göstermelidir. 

   [![Oran altyapıları sayfasında yeni bir derecelendirme altyapısı oluşturma.](./media/081.png)](./media/081.png)

5. Örnek oran altyapısını kullanan bir sevkiyat taşıyıcısı oluşturun. Altyapımız veri kullanmadığından, oran yöneticisi atamanız gerekmez. 

   [![Yeni bir sevkiyat taşıyıcısı oluşturma.](./media/092.png)](./media/092.png)

6. **Oran rotası workbench'i** sayfasında, **Oran atölyesi**'ni tıklayın. Aşağıdaki ekran görüntüsünde gösterildiği gibi, SampleCarrier'da 100,00 oranını görmelisiniz. Bu örnekte, ambar 24'ten müşteri US-004'e bir rota için sevkiyat değerlendirme işlemi yapıyoruz. Ancak oran sabit kodlanmış olduğundan, her zaman bir 100,00 oranını görürsünüz.

   [![Rota çalışma ekranı oranı.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>İpuçları ve püf noktaları

- Supply Chain Management için geliştirme araçlarını kullanıyorsanız, çözümünüze yeni bir proje eklemek yararlı olur. Bu projeyi başlangıç projeniz olarak ayarlarsanız ve bir hata ayıklama oturumu başlatırsanız, aynı hata ayıklama oturumunda hem X+++ hem de C\# kodunda hata ayıklaması yapabilirsiniz.
- ThirdPartyTMSEngines projenizi her değiştirdiğinizde ve yeniden derlediğinizde, elde edilen derlemeyi ikili yere el ile kopyalamanız veya bir dağıtım paketi üzerinden dağıtmanız gerekir. Aksi durumda, eski bir derleme kullanarak çalışabilir.
- Supply Chain Management'ta TMS'e özel işler çalıştırdıktan sonra, İnternet Bilgileri Hizmetleri (IIS) çalışan işlemi, ThirdPartyTMSEngines derlemesini kilitleyebilir ve böylece derleme güncelleştirilemez. Bu durumda, w3svc işlemini yeniden başlatın.

### <a name="whitepaper"></a>Teknik inceleme

Daha fazla bilgi için, aşağıdaki teknik incelemeyi indirin (AX2012'yi desteklemek için yazılmıştır ancak Dynamics 365 Supply Chain Management için de geçerlidir)

- [Taşıma yönetimi altyapılarını uygulama ve dağıtma](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]