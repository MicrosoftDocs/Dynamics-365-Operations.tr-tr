---
title: Vergi hesaplama konfigürasyonu için master veri aramasını etkinleştir
description: Bu konu, vergi hesaplama ana veri arama işlevini nasıl etkinleştirebileceğinizi ve kurabileceğinizi açıklamaktadır.
author: kai-cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7640144b1687fc64e55f659d49cdb0817c17294a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686725"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Vergi hesaplama konfigürasyonu için master veri aramasını etkinleştir 

[!include [banner](../includes/banner.md)]

Bu konu, vergi hesaplama ana veri arama işlevini nasıl etkinleştirebileceğinizi ve kurabileceğinizi açıklamaktadır. **Tüzel kişilik**, **Satıcı hesabı**, **Madde kodu** ve **Teslim koşulu** gibi alanlar için vergi hesaplama yapılandırmasındaki değerleri seçmek üzere bir açılan liste kullanılabilir. Bu değerler, bağlantılı Microsoft Dynamics 365 Finance ortamından Microsoft Dataverse veri kaynağı kullanılarak alınır.

> [!NOTE] 
> Vergi hesaplama yöneticisi veri arama işlevi isteğe bağlı işlevselliktir. Regulatory Configuration Service'teki (RCS) **Vergi Hizmeti Dataverse veri kaynağı desteği** özelliğini devre dışı bırakırsanız aşağıdaki adımları atlayabilirsiniz. Ancak, bu durumda, açılan liste vergi hesaplama yapılandırmasında kullanılamaz.

1. Microsoft Dynamics Lifecycle Services'ta (LCS) Microsoft Power Platform tümleştirmesi ayarlayın. Daha fazla bilgi için bkz. [Microsoft Power Platform tümleştirmesi - Eklentilere genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Bu adımı tamamladıktan sonra, bir Microsoft Power Platform ortamın adı, **Power Platform tümleştirmesi** bölümünde görünür.
2. [Microsoft Power Platform yönetim merkezine](https://admin.powerplatform.microsoft.com/environments) gidin ve ortam adını seçin. Ortam URL'si sağlanır.
3. Dynamics 365 Finance ve Dataverse'ü ayarlayın. Daha fazla bilgi için [Sanal varlık çözümünü edinme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) ve [Kimlik doğrulaması ve yetkilendirme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. Aşağıdaki varlıkları ayarlayın. Daha fazla bilgi için bkz. [Microsoft Dataverse sanal varlıklarını etkinleştirme](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCityEntity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity

5. Regulatory Configuration Service (RCS) kurulumu. **Özellik yönetimi** çalışma alanını açın ve aşağıdaki özellikleri etkinleştirin:

    - Elektronik raporlama Dataverse veri kaynakları desteği
    - Vergi Hizmeti Dataverse veri kaynakları desteği
    - Globalleştirme özellikleri

6. Kiracı yönetici hesabı kullanarak RCS'de oturum açın.
7. **Elektronik raporlama** > **Bağlantılı uygulamalar**'a gidin. 
8. Kayıt eklemek için **Yeni**'yi seçin ve aşağıdaki alan bilgilerini girin. 

    - **Ad** alanına, bir ad girin.
    - **Tür** alanında, **Dataverse**'ü seçin.
    - **Uygulama** alanına Dataverse URL'nizi girin.
    - **Kiracı** alanına kiracınızı girin.
    - **Özel URL** alanına Dataverse URL'nizi girin ve "/api/data/v9.1" ekleyin.

9. **Bağlantıyı denetle**'yi seçin ve bağlantı işlemini tamamlayın. 

    [![Bağlantıyı denetle düğmesi.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. **Elektronik raporlama** > **Vergi yapılandırmaları**'na gidin ve [Vergi yapılandırmaları](https://go.microsoft.com/fwlink/?linkid=2158352)'ndan veri yapılandırmalarını içeri aktarın.

    [![Vergi yapılandırmaları sayfası, Vergi veri modeli ağacı.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. **Vergiye tabi belge modeli eşlemesine** veya Microsoft yapılandırması kullanıyorsanız **Dataverse Model Eşleme**'ye gidin ve **Bağlantılı uygulama** alanında, adım 7'de oluşturduğunuz kaydı seçin.
12. **Model eşleme için varsayılan** seçeneğini **Evet** olarak ayarlayın.

    [![Model eşleme sayfası.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
