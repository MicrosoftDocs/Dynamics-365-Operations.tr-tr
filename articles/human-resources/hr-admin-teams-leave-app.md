---
title: Teams'de Human Resources uygulaması
description: Bu konu sizi Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulamasıyla tanıştırır.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388128"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="a01d0-103">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="a01d0-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a01d0-104">Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulaması, çalışanların hızlı bir şekilde izin istemelerine ve izin bakiyesi bilgilerini Microsoft Teams platformunda görüntülemelerine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a01d0-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="a01d0-105">Çalışanlar, bilgi istemek için bir botla etkileşime geçebilir.</span><span class="sxs-lookup"><span data-stu-id="a01d0-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="a01d0-106">**İzin** sekmesi, daha ayrıntılı bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a01d0-106">The **Time off** tab provides more detailed information.</span></span>

![Human Resources Teams izinler uygulaması botu](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teams izin uygulaması İzin sekmesi](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="a01d0-109">Yükleme ve ayarlama</span><span class="sxs-lookup"><span data-stu-id="a01d0-109">Install and setup</span></span>

<span data-ttu-id="a01d0-110">Human Resources uygulamasını Teams mağazasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a01d0-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="a01d0-111">Teams uygulamasını yükleme hakkında bilgi için bkz. [Teams'de izin isteklerini yönetme](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="a01d0-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="a01d0-112">Teams'de uygulama izinlerini yönetme hakkında bilgi için bkz. [Microsoft Teams platformunda uygulama izin ilkelerini yönetme](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="a01d0-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="a01d0-113">Bilinen sorunlar</span><span class="sxs-lookup"><span data-stu-id="a01d0-113">Known issues</span></span>

| <span data-ttu-id="a01d0-114">Çıkış</span><span class="sxs-lookup"><span data-stu-id="a01d0-114">Issue</span></span> | <span data-ttu-id="a01d0-115">Durum</span><span class="sxs-lookup"><span data-stu-id="a01d0-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="a01d0-116">İleriki bir tarih için izin işlenirken bakiye yanlıştır.</span><span class="sxs-lookup"><span data-stu-id="a01d0-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="a01d0-117">Tahmin, henüz mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="a01d0-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="a01d0-118">Bakiye, geçerli tarih için görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a01d0-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="a01d0-119">Var olan bir istekteki alınan izin saatlerini düşerken **Kalan bakiye** artacağına azalır.</span><span class="sxs-lookup"><span data-stu-id="a01d0-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="a01d0-120">Gelecekte, bu bilinen sorunu ele alacağız.</span><span class="sxs-lookup"><span data-stu-id="a01d0-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="a01d0-121">Görüntü yanlış, ancak gönderildikten sonra doğru miktarlara ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a01d0-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="a01d0-122">Aynı tarihler için iki **Yaklaşan izin** kartı görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a01d0-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="a01d0-123">Kartlar, ayrı gönderimleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="a01d0-123">The cards represent individual submissions.</span></span> <span data-ttu-id="a01d0-124">Geri bildirim almaya ve ayarlamalar yapmaya devam edeceğiz.</span><span class="sxs-lookup"><span data-stu-id="a01d0-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="a01d0-125">**İncelemede** isteği iptal edilemiyor.</span><span class="sxs-lookup"><span data-stu-id="a01d0-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="a01d0-126">Bu işlev şu anda desteklenmemektedir ve gelecekteki bir sürümde eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="a01d0-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="a01d0-127">Bakiye bilgileri, bugün itibarıyla hesaplanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a01d0-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="a01d0-128">Sistem şu anda İzin ve devamsızlık parametrelerinde yapılandırılmış olsa bile tahakkuk dönemi itibariyle bakiyeleri göstermemektedir.</span><span class="sxs-lookup"><span data-stu-id="a01d0-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="a01d0-129">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="a01d0-129">Privacy notice</span></span>

<span data-ttu-id="a01d0-130">Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir.</span><span class="sxs-lookup"><span data-stu-id="a01d0-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="a01d0-131">Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="a01d0-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="a01d0-132">LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a01d0-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="a01d0-133">LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar.</span><span class="sxs-lookup"><span data-stu-id="a01d0-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="a01d0-134">Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft’un  [Azure bot çerçevesine](https://azure.microsoft.com/services/bot-service/)  aktarılır.</span><span class="sxs-lookup"><span data-stu-id="a01d0-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="a01d0-135">Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a01d0-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="a01d0-136">LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="a01d0-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a01d0-137">LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure bot çerçevesine gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="a01d0-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="a01d0-138">Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="a01d0-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="a01d0-139">Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a01d0-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="a01d0-140">Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a01d0-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="a01d0-141">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="a01d0-141">See also</span></span> 

[<span data-ttu-id="a01d0-142">Microsoft Teams platformunu indirme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="a01d0-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="a01d0-143">Microsoft Teams yardım merkezi</span><span class="sxs-lookup"><span data-stu-id="a01d0-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="a01d0-144">Teams'de izin isteklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="a01d0-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

