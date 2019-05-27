---
title: Yardım sistemini bağlama
description: Bu konuda Microsoft Dynamics 365 for Finance and Operations için Yardım sistemin bileşenleri açıklanmakta, bu bileşenlere nasıl bağlanacağınıza ilişkin bir genel bakış ve özel yardımın nasıl oluşturulacağının bir özeti verilmektedir.
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 673b01648127fe1d19fb3c75c4d6812c4f22c761
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561987"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="8df3b-103">Yardım sistemini bağlama</span><span class="sxs-lookup"><span data-stu-id="8df3b-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8df3b-104">Bu konu, Microsoft Dynamics 365 for Finance and Operations için Yardım sisteminin bileşenlerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="8df3b-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="8df3b-105">Bu bileşenlere nasıl bağlanılacağı ve özel yardım oluşturma hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="8df3b-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="8df3b-106">Yardım mimarisi</span><span class="sxs-lookup"><span data-stu-id="8df3b-106">Help architecture</span></span>

<span data-ttu-id="8df3b-107">Aşağıdaki çizim, Finance and Operations Yardım sisteminin bölümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8df3b-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="8df3b-108">Ürün içi Yardım sistemi, Dynamics 365 Lifecycle Services'deki (LCS) İş Süreci Modelleyici'de ve https://docs.microsoft.com adresinde bulunan görev kayıtlarıyla Finance and Operations makalelerini çeker.</span><span class="sxs-lookup"><span data-stu-id="8df3b-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="8df3b-109">Not: Diyagramda yıldız işareti (\*) ile listelenen özellikler planlanmıştır, ancak henüz kullanılabilir değildir.</span><span class="sxs-lookup"><span data-stu-id="8df3b-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="8df3b-110">[![Yardım mimarisi](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="8df3b-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="8df3b-111">Yardım sistemine bağlanma</span><span class="sxs-lookup"><span data-stu-id="8df3b-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="8df3b-112">**Görev kılavuzları** sekmesi, şu anda Microsoft Dynamics 365 for Talent ve Microsoft Dynamics 365 for Retail için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8df3b-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="8df3b-113">Bu işlevi gelecekteki bir sürümde etkinleştirmek için çalışıyoruz.</span><span class="sxs-lookup"><span data-stu-id="8df3b-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="8df3b-114">Başlarken deneyimindeki Görev kılavuzları, temel işlevselliği kapsamak üzere kullanılabilir kalır.</span><span class="sxs-lookup"><span data-stu-id="8df3b-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="8df3b-115">Yordamlama yardımı da docs.microsoft.com sitesinde, hem Retail hem Talen için kullanılabilir ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)).</span><span class="sxs-lookup"><span data-stu-id="8df3b-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>

<span data-ttu-id="8df3b-116">**Sistem Parametreleri** sayfasını kullanarak, sistem yöneticileri bir uygulama için Yardım sisteminin parçalarını bağlar.</span><span class="sxs-lookup"><span data-stu-id="8df3b-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="8df3b-117">[![Yardım ayarlarıyla Sistem Parametreleri formu](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="8df3b-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="8df3b-118">**Sistem parametreleri** sayfası üzerinde, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="8df3b-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8df3b-119">**Yardım** sekmesini ilk kez açtığınızda Lifecycle Services'e bağlanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8df3b-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="8df3b-120">Formun ortasındaki bağlantıya tıkladığınızdan emin olun, bağlantı için bekleyin, iletişim kutusunu kapatın ve **Sistem parametreleri**sayfasına ulaşmak için **Tamam** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8df3b-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="8df3b-121">[![LCS'ye bağlan](./media/connect-to-lcs-crop-1024x365.png "LCS'ye bağlan")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="8df3b-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="8df3b-122">Bağlanmak için Lifecycle Hizmetleri projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8df3b-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="8df3b-123">Görev kayıtlarını almak için BPM kitaplıkları (Seçili proje içinde) seçin.</span><span class="sxs-lookup"><span data-stu-id="8df3b-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>

    - <span data-ttu-id="8df3b-124">Finance and Operations için, Microsoft içeriği için, en yeni APQC Unified Library for Finance and Operations'u seçin.</span><span class="sxs-lookup"><span data-stu-id="8df3b-124">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span>
    - <span data-ttu-id="8df3b-125">Retail için bir kütüphaneyi yakın zamanda yayımlayacağız.</span><span class="sxs-lookup"><span data-stu-id="8df3b-125">For Retail, we will be releasing a library in the near future.</span></span>
    - <span data-ttu-id="8df3b-126">Talent için bir kütüphane seçmeniz gerekmez; doğru kütüphane ile bağlantı sizin için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8df3b-126">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span>

3. <span data-ttu-id="8df3b-127">BPM kitaplıklarının görüntülenme sırasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8df3b-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="8df3b-128">Bu **Yardım** bölmesinde kitaplıklardaki görev kayıtlarının hangi sırayla görüneceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="8df3b-128">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="8df3b-129">Bu adımları tamamladıktan sonra, **Yardım** bölmesini açabilir ve **Görev kılavuzları** sekmesine tıklayabilirsiniz. Şimdi, Finance and Operations'ta içinde bulunduğunuz sayfa için geçerli olan görev kılavuzlarını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="8df3b-129">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations.</span></span> <span data-ttu-id="8df3b-130">Görev kılavuzu bulunamadıysa, anahtar sözcükler girerek aramanızı daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8df3b-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="8df3b-131">Çevrilmiş görev kılavuzları gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="8df3b-131">Showing translated task guides</span></span>

<span data-ttu-id="8df3b-132">Çevrilmiş görev kılavuzları ilk olarak Mayıs 2016 APQC Birleştirilmiş Kitaplığı'na ve Başlangıç kitaplığına sevk edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8df3b-132">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="8df3b-133">Finance and Operations içinde yerelleştirilmiş görev kılavuzu yardımını görmek için Mayıs kitaplığına bağlı olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="8df3b-133">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="8df3b-134">Görev kılavuzunun görüntülendiği dil her kullanıcı için **Seçenekler** &gt; **Tercihler** altındaki Dil ayarlarından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="8df3b-134">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="8df3b-135">Pek çok görev kılavuzu çevrilmiş olsa da şu anda Finance and Operations istemcisi çevrilmiş görev kılavuz adlarını göstermemektedir.</span><span class="sxs-lookup"><span data-stu-id="8df3b-135">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="8df3b-136">Ayrıca, yalnızca Şubat 2016'da yayımlanan görev kılavuzları, Mayıs ayı Kitaplığı'nda çeviri olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8df3b-136">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="8df3b-137">Ek çevirilerle güncelleştirilmiş bir kitaplık yayımlayacağız.</span><span class="sxs-lookup"><span data-stu-id="8df3b-137">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="8df3b-138">Görev kılavuzu çevrildiyse, görev kılavuzunu açtığınızda, görev kılavuzundaki tüm metin seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="8df3b-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="8df3b-139">Görev kılavuzu çevrilmediyse, açtığınızda, yalnızca bazı metinler (kontrollerin metinleri) seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="8df3b-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="8df3b-140">Özel yardım oluşturma</span><span class="sxs-lookup"><span data-stu-id="8df3b-140">Creating custom help</span></span>

<span data-ttu-id="8df3b-141">Görev kılavuzlarını özel yardım oluşturmak veya bir web sitesini Yardım panosuna bağlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8df3b-141">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="8df3b-142">Görev kılavuzlarıyla özel yardım oluşturmak</span><span class="sxs-lookup"><span data-stu-id="8df3b-142">Create custom help with task guides</span></span>

<span data-ttu-id="8df3b-143">Uygulamanızı yansıtan görev kayıtları oluşturarak ve bunları bir LCS İş Süreci Kitaplığına kaydederek Finance and Operations ve Retail uygulamanız için özel yardım oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8df3b-143">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="8df3b-144">Talent için özel görev kılavuzları oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="8df3b-144">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="8df3b-145">Ortaklar için, bir kitaplığı şirket kitaplığına yükseltirseniz ve bir çözüme eklerseniz, müşterileriniz tarafından kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="8df3b-145">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="8df3b-146">Ayrıca APQC Birleştirilmiş global kitaplığın bir kopyasını oluşturabilirsiniz ve ardından kopyayı açabilir, kopyadan görev kayıtlarını açarak onları değiştirebilir ve değişiklik yaptığınız kayıtları kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8df3b-146">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="8df3b-147">Daha fazla bilgi için bkz. [Belge veya eğitim olarak kullanmak için görev kaydı oluşturma](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="8df3b-147">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="8df3b-148">Özel bir siteye bağlanmak</span><span class="sxs-lookup"><span data-stu-id="8df3b-148">Connect a custom site</span></span>

<span data-ttu-id="8df3b-149">Microsoft, özel yardım sitesini oluşturma ve bağlamak hakkında bir teknik inceleme ve örnek kodu sağlamıştır.</span><span class="sxs-lookup"><span data-stu-id="8df3b-149">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="8df3b-150">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="8df3b-150">For more information, see:</span></span>

- [<span data-ttu-id="8df3b-151">Finance and Operations için Özel Yardım Oluşturmak (teknik inceleme)</span><span class="sxs-lookup"><span data-stu-id="8df3b-151">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="8df3b-152">Özel yardım GitHub havuzu</span><span class="sxs-lookup"><span data-stu-id="8df3b-152">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="8df3b-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8df3b-153">Additional resources</span></span>

[<span data-ttu-id="8df3b-154">Yardıma genel bakış</span><span class="sxs-lookup"><span data-stu-id="8df3b-154">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="8df3b-155">Görev kaydedici genel bakışı</span><span class="sxs-lookup"><span data-stu-id="8df3b-155">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="8df3b-156">Belge veya eğitim olarak kullanmak için görev kaydı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8df3b-156">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
