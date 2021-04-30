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
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="bfd6c-103">Ana veri arama için ortam ayarlama</span><span class="sxs-lookup"><span data-stu-id="bfd6c-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="bfd6c-104">Bu konu, Vergi Hesaplama ana veri arama işlevini kullanmak için ortamınızı nasıl ayarlayabileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="bfd6c-105">Lifecycle Services'ta (LCS) Power Platform tümleştirmesi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="bfd6c-106">Daha fazla bilgi için bkz. [Microsoft Power Platform tümleştirmesi - Eklentilere genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="bfd6c-107">Dynamics 365 Finance ve Microsoft Dataverse'i ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="bfd6c-108">Daha fazla bilgi için [Çözümü edinme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) ve [Kimlik doğrulaması ve yetkilendirme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="bfd6c-109">[Vergi hizmeti sanal varlığından](https://go.microsoft.com/fwlink/?linkid=2158160) *Önkoşul vergi hizmeti sanak varlığı çözümünü* içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="bfd6c-110">Dynamics 365 Regulatory Configuration Service'ı (RCS) kurun.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="bfd6c-111">Aşağıdaki özelliklerin denemesinin etkinleştirilmesi için Microsoft'a bir servis isteği oluşturun:</span><span class="sxs-lookup"><span data-stu-id="bfd6c-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="bfd6c-112">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="bfd6c-112">ERCdsFeature</span></span>
      - <span data-ttu-id="bfd6c-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="bfd6c-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="bfd6c-114">Finance'ta **Özellik yönetimi** çalışma alanına gidin ve aşağıdaki özellikleri etkinleştirin:</span><span class="sxs-lookup"><span data-stu-id="bfd6c-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="bfd6c-115">(Önizleme) Elektronik raporlama Dataverse veri kaynakları desteği</span><span class="sxs-lookup"><span data-stu-id="bfd6c-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="bfd6c-116">(Önizleme) Vergi Hizmeti Dataverse veri kaynakları desteği</span><span class="sxs-lookup"><span data-stu-id="bfd6c-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="bfd6c-117">(Önizleme) Genelleştirme özellikleri</span><span class="sxs-lookup"><span data-stu-id="bfd6c-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="bfd6c-118">Kiracı yönetici hesabı kullanarak RCS'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="bfd6c-119">**Elektronik raporlama** > **Bağlantılı uygulamalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="bfd6c-120">Kayıt eklemek için **Yeni**'yi seçin ve aşağıdaki alan bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="bfd6c-121">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="bfd6c-122">**Tür** alanında, **Dataverse**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="bfd6c-123">**Uygulama** alanına Dataverse URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="bfd6c-124">**Kiracı** alanına kiracınızı girin.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="bfd6c-125">**Özel URL** alanına Dataverse URL'nizi girin ve "/api/data/v9.1" ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="bfd6c-126">**Bağlantıyı denetle**'yi seçin ve bağlantı işlemini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="bfd6c-127">[![Bağlantıyı denetle düğmesi](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="bfd6c-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="bfd6c-128">**Elektronik raporlama** > **Vergi yapılandırmaları**'na gidin ve [Vergi yapılandırmaları](https://go.microsoft.com/fwlink/?linkid=2158352)'ndan veri yapılandırmalarını içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="bfd6c-129">[![Vergi yapılandırmaları sayfası, Vergi veri modeli ağacı](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="bfd6c-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="bfd6c-130">**Vergiye tabi belge modeli eşlemesine** veya Microsoft yapılandırması kullanıyorsanız **Dataverse Model Eşleme**'ye gidin ve **Bağlantılı uygulama** alanında, adım 7'de oluşturduğunuz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="bfd6c-131">**Model eşleme için varsayılan** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="bfd6c-132">[![Model eşleme sayfası](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="bfd6c-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
