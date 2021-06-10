---
title: Teams'de izin isteklerini yönetme
description: Bu konuda Microsoft Teams uygulamasındaki Dynamics 365 Human Resources uygulamasında, nasıl izin isteneceği gösterilmektedir.
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 661bb8369fe4dbe6cdf6ee0fb05d16f4350ecf5a
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097271"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="d8030-103">Teams'de izin isteklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="d8030-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d8030-104">Microsoft Teams platformundaki Dynamics 365 Human Resources uygulaması, hızlı bir şekilde izin isteğinde bulunmanıza ve izin bakiyesi bilgilerinizi doğrudan Microsoft Teams platformunda görüntülemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d8030-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="d8030-105">Bilgi istemek ve bir izin isteğini başlatmak için bir sohbet botu ile etkileşim kurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="d8030-106">**İzin** sekmesi, daha ayrıntılı bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="d8030-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="d8030-107">Teams'de yaklaşan izinler hakkında kişilere bilgi ve Human Resources uygulamasının dışındaki sohbetleri gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="d8030-108">Uygulamayı yükleme</span><span class="sxs-lookup"><span data-stu-id="d8030-108">Install the app</span></span>

<span data-ttu-id="d8030-109">Dynamics 365 Human Resources uygulamasını Teams mağazasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="d8030-110">Microsoft Teams İçinde uygulamalar listesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d8030-110">In Microsoft Teams, navigate to the list of apps.</span></span>
 
2. <span data-ttu-id="d8030-111">Dynamics 365 Human Resources uygulamasını arayın ve ardından **Human Resources** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

3. <span data-ttu-id="d8030-112">Uygulamayı yüklemek için **Ekle** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-112">Select the **Add** button to install the app.</span></span>

<span data-ttu-id="d8030-113">Uygulama otomatik olarak oturum açmazsa oturum açmak için **Ayarlar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-113">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

> [!NOTE]
> <span data-ttu-id="d8030-114">Oturum açma iletişim kutusunu görmüyorsanız açılır pencerelere izin vermek için tarayıcı ayarlarınızı kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="d8030-114">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="d8030-115">Birden fazla Human Resources örneğine erişiminiz varsa **Ayarlar** sekmesinden, hangi ortama bağlanmak istediğinizi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-115">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="d8030-116">Uygulama artık Sistem Yöneticisi güvenlik rolünü destekliyor.</span><span class="sxs-lookup"><span data-stu-id="d8030-116">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="d8030-117">Bot kullanma</span><span class="sxs-lookup"><span data-stu-id="d8030-117">Use the bot</span></span>

<span data-ttu-id="d8030-118">Uygulama yüklendikten sonra botun, sizin adınıza gerçekleştirebileceği eylem türlerini bildiren bir hoş geldiniz iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d8030-118">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

> [!NOTE]
> <span data-ttu-id="d8030-119">Bot ile ilk kez etkileşimde bulunurken oturum açmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="d8030-119">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="d8030-120">Oturum açma iletişim kutusunu görmüyorsanız açılır pencerelere izin vermek için tarayıcı ayarlarınızı kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="d8030-120">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="d8030-121">Bottan şunları isteyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d8030-121">You can ask the bot to:</span></span>

- <span data-ttu-id="d8030-122">Geçerli çıkış bakiylerinizi görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="d8030-122">View your current leave balances.</span></span> <span data-ttu-id="d8030-123">Örneğin, "bakiyeleri görüntüle" yazan bir ileti gönderin.</span><span class="sxs-lookup"><span data-stu-id="d8030-123">For example, send a message that says, "View leave balances."</span></span>

- <span data-ttu-id="d8030-124">Kendiniz için bir izin isteği başlatın.</span><span class="sxs-lookup"><span data-stu-id="d8030-124">Start a leave request for you.</span></span> <span data-ttu-id="d8030-125">Örneğin, "izin al" veya "sonraki Perşembe ve Cuma günleri izin almak istiyorum" şeklinde bir ileti gönderin, böylece tatil izin türüne izin vermek üzere daha belirgin olur.</span><span class="sxs-lookup"><span data-stu-id="d8030-125">For example, send a message that says, “Take time off” or “I want to take vacation time off next Thursday and Friday” to be more specific for requesting leave for the vacation leave type.</span></span> 

  ![Teams sohbetinde izin isteği başlatma](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="d8030-127">Sohbet botu sizin için bir izin isteği dolduracaktır.</span><span class="sxs-lookup"><span data-stu-id="d8030-127">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="d8030-128">**İzin talep et**'i seçin ve isteğinizin ayrıntılarını düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="d8030-128">Select **Request time off** and edit the details for your request.</span></span>

   <span data-ttu-id="d8030-129">Aynı tarih için birden fazla izin türü için ayrılma istekleri göndermek istiyorsanız, **Diğer Seçenekler** menüsünde o **ile bölünen gün** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-129">If you want to submit leave requests for multiple leave types for the same date, select the **Split day with** option from the **More options** menu.</span></span> 

   <span data-ttu-id="d8030-130">İzin isteği birimi gün olarak bir yarım gün bırak seçeneğini belirlerseniz, **Diğer Seçenekler** menüsünde **yarım gün tanımı** seçeneğini belirleyerek, zamanı ilk yarım gün veya ikinci yarım gün talep etmek isteyip istemediğinizi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-130">If you select a half day leave when the leave request unit is in days, you can specify whether you want to request time off the first half day or the second half day by selecting the **Half day definition** option from the **More options** menu.</span></span>
   
   ![Yarım gün tanımı](./media/HalfDayDefinitions.png)

- <span data-ttu-id="d8030-132">İzin İsteği ayrıntılarınızı düzenlemeyi tamamladığınızda onaya göndermek için **Gönder** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![İzin İsteği gönderme](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="d8030-134">Teams'de izninizi yönetme</span><span class="sxs-lookup"><span data-stu-id="d8030-134">Manage your leave in Teams</span></span>

<span data-ttu-id="d8030-135">**İzin** sekmesi şunları görüntülemenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="d8030-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="d8030-136">Kayıtlı olduğunuz her izin türü için bakiye bilgisini</span><span class="sxs-lookup"><span data-stu-id="d8030-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="d8030-137">Yaklaşan izin istekleri</span><span class="sxs-lookup"><span data-stu-id="d8030-137">Upcoming leave requests</span></span>

- <span data-ttu-id="d8030-138">İzin süresi istekleri</span><span class="sxs-lookup"><span data-stu-id="d8030-138">Time-off requests</span></span>

- <span data-ttu-id="d8030-139">Taslak izin istekleri</span><span class="sxs-lookup"><span data-stu-id="d8030-139">Draft leave requests</span></span>
 
### <a name="create-a-new-request"></a><span data-ttu-id="d8030-140">Yeni bir istek oluşturma</span><span class="sxs-lookup"><span data-stu-id="d8030-140">Create a new request</span></span>

1. <span data-ttu-id="d8030-141">Yeni bir izin isteği oluşturmak için **Yeni istek** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d8030-141">To create a new leave request, select **New request**.</span></span>

2. <span data-ttu-id="d8030-142">Talep ettiğiniz izin süresi için gün veya günleri girin ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-142">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teams izin uygulaması izin ekleme](./media/TimeOffHours.png)

3. <span data-ttu-id="d8030-144">Uygunsa, bir neden kodu girin.</span><span class="sxs-lookup"><span data-stu-id="d8030-144">If applicable, enter a reason code.</span></span> <span data-ttu-id="d8030-145">Ayrıca açıklama girin ve herhangi bir ek ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d8030-145">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="d8030-146">Farklı izin türleri için ancak aynı tarih için birden fazla izin türü için ayrılma istekleri göndermek istiyorsanız, **Diğer Seçenekler** menüsünde o **ile bölünen gün** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-146">Select the **Split day with** option from the **More options** menu if you want to submit multiple leave request entries for the same date for different leave types.</span></span>

5. <span data-ttu-id="d8030-147">İlk yarım günü veya ikinci yarım günü kapatmak isteyip istemediğinizi belirtmek için **yarım gün tanımı** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d8030-147">Select the **Half day definition** option to specify if you want to request the first half day off or the second half day off.</span></span> <span data-ttu-id="d8030-148">Bu seçenek, izin isteği birimi gün olarak kullanılırken ve istenen tutar 0,5 gün ise kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d8030-148">This option is available when the leave request unit is in days and the amount requested is 0.5 days.</span></span>

6. <span data-ttu-id="d8030-149">Bilgi girişini tamamladığınızda onaya göndermek için **Gönder** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-149">When you're done entering information, enter **Submit** to submit it for approval.</span></span> <span data-ttu-id="d8030-150">Daha sonra geri dönmek için **Taslak olarak kaydet**'e de basabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-150">You can also enter **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="d8030-151">Taslak istekleri yönetme</span><span class="sxs-lookup"><span data-stu-id="d8030-151">Manage draft requests</span></span>

1. <span data-ttu-id="d8030-152">**Taslaklar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-152">Select the **Drafts** tab.</span></span>

2. <span data-ttu-id="d8030-153">İsteği düzenlemek için kalemi veya isteği silmek için çöp kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="d8030-154">Gerekli tüm değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="d8030-154">Make any necessary changes.</span></span> <span data-ttu-id="d8030-155">Bilgi girişini tamamladığınızda onay için göndermek üzere **Gönder**'e basın.</span><span class="sxs-lookup"><span data-stu-id="d8030-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="d8030-156">Daha sonra geri dönmek için **Taslak olarak kaydet**'i de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-156">You can also select **Save as draft** to come back to it later.</span></span>
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="d8030-157">Teams bildirimlerini yanıtlama</span><span class="sxs-lookup"><span data-stu-id="d8030-157">Respond to Teams notifications</span></span>

<span data-ttu-id="d8030-158">Siz veya onaylayan taraf olduğunuz bir çalışan izin talebi gönderdiğinde, Teams'de Human Resources uygulamasından bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="d8030-158">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="d8030-159">Görüntülemek için bildirimi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-159">You can select the notification to view it.</span></span> <span data-ttu-id="d8030-160">Bildirimler **Sohbet** alanında da görünür.</span><span class="sxs-lookup"><span data-stu-id="d8030-160">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="d8030-161">Onaylayan iseniz, bildirimden **Onayla** veya **Reddet** seçeneklerini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-161">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="d8030-162">Ayrıca, isteğe bağlı bir ileti de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-162">You can also provide an optional message.</span></span>

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="d8030-163">Yaklaşan izin bilgilerini iş arkadaşlarınıza gönderme</span><span class="sxs-lookup"><span data-stu-id="d8030-163">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="d8030-164">Teams için Human Resources uygulamasını yükledikten sonra, ekiplere veya sohbetlere karşı iş arkadaşlarınıza yaklaşan izinler hakkında bilgi gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-164">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="d8030-165">Ekipte veya Teams'deki bir sohbette, sohbet penceresinin altındaki Human Resources düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-165">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Sohbet penceresinin altında Human Resources düğmesi](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="d8030-167">Paylaşmak istediğiniz izin isteğini seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-167">Select the leave request you want to share.</span></span> <span data-ttu-id="d8030-168">Bir taslak olarak izin isteğini paylaşmak istiyorsanız, önce **Taslaklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-168">If you want to share a draft leave request, select **Drafts** first.</span></span>

<span data-ttu-id="d8030-169">İzin talebiniz sohbette gösterilir.</span><span class="sxs-lookup"><span data-stu-id="d8030-169">Your leave request will display in the chat.</span></span>

<span data-ttu-id="d8030-170">Bir taslak talep paylaştıysanız, taslak olarak görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="d8030-170">If you shared a draft request, it will display as a draft.</span></span>

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="d8030-171">Ekip izin takviminizi görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d8030-171">View your team's leave calendar</span></span>

<span data-ttu-id="d8030-172">Astları bulunan bir yönetici iseniz, takımınızın onaylanmış ve bekleyen izinlerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-172">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="d8030-173">Teams'de Human Resources uygulamasında, **İzin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-173">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="d8030-174">**Ekip takvimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-174">Select **Team calendar**.</span></span> <span data-ttu-id="d8030-175">Takvim, doğrudan astlarınıza ait onaylı ve beklemede olan izinleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="d8030-175">The calendar displays your direct reports' approved and pending time off.</span></span>

   > [!NOTE]
   > <span data-ttu-id="d8030-176">Takım takvimini göremiyorsanız yöneticinizden takvimi etkinleştirmesini isteyin.</span><span class="sxs-lookup"><span data-stu-id="d8030-176">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="d8030-177">Daha fazla bilgi için bkz. [Yükleme ve ayarlama](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="d8030-177">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="d8030-178">Desteklenen diller</span><span class="sxs-lookup"><span data-stu-id="d8030-178">Supported languages</span></span>

<span data-ttu-id="d8030-179">Teams'deki Dynamics 365 Human Resources uygulaması aşağıdaki dilleri destekler:</span><span class="sxs-lookup"><span data-stu-id="d8030-179">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="d8030-180">Yerel Ayar Kimliği</span><span class="sxs-lookup"><span data-stu-id="d8030-180">Locale ID</span></span> | <span data-ttu-id="d8030-181">Dil</span><span class="sxs-lookup"><span data-stu-id="d8030-181">Language</span></span> |
| --- | --- |
| <span data-ttu-id="d8030-182">de-DE</span><span class="sxs-lookup"><span data-stu-id="d8030-182">de-DE</span></span> | <span data-ttu-id="d8030-183">Almanca (Almanya)</span><span class="sxs-lookup"><span data-stu-id="d8030-183">German (Germany)</span></span> |
| <span data-ttu-id="d8030-184">es-ES</span><span class="sxs-lookup"><span data-stu-id="d8030-184">es-ES</span></span> | <span data-ttu-id="d8030-185">İspanyolca (İspanya)</span><span class="sxs-lookup"><span data-stu-id="d8030-185">Spanish (Spain)</span></span> |
| <span data-ttu-id="d8030-186">es-MX</span><span class="sxs-lookup"><span data-stu-id="d8030-186">es-MX</span></span> | <span data-ttu-id="d8030-187">İspanyolca (Meksika)</span><span class="sxs-lookup"><span data-stu-id="d8030-187">Spanish (Mexico)</span></span> |
| <span data-ttu-id="d8030-188">fr-CA</span><span class="sxs-lookup"><span data-stu-id="d8030-188">fr-CA</span></span> | <span data-ttu-id="d8030-189">Fransızca (Kanada)</span><span class="sxs-lookup"><span data-stu-id="d8030-189">French (Canada)</span></span> |
| <span data-ttu-id="d8030-190">fr-FR</span><span class="sxs-lookup"><span data-stu-id="d8030-190">fr-FR</span></span> | <span data-ttu-id="d8030-191">Fransızca (Fransa)</span><span class="sxs-lookup"><span data-stu-id="d8030-191">French (France)</span></span> |
| <span data-ttu-id="d8030-192">it-IT</span><span class="sxs-lookup"><span data-stu-id="d8030-192">it-IT</span></span> | <span data-ttu-id="d8030-193">İtalyanca (İtalya)</span><span class="sxs-lookup"><span data-stu-id="d8030-193">Italian (Italy)</span></span> |
| <span data-ttu-id="d8030-194">nl-NL</span><span class="sxs-lookup"><span data-stu-id="d8030-194">nl-NL</span></span> | <span data-ttu-id="d8030-195">Felemenkçe (Hollanda)</span><span class="sxs-lookup"><span data-stu-id="d8030-195">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="d8030-196">pt-BR</span><span class="sxs-lookup"><span data-stu-id="d8030-196">pt-BR</span></span> | <span data-ttu-id="d8030-197">Portekizce (Brezilya)</span><span class="sxs-lookup"><span data-stu-id="d8030-197">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="d8030-198">tr-TR</span><span class="sxs-lookup"><span data-stu-id="d8030-198">tr-TR</span></span> | <span data-ttu-id="d8030-199">Türkçe (Türkiye)</span><span class="sxs-lookup"><span data-stu-id="d8030-199">Turkish (Turkey)</span></span> |
| <span data-ttu-id="d8030-200">zh-CN</span><span class="sxs-lookup"><span data-stu-id="d8030-200">zh-CN</span></span> | <span data-ttu-id="d8030-201">Çince (Basitleştirilmiş)</span><span class="sxs-lookup"><span data-stu-id="d8030-201">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="d8030-202">Sorun Giderme</span><span class="sxs-lookup"><span data-stu-id="d8030-202">Troubleshooting</span></span>

<span data-ttu-id="d8030-203">Dynamics 365 Human Resources Teams uygulamasında oturum açarken veya uygulamayı kullanırken sorun yaşıyorsanız, bu sorun giderme yönergelerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="d8030-203">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="d8030-204">Sorun giderme işleminden sonra hala sorun yaşıyorsanız, desteğe başvurun.</span><span class="sxs-lookup"><span data-stu-id="d8030-204">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="d8030-205">Daha fazla bilgi için [Destek alma](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="d8030-205">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="d8030-206">Teams'de Human Resource uygulaması oturumu açılamıyor</span><span class="sxs-lookup"><span data-stu-id="d8030-206">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="d8030-207">Uygulamada oturum açamazsınız, Microsoft Teams'de oturum açarken kullandığınız hesap Dynamics 365 Human Resources'taki bir personel kaydıyla ilişkilendirilmemiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="d8030-207">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d8030-208">Çalışan kaydınızın doğru bir şekilde ilişkilendirildiğinden emin olmak için sistem yöneticinize başvurun.</span><span class="sxs-lookup"><span data-stu-id="d8030-208">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="d8030-209">Çeviriler doğru görüntülenmiyor</span><span class="sxs-lookup"><span data-stu-id="d8030-209">Translations don't display correctly</span></span>

<span data-ttu-id="d8030-210">Çeviriler beklendiği gibi görüntülenmiyorsa Teams'de seçtiğiniz dilin Human Resources **Kullanıcı seçenekleri**'nde seçilen dille eşleştiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="d8030-210">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="d8030-211">Teams'de, **Ayarlar**'da **Uygulama dili**'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="d8030-211">In Teams, look at **App language** in **Settings**.</span></span>

![Teams ayarları](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="d8030-213">Human Resources'ta **Ayarlar**'ı ve ardından **Kullanıcı seçenekleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d8030-213">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="d8030-214">**Dil** alanının Teams'deki **Uygulama dili** alanıyla eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d8030-214">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Human Resources Kullanıcı seçenekleri](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="d8030-216">Hala çeviri sorunları yaşıyorsanız bize bildirin.</span><span class="sxs-lookup"><span data-stu-id="d8030-216">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="d8030-217">Bilgi için bkz. [Finance and Operations uygulamaları veya Lifecycle Services (LCS) için destek alma](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="d8030-217">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="d8030-218">Teams'deki Human Resources uygulamasındaki izin isteklerini onaylarken hata oluştu</span><span class="sxs-lookup"><span data-stu-id="d8030-218">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="d8030-219">Teams uygulamasında izin isteklerini onaylamaya çalışırken hata alırsanız, aşağıdaki sorun giderme adımlarını gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="d8030-219">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="d8030-220">Microsoft Teams'te Oturum açmak için kullandığınız hesabın Dynamics 365 Human Resources'a erişmek için kullandığınız hesapla aynı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d8030-220">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="d8030-221">İzin onayı için iş akışı ayarlarını denetleyerek istek için geçerli bir onaylayan olduğunuzu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d8030-221">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="d8030-222">İzin isteği iş akışları hakkında daha fazla bilgi için bkz. [İzin isteği iş akışı oluşturma](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="d8030-222">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="d8030-223">İzin onaylayanları, izin taleplerini onaylamak üzere Teams sohbet iletilerini almıyor</span><span class="sxs-lookup"><span data-stu-id="d8030-223">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="d8030-224">Ortam ve kullanıcı için bildirimlerin etkinleştirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="d8030-224">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="d8030-225">Daha fazla bilgi için bkz. [Teams'teki Human Resources uygulamasında bildirimleri etkinleştirme](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ve [Bireysel kullanıcılar için Teams bildirimlerini etkinleştirme](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="d8030-225">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="d8030-226">Kullanıcıların, **Sohbet** sekmesinde izin isteklerini onaylamak için kullandıkları kimlik bilgileriyle oturum açtığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="d8030-226">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="d8030-227">Doğru kimlik bilgileriyle oturum açmak için "oturumu Kapat" ve ardından "oturum aç" iletilerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d8030-227">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="d8030-228">Sorun devam ederse, sistem yöneticisi olarak İş Olayları sistem toplu işinin durumunu denetleyin.</span><span class="sxs-lookup"><span data-stu-id="d8030-228">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="d8030-229">Bekleme veya yürütme aşamasındaysa, birkaç dakika sonra yeniden denetleyin.</span><span class="sxs-lookup"><span data-stu-id="d8030-229">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="d8030-230">Durum değişmeden kalırsa, bir destek bileti oluşturun. Böylece ekibimiz sorunu gidermeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="d8030-230">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="d8030-231">Bilinen erişilebilirlik sorunları</span><span class="sxs-lookup"><span data-stu-id="d8030-231">Known accessibility issues</span></span>

<span data-ttu-id="d8030-232">Teams'te Human Resources uygulama, gelecekteki sürümlerde düzeltilirken aşağıdaki erişilebilirlik sorunlarına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="d8030-232">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="d8030-233">Çıkış</span><span class="sxs-lookup"><span data-stu-id="d8030-233">Issue</span></span> | <span data-ttu-id="d8030-234">Geçici çözüm veya açıklama</span><span class="sxs-lookup"><span data-stu-id="d8030-234">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="d8030-235">Masaüstünde %400 yakınlaştırma eylemi, bazı eylem düğmelerini görünümden gizler.</span><span class="sxs-lookup"><span data-stu-id="d8030-235">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="d8030-236">Bu yakınlaştırma düzeyini destekleyene kadar bunun yerine Büyüteç kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="d8030-236">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="d8030-237">**Zaman aşımı** sekmesinde, VoiceOver zaman kılavuzu için üstbilgiyi okurken düğme eylemini duyurur.</span><span class="sxs-lookup"><span data-stu-id="d8030-237">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="d8030-238">Kılavuz içindeki başlık ve öğeler yıla göre gruplandırılır ve bunlar daraltılabilir öğelerdir.</span><span class="sxs-lookup"><span data-stu-id="d8030-238">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="d8030-239">VoiceOver, bunu işlem yapılabilir bir madde olarak yorumlar, ancak böyle değildir.</span><span class="sxs-lookup"><span data-stu-id="d8030-239">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="d8030-240">**İzin süresi** sekmesinde, Yeni bir istekte **neden koduna** giderken fazladan bir çekme hareketi vardır.</span><span class="sxs-lookup"><span data-stu-id="d8030-240">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="d8030-241">Çekme gezintisinin alınmaya çalıştığı gizli denetim yoktur.</span><span class="sxs-lookup"><span data-stu-id="d8030-241">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="d8030-242">**İzin süresi** sekmesinde, takvim açıkken çekme yaparken yeni bir istekte en üstte veya bir istek düzenlenirken denetimin dışında sona erer.</span><span class="sxs-lookup"><span data-stu-id="d8030-242">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="d8030-243">**Bugüne git**'e ulaştığınızda , denetimin sonuna kadar, en üste geri dönmek için ters yönde çekin.</span><span class="sxs-lookup"><span data-stu-id="d8030-243">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="d8030-244">**Sohbet** sekmesinde, yardımcı aracı veya klavye gezintisini kullanırken bir tarih girdiğinizde odak en üste geri atlar.</span><span class="sxs-lookup"><span data-stu-id="d8030-244">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="d8030-245">Sekmesini yeniden girin.</span><span class="sxs-lookup"><span data-stu-id="d8030-245">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="d8030-246">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="d8030-246">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="d8030-247">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="d8030-247">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="d8030-248">Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir.</span><span class="sxs-lookup"><span data-stu-id="d8030-248">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="d8030-249">Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="d8030-249">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="d8030-250">LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-250">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="d8030-251">LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar.</span><span class="sxs-lookup"><span data-stu-id="d8030-251">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="d8030-252">Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft'un  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) servisine aktarılır.</span><span class="sxs-lookup"><span data-stu-id="d8030-252">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="d8030-253">Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="d8030-253">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="d8030-254">LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="d8030-254">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d8030-255">LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure bot çerçevesine gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="d8030-255">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="d8030-256">Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="d8030-256">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="d8030-257">Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8030-257">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="d8030-258">Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d8030-258">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="d8030-259">Microsoft Teams, Azure Event Grid ve Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d8030-259">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="d8030-260">Microsoft Teams'de Dynamics 365 Human Resources uygulamasını kullanılırken, belirli müşteri verileri kiracının Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışına akabilir.</span><span class="sxs-lookup"><span data-stu-id="d8030-260">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="d8030-261">Dynamics 365 Human Resources çalışanın izin talebini ve iş akışı görev ayrıntılarını Microsoft Azure Event Grid ve Microsoft Teams uygulamalarına iletir.</span><span class="sxs-lookup"><span data-stu-id="d8030-261">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="d8030-262">Bu veriler 24 saate kadar Microsoft Azure Event Grid uygulamasında saklanabilir ve Amerika Birleşik Devletlerinde işlenir, iletim ve bekleyen veri şifrelenir ve eğitim veya hizmet iyileştirmeleri için Microsoft veya onun alt işlemcileri tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="d8030-262">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="d8030-263">Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="d8030-263">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="d8030-264">Human Resources uygulamasında sohbet botu ile konuşurken, görüşme içeriği Azure Cosmos DB uygulamasında depolanabilir ve Microsoft Teams uygulamasına iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="d8030-264">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="d8030-265">Bu veriler, Azure Cosmos DB uygulamasında 24 saate kadar depolanabilir ve kiracınızın Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışında işlenerek, aktarım ve geri kalanında şifrelenir ve Microsoft 'un veya hizmet geliştirmeleri için bunların alt işlemcileri tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="d8030-265">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="d8030-266">Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="d8030-266">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="d8030-267">Kuruluşunuz veya kuruluşunuzdaki kullanıcılarınız için Microsoft Teams içinde Human Resources uygulamasına erişimi kısıtlamak için, bkz. [Microsoft Teams'deki uygulama izin ilkelerini yönetme](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="d8030-267">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="d8030-268">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="d8030-268">See also</span></span>

[<span data-ttu-id="d8030-269">Microsoft Teams platformunu indirme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="d8030-269">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="d8030-270">Microsoft Teams yardım merkezi</span><span class="sxs-lookup"><span data-stu-id="d8030-270">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="d8030-271">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="d8030-271">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
