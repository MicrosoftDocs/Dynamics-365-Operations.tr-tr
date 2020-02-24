---
title: Yardım sistemini bağlama
description: Bu konuda, Finance and Operations uygulamaları için Yardım sistemin bileşenleri açıklanmakta, bu bileşenlere nasıl bağlanacağınıza ilişkin bir genel bakış ve özel yardımın nasıl oluşturulacağının bir özeti verilmektedir.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4427388d75c1aef40a978ce35c831d5b714f2562
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006184"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="edf8e-103">Yardım sistemini bağlama</span><span class="sxs-lookup"><span data-stu-id="edf8e-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edf8e-104">Bu konuda, Dynamics 365 Finance, Supply Chain Management, Commerce ve Human Resources gibi Finance and Operations uygulamaları için Yardım sisteminin bileşenleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="edf8e-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Commerce, and Human Resources.</span></span> <span data-ttu-id="edf8e-105">Bu bileşenlere nasıl bağlanılacağı ve özel yardım oluşturma hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="edf8e-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="edf8e-106">Yardım mimarisi</span><span class="sxs-lookup"><span data-stu-id="edf8e-106">Help architecture</span></span>

<span data-ttu-id="edf8e-107">Aşağıdaki örnek Yardım sisteminin bölümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="edf8e-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="edf8e-108">Ürün içi Yardım sistemi, Lifecycle Services'deki (LCS) İş Süreci Modelleyici'de depolanan görev kılavuzlarını ve https://docs.microsoft.com adresindeki makaleleri çeker.</span><span class="sxs-lookup"><span data-stu-id="edf8e-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="edf8e-109">Not: Diyagramda yıldız işareti (\*) ile listelenen özellikler planlanmıştır, ancak henüz kullanılabilir değildir.</span><span class="sxs-lookup"><span data-stu-id="edf8e-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="edf8e-110">[![Yardım mimarisi](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="edf8e-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="edf8e-111">Yardım sistemine bağlanma</span><span class="sxs-lookup"><span data-stu-id="edf8e-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="edf8e-112">**Görev kılavuzları** sekmesi şu anda Dynamics 365 Human Resources veya Commerce'te kullanılmıyor.</span><span class="sxs-lookup"><span data-stu-id="edf8e-112">The **Task guides** tab is currently not available in Dynamics 365 Human Resources or Commerce.</span></span> <span data-ttu-id="edf8e-113">Bu işlevi gelecekteki bir sürümde etkinleştirmek için çalışıyoruz.</span><span class="sxs-lookup"><span data-stu-id="edf8e-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="edf8e-114">Human Resources'ın Başlarken deneyimindeki Görev kılavuzları, temel işlevselliği sağlamak üzere kullanılabilir kalıyor.</span><span class="sxs-lookup"><span data-stu-id="edf8e-114">The Task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="edf8e-115">Ayrıca, hem Human Resources hem de Commerce için docs.microsoft.com sitesinde yordamsal yardım da mevcut.</span><span class="sxs-lookup"><span data-stu-id="edf8e-115">Procedural help is also available on the docs.microsoft.com site for both Human Resources and Commerce.</span></span>

<span data-ttu-id="edf8e-116">**Sistem Parametreleri** sayfasını kullanarak, sistem yöneticileri bir uygulama için Yardım sisteminin parçalarını bağlar.</span><span class="sxs-lookup"><span data-stu-id="edf8e-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="edf8e-117">[![Yardım ayarlarıyla Sistem Parametreleri formu](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="edf8e-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="edf8e-118">**Sistem parametreleri** sayfası üzerinde, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="edf8e-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="edf8e-119">**Yardım** sekmesini ilk kez açtığınızda Lifecycle Services'e bağlanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="edf8e-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="edf8e-120">Formun ortasındaki bağlantıya tıkladığınızdan emin olun, bağlantı için bekleyin, iletişim kutusunu kapatın ve **Sistem parametreleri**sayfasına ulaşmak için **Tamam** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="edf8e-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="edf8e-121">[![LCS'ye bağlan](./media/connect-to-lcs-crop-1024x365.png "LCS'ye bağlan")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="edf8e-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="edf8e-122">Bağlanmak için Lifecycle Hizmetleri projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="edf8e-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="edf8e-123">Görev kayıtlarını almak için BPM kitaplıkları (Seçili proje içinde) seçin.</span><span class="sxs-lookup"><span data-stu-id="edf8e-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="edf8e-124">BPM kitaplıklarının görüntülenme sırasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="edf8e-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="edf8e-125">Bu **Yardım** bölmesinde kitaplıklardaki görev kayıtlarının hangi sırayla görüneceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="edf8e-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="edf8e-126">Bu adımları tamamladıktan sonra **Yardım** bölmesini açabilir ve **Görev kılavuzları** sekmesine tıklayabilirsiniz. Artık, Finance and Operations uygulamalarında bulunduğunuz sayfa için geçerli olan görev kılavuzlarını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="edf8e-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="edf8e-127">Görev kılavuzu bulunamadıysa, anahtar sözcükler girerek aramanızı daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="edf8e-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="edf8e-128">Çevrilmiş görev kılavuzları gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="edf8e-128">Showing translated task guides</span></span>

<span data-ttu-id="edf8e-129">Çevrilmiş görev kılavuzları ilk olarak Mayıs 2016 APQC Birleştirilmiş Kitaplığı'na ve Başlangıç kitaplığına sevk edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="edf8e-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="edf8e-130">Finance and Operations uygulamalarında, yerelleştirilmiş görev kılavuzu yardımını görmek için, Mayıs ayı kitaplığına bağlı olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="edf8e-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="edf8e-131">Görev kılavuzunun görüntülendiği dil her kullanıcı için **Seçenekler** &gt; **Tercihler** altındaki Dil ayarlarından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="edf8e-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="edf8e-132">Pek çok görev kılavuzu çevrilmiş olsa da şu anda istemci çevrilmiş görev kılavuz adlarını göstermemektedir.</span><span class="sxs-lookup"><span data-stu-id="edf8e-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="edf8e-133">Ayrıca, yalnızca Şubat 2016'da yayımlanan görev kılavuzları, Mayıs ayı Kitaplığı'nda çeviri olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="edf8e-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="edf8e-134">Ek çevirilerle güncelleştirilmiş bir kitaplık yayımlayacağız.</span><span class="sxs-lookup"><span data-stu-id="edf8e-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="edf8e-135">Görev kılavuzu çevrildiyse, görev kılavuzunu açtığınızda, görev kılavuzundaki tüm metin seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="edf8e-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="edf8e-136">Görev kılavuzu çevrilmediyse, açtığınızda, yalnızca bazı metinler (kontrollerin metinleri) seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="edf8e-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="edf8e-137">Özel yardım oluşturma</span><span class="sxs-lookup"><span data-stu-id="edf8e-137">Creating custom help</span></span>

<span data-ttu-id="edf8e-138">Görev kılavuzlarını özel yardım oluşturmak veya bir web sitesini Yardım panosuna bağlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="edf8e-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="edf8e-139">Görev kılavuzlarıyla özel yardım oluşturmak</span><span class="sxs-lookup"><span data-stu-id="edf8e-139">Create custom help with task guides</span></span>

<span data-ttu-id="edf8e-140">Uygulamanızı yansıtan görev kayıtları oluşturarak ve bunları bir LCS İş Süreci Kitaplığına kaydederek Finance, Supply Chain Management ve Commerce uygulamanız için özel yardım oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="edf8e-140">You can create custom help for Finance, Supply Chain Management, and Commerce by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="edf8e-141">Human Resources için özel görev kılavuzları oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="edf8e-141">You cannot create custom task guides for Human Resources.</span></span>

<span data-ttu-id="edf8e-142">Ortaklar için, bir kitaplığı şirket kitaplığına yükseltirseniz ve bir çözüme eklerseniz, müşterileriniz tarafından kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="edf8e-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="edf8e-143">Ayrıca APQC Birleştirilmiş global kitaplığın bir kopyasını oluşturabilirsiniz ve ardından kopyayı açabilir, kopyadan görev kayıtlarını açarak onları değiştirebilir ve değişiklik yaptığınız kayıtları kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="edf8e-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="edf8e-144">Daha fazla bilgi için bkz. [Görev kaydedici kaynakları](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="edf8e-144">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="edf8e-145">Özel bir siteye bağlanmak</span><span class="sxs-lookup"><span data-stu-id="edf8e-145">Connect a custom site</span></span>

<span data-ttu-id="edf8e-146">Microsoft, özel yardım sitesini oluşturma ve bağlamak hakkında bir teknik inceleme ve örnek kodu sağlamıştır.</span><span class="sxs-lookup"><span data-stu-id="edf8e-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="edf8e-147">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="edf8e-147">For more information, see:</span></span>

- [<span data-ttu-id="edf8e-148">Finance and Operations uygulamaları için Özel Yardım oluşturma (teknik inceleme)</span><span class="sxs-lookup"><span data-stu-id="edf8e-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="edf8e-149">Özel yardım GitHub havuzu</span><span class="sxs-lookup"><span data-stu-id="edf8e-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="edf8e-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="edf8e-150">Additional resources</span></span>

[<span data-ttu-id="edf8e-151">Yardım sistemi</span><span class="sxs-lookup"><span data-stu-id="edf8e-151">Help system</span></span>](help-overview.md)

[<span data-ttu-id="edf8e-152">Görev kaydedici kaynakları</span><span class="sxs-lookup"><span data-stu-id="edf8e-152">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="edf8e-153">Görev Kaydedici ile belge veya eğitim oluşturma</span><span class="sxs-lookup"><span data-stu-id="edf8e-153">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
