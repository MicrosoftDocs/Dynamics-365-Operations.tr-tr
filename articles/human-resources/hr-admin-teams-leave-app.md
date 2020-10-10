---
title: Teams'de Human Resources uygulaması
description: Bu konu sizi Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulamasıyla tanıştırır.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828926"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="f9ba6-103">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="f9ba6-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f9ba6-104">Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulaması, çalışanların hızlı bir şekilde izin istemelerine ve izin bakiyesi bilgilerini Microsoft Teams platformunda görüntülemelerine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="f9ba6-105">Çalışanlar, bilgi istemek için bir botla etkileşime geçebilir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="f9ba6-106">**İzin** sekmesi daha ayrıntılı bilgi sağlar. Ayrıca kişilere ekiplerindeki yaklaşan izinler hakkında bilgi, Human Resources uygulaması dışında sohbetler gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-106">The **Time off** tab provides more detailed information.In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teams izinler uygulaması botu](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teams izin uygulaması İzin sekmesi](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources izin istek kartı](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="f9ba6-110">Yükleme ve ayarlama</span><span class="sxs-lookup"><span data-stu-id="f9ba6-110">Install and setup</span></span>

<span data-ttu-id="f9ba6-111">Human Resources uygulamasını Teams mağazasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-111">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="f9ba6-112">Teams uygulamasını yükleme hakkında bilgi için bkz. [Teams'de izin isteklerini yönetme](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="f9ba6-112">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="f9ba6-113">Teams'de uygulama izinlerini yönetme hakkında bilgi için bkz. [Microsoft Teams platformunda uygulama izin ilkelerini yönetme](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="f9ba6-113">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="f9ba6-114">Teams'de Human Resources uygulaması için bildirimleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f9ba6-114">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="f9ba6-115">Kullanıcıların Teams uygulamasında izin talebi bildirimlerini almasını istiyorsanız, Human Resources uygulamasında bildirimleri etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-115">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="f9ba6-116">Yalnızca Teams'e kaydolan ve Human Resources Teams uygulamasını kullanan kullanıcılar bildirim alır.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-116">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="f9ba6-117">İnsan Kaynakları, **sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-117">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="f9ba6-118">**Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-118">Select **Links**.</span></span>

3. <span data-ttu-id="f9ba6-119">**Kurulum** altında **Sistem parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-119">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="f9ba6-120">**Genel** sekmesinde, **Teams uygulaması için bildirimleri etkinleştir** ayarını **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-120">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Sistem parametrelerinde Teams uygulama bildirimlerini etkinleştirme](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="f9ba6-122">Tüm kullanıcılar için Teams bildirimlerini açmak için sorulduğunda **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-122">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Tüm kullanıcılar için Teams bildirimlerini etkinleştirme](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="f9ba6-124">Bireysel kullanıcılar için Teams bildirimlerini açma veya kapatma</span><span class="sxs-lookup"><span data-stu-id="f9ba6-124">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="f9ba6-125">Human Resources Teams uygulaması için bildirimleri etkinleştirdikten sonra, bireysel kullanıcılar için bildirimleri açıp kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-125">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="f9ba6-126">İnsan Kaynakları, **sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="f9ba6-127">**Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-127">Select **Links**.</span></span>

3. <span data-ttu-id="f9ba6-128">**Kullanıcılar** altında, **Kullanıcı seçenekleri**'ni belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-128">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="f9ba6-129">**İş akışı** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-129">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="f9ba6-130">Kullanıcı için bildirimleri etkinleştirmek için **Teams uygulaması için bildirimleri etkinleştir** ayarını **Evet** olarak veya kullanıcı için bildirimleri devre dışı bırakmak için **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-130">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Kullanıcı seçenekleri İş Akışı sekmesinde Teams uygulaması bildirimlerini etkinleştirme](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="f9ba6-132">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-132">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="f9ba6-133">Bilinen sorunlar</span><span class="sxs-lookup"><span data-stu-id="f9ba6-133">Known issues</span></span>

| <span data-ttu-id="f9ba6-134">Çıkış</span><span class="sxs-lookup"><span data-stu-id="f9ba6-134">Issue</span></span> | <span data-ttu-id="f9ba6-135">Durum</span><span class="sxs-lookup"><span data-stu-id="f9ba6-135">Status</span></span> |
| --- | --- |
| <span data-ttu-id="f9ba6-136">Yatay kaydırma, Android telefonlarda çalışmaz</span><span class="sxs-lookup"><span data-stu-id="f9ba6-136">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="f9ba6-137">Yatay kaydırma iOS veya masaüstü cihazlarda sorun yaratmaz.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-137">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="f9ba6-138">Android için bir düzeltme üzerinde çalışıyoruz.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-138">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="f9ba6-139">İleriki bir tarih için izin işlenirken bakiye yanlıştır.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-139">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="f9ba6-140">Tahmin, henüz mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-140">Forecasting isn't yet available.</span></span> <span data-ttu-id="f9ba6-141">Bakiye, geçerli tarih için görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-141">The balance displays for the current date.</span></span> |
| <span data-ttu-id="f9ba6-142">**İncelemede** isteği iptal edilemiyor.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-142">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="f9ba6-143">Bu işlev şu anda desteklenmemektedir ve gelecekteki bir sürümde eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-143">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="f9ba6-144">Bakiye bilgileri, bugün itibarıyla hesaplanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-144">Balance information is calculated as of today.</span></span> | <span data-ttu-id="f9ba6-145">Sistem şu anda İzin ve devamsızlık parametrelerinde yapılandırılmış olsa bile tahakkuk dönemi itibariyle bakiyeleri göstermemektedir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-145">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="f9ba6-146">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="f9ba6-146">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="f9ba6-147">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="f9ba6-147">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="f9ba6-148">Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-148">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="f9ba6-149">Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-149">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="f9ba6-150">LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-150">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="f9ba6-151">LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-151">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="f9ba6-152">Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft'un  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) servisine aktarılır.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-152">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="f9ba6-153">Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-153">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="f9ba6-154">LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-154">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f9ba6-155">LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure bot çerçevesine gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-155">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="f9ba6-156">Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-156">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="f9ba6-157">Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-157">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="f9ba6-158">Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-158">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="f9ba6-159">Microsoft Teams, Azure Event Grid ve Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f9ba6-159">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="f9ba6-160">Microsoft Teams'de Dynamics 365 Human Resources uygulamasını kullanılırken, belirli müşteri verileri kiracının Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışına akabilir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-160">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="f9ba6-161">Dynamics 365 Human Resources çalışanın izin talebini ve iş akışı görev ayrıntılarını Microsoft Azure Event Grid ve Microsoft Teams uygulamalarına iletir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-161">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="f9ba6-162">Bu veriler 24 saate kadar Microsoft Azure Event Grid uygulamasında saklanabilir ve Amerika Birleşik Devletlerinde işlenir, iletim ve bekleyen veri şifrelenir ve eğitim veya hizmet iyileştirmeleri için Microsoft veya onun alt işlemcileri tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-162">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="f9ba6-163">Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="f9ba6-163">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="f9ba6-164">Human Resources uygulamasında sohbet botu ile konuşurken, görüşme içeriği Azure Cosmos DB uygulamasında depolanabilir ve Microsoft Teams uygulamasına iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-164">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="f9ba6-165">Bu veriler, Azure Cosmos DB uygulamasında 24 saate kadar depolanabilir ve kiracınızın Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışında işlenerek, aktarım ve geri kalanında şifrelenir ve Microsoft 'un veya hizmet geliştirmeleri için bunların alt işlemcileri tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-165">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="f9ba6-166">Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="f9ba6-166">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="f9ba6-167">Kuruluşunuz veya kuruluşunuzdaki kullanıcılarınız için Microsoft Teams içinde Human Resources uygulamasına erişimi kısıtlamak için, bkz. [Microsoft Teams'deki uygulama izin ilkelerini yönetme](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="f9ba6-167">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="f9ba6-168">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="f9ba6-168">See also</span></span> 

[<span data-ttu-id="f9ba6-169">Microsoft Teams platformunu indirme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="f9ba6-169">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="f9ba6-170">Microsoft Teams yardım merkezi</span><span class="sxs-lookup"><span data-stu-id="f9ba6-170">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="f9ba6-171">Teams'de izin isteklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="f9ba6-171">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

