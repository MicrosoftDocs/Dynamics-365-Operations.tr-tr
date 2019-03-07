---
title: İş akışında el ile girilen kararları yapılandırma
description: Bu konu, el ile bir kararın özelliklerini yapılandırmayı açıklar.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d09e99a5bf99593a8fa7682f9d4f29eaa4e7c836
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "341408"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="50d34-103">İş akışında el ile girilen kararları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="50d34-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50d34-104">Bu konu, el ile bir kararın özelliklerini yapılandırmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="50d34-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="50d34-105">El ile bir kararı iş akışı düzenleyicisinde yapılandırmak için el ile karara sağ tıklatın ve sonra **Özellikler**'i açmak için **Özellikler** sayfanı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="50d34-106">Ardından el ile kararın özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="50d34-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="50d34-107">Kararın adı</span><span class="sxs-lookup"><span data-stu-id="50d34-107">Name the decision</span></span>

<span data-ttu-id="50d34-108">El ile karara bir ad vermek için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="50d34-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="50d34-109">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="50d34-110">**Ad** alanına, el ile karar için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="50d34-111">Konu satırı ve açıklamaları girme</span><span class="sxs-lookup"><span data-stu-id="50d34-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="50d34-112">Bu el ile karara atanmış olan kullanıcılara bir konu satırı ve açıklama sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="50d34-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="50d34-113">Örneğin, eğer satınalma talepleri için bir karar yapılandırıyorsanız, bu karara atanmış kullanıcı konu satırını ve yönergeleri **Satınalma talepleri** sayfasında görür.</span><span class="sxs-lookup"><span data-stu-id="50d34-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="50d34-114">Konu satırı sayfa üzerindeki bir ileti çubuğunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="50d34-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="50d34-115">Daha sonra, kullanıcı yönergeleri görüntülemek için ileti çubuğundaki simgeye tıklayabilir.</span><span class="sxs-lookup"><span data-stu-id="50d34-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="50d34-116">Konu satırını ve açıklamaları girmek için şu adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="50d34-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="50d34-117">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="50d34-118">**Yönergeler** sekmesinde, **Çalışma öğesi konusu** alanında, konu satırını girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="50d34-119">Konu satırını kişiselleştirmek için yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="50d34-120">Yer tutucular, konu satırı kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="50d34-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="50d34-121">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="50d34-122">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="50d34-123">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="50d34-124">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="50d34-125">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-125">Click **Insert**.</span></span>

4. <span data-ttu-id="50d34-126">Konu satırı çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="50d34-127">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="50d34-128">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="50d34-129">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="50d34-130">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="50d34-131">Metni kişiselleştirmek için, 3. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="50d34-132">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-132">Click **Close**.</span></span>

5. <span data-ttu-id="50d34-133">**Çalışma öğesi yönergeleri** alanında, yönergeleri girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="50d34-134">Yönergeleri kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="50d34-135">Yer tutucular, yönergeler kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="50d34-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="50d34-136">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="50d34-137">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="50d34-138">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="50d34-139">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="50d34-140">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-140">Click **Insert**.</span></span>

7. <span data-ttu-id="50d34-141">Yönergelerin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="50d34-142">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="50d34-143">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="50d34-144">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="50d34-145">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="50d34-146">Metni kişiselleştirmek için, 6. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="50d34-147">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="50d34-148">Bir kararın olası sonucunu belirtin</span><span class="sxs-lookup"><span data-stu-id="50d34-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="50d34-149">Genellikle bir belge bir karar vericiye atandığı zaman, karar vericiye bir soru sorulur.</span><span class="sxs-lookup"><span data-stu-id="50d34-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="50d34-150">Sorunun yanıtı genellikle **Evet** veya **Hayır** ya da **Doğru** veya **Yanlış** olur.</span><span class="sxs-lookup"><span data-stu-id="50d34-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="50d34-151">El ile kararın olası sonuçlarını belirtmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="50d34-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="50d34-152">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="50d34-153">**Sonuçlar** sekmesinde **Sonuç 1** alanında, sonucun adını veya seçeneği girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="50d34-154">Sonucun çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="50d34-155">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="50d34-156">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="50d34-157">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="50d34-158">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="50d34-159">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-159">Click **Close**.</span></span>

4. <span data-ttu-id="50d34-160">**Sonuç 2** alanında, sonucun adını veya seçeneği girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="50d34-161">Sonucun çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="50d34-162">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="50d34-163">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="50d34-164">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="50d34-165">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="50d34-166">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="50d34-167">Bildirimlerin ne zaman gönderileceğini belirtme</span><span class="sxs-lookup"><span data-stu-id="50d34-167">Specify when notifications are sent</span></span>

<span data-ttu-id="50d34-168">Bir karar alındığında, ilerletildiğinde veya yetkilendirildiğinde insanlara bildirim gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="50d34-169">Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="50d34-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="50d34-170">Sol bölmede **Bildirimler**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="50d34-171">Bildirimlerin gönderilmesi gerektiği etkinlikler için yanlarındaki onay kutusunu işaretleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="50d34-172">**\[Seçim 1\]** – Atanan kullanıcı **\[Seçim 1\]**'i işaretledi.</span><span class="sxs-lookup"><span data-stu-id="50d34-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="50d34-173">**\[Seçim 2\]** – Atanan kullanıcı **\[Seçim 2\]**'i işaretledi.</span><span class="sxs-lookup"><span data-stu-id="50d34-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="50d34-174">**Temsilci** – Atanmış kullanıcı kararı başka bir kullanıcıya atadı.</span><span class="sxs-lookup"><span data-stu-id="50d34-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="50d34-175">**İlerlet** – Atanmış kullanıcı, ayrılan sürede karar vermedi.</span><span class="sxs-lookup"><span data-stu-id="50d34-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="50d34-176">2. adımda seçtiğiniz bir olay için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="50d34-177">**Bildirim metni** sekmesinde, metin kutusuna, bildirimin metnini girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="50d34-178">Bildirimi kişiselleştirmek için yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="50d34-179">Yer tutucular, bildirim kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="50d34-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="50d34-180">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="50d34-181">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="50d34-182">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="50d34-183">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="50d34-184">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-184">Click **Insert**.</span></span>

6. <span data-ttu-id="50d34-185">Bildirimin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="50d34-186">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="50d34-187">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="50d34-188">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="50d34-189">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="50d34-190">Metni kişiselleştirmek için, 5. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="50d34-191">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-191">Click **Close**.</span></span>

7. <span data-ttu-id="50d34-192">**Alıcı** sekmesinde, bildirimlerin kime gönderildiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="50d34-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="50d34-193">Aşağıdaki tablodaki seçeneklerden birini seçin ve 8. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="50d34-194">Seçenek</span><span class="sxs-lookup"><span data-stu-id="50d34-194">Option</span></span></th>
    <th><span data-ttu-id="50d34-195">Bildirim alıcıları</span><span class="sxs-lookup"><span data-stu-id="50d34-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="50d34-196">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="50d34-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="50d34-197">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="50d34-197">Participant</span></span></td>
    <td><span data-ttu-id="50d34-198">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="50d34-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="50d34-199"><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, bildirimlerin gönderileceği grup ya da rolün türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="50d34-200"><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="50d34-201">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="50d34-201">Workflow user</span></span></td>
    <td><span data-ttu-id="50d34-202">Mevcut iş akışındaki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="50d34-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="50d34-203"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="50d34-204">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="50d34-204">User</span></span></td>
    <td><span data-ttu-id="50d34-205">Özel Microsoft Dynamics 365 for Finance and Operations kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="50d34-205">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="50d34-206"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="50d34-207"><strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Finance and Operations kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="50d34-207">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="50d34-208">Bildirimlerin gönderileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="50d34-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="50d34-209">Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="50d34-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="50d34-210">Bir karar ata</span><span class="sxs-lookup"><span data-stu-id="50d34-210">Assign a decision</span></span>

<span data-ttu-id="50d34-211">El ile kararın kime atanacağını belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="50d34-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="50d34-212">Sol bölmede **Atama**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="50d34-213">**Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 3. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="50d34-214">Seçenek</span><span class="sxs-lookup"><span data-stu-id="50d34-214">Option</span></span></th>
    <th><span data-ttu-id="50d34-215">Kararın atandığı kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="50d34-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="50d34-216">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="50d34-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="50d34-217">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="50d34-217">Participant</span></span></td>
    <td><span data-ttu-id="50d34-218">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="50d34-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="50d34-219"><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, kararın atanacağı grup ya da rolün türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="50d34-220"><strong>Katılımcı</strong> listesinde, kararın atanacağı grup veya rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="50d34-221">Hiyerarşi</span><span class="sxs-lookup"><span data-stu-id="50d34-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="50d34-222">Belirli bir kuruluş hiyerarşisindeki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="50d34-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="50d34-223"><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, kararın atanacağı hiyerarşi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="50d34-224">Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir.</span><span class="sxs-lookup"><span data-stu-id="50d34-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="50d34-225">Bu adlar, kararın atanabileceği kullanıcıları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="50d34-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="50d34-226">Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="50d34-227">Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="50d34-228">Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="50d34-229">Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="50d34-230"><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara kararın atanması gerektiğini belirtin:</span><span class="sxs-lookup"><span data-stu-id="50d34-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="50d34-231"><strong>Alınan tüm kullanıcılara ata</strong> – Karar, bu aralıktaki tüm kullanıcılara atanır.</span><span class="sxs-lookup"><span data-stu-id="50d34-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="50d34-232"><strong>Yalnızca alınan son kullanıcıya ata</strong> – Karar, yalnızca aralıktaki son kullanıcıya atanır.</span><span class="sxs-lookup"><span data-stu-id="50d34-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="50d34-233"><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Karar, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya atanmaz.</span><span class="sxs-lookup"><span data-stu-id="50d34-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="50d34-234">Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="50d34-235">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="50d34-235">Workflow user</span></span></td>
    <td><span data-ttu-id="50d34-236">Mevcut iş akışındaki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="50d34-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="50d34-237"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="50d34-238">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="50d34-238">User</span></span></td>
    <td><span data-ttu-id="50d34-239">Belirli Finance and Operations kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="50d34-239">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="50d34-240"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="50d34-241"><strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Finance and Operations kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="50d34-241">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="50d34-242">Kararın atanacağı kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="50d34-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="50d34-243">Kuyruk</span><span class="sxs-lookup"><span data-stu-id="50d34-243">Queue</span></span></td>
    <td><span data-ttu-id="50d34-244">Bir iş maddesi kuyruğu</span><span class="sxs-lookup"><span data-stu-id="50d34-244">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="50d34-245"><strong>Kuyruk</strong>'u seçtikten sonra <strong>Kuyruk tabanlı</strong> sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-245">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="50d34-246">Kararı belirli bir kuyruğa atamak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-246">To assign the decision to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="50d34-247"><strong>Kuyruk türü</strong> listesinde, <strong>İş öğesi kuyrukları</strong>'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-247">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="50d34-248"><strong>Kuyruk adı</strong> listesinde, kuyruğu seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-248">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="50d34-249">Eğer belirli bir koşulun kararının hangi kuyruğa atanacağını belirlemesi gerekiyorsa, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-249">If a specific condition should determine which queue the decision is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="50d34-250"><strong>Kuyruk türü</strong> listesinde, <strong>Koşullu iş öğesi kuyrukları</strong>'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-250">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="50d34-251"><strong>Kuyruk adı</strong> listesinde, <strong>Koşullu kuyruk</strong>'u seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-251">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="50d34-252">Bu seçenek yalnızca servis talebi yönetimi gibi bazı iş akışları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="50d34-252">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="50d34-253">**Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının kararı almak üzere ne kadar zamanı olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="50d34-253">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="50d34-254">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-254">Select one of the following options:</span></span>

    - <span data-ttu-id="50d34-255">**Saatler** – Kullanıcının kararı alması gereken saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-255">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="50d34-256">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-256">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="50d34-257">**Günler** – Kullanıcının kararı alması gereken gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-257">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="50d34-258">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-258">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="50d34-259">**Haftalar** – Kullanıcının kararı alması gereken hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-259">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="50d34-260">**Aylar** – Kullanıcının kararı almış olması gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-260">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="50d34-261">Örneğin kullanıcının kararı ayın üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-261">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="50d34-262">**Yıllar** – Kullanıcının kararı almış olması gereken haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-262">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="50d34-263">Örneğin kullanıcının kararı Aralık ayının üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-263">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="50d34-264">Eğer kullanıcı ayırılan zaman içerisinde kararı alamazsa, kararın vadesi geçer.</span><span class="sxs-lookup"><span data-stu-id="50d34-264">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="50d34-265">Vadesi geçmiş bir karar, sayfanın **İlerletme** bölgesinde işaretlemiş olduğunuz seçeneklere göre ilerletilir.</span><span class="sxs-lookup"><span data-stu-id="50d34-265">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="50d34-266">Bir kararın süresi geçtiğinde ne olacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="50d34-266">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="50d34-267">Eğer bir kullanıcı ayırılan zaman içerisinde kararı alamazsa, kararın vadesi geçer.</span><span class="sxs-lookup"><span data-stu-id="50d34-267">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="50d34-268">Vadesi geçmiş bir karar ilerletilebilir veya başka bir kullanıcıya otomatik olarak atanabilir.</span><span class="sxs-lookup"><span data-stu-id="50d34-268">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="50d34-269">Vadesi geçmiş ise, kararın üst düzeye ilerletilmesi için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="50d34-269">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="50d34-270">Sol bölmede **İlerletilme**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-270">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="50d34-271">İlerletme yolu oluşturmak için **İlerletme yolunu kullan** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-271">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="50d34-272">Sistem kararı ilerletme yolunda listelenmiş olan kullanıcılara otomatik olarak atar.</span><span class="sxs-lookup"><span data-stu-id="50d34-272">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="50d34-273">Örneğin, aşağıdaki tablo bir ilerletme yolunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="50d34-273">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="50d34-274">Seri</span><span class="sxs-lookup"><span data-stu-id="50d34-274">Sequence</span></span> | <span data-ttu-id="50d34-275">İlerletme yolu</span><span class="sxs-lookup"><span data-stu-id="50d34-275">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="50d34-276">1</span><span class="sxs-lookup"><span data-stu-id="50d34-276">1</span></span>        | <span data-ttu-id="50d34-277">Şu kişiye ata: Donna</span><span class="sxs-lookup"><span data-stu-id="50d34-277">Assign to: Donna</span></span>           |
    | <span data-ttu-id="50d34-278">2</span><span class="sxs-lookup"><span data-stu-id="50d34-278">2</span></span>        | <span data-ttu-id="50d34-279">Şu kişiye ata: Erin</span><span class="sxs-lookup"><span data-stu-id="50d34-279">Assign to: Erin</span></span>            |
    | <span data-ttu-id="50d34-280">3</span><span class="sxs-lookup"><span data-stu-id="50d34-280">3</span></span>        | <span data-ttu-id="50d34-281">Son eylem: \[Karar 1\]</span><span class="sxs-lookup"><span data-stu-id="50d34-281">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="50d34-282">Bu örnekte sistem süresi geçen kararı Donna'ya atar.</span><span class="sxs-lookup"><span data-stu-id="50d34-282">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="50d34-283">Eğer Donna ayırılan süre içerisinde kararı alamazsa, sistem kararı Erin'e atar.</span><span class="sxs-lookup"><span data-stu-id="50d34-283">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="50d34-284">Eğer Erin ayırılan süre içerisinde kararı alamazsa, sistem karar olarak **\[Karar 1\]**'i karar olarak seçer</span><span class="sxs-lookup"><span data-stu-id="50d34-284">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="50d34-285">Bir kullanıcıyı ilerletme yoluna eklemek için **İlerletme ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-285">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="50d34-286">Aşağıdaki tablodaki seçeneklerden birini seçin ve 4. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-286">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="50d34-287">Seçenek</span><span class="sxs-lookup"><span data-stu-id="50d34-287">Option</span></span></th>
    <th><span data-ttu-id="50d34-288">Kararın ilerletildiği kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="50d34-288">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="50d34-289">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="50d34-289">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="50d34-290">Hiyerarşi</span><span class="sxs-lookup"><span data-stu-id="50d34-290">Hierarchy</span></span></td>
    <td><span data-ttu-id="50d34-291">Belirli bir kuruluş hiyerarşisindeki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="50d34-291">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="50d34-292"><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, kararın ilerletileceği hiyerarşi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-292">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="50d34-293">Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir.</span><span class="sxs-lookup"><span data-stu-id="50d34-293">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="50d34-294">Bu adlar kararın ilerletilebileceği kullanıcıları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="50d34-294">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="50d34-295">Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-295">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="50d34-296">Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-296">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="50d34-297">Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-297">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="50d34-298">Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-298">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="50d34-299"><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara kararın ilerletilmesi gerektiğini belirtin:</span><span class="sxs-lookup"><span data-stu-id="50d34-299">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="50d34-300"><strong>Alınan tüm kullanıcılara ata</strong> – Karar bu aralıktaki tüm kullanıcılara ilerletilir.</span><span class="sxs-lookup"><span data-stu-id="50d34-300"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="50d34-301"><strong>Yalnızca alınan son kullanıcıya ata</strong> – Karar yalnızca aralıktaki son kullanıcıya ilerletilir.</span><span class="sxs-lookup"><span data-stu-id="50d34-301"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="50d34-302"><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak:</strong> – Karar, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya ilerletilmez.</span><span class="sxs-lookup"><span data-stu-id="50d34-302"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="50d34-303">Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-303">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="50d34-304">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="50d34-304">Workflow user</span></span></td>
    <td><span data-ttu-id="50d34-305">Mevcut iş akışındaki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="50d34-305">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="50d34-306"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-306">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="50d34-307">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="50d34-307">User</span></span></td>
    <td><span data-ttu-id="50d34-308">Belirli Finance and Operations kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="50d34-308">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="50d34-309"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50d34-309">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="50d34-310"><strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Finance and Operations kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="50d34-310">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="50d34-311">Kararın ilerletileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="50d34-311">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="50d34-312">**Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının kararı almak üzere ne kadar zamanı olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="50d34-312">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="50d34-313">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-313">Select one of the following options:</span></span>

    - <span data-ttu-id="50d34-314">**Saatler** – Kullanıcının kararı alması gereken saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-314">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="50d34-315">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-315">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="50d34-316">**Günler** – Kullanıcının kararı alması gereken gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-316">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="50d34-317">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-317">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="50d34-318">**Haftalar** – Kullanıcının kararı alması gereken hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-318">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="50d34-319">**Aylar** – Kullanıcının kararı almış olması gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-319">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="50d34-320">Örneğin kullanıcının kararı ayın üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-320">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="50d34-321">**Yıllar** – Kullanıcının kararı almış olması gereken haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-321">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="50d34-322">Örneğin kullanıcının kararı Aralık ayının üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-322">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="50d34-323">İlerletme yoluna eklenecek tüm kullanıcılar için 3. adım ve 4. adımlar arasındaki süreci yineleyin.</span><span class="sxs-lookup"><span data-stu-id="50d34-323">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="50d34-324">Kullanıcıların sıralamasını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-324">You can change the order of the users.</span></span>
6. <span data-ttu-id="50d34-325">İlerletme yolundaki kullanıcılar verilen süre içinde kararı alamazsa, sistem görev üstünde karar alır.</span><span class="sxs-lookup"><span data-stu-id="50d34-325">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="50d34-326">Sistemin seçeceği seçeneği belirtmek için **Eylem** satırını seçin ve sonra **Eylemi bitir** sekmesi üzerinde bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-326">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="50d34-327">Zaman limiti ayarlama</span><span class="sxs-lookup"><span data-stu-id="50d34-327">Set a time limit</span></span>

<span data-ttu-id="50d34-328">Kararın belirli bir süre içerisinde alınması gerekiyorsa bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="50d34-328">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="50d34-329">Bu yordamda belirlediğiniz seçenekler, sayfanın **Atama** ve **İlerletme** alanlarında belirlemiş olduğunuz seçenekleri geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="50d34-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="50d34-330">Sol bölmede **Gelişmiş ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50d34-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="50d34-331">**İş akışı öğesi için bir zaman sınırı ayarlayın** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="50d34-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="50d34-332">**Süre** alanında, kararın ne zaman alınması gerektiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="50d34-332">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="50d34-333">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="50d34-333">Select one of the following options:</span></span>

    - <span data-ttu-id="50d34-334">**Saatler** – Saatlerin sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-334">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="50d34-335">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="50d34-336">**Günler** – Günlerin sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-336">**Days** – Enter the number of days.</span></span> <span data-ttu-id="50d34-337">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="50d34-338">**Haftalar** – Haftaların sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="50d34-338">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="50d34-339">**Aylar** – Kararın alınmış olması gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-339">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="50d34-340">Örneğin kararın ayın üçüncü haftasının Cuma gününden önce alınmış olmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-340">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="50d34-341">**Yıllar** – Kararın alınmış olması gereken günü, haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-341">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="50d34-342">Örneğin kararın Aralık ayının üçüncü haftasının Cuma gününden önce alınmış olmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50d34-342">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="50d34-343">Zaman limiti aşılırsa sistem kararı kendi alır.</span><span class="sxs-lookup"><span data-stu-id="50d34-343">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="50d34-344">**Eylem** listesinden sistemin tercih etmesi gereken seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="50d34-344">In the **Action** list, select the option that the system should select.</span></span>
