---
title: Finance and Operations uygulamaları için Yardım deneyimini yapılandırma
description: Bu konuda, bazı Microsoft Dynamics 365 uygulamalarının Yardım sisteminin bileşenleri hakkında bilgi verilmektedir.
author: margoc
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 82bb9a09e6d302b0d453ceb5131da039769b58fb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745701"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="1d301-103">Finance and Operations uygulamaları için Yardım deneyimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1d301-103">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d301-104">Bu konuda, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ve Dynamics 365 Human Resources gibi Finance and Operations uygulamaları için Yardım sisteminin bileşenlerine genel bir bakış bulacaksınız.</span><span class="sxs-lookup"><span data-stu-id="1d301-104">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="1d301-105">Bu konu ayrıca, bu bileşenlerin nasıl bağlanacağını açıklar ve özel Yardım oluşturma sürecinin bir özetini sağlar.</span><span class="sxs-lookup"><span data-stu-id="1d301-105">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="1d301-106">Yardım mimarisi</span><span class="sxs-lookup"><span data-stu-id="1d301-106">Help architecture</span></span>

<span data-ttu-id="1d301-107">Finance and Operations uygulamaları, [https://docs.microsoft.com/dynamics365](/dynamics365/) sitesinde yayınlanan kavramsal genel bakışları ve diğer konuları içerir.</span><span class="sxs-lookup"><span data-stu-id="1d301-107">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="1d301-108">Bu içeriğe daha sonra ürün içi **Yardım** bölmesinden erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="1d301-108">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="1d301-109">Aşağıdaki örnek Yardım sisteminin bölümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d301-109">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="1d301-110">[![Yardım mimarisi](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="1d301-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="1d301-111">Ürün içi Yardım sistemi, docs.microsoft.com ve bağlı diğer web sitelerinden makaleler alır.</span><span class="sxs-lookup"><span data-stu-id="1d301-111">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="1d301-112">Ayrıca Microsoft Dynamics Lifecycle Services (LCS) içindeki İş Süreci Modelleyici'de (BPM) saklanan görev kılavuzlarını da çeker.</span><span class="sxs-lookup"><span data-stu-id="1d301-112">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="1d301-113">Görev kılavuzları ekleme</span><span class="sxs-lookup"><span data-stu-id="1d301-113">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="1d301-114">**Görev kılavuzları** sekmesi şu anda Human Resources veya Commerce'te mevcut değildir.</span><span class="sxs-lookup"><span data-stu-id="1d301-114">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="1d301-115">Ancak, Human Resources'ın Başlarken deneyimindeki görev kılavuzları, temel işlevselliği sağlamak üzere kullanılabilir kalıyor.</span><span class="sxs-lookup"><span data-stu-id="1d301-115">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="1d301-116">Hem Human Resources hem de Commerce için [https://docs.microsoft.com/dynamics365](/dynamics365/) sitesinde yordamsal Yardım mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="1d301-116">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="1d301-117">**Sistem parametreleri** sayfasında sistem yöneticileri, bir uygulama için ilgili görev kılavuzu kitaplıklarına erişimi yapılandırabilir.</span><span class="sxs-lookup"><span data-stu-id="1d301-117">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="1d301-118">Yardım'ı yapılandırmak için uygulamanın dağıtıldığı kiracıyla aynı kiracıda bir hesap kullanarak oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d301-118">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="1d301-119">LCS kitaplığına, uygulamanın yerel bir sanal sabit sürücüde (VHD) çalışan bir örneğinden bağlanılamaz.</span><span class="sxs-lookup"><span data-stu-id="1d301-119">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="1d301-120">[![Yardım ayarlarıyla Sistem Parametreleri formu](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="1d301-120">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="1d301-121&quot;>Çözüm için görev kılavuzlarını yapılandırmak üzere **Sistem parametreleri** sayfasındaki şu adımları izleyin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1d301-121&quot;>To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id=&quot;1d301-122&quot;>**Yardım** sekmesini ilk kez açtığınızda Lifecycle Services'e bağlanmanız gerekir.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1d301-122&quot;>The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id=&quot;1d301-123&quot;>Formun ortasındaki bağlantıyı seçtiğinizden emin olun, bağlantı için bekleyin, iletişim kutusunu kapatın ve **Sistem parametreleri** sayfasına ulaşmak için **Tamam**'ı seçin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1d301-123&quot;>Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id=&quot;1d301-124&quot;>[![LCS'ye bağlan](./media/connect-to-lcs-crop-1024x365.png &quot;LCS'ye bağlan")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="1d301-124">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="1d301-125">Bağlanmak için Lifecycle Hizmetleri projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1d301-125">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="1d301-126">Görev kayıtlarını almak için BPM kitaplıkları (Seçili proje içinde) seçin.</span><span class="sxs-lookup"><span data-stu-id="1d301-126">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="1d301-127">BPM kitaplıklarının görüntülenme sırasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1d301-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="1d301-128">Görüntüleme sırası, kitaplıklardaki görev kayıtlarının **Yardım** bölmesinde hangi sırayla görüneceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="1d301-128">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="1d301-129">Bu adımları tamamladıktan sonra **Yardım** bölmesini açabilir ve **Görev kılavuzları**'nı seçebilirsiniz. Artık, Finance and Operations uygulamalarında bulunduğunuz sayfa için geçerli olan görev kılavuzlarını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="1d301-129">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="1d301-130">Görev kılavuzu bulunamadıysa, anahtar sözcükler girerek aramanızı daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d301-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="1d301-131">Çevrilmiş görev kılavuzları gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="1d301-131">Showing translated task guides</span></span>

<span data-ttu-id="1d301-132">Çevrilmiş görev kılavuzları ilk olarak Mayıs 2016 APQC Birleştirilmiş Kitaplığı'nda ve Başlangıç Kitaplığı'nda yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="1d301-132">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="1d301-133">Yerelleştirilmiş görev kılavuzu Yardım öğesini görüntülemek için Dynamics 365 çözümünüzün Mayıs 2016 kitaplığına bağlı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="1d301-133">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="1d301-134">Kullanıcılar, **Seçenekler** &gt; **Tercihler** altındaki dil ayarlarını değiştirerek görev kılavuzunun görüntülendiği dili değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="1d301-134">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="1d301-135">Birçok görev kılavuzu çevrilmiş olmasına rağmen istemci, şu anda çevrilmiş görev kılavuzu adlarını göstermez.</span><span class="sxs-lookup"><span data-stu-id="1d301-135">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="1d301-136">Ayrıca Mayıs 2016 kitaplığındaki çeviriler yalnızca Şubat 2016'da yayımlanan görev kılavuzları için mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="1d301-136">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="1d301-137">Microsoft, ek çeviriler içeren güncelleştirilmiş bir kitaplık yayımlayacak.</span><span class="sxs-lookup"><span data-stu-id="1d301-137">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="1d301-138">Görev kılavuzu çevrildiyse, görev kılavuzunu açtığınızda, görev kılavuzundaki tüm metin seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="1d301-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="1d301-139">Görev kılavuzu çevrilmediyse, açtığınızda, yalnızca bazı metinler (kontrollerin metinleri) seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="1d301-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="1d301-140">Özel Yardım ekleme</span><span class="sxs-lookup"><span data-stu-id="1d301-140">Adding custom Help</span></span>

<span data-ttu-id="1d301-141">Özel Yardım oluşturmak için görev kılavuzlarını kullanabilir veya **Yardım** bölmesine, özel bir Yardım web sitesi bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d301-141">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="1d301-142">Görev kılavuzları kullanarak özel Yardım oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d301-142">Create custom Help by using task guides</span></span>

<span data-ttu-id="1d301-143">Uygulamanızı yansıtan görev kayıtları oluşturarak ve ardından bunları LCS'deki bir İş süreci kitaplığına kaydederek desteklenen uygulamalar için özel Yardım oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d301-143">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="1d301-144">Human Resources için özel görev kılavuzları oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="1d301-144">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="1d301-145">Bir ortaksanız ve bir kitaplığı şirket kitaplığına yükseltirseniz ve bir çözüme eklerseniz müşterileriniz tarafından kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1d301-145">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="1d301-146">Ayrıca APQC Birleştirilmiş Kitaplığı'nın bir kopyasını oluşturabilir ve ardından kopyadaki görev kayıtlarını açabilir, düzenleyebilir ve değişikliklerinizi kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d301-146">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="1d301-147">Daha fazla bilgi için bkz. [Görev kaydedici kaynakları](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="1d301-147">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="1d301-148">Özel bir Yardım sitesini bağlama</span><span class="sxs-lookup"><span data-stu-id="1d301-148">Connect a custom Help site</span></span>

<span data-ttu-id="1d301-149">Finance and Operations uygulamaları, nadiren kullanıma hazır biçimlerinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1d301-149">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="1d301-150">Bunun yerine çözüm, kuruluşun ihtiyaçlarına göre özelleştirilir ve genişletilir.</span><span class="sxs-lookup"><span data-stu-id="1d301-150">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="1d301-151">Yardım deneyimini de özelleştirebilir ve genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d301-151">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="1d301-152">Örneğin, ürün içi **Yardım** bölmesine özel Yardım ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d301-152">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="1d301-153">Microsoft, özel Yardım'ı **Yardım** bölmesine dağıtmanıza ve bağlamanıza yardımcı olacak bir araç seti sağlamıştır.</span><span class="sxs-lookup"><span data-stu-id="1d301-153">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="1d301-154">**Yardım** bölmesine bağlı özel bir Yardım çözümünü nasıl ayarlayabileceğiniz hakkında bilgi için bkz. [Özel Yardım'a genel bakış](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d301-154">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="1d301-155">Yardım'ı özelleştirmek için araçlar ve işlemler konusunda Microsoft ile işbirliği yapmak istiyorsanız [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback) adresindeki formu doldurun.</span><span class="sxs-lookup"><span data-stu-id="1d301-155">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="1d301-156">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="1d301-156">See also</span></span>

[<span data-ttu-id="1d301-157">Yardım sistemi</span><span class="sxs-lookup"><span data-stu-id="1d301-157">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="1d301-158">Özel Yardım'a genel bakış</span><span class="sxs-lookup"><span data-stu-id="1d301-158">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="1d301-159">Görev kaydedici kaynakları</span><span class="sxs-lookup"><span data-stu-id="1d301-159">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="1d301-160">Görev Kaydedici ile belge veya eğitim oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d301-160">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="1d301-161">Özel Yardım, GitHub havuzu</span><span class="sxs-lookup"><span data-stu-id="1d301-161">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]