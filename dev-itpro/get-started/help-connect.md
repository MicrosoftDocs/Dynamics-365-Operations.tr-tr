---
title: "Yardım sistemini bağlama"
description: "Bu konu, Microsoft Dynamics 365 for Finance and Operations için Yardım sisteminin bileşenleri açıklar ve bu bileşenleri nasıl bağlanacağınıza genel bakış ve özel yardımın nasıl oluşturulacağının bir özetini sunar."
author: margoc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: acb832c422ccb5ddb98d6ddd6b69d2e2c3e11057
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="41144-103">Yardım sistemini bağlama</span><span class="sxs-lookup"><span data-stu-id="41144-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="41144-104">Bu konu, Microsoft Dynamics 365 for Finance and Operations'un Yardım sisteminin bileşenlerini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="41144-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="41144-105">Bu bileşenlere nasıl bağlanılacağı ve özel yardım oluşturma hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="41144-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="41144-106">Yardım mimarisi</span><span class="sxs-lookup"><span data-stu-id="41144-106">Help architecture</span></span>
<span data-ttu-id="41144-107">Aşağıdaki çizim, Finance and Operations Yardım sisteminin bölümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="41144-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="41144-108">Ürün içi Yardım sistemi, Dynamics 365 Lifecycle Services'deki (LCS) İş Süreci Modelleyici'de ve https://docs.microsoft.com adresinde bulunan görev kayıtlarıyla Finance and Operations makalelerini çeker.</span><span class="sxs-lookup"><span data-stu-id="41144-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="41144-109">Not: Diyagramda yıldız işareti (\*) ile listelenen özellikler planlanmıştır, ancak henüz kullanılabilir değildir.</span><span class="sxs-lookup"><span data-stu-id="41144-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="41144-110">[![Yardım mimarisi](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="41144-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="41144-111">Yardım sistemine bağlanma</span><span class="sxs-lookup"><span data-stu-id="41144-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="41144-112">**Görev kılavuzları** sekmesi Microsoft Dynamics 365 for Talent ve Microsoft Dynamics 365 for Retail için henüz kullanılabilir değildir.</span><span class="sxs-lookup"><span data-stu-id="41144-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="41144-113">Bu işlevi gelecekteki bir sürümde etkinleştirmek için çalışıyoruz.</span><span class="sxs-lookup"><span data-stu-id="41144-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="41144-114">Başlarken deneyimindeki Görev kılavuzları, temel işlevselliği kapsamak üzere kullanılabilir kalır.</span><span class="sxs-lookup"><span data-stu-id="41144-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="41144-115">Yordamlama yardımı da docs.microsoft.com sitesinde, hem Retail hem Talen için kullanılabilir ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)).</span><span class="sxs-lookup"><span data-stu-id="41144-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="41144-116">**Sistem Parametreleri** sayfasını kullanarak, sistem yöneticileri bir uygulama için Yardım sisteminin parçalarını bağlar.</span><span class="sxs-lookup"><span data-stu-id="41144-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="41144-117">[![Sistem Parametreleri formu Yardım ayarları](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) **Sistem parametreleri** sayfasında şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="41144-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41144-118">**Yardım** sekmesini ilk kez açtığınızda Lifecycle Services'e bağlanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="41144-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="41144-119">Formun ortasındaki bağlantıya tıkladığınızdan emin olun, bağlantı için bekleyin, iletişim kutusunu kapatın ve **Sistem Parametreleri** sayfasına ulaşmak için **Tamam**'a tıklayın.[![LCS'ye bağlan](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="41144-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="41144-120">Bağlanmak için Lifecycle Hizmetleri projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="41144-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="41144-121">Görev kayıtlarını almak için BPM kitaplıkları (Seçili proje içinde) seçin.</span><span class="sxs-lookup"><span data-stu-id="41144-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="41144-122">Finance and Operations için, Microsoft içeriği için, 2017 QPC Unified Library for Microsoft Dynamics for Finance and Operations'u seçin.</span><span class="sxs-lookup"><span data-stu-id="41144-122">For Finance and Operations, for Microsoft content, select the February 2017 QPC Unified Library for Microsoft Dynamics 365 for Finance and Operations.</span></span> 
    - <span data-ttu-id="41144-123">Retail için bir kütüphaneyi Temmuz'da yayımlayacağız.</span><span class="sxs-lookup"><span data-stu-id="41144-123">For Retail, we will be releasing a library in July.</span></span> 
    - <span data-ttu-id="41144-124">Talent için bir kütüphane seçmeniz gerekmez; doğru kütüphane ile bağlantı sizin için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="41144-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="41144-125">BPM kitaplıklarının görüntülenme sırasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="41144-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="41144-126">Bu **Yardım** bölmesinde kitaplıklardaki görev kayıtlarının hangi sırayla görüneceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="41144-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="41144-127">Bu adımları tamamladıktan sonra **Yardım** bölmesini açabilir ve **Görev kılavuzları** sekmesini tıklatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41144-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab.</span></span> <span data-ttu-id="41144-128">Finance and Operations'ta o anda bulunduğunuz sayfayla ilgili görev kılavuzlarını görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="41144-128">You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="41144-129">Görev kılavuzu bulunamadıysa, anahtar sözcükler girerek aramanızı daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41144-129">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="41144-130">Çevrilmiş görev kılavuzları gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="41144-130">Showing translated task guides</span></span>

<span data-ttu-id="41144-131">Çevrilmiş görev kılavuzları ilk olarak Mayıs 2016 APQC Birleştirilmiş Kitaplığı'na ve Başlangıç kitaplığına sevk edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="41144-131">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="41144-132">Finance and Operations içinde yerelleştirilmiş görev kılavuzu yardımını görmek için Mayıs kitaplığına bağlı olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="41144-132">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="41144-133">Görev kılavuzunun görüntülendiği dil her kullanıcı için **Seçenekler** &gt; **Tercihler** altındaki Dil ayarlarından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="41144-133">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="41144-134">Pek çok görev kılavuzu çevrilmiş olsa da şu anda Finance and Operations istemcisi çevrilmiş görev kılavuz adlarını göstermemektedir.</span><span class="sxs-lookup"><span data-stu-id="41144-134">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="41144-135">Ayrıca, yalnızca Şubat 2016'da yayımlanan görev kılavuzları, Mayıs ayı Kitaplığı'nda çeviri olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="41144-135">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="41144-136">Ek çevirilerle güncelleştirilmiş bir kitaplık yayımlayacağız.</span><span class="sxs-lookup"><span data-stu-id="41144-136">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="41144-137">Görev kılavuzu çevrildiyse, görev kılavuzunu açtığınızda, görev kılavuzundaki tüm metin seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="41144-137">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="41144-138">Görev kılavuzu çevrilmediyse, açtığınızda, yalnızca bazı metinler (kontrollerin metinleri) seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="41144-138">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="41144-139">Özel yardım oluşturma</span><span class="sxs-lookup"><span data-stu-id="41144-139">Creating custom help</span></span>
<span data-ttu-id="41144-140">Uygulamanızı yansıtan görev kayıtları oluşturarak ve bunları bir LCS İş Süreci Kitaplığına kaydederek Finance and Operations ve Retail uygulamanız için özel yardım oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41144-140">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="41144-141">Talent için özel görev kılavuzları oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="41144-141">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="41144-142">Ortaklar için, bir kitaplığı şirket kitaplığına yükseltirseniz ve bir çözüme eklerseniz, müşterileriniz tarafından kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="41144-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="41144-143">Ayrıca APQC Birleştirilmiş global kitaplığın bir kopyasını oluşturabilirsiniz ve ardından kopyayı açabilir, kopyadan görev kayıtlarını açarak onları değiştirebilir ve değişiklik yaptığınız kayıtları kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41144-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="41144-144">Daha fazla bilgi için bkz. [Belge veya eğitim olarak kullanmak için görev kaydı oluşturma](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="41144-144">For more information, see [How to create a task recording to use as documentation or training](../user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="41144-145">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="41144-145">See also</span></span>
--------

[<span data-ttu-id="41144-146">Yardıma genel bakış</span><span class="sxs-lookup"><span data-stu-id="41144-146">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="41144-147">Görev kaydedici genel bakışı</span><span class="sxs-lookup"><span data-stu-id="41144-147">Task recorder overview</span></span>](../user-interface/task-recorder.md)

[<span data-ttu-id="41144-148">Belge veya eğitim olarak kullanmak için görev kaydı oluşturma</span><span class="sxs-lookup"><span data-stu-id="41144-148">How to create a task recording to use as documentation or training</span></span>](../user-interface/task-recorder-training-docs.md)





