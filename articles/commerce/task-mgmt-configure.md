---
title: Görev yönetimini yapılandırma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te görev yönetimi özelliklerinin nasıl yapılandırılacağı açıklanmaktadır.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 742d49b1b7b46952d0a8bb6c8a33cde2a35d124f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791716"
---
# <a name="configure-task-management"></a><span data-ttu-id="018cb-103">Görev yönetimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="018cb-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="018cb-104">Bu konuda, Microsoft Dynamics 365 Commerce'te görev yönetimi özelliklerinin nasıl yapılandırılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="018cb-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="018cb-105">Yöneticiler ve çalışanlar ticari olarak görev yönetimi özelliklerini kullanabilmeniz için, görev yönetimi Dynamics 365 Commerce'in konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="018cb-105">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="018cb-106">Yapılandırma adımları, yöneticilere ve çalışanlara izinler verilmesinde, bir satış noktasına (POS) sahip müşterilere dağıtım, POS bildirimleri kurma ve bir POS uygulamasının giriş sayfasında **görevler** döşemesini konfigüre eder.</span><span class="sxs-lookup"><span data-stu-id="018cb-106">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="018cb-107">Mağaza yöneticileri izinlerini konfigüre et</span><span class="sxs-lookup"><span data-stu-id="018cb-107">Configure permissions for store managers</span></span>

<span data-ttu-id="018cb-108">Belirli bir depodaki her çalışan, o mağazaya atanan tüm görevleri görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="018cb-108">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="018cb-109">Kendilerine atanan görevlerin durumunu da güncelleştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="018cb-109">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="018cb-110">Ancak, depolama yöneticileri gibi kişiler, mağazaya atanan görevleri yönetmek ve tek amaçlı görevler oluşturmak için görev yönetimi izinleri bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="018cb-110">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="018cb-111">Mağaza yöneticilerinin görev yönetimi izinlerini konfigüre etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="018cb-111">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="018cb-112">**Perakende ve ticaret \> Çalışanlar \> Tüm çalışanlara** gidin.</span><span class="sxs-lookup"><span data-stu-id="018cb-112">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="018cb-113">Belirli bir izin grubu (örneğin, **yönetici**) seçin ve **Düzenle** seçin.</span><span class="sxs-lookup"><span data-stu-id="018cb-113">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="018cb-114">**İzinler** hızlı sekmesinde, **görev yönetimine izin ver** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="018cb-114">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="018cb-115">**Bildirimler** hızlı sekmesinde, **görev yönetimi** işlemini ekleyin ve **görüntüleme sırası** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="018cb-115">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="018cb-116">Örneğin, **sipariş karşılama** operasyonunu zaten **1** olan bir **görüntüleme emri** değerine sahip ise **2** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="018cb-116">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="018cb-117">Bir yönetici olmayan kişinin POS'ta görev yönetimi izinleri olması gerekiyorsa, kişiye izin verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="018cb-117">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="018cb-118">Alternatif olarak, yönetici olmayanlar için yeni bir izin grubu oluşturabilir ve **görev yönetimine izin ver** seçeneğini **Evet** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="018cb-118">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="018cb-119">Aşağıdaki çizim, mağaza yöneticilerinin görev yönetimi izinlerini konfigüre etmesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="018cb-119">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Mağaza yöneticilerinin görev yönetimi izinlerini konfigüre etmesi](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="018cb-121">Çalışanlar için izinleri konfigüre et</span><span class="sxs-lookup"><span data-stu-id="018cb-121">Configure permissions for employees</span></span>

<span data-ttu-id="018cb-122">Çalışanların görev listeleri oluşturmak, atama ölçütlerini yönetmek ve herhangi bir görev listesinin tekrarlarını konfigüre etmek için izinleri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="018cb-122">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="018cb-123">Bu izinleri konfigüre etmek için, çalışanları **perakende Görev Yöneticisi** rolüne atarsınız.</span><span class="sxs-lookup"><span data-stu-id="018cb-123">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="018cb-124">Bir çalışan için izinleri yapılandırmak üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="018cb-124">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="018cb-125">**Perakende ve Ticaret \> Personel \> Kullanıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="018cb-125">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="018cb-126">Bir çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="018cb-126">Select an employee.</span></span>
1. <span data-ttu-id="018cb-127">**Kullanıcının rolleri** hızlı sekmesinde, **Rol ata**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="018cb-127">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="018cb-128">**Kullanıcıya rol ata** iletişim kutusunda, **perakende görev Yöneticisi** rolünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="018cb-128">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="018cb-129">POS istemcilerine ilişkin izinleri dağıt</span><span class="sxs-lookup"><span data-stu-id="018cb-129">Distribute permissions to POS clients</span></span>

<span data-ttu-id="018cb-130">Çalışanların POS istemcilerini kullanabilmesi için, izinlerin o istemcilerle dağıtılması ve eşitlenmelerini sağlamak gerekir.</span><span class="sxs-lookup"><span data-stu-id="018cb-130">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="018cb-131">POS istemcilerine izin dağıtmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="018cb-131">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="018cb-132">**Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="018cb-132">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="018cb-133">**1060** (**personel**) dağıtım zamanlamasını seçin ve **şimdi Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="018cb-133">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="018cb-134">**1070** (**Kanal yapılandırması**) dağıtım zamanlamasını seçin ve **şimdi Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="018cb-134">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="018cb-135">Görevler için POS bildirimlerini konfigüre et</span><span class="sxs-lookup"><span data-stu-id="018cb-135">Configure POS notifications for tasks</span></span>

<span data-ttu-id="018cb-136">Bu bildirim POS uygulamasında kullanılabilir olacak şekilde görev yönetimi konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="018cb-136">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="018cb-137">Görevler için POS bildirimleri yapılandırmak üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="018cb-137">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="018cb-138">**Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS \> Operasyonlar** öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="018cb-138">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="018cb-139">**1400** (**Görev yönetimi**) işlemini bulun ve bunun için **bildirimleri etkinleştir** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="018cb-139">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="018cb-140">Aşağıdaki şekil, **POS işlemleri** sayfasındaki **görev yönetimi** işlemini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="018cb-140">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![POS işlemleri sayfasında görev yönetimi işlemi](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="018cb-142">POS bildirimlerinin nasıl yapılandırılacağı hakkında daha fazla bilgi için bkz. [satış noktasında (POS) sipariş bildirimleri göster](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="018cb-142">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="018cb-143">POS uygulaması giriş sayfasında görevler kutucuğunu konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="018cb-143">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="018cb-144">Bir POS uygulamasının giriş sayfasında **Görevler** döşemesini konfigüre etmeden önce, bir POS ekran düzenine nasıl yapılandırılacağı ve yeni düğmeler ekleneceği hakkında bilgi için [satış noktası (POS) ile ilgili ekran düzenlerine](pos-screen-layouts.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="018cb-144">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="018cb-145">POS uygulaması giriş sayfasında **görevler** kutucuğunu konfigüre etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="018cb-145">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="018cb-146">**Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS \> Ekran düzenleri** öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="018cb-146">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="018cb-147">Bir ekran düzeni seçin, bir düzen boyutu seçin ve bir düğme grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="018cb-147">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="018cb-148">**Düğme grupları** hızlı sekmesinde, seçili düğme grubunu düzenlemek için **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="018cb-148">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="018cb-149">Giriş sayfasının uygun bölümüne **görevler** kutucuğu ekleyin.</span><span class="sxs-lookup"><span data-stu-id="018cb-149">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="018cb-150">Aşağıdaki çizimde POS giriş sayfasındaki **Görevler** kutucuğunun bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="018cb-150">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Bir POS giriş sayfasındaki görevler bölmesi](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="018cb-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="018cb-152">Additional resources</span></span>

[<span data-ttu-id="018cb-153">Görev yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="018cb-153">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="018cb-154">Görev listeleri oluşturma ve görev ekleme</span><span class="sxs-lookup"><span data-stu-id="018cb-154">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="018cb-155">Mağazalara veya personele görev listeleri atama</span><span class="sxs-lookup"><span data-stu-id="018cb-155">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="018cb-156">POS'ta görev yönetimi</span><span class="sxs-lookup"><span data-stu-id="018cb-156">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
