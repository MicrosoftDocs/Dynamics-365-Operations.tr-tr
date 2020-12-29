---
title: Mağazalara veya personele görev listeleri atama
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta mağazalara veya çalışanlara görev listeleri atama açıklanmaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 82cec9861b759037f40315fb2e6f36002a0ac059
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416492"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="cf554-103">Mağazalara veya personele görev listeleri atama</span><span class="sxs-lookup"><span data-stu-id="cf554-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf554-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta mağazalara veya çalışanlara görev listeleri atama açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="cf554-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cf554-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="cf554-105">Overview</span></span>

<span data-ttu-id="cf554-106">Dynamics 365 Commerce'teki görev yönetimi, bir görev listesini birden fazla mağazaya veya çalışana veya mağaza ve çalışanların bir birleşimine atamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="cf554-106">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="cf554-107">Örneğin, 20 mağaza için bir bölgesel yönetici, **tatil sezonuna hazırlık** görev listesini tüm 20 mağazalara atamak isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="cf554-107">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="cf554-108">Görev listesi atama işlemini Başlat</span><span class="sxs-lookup"><span data-stu-id="cf554-108">Start the task list assignment process</span></span>

<span data-ttu-id="cf554-109">Görev listesi atama işlemini başlatmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="cf554-109">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="cf554-110">**Retail ve Commerce \> görev yönetimi \>görev yönetimi idaresi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="cf554-110">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="cf554-111">Atanacak görev listesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cf554-111">Select the task list to assign.</span></span>
1. <span data-ttu-id="cf554-112">**İşlemi başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cf554-112">Select **Start process**.</span></span>
1. <span data-ttu-id="cf554-113">**İşlem Başlat** iletişim kutusundaki **genel** sekmesinde, **işlem adı** alanına bir ad girin (örneğin, **Doğu bölge depoları**).</span><span class="sxs-lookup"><span data-stu-id="cf554-113">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="cf554-114">**Hedef Tarih** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="cf554-114">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="cf554-115">Görev listesini mağazalara atamak için **mağazalar** sekmesinde, depoları bulup seçmek için **organizasyon hiyerarşisi** filtresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cf554-115">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="cf554-116">Görev listesini çalışanlara atamak için **çalışanlar** sekmesinde, çalışanları bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cf554-116">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="cf554-117">İşlemi başlatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cf554-117">Select **OK** to start the process.</span></span> <span data-ttu-id="cf554-118">Görevler listesi seçilen mağazalara veya çalışanlara atanır.</span><span class="sxs-lookup"><span data-stu-id="cf554-118">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="cf554-119">Aşağıdaki şekil, **işlem Başlat** iletişim kutusunda depoların nasıl bulunacağı ve seçgeleile ilgili bir örnek göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="cf554-119">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![İşlem Başlat iletişim kutusunda depoları bulma ve seçme](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="cf554-121">Görev listelerini yinelenen bir temelde ata</span><span class="sxs-lookup"><span data-stu-id="cf554-121">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="cf554-122">Perakende, bazen "Perşembe kapatma denetim listesi" veya "ay denetim listesinin ilk günü" gibi görevlere tekrarlayan görevler de içerebilir.</span><span class="sxs-lookup"><span data-stu-id="cf554-122">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="cf554-123">Bu nedenle, görev listesini yinelenen bir temelde atamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf554-123">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="cf554-124">**Retail ve Commerce \> görev yönetimi \>görev yönetimi idaresi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="cf554-124">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="cf554-125">Atanacak görev listesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cf554-125">Select the task list to assign.</span></span>
1. <span data-ttu-id="cf554-126">**İşlemi başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cf554-126">Select **Start process**.</span></span>
1. <span data-ttu-id="cf554-127">**İşlem Başlat** iletişim kutusundaki **genel** sekmesinde, **işlem adı** alanına bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="cf554-127">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="cf554-128">**Yineleme** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cf554-128">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="cf554-129">**Gün cinsinden tekrarlama hedefi Tarih farkı** alanında, gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="cf554-129">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="cf554-130">Örneğin, **4** girerseniz, hedef tarih tekrarlama tarihi artı dört gün olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="cf554-130">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="cf554-131">**Arka planda çalıştır** sekmesinde **Tekrar** ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cf554-131">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="cf554-132">**Tekrarı tanımla** iletişim kutusunda sıklık ölçütünü girin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cf554-132">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="cf554-133">Aşağıdaki çizimde, **yinelenme tanımla** iletişim kutusunda sıklık ölçütünün nasıl girmenin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="cf554-133">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Tekrarı tanımla iletişim kutusunda sıklık ölçütünü girin](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="cf554-135">Görev listesi durumunu izle</span><span class="sxs-lookup"><span data-stu-id="cf554-135">Track task list status</span></span>

<span data-ttu-id="cf554-136">Bir bölgesel yönetici veya mağaza yöneticisiyseniz, birden fazla mağazaya veya çalışana atanmış görev listelerinin durumunu izlemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf554-136">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="cf554-137">Böylece, kendilerine atanan görevleri zamanında tamamlamadıkları mağazalar veya işçilere göre izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf554-137">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="cf554-138">Commerce arka ofisi, görev listelerinin durumunu görüntülemenizi, görevlerin yeniden atanmasını veya bir görevin durumunu değiştirmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="cf554-138">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="cf554-139">Tüm görevlerin görev listesi durumunu izlemek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="cf554-139">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="cf554-140">**Retail ve Commerce \> görev yönetimi \>görev yönetimi süreçleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="cf554-140">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="cf554-141">Çeşitli mağazalara atanan tüm görev listelerinin durumunu görüntülemek için **tüm görev listeleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cf554-141">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="cf554-142">Size atanan tüm görevlerin görev listesi durumunu izlemek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="cf554-142">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="cf554-143">**Retail ve Commerce \> görev yönetimi \>görev yönetimi süreçleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="cf554-143">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="cf554-144">Size atanan görevlerin durumunu görüntülemek veya güncelleştirmek için **Görevlerim** veya **tüm görevler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cf554-144">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf554-145">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cf554-145">Additional resources</span></span>

[<span data-ttu-id="cf554-146">Görev yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="cf554-146">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="cf554-147">Görev yönetimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="cf554-147">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="cf554-148">Görev listeleri oluşturma ve görev ekleme</span><span class="sxs-lookup"><span data-stu-id="cf554-148">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="cf554-149">POS'ta görev yönetimi</span><span class="sxs-lookup"><span data-stu-id="cf554-149">Task management in POS</span></span>](task-mgmt-POS.md)
