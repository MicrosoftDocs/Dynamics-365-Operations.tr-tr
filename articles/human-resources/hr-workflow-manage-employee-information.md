---
title: Personel bilgilerini yönetmek için iş akışları kullanma
description: Bu konu, personel bilgisini yönetmek için İnsan kaynakları için iş akışı yeteneğini nasıl kullanabileceğinizi açıklar. Örneğin, bir iş akışını bir pozisyonla ilişkilendirebilir ve çalışanların kendi kayıtlarını değiştirdiklerinde başlatılan bir onay iş akışı yapılandırabilirsiniz.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: aba7627877cd9b79dce5930e528f892e2d80baac
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058764"
---
# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="73460-104">Personel bilgilerini yönetmek için iş akışları kullanma</span><span class="sxs-lookup"><span data-stu-id="73460-104">Use workflows to manage employee information</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="73460-105">Bu konu, personel bilgisini yönetmek için İnsan kaynakları için iş akışı yeteneğini nasıl kullanabileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="73460-105">This article explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="73460-106">Örneğin, bir iş akışını bir pozisyonla ilişkilendirebilir ve çalışanların kendi kayıtlarını değiştirdiklerinde başlatılan bir onay iş akışı yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73460-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="73460-107">İnsan kaynakları için iş akışı kabiliyeti, insan kaynakları faaliyetlerini yönetmek için çok sayıda iş akışı sağlar.</span><span class="sxs-lookup"><span data-stu-id="73460-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="73460-108">Ek olarak, belirli iş akışlarını değiştirebilmeniz ve onları bir raporlama hiyerarşisiyle ilişkilendirebilmeniz için çok sayıda seçenek kullanabilmektedir.</span><span class="sxs-lookup"><span data-stu-id="73460-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="73460-109">İş akışları, yöneticilerin personel bilgilerinin çeşitli standart türlerinde değişik yapmalarını kolaylaştırmak için mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="73460-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="73460-110">İş akışını bir pozisyon ile ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73460-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="73460-111">Daha sonra, personeller kendi personel kayıtlarını değiştirirlerse, yeni bilgiler kaydedilemeden önce onay gerektiren bir iş akışı başlatılır.</span><span class="sxs-lookup"><span data-stu-id="73460-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="73460-112">İş akışları, değişiklikleri daha etkin şekilde yönetebilmeniz ve personel bilgilerinizi daha doğru tutabilmeniz için aşağıdaki türde bilgiler için önceden tanımlıdır:</span><span class="sxs-lookup"><span data-stu-id="73460-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="73460-113">Kimlik numaraları</span><span class="sxs-lookup"><span data-stu-id="73460-113">Identification numbers</span></span>
-   <span data-ttu-id="73460-114">Kurslar</span><span class="sxs-lookup"><span data-stu-id="73460-114">Courses</span></span>
-   <span data-ttu-id="73460-115">Eğitim</span><span class="sxs-lookup"><span data-stu-id="73460-115">Education</span></span>
-   <span data-ttu-id="73460-116">Resim</span><span class="sxs-lookup"><span data-stu-id="73460-116">Image</span></span>
-   <span data-ttu-id="73460-117">Ödünç verilen maddeler</span><span class="sxs-lookup"><span data-stu-id="73460-117">Loaned items</span></span>
-   <span data-ttu-id="73460-118">Mesleki deneyim</span><span class="sxs-lookup"><span data-stu-id="73460-118">Professional experience</span></span>
-   <span data-ttu-id="73460-119">Proje deneyimi</span><span class="sxs-lookup"><span data-stu-id="73460-119">Project experience</span></span>
-   <span data-ttu-id="73460-120">Yetenekler</span><span class="sxs-lookup"><span data-stu-id="73460-120">Skills</span></span>
-   <span data-ttu-id="73460-121">Güven gerektiren pozisyonlar</span><span class="sxs-lookup"><span data-stu-id="73460-121">Positions of trust</span></span>
-   <span data-ttu-id="73460-122">İnsan kaynakları eylemleri</span><span class="sxs-lookup"><span data-stu-id="73460-122">Human resources actions</span></span>
-   <span data-ttu-id="73460-123">Kurs kaydı</span><span class="sxs-lookup"><span data-stu-id="73460-123">Course registration</span></span>

<span data-ttu-id="73460-124">Personeller işe alındıklarını, transfer edildiklerinde veya işten çıkarıldıklarında, iş akışı bir gözden geçirme işlemi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="73460-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="73460-125">Bu şekilde, bir belge gözden geçirilebilir veya bir eylemin koşulları, iş akışının bir parçası tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="73460-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="73460-126">Gözden geçirme işlemi tamamlandığında, belge veya eylem tamamlanır ve iş akışını son onayı adımına taşınır.</span><span class="sxs-lookup"><span data-stu-id="73460-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="73460-127">İş akışını bir pozisyon hiyerarşisiyle ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="73460-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="73460-128">Bir iş akışını, yapılandırdığınız herhangi bir hiyerarşiyle ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73460-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="73460-129">Örneğin, bir pozisyon, bir matris raporlama hiyerarşisi ile ilişkili ise, bir iş akışının belirli bir proje için giderleri, bu pozisyonla ilişkili bir personelin yöneticisi yerine proje liderine yönlendirmesini sağlayacak üzere yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73460-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="73460-130">Yeni bir iş akışı oluşturun veya varolan bir iş akışını değiştirmek için **İnsan Kaynakları iş akışı** sayfasında **Yeni** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73460-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="73460-131">İş akışı tasarımcısını başlatmak için listeden bir iş akışını seçin.</span><span class="sxs-lookup"><span data-stu-id="73460-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="73460-132">Yeni bir iş akışı oluşturmak için tasarımcıyı kullanabilir veya mevcut bir iş akışındaki adımları değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73460-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="73460-133">Mevcut bir iş akışını değiştirdiğinizde, değişiklikleriniz yeni bir sürüm olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="73460-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="73460-134">Gerekirse bu nedenle, her zaman önceki sürüme geri dönebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73460-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="73460-135">İnsan kaynakları iş akışı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="73460-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="73460-136">Çalışanlar kişisel kimlik saptamalarında değişiklik talep ettiklerinde başlatılacak basit bir iş akışı yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="73460-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="73460-137">**İnsan Kaynakları iş akışları** sayfasında **Yeni**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="73460-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="73460-138">Kullanılabilir iş akışları listesinden **Kimlik saptama numaraları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="73460-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="73460-139">İş akışı tasarımcısını başlatmak için **Çalıştır**'ı tıklatın ve istenildiğinde kullanıcı adınızı ve parolanızı girin.</span><span class="sxs-lookup"><span data-stu-id="73460-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="73460-140">İş akışı öğeleri listesinden **Kimlik saptama numarasını** öğesini, tasarımcı tuvaline sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="73460-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="73460-141">Onay öğesini **Başlat** ve **Bitir** ile bağlayın.</span><span class="sxs-lookup"><span data-stu-id="73460-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="73460-142">**Öğeyi onayla** üzerine çift tıklatın ve sonra sağ tıklayıp **Özellikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="73460-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="73460-143">İş öğesi yönergeleri eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="73460-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="73460-144">**Atama**'yı seçin ve sonra atama türü altında **Hiyerarşi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="73460-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="73460-145">**Hiyerarşi** seçimi altında **Yapılandırılabilir hiyerarşi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="73460-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="73460-146">Bir durdurma koşulu ekleyin ve sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="73460-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="73460-147">Tüm ek yönergeleri tamamlayın (ek uyarılar mevcut olmamalıdır).</span><span class="sxs-lookup"><span data-stu-id="73460-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="73460-148">**Kaydet ve kapat**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="73460-148">Click **Save and close**.</span></span> <span data-ttu-id="73460-149">Yeni iş akışını etkinleştirip iletişim kutusu açılınca **Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="73460-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="73460-150">**İnsan Kaynakları** &gt; **Pozisyonlar** &gt; **Pozisyon hiyerarşi türleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="73460-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="73460-151">**Matris**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="73460-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="73460-152">**Çalışan kimlik saptama numarası**'nı iş akışı listesine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="73460-152">Add the **Worker identification number** workflow to the list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73460-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="73460-153">Additional resources</span></span>

[<span data-ttu-id="73460-154">Adres değişikliklerini görüntüle ve yönet</span><span class="sxs-lookup"><span data-stu-id="73460-154">View and manage address changes</span></span>](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]