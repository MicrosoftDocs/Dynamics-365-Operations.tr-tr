---
title: "Bir görev akışında el ile yapılan görevi yapılandır"
description: "Bu konu, el ile bir görevin özelliklerini yapılandırmayı açıklar."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 09bd86ff7a4aa8ae64cfa4a38fba643f9117d6eb
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-manual-task-in-a-workflow"></a><span data-ttu-id="f403f-103">Bir görev akışında el ile yapılan görevi yapılandır</span><span class="sxs-lookup"><span data-stu-id="f403f-103">Configure a manual task in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f403f-104">Bu konu, el ile bir görevin özelliklerini yapılandırmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="f403f-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="f403f-105">El ile bir görevi iş akışı düzenleyicisinde yapılandırmak için göreve sağ tıklatın ve sonra **Özellikler**'i açmak için **Özellikler** sayfanı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="f403f-106">Ardından el ile görevin özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="f403f-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="f403f-107">Görevi adlandırma</span><span class="sxs-lookup"><span data-stu-id="f403f-107">Name the task</span></span>
<span data-ttu-id="f403f-108">El ile göreve bir ad vermek için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="f403f-108">Follow these steps to enter a name for the manual task.</span></span>

1.  <span data-ttu-id="f403f-109">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="f403f-110">**Ad** alanına görev için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="f403f-111">Konu satırı ve açıklamaları girme</span><span class="sxs-lookup"><span data-stu-id="f403f-111">Enter a subject line and instructions</span></span>
<span data-ttu-id="f403f-112">Göreve atanan kullanıcılara bir konu satırı ve açıklama sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f403f-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="f403f-113">Örneğin, eğer satınalma talepleri için bir görev yapılandırıyorsanız, bu göreve atanmış kullanıcı konu satırını ve yönergeleri **Satınalma talepleri** sayfasında görür.</span><span class="sxs-lookup"><span data-stu-id="f403f-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="f403f-114">Konu satırı sayfa üzerindeki bir ileti çubuğunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f403f-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="f403f-115">Daha sonra, kullanıcı yönergeleri görüntülemek için ileti çubuğundaki simgeye tıklayabilir.</span><span class="sxs-lookup"><span data-stu-id="f403f-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="f403f-116">Konu satırını ve açıklamaları girmek için şu adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="f403f-116">Follow these steps to enter a subject line and instructions.</span></span>

1.  <span data-ttu-id="f403f-117">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-117">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="f403f-118">**Çalışma öğesi konusu** alanında, konu satırını girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-118">In the **Work item subject** field, enter the subject line.</span></span>
3.  <span data-ttu-id="f403f-119">Konu satırını kişiselleştirmek için yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="f403f-120">Yer tutucular, konu satırı kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="f403f-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="f403f-121">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-121">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="f403f-122">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-122">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="f403f-123">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-123">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="f403f-124">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-124">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="f403f-125">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-125">Click **Insert**.</span></span>

4.  <span data-ttu-id="f403f-126">Konu satırı çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-126">To add translations of the subject line, follow these steps:</span></span>
    1.  <span data-ttu-id="f403f-127">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-127">Click **Translations**.</span></span>
    2.  <span data-ttu-id="f403f-128">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-128">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="f403f-129">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="f403f-130">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-130">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="f403f-131">Metni kişiselleştirmek için, 3. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6.  <span data-ttu-id="f403f-132">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-132">Click **Close**.</span></span>

5.  <span data-ttu-id="f403f-133">**Çalışma öğesi yönergeleri** alanında, yönergeleri girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-133">In the **Work item instructions** field, enter the instructions.</span></span>
6.  <span data-ttu-id="f403f-134">Yönergeleri kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="f403f-135">Yer tutucular, yönergeler kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="f403f-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="f403f-136">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-136">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="f403f-137">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-137">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="f403f-138">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-138">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="f403f-139">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-139">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="f403f-140">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-140">Click **Insert**.</span></span>

7.  <span data-ttu-id="f403f-141">Yönergelerin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-141">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="f403f-142">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-142">Click **Translations**.</span></span>
    2.  <span data-ttu-id="f403f-143">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-143">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="f403f-144">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="f403f-145">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-145">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="f403f-146">Metni kişiselleştirmek için, 6. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6.  <span data-ttu-id="f403f-147">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="f403f-148">Görev atama</span><span class="sxs-lookup"><span data-stu-id="f403f-148">Assign the task</span></span>
<span data-ttu-id="f403f-149">El ile görev kime atanacağını belirtmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1.  <span data-ttu-id="f403f-150">Sol bölmede **Atama**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-150">In the left pane, click **Assignment**.</span></span>
2.  <span data-ttu-id="f403f-151">**Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 3. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f403f-152">Seçenek</span><span class="sxs-lookup"><span data-stu-id="f403f-152">Option</span></span></th>
    <th><span data-ttu-id="f403f-153">Görevin atandığı kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="f403f-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="f403f-154">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="f403f-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="f403f-155">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="f403f-155">Participant</span></span></td>
    <td><span data-ttu-id="f403f-156">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="f403f-156">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f403f-157"><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, görevin atanacağı grup ya da rolün türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="f403f-158"><strong>Katılımcı</strong> listesinde, görevin atanacağı grup veya rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f403f-159">Hiyerarşi</span><span class="sxs-lookup"><span data-stu-id="f403f-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="f403f-160">Belirli bir kuruluş hiyerarşisindeki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="f403f-160">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f403f-161"><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, görevin atanacağı hiyerarşi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="f403f-162">Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f403f-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="f403f-163">Bu adlar, görevin atanabileceği kullanıcıları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f403f-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="f403f-164">Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="f403f-165">Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="f403f-166">Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="f403f-167">Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="f403f-168"><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara görevin atanması gerektiğini belirtin:</span><span class="sxs-lookup"><span data-stu-id="f403f-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="f403f-169"><strong>Alınan tüm kullanıcılara ata</strong> – Görev, bu aralıktaki tüm kullanıcılara atanır.</span><span class="sxs-lookup"><span data-stu-id="f403f-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="f403f-170"><strong>Yalnızca alınan son kullanıcıya ata</strong> – Görev, yalnızca aralıktaki son kullanıcıya atanır.</span><span class="sxs-lookup"><span data-stu-id="f403f-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="f403f-171"><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Görev, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya atanmaz.</span><span class="sxs-lookup"><span data-stu-id="f403f-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="f403f-172">Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="f403f-173">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="f403f-173">Workflow user</span></span></td>
    <td><span data-ttu-id="f403f-174">Mevcut iş akışındaki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="f403f-174">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="f403f-175"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f403f-176">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="f403f-176">User</span></span></td>
    <td><span data-ttu-id="f403f-177">Belirli Microsoft Dynamics 365 for Finance and Operations kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="f403f-177">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f403f-178"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f403f-179"><strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Finance and Operations kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="f403f-179">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="f403f-180">Görevin atanacağı kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="f403f-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="f403f-181">Kuyruk</span><span class="sxs-lookup"><span data-stu-id="f403f-181">Queue</span></span></td>
    <td><span data-ttu-id="f403f-182">Bir iş maddesi kuyruğu</span><span class="sxs-lookup"><span data-stu-id="f403f-182">A work item queue</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f403f-183"><strong>Kuyruk</strong>'u seçtikten sonra <strong>Kuyruk tabanlı</strong> sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="f403f-184">Görevi belirli bir kuyruğa atamak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="f403f-185"><strong>Kuyruk türü</strong> listesinde, <strong>İş öğesi kuyrukları</strong>'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="f403f-186"><strong>Kuyruk adı</strong> listesinde, kuyruğu seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="f403f-187">Eğer belirli bir koşulun görevin hangi kuyruğa atanacağını belirlemesi gerekiyorsa, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="f403f-188"><strong>Kuyruk türü</strong> listesinde, <strong>Koşullu iş öğesi kuyrukları</strong>'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="f403f-189"><strong>Kuyruk adı</strong> listesinde, <strong>Koşullu kuyruk</strong>'u seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol></li>
    </ol><span data-ttu-id="f403f-190">
    <strong>Not:</strong> Bu seçenek yalnızca servis talebi yönetimi gibi bazı iş akışları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f403f-190">
    <strong>Note:</strong> This option is used for only a few workflows, such as Case management.</span></span></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="f403f-191">**Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının görevi tamamlamak üzere ne kadar zamanı olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="f403f-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="f403f-192">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-192">Select one of the following options:</span></span>
    -   <span data-ttu-id="f403f-193">**Saatler** – Kullanıcının görevi tamamlaması gereken saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="f403f-194">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="f403f-195">**Günler** – Kullanıcının görevi tamamlaması gereken gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="f403f-196">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="f403f-197">**Haftalar** – Kullanıcının görevi tamamlaması gereken hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="f403f-198">**Aylar** – Kullanıcının görevi tamamlamış olması gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="f403f-199">Örneğin kullanıcının görevi ayın üçüncü haftasının Cuma günü tamamlamasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="f403f-200">**Yıllar** – Kullanıcının görevi tamamlamış olması gereken günü, haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="f403f-201">Örneğin kullanıcının görevi Aralık ayının üçüncü haftasının Cuma günü tamamlamasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="f403f-202">Eğer kullanıcı ayırılan zaman içerisinde görevi tamamlamazsa, görevin vadesi geçer.</span><span class="sxs-lookup"><span data-stu-id="f403f-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="f403f-203">Vadesi geçmiş bir görev, sayfanın **İlerletme** bölgesinde işaretlemiş olduğunuz seçeneklere göre ilerletilebilir.</span><span class="sxs-lookup"><span data-stu-id="f403f-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="f403f-204">Görevin süresi geçtiğinde ne olacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="f403f-204">Specify what happens when the task is overdue</span></span>
<span data-ttu-id="f403f-205">Eğer bir kullanıcı ayırılan zaman içerisinde el ile görevi tamamlamazsa, görevin vadesi geçer.</span><span class="sxs-lookup"><span data-stu-id="f403f-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="f403f-206">Vadesi geçmiş bir görev ilerletilebilir veya başka bir kullanıcıya otomatik olarak atanabilir.</span><span class="sxs-lookup"><span data-stu-id="f403f-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="f403f-207">Vadesi geçmiş ise, görevin üst düzeye ilerletilmesi için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-207">Follow these steps to escalate the task if it's overdue.</span></span>

1.  <span data-ttu-id="f403f-208">Sol bölmede **İlerletilme**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-208">In the left pane, click **Escalation**.</span></span>
2.  <span data-ttu-id="f403f-209">İlerletme yolu oluşturmak için **İlerletme yolunu kullan** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="f403f-210">Sistem görevi ilerletme yolunda listelenmiş olan kullanıcılara otomatik olarak atar.</span><span class="sxs-lookup"><span data-stu-id="f403f-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="f403f-211">Örneğin, aşağıdaki tablo bir ilerletme yolunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f403f-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="f403f-212">Seri</span><span class="sxs-lookup"><span data-stu-id="f403f-212">Sequence</span></span> | <span data-ttu-id="f403f-213">İlerletme yolu</span><span class="sxs-lookup"><span data-stu-id="f403f-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="f403f-214">1</span><span class="sxs-lookup"><span data-stu-id="f403f-214">1</span></span>        | <span data-ttu-id="f403f-215">Şu kişiye ata: Donna</span><span class="sxs-lookup"><span data-stu-id="f403f-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="f403f-216">2</span><span class="sxs-lookup"><span data-stu-id="f403f-216">2</span></span>        | <span data-ttu-id="f403f-217">Şu kişiye ata: Erin</span><span class="sxs-lookup"><span data-stu-id="f403f-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="f403f-218">3</span><span class="sxs-lookup"><span data-stu-id="f403f-218">3</span></span>        | <span data-ttu-id="f403f-219">Son eylem: Reddet</span><span class="sxs-lookup"><span data-stu-id="f403f-219">Final action: Reject</span></span> |

    <span data-ttu-id="f403f-220">Bu örnekte sistem süresi geçen görevi Donna'ya atar.</span><span class="sxs-lookup"><span data-stu-id="f403f-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="f403f-221">Eğer Donna ayırılan süre içerisinde görevi tamamlamazsa, sistem görevi Erin'e atar.</span><span class="sxs-lookup"><span data-stu-id="f403f-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="f403f-222">Eğer Erin ayırılan süre içerisinde görevi tamamlamazsa, sistem işlenmek üzere gönderilen belgeyi reddeder.</span><span class="sxs-lookup"><span data-stu-id="f403f-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>
3.  <span data-ttu-id="f403f-223">Bir kullanıcıyı ilerletme yoluna eklemek için **İlerletme ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="f403f-224">**Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 4. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f403f-225">Seçenek</span><span class="sxs-lookup"><span data-stu-id="f403f-225">Option</span></span></th>
    <th><span data-ttu-id="f403f-226">Görevin ilerletileceği kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="f403f-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="f403f-227">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="f403f-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="f403f-228">Hiyerarşi</span><span class="sxs-lookup"><span data-stu-id="f403f-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="f403f-229">Belirli bir kuruluş hiyerarşisindeki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="f403f-229">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f403f-230"><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, görevin ilerletileceği hiyerarşi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="f403f-231">Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f403f-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="f403f-232">Bu adlar, görevin ilerletilebileceği kullanıcıları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f403f-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="f403f-233">Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="f403f-234">Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="f403f-235">Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="f403f-236">Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="f403f-237"><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara görevin ilerletilmesi gerektiğini belirtin:</span><span class="sxs-lookup"><span data-stu-id="f403f-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="f403f-238"><strong>Alınan tüm kullanıcılara ata</strong> – Görev, bu aralıktaki tüm kullanıcılara ilerletilir.</span><span class="sxs-lookup"><span data-stu-id="f403f-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="f403f-239"><strong>Yalnızca alınan son kullanıcıya ata</strong> – Görev, yalnızca aralıktaki son kullanıcıya ilerletilir.</span><span class="sxs-lookup"><span data-stu-id="f403f-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="f403f-240"><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Bu görev, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya ilerletilmez.</span><span class="sxs-lookup"><span data-stu-id="f403f-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="f403f-241">Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f403f-242">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="f403f-242">Workflow user</span></span></td>
    <td><span data-ttu-id="f403f-243">Mevcut iş akışındaki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="f403f-243">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="f403f-244"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="f403f-245">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="f403f-245">User</span></span></td>
    <td><span data-ttu-id="f403f-246">Belirli Finance and Operations kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="f403f-246">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f403f-247"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f403f-248"><strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Finance and Operations kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="f403f-248">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="f403f-249">Görevin ilerletileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="f403f-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  <span data-ttu-id="f403f-250">**Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının görevi tamamlamak üzere ne kadar zamanı olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="f403f-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="f403f-251">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-251">Select one of the following options:</span></span>
    -   <span data-ttu-id="f403f-252">**Saatler** – Kullanıcının görevi tamamlaması gereken saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="f403f-253">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="f403f-254">**Günler** – Kullanıcının görevi tamamlaması gereken gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="f403f-255">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="f403f-256">**Haftalar** – Kullanıcının görevi tamamlaması gereken hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="f403f-257">**Aylar** – Kullanıcının görevi tamamlamış olması gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="f403f-258">Örneğin kullanıcının görevi ayın üçüncü haftasının Cuma günü tamamlamasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="f403f-259">**Yıllar** – Kullanıcının görevi tamamlamış olması gereken günü, haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="f403f-260">Örneğin kullanıcının görevi Aralık ayının üçüncü haftasının Cuma günü tamamlamasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5.  <span data-ttu-id="f403f-261">İlerletme yoluna eklenecek tüm kullanıcılar için 3. adım ve 4. adımlar arasındaki süreci yineleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="f403f-262">Kullanıcıların sıralamasını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-262">You can change the order of the users.</span></span>
6.  <span data-ttu-id="f403f-263">İlerletme yolundaki kullanıcılar verilen süre içinde görevi tamamlamazsa, sistem görev üstünde otomatik olarak eylem alır.</span><span class="sxs-lookup"><span data-stu-id="f403f-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="f403f-264">Sistemin alacağı eylemi belirtmek için **Eylem** satırını seçin ve sonra **Eylemi bitir** sekmesi üzerinde bir eylem seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="f403f-265">Sistemin ne zaman görev üzerinde otomatik olarak eylem alacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="f403f-265">Specify when the system automatically acts on the task</span></span>
<span data-ttu-id="f403f-266">Belirli koşullar sağlandığında sistemin el ile görevler üzerinde eylem almasını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="f403f-267">Örneğin, bir görev, Gider raporları departmanının bir üyesinin, bir gider raporu ile birlikte gönderilen girişleri gözden geçirmesini gerektirmektedir.</span><span class="sxs-lookup"><span data-stu-id="f403f-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="f403f-268">Şirket ilkesi uyarınca, bu görev, gider raporunun toplam tutarı 100 USD'den fazlaysa gerçekleştirilmek zorundadır.</span><span class="sxs-lookup"><span data-stu-id="f403f-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="f403f-269">Bu senaryoda, toplam tutar 100'den az ise sistemi, görevi otomatik olarak **Tamamlandı** olarak işaretlemek üzere yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="f403f-270">Sistemin bir el ile görev üzerinde ne zaman eylem alması gerektiğin belirtmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1.  <span data-ttu-id="f403f-271">Sol bölmede **Otomatik eylemler**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-271">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="f403f-272">**Otomatik eylemleri etkinleştir** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-272">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="f403f-273">**Koşul ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-273">Click **Add condition**.</span></span>
4.  <span data-ttu-id="f403f-274">Koşulu girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-274">Enter a condition.</span></span>
5.  <span data-ttu-id="f403f-275">Varsa, gerekli ek koşulları girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-275">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="f403f-276">Girdiğiniz koşulların doğru biçimde yapılandırıldığını doğrulamak için, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="f403f-277">**Sına**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-277">Click **Test**.</span></span>
    2.  <span data-ttu-id="f403f-278">**İş akışını test et** sayfasında, **Koşulu doğrula** alanında, bir kayıt seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="f403f-279">**Sına**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-279">Click **Test**.</span></span> <span data-ttu-id="f403f-280">Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="f403f-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="f403f-281">**Özellikler** sayfasında geri dönmek için **OK** ya da **İptal Et**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7.  <span data-ttu-id="f403f-282">**Eylemi otomatik tamamla** listesinden sistemin görev üzerinde gerçekleştirmesi gereken eylemi seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="f403f-283">Bildirimlerin ne zaman gönderileceğini belirtme</span><span class="sxs-lookup"><span data-stu-id="f403f-283">Specify when notifications are sent</span></span>
<span data-ttu-id="f403f-284">Bir el ile görev tamamlandığında, temsilci atandığında, ilerletildiğinde, tamamlandığında, reddedildiğinde veya bir değişiklik istendiğinde kişilere bildirim gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="f403f-285">Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1.  <span data-ttu-id="f403f-286">Sol bölmede **Bildirimler**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-286">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="f403f-287">Bildirimlerin gönderilmesi gerektiği etkinlikler için yanlarındaki onay kutusunu işaretleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-287">Select the check box next to the events that notifications should be sent for:</span></span>
    -   <span data-ttu-id="f403f-288">**Temsilci** – Görev başka bir kullanıcıya atandı.</span><span class="sxs-lookup"><span data-stu-id="f403f-288">**Delegate** – The task has been assigned to another user.</span></span>
    -   <span data-ttu-id="f403f-289">**İlerlet** – Atanmış kullanıcı, ayrılan sürede görevi tamamlamadı.</span><span class="sxs-lookup"><span data-stu-id="f403f-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    -   <span data-ttu-id="f403f-290">**Tamamlandı** – Atanmış kullanıcı, görevi tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="f403f-290">**Complete** – The assigned user has completed the task.</span></span>
    -   <span data-ttu-id="f403f-291">**Reddetme** – Atanmış kullanıcı gönderilen belgeyi reddetti.</span><span class="sxs-lookup"><span data-stu-id="f403f-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    -   <span data-ttu-id="f403f-292">**Değişiklik iste** – Atanmış kullanıcı gönderilmiş olan belgede bir değişiklik talep etti.</span><span class="sxs-lookup"><span data-stu-id="f403f-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3.  <span data-ttu-id="f403f-293">2. adımda seçtiğiniz bir olay için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-293">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="f403f-294">**Bildirim metni** sekmesinde, metin kutusuna, bildirimin metnini girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="f403f-295">Bildirimi kişiselleştirmek için yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="f403f-296">Yer tutucular, bildirim kullanıcılara gösterildiğinde uygun bilgilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="f403f-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="f403f-297">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-297">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="f403f-298">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-298">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="f403f-299">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-299">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="f403f-300">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-300">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="f403f-301">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-301">Click **Insert**.</span></span>

6.  <span data-ttu-id="f403f-302">Bildirimin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-302">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="f403f-303">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-303">Click **Translations**.</span></span>
    2.  <span data-ttu-id="f403f-304">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-304">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="f403f-305">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="f403f-306">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-306">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="f403f-307">Metni kişiselleştirmek için, 5. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="f403f-308">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-308">Click **Close**.</span></span>

7.  <span data-ttu-id="f403f-309">**Alıcı** sekmesinde, bildirimlerin kime gönderildiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f403f-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="f403f-310">Aşağıdaki tablodaki seçeneklerden birini seçin ve 8. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f403f-311">Seçenek</span><span class="sxs-lookup"><span data-stu-id="f403f-311">Option</span></span></th>
    <th><span data-ttu-id="f403f-312">Bildirim alıcıları</span><span class="sxs-lookup"><span data-stu-id="f403f-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="f403f-313">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="f403f-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="f403f-314">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="f403f-314">Participant</span></span></td>
    <td><span data-ttu-id="f403f-315">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="f403f-315">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f403f-316"><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, bildirimlerin gönderileceği grup ya da rolün türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="f403f-317"><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f403f-318">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="f403f-318">Workflow user</span></span></td>
    <td><span data-ttu-id="f403f-319">Mevcut iş akışındaki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="f403f-319">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="f403f-320"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="f403f-321">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="f403f-321">User</span></span></td>
    <td><span data-ttu-id="f403f-322">Belirli Finance and Operations kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="f403f-322">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f403f-323"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f403f-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f403f-324"><strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Finance and Operations kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="f403f-324">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="f403f-325">Bildirimlerin gönderileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="f403f-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="f403f-326">Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="f403f-327">Zaman limiti ayarlama</span><span class="sxs-lookup"><span data-stu-id="f403f-327">Set a time limit</span></span>
<span data-ttu-id="f403f-328">El ile görevin belirli bir süre içerisinde tamamlanması gerekiyorsa bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-328">Follow these steps if the manual task must be completed in a specific time.</span></span> 

<span data-ttu-id="f403f-329">**Not:** Bu yordamda belirlediğiniz seçenekler, sayfanın **Atama** ve **İlerletme** alanlarında belirlemiş olduğunuz seçenekleri geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="f403f-329">**Note:** The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1.  <span data-ttu-id="f403f-330">Sol bölmede **Gelişmiş ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-330">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="f403f-331">**İş akışı öğesi için bir zaman sınırı ayarlayın** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3.  <span data-ttu-id="f403f-332">**Süre** alanında, görevin ne zaman tamamlanması gerektiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f403f-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="f403f-333">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-333">Select one of the following options:</span></span>
    -   <span data-ttu-id="f403f-334">**Saatler** – Görevin tamamlaması gereken saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="f403f-335">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="f403f-336">**Günler** – Görevin tamamlaması gereken gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="f403f-337">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="f403f-338">**Haftalar** – Görevin tamamlaması gereken hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="f403f-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    -   <span data-ttu-id="f403f-339">**Aylar** – Görevin tamamlamış olması gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="f403f-340">Örneğin görevin ayın üçüncü haftasının Cuma gününden önce tamamlanmış olmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="f403f-341">**Yıllar** – Görevin tamamlamış olması gereken günü, haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="f403f-342">Örneğin görevin Aralık ayının üçüncü haftasının Cuma gününden önce tamamlanmış olmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f403f-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="f403f-343">Zaman limiti aşılırsa sistem görev üstünde eylem yapar.</span><span class="sxs-lookup"><span data-stu-id="f403f-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="f403f-344">**Eylem** listesinde sistemin gerçekleştirmesi gereken eylemi seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="f403f-345">Hangi eylemlerin kullanıcı tarafından kullanılabilir olacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="f403f-345">Specify which actions are available to the user</span></span>
<span data-ttu-id="f403f-346">El ile görev bir kullanıcıya atandığında kullanıcı görev üstünde eylem yapmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f403f-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="f403f-347">Kullanıcının görev üzerinde hangi eylemleri yapabileceğini belirtmek için bu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f403f-347">Follow these steps to specify which actions the user can take on the task.</span></span> <span data-ttu-id="f403f-348">**Not:** Gerçekleştirilebilecek eylemler, görevin tasarımına bağlı olarak değişebilir.</span><span class="sxs-lookup"><span data-stu-id="f403f-348">**Note:** The actions that are available vary, depending on the design of the task.</span></span>

1.  <span data-ttu-id="f403f-349">Sol bölmede **Gelişmiş ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f403f-349">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="f403f-350">Eğer kullanıcı görevi **Tamamlanmış** olarak işaretleyebilecekse, **Tamamlandı** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3.  <span data-ttu-id="f403f-351">Eğer kullanıcı gönderilen belgeyi reddedebilecekse, **Reddet** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4.  <span data-ttu-id="f403f-352">Kullanıcı gönderilen belgede değişiklik talep edebilecekse **Değişiklik iste** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f403f-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5.  <span data-ttu-id="f403f-353">Kullanıcı görevi başka bir kullanıcıya atayabilecekse **Temsilci seç** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6.  <span data-ttu-id="f403f-354">Kullanıcı görevi, iş öğesi kuyruğundaki başka bir kullanıcıya yeniden atayabilecekse **Yeniden Ata** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7.  <span data-ttu-id="f403f-355">Kullanıcı görevi, iş öğesi kuyruğundaki başka bir kullanıcıya serbest bırakabilecekse, **Serbest Bırak** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f403f-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="f403f-356">Daha sonra başka bir kullanıcı bu görevi tamamlayabilir.</span><span class="sxs-lookup"><span data-stu-id="f403f-356">Another user can then complete the task.</span></span>





