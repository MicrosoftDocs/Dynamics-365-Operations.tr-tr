---
title: "Bütçe planlama gerekçe belgeleri"
description: "Gerekçe belgeleri, belirli bir bütçenin neden gerekli olduğunu açıklamak isteyenler için açıklama sağlar."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b033f6197e61a6030e12081a9e4f1d820bac458f
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="budget-planning-justification-documents"></a><span data-ttu-id="1f2f6-103">Bütçe planlama gerekçe belgeleri</span><span class="sxs-lookup"><span data-stu-id="1f2f6-103">Budget planning justification documents</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1f2f6-104">Gerekçe belgeleri, belirli bir bütçenin neden gerekli olduğunu açıklamak isteyenler için açıklama sağlar.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="1f2f6-105">Bir bütçe planı şablonu, bütçe yöneticisi tarafından Microsoft Word içerisinde oluşturulur ve geçerli bütçe planlama işlemine atanır.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="1f2f6-106">Bütçe sahipleri daha sonra şablonu açabilir ve verinin bütçe isteklerine göre Word içerisinde otomatik doldurulmasını sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="1f2f6-107">Daha sonra, kaydetmeden önce ek metin veya veri ekleyebilir ve kişiselleştirilmiş gerekçe belgelerini bütçe planına ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="1f2f6-108">Microsoft Word için Microsoft Dynamics Office eklentisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1f2f6-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="1f2f6-109">Yeni bir Microsoft Word belgesi açın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="1f2f6-110">Şerit üzerinde **Ekle**'yi tıklatın ve **Depola**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="1f2f6-111">Microsoft Dynamics Office Eklentisi'ni aratın ve **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="1f2f6-112">Word içerisinde, sağdaki bölmede **Sunucu bilgisi ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="1f2f6-113">Sunucu URL'sini yazın veya yapıştırın ve **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="1f2f6-114">Microsoft Word içerisinde Gerekçe şablonunu tanımlama</span><span class="sxs-lookup"><span data-stu-id="1f2f6-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="1f2f6-115">Microsoft Dynamics Office Ekletisi'ne oturum açtıktan sonra **Tasarım**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="1f2f6-116">Başlık bilgisi için **Alanlar ekle** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="1f2f6-117">BudgetPlanJustification varlık veri kaynağını seçin ve **İleri**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="1f2f6-118">**Not:** Bu varlık tüm gerekçe belgeleri için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="1f2f6-119">Diğer varlıklar da kullanılabilir ancak bu varlık dahil edilmemişse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a geri yüklerken başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-119">Other entities can be used but the upload back to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="1f2f6-120">BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ve DocumentNumber etiketlerini ve değerlerini Word dosyasına ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="1f2f6-121">**Not:** Gerekirse standart etiketler yerine kendi özel etiketlerinizi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="1f2f6-122">Başlık bölümünü tamamlamak için **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="1f2f6-123">Bütçe planı tutarlarının satır düzeyi ayrıntıları için **Tablo ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="1f2f6-124">Daha sonra yine BudgetPlanJustification varlık veri kaynağını seçin ve **İleri**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="1f2f6-125">EffectiveDate, ScenarioName, AccountDisplayValue ve AccountingCurrencyExpenseAmount için alanlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="1f2f6-126">**Not:** Yorumlar, Tekil bütçe planı satırlarına eklenmek için kullanılabilirse, bunlar buradaki tabloya eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="1f2f6-127">Son kullanıcıya sağlamak için varsa ek yönergeleri ekleyin ve belge üzerinde gerekli biçimlendirme ve stilleri gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="1f2f6-128">Belgeyi yerel bilgisayarınıza kaydedin ve devam etmeden önce dosyayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="1f2f6-129">Gerekçe şablonunu kullanmak için Bütçe planlama işlemini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1f2f6-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="1f2f6-130">Finance and Operations içerisinde **Bütçelendirme** &gt; **Kurulum** &gt; **Bütçe planlama** &gt; **Gerekçe belge şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-130">In Finance and Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="1f2f6-131">**Yeni**'yi tıklatın ve yeni oluşturulan Microsoft Word belgenize gidin.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="1f2f6-132">Şablon görüntüleme adı ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-132">Enter a template display name and description.</span></span> <span data-ttu-id="1f2f6-133">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-133">Click **OK**.</span></span>
4.  <span data-ttu-id="1f2f6-134">**Bütçeleme** &gt; **Kurulum** &gt; **Bütçe** **planlama** &gt; **Bütçe planlama işlemi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="1f2f6-135">Gerekçe şablonunun kullanılacağı işlemi seçin ve **Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="1f2f6-136">**Gerekçe belge şablonu** alanında, uygun şablonu seçin ve kaydedin.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="1f2f6-137">Kişiselleştirilmiş gerekçe belgelerini düzenleme ve kaydetme</span><span class="sxs-lookup"><span data-stu-id="1f2f6-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="1f2f6-138">Finance and Operations içerisinde, yeni bir bütçe planı oluşturun veya var olan bir bütçe planını açın.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-138">In Finance and Operations, create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="1f2f6-139">**Gerekçe** aşağı açılan menüsünden **Yeni gerekçe oluşturma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="1f2f6-140">Ayrıntılar doldurduktan sonra, karşıya yüklemek için **Gerekçe** aşağı açılan menü üzerinden kişiselleştirilmiş belgeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f2f6-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>





