---
title: İş akışında el ile girilen kararları yapılandırma
description: Bu konu, el ile bir kararın özelliklerini yapılandırmayı açıklar.
author: ChrisGarty
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e16ed97351423a50aff433d535ea4c575d97e7fd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747891"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="47a3c-103">İş akışında el ile girilen kararları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="47a3c-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47a3c-104">Bu konu, el ile bir kararın özelliklerini yapılandırmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="47a3c-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="47a3c-105">El ile bir kararı iş akışı düzenleyicisinde yapılandırmak için el ile karara sağ tıklatın ve sonra **Özellikler**'i açmak için **Özellikler** sayfanı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="47a3c-106">Ardından el ile kararın özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="47a3c-107">Kararın adı</span><span class="sxs-lookup"><span data-stu-id="47a3c-107">Name the decision</span></span>

<span data-ttu-id="47a3c-108">El ile karara bir ad vermek için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="47a3c-109">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="47a3c-110">**Ad** alanına, el ile karar için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="47a3c-111">Konu satırı ve açıklamaları girme</span><span class="sxs-lookup"><span data-stu-id="47a3c-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="47a3c-112">Bu el ile karara atanmış olan kullanıcılara bir konu satırı ve açıklama sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="47a3c-113">Örneğin, eğer satınalma talepleri için bir karar yapılandırıyorsanız, bu karara atanmış kullanıcı konu satırını ve yönergeleri **Satınalma talepleri** sayfasında görür.</span><span class="sxs-lookup"><span data-stu-id="47a3c-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="47a3c-114">Konu satırı sayfa üzerindeki bir ileti çubuğunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="47a3c-115">Daha sonra, kullanıcı yönergeleri görüntülemek için ileti çubuğundaki simgeye tıklayabilir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="47a3c-116">Konu satırını ve açıklamaları girmek için şu adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="47a3c-117">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="47a3c-118">**Yönergeler** sekmesinde, **Çalışma öğesi konusu** alanında, konu satırını girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="47a3c-119">Konu satırını kişiselleştirmek için yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="47a3c-120">Yer tutucular, konu satırı kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="47a3c-121">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="47a3c-122">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="47a3c-123">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="47a3c-124">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="47a3c-125">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-125">Click **Insert**.</span></span>

4. <span data-ttu-id="47a3c-126">Konu satırı çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="47a3c-127">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="47a3c-128">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="47a3c-129">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="47a3c-130">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="47a3c-131">Metni kişiselleştirmek için, 3. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="47a3c-132">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-132">Click **Close**.</span></span>

5. <span data-ttu-id="47a3c-133">**Çalışma öğesi yönergeleri** alanında, yönergeleri girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="47a3c-134">Yönergeleri kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="47a3c-135">Yer tutucular, yönergeler kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="47a3c-136">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="47a3c-137">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="47a3c-138">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="47a3c-139">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="47a3c-140">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-140">Click **Insert**.</span></span>

7. <span data-ttu-id="47a3c-141">Yönergelerin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="47a3c-142">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="47a3c-143">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="47a3c-144">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="47a3c-145">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="47a3c-146">Metni kişiselleştirmek için, 6. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="47a3c-147">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="47a3c-148">Bir kararın olası sonucunu belirtin</span><span class="sxs-lookup"><span data-stu-id="47a3c-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="47a3c-149">Genellikle bir belge bir karar vericiye atandığı zaman, karar vericiye bir soru sorulur.</span><span class="sxs-lookup"><span data-stu-id="47a3c-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="47a3c-150">Sorunun yanıtı genellikle **Evet** veya **Hayır** ya da **Doğru** veya **Yanlış** olur.</span><span class="sxs-lookup"><span data-stu-id="47a3c-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="47a3c-151">El ile kararın olası sonuçlarını belirtmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="47a3c-152">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="47a3c-153">**Sonuçlar** sekmesinde **Sonuç 1** alanında, sonucun adını veya seçeneği girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="47a3c-154">Sonucun çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="47a3c-155">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="47a3c-156">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="47a3c-157">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="47a3c-158">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="47a3c-159">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-159">Click **Close**.</span></span>

4. <span data-ttu-id="47a3c-160">**Sonuç 2** alanında, sonucun adını veya seçeneği girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="47a3c-161">Sonucun çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="47a3c-162">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="47a3c-163">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="47a3c-164">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="47a3c-165">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="47a3c-166">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="47a3c-167">Bildirimlerin ne zaman gönderileceğini belirtme</span><span class="sxs-lookup"><span data-stu-id="47a3c-167">Specify when notifications are sent</span></span>

<span data-ttu-id="47a3c-168">Bir karar alındığında, ilerletildiğinde veya yetkilendirildiğinde insanlara bildirim gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="47a3c-169">Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="47a3c-170">Sol bölmede **Bildirimler**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="47a3c-171">Bildirimlerin gönderilmesi gerektiği etkinlikler için yanlarındaki onay kutusunu işaretleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="47a3c-172">**\[Seçim 1\]** – Atanan kullanıcı **\[Seçim 1\]**'i işaretledi.</span><span class="sxs-lookup"><span data-stu-id="47a3c-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="47a3c-173">**\[Seçim 2\]** – Atanan kullanıcı **\[Seçim 2\]**'i işaretledi.</span><span class="sxs-lookup"><span data-stu-id="47a3c-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="47a3c-174">**Temsilci** – Atanmış kullanıcı kararı başka bir kullanıcıya atadı.</span><span class="sxs-lookup"><span data-stu-id="47a3c-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="47a3c-175">**İlerlet** – Atanmış kullanıcı, ayrılan sürede karar vermedi.</span><span class="sxs-lookup"><span data-stu-id="47a3c-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="47a3c-176">2. adımda seçtiğiniz bir olay için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="47a3c-177">**Bildirim metni** sekmesinde, metin kutusuna, bildirimin metnini girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="47a3c-178">Bildirimi kişiselleştirmek için yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="47a3c-179">Yer tutucular, bildirim kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="47a3c-180">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="47a3c-181">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="47a3c-182">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="47a3c-183">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="47a3c-184">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-184">Click **Insert**.</span></span>

6. <span data-ttu-id="47a3c-185">Bildirimin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="47a3c-186">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="47a3c-187">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="47a3c-188">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="47a3c-189">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="47a3c-190">Metni kişiselleştirmek için, 5. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="47a3c-191">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-191">Click **Close**.</span></span>

7. <span data-ttu-id="47a3c-192">**Alıcı** sekmesinde, bildirimlerin kime gönderildiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="47a3c-193">Aşağıdaki tablodaki seçeneklerden birini seçin ve 8. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="47a3c-194">Seçenek</span><span class="sxs-lookup"><span data-stu-id="47a3c-194">Option</span></span></th>
    <th><span data-ttu-id="47a3c-195">Bildirim alıcıları</span><span class="sxs-lookup"><span data-stu-id="47a3c-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="47a3c-196">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="47a3c-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="47a3c-197">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="47a3c-197">Participant</span></span></td>
    <td><span data-ttu-id="47a3c-198">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="47a3c-199"><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, bildirimlerin gönderileceği grup ya da rolün türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="47a3c-200"><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="47a3c-201">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="47a3c-201">Workflow user</span></span></td>
    <td><span data-ttu-id="47a3c-202">Mevcut iş akışındaki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="47a3c-203"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="47a3c-204">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="47a3c-204">User</span></span></td>
    <td><span data-ttu-id="47a3c-205">Belirli kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="47a3c-206"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="47a3c-207"><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm  kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="47a3c-208">Bildirimlerin gönderileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="47a3c-209">Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="47a3c-210">Bir karar ata</span><span class="sxs-lookup"><span data-stu-id="47a3c-210">Assign a decision</span></span>

<span data-ttu-id="47a3c-211">El ile kararın kime atanacağını belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="47a3c-212">Sol bölmede **Atama**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="47a3c-213">**Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 3. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="47a3c-214">Seçenek</span><span class="sxs-lookup"><span data-stu-id="47a3c-214">Option</span></span></th>
    <th><span data-ttu-id="47a3c-215">Kararın atandığı kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="47a3c-216">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="47a3c-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="47a3c-217">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="47a3c-217">Participant</span></span></td>
    <td><span data-ttu-id="47a3c-218">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="47a3c-219"><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, kararın atanacağı grup ya da rolün türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="47a3c-220"><strong>Katılımcı</strong> listesinde, kararın atanacağı grup veya rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="47a3c-221">Hiyerarşi</span><span class="sxs-lookup"><span data-stu-id="47a3c-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="47a3c-222">Belirli bir kuruluş hiyerarşisindeki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="47a3c-223"><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, kararın atanacağı hiyerarşi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="47a3c-224">Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="47a3c-225">Bu adlar, kararın atanabileceği kullanıcıları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="47a3c-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="47a3c-226">Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="47a3c-227">Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="47a3c-228">Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="47a3c-229">Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="47a3c-230"><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara kararın atanması gerektiğini belirtin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="47a3c-231"><strong>Alınan tüm kullanıcılara ata</strong> – Karar, bu aralıktaki tüm kullanıcılara atanır.</span><span class="sxs-lookup"><span data-stu-id="47a3c-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="47a3c-232"><strong>Yalnızca alınan son kullanıcıya ata</strong> – Karar, yalnızca aralıktaki son kullanıcıya atanır.</span><span class="sxs-lookup"><span data-stu-id="47a3c-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="47a3c-233"><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Karar, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya atanmaz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="47a3c-234">Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="47a3c-235">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="47a3c-235">Workflow user</span></span></td>
    <td><span data-ttu-id="47a3c-236">Mevcut iş akışındaki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="47a3c-237"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="47a3c-238">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="47a3c-238">User</span></span></td>
    <td><span data-ttu-id="47a3c-239">Belirli kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="47a3c-240"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="47a3c-241"><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm  kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="47a3c-242">Kararın atanacağı kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="47a3c-243">**Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının kararı almak üzere ne kadar zamanı olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="47a3c-244">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-244">Select one of the following options:</span></span>

    - <span data-ttu-id="47a3c-245">**Saatler** – Kullanıcının kararı alması gereken saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="47a3c-246">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="47a3c-247">**Günler** – Kullanıcının kararı alması gereken gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="47a3c-248">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="47a3c-249">**Haftalar** – Kullanıcının kararı alması gereken hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="47a3c-250">**Aylar** – Kullanıcının kararı almış olması gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="47a3c-251">Örneğin kullanıcının kararı ayın üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="47a3c-252">**Yıllar** – Kullanıcının kararı almış olması gereken haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="47a3c-253">Örneğin kullanıcının kararı Aralık ayının üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="47a3c-254">Eğer kullanıcı ayırılan zaman içerisinde kararı alamazsa, kararın vadesi geçer.</span><span class="sxs-lookup"><span data-stu-id="47a3c-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="47a3c-255">Vadesi geçmiş bir karar, sayfanın **İlerletme** bölgesinde işaretlemiş olduğunuz seçeneklere göre ilerletilir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="47a3c-256">Bir kararın süresi geçtiğinde ne olacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="47a3c-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="47a3c-257">Eğer bir kullanıcı ayırılan zaman içerisinde kararı alamazsa, kararın vadesi geçer.</span><span class="sxs-lookup"><span data-stu-id="47a3c-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="47a3c-258">Vadesi geçmiş bir karar ilerletilebilir veya başka bir kullanıcıya otomatik olarak atanabilir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="47a3c-259">Vadesi geçmiş ise, kararın üst düzeye ilerletilmesi için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="47a3c-260">Sol bölmede **İlerletilme**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="47a3c-261">İlerletme yolu oluşturmak için **İlerletme yolunu kullan** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="47a3c-262">Sistem kararı ilerletme yolunda listelenmiş olan kullanıcılara otomatik olarak atar.</span><span class="sxs-lookup"><span data-stu-id="47a3c-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="47a3c-263">Örneğin, aşağıdaki tablo bir ilerletme yolunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="47a3c-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="47a3c-264">Seri</span><span class="sxs-lookup"><span data-stu-id="47a3c-264">Sequence</span></span> | <span data-ttu-id="47a3c-265">İlerletme yolu</span><span class="sxs-lookup"><span data-stu-id="47a3c-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="47a3c-266">1</span><span class="sxs-lookup"><span data-stu-id="47a3c-266">1</span></span>        | <span data-ttu-id="47a3c-267">Şu kişiye ata: Donna</span><span class="sxs-lookup"><span data-stu-id="47a3c-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="47a3c-268">2</span><span class="sxs-lookup"><span data-stu-id="47a3c-268">2</span></span>        | <span data-ttu-id="47a3c-269">Şu kişiye ata: Erin</span><span class="sxs-lookup"><span data-stu-id="47a3c-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="47a3c-270">3</span><span class="sxs-lookup"><span data-stu-id="47a3c-270">3</span></span>        | <span data-ttu-id="47a3c-271">Son eylem: \[Karar 1\]</span><span class="sxs-lookup"><span data-stu-id="47a3c-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="47a3c-272">Bu örnekte sistem süresi geçen kararı Donna'ya atar.</span><span class="sxs-lookup"><span data-stu-id="47a3c-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="47a3c-273">Eğer Donna ayırılan süre içerisinde kararı alamazsa, sistem kararı Erin'e atar.</span><span class="sxs-lookup"><span data-stu-id="47a3c-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="47a3c-274">Eğer Erin ayırılan süre içerisinde kararı alamazsa, sistem karar olarak **\[Karar 1\]**'i karar olarak seçer</span><span class="sxs-lookup"><span data-stu-id="47a3c-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="47a3c-275">Bir kullanıcıyı ilerletme yoluna eklemek için **İlerletme ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="47a3c-276">Aşağıdaki tablodaki seçeneklerden birini seçin ve 4. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="47a3c-277">Seçenek</span><span class="sxs-lookup"><span data-stu-id="47a3c-277">Option</span></span></th>
    <th><span data-ttu-id="47a3c-278">Kararın ilerletildiği kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="47a3c-279">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="47a3c-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="47a3c-280">Hiyerarşi</span><span class="sxs-lookup"><span data-stu-id="47a3c-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="47a3c-281">Belirli bir kuruluş hiyerarşisindeki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="47a3c-282"><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, kararın ilerletileceği hiyerarşi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="47a3c-283">Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="47a3c-284">Bu adlar kararın ilerletilebileceği kullanıcıları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="47a3c-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="47a3c-285">Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="47a3c-286">Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="47a3c-287">Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="47a3c-288">Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="47a3c-289"><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara kararın ilerletilmesi gerektiğini belirtin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="47a3c-290"><strong>Alınan tüm kullanıcılara ata</strong> – Karar bu aralıktaki tüm kullanıcılara ilerletilir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="47a3c-291"><strong>Yalnızca alınan son kullanıcıya ata</strong> – Karar yalnızca aralıktaki son kullanıcıya ilerletilir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="47a3c-292"><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak:</strong> – Karar, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya ilerletilmez.</span><span class="sxs-lookup"><span data-stu-id="47a3c-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="47a3c-293">Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="47a3c-294">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="47a3c-294">Workflow user</span></span></td>
    <td><span data-ttu-id="47a3c-295">Mevcut iş akışındaki kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="47a3c-296"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="47a3c-297">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="47a3c-297">User</span></span></td>
    <td><span data-ttu-id="47a3c-298">Belirli kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="47a3c-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="47a3c-299"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="47a3c-300"><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm  kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="47a3c-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="47a3c-301">Kararın ilerletileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="47a3c-302">**Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının kararı almak üzere ne kadar zamanı olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="47a3c-303">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-303">Select one of the following options:</span></span>

    - <span data-ttu-id="47a3c-304">**Saatler** – Kullanıcının kararı alması gereken saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="47a3c-305">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="47a3c-306">**Günler** – Kullanıcının kararı alması gereken gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="47a3c-307">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="47a3c-308">**Haftalar** – Kullanıcının kararı alması gereken hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="47a3c-309">**Aylar** – Kullanıcının kararı almış olması gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="47a3c-310">Örneğin kullanıcının kararı ayın üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="47a3c-311">**Yıllar** – Kullanıcının kararı almış olması gereken haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="47a3c-312">Örneğin kullanıcının kararı Aralık ayının üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="47a3c-313">İlerletme yoluna eklenecek tüm kullanıcılar için 3. adım ve 4. adımlar arasındaki süreci yineleyin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="47a3c-314">Kullanıcıların sıralamasını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="47a3c-315">İlerletme yolundaki kullanıcılar verilen süre içinde kararı alamazsa, sistem görev üstünde karar alır.</span><span class="sxs-lookup"><span data-stu-id="47a3c-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="47a3c-316">Sistemin seçeceği seçeneği belirtmek için **Eylem** satırını seçin ve sonra **Eylemi bitir** sekmesi üzerinde bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="47a3c-317">Zaman limiti ayarlama</span><span class="sxs-lookup"><span data-stu-id="47a3c-317">Set a time limit</span></span>

<span data-ttu-id="47a3c-318">Kararın belirli bir süre içerisinde alınması gerekiyorsa bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="47a3c-319">Bu yordamda belirlediğiniz seçenekler, sayfanın **Atama** ve **İlerletme** alanlarında belirlemiş olduğunuz seçenekleri geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="47a3c-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="47a3c-320">Sol bölmede **Gelişmiş ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47a3c-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="47a3c-321">**İş akışı öğesi için bir zaman sınırı ayarlayın** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="47a3c-322">**Süre** alanında, kararın ne zaman alınması gerektiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="47a3c-323">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="47a3c-323">Select one of the following options:</span></span>

    - <span data-ttu-id="47a3c-324">**Saatler** – Saatlerin sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="47a3c-325">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="47a3c-326">**Günler** – Günlerin sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="47a3c-327">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="47a3c-328">**Haftalar** – Haftaların sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="47a3c-329">**Aylar** – Kararın alınmış olması gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="47a3c-330">Örneğin kararın ayın üçüncü haftasının Cuma gününden önce alınmış olmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="47a3c-331">**Yıllar** – Kararın alınmış olması gereken günü, haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="47a3c-332">Örneğin kararın Aralık ayının üçüncü haftasının Cuma gününden önce alınmış olmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a3c-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="47a3c-333">Zaman limiti aşılırsa sistem kararı kendi alır.</span><span class="sxs-lookup"><span data-stu-id="47a3c-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="47a3c-334">**Eylem** listesinden sistemin tercih etmesi gereken seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="47a3c-334">In the **Action** list, select the option that the system should select.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]