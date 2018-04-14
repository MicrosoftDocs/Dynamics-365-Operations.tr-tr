---
title: "İş akışı özelliklerini yapılandırma"
description: "Bu konu İş akışının çeşitli özelliklerini yapılandırmayı açıklar."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0b8f17285fb845101e9fbec23de7dd7866811bbd
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="configure-workflow-properties"></a><span data-ttu-id="c7778-103">İş akışı özelliklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c7778-103">Configure workflow properties</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="c7778-104">Bu konu İş akışının çeşitli özelliklerini yapılandırmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="c7778-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="c7778-105">Bir iş akışının özelliklerini yapılandırmak için iş akışını, iş akışı düzenleyicisinde açın.</span><span class="sxs-lookup"><span data-stu-id="c7778-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="c7778-106">İş akışı düzenleyicisinin tuvaline tıklayın ve sonra **Seçenekler**'e tıklayarak **Özellikler** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="c7778-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="c7778-107">Daha sonra aşağıdaki yordamları kullanarak iş akışının çeşitli özelliklerini yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7778-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="c7778-108">İş akışını adlandırma</span><span class="sxs-lookup"><span data-stu-id="c7778-108">Name the workflow</span></span>
<span data-ttu-id="c7778-109">İş akışı için bir ad girmek üzere şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c7778-109">Follow these steps to enter a name for the workflow.</span></span>

1.  <span data-ttu-id="c7778-110">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-110">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="c7778-111">**Adı** alanına iş akışı için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="c7778-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="c7778-112">Örneğin, faaliyet göstermekte olduğunuz her ülke/bölge için bir satınalma talebi iş akışı oluşturursanız, satınalma talebi iş akışını **Satınalma Talepleri Danimarka** veya **Satınalma Talepleri İspanya** olarak adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7778-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="c7778-113">İş akışı sahibini belirtme</span><span class="sxs-lookup"><span data-stu-id="c7778-113">Specify the workflow owner</span></span>
<span data-ttu-id="c7778-114">İş akışının sahibi, ilgili iş akışını yönetecek ve bakımını yapacak olan kişidir.</span><span class="sxs-lookup"><span data-stu-id="c7778-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="c7778-115">İş akışı sahibini belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c7778-115">Follow these steps to specify the workflow owner.</span></span>

1.  <span data-ttu-id="c7778-116">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-116">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="c7778-117">**Sahibi** listesinde, iş akışını yönetecek olan kişinin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="c7778-118">Bir e-posta şablonu seçin</span><span class="sxs-lookup"><span data-stu-id="c7778-118">Select an email template</span></span>
<span data-ttu-id="c7778-119">İş akışı hakkında bildirim iletilerini oluşturmakta kullanılacak e-posta şablonunu seçmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c7778-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1.  <span data-ttu-id="c7778-120">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-120">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="c7778-121">**İş akışı bildirimleri için e-posta şablonu** listesinde, şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="c7778-122">Kullanıcılar için yönergeler girme</span><span class="sxs-lookup"><span data-stu-id="c7778-122">Enter instructions for users</span></span>
<span data-ttu-id="c7778-123">İşlenmek ve onaylanmak üzere belgeler gönderen kullanıcılara yönergeler sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7778-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="c7778-124">Bu kullanıcılar ayrıca *oluşturucular* olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="c7778-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="c7778-125">Örneğin, bir satınalma talebi iş akışı oluşturuyorsunuz ve yönergeleri giriyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="c7778-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="c7778-126">Bu yönergeler daha sonra satınalma taleplerini **Satınalma talepleri** sayfasına giren kullanıcılar tarafından görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="c7778-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="c7778-127">Oluşturucu, yönergeleri görüntülemek için iş akışı ileti çubuğundaki simgeye tıklar.</span><span class="sxs-lookup"><span data-stu-id="c7778-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="c7778-128">Kullanıcılar için yönergeler girmek üzere şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c7778-128">Follow these steps to enter instructions for users.</span></span>

1.  <span data-ttu-id="c7778-129">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-129">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="c7778-130">**Gönderim yönergeleri** alanında, yönergeleri girin.</span><span class="sxs-lookup"><span data-stu-id="c7778-130">In the **Submission instructions** field, enter the instructions.</span></span>
3.  <span data-ttu-id="c7778-131">Yönergeleri kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7778-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="c7778-132">Yer tutucular, yönergeler kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="c7778-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="c7778-133">Yer tutucu girmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="c7778-133">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="c7778-134">Yer tutucunun görünmesini istediğiniz yeri belirtmek üzere **Gönderi yönergeleri** alanını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="c7778-135">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-135">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="c7778-136">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-136">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="c7778-137">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-137">Click **Insert**.</span></span>

4.  <span data-ttu-id="c7778-138">Yönergelerin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="c7778-138">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="c7778-139">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7778-139">Click **Translations**.</span></span>
    2.  <span data-ttu-id="c7778-140">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-140">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="c7778-141">Beliren listede, metni gireceğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="c7778-142">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="c7778-142">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="c7778-143">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7778-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c7778-144">Yer tutucu girmek hakkında yönergeler için, adım 3'e bakın.</span><span class="sxs-lookup"><span data-stu-id="c7778-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6.  <span data-ttu-id="c7778-145">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7778-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="c7778-146">Bu iş akışının ne zaman kullanılacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="c7778-146">Specify when this workflow is used</span></span>
<span data-ttu-id="c7778-147">Aynı türe dayalı birden çok iş akışı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7778-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="c7778-148">Örneğin, faaliyet gösterdiğiniz her ülke/bölge için bir satınalma talebi iş akışı oluşturabilirsiniz, örneğin Satınalma Talepleri Danimarka ve Satınalma Talepleri İspanya gibi.</span><span class="sxs-lookup"><span data-stu-id="c7778-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="c7778-149">Aynı türe dayalı birden çok iş akışınız olduğunda, her bir iş akışının ne zaman kullanıldığını belirtmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="c7778-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="c7778-150">Önceki örnek için, aşağıdaki koşulları belirtebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="c7778-150">For the preceding example, you specify the following conditions:</span></span>

-   <span data-ttu-id="c7778-151">Satınalma Talebi Danimarka: ülke/bölge = DK olduğunda kullanılır</span><span class="sxs-lookup"><span data-stu-id="c7778-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
-   <span data-ttu-id="c7778-152">Satınalma Talebi İspanya: ülke/bölge = ES olduğunda kullanılır</span><span class="sxs-lookup"><span data-stu-id="c7778-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="c7778-153">Yapılandırmakta olduğunuz iş akışının ne zaman kullanılacağını belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c7778-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1.  <span data-ttu-id="c7778-154">Sol bölmede **Etkinleştirme**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-154">In the left pane, click **Activation**.</span></span>
2.  <span data-ttu-id="c7778-155">**Bu iş akışını çalıştırmak için koşullar** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3.  <span data-ttu-id="c7778-156">**Koşul ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-156">Click **Add condition**.</span></span>
4.  <span data-ttu-id="c7778-157">Koşulu girin.</span><span class="sxs-lookup"><span data-stu-id="c7778-157">Enter a condition.</span></span>
5.  <span data-ttu-id="c7778-158">Varsa, gerekli ek koşulları girin.</span><span class="sxs-lookup"><span data-stu-id="c7778-158">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="c7778-159">Girdiğiniz koşulların doğru biçimde ayarlandığını doğrulamak için, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="c7778-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="c7778-160">**Sına**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-160">Click **Test**.</span></span>
    2.  <span data-ttu-id="c7778-161">**İş akışını test et** sayfasında, **Koşulu doğrula** alanında, bir kayıt seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="c7778-162">**Sına**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-162">Click **Test**.</span></span> <span data-ttu-id="c7778-163">Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="c7778-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="c7778-164">Örneğin, İspanya için bir satınalma talebi iş akışı oluşturuyorsanız, sayfanın **Koşulu doğrula** bölgesi satınalma taleplerinin bir listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7778-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="c7778-165">**Sına**'yı tıklattığınızda, sistem seçili olan satınalma talebini değerlendirir ve ülke/bölgenin olarak ES olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="c7778-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4.  <span data-ttu-id="c7778-166">**Özellikler** sayfasında geri dönmek için **OK** ya da **İptal Et**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7778-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="c7778-167">Bildirimlerin ne zaman gönderileceğini belirtme</span><span class="sxs-lookup"><span data-stu-id="c7778-167">Specify when notifications are sent</span></span>
<span data-ttu-id="c7778-168">Bir belge işlenmek üzere gönderildiğinde, bir iş akışı örneği oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7778-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="c7778-169">Bu iş akışını temel alan iş akışı örnekleri başlatıldığında, sona erdirildiğinde, bitirildiğinde veya bir hata nedeniyle durdurulduğunda kullanıcılara bildirimler gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7778-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="c7778-170">Bildirimlerin ne zaman gönderileceğini belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c7778-170">Follow these steps to specify when notifications are sent.</span></span>

1.  <span data-ttu-id="c7778-171">Sol bölmede **Bildirimler**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-171">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="c7778-172">Bildirimleri tetiklemesi gereken her olay için onay kutusunu seçin:</span><span class="sxs-lookup"><span data-stu-id="c7778-172">Select the check box for each event that should trigger notifications:</span></span>
    -   <span data-ttu-id="c7778-173">**Başlatıldı** — Bir iş akışı örneği başlatıldığında bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="c7778-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    -   <span data-ttu-id="c7778-174">**Durduruldu** — İş akışı örneği oluşan bir hata nedeniyle durdurulduğunda bildirimler gönder.</span><span class="sxs-lookup"><span data-stu-id="c7778-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    -   <span data-ttu-id="c7778-175">**Tamamlandı** — Bir iş akışı örneği tamamlandığında bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="c7778-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    -   <span data-ttu-id="c7778-176">**Kurtarılamaz** — İş akışı örneği oluşan kurtarılamaz bir hata nedeniyle durdurulduğunda bildirimler gönder.</span><span class="sxs-lookup"><span data-stu-id="c7778-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    -   <span data-ttu-id="c7778-177">**Sona erdirildi** — Bir iş akışı örneği sone erdirildiğinde bildirim gönder.</span><span class="sxs-lookup"><span data-stu-id="c7778-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3.  <span data-ttu-id="c7778-178">2. adımda seçtiğiniz bir olay için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-178">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="c7778-179">**Bildirim metni** sekmesinde bildirimin metnini girin.</span><span class="sxs-lookup"><span data-stu-id="c7778-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5.  <span data-ttu-id="c7778-180">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7778-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c7778-181">Yer tutucular, metin kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="c7778-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="c7778-182">Yer tutucu girmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="c7778-182">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="c7778-183">Yer tutucunun görünmesini istediğiniz yeri belirtmek üzere alan içerisine tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-183">Click in the field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="c7778-184">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-184">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="c7778-185">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-185">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="c7778-186">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-186">Click **Insert**.</span></span>

6.  <span data-ttu-id="c7778-187">Metnin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="c7778-187">To add translations of the text, follow these steps:</span></span>
    1.  <span data-ttu-id="c7778-188">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7778-188">Click **Translations**.</span></span>
    2.  <span data-ttu-id="c7778-189">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-189">On the page that appears, Click **Add**.</span></span>
    3.  <span data-ttu-id="c7778-190">Beliren listede, metni gireceğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-190">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="c7778-191">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="c7778-191">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="c7778-192">Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7778-192">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c7778-193">Yer tutucu girmek hakkında yönergeler için, adım 5'e bakın.</span><span class="sxs-lookup"><span data-stu-id="c7778-193">For instructions about how to enter a placeholder, see step 5.</span></span>
    6.  <span data-ttu-id="c7778-194">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7778-194">Click **Close**.</span></span>

7.  <span data-ttu-id="c7778-195">**Alıcı** sekmesinde, aşağıdaki seçenekleri kimin bildirim alacağını belirtmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="c7778-195">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c7778-196">Seçenek</span><span class="sxs-lookup"><span data-stu-id="c7778-196">Option</span></span></th>
    <th><span data-ttu-id="c7778-197">Bildirimler bu kullanıcılara gönderilir.</span><span class="sxs-lookup"><span data-stu-id="c7778-197">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="c7778-198">Bildirimleri göndermek için aşağıdaki adımları izleyin</span><span class="sxs-lookup"><span data-stu-id="c7778-198">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="c7778-199">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="c7778-199">Participant</span></span></td>
    <td><span data-ttu-id="c7778-200">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="c7778-200">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c7778-201"><strong>Alıcı</strong> sekmesinde, <strong>Katılımcı</strong>'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-201">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="c7778-202"><strong>Rol tabanlı</strong> sekmesindeki <strong>Katılımcı türü</strong> listesinde, bildirimin gönderileceği grup türünü veya rolünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-202">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="c7778-203"><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-203">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="c7778-204">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="c7778-204">Workflow user</span></span></td>
    <td><span data-ttu-id="c7778-205">Bu iş akışında katılımcı olan kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="c7778-205">Users who are participants in this workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c7778-206"><strong>Alıcı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-206">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="c7778-207"><strong>İş akışı kullanıcısı</strong> sekmesindeki <strong>İş akışı kullanıcısı</strong> listesinden, bu iş akışının bir katılımcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="c7778-207">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="c7778-208">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="c7778-208">User</span></span></td>
    <td><span data-ttu-id="c7778-209">Belirli Finance and Operations kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="c7778-209">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c7778-210"><strong>Alıcı</strong> sekmesinde, <strong>Kullanıcı</strong>'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-210">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="c7778-211"><strong>Kullanıcı</strong> sekmesindeki <strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Finance and Operations kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="c7778-211">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="c7778-212">Bildirimlerin gönderileceği kullanıcıları seçin ve bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="c7778-212">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="c7778-213">Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="c7778-213">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="c7778-214">İş akışında yaptığınız değişiklikler hakkında açıklamalar girin</span><span class="sxs-lookup"><span data-stu-id="c7778-214">Enter comments about the changes that you made to the workflow</span></span>
<span data-ttu-id="c7778-215">İş akışında yaptığınız değişiklikler hakkında açıklamalar girmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c7778-215">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="c7778-216">Sol bölmede **Notlar**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-216">In the left pane, click **Notes**.</span></span>
2.  <span data-ttu-id="c7778-217">**İş akışı hakkında yorumlar girin** alanında, yorumlarınızı girin.</span><span class="sxs-lookup"><span data-stu-id="c7778-217">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3.  <span data-ttu-id="c7778-218">Yorumlarınızı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="c7778-218">Review your comments.</span></span> <span data-ttu-id="c7778-219">Yorumlarınızı ekledikten sonra üzerlerinde değişiklik yapamazsınız.</span><span class="sxs-lookup"><span data-stu-id="c7778-219">After you add comments, you can't modify them.</span></span>
4.  <span data-ttu-id="c7778-220">**Yorum geçmişi** alanına yorumlarınızı eklemek için **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c7778-220">Click **Add** to add your comments to the **Comment history** area.</span></span>





