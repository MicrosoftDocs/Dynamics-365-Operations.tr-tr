---
title: Yetenekleri girin
description: Çalışanlar ve yöneticiler Dynamics 365 Human Resources'da yetenek girebilir.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193989"
---
# <a name="enter-skills"></a><span data-ttu-id="2b380-103">Yetenekleri girin</span><span class="sxs-lookup"><span data-stu-id="2b380-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2b380-104">Dynamics 365 Human Resources'ta çalışanlar, başvuranlar veya ilgili kişiler için hedef yetenekler veya gerçek yetenekler girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b380-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2b380-105">Hedef yetenek, bir kişinin elde etmeyi planladığı yetenektir.</span><span class="sxs-lookup"><span data-stu-id="2b380-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="2b380-106">Gerçek yetenek, bir kişinin sahip olduğu yetenektir.</span><span class="sxs-lookup"><span data-stu-id="2b380-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="2b380-107">Otomatik onay becerileri için iş akışı oluştur</span><span class="sxs-lookup"><span data-stu-id="2b380-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="2b380-108">Onay gerektirmeden yetenekleri girmek için, otomatik onay becerileri için bir iş akışı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b380-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="2b380-109">Çalışanlar tarafından girilen yetenekler her zaman yönetici onayını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="2b380-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="2b380-110">Bu iş akışı, yalnızca yöneticiler tarafından çalışanlar adına girilen yetenekleri otomatik olarak onaylar.</span><span class="sxs-lookup"><span data-stu-id="2b380-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="2b380-111">**Personel yönetimi** çalışma alanında, **Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="2b380-112">**Kurulum**'un altında, **İnsan kaynakları iş akışlarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="2b380-113">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-113">Select **New**.</span></span>

4. <span data-ttu-id="2b380-114">**İş akışı oluştur** bölmesinde, **Çalışan yetenekleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="2b380-115">[![Çalışan becerileri iş akışı Seç](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="2b380-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="2b380-116">**Bu dosyada açılsın mı?** iletişim kutusunda **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="2b380-117">İstendiğinde, kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="2b380-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="2b380-118">İş akışı Düzenleyicisi 'nde, **onay becerileri** iş akışı öğesini seçin ve tuvale sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="2b380-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="2b380-119">[![Onay yeteneklerini Seç iş akışı öğesi](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="2b380-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="2b380-120">**Başlangıç** öğesini **onay yetenekleri 1** öğesine bağlayın ve sonra da **onay yetenekleri 1** öğesini **son** öğeye bağlayın.</span><span class="sxs-lookup"><span data-stu-id="2b380-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="2b380-121">**Son** öğeyi görmek için aşağı doğru gitmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="2b380-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="2b380-122">Diğer öğelere daha yakın bir yere sürükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b380-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="2b380-123">[![Connect iş akışı öğeleri](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="2b380-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="2b380-124">**Onay yetenekleri 1** iş akışı öğesini çift tıklatın ve sonra **Adım 1** öğesini sağ tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2b380-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="2b380-125">**1. adımı** Sağ tıklatın ve sonra **Özellikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="2b380-126">**Özellikler** penceresinde, sol taraftaki Gezinti çubuğunda **Koşul**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="2b380-127">**Bu adımı yalnızca aşağıdaki koşul karşılandığında çalıştır** belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2b380-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="2b380-128">**Koşulu ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-128">Select **Add condition**.</span></span> <span data-ttu-id="2b380-129">**Nerede** seçeneğinden sonra, **Çalışan Self Servis yeteneklerini** seçin ve ardından **Çalışan Self Servis becerileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="2b380-130">**is**'den sonra, **alan** seçin ve **kişiye göre kullanıcı ilişkisi.Kişi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="2b380-131">[![Koşul Belirt](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="2b380-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="2b380-132">Sol gezinti çubuğunda **atama** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="2b380-133">**Atama türü** sekmesinde **hiyerarşi** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="2b380-134">**Hiyerarşi seçimi** sekmesinde, **Hiyerarşi türü:** alanında, **Yönetim hiyerarşisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="2b380-135">[![Yönetim hiyerarşisini belirtin](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="2b380-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="2b380-136">**Kapat**'ı seçin, tuval içerik listesinde **iş akışı**'nı seçin ve sonra **Kaydet ve Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="2b380-137">İş akışları oluşturmayla ilgili daha fazla bilgi için bkz. [İş akışı sistemine genel bakış](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2b380-137">For more information about creating workflows, see [Workflow system overview](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="2b380-138">Bir işçi için yetenekler girin</span><span class="sxs-lookup"><span data-stu-id="2b380-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="2b380-139">Çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-139">Select a worker.</span></span>

2. <span data-ttu-id="2b380-140">**İşçi** sayfasının eylem çubuğunda , **kişi**'yi seçin ve sonra da **yetenekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="2b380-141">**Yetenekler** sayfasında, her yetenek için aşağıdaki alanları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="2b380-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="2b380-142">**Yetenek**: bir yetenek seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="2b380-143">**Düzey türü**: çalışanın zaten sahip olduğu bir yetenek için **gerçek** 'ı seçin veya çalışanın doğru çalıştığı bir yetenek için **hedef** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="2b380-144">**Düzey**: çalışan becerisi için bir düzey seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="2b380-145">**Düzey tarihi**: Takvim aracında bir tarih seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="2b380-146">**Denetleyici** : uygunsa, listeden bir Denetleyicisi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="2b380-147">Aramanıza filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b380-147">You can filter your search.</span></span>
   - <span data-ttu-id="2b380-148">**Deneyim yılı**: deneyim yıllarına girin.</span><span class="sxs-lookup"><span data-stu-id="2b380-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="2b380-149">**Doğrulandı**: Yetenek doğrulanırsa, kutuyu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2b380-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="2b380-150">**Doğrulayan**: Doğrulayıcı adını girin.</span><span class="sxs-lookup"><span data-stu-id="2b380-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="2b380-151">Yetenekleri girmeyi tamamladığınızda, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b380-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b380-152">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="2b380-152">See also</span></span>

[<span data-ttu-id="2b380-153">Yetenekleri konfigüre et</span><span class="sxs-lookup"><span data-stu-id="2b380-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="2b380-154">Becerileri eşleştirme</span><span class="sxs-lookup"><span data-stu-id="2b380-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]