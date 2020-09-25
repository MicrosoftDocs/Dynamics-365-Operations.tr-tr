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
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776320"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="e556f-103">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="e556f-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e556f-104">Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulaması, çalışanların hızlı bir şekilde izin istemelerine ve izin bakiyesi bilgilerini Microsoft Teams platformunda görüntülemelerine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e556f-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="e556f-105">Çalışanlar, bilgi istemek için bir botla etkileşime geçebilir.</span><span class="sxs-lookup"><span data-stu-id="e556f-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="e556f-106">**İzin** sekmesi, daha ayrıntılı bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e556f-106">The **Time off** tab provides more detailed information.</span></span>

![Human Resources Teams izinler uygulaması botu](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teams izin uygulaması İzin sekmesi](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="e556f-109">Yükleme ve ayarlama</span><span class="sxs-lookup"><span data-stu-id="e556f-109">Install and setup</span></span>

<span data-ttu-id="e556f-110">Human Resources uygulamasını Teams mağazasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e556f-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="e556f-111">Teams uygulamasını yükleme hakkında bilgi için bkz. [Teams'de izin isteklerini yönetme](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="e556f-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="e556f-112">Teams'de uygulama izinlerini yönetme hakkında bilgi için bkz. [Microsoft Teams platformunda uygulama izin ilkelerini yönetme](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="e556f-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="e556f-113">Teams'de Human Resources uygulaması için bildirimleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e556f-113">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="e556f-114">Kullanıcıların Teams uygulamasında izin talebi bildirimlerini almasını istiyorsanız, Human Resources uygulamasında bildirimleri etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="e556f-114">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="e556f-115">Yalnızca Teams'e kaydolan ve Human Resources Teams uygulamasını kullanan kullanıcılar bildirim alır.</span><span class="sxs-lookup"><span data-stu-id="e556f-115">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="e556f-116">İnsan Kaynakları, **sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e556f-116">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="e556f-117">**Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e556f-117">Select **Links**.</span></span>

3. <span data-ttu-id="e556f-118">**Kurulum** altında **Sistem parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e556f-118">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="e556f-119">**Genel** sekmesinde, **Teams uygulaması için bildirimleri etkinleştir** ayarını **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e556f-119">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Sistem parametrelerinde Teams uygulama bildirimlerini etkinleştirme](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="e556f-121">Tüm kullanıcılar için Teams bildirimlerini açmak için sorulduğunda **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e556f-121">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Tüm kullanıcılar için Teams bildirimlerini etkinleştirme](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="e556f-123">Bireysel kullanıcılar için Teams bildirimlerini açma veya kapatma</span><span class="sxs-lookup"><span data-stu-id="e556f-123">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="e556f-124">Human Resources Teams uygulaması için bildirimleri etkinleştirdikten sonra, bireysel kullanıcılar için bildirimleri açıp kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e556f-124">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="e556f-125">İnsan Kaynakları, **sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e556f-125">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="e556f-126">**Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e556f-126">Select **Links**.</span></span>

3. <span data-ttu-id="e556f-127">**Kullanıcılar** altında, **Kullanıcı seçenekleri**'ni belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e556f-127">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="e556f-128">**İş akışı** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e556f-128">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="e556f-129">Kullanıcı için bildirimleri etkinleştirmek için **Teams uygulaması için bildirimleri etkinleştir** ayarını **Evet** olarak veya kullanıcı için bildirimleri devre dışı bırakmak için **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e556f-129">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Kullanıcı seçenekleri İş Akışı sekmesinde Teams uygulaması bildirimlerini etkinleştirme](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="e556f-131">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e556f-131">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="e556f-132">Bilinen sorunlar</span><span class="sxs-lookup"><span data-stu-id="e556f-132">Known issues</span></span>

| <span data-ttu-id="e556f-133">Çıkış</span><span class="sxs-lookup"><span data-stu-id="e556f-133">Issue</span></span> | <span data-ttu-id="e556f-134">Durum</span><span class="sxs-lookup"><span data-stu-id="e556f-134">Status</span></span> |
| --- | --- |
| <span data-ttu-id="e556f-135">Yatay kaydırma, Android telefonlarda çalışmaz</span><span class="sxs-lookup"><span data-stu-id="e556f-135">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="e556f-136">Yatay kaydırma iOS veya masaüstü cihazlarda sorun yaratmaz.</span><span class="sxs-lookup"><span data-stu-id="e556f-136">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="e556f-137">Android için bir düzeltme üzerinde çalışıyoruz.</span><span class="sxs-lookup"><span data-stu-id="e556f-137">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="e556f-138">Hata: Bağlanılacak ortam bulunurken bir sorun oluştu.</span><span class="sxs-lookup"><span data-stu-id="e556f-138">Error: There is an issue finding an environment to connect to.</span></span> | <span data-ttu-id="e556f-139">Kullanıcının bir veya daha fazla İnsan Kaynakları ortamına erişebileceğini doğrulasanız bile bu hatayı alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e556f-139">You might receive this error even if you've verified that the user can access one or more Human Resources environments.</span></span> <span data-ttu-id="e556f-140">Ayrıca, beklediğiniz tüm ortamları görmeyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e556f-140">Also, you might not see all the environments you expect.</span></span> <span data-ttu-id="e556f-141">Bu sorunu düzeltdik, sorunu gidermek için kullanıcıyı silin ve yeniden içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="e556f-141">Until we fix this issue, delete the user and then import them in again to resolve the problem.</span></span> |
| <span data-ttu-id="e556f-142">İleriki bir tarih için izin işlenirken bakiye yanlıştır.</span><span class="sxs-lookup"><span data-stu-id="e556f-142">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="e556f-143">Tahmin, henüz mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="e556f-143">Forecasting isn't yet available.</span></span> <span data-ttu-id="e556f-144">Bakiye, geçerli tarih için görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e556f-144">The balance displays for the current date.</span></span> |
| <span data-ttu-id="e556f-145">**İncelemede** isteği iptal edilemiyor.</span><span class="sxs-lookup"><span data-stu-id="e556f-145">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="e556f-146">Bu işlev şu anda desteklenmemektedir ve gelecekteki bir sürümde eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="e556f-146">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="e556f-147">Bakiye bilgileri, bugün itibarıyla hesaplanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e556f-147">Balance information is calculated as of today.</span></span> | <span data-ttu-id="e556f-148">Sistem şu anda İzin ve devamsızlık parametrelerinde yapılandırılmış olsa bile tahakkuk dönemi itibariyle bakiyeleri göstermemektedir.</span><span class="sxs-lookup"><span data-stu-id="e556f-148">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="e556f-149">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="e556f-149">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="e556f-150">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="e556f-150">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="e556f-151">Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir.</span><span class="sxs-lookup"><span data-stu-id="e556f-151">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="e556f-152">Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="e556f-152">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="e556f-153">LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e556f-153">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="e556f-154">LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar.</span><span class="sxs-lookup"><span data-stu-id="e556f-154">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="e556f-155">Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft'un  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) servisine aktarılır.</span><span class="sxs-lookup"><span data-stu-id="e556f-155">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="e556f-156">Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e556f-156">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="e556f-157">LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="e556f-157">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e556f-158">LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure bot çerçevesine gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="e556f-158">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="e556f-159">Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="e556f-159">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="e556f-160">Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e556f-160">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="e556f-161">Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e556f-161">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="e556f-162">Microsoft Azure Event Grid ve Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="e556f-162">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="e556f-163">Teams'de Dynamics 365 Human Resources uygulaması için bildirimler özelliği kullanılırken, belirli müşteri verileri kiracının Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışına akacaktır.</span><span class="sxs-lookup"><span data-stu-id="e556f-163">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="e556f-164">Dynamics 365 Human Resources çalışanın izin talebini ve iş akışı görev ayrıntılarını Microsoft Azure Event Grid ve Microsoft Teams uygulamalarına iletir.</span><span class="sxs-lookup"><span data-stu-id="e556f-164">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="e556f-165">Bu veriler 24 saate kadar saklanabilir ve Amerika Birleşik Devletlerinde işlenir, iletim ve bekleyen veri şifrelenir ve eğitim veya hizmet iyileştirmeleri için Microsoft veya onun alt işlemcileri tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="e556f-165">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="e556f-166">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="e556f-166">See also</span></span> 

[<span data-ttu-id="e556f-167">Microsoft Teams platformunu indirme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="e556f-167">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="e556f-168">Microsoft Teams yardım merkezi</span><span class="sxs-lookup"><span data-stu-id="e556f-168">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="e556f-169">Teams'de izin isteklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="e556f-169">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

