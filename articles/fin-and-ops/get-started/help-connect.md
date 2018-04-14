---
title: "Yardım sistemini bağlama"
description: "Bu konu, Microsoft Dynamics 365 for Finance and Operations için Yardım sisteminin bileşenleri açıklar ve bu bileşenleri nasıl bağlanacağınıza genel bakış ve özel yardımın nasıl oluşturulacağının bir özetini sunar."
author: margoc
manager: AnnBe
ms.date: 09/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2deb2aea7dce889a655fbd5dec5ec928e0f10bb8
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="connect-the-help-system"></a><span data-ttu-id="ebe62-103">Yardım sistemini bağlama</span><span class="sxs-lookup"><span data-stu-id="ebe62-103">Connect the Help system</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ebe62-104">Bu konu, Microsoft Dynamics 365 for Finance and Operations'un Yardım sisteminin bileşenlerini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="ebe62-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="ebe62-105">Bu bileşenlere nasıl bağlanılacağı ve özel yardım oluşturma hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="ebe62-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="ebe62-106">Yardım mimarisi</span><span class="sxs-lookup"><span data-stu-id="ebe62-106">Help architecture</span></span>
<span data-ttu-id="ebe62-107">Aşağıdaki çizim, Finance and Operations Yardım sisteminin bölümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ebe62-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="ebe62-108">Ürün içi Yardım sistemi, Dynamics 365 Lifecycle Services'deki (LCS) İş Süreci Modelleyici'de ve https://docs.microsoft.com adresinde bulunan görev kayıtlarıyla Finance and Operations makalelerini çeker.</span><span class="sxs-lookup"><span data-stu-id="ebe62-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="ebe62-109">Not: Diyagramda yıldız işareti (\*) ile listelenen özellikler planlanmıştır, ancak henüz kullanılabilir değildir.</span><span class="sxs-lookup"><span data-stu-id="ebe62-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="ebe62-110">[![Yardım mimarisi](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="ebe62-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="ebe62-111">Yardım sistemine bağlanma</span><span class="sxs-lookup"><span data-stu-id="ebe62-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="ebe62-112">**Görev kılavuzları** sekmesi Microsoft Dynamics 365 for Talent ve Microsoft Dynamics 365 for Retail için henüz kullanılabilir değildir.</span><span class="sxs-lookup"><span data-stu-id="ebe62-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="ebe62-113">Bu işlevi gelecekteki bir sürümde etkinleştirmek için çalışıyoruz.</span><span class="sxs-lookup"><span data-stu-id="ebe62-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="ebe62-114">Başlarken deneyimindeki Görev kılavuzları, temel işlevselliği kapsamak üzere kullanılabilir kalır.</span><span class="sxs-lookup"><span data-stu-id="ebe62-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="ebe62-115">Yordamlama yardımı da docs.microsoft.com sitesinde, hem Retail hem Talen için kullanılabilir ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)).</span><span class="sxs-lookup"><span data-stu-id="ebe62-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>


<span data-ttu-id="ebe62-116">**Sistem Parametreleri** sayfasını kullanarak, sistem yöneticileri bir uygulama için Yardım sisteminin parçalarını bağlar.</span><span class="sxs-lookup"><span data-stu-id="ebe62-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="ebe62-117">[![Sistem Parametreleri formu Yardım ayarları](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) **Sistem parametreleri** sayfasında şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="ebe62-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ebe62-118">**Yardım** sekmesini ilk kez açtığınızda Lifecycle Services'e bağlanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ebe62-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="ebe62-119">Formun ortasındaki bağlantıya tıkladığınızdan emin olun, bağlantı için bekleyin, iletişim kutusunu kapatın ve **Sistem parametreleri** sayfasını almak için **Tamam**'a tıklayın.[![LCS'ye bağlan](./media/connect-to-lcs-crop-1024x365.png "LCS'ye bağlan")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="ebe62-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="ebe62-120">Bağlanmak için Lifecycle Hizmetleri projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ebe62-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="ebe62-121">Görev kayıtlarını almak için BPM kitaplıkları (Seçili proje içinde) seçin.</span><span class="sxs-lookup"><span data-stu-id="ebe62-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="ebe62-122">Finance and Operations için, Microsoft içeriği için, en yeni APQC Unified Library for Finance and Operations'u seçin.</span><span class="sxs-lookup"><span data-stu-id="ebe62-122">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span> 
    - <span data-ttu-id="ebe62-123">Retail için bir kütüphaneyi yakın zamanda yayımlayacağız.</span><span class="sxs-lookup"><span data-stu-id="ebe62-123">For Retail, we will be releasing a library in the near future.</span></span> 
    - <span data-ttu-id="ebe62-124">Talent için bir kütüphane seçmeniz gerekmez; doğru kütüphane ile bağlantı sizin için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ebe62-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="ebe62-125">BPM kitaplıklarının görüntülenme sırasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ebe62-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="ebe62-126">Bu **Yardım** bölmesinde kitaplıklardaki görev kayıtlarının hangi sırayla görüneceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="ebe62-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="ebe62-127">Bu adımları tamamladıktan sonra, **Yardım** bölmesini açabilir ve **Görev kılavuzları** sekmesine tıklayabilirsiniz. Şimdi, Finance and Operations'ta içinde bulunduğunuz sayfa için geçerli olan görev kılavuzlarını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="ebe62-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="ebe62-128">Görev kılavuzu bulunamadıysa, anahtar sözcükler girerek aramanızı daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ebe62-128">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="ebe62-129">Çevrilmiş görev kılavuzları gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="ebe62-129">Showing translated task guides</span></span>

<span data-ttu-id="ebe62-130">Çevrilmiş görev kılavuzları ilk olarak Mayıs 2016 APQC Birleştirilmiş Kitaplığı'na ve Başlangıç kitaplığına sevk edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ebe62-130">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="ebe62-131">Finance and Operations içinde yerelleştirilmiş görev kılavuzu yardımını görmek için Mayıs kitaplığına bağlı olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ebe62-131">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="ebe62-132">Görev kılavuzunun görüntülendiği dil her kullanıcı için **Seçenekler** &gt; **Tercihler** altındaki Dil ayarlarından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="ebe62-132">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ebe62-133">Pek çok görev kılavuzu çevrilmiş olsa da şu anda Finance and Operations istemcisi çevrilmiş görev kılavuz adlarını göstermemektedir.</span><span class="sxs-lookup"><span data-stu-id="ebe62-133">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="ebe62-134">Ayrıca, yalnızca Şubat 2016'da yayımlanan görev kılavuzları, Mayıs ayı Kitaplığı'nda çeviri olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ebe62-134">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="ebe62-135">Ek çevirilerle güncelleştirilmiş bir kitaplık yayımlayacağız.</span><span class="sxs-lookup"><span data-stu-id="ebe62-135">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="ebe62-136">Görev kılavuzu çevrildiyse, görev kılavuzunu açtığınızda, görev kılavuzundaki tüm metin seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ebe62-136">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="ebe62-137">Görev kılavuzu çevrilmediyse, açtığınızda, yalnızca bazı metinler (kontrollerin metinleri) seçmiş olduğunuz dilde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ebe62-137">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="ebe62-138">Özel yardım oluşturma</span><span class="sxs-lookup"><span data-stu-id="ebe62-138">Creating custom help</span></span>
<span data-ttu-id="ebe62-139">Uygulamanızı yansıtan görev kayıtları oluşturarak ve bunları bir LCS İş Süreci Kitaplığına kaydederek Finance and Operations ve Retail uygulamanız için özel yardım oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ebe62-139">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="ebe62-140">Talent için özel görev kılavuzları oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="ebe62-140">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="ebe62-141">Ortaklar için, bir kitaplığı şirket kitaplığına yükseltirseniz ve bir çözüme eklerseniz, müşterileriniz tarafından kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ebe62-141">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="ebe62-142">Ayrıca APQC Birleştirilmiş global kitaplığın bir kopyasını oluşturabilirsiniz ve ardından kopyayı açabilir, kopyadan görev kayıtlarını açarak onları değiştirebilir ve değişiklik yaptığınız kayıtları kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ebe62-142">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="ebe62-143">Daha fazla bilgi için bkz. [Belge veya eğitim olarak kullanmak için görev kaydı oluşturma](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="ebe62-143">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="ebe62-144">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="ebe62-144">See also</span></span>
--------

[<span data-ttu-id="ebe62-145">Yardıma genel bakış</span><span class="sxs-lookup"><span data-stu-id="ebe62-145">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="ebe62-146">Görev kaydedici genel bakışı</span><span class="sxs-lookup"><span data-stu-id="ebe62-146">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="ebe62-147">Belge veya eğitim olarak kullanmak için görev kaydı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ebe62-147">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)





