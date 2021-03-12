---
title: Görev listeleri oluşturma ve görev ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'tegörev listeleri oluşturma ve bunlara görev ekleme açıklanmaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cca5e0efd6516d02c372e8a616b6bb0c39f3088c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006222"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="9918d-103">Görev listeleri oluşturma ve görev ekleme</span><span class="sxs-lookup"><span data-stu-id="9918d-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9918d-104">Bu konuda, Microsoft Dynamics 365 Commerce'tegörev listeleri oluşturma ve bunlara görev ekleme açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9918d-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9918d-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="9918d-105">Overview</span></span>

<span data-ttu-id="9918d-106">Bir *görev*, bir kişinin belirli bir iş parçasını veya belirtilen bir vade tarihinden önce veya bu tarihten önce tamamlanması gereken bir eylemi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="9918d-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="9918d-107">Dynamics 365 Commerce'De bir görev, ilgili kişi hakkında ayrıntılı yönergeler ve bilgiler içerebilir.</span><span class="sxs-lookup"><span data-stu-id="9918d-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="9918d-108">Ayrıca, üretkenliği artırmaya yardımcı olmak ve görev sahibinin görevi etkili şekilde tamamlaması için gereken bağlamı sağlamak amacıyla, geri-ofis operasyonları, satış noktası (POS) işlemleri veya site sayfaları ile ilgili bağlantılar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="9918d-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="9918d-109">*Görev listesi*, iş sürecinin bir parçası olarak tamamlanması gereken görevler topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="9918d-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="9918d-110">Örneğin, yeni bir çalışanın ekleme sırasında tamamlanması gereken bir görev listesi, akşam vardiyaları olan kasiyerlerin görev listesi veya depoyu yaklaşan bir tatil döneminde hazırlamak için tamamlanması gereken bir görev listesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="9918d-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="9918d-111">Commerce'te, hedef tarihi olan her görev listesi herhangi bir sayıda mağazaya veya çalışana atanabilir ve yinelenecek şekilde konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="9918d-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="9918d-112">Hem Yöneticiler hem de çalışanlar, ticari ofislerinde görev listeleri oluşturabilir ve bunları bir mağaza kümesine atayabilirler.</span><span class="sxs-lookup"><span data-stu-id="9918d-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="9918d-113">Bir görev oluştur</span><span class="sxs-lookup"><span data-stu-id="9918d-113">Create a task list</span></span>

<span data-ttu-id="9918d-114">Görev listesi oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9918d-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="9918d-115">**Retail ve Commerce \> görev yönetimi \>görev yönetimi idaresi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9918d-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="9918d-116">**Yeni**'yi seçin ve sonra **ad**, **Açıklama** ve **sahip** alanlarına değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="9918d-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="9918d-117">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9918d-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="9918d-118">Görev listesine görev ekleme</span><span class="sxs-lookup"><span data-stu-id="9918d-118">Add tasks to a task list</span></span>

<span data-ttu-id="9918d-119">Bir görev listesine görevler eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9918d-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="9918d-120">Görev eklemek için, varolan bir görev listesinin **görevler** hızlı sekmesinde **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9918d-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="9918d-121">**Yeni görev oluştur** iletişim kutusunda, **ad** alanına görev için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="9918d-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="9918d-122">**Son veri bitiş tarihi** alanına, artı veya eksi bir tamsayı değeri girin.</span><span class="sxs-lookup"><span data-stu-id="9918d-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="9918d-123">Örneğin görev listesinin vade tarihinden iki gün önce tamamlanması gerekiyorsa, **-2** girin.</span><span class="sxs-lookup"><span data-stu-id="9918d-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="9918d-124">**Notlar** alanına ayrıntılı yönergeler girin.</span><span class="sxs-lookup"><span data-stu-id="9918d-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="9918d-125">**İlgili kişi** alanında, yardım gerekirse görev sahibinin başvurmasının gerektiği konu uzmanı adını girin.</span><span class="sxs-lookup"><span data-stu-id="9918d-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="9918d-126">**Görev bağlantısı** alanına, görevin doğasına göre bir bağlantı girin.</span><span class="sxs-lookup"><span data-stu-id="9918d-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="9918d-127">Görev listesi oluştururken bir kişiye **görev atamak** için atanan alanını kullanabilseniz de, görev listesi oluşturma sırasında görev atamaktan kaçınmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="9918d-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="9918d-128">Bunun yerine, belirli Mağazalar için liste örneği oluşturulduktan sonra görevleri atayın.</span><span class="sxs-lookup"><span data-stu-id="9918d-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="9918d-129">Çalışanların üretkenliğini artırmaya yardımcı olması için görev bağlantılarını kullan</span><span class="sxs-lookup"><span data-stu-id="9918d-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="9918d-130">Commerce, bir satış raporu çalıştırmak, yeni çalışan yönlendirmesi için çevrimiçi eğitim videosunu görüntülemek veya bir arka ofis operasyonu gerçekleştirmek gibi, görevleri belirli POS operasyonlarına bağlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="9918d-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="9918d-131">Bu özellik, görev sahiplerinin bir görevi etkili şekilde tamamlamak için gereken bilgileri edinmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="9918d-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="9918d-132">Görev oluştururken görev bağlantıları eklemek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9918d-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="9918d-133">Varolan bir görev listesinin **görevler** hızlı sekmesinde **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9918d-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="9918d-134">**Görev bağlantısı** alanındaki **Görevi Düzenle** iletişim kutusunda aşağıdaki seçeneklerden bir veya birkaçını seçin:</span><span class="sxs-lookup"><span data-stu-id="9918d-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="9918d-135">"Ürün takımları" gibi bir arka ofis işlemi yapılandırmak için **menü öğesini** seçin.</span><span class="sxs-lookup"><span data-stu-id="9918d-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="9918d-136">"Satış raporları" gibi bir POS işlemini konfigüre etmek için **POS işlemi** seçin.</span><span class="sxs-lookup"><span data-stu-id="9918d-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="9918d-137">Mutlak bir URL konfigüre etmek için **URL**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9918d-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="9918d-138">Aşağıdaki resimde, **görevi düzenle** iletişim kutusunda görev bağlantılarının seçimi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9918d-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Düzenle görev iletişim kutusunda görev bağlantıları seçme](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="9918d-140">Bir göreve bağlanabilmesi için bir POS operasyonu konfigüre et</span><span class="sxs-lookup"><span data-stu-id="9918d-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="9918d-141">Bir göreve bağlanabilmesi için bir POS operasyonu konfigüre etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9918d-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="9918d-142">**Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS \> Operasyonlar** öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="9918d-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="9918d-143">**Düzenle**'yi seçin, POS işlemini bulun ve bunun için **Görev yönetimini etkinleştir** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="9918d-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9918d-144">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9918d-144">Additional resources</span></span>

[<span data-ttu-id="9918d-145">Görev yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="9918d-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="9918d-146">Görev yönetimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9918d-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="9918d-147">Mağazalara veya personele görev listeleri atama</span><span class="sxs-lookup"><span data-stu-id="9918d-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="9918d-148">POS'ta görev yönetimi</span><span class="sxs-lookup"><span data-stu-id="9918d-148">Task management in POS</span></span>](task-mgmt-POS.md)
