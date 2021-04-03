---
title: İş akışında onay adımlarını yapılandırma
description: Bu konu, bir onay adımının özelliklerini yapılandırmayı açıklar.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5442b7db0a1ccd2a2e07faf8635ac12ff06c560
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565746"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="2a5aa-103">İş akışında onay adımlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2a5aa-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a5aa-104">Bu konu, bir onay adımının özelliklerini yapılandırmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="2a5aa-105">Bir onay adımını iş akışı düzenleyicisinde yapılandırmak için onay adımına sağ tıklatın ve sonra **Özellikler**'i açmak için **Özellikler** sayfanı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="2a5aa-106">Ardından onay adımının özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="2a5aa-107">Adımı adlandırma</span><span class="sxs-lookup"><span data-stu-id="2a5aa-107">Name the step</span></span>
<span data-ttu-id="2a5aa-108">Onay adımına bir ad vermek için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="2a5aa-109">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2a5aa-110">**Ad** alanına onay adımı için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="2a5aa-111">Konu satırı ve açıklamaları girme</span><span class="sxs-lookup"><span data-stu-id="2a5aa-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="2a5aa-112">Bu onay adımına atanmış olan kullanıcılara bir konu satırı ve açıklama sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="2a5aa-113">Örneğin, eğer satınalma talepleri için bir onay adımı yapılandırıyorsanız, bu adıma atanmış kullanıcı konu satırını ve yönergeleri **Satınalma talepleri** sayfasında görür.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="2a5aa-114">Konu satırı sayfa üzerindeki bir ileti çubuğunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="2a5aa-115">Daha sonra, kullanıcı yönergeleri görmek için ileti çubuğundaki simgeye tıklayabilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="2a5aa-116">Konu satırını ve açıklamaları girmek için şu adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="2a5aa-117">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2a5aa-118">**Çalışma öğesi konusu** alanında, konu satırını girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="2a5aa-119">Konu satırını kişiselleştirmek için yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="2a5aa-120">Yer tutucular, konu satırı kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="2a5aa-121">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2a5aa-122">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2a5aa-123">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2a5aa-124">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2a5aa-125">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-125">Click **Insert**.</span></span>

4. <span data-ttu-id="2a5aa-126">Konu satırı çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="2a5aa-127">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="2a5aa-128">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2a5aa-129">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2a5aa-130">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2a5aa-131">Metni kişiselleştirmek için, 3. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="2a5aa-132">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-132">Click **Close**.</span></span>

5. <span data-ttu-id="2a5aa-133">**Çalışma öğesi yönergeleri** alanında, yönergeleri girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="2a5aa-134">Yönergeleri kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="2a5aa-135">Yer tutucular, yönergeler kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="2a5aa-136">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2a5aa-137">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2a5aa-138">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2a5aa-139">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2a5aa-140">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-140">Click **Insert**.</span></span>

7. <span data-ttu-id="2a5aa-141">Yönergelerin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="2a5aa-142">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="2a5aa-143">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2a5aa-144">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2a5aa-145">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2a5aa-146">Metni kişiselleştirmek için, 6. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="2a5aa-147">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="2a5aa-148">Onay adımını atama</span><span class="sxs-lookup"><span data-stu-id="2a5aa-148">Assign the approval step</span></span>

<span data-ttu-id="2a5aa-149">Onay adımının kime atanacağını belirtmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="2a5aa-150">Sol bölmede **Atama**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="2a5aa-151">**Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 3. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2a5aa-152">Seçenek</span><span class="sxs-lookup"><span data-stu-id="2a5aa-152">Option</span></span></th>
    <th><span data-ttu-id="2a5aa-153">Onay adımının atandığı kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="2a5aa-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="2a5aa-154">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="2a5aa-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2a5aa-155">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="2a5aa-155">Participant</span></span></td>
    <td><span data-ttu-id="2a5aa-156">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="2a5aa-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2a5aa-157"><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, adımın atanacağı grup ya da rolün türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="2a5aa-158"><strong>Katılımcı</strong> listesinde, adımın atanacağı grup veya rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2a5aa-159">Hiyerarşi</span><span class="sxs-lookup"><span data-stu-id="2a5aa-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="2a5aa-160">Belirli bir kuruluş hiyerarşisindeki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="2a5aa-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2a5aa-161"><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, adımın atanacağı hiyerarşi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="2a5aa-162">Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2a5aa-163">Bu adlar, adımın atanabileceği kullanıcıları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="2a5aa-164">Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2a5aa-165">Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2a5aa-166">Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2a5aa-167">Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2a5aa-168"><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara adımın atanması gerektiğini belirtin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="2a5aa-169"><strong>Alınan tüm kullanıcılara ata</strong> – Adım, bu aralıktaki tüm kullanıcılara atanır.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="2a5aa-170"><strong>Yalnızca alınan son kullanıcıya ata</strong> – Adım, yalnızca aralıktaki son kullanıcıya atanır.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2a5aa-171"><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Adım, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya atanmaz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="2a5aa-172">Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2a5aa-173">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="2a5aa-173">Workflow user</span></span></td>
    <td><span data-ttu-id="2a5aa-174">Mevcut iş akışındaki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="2a5aa-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2a5aa-175"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2a5aa-176">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="2a5aa-176">User</span></span></td>
    <td><span data-ttu-id="2a5aa-177">Belirli kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="2a5aa-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2a5aa-178"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2a5aa-179"><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm sistem kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="2a5aa-180">Adımların atanacağı kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="2a5aa-181">**Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının onay adımına ulaşan belgelere yanıt vermek veya bunlar üzerinde eyleme geçmek üzere ne kadar zamanı olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="2a5aa-182">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-182">Select one of the following options:</span></span>

    - <span data-ttu-id="2a5aa-183">**Saatler** – Kullanıcının yanıt vermesi gereken saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="2a5aa-184">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2a5aa-185">**Günler** – Kullanıcının yanıt vermesi gereken gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="2a5aa-186">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2a5aa-187">**Haftalar** – Kullanıcının yanıt vermesi gereken hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="2a5aa-188">**Aylar** – Kullanıcının yanıt vermesi gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="2a5aa-189">Örneğin, kullanıcının ayın üçüncü haftasındaki Cuma günü yanıt vermesini isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2a5aa-190">**Yıllar** – Kullanıcının yanıt vermesi gereken haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="2a5aa-191">Örneğin, kullanıcının Aralık ayının üçüncü haftasındaki Cuma günü yanıt vermesini isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="2a5aa-192">Eğer kullanıcı bu zaman içerisinde belge üzerinde eyleme geçmezse, belgenin vadesi geçer.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="2a5aa-193">Vadesi geçmiş bir belge, sayfanın **İlerletme** bölgesinde işaretlemiş olduğunuz seçeneklere göre ilerletilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="2a5aa-194">Eğer onay adımını birden fazla kullanıcıya ya da bir kullanıcı grubuna atadıysanız, **Tamamlanma ilkesi** sekmesinde aşağıdaki seçeneklerden birini işaretleyin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="2a5aa-195">**Tek onaylayan** – Belgeye uygulanan eylem, yanıt veren ilk kişi tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="2a5aa-196">Örneğin, Sam 15.000 USD tutarında bir gider raporu gönderdi.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="2a5aa-197">Gider raporu şu an Sue, Jo ve Bill'e atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="2a5aa-198">Eğer Sue belgeye ilk yanıt veren kişi olursa, onun aldığı eylem belgeye uygulanır.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="2a5aa-199">Sue belgeyi reddederse, belge reddedilir ve Sam'e geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="2a5aa-200">Sue belgeyi onaylarsa, onaylanmak üzere Ann'e gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![Onay işlemine sahip bir iş akışı](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="2a5aa-202">**Onaylayanların çoğunluğu** – Belgeye uygulanan eylem, onaylayanların çoğunluğu yanıt verdiğinde belirlenir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="2a5aa-203">Örneğin, Sam 15.000 USD tutarında bir gider raporu gönderdi.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="2a5aa-204">Gider raporu şu an Sue, Jo ve Bill'e atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="2a5aa-205">Eğer Sue ve Jo yanıt veren ilk iki kişiyse, aldıkları eylem belgeye uygulanır.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="2a5aa-206">Sue belgeyi onaylar ama Jo reddederse, belge reddedilir ve Sam'e geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="2a5aa-207">Eğer hem Sue hem de Jo belgeye onay verirse, onay için Ann'e gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="2a5aa-208">**Onaylayanların yüzdesi** – Belgeye uygulanan eylem, onaylayanların belirli bir yüzdesi yanıt verdiğinde belirlenir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="2a5aa-209">Örneğin, Sam 15.000 USD tutarında bir gider raporu gönderdi.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="2a5aa-210">Gider raporu şu anda Sue, Jo ve Bill'e atanmıştır ve oran olarak **50** girdiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="2a5aa-211">Eğer Sue ve Jo yanıt veren ilk iki kişi olurlarsa, onların aldıkları eylem belgeye uygulanır çünkü onaylayanların yüzde 50'si gereksinimini karşılamaktadırlar.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="2a5aa-212">Sue belgeyi onaylar ama Jo reddederse, belge reddedilir ve Sam'e geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="2a5aa-213">Eğer hem Sue hem de Jo belgeye onay verirse, onay için Ann'e gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="2a5aa-214">**Tüm onaylayanlar** – Tüm onaylayanlar belgeyi onaylamalıdırlar.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="2a5aa-215">Aksi halde, iş akışı devam edemez.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="2a5aa-216">Örneğin, Sam 15.000 USD tutarında bir gider raporu gönderdi.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="2a5aa-217">Gider raporu şu an Sue, Jo ve Bill'e atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="2a5aa-218">Sue ve Joe belgeye onay verir fakat Bill reddederse, belge reddedilir ve Sam'e geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="2a5aa-219">Eğer Sue, Jo ve Bill'in tamamı belgeye onay verirse, onay için Ann'e gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="2a5aa-220">Onay adımının ne zaman gerekli olduğunu belirtin</span><span class="sxs-lookup"><span data-stu-id="2a5aa-220">Specify when the approval step is required</span></span>

<span data-ttu-id="2a5aa-221">Onay adımının ne zaman gerekli olduğunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="2a5aa-222">Onay adımı her zaman gerekli olabilir veya yalnızca belirli koşullar sağlanırsa gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="2a5aa-223">Onay adımı her zaman gereklidir</span><span class="sxs-lookup"><span data-stu-id="2a5aa-223">The approval step is always required</span></span>

<span data-ttu-id="2a5aa-224">Onay adımı her zaman gerekli ise, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="2a5aa-225">Sol bölmede **Koşul**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="2a5aa-226">**Bu adımı her zaman çalıştır** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="2a5aa-227">Onay adımı belirli koşullarda gerekiyor</span><span class="sxs-lookup"><span data-stu-id="2a5aa-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="2a5aa-228">Yapılandırmakta olduğunuz onay adımı yalnızca belirli koşullar sağlandığında gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="2a5aa-229">Örneğin, satınalma talebi iş akışı için bir onay adımı yapılandırıyorsanız, onay adımının yalnızca satın alma talebi 10.000 USD'den fazla olduğunu gerçekleşmesini isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="2a5aa-230">Onay adımının ne zaman gerekli olduğunu belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="2a5aa-231">Sol bölmede **Koşul**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="2a5aa-232">**Bu adımı yalnızca aşağıdaki koşul karşılandığında çalıştır** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="2a5aa-233">Koşulu girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-233">Enter a condition.</span></span>
4. <span data-ttu-id="2a5aa-234">Varsa, gerekli ek koşulları girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="2a5aa-235">Girdiğiniz koşulların doğru biçimde yapılandırıldığını doğrulamak için, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="2a5aa-236">**Sına**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-236">Click **Test**.</span></span>
    2. <span data-ttu-id="2a5aa-237">**İş akışını test et** sayfasında, **Koşulu doğrula** alanında, bir kayıt seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="2a5aa-238">**Sına**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-238">Click **Test**.</span></span> <span data-ttu-id="2a5aa-239">Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="2a5aa-240">**Özellikler** sayfasında geri dönmek için **OK** ya da **İptal Et**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="2a5aa-241">Belgenin vadesi geçtiğinde ne olduğunu belirtin</span><span class="sxs-lookup"><span data-stu-id="2a5aa-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="2a5aa-242">Eğer bir kullanıcı bu zaman içerisinde bir belge üzerinde eyleme geçmezse, belgenin vadesi geçer.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="2a5aa-243">Vadesi geçmiş bir belge ilerletilebilir veya onay için başka bir kullanıcıya otomatik olarak atanabilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="2a5aa-244">Vadesi geçmiş ise, belgenin üst düzeye ilerletilmesi için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="2a5aa-245">Sol bölmede **İlerletilme**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="2a5aa-246">İlerletme yolu oluşturmak için **İlerletme yolunu kullan** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="2a5aa-247">Sistem belgeyi ilerletme yolunda listelenmiş olan kullanıcılara otomatik olarak atar.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="2a5aa-248">Örneğin, aşağıdaki tablo bir ilerletme yolunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="2a5aa-249">Seri</span><span class="sxs-lookup"><span data-stu-id="2a5aa-249">Sequence</span></span> | <span data-ttu-id="2a5aa-250">İlerletme yolu</span><span class="sxs-lookup"><span data-stu-id="2a5aa-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="2a5aa-251">1</span><span class="sxs-lookup"><span data-stu-id="2a5aa-251">1</span></span>        | <span data-ttu-id="2a5aa-252">Şu kişiye ata: Donna</span><span class="sxs-lookup"><span data-stu-id="2a5aa-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="2a5aa-253">2</span><span class="sxs-lookup"><span data-stu-id="2a5aa-253">2</span></span>        | <span data-ttu-id="2a5aa-254">Şu kişiye ata: Erin</span><span class="sxs-lookup"><span data-stu-id="2a5aa-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="2a5aa-255">3</span><span class="sxs-lookup"><span data-stu-id="2a5aa-255">3</span></span>        | <span data-ttu-id="2a5aa-256">Son eylem: Reddet</span><span class="sxs-lookup"><span data-stu-id="2a5aa-256">Final action: Reject</span></span> |

    <span data-ttu-id="2a5aa-257">Bu örnekte sistem süresi geçen belgeyi Donna'ya atar.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="2a5aa-258">Eğer Donna ayrılan süre içerisinde yanıt vermezse, sistem belgeyi Erin'e atar.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="2a5aa-259">Eğer Erin ayrılan süre içerisinde yanıt vermezse, sistem belgeyi reddeder.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="2a5aa-260">Bir kullanıcıyı ilerletme yoluna eklemek için **İlerletme ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="2a5aa-261">**Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 4. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2a5aa-262">Seçenek</span><span class="sxs-lookup"><span data-stu-id="2a5aa-262">Option</span></span></th>
    <th><span data-ttu-id="2a5aa-263">Belgenin ilerletildiği kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="2a5aa-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="2a5aa-264">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="2a5aa-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2a5aa-265">Hiyerarşi</span><span class="sxs-lookup"><span data-stu-id="2a5aa-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="2a5aa-266">Belirli bir kuruluş hiyerarşisindeki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="2a5aa-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2a5aa-267"><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, belgenin ilerletileceği hiyerarşi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="2a5aa-268">Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2a5aa-269">Bu adlar belgenin ilerletilebileceği kullanıcıları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="2a5aa-270">Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2a5aa-271">Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2a5aa-272">Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2a5aa-273">Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2a5aa-274"><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara belgenin ilerletilmesi gerektiğini belirtin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="2a5aa-275"><strong>Alınan tüm kullanıcılara ata</strong> – Belge bu aralıktaki tüm kullanıcılara ilerletilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="2a5aa-276"><strong>Yalnızca alınan son kullanıcıya ata</strong> – Belge yalnızca aralıktaki son kullanıcıya ilerletilir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2a5aa-277"><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Belge, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya ilerletilmez.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="2a5aa-278">Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2a5aa-279">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="2a5aa-279">Workflow user</span></span></td>
    <td><span data-ttu-id="2a5aa-280">Mevcut iş akışındaki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="2a5aa-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2a5aa-281"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2a5aa-282">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="2a5aa-282">User</span></span></td>
    <td><span data-ttu-id="2a5aa-283">Belirli kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="2a5aa-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2a5aa-284"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2a5aa-285"><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm  kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="2a5aa-286">Belgenin ilerletileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="2a5aa-287">**Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının onay adımına ulaşan belgeler üzerinde eyleme geçmek üzere ne kadar zamanı olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="2a5aa-288">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="2a5aa-288">Select one of the following options:</span></span>

    - <span data-ttu-id="2a5aa-289">**Saatler** – Kullanıcının yanıt vermesi gereken saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="2a5aa-290">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2a5aa-291">**Günler** – Kullanıcının yanıt vermesi gereken gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="2a5aa-292">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2a5aa-293">**Haftalar** – Kullanıcının yanıt vermesi gereken hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="2a5aa-294">**Aylar** – Kullanıcının yanıt vermesi gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="2a5aa-295">Örneğin, kullanıcının ayın üçüncü haftasındaki Cuma günü yanıt vermesini isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2a5aa-296">**Yıllar** – Kullanıcının yanıt vermesi gereken haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="2a5aa-297">Örneğin, kullanıcının Aralık ayının üçüncü haftasındaki Cuma günü yanıt vermesini isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="2a5aa-298">İlerletme yoluna eklenecek tüm kullanıcılar için 3. adım ve 4. adımlar arasındaki süreci yineleyin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="2a5aa-299">Kullanıcıların sıralamasını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="2a5aa-300">İlerletme yolundaki kullanıcılar verilen süre içinde yanıt vermezlerse, sistem belge üstünde otomatik olarak eylem yapar.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="2a5aa-301">Sistemin alacağı eylemi belirtmek için **Eylem** satırını seçin ve sonra **Eylemi bitir** sekmesi üzerinde bir eylem seçin.</span><span class="sxs-lookup"><span data-stu-id="2a5aa-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]