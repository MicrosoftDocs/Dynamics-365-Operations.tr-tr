---
title: Teams'de izin isteklerini yönetme
description: Bu konuda Microsoft Teams uygulamasındaki Dynamics 365 Human Resources uygulamasında, nasıl izin isteneceği gösterilmektedir.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: c7b74983cbddf661456b0a65939e272078d59f6d
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828956"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="4404d-103">Teams'de izin isteklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="4404d-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="4404d-104">Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulaması, hızlı bir şekilde izin isteğinde bulunmanıza ve izin bakiyesi bilgilerinizi doğrudan Microsoft Teams platformunda görüntülemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4404d-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="4404d-105">Bilgi istemek ve bir izin isteğini başlatmak için bir sohbet botu ile etkileşim kurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="4404d-106">**İzin** sekmesi, daha ayrıntılı bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="4404d-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="4404d-107">Ek olarak, ekipte yaklaşan izinler hakkında kişilere bilgi ve Human Resources uygulamasının dışındaki sohbetleri gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-107">In addition, you can send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="4404d-108">Uygulamayı yükleme</span><span class="sxs-lookup"><span data-stu-id="4404d-108">Install the app</span></span>

<span data-ttu-id="4404d-109">Human Resources uygulamasını Teams mağazasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="4404d-110">Microsoft Teams platformuna üç nokta simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teams izin uygulaması üç nokta simgesi](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="4404d-112">Dynamics 365 Human Resources uygulamasını arayın ve ardından **Human Resources** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teams izin uygulaması HR kutucuğu](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="4404d-114">Uygulamayı yüklemek için **Ekle** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-114">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teams izin uygulaması yükleme](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="4404d-116">Uygulama otomatik olarak oturum açmazsa oturum açmak için **Ayarlar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teams izin uygulaması Ayarlar sekmesi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="4404d-118">Oturum açma iletişim kutusunu görmüyorsanız açılır pencerelere izin vermek için tarayıcı ayarlarınızı kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="4404d-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="4404d-119">Birden fazla Human Resources örneğine erişiminiz varsa **Ayarlar** sekmesinden, hangi ortama bağlanmak istediğinizi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="4404d-120">Uygulama artık Sistem Yöneticisi güvenlik rolünü destekliyor.</span><span class="sxs-lookup"><span data-stu-id="4404d-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="4404d-121">Bot kullanma</span><span class="sxs-lookup"><span data-stu-id="4404d-121">Use the bot</span></span>

<span data-ttu-id="4404d-122">Uygulama yüklendikten sonra botun, sizin adınıza gerçekleştirebileceği eylem türlerini bildiren bir hoş geldiniz iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4404d-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams izin uygulaması botun hoş geldiniz iletisi](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="4404d-124">Bot ile ilk kez etkileşimde bulunurken oturum açmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="4404d-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="4404d-125">Oturum açma iletişim kutusunu görmüyorsanız açılır pencerelere izin vermek için tarayıcı ayarlarınızı kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="4404d-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="4404d-126">Bottan şunları isteyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4404d-126">You can ask the bot to:</span></span>

- <span data-ttu-id="4404d-127">Kayıtlı olduğunuz her izin türü için izin bakiyesi bilgisini göstermesini.</span><span class="sxs-lookup"><span data-stu-id="4404d-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources Teams izin uygulaması bakiyeleri gösterme](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="4404d-129">Belirli bir izin türü hakkında ek ayrıntıların gösterilmesi.</span><span class="sxs-lookup"><span data-stu-id="4404d-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources Teams izin uygulaması ayrıntıları gösterme](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="4404d-131">Kendiniz için bir izin isteği başlatın.</span><span class="sxs-lookup"><span data-stu-id="4404d-131">Start a leave request for you.</span></span>

   ![Human Resources Teams izin uygulaması izin isteği](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="4404d-133">Bir izin talebini başlattıktan sonra, kartın içindeki günleri ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Human Resources Teams izin uygulaması isteği düzenleme](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="4404d-135">Bilgi girişini tamamladığınızda onaya göndermek için **Gönder** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="4404d-136">Daha sonra geri dönmek için **Taslak olarak kaydet**'i de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-136">You can also select **Save as draft** to come back to it later.</span></span>

![Human Resources Teams izin uygulaması istek gönderme](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="4404d-138">Teams'de izninizi yönetme</span><span class="sxs-lookup"><span data-stu-id="4404d-138">Manage your leave in Teams</span></span>

<span data-ttu-id="4404d-139">**İzin** sekmesi şunları görüntülemenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="4404d-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="4404d-140">Kayıtlı olduğunuz her izin türü için bakiye bilgisini</span><span class="sxs-lookup"><span data-stu-id="4404d-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="4404d-141">Yaklaşan izin istekleri</span><span class="sxs-lookup"><span data-stu-id="4404d-141">Upcoming leave requests</span></span>

- <span data-ttu-id="4404d-142">İzin süresi istekleri</span><span class="sxs-lookup"><span data-stu-id="4404d-142">Time-off requests</span></span>

- <span data-ttu-id="4404d-143">Taslak izin istekleri</span><span class="sxs-lookup"><span data-stu-id="4404d-143">Draft leave requests</span></span>

![Human Resources Teams izin uygulaması İzin sekmesi](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="4404d-145">Yeni bir istek oluşturma</span><span class="sxs-lookup"><span data-stu-id="4404d-145">Create a new request</span></span>

1. <span data-ttu-id="4404d-146">Yeni bir izin isteği oluşturmak için **Yeni istek** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4404d-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teams izin uygulaması Yeni istek](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="4404d-148">Talep ettiğiniz izin süresi için gün veya günleri girin ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teams izin uygulaması izin ekleme](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="4404d-150">Uygunsa, bir neden kodu girin.</span><span class="sxs-lookup"><span data-stu-id="4404d-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="4404d-151">Ayrıca açıklama girin ve herhangi bir ek ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4404d-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="4404d-152">Bilgi girişini tamamladığınızda onay için göndermek üzere **Gönder**'e basın.</span><span class="sxs-lookup"><span data-stu-id="4404d-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="4404d-153">Daha sonra geri dönmek için **Taslak olarak kaydet**'e de basabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="4404d-154">Taslak istekleri yönetme</span><span class="sxs-lookup"><span data-stu-id="4404d-154">Manage draft requests</span></span>

1. <span data-ttu-id="4404d-155">**Taslaklar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-155">Select the **Drafts** tab.</span></span>

   ![Human Resources Teams izin uygulaması Taslaklar sekmesi](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="4404d-157">İsteği düzenlemek için kalemi veya isteği silmek için çöp kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="4404d-158">Gerekli tüm değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="4404d-158">Make any necessary changes.</span></span> <span data-ttu-id="4404d-159">Bilgi girişini tamamladığınızda onay için göndermek üzere **Gönder**'e basın.</span><span class="sxs-lookup"><span data-stu-id="4404d-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="4404d-160">Daha sonra geri dönmek için **Taslak olarak kaydet**'i de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teams izin uygulaması taslağı düzenleme](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="4404d-162">Teams bildirimlerini yanıtlama</span><span class="sxs-lookup"><span data-stu-id="4404d-162">Respond to Teams notifications</span></span>

<span data-ttu-id="4404d-163">Siz veya onaylayan taraf olduğunuz bir çalışan izin talebi gönderdiğinde, Teams'de Human Resources uygulamasından bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4404d-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="4404d-164">Görüntülemek için bildirimi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-164">You can select the notification to view it.</span></span> <span data-ttu-id="4404d-165">Bildirimler **Sohbet** alanında da görünür.</span><span class="sxs-lookup"><span data-stu-id="4404d-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="4404d-166">Onaylayan iseniz, bildirimden **Onayla** veya **Reddet** seçeneklerini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="4404d-167">Ayrıca, isteğe bağlı bir ileti de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-167">You can also provide an optional message.</span></span>

![Human Resources Teams uygulamasında izin talebi bildirimi](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="4404d-169">Yaklaşan izin bilgilerini iş arkadaşlarınıza gönderme</span><span class="sxs-lookup"><span data-stu-id="4404d-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="4404d-170">Teams için Human Resources uygulamasını yükledikten sonra, ekiplere veya sohbetlere karşı iş arkadaşlarınıza yaklaşan izinler hakkında bilgi gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="4404d-171">Ekipte veya Teams'deki bir sohbette, sohbet penceresinin altındaki Human Resources düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Sohbet penceresinin altında Human Resources düğmesi](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="4404d-173">Paylaşmak istediğiniz izin isteğini seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-173">Select the leave request you want to share.</span></span> <span data-ttu-id="4404d-174">Bir taslak olarak izin isteğini paylaşmak istiyorsanız, önce **Taslaklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Paylaşılacak bir yaklaşan izin isteğini seçme](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="4404d-176">İzin talebiniz sohbette gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4404d-176">Your leave request will display in the chat.</span></span>

![Human Resources izin istek kartı](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="4404d-178">Bir taslak talep paylaştıysanız, taslak olarak görüntülenecektir:</span><span class="sxs-lookup"><span data-stu-id="4404d-178">If you shared a draft request, it will display as a draft:</span></span>

![Human Resources taslak izin istek kartı](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="4404d-180">Ekip izin takviminizi görüntüleme</span><span class="sxs-lookup"><span data-stu-id="4404d-180">View your team's leave calendar</span></span>

<span data-ttu-id="4404d-181">Astları bulunan bir yönetici iseniz, takımınızın onaylanmış ve bekleyen izinlerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="4404d-182">Teams'de Human Resources uygulamasında, **İzin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="4404d-183">**Ekip takvimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4404d-183">Select **Team calendar**.</span></span>

   ![Human Resources Teams uygulamasında takvimi görüntüleme](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="4404d-185">Takvim, doğrudan astlarınıza ait onaylı ve beklemede olan izinleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="4404d-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Human Resources Teams uygulamasında izin takvimi](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="4404d-187">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="4404d-187">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="4404d-188">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="4404d-188">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="4404d-189">Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir.</span><span class="sxs-lookup"><span data-stu-id="4404d-189">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="4404d-190">Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="4404d-190">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="4404d-191">LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-191">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="4404d-192">LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar.</span><span class="sxs-lookup"><span data-stu-id="4404d-192">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="4404d-193">Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft'un  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) servisine aktarılır.</span><span class="sxs-lookup"><span data-stu-id="4404d-193">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="4404d-194">Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="4404d-194">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="4404d-195">LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="4404d-195">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="4404d-196">LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure bot çerçevesine gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="4404d-196">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="4404d-197">Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="4404d-197">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="4404d-198">Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4404d-198">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="4404d-199">Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4404d-199">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="4404d-200">Microsoft Teams, Azure Event Grid ve Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4404d-200">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="4404d-201">Microsoft Teams'de Dynamics 365 Human Resources uygulamasını kullanılırken, belirli müşteri verileri kiracının Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışına akabilir.</span><span class="sxs-lookup"><span data-stu-id="4404d-201">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="4404d-202">Dynamics 365 Human Resources çalışanın izin talebini ve iş akışı görev ayrıntılarını Microsoft Azure Event Grid ve Microsoft Teams uygulamalarına iletir.</span><span class="sxs-lookup"><span data-stu-id="4404d-202">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="4404d-203">Bu veriler 24 saate kadar Microsoft Azure Event Grid uygulamasında saklanabilir ve Amerika Birleşik Devletlerinde işlenir, iletim ve bekleyen veri şifrelenir ve eğitim veya hizmet iyileştirmeleri için Microsoft veya onun alt işlemcileri tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="4404d-203">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="4404d-204">Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="4404d-204">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="4404d-205">Human Resources uygulamasında sohbet botu ile konuşurken, görüşme içeriği Azure Cosmos DB uygulamasında depolanabilir ve Microsoft Teams uygulamasına iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="4404d-205">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="4404d-206">Bu veriler, Azure Cosmos DB uygulamasında 24 saate kadar depolanabilir ve kiracınızın Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışında işlenerek, aktarım ve geri kalanında şifrelenir ve Microsoft 'un veya hizmet geliştirmeleri için bunların alt işlemcileri tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="4404d-206">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="4404d-207">Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="4404d-207">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="4404d-208">Kuruluşunuz veya kuruluşunuzdaki kullanıcılarınız için Microsoft Teams içinde Human Resources uygulamasına erişimi kısıtlamak için, bkz. [Microsoft Teams'deki uygulama izin ilkelerini yönetme](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="4404d-208">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="4404d-209">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="4404d-209">See also</span></span>

[<span data-ttu-id="4404d-210">Microsoft Teams platformunu indirme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="4404d-210">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="4404d-211">Microsoft Teams yardım merkezi</span><span class="sxs-lookup"><span data-stu-id="4404d-211">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="4404d-212">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="4404d-212">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
