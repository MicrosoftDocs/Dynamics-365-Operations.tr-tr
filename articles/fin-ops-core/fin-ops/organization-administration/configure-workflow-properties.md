---
title: İş akışı özelliklerini yapılandırma
description: Bu konu İş akışının çeşitli özelliklerini yapılandırmayı açıklar.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bd3c9bea010099f83d16dad70261bc2d46a1dac
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693294"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="b93ed-103">İş akışı özelliklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b93ed-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b93ed-104">Bu konu İş akışının çeşitli özelliklerini yapılandırmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="b93ed-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="b93ed-105">Bir iş akışının özelliklerini yapılandırmak için iş akışını, iş akışı düzenleyicisinde açın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="b93ed-106">İş akışı düzenleyicisinin tuvaline tıklayın ve sonra **Seçenekler**'e tıklayarak **Özellikler** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="b93ed-107">Daha sonra aşağıdaki yordamları kullanarak iş akışının çeşitli özelliklerini yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b93ed-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="b93ed-108">İş akışını adlandırma</span><span class="sxs-lookup"><span data-stu-id="b93ed-108">Name the workflow</span></span>

<span data-ttu-id="b93ed-109">İş akışı için bir ad girmek üzere şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="b93ed-110">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="b93ed-111">**Adı** alanına iş akışı için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="b93ed-112">Örneğin, faaliyet göstermekte olduğunuz her ülke/bölge için bir satınalma talebi iş akışı oluşturursanız, satınalma talebi iş akışını **Satınalma Talepleri Danimarka** veya **Satınalma Talepleri İspanya** olarak adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b93ed-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="b93ed-113">İş akışı sahibini belirtme</span><span class="sxs-lookup"><span data-stu-id="b93ed-113">Specify the workflow owner</span></span>

<span data-ttu-id="b93ed-114">İş akışının sahibi, ilgili iş akışını yönetecek ve bakımını yapacak olan kişidir.</span><span class="sxs-lookup"><span data-stu-id="b93ed-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="b93ed-115">İş akışı sahibini belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="b93ed-116">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="b93ed-117">**Sahibi** listesinde, iş akışını yönetecek olan kişinin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="b93ed-118">Bir e-posta şablonu seçin</span><span class="sxs-lookup"><span data-stu-id="b93ed-118">Select an email template</span></span>

<span data-ttu-id="b93ed-119">İş akışı hakkında bildirim iletilerini oluşturmakta kullanılacak e-posta şablonunu seçmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="b93ed-120">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="b93ed-121">**İş akışı bildirimleri için e-posta şablonu** listesinde, şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="b93ed-122">Kullanıcılar için yönergeler girme</span><span class="sxs-lookup"><span data-stu-id="b93ed-122">Enter instructions for users</span></span>

<span data-ttu-id="b93ed-123">İşlenmek ve onaylanmak üzere belgeler gönderen kullanıcılara yönergeler sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b93ed-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="b93ed-124">Bu kullanıcılar ayrıca *oluşturucular* olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="b93ed-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="b93ed-125">Örneğin, bir satınalma talebi iş akışı oluşturuyorsunuz ve yönergeleri giriyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="b93ed-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="b93ed-126">Bu yönergeler daha sonra satınalma taleplerini **Satınalma talepleri** sayfasına giren kullanıcılar tarafından görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="b93ed-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="b93ed-127">Oluşturucu, yönergeleri görüntülemek için iş akışı ileti çubuğundaki simgeye tıklar.</span><span class="sxs-lookup"><span data-stu-id="b93ed-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="b93ed-128">Kullanıcılar için yönergeler girmek üzere şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="b93ed-129">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="b93ed-130">**Gönderim yönergeleri** alanında, yönergeleri girin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="b93ed-131">Yönergeleri kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b93ed-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="b93ed-132">Yer tutucular, yönergeler kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="b93ed-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="b93ed-133">Yer tutucu girmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="b93ed-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="b93ed-134">Yer tutucunun görünmesini istediğiniz yeri belirtmek üzere **Gönderi yönergeleri** alanını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="b93ed-135">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="b93ed-136">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="b93ed-137">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-137">Click **Insert**.</span></span>

4. <span data-ttu-id="b93ed-138">Yönergelerin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="b93ed-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="b93ed-139">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="b93ed-140">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="b93ed-141">Beliren listede, metni gireceğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="b93ed-142">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="b93ed-143">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b93ed-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="b93ed-144">Yer tutucu girmek hakkında yönergeler için, adım 3'e bakın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="b93ed-145">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="b93ed-146">Bu iş akışının etkinleştirme koşulları üzerinden ne zaman kullanılacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="b93ed-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="b93ed-147">Aynı iş akışı türüne dayalı birden çok iş akışı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b93ed-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="b93ed-148">Aynı türe dayalı birden çok iş akışınız olduğunda, etkinleştirme koşullarını kullanarak her bir iş akışının ne zaman kullanıldığını belirtmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="b93ed-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="b93ed-149">Etkinleştirme koşulları karşılanmazsa, varsayılan iş akışı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b93ed-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="b93ed-150">Benzer şekilde, bir iş akışı türü için tanımlanmış yalnızca bir iş akışı yapılandırması varsa, bu iş akışı yapılandırması etkinleştirme koşullarına bağlı olmaksızın kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="b93ed-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="b93ed-151">Örneğin, faaliyet gösterdiğiniz her ülke/bölge için bir satınalma talebi iş akışı oluşturabilirsiniz, örneğin aşağıdaki koşullarla Satınalma Talepleri Danimarka ve Satınalma Talepleri İspanya gibi.</span><span class="sxs-lookup"><span data-stu-id="b93ed-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="b93ed-152">Satınalma Talebi Danimarka: ülke/bölge = DK olduğunda kullanılır</span><span class="sxs-lookup"><span data-stu-id="b93ed-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="b93ed-153">Satınalma Talebi İspanya: ülke/bölge = ES olduğunda kullanılır</span><span class="sxs-lookup"><span data-stu-id="b93ed-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="b93ed-154">Yapılandırmakta olduğunuz iş akışının ne zaman kullanılacağını belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="b93ed-155">Sol bölmede **Etkinleştirme**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="b93ed-156">**Bu iş akışını çalıştırmak için koşullar** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="b93ed-157">**Koşul ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="b93ed-158">Koşulu girin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-158">Enter a condition.</span></span>
5. <span data-ttu-id="b93ed-159">Varsa, gerekli ek koşulları girin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="b93ed-160">Koşulun, kayıtları doğru şekilde dahil ettiğinden ve hariç tuttuğundan emin olmak için bazı hedef kayıtları bulunan iş akışı aracılığıyla çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-160">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="b93ed-161">Bildirimlerin ne zaman gönderileceğini belirtme</span><span class="sxs-lookup"><span data-stu-id="b93ed-161">Specify when notifications are sent</span></span>

<span data-ttu-id="b93ed-162">Bir belge işlenmek üzere gönderildiğinde, bir iş akışı örneği oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b93ed-162">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="b93ed-163">Bu iş akışını temel alan iş akışı örnekleri başlatıldığında, sona erdirildiğinde, bitirildiğinde veya bir hata nedeniyle durdurulduğunda kullanıcılara bildirimler gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b93ed-163">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="b93ed-164">Bildirimlerin ne zaman gönderileceğini belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-164">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="b93ed-165">Sol bölmede **Bildirimler**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-165">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="b93ed-166">Bildirimleri tetiklemesi gereken her olay için onay kutusunu seçin:</span><span class="sxs-lookup"><span data-stu-id="b93ed-166">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="b93ed-167">**Başlatıldı** — Bir iş akışı örneği başlatıldığında bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="b93ed-167">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="b93ed-168">**Durduruldu** — İş akışı örneği oluşan bir hata nedeniyle durdurulduğunda bildirimler gönder.</span><span class="sxs-lookup"><span data-stu-id="b93ed-168">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="b93ed-169">**Tamamlandı** — Bir iş akışı örneği tamamlandığında bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="b93ed-169">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="b93ed-170">**Kurtarılamaz** — İş akışı örneği oluşan kurtarılamaz bir hata nedeniyle durdurulduğunda bildirimler gönder.</span><span class="sxs-lookup"><span data-stu-id="b93ed-170">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="b93ed-171">**Sona erdirildi** — Bir iş akışı örneği sone erdirildiğinde bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="b93ed-171">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="b93ed-172">2. adımda seçtiğiniz bir olay için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-172">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="b93ed-173">**Bildirim metni** sekmesinde bildirimin metnini girin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-173">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="b93ed-174">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b93ed-174">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="b93ed-175">Yer tutucular, metin kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="b93ed-175">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="b93ed-176">Yer tutucu girmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="b93ed-176">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="b93ed-177">Yer tutucunun görünmesini istediğiniz yeri belirtmek üzere alan içerisine tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-177">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="b93ed-178">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-178">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="b93ed-179">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-179">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="b93ed-180">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-180">Click **Insert**.</span></span>
    5. <span data-ttu-id="b93ed-181">Eklenecek ortak **Bildirim metni** yer tutucusu önceki adımdaki yorumları görüntüleyen "Son Notlar: %Workflow.Last note%" öğesidir.</span><span class="sxs-lookup"><span data-stu-id="b93ed-181">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="b93ed-182">Metnin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="b93ed-182">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="b93ed-183">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-183">Click **Translations**.</span></span>
    2. <span data-ttu-id="b93ed-184">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-184">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="b93ed-185">Beliren listede, metni gireceğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-185">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="b93ed-186">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-186">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="b93ed-187">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b93ed-187">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="b93ed-188">Yer tutucu girmek hakkında yönergeler için, adım 5'e bakın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-188">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="b93ed-189">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-189">Click **Close**.</span></span>

7. <span data-ttu-id="b93ed-190">**Alıcı** sekmesinde, aşağıdaki seçenekleri kimin bildirim alacağını belirtmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-190">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="b93ed-191">Seçenek</span><span class="sxs-lookup"><span data-stu-id="b93ed-191">Option</span></span></th>
    <th><span data-ttu-id="b93ed-192">Bildirimler bu kullanıcılara gönderilir.</span><span class="sxs-lookup"><span data-stu-id="b93ed-192">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="b93ed-193">Bildirimleri göndermek için aşağıdaki adımları izleyin</span><span class="sxs-lookup"><span data-stu-id="b93ed-193">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="b93ed-194">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="b93ed-194">Participant</span></span></td>
    <td><span data-ttu-id="b93ed-195">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="b93ed-195">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="b93ed-196"><strong>Alıcı</strong> sekmesinde, <strong>Katılımcı</strong>'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-196">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="b93ed-197"><strong>Rol tabanlı</strong> sekmesindeki <strong>Katılımcı türü</strong> listesinde, bildirimin gönderileceği grup türünü veya rolünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-197">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="b93ed-198"><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-198">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="b93ed-199">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="b93ed-199">Workflow user</span></span></td>
    <td><span data-ttu-id="b93ed-200">Bu iş akışında katılımcı olan kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="b93ed-200">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="b93ed-201"><strong>Alıcı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-201">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="b93ed-202"><strong>İş akışı kullanıcısı</strong> sekmesindeki <strong>İş akışı kullanıcısı</strong> listesinden, bu iş akışının bir katılımcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-202">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="b93ed-203">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="b93ed-203">User</span></span></td>
    <td><span data-ttu-id="b93ed-204">Belirli kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="b93ed-204">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="b93ed-205"><strong>Alıcı</strong> sekmesinde, <strong>Kullanıcı</strong>'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-205">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="b93ed-206"><strong>Kullanıcı</strong> sekmesindeki <strong>Mevcut kullanıcılar</strong> listesi mevcut tüm kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="b93ed-206">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="b93ed-207">Bildirimlerin gönderileceği kullanıcıları seçin ve bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-207">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="b93ed-208">Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-208">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="b93ed-209">İş akışında yaptığınız değişiklikler hakkında açıklamalar girin</span><span class="sxs-lookup"><span data-stu-id="b93ed-209">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="b93ed-210">İş akışında yaptığınız değişiklikler hakkında açıklamalar girmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-210">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="b93ed-211">Sol bölmede **Notlar**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-211">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="b93ed-212">**İş akışı hakkında yorumlar girin** alanında, yorumlarınızı girin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-212">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="b93ed-213">Yorumlarınızı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="b93ed-213">Review your comments.</span></span> <span data-ttu-id="b93ed-214">Yorumlarınızı ekledikten sonra üzerlerinde değişiklik yapamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b93ed-214">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="b93ed-215">**Yorum geçmişi** alanına yorumlarınızı eklemek için **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b93ed-215">Click **Add** to add your comments to the **Comment history** area.</span></span>
