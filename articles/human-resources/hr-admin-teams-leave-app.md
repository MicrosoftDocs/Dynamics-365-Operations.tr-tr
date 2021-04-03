---
title: Teams'de Human Resources uygulaması
description: Bu konu sizi Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulamasıyla tanıştırır.
author: andreabichsel
manager: tfehr
ms.date: 02/23/2021
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
ms.openlocfilehash: 86abe32f76f2cc21c773727be07a44be49cdbac7
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487885"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="608da-103">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="608da-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="608da-104">Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulaması, çalışanların hızlı bir şekilde izin istemelerine ve izin bakiyesi bilgilerini Microsoft Teams platformunda görüntülemelerine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="608da-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="608da-105">Çalışanlar, bilgi istemek için bir botla etkileşime geçebilir.</span><span class="sxs-lookup"><span data-stu-id="608da-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="608da-106">**İzin** sekmesi, daha ayrıntılı bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="608da-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="608da-107">Ek olarak, ekipte yaklaşan izinler hakkında kişilere bilgi ve Human Resources uygulamasının dışındaki sohbetleri gönderebilirler.</span><span class="sxs-lookup"><span data-stu-id="608da-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teams izinler uygulaması botu](./media/hr-teams-leave-app-bot.png)

![Human Resources Teams izin uygulaması İzin sekmesi](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources izin istek kartı](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="608da-111">Yükleme ve ayarlama</span><span class="sxs-lookup"><span data-stu-id="608da-111">Install and setup</span></span>

<span data-ttu-id="608da-112">Dynamics 365 Human Resources uygulamasını Teams mağazasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="608da-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="608da-113">Teams uygulamasını yükleme hakkında bilgi için bkz. [Teams'de izin isteklerini yönetme](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="608da-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="608da-114">Teams'de uygulama izinlerini yönetme hakkında bilgi için bkz. [Microsoft Teams platformunda uygulama izin ilkelerini yönetme](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="608da-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="608da-115">Kullanıcılarınızın uygulamadaki İzin ve devamsızlık takvimini görüntülemesini istiyorsanız Özellik yönetimindeki **Teams'de İzin ve devamsızlık takvimi** özelliğini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="608da-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="608da-116">Özellikleri etkinleştirme hakkında daha fazla bilgi edinmek için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="608da-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="608da-117">Teams'de Human Resources uygulaması için bildirimleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="608da-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="608da-118">Kullanıcıların Teams uygulamasında izin talebi bildirimlerini almasını istiyorsanız Dynamics 365 Human Resources uygulamasında bildirimleri etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="608da-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="608da-119">Yalnızca Teams'e kaydolan ve Dynamics 365 Human Resources Teams uygulamasını kullanan kullanıcılar bildirim alır.</span><span class="sxs-lookup"><span data-stu-id="608da-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="608da-120">İnsan Kaynakları, **sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="608da-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="608da-121">**Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="608da-121">Select **Links**.</span></span>

3. <span data-ttu-id="608da-122">**Kurulum** altında **Sistem parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="608da-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="608da-123">**Genel** sekmesinde, **Teams uygulaması için bildirimleri etkinleştir** ayarını **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="608da-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Sistem parametrelerinde Teams uygulama bildirimlerini etkinleştirme](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="608da-125">Tüm kullanıcılar için Teams bildirimlerini açmak için sorulduğunda **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="608da-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Tüm kullanıcılar için Teams bildirimlerini etkinleştirme](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="608da-127">Bireysel kullanıcılar için Teams bildirimlerini açma veya kapatma</span><span class="sxs-lookup"><span data-stu-id="608da-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="608da-128">Dynamics 365 Human Resources Teams uygulaması için bildirimleri etkinleştirdikten sonra, bireysel kullanıcılar için bildirimleri açıp kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="608da-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="608da-129">İnsan Kaynakları, **sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="608da-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="608da-130">**Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="608da-130">Select **Links**.</span></span>

3. <span data-ttu-id="608da-131">**Kullanıcılar** altında, **Kullanıcı seçenekleri**'ni belirleyin.</span><span class="sxs-lookup"><span data-stu-id="608da-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="608da-132">**İş akışı** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="608da-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="608da-133">Kullanıcı için bildirimleri etkinleştirmek için **Teams uygulaması için bildirimleri etkinleştir** ayarını **Evet** olarak veya kullanıcı için bildirimleri devre dışı bırakmak için **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="608da-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Kullanıcı seçenekleri İş Akışı sekmesinde Teams uygulaması bildirimlerini etkinleştirme](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="608da-135">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="608da-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="608da-136">Desteklenen diller</span><span class="sxs-lookup"><span data-stu-id="608da-136">Supported languages</span></span>

<span data-ttu-id="608da-137">Teams'deki Dynamics 365 Human Resources uygulaması aşağıdaki dilleri destekler:</span><span class="sxs-lookup"><span data-stu-id="608da-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="608da-138">Yerel Ayar Kimliği</span><span class="sxs-lookup"><span data-stu-id="608da-138">Locale ID</span></span> | <span data-ttu-id="608da-139">Dil</span><span class="sxs-lookup"><span data-stu-id="608da-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="608da-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="608da-140">de-DE</span></span> | <span data-ttu-id="608da-141">Almanca (Almanya)</span><span class="sxs-lookup"><span data-stu-id="608da-141">German (Germany)</span></span> |
| <span data-ttu-id="608da-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="608da-142">es-ES</span></span> | <span data-ttu-id="608da-143">İspanyolca (İspanya)</span><span class="sxs-lookup"><span data-stu-id="608da-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="608da-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="608da-144">es-MX</span></span> | <span data-ttu-id="608da-145">İspanyolca (Meksika)</span><span class="sxs-lookup"><span data-stu-id="608da-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="608da-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="608da-146">fr-CA</span></span> | <span data-ttu-id="608da-147">Fransızca (Kanada)</span><span class="sxs-lookup"><span data-stu-id="608da-147">French (Canada)</span></span> |
| <span data-ttu-id="608da-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="608da-148">fr-FR</span></span> | <span data-ttu-id="608da-149">Fransızca (Fransa)</span><span class="sxs-lookup"><span data-stu-id="608da-149">French (France)</span></span> |
| <span data-ttu-id="608da-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="608da-150">it-IT</span></span> | <span data-ttu-id="608da-151">İtalyanca (İtalya)</span><span class="sxs-lookup"><span data-stu-id="608da-151">Italian (Italy)</span></span> |
| <span data-ttu-id="608da-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="608da-152">nl-NL</span></span> | <span data-ttu-id="608da-153">Felemenkçe (Hollanda)</span><span class="sxs-lookup"><span data-stu-id="608da-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="608da-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="608da-154">pt-BR</span></span> | <span data-ttu-id="608da-155">Portekizce (Brezilya)</span><span class="sxs-lookup"><span data-stu-id="608da-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="608da-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="608da-156">tr-TR</span></span> | <span data-ttu-id="608da-157">Türkçe (Türkiye)</span><span class="sxs-lookup"><span data-stu-id="608da-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="608da-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="608da-158">zh-CN</span></span> | <span data-ttu-id="608da-159">Çince (Basitleştirilmiş)</span><span class="sxs-lookup"><span data-stu-id="608da-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="608da-160">Notlar</span><span class="sxs-lookup"><span data-stu-id="608da-160">Notes</span></span>

<span data-ttu-id="608da-161">Aşağıdaki iş öğeleri gelecekteki sürümler için planlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="608da-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="608da-162">İş maddesi</span><span class="sxs-lookup"><span data-stu-id="608da-162">Work item</span></span> | <span data-ttu-id="608da-163">Durum</span><span class="sxs-lookup"><span data-stu-id="608da-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="608da-164">İleriki bir tarih için izin işlenirken bakiye yanlıştır.</span><span class="sxs-lookup"><span data-stu-id="608da-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="608da-165">Tahmin, henüz mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="608da-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="608da-166">Bakiye, geçerli tarih için görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="608da-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="608da-167">**İncelemede** isteği iptal edilemiyor.</span><span class="sxs-lookup"><span data-stu-id="608da-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="608da-168">Bu işlev şu anda desteklenmemektedir ve gelecekteki bir sürümde eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="608da-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="608da-169">Bakiye bilgileri, bugün itibarıyla hesaplanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="608da-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="608da-170">Sistem şu anda İzin ve devamsızlık parametrelerinde yapılandırılmış olsa bile tahakkuk dönemi itibariyle bakiyeleri göstermemektedir.</span><span class="sxs-lookup"><span data-stu-id="608da-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="608da-171">Sorun Giderme</span><span class="sxs-lookup"><span data-stu-id="608da-171">Troubleshooting</span></span>

<span data-ttu-id="608da-172">Bir kullanıcı Human Resources Teams uygulamasında oturum açarken veya uygulamayı kullanırken sorun yaşarsa bu sorun giderme yönergelerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="608da-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="608da-173">Sorun giderme işleminden sonra hala sorun yaşıyorsanız, desteğe başvurun.</span><span class="sxs-lookup"><span data-stu-id="608da-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="608da-174">Daha fazla bilgi için [Destek alma](hr-admin-troubleshooting-support.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="608da-174">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="608da-175">Teams'de Human Resource uygulaması oturumu açılamıyor</span><span class="sxs-lookup"><span data-stu-id="608da-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="608da-176">Bir kullanıcı uygulamada oturum açamadığı için sizinle iletişim kurarsa kullanıcının Human Resources'ta ilişkili bir çalışan kaydı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="608da-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="608da-177">Teams'deki Human Resources uygulamasındaki izin isteklerini onaylarken hata oluştu</span><span class="sxs-lookup"><span data-stu-id="608da-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="608da-178">Kullanıcı Teams uygulamasında izin isteklerini onaylamaya çalışırken hata alırsa aşağıdaki sorun giderme adımlarını deneyin:</span><span class="sxs-lookup"><span data-stu-id="608da-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="608da-179">Teams hesabının Human Resources'a erişmek için kullanılan hesapla aynı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="608da-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="608da-180">İzin onayı için iş akışı ayarlarını denetleyerek istek için geçerli bir onaylayan olduklarını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="608da-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="608da-181">İzin isteği iş akışları hakkında daha fazla bilgi için bkz. [İzin isteği iş akışı oluşturma](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="608da-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="608da-182">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="608da-182">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="608da-183">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="608da-183">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="608da-184">Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir.</span><span class="sxs-lookup"><span data-stu-id="608da-184">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="608da-185">Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="608da-185">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="608da-186">LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="608da-186">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="608da-187">LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar.</span><span class="sxs-lookup"><span data-stu-id="608da-187">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="608da-188">Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft'un  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) servisine aktarılır.</span><span class="sxs-lookup"><span data-stu-id="608da-188">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="608da-189">Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="608da-189">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="608da-190">LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="608da-190">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="608da-191">LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure bot çerçevesine gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="608da-191">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="608da-192">Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="608da-192">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="608da-193">Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="608da-193">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="608da-194">Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="608da-194">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="608da-195">Microsoft Teams, Azure Event Grid ve Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="608da-195">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="608da-196">Microsoft Teams'de Dynamics 365 Human Resources uygulamasını kullanılırken, belirli müşteri verileri kiracının Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışına akabilir.</span><span class="sxs-lookup"><span data-stu-id="608da-196">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="608da-197">Dynamics 365 Human Resources çalışanın izin talebini ve iş akışı görev ayrıntılarını Microsoft Azure Event Grid ve Microsoft Teams uygulamalarına iletir.</span><span class="sxs-lookup"><span data-stu-id="608da-197">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="608da-198">Bu veriler 24 saate kadar Microsoft Azure Event Grid uygulamasında saklanabilir ve Amerika Birleşik Devletlerinde işlenir, iletim ve bekleyen veri şifrelenir ve eğitim veya hizmet iyileştirmeleri için Microsoft veya onun alt işlemcileri tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="608da-198">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="608da-199">Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="608da-199">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="608da-200">Human Resources uygulamasında sohbet botu ile konuşurken, görüşme içeriği Azure Cosmos DB uygulamasında depolanabilir ve Microsoft Teams uygulamasına iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="608da-200">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="608da-201">Bu veriler, Azure Cosmos DB uygulamasında 24 saate kadar depolanabilir ve kiracınızın Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışında işlenerek, aktarım ve geri kalanında şifrelenir ve Microsoft 'un veya hizmet geliştirmeleri için bunların alt işlemcileri tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="608da-201">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="608da-202">Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="608da-202">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="608da-203">Kuruluşunuz veya kuruluşunuzdaki kullanıcılarınız için Microsoft Teams içinde Human Resources uygulamasına erişimi kısıtlamak için, bkz. [Microsoft Teams'deki uygulama izin ilkelerini yönetme](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="608da-203">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="608da-204">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="608da-204">See also</span></span> 

[<span data-ttu-id="608da-205">Microsoft Teams platformunu indirme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="608da-205">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="608da-206">Microsoft Teams yardım merkezi</span><span class="sxs-lookup"><span data-stu-id="608da-206">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="608da-207">Teams'de izin isteklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="608da-207">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]