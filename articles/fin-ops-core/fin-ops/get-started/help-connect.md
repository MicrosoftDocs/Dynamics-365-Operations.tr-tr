---
title: Finance and Operations uygulamaları için Yardım deneyimini yapılandırma
description: Bu konuda, bazı Microsoft Dynamics 365 uygulamalarının Yardım sisteminin bileşenleri hakkında bilgi verilmektedir. Ayrıca, bu uygulamaların nasıl bağlanacağını açıklar ve özel Yardım oluşturma sürecinin bir özetini sağlar.
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d000c3f801d382921a027c8ee259fd44ac5cdc80
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798292"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="dd0f1-104">Finance and Operations uygulamaları için Yardım deneyimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="dd0f1-104">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd0f1-105">Bu konuda, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ve Dynamics 365 Human Resources gibi Finance and Operations uygulamaları için Yardım sisteminin bileşenlerine genel bir bakış bulacaksınız.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-105">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="dd0f1-106">Bu konu ayrıca, bu bileşenlerin nasıl bağlanacağını açıklar ve özel Yardım oluşturma sürecinin bir özetini sağlar.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-106">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="dd0f1-107">Yardım mimarisi</span><span class="sxs-lookup"><span data-stu-id="dd0f1-107">Help architecture</span></span>

<span data-ttu-id="dd0f1-108">Finance and Operations uygulamaları, [https://docs.microsoft.com/dynamics365](/dynamics365/) sitesinde yayınlanan kavramsal genel bakışları ve diğer konuları içerir.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-108">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="dd0f1-109">Bu içeriğe daha sonra ürün içi **Yardım** bölmesinden erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-109">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="dd0f1-110">Aşağıdaki örnek Yardım sisteminin bölümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-110">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="dd0f1-111">[![Yardım mimarisi](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="dd0f1-111">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="dd0f1-112">Ürün içi Yardım sistemi, docs.microsoft.com ve bağlı diğer web sitelerinden makaleler alır.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-112">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="dd0f1-113">Ayrıca Microsoft Dynamics Lifecycle Services (LCS) içindeki İş Süreci Modelleyici'de (BPM) saklanan görev kılavuzlarını da çeker.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-113">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="dd0f1-114">Görev kılavuzları ekleme</span><span class="sxs-lookup"><span data-stu-id="dd0f1-114">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="dd0f1-115">**Görev kılavuzları** sekmesi şu anda Human Resources veya Commerce'te mevcut değildir.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-115">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="dd0f1-116">Ancak, Human Resources'ın Başlarken deneyimindeki görev kılavuzları, temel işlevselliği sağlamak üzere kullanılabilir kalıyor.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-116">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="dd0f1-117">Hem Human Resources hem de Commerce için [https://docs.microsoft.com/dynamics365](/dynamics365/) sitesinde yordamsal Yardım mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-117">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="dd0f1-118">**Sistem parametreleri** sayfasında sistem yöneticileri, bir uygulama için ilgili görev kılavuzu kitaplıklarına erişimi yapılandırabilir.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-118">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="dd0f1-119">Yardım'ı yapılandırmak için uygulamanın dağıtıldığı kiracıyla aynı kiracıda bir hesap kullanarak oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-119">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="dd0f1-120">LCS kitaplığına, uygulamanın yerel bir sanal sabit sürücüde (VHD) çalışan bir örneğinden bağlanılamaz.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-120">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="dd0f1-121">[![Yardım ayarlarıyla Sistem Parametreleri formu](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="dd0f1-121">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="dd0f1-122">Çözüm için görev kılavuzlarını yapılandırmak üzere **Sistem parametreleri** sayfasındaki şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-122">To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd0f1-123">**Yardım** sekmesini ilk kez açtığınızda Lifecycle Services'e bağlanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-123">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="dd0f1-124">Formun ortasındaki bağlantıyı seçtiğinizden emin olun, bağlantı için bekleyin, iletişim kutusunu kapatın ve **Sistem parametreleri** sayfasına ulaşmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-124">Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="dd0f1-125">[![LCS'ye bağlan](./media/connect-to-lcs-crop-1024x365.png "LCS'ye bağlan")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="dd0f1-125">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="dd0f1-126">Bağlanmak için Lifecycle Hizmetleri projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-126">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="dd0f1-127">Görev kayıtlarını almak için BPM kitaplıkları (Seçili proje içinde) seçin.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-127">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="dd0f1-128">BPM kitaplıklarının görüntülenme sırasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-128">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="dd0f1-129">Görüntüleme sırası, kitaplıklardaki görev kayıtlarının **Yardım** bölmesinde hangi sırayla görüneceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-129">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="dd0f1-130">Bu adımları tamamladıktan sonra **Yardım** bölmesini açabilir ve **Görev kılavuzları**'nı seçebilirsiniz. Artık, Finance and Operations uygulamalarında bulunduğunuz sayfa için geçerli olan görev kılavuzlarını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-130">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="dd0f1-131">Görev kılavuzu bulunamadıysa, anahtar sözcükler girerek aramanızı daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-131">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="dd0f1-132">Çevrilmiş görev kılavuzları gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="dd0f1-132">Showing translated task guides</span></span>

<span data-ttu-id="dd0f1-133">Çevrilmiş görev kılavuzları ilk olarak Mayıs 2016 APQC Birleştirilmiş Kitaplığı'nda ve Başlangıç Kitaplığı'nda yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-133">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="dd0f1-134">Yerelleştirilmiş görev kılavuzu Yardım öğesini görüntülemek için Dynamics 365 çözümünüzün Mayıs 2016 kitaplığına bağlı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-134">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="dd0f1-135">Kullanıcılar, **Seçenekler** &gt; **Tercihler** altındaki dil ayarlarını değiştirerek görev kılavuzunun görüntülendiği dili değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-135">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="dd0f1-136">Birçok görev kılavuzu çevrilmiş olmasına rağmen istemci, şu anda çevrilmiş görev kılavuzu adlarını göstermez.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-136">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="dd0f1-137">Ayrıca Mayıs 2016 kitaplığındaki çeviriler yalnızca Şubat 2016'da yayımlanan görev kılavuzları için mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-137">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="dd0f1-138">Microsoft, ek çeviriler içeren güncelleştirilmiş bir kitaplık yayımlayacak.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-138">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="dd0f1-139">Görev kılavuzu çevrildiyse, görev kılavuzunu açtığınızda, görev kılavuzundaki tüm metin seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-139">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="dd0f1-140">Görev kılavuzu çevrilmediyse, açtığınızda, yalnızca bazı metinler (kontrollerin metinleri) seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-140">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="dd0f1-141">Özel Yardım ekleme</span><span class="sxs-lookup"><span data-stu-id="dd0f1-141">Adding custom Help</span></span>

<span data-ttu-id="dd0f1-142">Özel Yardım oluşturmak için görev kılavuzlarını kullanabilir veya **Yardım** bölmesine, özel bir Yardım web sitesi bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-142">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="dd0f1-143">Görev kılavuzları kullanarak özel Yardım oluşturma</span><span class="sxs-lookup"><span data-stu-id="dd0f1-143">Create custom Help by using task guides</span></span>

<span data-ttu-id="dd0f1-144">Uygulamanızı yansıtan görev kayıtları oluşturarak ve ardından bunları LCS'deki bir İş süreci kitaplığına kaydederek desteklenen uygulamalar için özel Yardım oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-144">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="dd0f1-145">Human Resources için özel görev kılavuzları oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-145">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="dd0f1-146">Bir ortaksanız ve bir kitaplığı şirket kitaplığına yükseltirseniz ve bir çözüme eklerseniz müşterileriniz tarafından kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-146">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="dd0f1-147">Ayrıca APQC Birleştirilmiş Kitaplığı'nın bir kopyasını oluşturabilir ve ardından kopyadaki görev kayıtlarını açabilir, düzenleyebilir ve değişikliklerinizi kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-147">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="dd0f1-148">Daha fazla bilgi için bkz. [Görev kaydedici kaynakları](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="dd0f1-148">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="dd0f1-149">Özel bir Yardım sitesini bağlama</span><span class="sxs-lookup"><span data-stu-id="dd0f1-149">Connect a custom Help site</span></span>

<span data-ttu-id="dd0f1-150">Finance and Operations uygulamaları, nadiren kullanıma hazır biçimlerinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-150">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="dd0f1-151">Bunun yerine çözüm, kuruluşun ihtiyaçlarına göre özelleştirilir ve genişletilir.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-151">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="dd0f1-152">Yardım deneyimini de özelleştirebilir ve genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-152">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="dd0f1-153">Örneğin, ürün içi **Yardım** bölmesine özel Yardım ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-153">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="dd0f1-154">Microsoft, özel Yardım'ı **Yardım** bölmesine dağıtmanıza ve bağlamanıza yardımcı olacak bir araç seti sağlamıştır.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-154">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="dd0f1-155">**Yardım** bölmesine bağlı özel bir Yardım çözümünü nasıl ayarlayabileceğiniz hakkında bilgi için bkz. [Özel Yardım'a genel bakış](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dd0f1-155">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="dd0f1-156">Yardım'ı özelleştirmek için araçlar ve işlemler konusunda Microsoft ile işbirliği yapmak istiyorsanız [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback) adresindeki formu doldurun.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-156">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="dd0f1-157">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="dd0f1-157">See also</span></span>

[<span data-ttu-id="dd0f1-158">Yardım sistemi</span><span class="sxs-lookup"><span data-stu-id="dd0f1-158">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="dd0f1-159">Özel Yardım'a genel bakış</span><span class="sxs-lookup"><span data-stu-id="dd0f1-159">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="dd0f1-160">Görev kaydedici kaynakları</span><span class="sxs-lookup"><span data-stu-id="dd0f1-160">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="dd0f1-161">Görev Kaydedici ile belge veya eğitim oluşturma</span><span class="sxs-lookup"><span data-stu-id="dd0f1-161">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="dd0f1-162">Özel Yardım, GitHub havuzu</span><span class="sxs-lookup"><span data-stu-id="dd0f1-162">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  
