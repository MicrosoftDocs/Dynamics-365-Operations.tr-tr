---
title: Ana veri arama için ortam ayarlama
description: Bu konu, Vergi Hesaplama ana veri arama işlevini kullanmak için ortamınızı nasıl ayarlayabileceğinizi açıklamaktadır.
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869106"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Ana veri arama için ortam ayarlama

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Bu konu, Vergi Hesaplama ana veri arama işlevini kullanmak için ortamınızı nasıl ayarlayabileceğinizi açıklamaktadır.

1. Lifecycle Services'ta (LCS) Power Platform tümleştirmesi ayarlayın. Daha fazla bilgi için bkz. [Microsoft Power Platform tümleştirmesi - Eklentilere genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Dynamics 365 Finance ve Microsoft Dataverse'i ayarlayın. Daha fazla bilgi için [Çözümü edinme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) ve [Kimlik doğrulaması ve yetkilendirme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. [Vergi hizmeti sanal varlığından](https://go.microsoft.com/fwlink/?linkid=2158160) *Önkoşul vergi hizmeti sanak varlığı çözümünü* içeri aktarın.
4. Dynamics 365 Regulatory Configuration Service'ı (RCS) kurun. 
5. Aşağıdaki özelliklerin denemesinin etkinleştirilmesi için Microsoft'a bir servis isteği oluşturun:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. Finance'ta **Özellik yönetimi** çalışma alanına gidin ve aşağıdaki özellikleri etkinleştirin:

      - (Önizleme) Elektronik raporlama Dataverse veri kaynakları desteği
      - (Önizleme) Vergi Hizmeti Dataverse veri kaynakları desteği
      - (Önizleme) Genelleştirme özellikleri

5. Kiracı yönetici hesabı kullanarak RCS'de oturum açın.
6. **Elektronik raporlama** > **Bağlantılı uygulamalar**'a gidin. 
7. Kayıt eklemek için **Yeni**'yi seçin ve aşağıdaki alan bilgilerini girin. 

   - **Ad** alanına, bir ad girin.
   - **Tür** alanında, **Dataverse**'ü seçin.
   - **Uygulama** alanına Dataverse URL'nizi girin.
   - **Kiracı** alanına kiracınızı girin.
   - **Özel URL** alanına Dataverse URL'nizi girin ve "/api/data/v9.1" ekleyin.

8. **Bağlantıyı denetle**'yi seçin ve bağlantı işlemini tamamlayın. 

   [![Bağlantıyı denetle düğmesi](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. **Elektronik raporlama** > **Vergi yapılandırmaları**'na gidin ve [Vergi yapılandırmaları](https://go.microsoft.com/fwlink/?linkid=2158352)'ndan veri yapılandırmalarını içeri aktarın.

   [![Vergi yapılandırmaları sayfası, Vergi veri modeli ağacı](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. **Vergiye tabi belge modeli eşlemesine** veya Microsoft yapılandırması kullanıyorsanız **Dataverse Model Eşleme**'ye gidin ve **Bağlantılı uygulama** alanında, adım 7'de oluşturduğunuz kaydı seçin.
11. **Model eşleme için varsayılan** seçeneğini **Evet** olarak ayarlayın.

   [![Model eşleme sayfası](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
