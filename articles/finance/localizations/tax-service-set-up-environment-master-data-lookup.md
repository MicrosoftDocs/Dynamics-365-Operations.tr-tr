---
title: Ana veri arama için ortam ayarlama
description: Bu konu, Vergi Hesaplama ana veri arama işlevini kullanmak için ortamınızı nasıl ayarlayabileceğinizi açıklamaktadır.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e4aa941c57e8c31793d6db8ae87140cd1bb1a82b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021356"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Ana veri arama için ortam ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, Vergi Hesaplama ana veri arama işlevini kullanmak için ortamınızı nasıl ayarlayabileceğinizi açıklamaktadır.

1. Lifecycle Services'ta (LCS) Power Platform tümleştirmesi ayarlayın. Daha fazla bilgi için bkz. [Microsoft Power Platform tümleştirmesi - Eklentilere genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Dynamics 365 Finance ve Microsoft Dataverse'i ayarlayın. Daha fazla bilgi için [Çözümü edinme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) ve [Kimlik doğrulaması ve yetkilendirme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Aşağıdaki varlıkları ayarlayın. Daha fazla bilgi için bkz. [Sanal varlıkları etkinleştirme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).
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
4. Dynamics 365 Regulatory Configuration Service'ı (RCS) kurun. 
5. Aşağıdaki özelliklerin denemesinin etkinleştirilmesi için Microsoft'a bir servis isteği oluşturun:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. **Özellik yönetimi** çalışma alanına gidin ve aşağıdaki özellikleri etkinleştirin:

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
