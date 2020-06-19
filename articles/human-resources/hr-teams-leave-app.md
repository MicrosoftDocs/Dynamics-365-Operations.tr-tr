---
title: Teams'de izin isteklerini yönetme
description: Bu konuda Microsoft Teams uygulamasındaki Dynamics 365 Human Resources uygulamasında, nasıl izin isteneceği gösterilmektedir.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.openlocfilehash: b3daa76385518ad4c7150fa93ce33be0351bfd57
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428840"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="a2a75-103">Teams'de izin isteklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="a2a75-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a2a75-104">Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulaması, hızlı bir şekilde izin isteğinde bulunmanıza ve izin bakiyesi bilgilerinizi doğrudan Microsoft Teams platformunda görüntülemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a2a75-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="a2a75-105">Bilgi istemek için bir botla etkileşime geçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2a75-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="a2a75-106">**İzin** sekmesi, daha ayrıntılı bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2a75-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="a2a75-107">Uygulamayı yükleme</span><span class="sxs-lookup"><span data-stu-id="a2a75-107">Install the app</span></span>

<span data-ttu-id="a2a75-108">Human Resources uygulamasını Teams mağazasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2a75-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="a2a75-109">Microsoft Teams platformuna üç nokta simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teams izin uygulaması üç nokta simgesi](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="a2a75-111">Dynamics 365 Human Resources uygulamasını arayın ve ardından **Human Resources** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teams izin uygulaması HR kutucuğu](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="a2a75-113">Uygulamayı yüklemek için **Ekle** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-113">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teams izin uygulaması yükleme](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="a2a75-115">Uygulama otomatik olarak oturum açmazsa oturum açmak için **Ayarlar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teams izin uygulaması Ayarlar sekmesi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="a2a75-117">Oturum açma iletişim kutusunu görmüyorsanız açılır pencerelere izin vermek için tarayıcı ayarlarınızı kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="a2a75-118">Birden fazla Human Resources örneğine erişiminiz varsa **Ayarlar** sekmesinden, hangi ortama bağlanmak istediğinizi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2a75-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="a2a75-119">Uygulama, şu anda Sistem Yöneticisi güvenlik rolünü desteklememektedir ve bir Sistem Yöneticisi hesabıyla oturum açarsanız hata iletisi görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a2a75-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="a2a75-120">Farklı bir hesapla oturum açmak için **Ayarlar** sekmesinde **Hesap değiştir** düğmesini seçin ve ardından Sistem Yöneticisi ayrıcalıklarına sahip olmayan bir kullanıcı hesabıyla oturum açın.</span><span class="sxs-lookup"><span data-stu-id="a2a75-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="a2a75-121">Bot kullanma</span><span class="sxs-lookup"><span data-stu-id="a2a75-121">Use the bot</span></span>

<span data-ttu-id="a2a75-122">Uygulama yüklendikten sonra botun, sizin adınıza gerçekleştirebileceği eylem türlerini bildiren bir hoş geldiniz iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a2a75-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams izin uygulaması botun hoş geldiniz iletisi](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="a2a75-124">Bot ile ilk kez etkileşimde bulunurken oturum açmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="a2a75-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="a2a75-125">Oturum açma iletişim kutusunu görmüyorsanız açılır pencerelere izin vermek için tarayıcı ayarlarınızı kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="a2a75-126">Bottan şunları isteyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a2a75-126">You can ask the bot to:</span></span>

- <span data-ttu-id="a2a75-127">Kayıtlı olduğunuz her izin türü için izin bakiyesi bilgisini göstermesini.</span><span class="sxs-lookup"><span data-stu-id="a2a75-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources Teams izin uygulaması bakiyeleri gösterme](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="a2a75-129">Belirli bir izin türü hakkında ek ayrıntıların gösterilmesi.</span><span class="sxs-lookup"><span data-stu-id="a2a75-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources Teams izin uygulaması ayrıntıları gösterme](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="a2a75-131">Kendiniz için bir izin isteği başlatın.</span><span class="sxs-lookup"><span data-stu-id="a2a75-131">Start a leave request for you.</span></span>

   ![Human Resources Teams izin uygulaması izin isteği](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="a2a75-133">İzin isteğini başlattıktan sonra günleri kartın içinden ayarlayabilir veya isteğinize ek bilgi eklemek için **Ayrıntıları düzenle**'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2a75-133">After you start a leave request, you can adjust the days right within the card, or you can select **Edit details** to add additional information to your request.</span></span>

![Human Resources Teams izin uygulaması isteği düzenleme](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="a2a75-135">Bilgi girişini tamamladığınızda onay için göndermek üzere **Gönder**'e basın.</span><span class="sxs-lookup"><span data-stu-id="a2a75-135">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a2a75-136">Daha sonra geri dönmek için **Taslak olarak kaydet**'e de basabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2a75-136">You can also type **Save as draft** to come back to it later.</span></span>

![Human Resources Teams izin uygulaması istek gönderme](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="a2a75-138">Teams'de izninizi yönetme</span><span class="sxs-lookup"><span data-stu-id="a2a75-138">Manage your leave in Teams</span></span>

<span data-ttu-id="a2a75-139">**İzin** sekmesi şunları görüntülemenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="a2a75-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="a2a75-140">Kayıtlı olduğunuz her izin türü için bakiye bilgisini</span><span class="sxs-lookup"><span data-stu-id="a2a75-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="a2a75-141">Yaklaşan izin istekleri</span><span class="sxs-lookup"><span data-stu-id="a2a75-141">Upcoming leave requests</span></span>

- <span data-ttu-id="a2a75-142">İzin süresi istekleri</span><span class="sxs-lookup"><span data-stu-id="a2a75-142">Time-off requests</span></span>

- <span data-ttu-id="a2a75-143">Taslak izin istekleri</span><span class="sxs-lookup"><span data-stu-id="a2a75-143">Draft leave requests</span></span>

![Human Resources Teams izin uygulaması İzin sekmesi](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="a2a75-145">Yeni bir istek oluşturma</span><span class="sxs-lookup"><span data-stu-id="a2a75-145">Create a new request</span></span>

1. <span data-ttu-id="a2a75-146">Yeni bir izin isteği oluşturmak için **Yeni istek** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teams izin uygulaması Yeni istek](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="a2a75-148">Talep ettiğiniz izin süresi için gün veya günleri girin ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teams izin uygulaması izin ekleme](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="a2a75-150">Uygunsa, bir neden kodu girin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="a2a75-151">Ayrıca açıklama girin ve herhangi bir ek ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="a2a75-152">Bilgi girişini tamamladığınızda onay için göndermek üzere **Gönder**'e basın.</span><span class="sxs-lookup"><span data-stu-id="a2a75-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a2a75-153">Daha sonra geri dönmek için **Taslak olarak kaydet**'e de basabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2a75-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="a2a75-154">Taslak istekleri yönetme</span><span class="sxs-lookup"><span data-stu-id="a2a75-154">Manage draft requests</span></span>

1. <span data-ttu-id="a2a75-155">**Taslaklar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-155">Select the **Drafts** tab.</span></span>

   ![Human Resources Teams izin uygulaması Taslaklar sekmesi](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="a2a75-157">İsteği düzenlemek için kalemi veya isteği silmek için çöp kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="a2a75-158">Gerekli tüm değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="a2a75-158">Make any necessary changes.</span></span> <span data-ttu-id="a2a75-159">Bilgi girişini tamamladığınızda onay için göndermek üzere **Gönder**'e basın.</span><span class="sxs-lookup"><span data-stu-id="a2a75-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a2a75-160">Daha sonra geri dönmek için **Taslak olarak kaydet**'i de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2a75-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teams izin uygulaması taslağı düzenleme](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a><span data-ttu-id="a2a75-162">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="a2a75-162">Privacy notice</span></span>

<span data-ttu-id="a2a75-163">Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir.</span><span class="sxs-lookup"><span data-stu-id="a2a75-163">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="a2a75-164">Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="a2a75-164">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="a2a75-165">LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2a75-165">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="a2a75-166">LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar.</span><span class="sxs-lookup"><span data-stu-id="a2a75-166">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="a2a75-167">Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft’un  [Azure bot çerçevesine](https://azure.microsoft.com/services/bot-service/)  aktarılır.</span><span class="sxs-lookup"><span data-stu-id="a2a75-167">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="a2a75-168">Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2a75-168">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="a2a75-169">LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="a2a75-169">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a2a75-170">LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure bot çerçevesine gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="a2a75-170">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="a2a75-171">Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="a2a75-171">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="a2a75-172">Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2a75-172">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="a2a75-173">Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a2a75-173">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="a2a75-174">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="a2a75-174">See also</span></span>

[<span data-ttu-id="a2a75-175">Microsoft Teams platformunu indirme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="a2a75-175">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="a2a75-176">Microsoft Teams yardım merkezi</span><span class="sxs-lookup"><span data-stu-id="a2a75-176">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="a2a75-177">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="a2a75-177">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
