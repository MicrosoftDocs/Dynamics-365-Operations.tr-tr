---
title: Deneme ayarlama
description: Bu konuda, üçüncü taraf bir hizmette deneme ayarlamanın nasıl yapılacağı anlatılmaktadır.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0f7db0ce009f6ee7603952891aacfdc16fcde016
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930308"
---
# <a name="set-up-an-experiment"></a>Deneme ayarlama

[Bir varsayım tanımladıktan ve hangi başarı ölçümlerini kullanmak istediğinizi belirledikten](experimentation-identify.md) sonra üçüncü taraf hizmette denemenizi ayarlamanız gerekir. Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir. Ek adımlar ayrı konularda ele alınmıştır.

[ ![Deneme kullanıcı yolculuğu - Ayarlama](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Üçüncü taraf hizmetinde denemenizi ayarlama
Artık denemenizi çalıştırmak ve izlemek için üçüncü taraf hizmetinizi seçmiş ve deneme bağlayıcısını ayarlamanız olmanız gerekir. Bu önkoşullar [Dynamics 365 Commerce'ta deneme](experimentation-overview.md) bölümünde listelenir.

Üçüncü taraf hizmetinde denemenizi oluşturmak için gereken adımları izleyin. Bağlayıcı doğru yapılandırılırsa, üçüncü taraf hizmetinde ayarladığınız tüm denemelerin listesi, yaklaşık 5 dakika içindesite oluşturucuda görünür.

## <a name="set-up-your-success-metrics"></a>Başarı ölçümlerinizi ayarlama
Her deneme varyasyonların etkisini ölçmek ve varsayımı doğrulamak için ölçümlere gereksinim duyar. Dynamics 365 Commerce'taki canlı telemetri olaylarını kullanarak üçüncü taraf hizmetindeki ölçümlerin hesaplanmasını sağlamak için aşağıdaki adımları izleyin.

1. Site oluşturucuda sol gezinti bölmesinde **Sayfalar** sekmesini seçin ve sonra ölçümleri toplamak istediğiniz sayfayı seçin. 
1. İzlemek istediğiniz sayfanın veya modülün sağ özellik bölmesindeki **İzlenecek olay kimlikleri** bölümüne gidin.
1. **Görüntüle**'yi seçin. Tüm olay kimliklerinin listesi görüntülenir. İzlemek istediğiniz olayı kopyalayın ve olay anahtarını üçüncü taraf hizmetinde belirtilen konuma yapıştırın. Birden fazla olaya gereksinim duyarsanız, anahtarları tek tek kopyalayın. 
    - Sayfa görünümleri ve gelir izleme dahil tüm kullanılabilir olay ve özniteliklerin nasıl görüntüleneceğini öğrenmek için bkz. [Tanılama ve sorun giderme için Commerce bileşeni olayları](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).
1. Üçüncü taraf hizmetinde, ölçümleri izlemek için diğer adımları uygulayın.

## <a name="previous-step"></a>Önceki adım
[Varsayım tanımlama ve deneme için ölçümleri belirleme](experimentation-identify.md) 


## <a name="next-step"></a>Sonraki adım
[Deneme bağlama ve düzenleme](experimentation-connect-edit.md)
