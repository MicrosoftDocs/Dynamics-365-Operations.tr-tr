---
title: İş akışı özelliklerini yapılandırma
description: Bu konu İş akışının çeşitli özelliklerini yapılandırmayı açıklar.
author: sericks007
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: d745389b37b899760ea32ae75c5cb80d9139be2d
ms.sourcegitcommit: 1852f08f015acd106f4cefd03fa07985dc009123
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2020
ms.locfileid: "3199448"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="e639c-103">İş akışı özelliklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e639c-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e639c-104">Bu konu İş akışının çeşitli özelliklerini yapılandırmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="e639c-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="e639c-105">Bir iş akışının özelliklerini yapılandırmak için iş akışını, iş akışı düzenleyicisinde açın.</span><span class="sxs-lookup"><span data-stu-id="e639c-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="e639c-106">İş akışı düzenleyicisinin tuvaline tıklayın ve sonra **Seçenekler**'e tıklayarak **Özellikler** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="e639c-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="e639c-107">Daha sonra aşağıdaki yordamları kullanarak iş akışının çeşitli özelliklerini yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e639c-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="e639c-108">İş akışını adlandırma</span><span class="sxs-lookup"><span data-stu-id="e639c-108">Name the workflow</span></span>

<span data-ttu-id="e639c-109">İş akışı için bir ad girmek üzere şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e639c-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="e639c-110">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="e639c-111">**Adı** alanına iş akışı için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="e639c-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="e639c-112">Örneğin, faaliyet göstermekte olduğunuz her ülke/bölge için bir satınalma talebi iş akışı oluşturursanız, satınalma talebi iş akışını **Satınalma Talepleri Danimarka** veya **Satınalma Talepleri İspanya** olarak adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e639c-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="e639c-113">İş akışı sahibini belirtme</span><span class="sxs-lookup"><span data-stu-id="e639c-113">Specify the workflow owner</span></span>

<span data-ttu-id="e639c-114">İş akışının sahibi, ilgili iş akışını yönetecek ve bakımını yapacak olan kişidir.</span><span class="sxs-lookup"><span data-stu-id="e639c-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="e639c-115">İş akışı sahibini belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e639c-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="e639c-116">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="e639c-117">**Sahibi** listesinde, iş akışını yönetecek olan kişinin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="e639c-118">Bir e-posta şablonu seçin</span><span class="sxs-lookup"><span data-stu-id="e639c-118">Select an email template</span></span>

<span data-ttu-id="e639c-119">İş akışı hakkında bildirim iletilerini oluşturmakta kullanılacak e-posta şablonunu seçmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e639c-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="e639c-120">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="e639c-121">**İş akışı bildirimleri için e-posta şablonu** listesinde, şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="e639c-122">Kullanıcılar için yönergeler girme</span><span class="sxs-lookup"><span data-stu-id="e639c-122">Enter instructions for users</span></span>

<span data-ttu-id="e639c-123">İşlenmek ve onaylanmak üzere belgeler gönderen kullanıcılara yönergeler sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e639c-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="e639c-124">Bu kullanıcılar ayrıca *oluşturucular* olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="e639c-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="e639c-125">Örneğin, bir satınalma talebi iş akışı oluşturuyorsunuz ve yönergeleri giriyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="e639c-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="e639c-126">Bu yönergeler daha sonra satınalma taleplerini **Satınalma talepleri** sayfasına giren kullanıcılar tarafından görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="e639c-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="e639c-127">Oluşturucu, yönergeleri görüntülemek için iş akışı ileti çubuğundaki simgeye tıklar.</span><span class="sxs-lookup"><span data-stu-id="e639c-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="e639c-128">Kullanıcılar için yönergeler girmek üzere şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e639c-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="e639c-129">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="e639c-130">**Gönderim yönergeleri** alanında, yönergeleri girin.</span><span class="sxs-lookup"><span data-stu-id="e639c-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="e639c-131">Yönergeleri kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e639c-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="e639c-132">Yer tutucular, yönergeler kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="e639c-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="e639c-133">Yer tutucu girmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e639c-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="e639c-134">Yer tutucunun görünmesini istediğiniz yeri belirtmek üzere **Gönderi yönergeleri** alanını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="e639c-135">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="e639c-136">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="e639c-137">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-137">Click **Insert**.</span></span>

4. <span data-ttu-id="e639c-138">Yönergelerin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e639c-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="e639c-139">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e639c-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="e639c-140">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="e639c-141">Beliren listede, metni gireceğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="e639c-142">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="e639c-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="e639c-143">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e639c-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="e639c-144">Yer tutucu girmek hakkında yönergeler için, adım 3'e bakın.</span><span class="sxs-lookup"><span data-stu-id="e639c-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="e639c-145">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e639c-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="e639c-146">Bu iş akışının etkinleştirme koşulları üzerinden ne zaman kullanılacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="e639c-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="e639c-147">Aynı iş akışı türüne dayalı birden çok iş akışı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e639c-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="e639c-148">Aynı türe dayalı birden çok iş akışınız olduğunda, etkinleştirme koşullarını kullanarak her bir iş akışının ne zaman kullanıldığını belirtmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="e639c-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="e639c-149">Etkinleştirme koşulları karşılanmazsa, varsayılan iş akışı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e639c-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="e639c-150">Benzer şekilde, bir iş akışı türü için tanımlanmış yalnızca bir iş akışı yapılandırması varsa, bu iş akışı yapılandırması etkinleştirme koşullarına bağlı olmaksızın kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e639c-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="e639c-151">Örneğin, faaliyet gösterdiğiniz her ülke/bölge için bir satınalma talebi iş akışı oluşturabilirsiniz, örneğin aşağıdaki koşullarla Satınalma Talepleri Danimarka ve Satınalma Talepleri İspanya gibi.</span><span class="sxs-lookup"><span data-stu-id="e639c-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="e639c-152">Satınalma Talebi Danimarka: ülke/bölge = DK olduğunda kullanılır</span><span class="sxs-lookup"><span data-stu-id="e639c-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="e639c-153">Satınalma Talebi İspanya: ülke/bölge = ES olduğunda kullanılır</span><span class="sxs-lookup"><span data-stu-id="e639c-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="e639c-154">Yapılandırmakta olduğunuz iş akışının ne zaman kullanılacağını belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e639c-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="e639c-155">Sol bölmede **Etkinleştirme**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="e639c-156">**Bu iş akışını çalıştırmak için koşullar** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="e639c-157">**Koşul ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="e639c-158">Koşulu girin.</span><span class="sxs-lookup"><span data-stu-id="e639c-158">Enter a condition.</span></span>
5. <span data-ttu-id="e639c-159">Varsa, gerekli ek koşulları girin.</span><span class="sxs-lookup"><span data-stu-id="e639c-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="e639c-160">Girdiğiniz koşulların doğru biçimde ayarlandığını doğrulamak için, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e639c-160">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>

    1. <span data-ttu-id="e639c-161">**Sına**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-161">Click **Test**.</span></span>
    2. <span data-ttu-id="e639c-162">**İş akışını test et** sayfasında, **Koşulu doğrula** alanında, bir kayıt seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-162">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="e639c-163">**Sına**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-163">Click **Test**.</span></span> <span data-ttu-id="e639c-164">Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="e639c-164">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="e639c-165">Örneğin, İspanya için bir satınalma talebi iş akışı oluşturuyorsanız, sayfanın **Koşulu doğrula** bölgesi satınalma taleplerinin bir listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e639c-165">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="e639c-166">**Sına**'yı tıklattığınızda, sistem seçili olan satınalma talebini değerlendirir ve ülke/bölgenin olarak ES olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="e639c-166">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4. <span data-ttu-id="e639c-167">**Özellikler** sayfasında geri dönmek için **OK** ya da **İptal Et**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e639c-167">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="e639c-168">Bildirimlerin ne zaman gönderileceğini belirtme</span><span class="sxs-lookup"><span data-stu-id="e639c-168">Specify when notifications are sent</span></span>

<span data-ttu-id="e639c-169">Bir belge işlenmek üzere gönderildiğinde, bir iş akışı örneği oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e639c-169">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="e639c-170">Bu iş akışını temel alan iş akışı örnekleri başlatıldığında, sona erdirildiğinde, bitirildiğinde veya bir hata nedeniyle durdurulduğunda kullanıcılara bildirimler gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e639c-170">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="e639c-171">Bildirimlerin ne zaman gönderileceğini belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e639c-171">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="e639c-172">Sol bölmede **Bildirimler**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-172">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="e639c-173">Bildirimleri tetiklemesi gereken her olay için onay kutusunu seçin:</span><span class="sxs-lookup"><span data-stu-id="e639c-173">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="e639c-174">**Başlatıldı** — Bir iş akışı örneği başlatıldığında bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="e639c-174">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="e639c-175">**Durduruldu** — İş akışı örneği oluşan bir hata nedeniyle durdurulduğunda bildirimler gönder.</span><span class="sxs-lookup"><span data-stu-id="e639c-175">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="e639c-176">**Tamamlandı** — Bir iş akışı örneği tamamlandığında bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="e639c-176">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="e639c-177">**Kurtarılamaz** — İş akışı örneği oluşan kurtarılamaz bir hata nedeniyle durdurulduğunda bildirimler gönder.</span><span class="sxs-lookup"><span data-stu-id="e639c-177">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="e639c-178">**Sona erdirildi** — Bir iş akışı örneği sone erdirildiğinde bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="e639c-178">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="e639c-179">2. adımda seçtiğiniz bir olay için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-179">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="e639c-180">**Bildirim metni** sekmesinde bildirimin metnini girin.</span><span class="sxs-lookup"><span data-stu-id="e639c-180">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="e639c-181">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e639c-181">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="e639c-182">Yer tutucular, metin kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="e639c-182">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="e639c-183">Yer tutucu girmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e639c-183">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="e639c-184">Yer tutucunun görünmesini istediğiniz yeri belirtmek üzere alan içerisine tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-184">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="e639c-185">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-185">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="e639c-186">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-186">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="e639c-187">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-187">Click **Insert**.</span></span>
    5. <span data-ttu-id="e639c-188">Eklenecek ortak **Bildirim metni** yer tutucusu önceki adımdaki yorumları görüntüleyen "Son Notlar: %Workflow.Last note%" öğesidir.</span><span class="sxs-lookup"><span data-stu-id="e639c-188">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="e639c-189">Metnin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e639c-189">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="e639c-190">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e639c-190">Click **Translations**.</span></span>
    2. <span data-ttu-id="e639c-191">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-191">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="e639c-192">Beliren listede, metni gireceğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-192">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="e639c-193">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="e639c-193">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="e639c-194">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e639c-194">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="e639c-195">Yer tutucu girmek hakkında yönergeler için, adım 5'e bakın.</span><span class="sxs-lookup"><span data-stu-id="e639c-195">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="e639c-196">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e639c-196">Click **Close**.</span></span>

7. <span data-ttu-id="e639c-197">**Alıcı** sekmesinde, aşağıdaki seçenekleri kimin bildirim alacağını belirtmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="e639c-197">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="e639c-198">Seçenek</span><span class="sxs-lookup"><span data-stu-id="e639c-198">Option</span></span></th>
    <th><span data-ttu-id="e639c-199">Bildirimler bu kullanıcılara gönderilir.</span><span class="sxs-lookup"><span data-stu-id="e639c-199">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="e639c-200">Bildirimleri göndermek için aşağıdaki adımları izleyin</span><span class="sxs-lookup"><span data-stu-id="e639c-200">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="e639c-201">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="e639c-201">Participant</span></span></td>
    <td><span data-ttu-id="e639c-202">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="e639c-202">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="e639c-203"><strong>Alıcı</strong> sekmesinde, <strong>Katılımcı</strong>'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-203">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="e639c-204"><strong>Rol tabanlı</strong> sekmesindeki <strong>Katılımcı türü</strong> listesinde, bildirimin gönderileceği grup türünü veya rolünü seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-204">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="e639c-205"><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-205">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="e639c-206">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="e639c-206">Workflow user</span></span></td>
    <td><span data-ttu-id="e639c-207">Bu iş akışında katılımcı olan kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="e639c-207">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="e639c-208"><strong>Alıcı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-208">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="e639c-209"><strong>İş akışı kullanıcısı</strong> sekmesindeki <strong>İş akışı kullanıcısı</strong> listesinden, bu iş akışının bir katılımcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="e639c-209">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="e639c-210">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="e639c-210">User</span></span></td>
    <td><span data-ttu-id="e639c-211">Belirli kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="e639c-211">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="e639c-212"><strong>Alıcı</strong> sekmesinde, <strong>Kullanıcı</strong>'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-212">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="e639c-213"><strong>Kullanıcı</strong> sekmesindeki <strong>Mevcut kullanıcılar</strong> listesi mevcut tüm kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="e639c-213">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="e639c-214">Bildirimlerin gönderileceği kullanıcıları seçin ve bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="e639c-214">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="e639c-215">Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="e639c-215">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="e639c-216">İş akışında yaptığınız değişiklikler hakkında açıklamalar girin</span><span class="sxs-lookup"><span data-stu-id="e639c-216">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="e639c-217">İş akışında yaptığınız değişiklikler hakkında açıklamalar girmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e639c-217">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="e639c-218">Sol bölmede **Notlar**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-218">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="e639c-219">**İş akışı hakkında yorumlar girin** alanında, yorumlarınızı girin.</span><span class="sxs-lookup"><span data-stu-id="e639c-219">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="e639c-220">Yorumlarınızı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="e639c-220">Review your comments.</span></span> <span data-ttu-id="e639c-221">Yorumlarınızı ekledikten sonra üzerlerinde değişiklik yapamazsınız.</span><span class="sxs-lookup"><span data-stu-id="e639c-221">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="e639c-222">**Yorum geçmişi** alanına yorumlarınızı eklemek için **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e639c-222">Click **Add** to add your comments to the **Comment history** area.</span></span>
