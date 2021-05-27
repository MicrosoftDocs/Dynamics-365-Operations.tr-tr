---
title: Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesinin nasıl etkinleştirileceğini açıklamaktadır.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019847"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="f97e6-103">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f97e6-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f97e6-104">Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesinin nasıl etkinleştirileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f97e6-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="f97e6-105">Dynamics 365 Commerce'den gelen bilgilerle Teams'i sağlamak ve Teams ile satış noktası (POS) uygulaması arasındaki görev yönetimi özelliklerini eşlemek için Commerce Headquarters'da tümleştirme özelliklerini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f97e6-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="f97e6-106">Teams tümleştirmesini etkinleştirdiğinizde, verilerinizi Teams ile paylaşmayı kabul edersiniz.</span><span class="sxs-lookup"><span data-stu-id="f97e6-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="f97e6-107">Teams paylaşılan veriler Commerce verilerinizden farklı bir ülkede yer alabilir ve farklı uyumluluk standartlarına tabi olabilir.</span><span class="sxs-lookup"><span data-stu-id="f97e6-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="f97e6-108">Daha fazla bilgi için bkz. [Microsoft Güven Merkezi](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="f97e6-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="f97e6-109">Microsoft Gizlilik ilkeleri hakkında bilgi için, bkz. [Microsoft gizlilik bildirimi](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="f97e6-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="f97e6-110">Teams tümleştirmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f97e6-110">Enable Teams integration</span></span>

<span data-ttu-id="f97e6-111">Microsoft Teams ve Commerce tümleştirmesini etkinleştirmeden önce, Teams uygulamasını Azure portalında kiracınızla kaydettirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f97e6-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="f97e6-112">Teams uygulamasını kiracınızla Azure portalında kaydetmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="f97e6-113">Azure portalında kiracınız ile Teams uygulamasını kaydettirmek için [Hızlı Başlangıç: Microsoft Kimlik Platformunda bir uygulamayı kaydetme](/azure/active-directory/develop/quickstart-register-app) konusundaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="f97e6-114">Kayıtlı uygulama için **genel bakış** sayfasından **uygulama (istemci) Kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="f97e6-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="f97e6-115">Bu değeri Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="f97e6-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="f97e6-116">Adım 1'de [bir sertifika eklediğinizde](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) girilen sertifika değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="f97e6-116">Copy the certificate value that was entered when you [added a certificate](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="f97e6-117">Sertifika, ortak anahtar veya uygulama anahtarı olarak da bilinir.</span><span class="sxs-lookup"><span data-stu-id="f97e6-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="f97e6-118">Bu değeri Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="f97e6-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="f97e6-119">Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f97e6-120">**Retail ve Commerce \> Kanal kurulumu \> Microsoft Teams tümleştirme yapılandırması** na gidin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="f97e6-121">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="f97e6-122">**Microsoft Teams tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f97e6-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="f97e6-123">**Uygulama kodu** ve **uygulama anahtarı** alanlarına, Azure portalında Teams uygulamasını kaydettirdiğinizde elde ettiğiniz değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="f97e6-124">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="f97e6-125">Aşağıdaki çizimde, Commerce Headquarters'da Teams tümleştirmesi yapılandırmasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f97e6-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Commerce Headquarters'da Teams tümleştirmesi yapılandırması](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="f97e6-127">Teams tümleştirmesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="f97e6-127">Disable Teams integration</span></span>

<span data-ttu-id="f97e6-128">Commerce Headquarters'da Microsoft Teams tümleştirmesini devre dışı bırakmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f97e6-129">**Retail ve Commerce \> Kanal kurulumu \> Microsoft Teams tümleştirme yapılandırması** na gidin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="f97e6-130">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="f97e6-131">**Microsoft Teams tümleştirmesini etkinleştir** seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f97e6-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="f97e6-132">**Uygulama kodu** ve **uygulama anahtarı** alanlarındaki değerleri temizleyin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="f97e6-133">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f97e6-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="f97e6-134">Commerce ile Teams tümleşmesini devre dışı bıraktıktan sonra, POS terminalleri Teams uygulamasından yayımlanan görevleri artık göstermez.</span><span class="sxs-lookup"><span data-stu-id="f97e6-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f97e6-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f97e6-135">Additional resources</span></span>

[<span data-ttu-id="f97e6-136">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış</span><span class="sxs-lookup"><span data-stu-id="f97e6-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="f97e6-137">Dynamics 365 Commerce'ten Microsoft Teams sağlama</span><span class="sxs-lookup"><span data-stu-id="f97e6-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="f97e6-138">Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme</span><span class="sxs-lookup"><span data-stu-id="f97e6-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="f97e6-139">Microsoft Teams'de kullanıcı rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="f97e6-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="f97e6-140">Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme</span><span class="sxs-lookup"><span data-stu-id="f97e6-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="f97e6-141">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS</span><span class="sxs-lookup"><span data-stu-id="f97e6-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)