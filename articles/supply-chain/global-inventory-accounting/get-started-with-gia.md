---
title: Global Stok Muhasebesi kullanmaya başlama
description: Bu konuda, Global Stok Muhasebesi kullanmaya nasıl başlayabileceğiniz açıklanmaktadır.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301710"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="32b1b-103">Global Stok Muhasebesi kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="32b1b-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="32b1b-104">Global Stok Muhasebesi, ayarlamış olduğunuz Global Stok Muhasebesi defterlerinde çoklu stok muhasebesi yapmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="32b1b-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="32b1b-105">Her bir Global Stok Muhasebesi genel defterini bir *kural* ile ilişkilendirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="32b1b-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="32b1b-106">Kural, aşağıdaki muhasebe ilkesi türlerinin bir koleksiyondur:</span><span class="sxs-lookup"><span data-stu-id="32b1b-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="32b1b-107">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="32b1b-107">Cost object</span></span>
- <span data-ttu-id="32b1b-108">Giriş ölçümü esası</span><span class="sxs-lookup"><span data-stu-id="32b1b-108">Input measurement basis</span></span>
- <span data-ttu-id="32b1b-109">Maliyet akışı varsayımı</span><span class="sxs-lookup"><span data-stu-id="32b1b-109">Cost flow assumption</span></span>
- <span data-ttu-id="32b1b-110">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="32b1b-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="32b1b-111">Global Stok Muhasebesi'ni açıktan sonra da Microsoft Dynamics 365 Supply Chain Management'ta stok muhasebesini her zamanki gibi yapmaya devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="32b1b-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="32b1b-112">Global Stok Muhasebesi bir eklentidir.</span><span class="sxs-lookup"><span data-stu-id="32b1b-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="32b1b-113">Özelliklerini kullanılabilir hale getirmek için Microsoft Dynamics Lifecycle Services'tan (LCS) yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="32b1b-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="32b1b-114">Üretim ortamları için etkinleştirmeden önce bir test ortamında değerlendirmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="32b1b-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="32b1b-115">Global Stok Muhasebesi, Supply Chain Management'ta yerleşik olan tüm maliyet yönetimi özelliklerini desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="32b1b-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="32b1b-116">Bu nedenle, şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="32b1b-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="32b1b-117">Global Stok Muhasebesi genel önizlemesi nasıl alınır</span><span class="sxs-lookup"><span data-stu-id="32b1b-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32b1b-118">Global Stok Muhasebesi kullanmak için, LCS etkin bir yüksek kullanılabilirlik ortamına sahip olmanız (OneBox ortamı değil) gerekir.</span><span class="sxs-lookup"><span data-stu-id="32b1b-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="32b1b-119">Ek olarak, Supply Chain Management sürüm 10.0.19 veya üstünü çalıştırıyor olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="32b1b-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="32b1b-120">Global Stok Muhasebesi genel önizlemesine kaydolmak için, LCS ortam kimliğinizi e-posta ile [Global Stok Muhasebesi ekibine gönderin](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="32b1b-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="32b1b-121">Program için onaylandıktan sonra, takım Global Stok Muhasebesi Beta anahtarı ve servis uç noktalarınızı içeren bir takip e-postası gönderir.</span><span class="sxs-lookup"><span data-stu-id="32b1b-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="32b1b-122">Beta anahtarını aldıktan sonra [eklentiyi yükleyebilirsiniz](#install).</span><span class="sxs-lookup"><span data-stu-id="32b1b-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="32b1b-123">Lisans</span><span class="sxs-lookup"><span data-stu-id="32b1b-123">Licensing</span></span>

<span data-ttu-id="32b1b-124">Global Stok Muhasebesi, Supply Chain Management için kullanılabilir olan stok muhasebesi standart özellikleri ile birlikte lisanslanır.</span><span class="sxs-lookup"><span data-stu-id="32b1b-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="32b1b-125">Global Stok Muhasebesini kullanmak için ek lisans satın almanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="32b1b-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="32b1b-126">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="32b1b-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="32b1b-127">Microsoft Power Platform entegrasyonunu ayarla</span><span class="sxs-lookup"><span data-stu-id="32b1b-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="32b1b-128">Eklenti işlevselliğini etkinleştirebilmek için, aşağıdaki adımları izleyerek Microsoft Power Platform ile tümleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="32b1b-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="32b1b-129">Hizmeti eklemek istediğiniz LCS ortamını açın.</span><span class="sxs-lookup"><span data-stu-id="32b1b-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="32b1b-130">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="32b1b-131">**Power Platform Tümleştirme** bölümünde **Kurulum** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="32b1b-132">**Power Platform ortam kurulumu** iletişim kutusunda, onay kutusunu seçin ve sonra **Kurulum**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="32b1b-133">Kurulum genellikle 60 ila 90 dakika arasında sürer.</span><span class="sxs-lookup"><span data-stu-id="32b1b-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="32b1b-134">Microsoft Power Platform ortam kurulumu tamamlandıktan sonra, sayfa ortamınızın adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32b1b-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="32b1b-135">Ayrıca, **Power Platform Tümleştirmesi** vbölümünde "Power Platform ortam kurulumu tamamlandı" ifadesi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="32b1b-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="32b1b-136">Global Stok Muhasebesi, çift yazma uygulaması gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="32b1b-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="32b1b-137">Daha fazla bilgi için bkz. [Ortam dağıtımından sonra ayarlama](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="32b1b-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="32b1b-138">Dataverse Kurma</span><span class="sxs-lookup"><span data-stu-id="32b1b-138">Set up Dataverse</span></span>

<span data-ttu-id="32b1b-139">Dataverse kurulumundan önce, aşağıdaki adımları izleyerek Global Stok Muhasebesi ilkelerini kiracınıza ekleyin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="32b1b-140">Wşndowa PowerShell v2 için Azure AD Modülünü [Graph için Azure Active Directory PowerShell'i Yükleme](/powershell/azure/active-directory/install-adv2) bölümünde açıklandığı gibi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="32b1b-141">Aşağıdaki PowerShell komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="32b1b-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="32b1b-142">Sonra, aşağıdaki adımları izleyerek, Dataverse'de Global Stok Muhasebesi için uygulama kullanıcıları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="32b1b-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="32b1b-143">Dataverse ortamınızın URL'sini açın.</span><span class="sxs-lookup"><span data-stu-id="32b1b-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="32b1b-144">**Gelişmiş Ayar \> Sistem \> Güvenlik \> Kullanıcılar**'a gidin ve bir uygulama kullanıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="32b1b-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="32b1b-145">Sayfa görünümünü **Uygulama Kullanıcıları** olarak değiştirmek için *Görünüm* alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="32b1b-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="32b1b-146">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-146">Select **New**.</span></span>
1. <span data-ttu-id="32b1b-147">**Uygulama Kimliği** alanını *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="32b1b-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="32b1b-148">**Rol Ata**'yı ve sonra *Sistem Yöneticisi*'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="32b1b-149">*Common Data Service Kullanıcısı* adlı bir rol varsa onu da seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="32b1b-150">Önceki adımları yineleyin, ancak **Uygulama kodu** alanını *5f58fc56-0202-49a8-ac9e-0946b049718b* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="32b1b-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="32b1b-151">Daha fazla bilgi için bkz. [Uygulama kullanıcısı oluşturma](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="32b1b-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="32b1b-152">Dataverse yüklemenizin varsayılan dili İngilizcedeğilse, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="32b1b-153">**Gelişmiş Ayar \> Yönetim \>Diller**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="32b1b-154">*İngilizce* (*LanguageCode=1033*) dilini ve **Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="32b1b-155">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="32b1b-155">Install the add-in</span></span>

<span data-ttu-id="32b1b-156">Global Stok Muhasebesi kullanabilmeniz için eklentiyi yüklemek üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="32b1b-157">Global Stok Muhasebesi genel önizlemesi için [kaydolma](#sign-up).</span><span class="sxs-lookup"><span data-stu-id="32b1b-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="32b1b-158">[LCS](https://lcs.dynamics.com/Logon/Index)'de oturum açın</span><span class="sxs-lookup"><span data-stu-id="32b1b-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="32b1b-159">**Özellik yönetimi önizlemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="32b1b-160">Artı işaretini (**+**) seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="32b1b-161">**Kod** alanına Global Stok Muhasebesi için eklenti beta anahtarınızı girin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="32b1b-162">(Kaydolduğunuzda Beta anahtarınızı e-posta ile almış olmanız gerekir.)</span><span class="sxs-lookup"><span data-stu-id="32b1b-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="32b1b-163">**Engellemeyi Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="32b1b-164">Hizmeti eklemek istediğiniz LCS ortamını açın.</span><span class="sxs-lookup"><span data-stu-id="32b1b-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="32b1b-165">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="32b1b-166">**Power Platform Tümleştirmesi**'ne gidin **Kurulum**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="32b1b-167">**Power Platform ortam kurulumu** iletişim kutusunda, onay kutusunu seçin ve sonra **Kurulum**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="32b1b-168">Kurulum genellikle 60 ila 90 dakika arasında sürer.</span><span class="sxs-lookup"><span data-stu-id="32b1b-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="32b1b-169">Microsoft Power Platform ortamı kurulumu tamamlandıktan sonra, **Ortam eklentileri** hızlı sekmesinde, **Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="32b1b-170">**Global stok muhasebesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="32b1b-171">Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="32b1b-172">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-172">Select **Install**.</span></span>
1. <span data-ttu-id="32b1b-173">**Ortam eklentileri** hızlı sekmesinde, Global Stok Muhasebesi'nin yüklenmekte olduğunu görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="32b1b-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="32b1b-174">Birkaç dakika sonra, durum *Yükleniyor* yerine *Yüklü* olarak değişmelidir.</span><span class="sxs-lookup"><span data-stu-id="32b1b-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="32b1b-175">(Bu değişikliği görmek için sayfayı yenilemeniz gerekebilir.) Bu noktada, Global Stok Muhasebesi kullanıma hazırdır.</span><span class="sxs-lookup"><span data-stu-id="32b1b-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="32b1b-176">Tümleştirmeyi ayarlama</span><span class="sxs-lookup"><span data-stu-id="32b1b-176">Set up the integration</span></span>

<span data-ttu-id="32b1b-177">Global Stok Muhasebesi ile Supply Chain Management arasındaki tümleştirmeyi ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="32b1b-178">Supply Chain Management'ta oturun açın.</span><span class="sxs-lookup"><span data-stu-id="32b1b-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="32b1b-179">**Sistem yönetimi \> Özellik Yönetimi** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="32b1b-180">**Güncelleştirmeleri denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="32b1b-181">**Tümü** sekmesinde, *Global stok muhasebesi* olarak adlandırılan özelliği arayın.</span><span class="sxs-lookup"><span data-stu-id="32b1b-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="32b1b-182">**Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="32b1b-183">**Global stok muhasebesi \> Kurulum \> Global stok muhasebesi parametreleri \> Tümleştirme parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="32b1b-184">**Veri hizmeti uç noktası** ve **Global stok muhasebesi uç noktası** alanlarında, önizleme Için kayıt olduğunuzda Global Stok Muhasebesi takımının gönderdiği e-postadaki URL'leri girin.</span><span class="sxs-lookup"><span data-stu-id="32b1b-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="32b1b-185">Global Stok Muhasebesi artık kullanıma hazır.</span><span class="sxs-lookup"><span data-stu-id="32b1b-185">Global Inventory Accounting is now ready to use.</span></span>
