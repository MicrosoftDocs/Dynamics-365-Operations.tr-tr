---
title: Bütçe planlama gerekçe belgeleri
description: Gerekçe belgeleri, belirli bir bütçenin neden gerekli olduğunu açıklamak isteyenler için açıklama sağlar.
author: panolte
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8754c017a966cb1d11a72d6f8a80e1088aeb9100
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210325"
---
# <a name="budget-planning-justification-documents"></a><span data-ttu-id="9208c-103">Bütçe planlama gerekçe belgeleri</span><span class="sxs-lookup"><span data-stu-id="9208c-103">Budget planning justification documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9208c-104">Gerekçe belgeleri, belirli bir bütçenin neden gerekli olduğunu açıklamak isteyenler için açıklama sağlar.</span><span class="sxs-lookup"><span data-stu-id="9208c-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="9208c-105">Bir bütçe planı şablonu, bütçe yöneticisi tarafından Microsoft Word içerisinde oluşturulur ve geçerli bütçe planlama işlemine atanır.</span><span class="sxs-lookup"><span data-stu-id="9208c-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="9208c-106">Bütçe sahipleri daha sonra şablonu açabilir ve verinin bütçe isteklerine göre Word içerisinde otomatik doldurulmasını sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="9208c-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="9208c-107">Daha sonra, kaydetmeden önce ek metin veya veri ekleyebilir ve kişiselleştirilmiş gerekçe belgelerini bütçe planına ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="9208c-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="9208c-108">Microsoft Word için Microsoft Dynamics Office Eklentisini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="9208c-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="9208c-109">Yeni bir Microsoft Word belgesi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="9208c-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="9208c-110">Şerit üzerinde **Ekle**'yi tıklatın ve **Depola**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="9208c-111">Microsoft Dynamics Office Eklentisi'ni aratın ve **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="9208c-112">Word içerisinde, sağdaki bölmede **Sunucu bilgisi ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="9208c-113">Sunucu URL'sini yazın veya yapıştırın ve **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="9208c-114">Microsoft Word içinde doğrulama şablonunu tanımlayın</span><span class="sxs-lookup"><span data-stu-id="9208c-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="9208c-115">Microsoft Dynamics Office Ekletisi'ne oturum açtıktan sonra **Tasarım**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="9208c-116">Başlık bilgisi için **Alanlar ekle** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9208c-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="9208c-117">BudgetPlanJustification varlık veri kaynağını seçin ve **İleri**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="9208c-118">**Not:** Bu varlık tüm gerekçe belgeleri için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9208c-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="9208c-119">Diğer varlıklar da kullanılabilir ancak bu varlık dahil edilmemişse Microsoft Dynamics 365 Finance'a geri yüklerken başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="9208c-119">Other entities can be used but the upload back to Microsoft Dynamics 365 Finance will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="9208c-120">BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ve DocumentNumber etiketlerini ve değerlerini Word dosyasına ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9208c-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="9208c-121">**Not:** Gerekirse standart etiketler yerine kendi özel etiketlerinizi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9208c-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="9208c-122">Başlık bölümünü tamamlamak için **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="9208c-123">Bütçe planı tutarlarının satır düzeyi ayrıntıları için **Tablo ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="9208c-124">Daha sonra yine BudgetPlanJustification varlık veri kaynağını seçin ve **İleri**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="9208c-125">EffectiveDate, ScenarioName, AccountDisplayValue ve AccountingCurrencyExpenseAmount için alanlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9208c-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="9208c-126">**Not:** Yorumlar, Tekil bütçe planı satırlarına eklenmek için kullanılabilirse, bunlar buradaki tabloya eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="9208c-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="9208c-127">Son kullanıcıya sağlamak için varsa ek yönergeleri ekleyin ve belge üzerinde gerekli biçimlendirme ve stilleri gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="9208c-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="9208c-128">Belgeyi yerel bilgisayarınıza kaydedin ve devam etmeden önce dosyayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="9208c-129">Gerekçe şablonunu kullanmak için Bütçe planlama işlemini ayarlama</span><span class="sxs-lookup"><span data-stu-id="9208c-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="9208c-130">**Bütçelendirme** &gt; **Kurulum** &gt; **Bütçe planlama** &gt; **Gerekçe belge şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="9208c-130">Go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="9208c-131">**Yeni**'yi tıklatın ve yeni oluşturulan Microsoft Word belgenize gidin.</span><span class="sxs-lookup"><span data-stu-id="9208c-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="9208c-132">Şablon görüntüleme adı ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="9208c-132">Enter a template display name and description.</span></span> <span data-ttu-id="9208c-133">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-133">Click **OK**.</span></span>
4.  <span data-ttu-id="9208c-134">**Bütçeleme** &gt; **Kurulum** &gt; **Bütçe** **planlama** &gt; **Bütçe planlama işlemi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9208c-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="9208c-135">Gerekçe şablonunun kullanılacağı işlemi seçin ve **Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9208c-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="9208c-136">**Gerekçe belge şablonu** alanında, uygun şablonu seçin ve kaydedin.</span><span class="sxs-lookup"><span data-stu-id="9208c-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="9208c-137">Kişiselleştirilmiş gerekçe belgelerini düzenleme ve kaydetme</span><span class="sxs-lookup"><span data-stu-id="9208c-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="9208c-138">Yeni bir bütçe planı oluşturun veya var olan bir bütçe planını açın.</span><span class="sxs-lookup"><span data-stu-id="9208c-138">Create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="9208c-139">**Gerekçe** aşağı açılan menüsünden **Yeni gerekçe oluşturma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="9208c-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="9208c-140">Ayrıntılar doldurduktan sonra, karşıya yüklemek için **Gerekçe** aşağı açılan menü üzerinden kişiselleştirilmiş belgeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="9208c-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]