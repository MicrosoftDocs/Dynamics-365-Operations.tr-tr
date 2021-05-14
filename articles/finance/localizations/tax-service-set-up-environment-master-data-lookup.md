---
title: Ana veri arama için ortam ayarlama
description: Bu konu, Vergi Hesaplama ana veri arama işlevini kullanmak için ortamınızı nasıl ayarlayabileceğinizi açıklamaktadır.
author: kai-cloud
ms.date: 04/21/2021
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
ms.openlocfilehash: 9f9b385df1db60b27698d90281c43fabb574af49
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924166"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="56a50-103">Ana veri arama için ortam ayarlama</span><span class="sxs-lookup"><span data-stu-id="56a50-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56a50-104">Bu konu, Vergi Hesaplama ana veri arama işlevini kullanmak için ortamınızı nasıl ayarlayabileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="56a50-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="56a50-105">Lifecycle Services'ta (LCS) Power Platform tümleştirmesi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="56a50-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="56a50-106">Daha fazla bilgi için bkz. [Microsoft Power Platform tümleştirmesi - Eklentilere genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="56a50-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="56a50-107">Dynamics 365 Finance ve Microsoft Dataverse'i ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="56a50-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="56a50-108">Daha fazla bilgi için [Çözümü edinme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) ve [Kimlik doğrulaması ve yetkilendirme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="56a50-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="56a50-109">Aşağıdaki varlıkları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="56a50-109">Set up the following entities.</span></span> <span data-ttu-id="56a50-110">Daha fazla bilgi için bkz. [Sanal varlıkları etkinleştirme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="56a50-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="56a50-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="56a50-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="56a50-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="56a50-112">CurrencyEntity</span></span>
      - <span data-ttu-id="56a50-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="56a50-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="56a50-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="56a50-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="56a50-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="56a50-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="56a50-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="56a50-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="56a50-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="56a50-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="56a50-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="56a50-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="56a50-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="56a50-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="56a50-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="56a50-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="56a50-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="56a50-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="56a50-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="56a50-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="56a50-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="56a50-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="56a50-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="56a50-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="56a50-125">Dynamics 365 Regulatory Configuration Service'ı (RCS) kurun.</span><span class="sxs-lookup"><span data-stu-id="56a50-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="56a50-126">Aşağıdaki özelliklerin denemesinin etkinleştirilmesi için Microsoft'a bir servis isteği oluşturun:</span><span class="sxs-lookup"><span data-stu-id="56a50-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="56a50-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="56a50-127">ERCdsFeature</span></span>
      - <span data-ttu-id="56a50-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="56a50-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="56a50-129">**Özellik yönetimi** çalışma alanına gidin ve aşağıdaki özellikleri etkinleştirin:</span><span class="sxs-lookup"><span data-stu-id="56a50-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="56a50-130">(Önizleme) Elektronik raporlama Dataverse veri kaynakları desteği</span><span class="sxs-lookup"><span data-stu-id="56a50-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="56a50-131">(Önizleme) Vergi Hizmeti Dataverse veri kaynakları desteği</span><span class="sxs-lookup"><span data-stu-id="56a50-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="56a50-132">(Önizleme) Genelleştirme özellikleri</span><span class="sxs-lookup"><span data-stu-id="56a50-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="56a50-133">Kiracı yönetici hesabı kullanarak RCS'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="56a50-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="56a50-134">**Elektronik raporlama** > **Bağlantılı uygulamalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="56a50-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="56a50-135">Kayıt eklemek için **Yeni**'yi seçin ve aşağıdaki alan bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="56a50-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="56a50-136">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="56a50-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="56a50-137">**Tür** alanında, **Dataverse**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="56a50-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="56a50-138">**Uygulama** alanına Dataverse URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="56a50-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="56a50-139">**Kiracı** alanına kiracınızı girin.</span><span class="sxs-lookup"><span data-stu-id="56a50-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="56a50-140">**Özel URL** alanına Dataverse URL'nizi girin ve "/api/data/v9.1" ekleyin.</span><span class="sxs-lookup"><span data-stu-id="56a50-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="56a50-141">**Bağlantıyı denetle**'yi seçin ve bağlantı işlemini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="56a50-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="56a50-142">[![Bağlantıyı denetle düğmesi](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="56a50-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="56a50-143">**Elektronik raporlama** > **Vergi yapılandırmaları**'na gidin ve [Vergi yapılandırmaları](https://go.microsoft.com/fwlink/?linkid=2158352)'ndan veri yapılandırmalarını içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="56a50-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="56a50-144">[![Vergi yapılandırmaları sayfası, Vergi veri modeli ağacı](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="56a50-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="56a50-145">**Vergiye tabi belge modeli eşlemesine** veya Microsoft yapılandırması kullanıyorsanız **Dataverse Model Eşleme**'ye gidin ve **Bağlantılı uygulama** alanında, adım 7'de oluşturduğunuz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="56a50-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="56a50-146">**Model eşleme için varsayılan** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="56a50-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="56a50-147">[![Model eşleme sayfası](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="56a50-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
