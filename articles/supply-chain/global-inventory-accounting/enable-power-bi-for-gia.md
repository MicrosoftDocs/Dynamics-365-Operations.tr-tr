---
title: Global Stok Muhasebesi için Power BI'yı etkinleştirme
description: Bu konuda, Global Stok Muhasebesi için Microsoft Power BI'yı nasıl etkinleştirebileceğiniz açıklanmaktadır.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273239"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="63d68-103">Global Stok Muhasebesi için Power BI'yı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="63d68-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="63d68-104">[PowerBI.com](https://powerbi.com/) hesabınızdaki kutucukları, panoları ve raporları Microsoft Dynamics 365 uygulaması çalışma alanınıza sabitleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="63d68-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="63d68-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="63d68-105">Prerequisites</span></span>

<span data-ttu-id="63d68-106">Power BI raporlamasını etkinleştirmeden önce aşağıdaki önkoşulların karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="63d68-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="63d68-107">Dynamics 365 uygulamasında sistem yöneticisi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="63d68-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="63d68-108">[PowerBI.com](https://powerbi.com/) hesabınız olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="63d68-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="63d68-109">Power BI hesabınızda en az bir pano ve bir rapor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="63d68-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="63d68-110">Azure Active Directory (Azure AD) hesabınız için yönetici olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="63d68-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="63d68-111">Azure AD etki alanının, [PowerBI.com](https://powerbi.com/) hesabınız için kullandığınız etki alanıyla aynı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="63d68-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="63d68-112">Ayar</span><span class="sxs-lookup"><span data-stu-id="63d68-112">Setup</span></span>

<span data-ttu-id="63d68-113">Power BI tümleştirmesini ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="63d68-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="63d68-114">[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="63d68-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="63d68-115">**Paylaşılan varlık kitaplığı**'na gidin, varlık türü olarak **Power BI rapor modeli**'ni seçin ve **Global Stok Muhasebesi** paketini indirin.</span><span class="sxs-lookup"><span data-stu-id="63d68-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="63d68-116">[PowerBI.com](https://app.powerbi.com/)'a giriş yapın ve aşağıdaki adımları izleyerek **Global Stok Muhasebesi** Power BI rapor dosyasını yükleyin:</span><span class="sxs-lookup"><span data-stu-id="63d68-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="63d68-117">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63d68-117">Select **New**.</span></span>
    1. <span data-ttu-id="63d68-118">**Dosya yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63d68-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="63d68-119">**Global Stok Muhasebesi** Power BI raporu dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="63d68-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="63d68-120">Aşağıdaki adımları izleyerek **Global Stok Muhasebesi** Power BI raporunu yapılandırın:</span><span class="sxs-lookup"><span data-stu-id="63d68-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="63d68-121">**Çalışma alanım**'a gidin, Global Stok Muhasebesi veri kümesini bulun ve **Seçenekler** menüsünde **Ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="63d68-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="63d68-122">**Global stok muhasebesi ayarları**'nda **Parametreler**'i genişletin ve tüm parametreleri gerektiği gibi güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="63d68-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="63d68-123">Uygulamayı, [PowerBI.com tümleştirmesini yapılandırma](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process) bölümünde açıklandığı gibi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="63d68-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="63d68-124">Aşağıdaki adımları izleyerek **Global Stok Muhasebesi** Power BI raporu dosyasını Dynamics 365 Supply Chain Management ile tümleştirin:</span><span class="sxs-lookup"><span data-stu-id="63d68-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="63d68-125">**Sistem yönetimi \> Kurulum \> PowerBI.com yapılandırması** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="63d68-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="63d68-126">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="63d68-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="63d68-127">**PowerBI.Com tümleştirmesini etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63d68-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="63d68-128">**Uygulama kodu** alanına uygulama kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="63d68-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="63d68-129">**Uygulama anahtarı** alanına uygulama anahtarını girin.</span><span class="sxs-lookup"><span data-stu-id="63d68-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="63d68-130">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63d68-130">Select **Save**.</span></span>

1. <span data-ttu-id="63d68-131">Power BI oturum açma iletişim kutusunun görünmesi için sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="63d68-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="63d68-132">**Seçenekler** sekmesinde **Rapor kataloğunu aç**'ı seçin ve ardından daha önce yüklediğiniz **Global Stok Muhasebesi** Power BI rapor dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="63d68-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="63d68-133">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="63d68-133">Refresh the page.</span></span> <span data-ttu-id="63d68-134">Raporunuzun eklendiğini görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="63d68-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="63d68-135">**Power BI raporları** altında **Global Stok Muhasebesi** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="63d68-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="63d68-136">Daha fazla bilgi için bkz. [PowerBI.com tümleştirmesini yapılandırma](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="63d68-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
