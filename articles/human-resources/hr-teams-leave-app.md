---
title: Teams'de izin isteklerini yönetme
description: Bu konuda Microsoft Teams uygulamasındaki Dynamics 365 Human Resources uygulamasında, nasıl izin isteneceği gösterilmektedir.
author: andreabichsel
manager: tfehr
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 79bded5a241a8d5de1847adff3e663359ce1b26f
ms.sourcegitcommit: d7c18228256daeefbf6518c3ef82fed4f7dbc161
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571740"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="66912-103">Teams'de izin isteklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="66912-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="66912-104">Microsoft Teams platformundaki Dynamics 365 Human Resources uygulaması, hızlı bir şekilde izin isteğinde bulunmanıza ve izin bakiyesi bilgilerinizi doğrudan Microsoft Teams platformunda görüntülemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="66912-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="66912-105">Bilgi istemek ve bir izin isteğini başlatmak için bir sohbet botu ile etkileşim kurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="66912-106">**İzin** sekmesi, daha ayrıntılı bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="66912-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="66912-107">Teams'de yaklaşan izinler hakkında kişilere bilgi ve Human Resources uygulamasının dışındaki sohbetleri gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="66912-108">Uygulamayı yükleme</span><span class="sxs-lookup"><span data-stu-id="66912-108">Install the app</span></span>

<span data-ttu-id="66912-109">Dynamics 365 Human Resources uygulamasını Teams mağazasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="66912-110">Microsoft Teams platformuna üç nokta simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teams izin uygulaması üç nokta simgesi](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="66912-112">Dynamics 365 Human Resources uygulamasını arayın ve ardından **Human Resources** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teams izin uygulaması HR kutucuğu](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="66912-114">Uygulamayı yüklemek için **Ekle** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-114">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teams izin uygulaması yükleme](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="66912-116">Uygulama otomatik olarak oturum açmazsa oturum açmak için **Ayarlar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teams izin uygulaması Ayarlar sekmesi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="66912-118">Oturum açma iletişim kutusunu görmüyorsanız açılır pencerelere izin vermek için tarayıcı ayarlarınızı kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="66912-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="66912-119">Birden fazla Human Resources örneğine erişiminiz varsa **Ayarlar** sekmesinden, hangi ortama bağlanmak istediğinizi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="66912-120">Uygulama artık Sistem Yöneticisi güvenlik rolünü destekliyor.</span><span class="sxs-lookup"><span data-stu-id="66912-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="66912-121">Bot kullanma</span><span class="sxs-lookup"><span data-stu-id="66912-121">Use the bot</span></span>

<span data-ttu-id="66912-122">Uygulama yüklendikten sonra botun, sizin adınıza gerçekleştirebileceği eylem türlerini bildiren bir hoş geldiniz iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="66912-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams izin uygulaması botun hoş geldiniz iletisi](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="66912-124">Bot ile ilk kez etkileşimde bulunurken oturum açmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="66912-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="66912-125">Oturum açma iletişim kutusunu görmüyorsanız açılır pencerelere izin vermek için tarayıcı ayarlarınızı kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="66912-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="66912-126">Bottan şunları isteyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="66912-126">You can ask the bot to:</span></span>

- <span data-ttu-id="66912-127">Kendiniz için bir izin isteği başlatın.</span><span class="sxs-lookup"><span data-stu-id="66912-127">Start a leave request for you.</span></span>

  ![Teams sohbetinde izin isteği başlatma](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="66912-129">Sohbet botu sizin için bir izin isteği dolduracaktır.</span><span class="sxs-lookup"><span data-stu-id="66912-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="66912-130">**İzin talep et**'i seçin ve isteğinizin ayrıntılarını düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="66912-130">Select **Request time off** and edit the details for your request.</span></span>

  ![İzin İsteği ayrıntılarını düzenleme](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="66912-132">İzin İsteği ayrıntılarınızı düzenlemeyi tamamladığınızda onaya göndermek için **Gönder** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![İzin İsteği gönderme](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="66912-134">Teams'de izninizi yönetme</span><span class="sxs-lookup"><span data-stu-id="66912-134">Manage your leave in Teams</span></span>

<span data-ttu-id="66912-135">**İzin** sekmesi şunları görüntülemenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="66912-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="66912-136">Kayıtlı olduğunuz her izin türü için bakiye bilgisini</span><span class="sxs-lookup"><span data-stu-id="66912-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="66912-137">Yaklaşan izin istekleri</span><span class="sxs-lookup"><span data-stu-id="66912-137">Upcoming leave requests</span></span>

- <span data-ttu-id="66912-138">İzin süresi istekleri</span><span class="sxs-lookup"><span data-stu-id="66912-138">Time-off requests</span></span>

- <span data-ttu-id="66912-139">Taslak izin istekleri</span><span class="sxs-lookup"><span data-stu-id="66912-139">Draft leave requests</span></span>

![Human Resources Teams izin uygulaması İzin sekmesi](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="66912-141">Yeni bir istek oluşturma</span><span class="sxs-lookup"><span data-stu-id="66912-141">Create a new request</span></span>

1. <span data-ttu-id="66912-142">Yeni bir izin isteği oluşturmak için **Yeni istek** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="66912-142">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teams izin uygulaması Yeni istek](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="66912-144">Talep ettiğiniz izin süresi için gün veya günleri girin ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teams izin uygulaması izin ekleme](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="66912-146">Uygunsa, bir neden kodu girin.</span><span class="sxs-lookup"><span data-stu-id="66912-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="66912-147">Ayrıca açıklama girin ve herhangi bir ek ekleyin.</span><span class="sxs-lookup"><span data-stu-id="66912-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="66912-148">Bilgi girişini tamamladığınızda onay için göndermek üzere **Gönder**'e basın.</span><span class="sxs-lookup"><span data-stu-id="66912-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="66912-149">Daha sonra geri dönmek için **Taslak olarak kaydet**'e de basabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="66912-150">Taslak istekleri yönetme</span><span class="sxs-lookup"><span data-stu-id="66912-150">Manage draft requests</span></span>

1. <span data-ttu-id="66912-151">**Taslaklar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-151">Select the **Drafts** tab.</span></span>

   ![Human Resources Teams izin uygulaması Taslaklar sekmesi](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="66912-153">İsteği düzenlemek için kalemi veya isteği silmek için çöp kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="66912-154">Gerekli tüm değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="66912-154">Make any necessary changes.</span></span> <span data-ttu-id="66912-155">Bilgi girişini tamamladığınızda onay için göndermek üzere **Gönder**'e basın.</span><span class="sxs-lookup"><span data-stu-id="66912-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="66912-156">Daha sonra geri dönmek için **Taslak olarak kaydet**'i de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teams izin uygulaması taslağı düzenleme](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="66912-158">Teams bildirimlerini yanıtlama</span><span class="sxs-lookup"><span data-stu-id="66912-158">Respond to Teams notifications</span></span>

<span data-ttu-id="66912-159">Siz veya onaylayan taraf olduğunuz bir çalışan izin talebi gönderdiğinde, Teams'de Human Resources uygulamasından bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="66912-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="66912-160">Görüntülemek için bildirimi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-160">You can select the notification to view it.</span></span> <span data-ttu-id="66912-161">Bildirimler **Sohbet** alanında da görünür.</span><span class="sxs-lookup"><span data-stu-id="66912-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="66912-162">Onaylayan iseniz, bildirimden **Onayla** veya **Reddet** seçeneklerini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="66912-163">Ayrıca, isteğe bağlı bir ileti de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-163">You can also provide an optional message.</span></span>

![Human Resources Teams uygulamasında izin talebi bildirimi](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="66912-165">Yaklaşan izin bilgilerini iş arkadaşlarınıza gönderme</span><span class="sxs-lookup"><span data-stu-id="66912-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="66912-166">Teams için Human Resources uygulamasını yükledikten sonra, ekiplere veya sohbetlere karşı iş arkadaşlarınıza yaklaşan izinler hakkında bilgi gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="66912-167">Ekipte veya Teams'deki bir sohbette, sohbet penceresinin altındaki Human Resources düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Sohbet penceresinin altında Human Resources düğmesi](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="66912-169">Paylaşmak istediğiniz izin isteğini seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-169">Select the leave request you want to share.</span></span> <span data-ttu-id="66912-170">Bir taslak olarak izin isteğini paylaşmak istiyorsanız, önce **Taslaklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Paylaşılacak bir yaklaşan izin isteğini seçme](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="66912-172">İzin talebiniz sohbette gösterilir.</span><span class="sxs-lookup"><span data-stu-id="66912-172">Your leave request will display in the chat.</span></span>

![Human Resources izin istek kartı](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="66912-174">Bir taslak talep paylaştıysanız, taslak olarak görüntülenecektir:</span><span class="sxs-lookup"><span data-stu-id="66912-174">If you shared a draft request, it will display as a draft:</span></span>

![Human Resources taslak izin istek kartı](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="66912-176">Ekip izin takviminizi görüntüleme</span><span class="sxs-lookup"><span data-stu-id="66912-176">View your team's leave calendar</span></span>

<span data-ttu-id="66912-177">Astları bulunan bir yönetici iseniz, takımınızın onaylanmış ve bekleyen izinlerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="66912-178">Teams'de Human Resources uygulamasında, **İzin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="66912-179">**Ekip takvimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-179">Select **Team calendar**.</span></span> <span data-ttu-id="66912-180">Takvim, doğrudan astlarınıza ait onaylı ve beklemede olan izinleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="66912-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![Human Resources Teams uygulamasında takvimi görüntüleme](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="66912-182">Takım takvimini göremiyorsanız yöneticinizden takvimi etkinleştirmesini isteyin.</span><span class="sxs-lookup"><span data-stu-id="66912-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="66912-183">Daha fazla bilgi için bkz. [Yükleme ve ayarlama](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="66912-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="66912-184">Desteklenen diller</span><span class="sxs-lookup"><span data-stu-id="66912-184">Supported languages</span></span>

<span data-ttu-id="66912-185">Teams'deki Dynamics 365 Human Resources uygulaması aşağıdaki dilleri destekler:</span><span class="sxs-lookup"><span data-stu-id="66912-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="66912-186">Yerel Ayar Kimliği</span><span class="sxs-lookup"><span data-stu-id="66912-186">Locale ID</span></span> | <span data-ttu-id="66912-187">Dil</span><span class="sxs-lookup"><span data-stu-id="66912-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="66912-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="66912-188">de-DE</span></span> | <span data-ttu-id="66912-189">Almanca (Almanya)</span><span class="sxs-lookup"><span data-stu-id="66912-189">German (Germany)</span></span> |
| <span data-ttu-id="66912-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="66912-190">es-ES</span></span> | <span data-ttu-id="66912-191">İspanyolca (İspanya)</span><span class="sxs-lookup"><span data-stu-id="66912-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="66912-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="66912-192">es-MX</span></span> | <span data-ttu-id="66912-193">İspanyolca (Meksika)</span><span class="sxs-lookup"><span data-stu-id="66912-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="66912-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="66912-194">fr-CA</span></span> | <span data-ttu-id="66912-195">Fransızca (Kanada)</span><span class="sxs-lookup"><span data-stu-id="66912-195">French (Canada)</span></span> |
| <span data-ttu-id="66912-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="66912-196">fr-FR</span></span> | <span data-ttu-id="66912-197">Fransızca (Fransa)</span><span class="sxs-lookup"><span data-stu-id="66912-197">French (France)</span></span> |
| <span data-ttu-id="66912-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="66912-198">it-IT</span></span> | <span data-ttu-id="66912-199">İtalyanca (İtalya)</span><span class="sxs-lookup"><span data-stu-id="66912-199">Italian (Italy)</span></span> |
| <span data-ttu-id="66912-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="66912-200">nl-NL</span></span> | <span data-ttu-id="66912-201">Felemenkçe (Hollanda)</span><span class="sxs-lookup"><span data-stu-id="66912-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="66912-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="66912-202">pt-BR</span></span> | <span data-ttu-id="66912-203">Portekizce (Brezilya)</span><span class="sxs-lookup"><span data-stu-id="66912-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="66912-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="66912-204">tr-TR</span></span> | <span data-ttu-id="66912-205">Türkçe (Türkiye)</span><span class="sxs-lookup"><span data-stu-id="66912-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="66912-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="66912-206">zh-CN</span></span> | <span data-ttu-id="66912-207">Çince (Basitleştirilmiş)</span><span class="sxs-lookup"><span data-stu-id="66912-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="66912-208">Sorun Giderme</span><span class="sxs-lookup"><span data-stu-id="66912-208">Troubleshooting</span></span>

<span data-ttu-id="66912-209">Dynamics 365 Human Resources Teams uygulamasında oturum açarken veya uygulamayı kullanırken sorun yaşıyorsanız, bu sorun giderme yönergelerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="66912-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="66912-210">Sorun giderme işleminden sonra hala sorun yaşıyorsanız, desteğe başvurun.</span><span class="sxs-lookup"><span data-stu-id="66912-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="66912-211">Daha fazla bilgi için [Destek alma](hr-admin-troubleshooting-support.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="66912-211">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="66912-212">Teams'de Human Resource uygulaması oturumu açılamıyor</span><span class="sxs-lookup"><span data-stu-id="66912-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="66912-213">Uygulamada oturum açamazsınız, Microsoft Teams'de oturum açarken kullandığınız hesap Dynamics 365 Human Resources'taki bir personel kaydıyla ilişkilendirilmemiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="66912-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="66912-214">Çalışan kaydınızın doğru bir şekilde ilişkilendirildiğinden emin olmak için sistem yöneticinize başvurun.</span><span class="sxs-lookup"><span data-stu-id="66912-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="66912-215">Çeviriler doğru görüntülenmiyor</span><span class="sxs-lookup"><span data-stu-id="66912-215">Translations don't display correctly</span></span>

<span data-ttu-id="66912-216">Çeviriler beklendiği gibi görüntülenmiyorsa Teams'de seçtiğiniz dilin Human Resources **Kullanıcı seçenekleri**'nde seçilen dille eşleştiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="66912-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="66912-217">Teams'de, **Ayarlar**'da **Uygulama dili**'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="66912-217">In Teams, look at **App language** in **Settings**.</span></span>

![Teams ayarları](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="66912-219">Human Resources'ta **Ayarlar**'ı ve ardından **Kullanıcı seçenekleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="66912-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="66912-220">**Dil** alanının Teams'deki **Uygulama dili** alanıyla eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="66912-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Human Resources Kullanıcı seçenekleri](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="66912-222">Hala çeviri sorunları yaşıyorsanız bize bildirin.</span><span class="sxs-lookup"><span data-stu-id="66912-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="66912-223">Bilgi için bkz. [Finance and Operations uygulamaları veya Lifecycle Services (LCS) için destek alma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="66912-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="66912-224">Teams'deki Human Resources uygulamasındaki izin isteklerini onaylarken hata oluştu</span><span class="sxs-lookup"><span data-stu-id="66912-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="66912-225">Teams uygulamasında izin isteklerini onaylamaya çalışırken hata alırsanız, aşağıdaki sorun giderme adımlarını gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="66912-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="66912-226">Microsoft Teams'te Oturum açmak için kullandığınız hesabın Dynamics 365 Human Resources'a erişmek için kullandığınız hesapla aynı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="66912-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="66912-227">İzin onayı için iş akışı ayarlarını denetleyerek istek için geçerli bir onaylayan olduğunuzu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="66912-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="66912-228">İzin isteği iş akışları hakkında daha fazla bilgi için bkz. [İzin isteği iş akışı oluşturma](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="66912-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="66912-229">Bilinen erişilebilirlik sorunları</span><span class="sxs-lookup"><span data-stu-id="66912-229">Known accessibility issues</span></span>

<span data-ttu-id="66912-230">Teams'te Human Resources uygulama, gelecekteki sürümlerde düzeltilirken aşağıdaki erişilebilirlik sorunlarına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="66912-230">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="66912-231">Çıkış</span><span class="sxs-lookup"><span data-stu-id="66912-231">Issue</span></span> | <span data-ttu-id="66912-232">Geçici çözüm veya açıklama</span><span class="sxs-lookup"><span data-stu-id="66912-232">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="66912-233">Masaüstünde %400 yakınlaştırma eylemi, bazı eylem düğmelerini görünümden gizler.</span><span class="sxs-lookup"><span data-stu-id="66912-233">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="66912-234">Bu yakınlaştırma düzeyini destekleyene kadar bunun yerine Büyüteç kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="66912-234">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="66912-235">**Zaman aşımı** sekmesinde, VoiceOver zaman kılavuzu için üstbilgiyi okurken düğme eylemini duyurur.</span><span class="sxs-lookup"><span data-stu-id="66912-235">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="66912-236">Kılavuz içindeki başlık ve öğeler yıla göre gruplandırılır ve bunlar daraltılabilir öğelerdir.</span><span class="sxs-lookup"><span data-stu-id="66912-236">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="66912-237">VoiceOver, bunu işlem yapılabilir bir madde olarak yorumlar, ancak böyle değildir.</span><span class="sxs-lookup"><span data-stu-id="66912-237">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="66912-238">**İzin süresi** sekmesinde, Yeni bir istekte **neden koduna** giderken fazladan bir çekme hareketi vardır.</span><span class="sxs-lookup"><span data-stu-id="66912-238">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="66912-239">Çekme gezintisinin alınmaya çalıştığı gizli denetim yoktur.</span><span class="sxs-lookup"><span data-stu-id="66912-239">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="66912-240">**İzin süresi** sekmesinde, takvim açıkken çekme yaparken yeni bir istekte en üstte veya bir istek düzenlenirken denetimin dışında sona erer.</span><span class="sxs-lookup"><span data-stu-id="66912-240">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="66912-241">**Bugüne git**'e ulaştığınızda , denetimin sonuna kadar, en üste geri dönmek için ters yönde çekin.</span><span class="sxs-lookup"><span data-stu-id="66912-241">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="66912-242">**Sohbet** sekmesinde, yardımcı aracı veya klavye gezintisini kullanırken bir tarih girdiğinizde odak en üste geri atlar.</span><span class="sxs-lookup"><span data-stu-id="66912-242">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="66912-243">Sekmesini yeniden girin.</span><span class="sxs-lookup"><span data-stu-id="66912-243">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="66912-244">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="66912-244">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="66912-245">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="66912-245">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="66912-246">Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir.</span><span class="sxs-lookup"><span data-stu-id="66912-246">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="66912-247">Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="66912-247">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="66912-248">LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-248">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="66912-249">LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar.</span><span class="sxs-lookup"><span data-stu-id="66912-249">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="66912-250">Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft'un  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) servisine aktarılır.</span><span class="sxs-lookup"><span data-stu-id="66912-250">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="66912-251">Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="66912-251">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="66912-252">LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="66912-252">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="66912-253">LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure bot çerçevesine gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="66912-253">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="66912-254">Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="66912-254">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="66912-255">Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66912-255">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="66912-256">Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="66912-256">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="66912-257">Microsoft Teams, Azure Event Grid ve Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="66912-257">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="66912-258">Microsoft Teams'de Dynamics 365 Human Resources uygulamasını kullanılırken, belirli müşteri verileri kiracının Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışına akabilir.</span><span class="sxs-lookup"><span data-stu-id="66912-258">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="66912-259">Dynamics 365 Human Resources çalışanın izin talebini ve iş akışı görev ayrıntılarını Microsoft Azure Event Grid ve Microsoft Teams uygulamalarına iletir.</span><span class="sxs-lookup"><span data-stu-id="66912-259">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="66912-260">Bu veriler 24 saate kadar Microsoft Azure Event Grid uygulamasında saklanabilir ve Amerika Birleşik Devletlerinde işlenir, iletim ve bekleyen veri şifrelenir ve eğitim veya hizmet iyileştirmeleri için Microsoft veya onun alt işlemcileri tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="66912-260">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="66912-261">Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="66912-261">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="66912-262">Human Resources uygulamasında sohbet botu ile konuşurken, görüşme içeriği Azure Cosmos DB uygulamasında depolanabilir ve Microsoft Teams uygulamasına iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="66912-262">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="66912-263">Bu veriler, Azure Cosmos DB uygulamasında 24 saate kadar depolanabilir ve kiracınızın Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışında işlenerek, aktarım ve geri kalanında şifrelenir ve Microsoft 'un veya hizmet geliştirmeleri için bunların alt işlemcileri tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="66912-263">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="66912-264">Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="66912-264">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="66912-265">Kuruluşunuz veya kuruluşunuzdaki kullanıcılarınız için Microsoft Teams içinde Human Resources uygulamasına erişimi kısıtlamak için, bkz. [Microsoft Teams'deki uygulama izin ilkelerini yönetme](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="66912-265">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="66912-266">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="66912-266">See also</span></span>

[<span data-ttu-id="66912-267">Microsoft Teams platformunu indirme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="66912-267">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="66912-268">Microsoft Teams yardım merkezi</span><span class="sxs-lookup"><span data-stu-id="66912-268">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="66912-269">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="66912-269">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]