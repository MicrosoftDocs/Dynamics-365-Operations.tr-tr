---
title: İş akışı özelliklerini yapılandırma
description: Bu konu İş akışının çeşitli özelliklerini yapılandırmayı açıklar.
author: sericks007
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 268448049955170b8eb9e64cbd50416565a041b1
ms.sourcegitcommit: 561d06c2a74602dfaa40334d8afac5053aebc055
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2020
ms.locfileid: "3541121"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="08dc3-103">İş akışı özelliklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="08dc3-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08dc3-104">Bu konu İş akışının çeşitli özelliklerini yapılandırmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="08dc3-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="08dc3-105">Bir iş akışının özelliklerini yapılandırmak için iş akışını, iş akışı düzenleyicisinde açın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="08dc3-106">İş akışı düzenleyicisinin tuvaline tıklayın ve sonra **Seçenekler**'e tıklayarak **Özellikler** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="08dc3-107">Daha sonra aşağıdaki yordamları kullanarak iş akışının çeşitli özelliklerini yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08dc3-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="08dc3-108">İş akışını adlandırma</span><span class="sxs-lookup"><span data-stu-id="08dc3-108">Name the workflow</span></span>

<span data-ttu-id="08dc3-109">İş akışı için bir ad girmek üzere şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="08dc3-110">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="08dc3-111">**Adı** alanına iş akışı için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="08dc3-112">Örneğin, faaliyet göstermekte olduğunuz her ülke/bölge için bir satınalma talebi iş akışı oluşturursanız, satınalma talebi iş akışını **Satınalma Talepleri Danimarka** veya **Satınalma Talepleri İspanya** olarak adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08dc3-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="08dc3-113">İş akışı sahibini belirtme</span><span class="sxs-lookup"><span data-stu-id="08dc3-113">Specify the workflow owner</span></span>

<span data-ttu-id="08dc3-114">İş akışının sahibi, ilgili iş akışını yönetecek ve bakımını yapacak olan kişidir.</span><span class="sxs-lookup"><span data-stu-id="08dc3-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="08dc3-115">İş akışı sahibini belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="08dc3-116">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="08dc3-117">**Sahibi** listesinde, iş akışını yönetecek olan kişinin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="08dc3-118">Bir e-posta şablonu seçin</span><span class="sxs-lookup"><span data-stu-id="08dc3-118">Select an email template</span></span>

<span data-ttu-id="08dc3-119">İş akışı hakkında bildirim iletilerini oluşturmakta kullanılacak e-posta şablonunu seçmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="08dc3-120">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="08dc3-121">**İş akışı bildirimleri için e-posta şablonu** listesinde, şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="08dc3-122">Kullanıcılar için yönergeler girme</span><span class="sxs-lookup"><span data-stu-id="08dc3-122">Enter instructions for users</span></span>

<span data-ttu-id="08dc3-123">İşlenmek ve onaylanmak üzere belgeler gönderen kullanıcılara yönergeler sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08dc3-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="08dc3-124">Bu kullanıcılar ayrıca *oluşturucular* olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="08dc3-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="08dc3-125">Örneğin, bir satınalma talebi iş akışı oluşturuyorsunuz ve yönergeleri giriyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="08dc3-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="08dc3-126">Bu yönergeler daha sonra satınalma taleplerini **Satınalma talepleri** sayfasına giren kullanıcılar tarafından görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="08dc3-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="08dc3-127">Oluşturucu, yönergeleri görüntülemek için iş akışı ileti çubuğundaki simgeye tıklar.</span><span class="sxs-lookup"><span data-stu-id="08dc3-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="08dc3-128">Kullanıcılar için yönergeler girmek üzere şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="08dc3-129">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="08dc3-130">**Gönderim yönergeleri** alanında, yönergeleri girin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="08dc3-131">Yönergeleri kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08dc3-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="08dc3-132">Yer tutucular, yönergeler kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="08dc3-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="08dc3-133">Yer tutucu girmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="08dc3-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="08dc3-134">Yer tutucunun görünmesini istediğiniz yeri belirtmek üzere **Gönderi yönergeleri** alanını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="08dc3-135">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="08dc3-136">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="08dc3-137">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-137">Click **Insert**.</span></span>

4. <span data-ttu-id="08dc3-138">Yönergelerin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="08dc3-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="08dc3-139">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="08dc3-140">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="08dc3-141">Beliren listede, metni gireceğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="08dc3-142">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="08dc3-143">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08dc3-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="08dc3-144">Yer tutucu girmek hakkında yönergeler için, adım 3'e bakın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="08dc3-145">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="08dc3-146">Bu iş akışının etkinleştirme koşulları üzerinden ne zaman kullanılacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="08dc3-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="08dc3-147">Aynı iş akışı türüne dayalı birden çok iş akışı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08dc3-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="08dc3-148">Aynı türe dayalı birden çok iş akışınız olduğunda, etkinleştirme koşullarını kullanarak her bir iş akışının ne zaman kullanıldığını belirtmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="08dc3-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="08dc3-149">Etkinleştirme koşulları karşılanmazsa, varsayılan iş akışı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="08dc3-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="08dc3-150">Benzer şekilde, bir iş akışı türü için tanımlanmış yalnızca bir iş akışı yapılandırması varsa, bu iş akışı yapılandırması etkinleştirme koşullarına bağlı olmaksızın kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="08dc3-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="08dc3-151">Örneğin, faaliyet gösterdiğiniz her ülke/bölge için bir satınalma talebi iş akışı oluşturabilirsiniz, örneğin aşağıdaki koşullarla Satınalma Talepleri Danimarka ve Satınalma Talepleri İspanya gibi.</span><span class="sxs-lookup"><span data-stu-id="08dc3-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="08dc3-152">Satınalma Talebi Danimarka: ülke/bölge = DK olduğunda kullanılır</span><span class="sxs-lookup"><span data-stu-id="08dc3-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="08dc3-153">Satınalma Talebi İspanya: ülke/bölge = ES olduğunda kullanılır</span><span class="sxs-lookup"><span data-stu-id="08dc3-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="08dc3-154">Yapılandırmakta olduğunuz iş akışının ne zaman kullanılacağını belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="08dc3-155">Sol bölmede **Etkinleştirme**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="08dc3-156">**Bu iş akışını çalıştırmak için koşullar** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="08dc3-157">**Koşul ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="08dc3-158">Koşulu girin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-158">Enter a condition.</span></span>
5. <span data-ttu-id="08dc3-159">Varsa, gerekli ek koşulları girin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="08dc3-160">Koşulun, kayıtları doğru şekilde dahil ettiğinden ve hariç tuttuğundan emin olmak için bazı hedef kayıtları bulunan iş akışı aracılığıyla çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-160">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="08dc3-161">Bildirimlerin ne zaman gönderileceğini belirtme</span><span class="sxs-lookup"><span data-stu-id="08dc3-161">Specify when notifications are sent</span></span>

<span data-ttu-id="08dc3-162">Bir belge işlenmek üzere gönderildiğinde, bir iş akışı örneği oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="08dc3-162">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="08dc3-163">Bu iş akışını temel alan iş akışı örnekleri başlatıldığında, sona erdirildiğinde, bitirildiğinde veya bir hata nedeniyle durdurulduğunda kullanıcılara bildirimler gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08dc3-163">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="08dc3-164">Bildirimlerin ne zaman gönderileceğini belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-164">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="08dc3-165">Sol bölmede **Bildirimler**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-165">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="08dc3-166">Bildirimleri tetiklemesi gereken her olay için onay kutusunu seçin:</span><span class="sxs-lookup"><span data-stu-id="08dc3-166">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="08dc3-167">**Başlatıldı** — Bir iş akışı örneği başlatıldığında bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="08dc3-167">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="08dc3-168">**Durduruldu** — İş akışı örneği oluşan bir hata nedeniyle durdurulduğunda bildirimler gönder.</span><span class="sxs-lookup"><span data-stu-id="08dc3-168">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="08dc3-169">**Tamamlandı** — Bir iş akışı örneği tamamlandığında bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="08dc3-169">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="08dc3-170">**Kurtarılamaz** — İş akışı örneği oluşan kurtarılamaz bir hata nedeniyle durdurulduğunda bildirimler gönder.</span><span class="sxs-lookup"><span data-stu-id="08dc3-170">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="08dc3-171">**Sona erdirildi** — Bir iş akışı örneği sone erdirildiğinde bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="08dc3-171">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="08dc3-172">2. adımda seçtiğiniz bir olay için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-172">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="08dc3-173">**Bildirim metni** sekmesinde bildirimin metnini girin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-173">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="08dc3-174">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08dc3-174">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="08dc3-175">Yer tutucular, metin kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="08dc3-175">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="08dc3-176">Yer tutucu girmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="08dc3-176">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="08dc3-177">Yer tutucunun görünmesini istediğiniz yeri belirtmek üzere alan içerisine tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-177">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="08dc3-178">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-178">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="08dc3-179">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-179">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="08dc3-180">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-180">Click **Insert**.</span></span>
    5. <span data-ttu-id="08dc3-181">Eklenecek ortak **Bildirim metni** yer tutucusu önceki adımdaki yorumları görüntüleyen "Son Notlar: %Workflow.Last note%" öğesidir.</span><span class="sxs-lookup"><span data-stu-id="08dc3-181">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="08dc3-182">Metnin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="08dc3-182">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="08dc3-183">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-183">Click **Translations**.</span></span>
    2. <span data-ttu-id="08dc3-184">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-184">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="08dc3-185">Beliren listede, metni gireceğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-185">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="08dc3-186">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-186">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="08dc3-187">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08dc3-187">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="08dc3-188">Yer tutucu girmek hakkında yönergeler için, adım 5'e bakın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-188">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="08dc3-189">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-189">Click **Close**.</span></span>

7. <span data-ttu-id="08dc3-190">**Alıcı** sekmesinde, aşağıdaki seçenekleri kimin bildirim alacağını belirtmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-190">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="08dc3-191">Seçenek</span><span class="sxs-lookup"><span data-stu-id="08dc3-191">Option</span></span></th>
    <th><span data-ttu-id="08dc3-192">Bildirimler bu kullanıcılara gönderilir.</span><span class="sxs-lookup"><span data-stu-id="08dc3-192">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="08dc3-193">Bildirimleri göndermek için aşağıdaki adımları izleyin</span><span class="sxs-lookup"><span data-stu-id="08dc3-193">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="08dc3-194">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="08dc3-194">Participant</span></span></td>
    <td><span data-ttu-id="08dc3-195">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="08dc3-195">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="08dc3-196"><strong>Alıcı</strong> sekmesinde, <strong>Katılımcı</strong>'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-196">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="08dc3-197"><strong>Rol tabanlı</strong> sekmesindeki <strong>Katılımcı türü</strong> listesinde, bildirimin gönderileceği grup türünü veya rolünü seçin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-197">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="08dc3-198"><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-198">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="08dc3-199">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="08dc3-199">Workflow user</span></span></td>
    <td><span data-ttu-id="08dc3-200">Bu iş akışında katılımcı olan kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="08dc3-200">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="08dc3-201"><strong>Alıcı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-201">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="08dc3-202"><strong>İş akışı kullanıcısı</strong> sekmesindeki <strong>İş akışı kullanıcısı</strong> listesinden, bu iş akışının bir katılımcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-202">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="08dc3-203">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="08dc3-203">User</span></span></td>
    <td><span data-ttu-id="08dc3-204">Belirli kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="08dc3-204">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="08dc3-205"><strong>Alıcı</strong> sekmesinde, <strong>Kullanıcı</strong>'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-205">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="08dc3-206"><strong>Kullanıcı</strong> sekmesindeki <strong>Mevcut kullanıcılar</strong> listesi mevcut tüm kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="08dc3-206">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="08dc3-207">Bildirimlerin gönderileceği kullanıcıları seçin ve bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-207">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="08dc3-208">Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-208">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="08dc3-209">İş akışında yaptığınız değişiklikler hakkında açıklamalar girin</span><span class="sxs-lookup"><span data-stu-id="08dc3-209">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="08dc3-210">İş akışında yaptığınız değişiklikler hakkında açıklamalar girmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-210">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="08dc3-211">Sol bölmede **Notlar**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-211">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="08dc3-212">**İş akışı hakkında yorumlar girin** alanında, yorumlarınızı girin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-212">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="08dc3-213">Yorumlarınızı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="08dc3-213">Review your comments.</span></span> <span data-ttu-id="08dc3-214">Yorumlarınızı ekledikten sonra üzerlerinde değişiklik yapamazsınız.</span><span class="sxs-lookup"><span data-stu-id="08dc3-214">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="08dc3-215">**Yorum geçmişi** alanına yorumlarınızı eklemek için **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08dc3-215">Click **Add** to add your comments to the **Comment history** area.</span></span>
