---
title: Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesinin nasıl etkinleştirileceğini açıklamaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c4d596f27ffe15a97dc04e2ce7e85d21f8e7161f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908407"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="9ad30-103">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9ad30-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9ad30-104">Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesinin nasıl etkinleştirileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="9ad30-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="9ad30-105">Dynamics 365 Commerce'den gelen bilgilerle Teams'i sağlamak ve Teams ile satış noktası (POS) uygulaması arasındaki görev yönetimi özelliklerini eşlemek için Commerce Headquarters'da tümleştirme özelliklerini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9ad30-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="9ad30-106">Teams tümleştirmesini etkinleştirdiğinizde, verilerinizi Teams ile paylaşmayı kabul edersiniz.</span><span class="sxs-lookup"><span data-stu-id="9ad30-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="9ad30-107">Teams paylaşılan veriler Commerce verilerinizden farklı bir ülkede yer alabilir ve farklı uyumluluk standartlarına tabi olabilir.</span><span class="sxs-lookup"><span data-stu-id="9ad30-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="9ad30-108">Daha fazla bilgi için bkz. [Microsoft Güven Merkezi](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="9ad30-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="9ad30-109">Microsoft Gizlilik ilkeleri hakkında bilgi için, bkz. [Microsoft gizlilik bildirimi](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="9ad30-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="9ad30-110">Teams tümleştirmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9ad30-110">Enable Teams integration</span></span>

<span data-ttu-id="9ad30-111">Microsoft Teams ve Commerce tümleştirmesini etkinleştirmeden önce, Teams uygulamasını Azure portalında kiracınızla kaydettirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9ad30-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="9ad30-112">Teams uygulamasını kiracınızla Azure portalında kaydetmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="9ad30-113">Azure portalında kiracınız ile Teams uygulamasını kaydettirmek için [Hızlı Başlangıç: Microsoft Kimlik Platformunda bir uygulamayı kaydetme](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) konusundaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="9ad30-114">Kayıtlı uygulama için **genel bakış** sayfasından **uygulama (istemci) Kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="9ad30-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="9ad30-115">Bu değeri Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="9ad30-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="9ad30-116">Adım 1'de [bir sertifika eklediğinizde](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) girilen sertifika değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="9ad30-116">Copy the certificate value that was entered when you [added a certificate](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="9ad30-117">Sertifika, ortak anahtar veya uygulama anahtarı olarak da bilinir.</span><span class="sxs-lookup"><span data-stu-id="9ad30-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="9ad30-118">Bu değeri Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="9ad30-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="9ad30-119">Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9ad30-120">**Retail ve Commerce \> Kanal kurulumu \> Microsoft Teams tümleştirme yapılandırması** na gidin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="9ad30-121">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="9ad30-122">**Microsoft Teams tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9ad30-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="9ad30-123">**Uygulama kodu** ve **uygulama anahtarı** alanlarına, Azure portalında Teams uygulamasını kaydettirdiğinizde elde ettiğiniz değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="9ad30-124">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="9ad30-125">Aşağıdaki çizimde, Commerce Headquarters'da Teams tümleştirmesi yapılandırmasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9ad30-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Commerce Headquarters'da Teams tümleştirmesi yapılandırması](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="9ad30-127">Teams tümleştirmesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="9ad30-127">Disable Teams integration</span></span>

<span data-ttu-id="9ad30-128">Commerce Headquarters'da Microsoft Teams tümleştirmesini devre dışı bırakmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9ad30-129">**Retail ve Commerce \> Kanal kurulumu \> Microsoft Teams tümleştirme yapılandırması** na gidin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="9ad30-130">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="9ad30-131">**Microsoft Teams tümleştirmesini etkinleştir** seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9ad30-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="9ad30-132">**Uygulama kodu** ve **uygulama anahtarı** alanlarındaki değerleri temizleyin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="9ad30-133">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9ad30-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="9ad30-134">Commerce ile Teams tümleşmesini devre dışı bıraktıktan sonra, POS terminalleri Teams uygulamasından yayımlanan görevleri artık göstermez.</span><span class="sxs-lookup"><span data-stu-id="9ad30-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9ad30-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9ad30-135">Additional resources</span></span>

[<span data-ttu-id="9ad30-136">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış</span><span class="sxs-lookup"><span data-stu-id="9ad30-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="9ad30-137">Dynamics 365 Commerce'ten Microsoft Teams sağlama</span><span class="sxs-lookup"><span data-stu-id="9ad30-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="9ad30-138">Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme</span><span class="sxs-lookup"><span data-stu-id="9ad30-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="9ad30-139">Microsoft Teams'de kullanıcı rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="9ad30-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="9ad30-140">Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme</span><span class="sxs-lookup"><span data-stu-id="9ad30-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="9ad30-141">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS</span><span class="sxs-lookup"><span data-stu-id="9ad30-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
