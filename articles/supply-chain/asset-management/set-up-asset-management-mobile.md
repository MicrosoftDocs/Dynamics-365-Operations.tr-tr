---
title: Kıymet yönetimi mobil çalışma alanını ayarlama
description: Bu konu, çalışanların kıymet yönetimi görevlerini gerçekleştirmek için kullanabileceği bir Kıymet yönetimi mobil çalışma alanı çalıştırmak için Microsoft Dynamics 365 Supply Chain Management ve Finance and Operations (Dynamics 365) mobil uygulamasını ayarlamayı açıklar.
author: johanhoffmann
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9c2410c50b5d289792e2cc364674e1e093653590
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033235"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="f35ef-103">Kıymet yönetimi mobil çalışma alanını ayarlama</span><span class="sxs-lookup"><span data-stu-id="f35ef-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f35ef-104">Bu konu, çalışanların kıymet yönetimi görevlerini gerçekleştirmek için kullanabileceği bir **Kıymet yönetimi** mobil çalışma alanı çalıştırmak için Microsoft Dynamics 365 Supply Chain Management ve Finance and Operations (Dynamics 365) mobil uygulamasını ayarlamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="f35ef-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="f35ef-105">Supply Chain Management'ta bakım görevlisi kullanıcılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="f35ef-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="f35ef-106">**Kıymet yönetimi** mobil çalışma alanına erişmesi gereken her bir kullanıcı için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f35ef-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="f35ef-107">Supply Chain Management'ta **İnsan kaynakları \> Çalışanlar**'a gidin ve ayarlamak istediğiniz kullanıcı için bir çalışan kaydının olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f35ef-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="f35ef-108">Gerekirse yeni bir çalışan kaydı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f35ef-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="f35ef-109">**Kıymet yönetimi \> Kurulum \> Çalışanlar \> Çalışanlar**'a gidin ve önceki adımda tanımladığınız (veya oluşturduğunuz) çalışan kaydının bakım görevlisi kaydıyla eşleştiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="f35ef-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="f35ef-110">Gereken şekilde yeni bir bakım görevlisi kaydı oluşturun ve **Çalışan** alanını önceki adımdaki çalışan kaydı olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f35ef-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="f35ef-111">**Kıymet yönetimi \> Kurulum \> Çalışanlar \> Bakım görevlisi grupları**'na gidin ve önceki adımda tanımladığınız (veya oluşturduğunuz) çalışan kaydının bakım görevlisi grubuna ait olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f35ef-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="f35ef-112">**Sistem yönetimi \> Kullanıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="f35ef-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="f35ef-113">Izgaradan ilgili kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="f35ef-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="f35ef-114">**Kullanıcı Ayrıntıları** hızlı sekmesinde, **Kişi** alanını geçerli kullanıcıyla eşleştirmek istediğiniz çalışan hesabına ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f35ef-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="f35ef-115">Bu çalışan hesabı, 1. adımda tanımladığınız (veya oluşturduğunuz) çalışan kaydı olmalıdır ve 2. adımdaki bakım görevlisi kaydına eşlenmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f35ef-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="f35ef-116">Kullanıcı izinleri ve güvenlik rolleri, Supply Chain Management kullanıcı arabiriminin özellikleri için geçerli oldukları gibi **Kıymet yönetimi** mobil çalışma alanının özellikleri için de geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="f35ef-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="f35ef-117">Bu nedenle, **Kıymet yönetimi** mobil çalışma alanına erişmek için ayarladığınız her kullanıcının Supply Chain Management'ta doğrudan benzer işlemleri gerçekleştirmek için gerekli güvenlik rollerine sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f35ef-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="f35ef-118">Kıymet yönetimi mobil çalışma alanını yayımlama</span><span class="sxs-lookup"><span data-stu-id="f35ef-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="f35ef-119">Finance and Operations (Dynamics 365) mobil uygulamasında kıymet yönetimi özelliklerini kullanılabilir hale getirmek için **Kıymet yönetimi** mobil uygulamasını yayımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f35ef-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="f35ef-120">Supply Chain Management'ta **Ayarlar** düğmesini (sağ üst köşedeki dişli simgesi) seçin ve ardından menüdeki **Mobil uygulama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f35ef-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="f35ef-121">**Mobil uygulamayı yönet** iletişim kutusunda **Kıymet Yönetimi** kutucuğunu bulun.</span><span class="sxs-lookup"><span data-stu-id="f35ef-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="f35ef-122">"Meta veride - yayımlanmadı" metnini içeriyorsa çalışma alanı henüz yayımlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="f35ef-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="f35ef-123">"Meta veride - yayımlandı" metnini içeriyorsa çalışma alanı zaten yayımlanmıştır ve bu yordamın geri kalanını atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f35ef-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="f35ef-124">![Mobil uygulamayı yönet iletişim kutusu](media/mobile-workspaces.png "Mobil uygulamayı yönet iletişim kutusu")</span><span class="sxs-lookup"><span data-stu-id="f35ef-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="f35ef-125">**Kıymet yönetimi** kutucuğunu seçin ve ardından araç çubuğunda **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f35ef-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="f35ef-126">Birkaç saniye sonra, çalışma alanının başarıyla yayımlandığını bildiren bir bildirim almalısınız.</span><span class="sxs-lookup"><span data-stu-id="f35ef-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="f35ef-127">Ek olarak, kutucuktaki metin "Metaveride - yayımlandı" olarak değişmelidir.</span><span class="sxs-lookup"><span data-stu-id="f35ef-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="f35ef-128">Finance and Operations (Dynamics 365) mobil uygulamasını yükleme ve kurma</span><span class="sxs-lookup"><span data-stu-id="f35ef-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="f35ef-129">Mobil cihazınıza **Microsoft Finance and Operations (Dynamics 365)** uygulamasını yüklemek için aşağıdaki uygulama mağazalarından birine gidin:</span><span class="sxs-lookup"><span data-stu-id="f35ef-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="f35ef-130">Google Android cihazlar için</span><span class="sxs-lookup"><span data-stu-id="f35ef-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="f35ef-131">Apple iOS cihazlar için</span><span class="sxs-lookup"><span data-stu-id="f35ef-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="f35ef-132">Finance and Operations (Dynamics 365) uygulamasını açın.</span><span class="sxs-lookup"><span data-stu-id="f35ef-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="f35ef-133">Oturum açma sayfası görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="f35ef-133">The sign-in page should appear.</span></span> <span data-ttu-id="f35ef-134">**Oturum açma** alanına, Supply Chain Management URL'nizi girin veya **Son ortamlar** listesinde son URL'yi seçin ve **Bağlan**'a dokunun.</span><span class="sxs-lookup"><span data-stu-id="f35ef-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="f35ef-135">![Oturum açma sayfası](media/mobile-app-sign-in.png "Oturum açma sayfası")</span><span class="sxs-lookup"><span data-stu-id="f35ef-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="f35ef-136">Bağlantıyı onaylamanız istenirse **Anladım** onay kutusunu seçin ve ardından **Bağlan**'a dokunun.</span><span class="sxs-lookup"><span data-stu-id="f35ef-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="f35ef-137">**Bir hesap seçin** sayfasında, mobil uygulamada oturum açmak için Microsoft hesabınızı kullanın.</span><span class="sxs-lookup"><span data-stu-id="f35ef-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="f35ef-138">**Çalışma alanları** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f35ef-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="f35ef-139">Supply Chain Management kurulumunuz tarafından yayımlanmış tüm mobil çalışma alanını listeler.</span><span class="sxs-lookup"><span data-stu-id="f35ef-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="f35ef-140">![Çalışma alanları listesi](media/mobile-app-workspaces.png "Çalışma alanları listesi")</span><span class="sxs-lookup"><span data-stu-id="f35ef-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="f35ef-141">Tüzel kişiliği (şirket) değiştirmeniz gerekiyorsa sol üst köşedeki Menü düğmesine (bazen hamburger veya hamburger düğmesi olarak da adlandırılır) dokunun ve ardından **Şirketi değiştir**'e dokunun.</span><span class="sxs-lookup"><span data-stu-id="f35ef-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="f35ef-142">![Tüzel kişiliği değiştirme](media/mobile-app-change-comp.png "Tüzel kişiliği değiştirme")</span><span class="sxs-lookup"><span data-stu-id="f35ef-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="f35ef-143">**Çalışma alanları** sayfasında, çalışmak istediğiniz çalışma alanını seçerek açın.</span><span class="sxs-lookup"><span data-stu-id="f35ef-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="f35ef-144">![Varlık yönetimi mobil çalışma alanı](media/mobile-app-asset-workspace.png "Varlık yönetimi mobil çalışma alanı")</span><span class="sxs-lookup"><span data-stu-id="f35ef-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="f35ef-145">Kıymet yönetimi mobil çalışma alanıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="f35ef-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="f35ef-146">**Kıymet yönetimi** mobil çalışma alanıyla nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Kıymet yönetimi mobil çalışma alanını kullanma](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="f35ef-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="f35ef-147">Finance and Operations (Dynamics 365) mobil uygulaması hakkında daha fazla bilgi için bkz. [Mobil uygulama giriş sayfası](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="f35ef-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>
