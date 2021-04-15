---
title: Ücret yapısı geliştirme
description: Bu makale, bir Sabit ücret planı oluşturma ve çalışanların uygunluk kuralları aracılığıyla plana kaydedilmesini sağlama konusunda sizi yönlendirir.
author: andreabichsel
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75d1a05d4f94689581e2a67a13adeef6b14ac0cd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800915"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="99e0c-103">Ücret yapısı geliştirme</span><span class="sxs-lookup"><span data-stu-id="99e0c-103">Develop a compensation structure</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="99e0c-104">Bu makale, bir Sabit ücret planı oluşturma ve çalışanların uygunluk kuralları aracılığıyla plana kaydedilmesini sağlama konusunda sizi yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="99e0c-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="99e0c-105">Bu makale USMF demo verilerini kullanır ve ücret ve sosyal haklar yöneticilerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="99e0c-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="99e0c-106">Sabit ücret planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="99e0c-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="99e0c-107">**Ücret Yönetimi** seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="99e0c-108">**Sabit ücret planları** seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="99e0c-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-109">Select **New**.</span></span>

4. <span data-ttu-id="99e0c-110">**Plan** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="99e0c-111">**Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="99e0c-112">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="99e0c-113">**Tür** alanında, sabit ücret planının bir **Bant**, **Derece** veya **Adım** planı olup olmadığını seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="99e0c-114">**İzin verilen öneri onay kutusu**, İşlem olayı sırasında bu plana eklenen tüm eylemler için varsayılan değer olarak işlev görür.</span><span class="sxs-lookup"><span data-stu-id="99e0c-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="99e0c-115">Önerilere izin vermek, ücreti işlerken hesaplanan kılavuz tutarı geçersiz kılmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="99e0c-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="99e0c-116">**Aralık dışında toleransı**, belirli bir düzey için belirtilen ücret yapısı aralığının dışında kalan ücret tutarlarının nasıl ele alınacağını belirtmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="99e0c-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="99e0c-117">**Aralık dışı tolerans** alanını **yok** olarak ayarlamak, herhangi bir maaş tutarını kullanmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="99e0c-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="99e0c-118">**Yumuşak tolerans**, ücret tutarı bu düzeye ilişkin minimum referans noktası tutarından düşük olduğunda veya bu düzeye ilişkin maksimum tutardan yüksek olduğunda kullanıcıyı uyarır.</span><span class="sxs-lookup"><span data-stu-id="99e0c-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="99e0c-119">Kullanıcı uyarıyı yok sayıp devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="99e0c-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="99e0c-120">**Sert tolerans**, bir çalışanın ücreti düzeye ilişkin minimum ve maksimum referans noktalarının dışında olacak şekilde ayarlandığında hata verir ve çalışanın ücretini bu aralıkta olacak şekilde otomatik olarak düzenler.</span><span class="sxs-lookup"><span data-stu-id="99e0c-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="99e0c-121">**İşe alma kuralı** alanı bir çalışanın işlem olayı sırasında maaşına karşılık hesaplar.</span><span class="sxs-lookup"><span data-stu-id="99e0c-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="99e0c-122">**İşe alma kuralı** **Yüzdesi**, çalışanın istihdam edildiği süreye eşit oranda dağıtılan artışı hesaplar.</span><span class="sxs-lookup"><span data-stu-id="99e0c-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="99e0c-123">**Para birimi** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99e0c-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="99e0c-124">**Ödeme oranı dönüştürme** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="99e0c-125">**Aralık kullanım matrisi** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="99e0c-126">İsteğe bağlı olarak, çalışanların orta noktadaki ödemeye daha hızlı ulaşmalarını ve kendi ücret aralıklarındaki maksimum kademeye daha yavaş ulaşmalarını sağlamak için ücret kademesi kullanım kayıtları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="99e0c-127">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-127">Select **Save**.</span></span> <span data-ttu-id="99e0c-128">Bu, **maaş ayarla** düğmesini etkinleştirir ve plan için maaş yapınızı tanımlamaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="99e0c-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="99e0c-129">**Ücret ayarlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-129">Select **Set up compensation**.</span></span> <span data-ttu-id="99e0c-130">Ücret yapısı bu üç yöntemlerden birini kullanarak oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="99e0c-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="99e0c-131">Bir referans noktası kümesi seçip kendi yapınızı oluşturmak için düzeyler ekleyerek tamamen yeni bir yapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="99e0c-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="99e0c-132">Başlangıç noktası olarak mevcut bir plandan ücret yapısını kopyalayın ve bunu yeni plan için değiştirin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="99e0c-133">Mevcut bir ücret kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-133">Select an existing compensation grid.</span></span> <span data-ttu-id="99e0c-134">Ücret kılavuzu başka bir plan tarafından kullanılıyorsa, kılavuzda yapılan değişiklikler diğer plana da yansır.</span><span class="sxs-lookup"><span data-stu-id="99e0c-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="99e0c-135">**Mevcut maaş matrisinden yeni oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="99e0c-136">**Izgaradan kopyala** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="99e0c-137">İsteğe bağlı olarak, seçilen kılavuzun kopyası olarak oluşturulacak yeni ücret kılavuzunun adını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99e0c-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="99e0c-138">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-138">Select **OK**.</span></span>

19. <span data-ttu-id="99e0c-139">**Toplu değişiklik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-139">Select **Mass change**.</span></span> <span data-ttu-id="99e0c-140">**Toplu değiştirme**, bir veya daha fazla düzeye ve/veya referans noktasına bir yüzde veya sabit tutar artışı uygulayarak ücret matrisi tutarlarını korumanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="99e0c-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="99e0c-141">**Ayarlama tutarı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="99e0c-142">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="99e0c-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="99e0c-143">**Kılavuza uygula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99e0c-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="99e0c-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99e0c-144">Close the page.</span></span> <span data-ttu-id="99e0c-145">Ücret yapısı oluşturulduktan veya seçildikten sonra, Sabit ücret planı için hangi referans noktalarının Denetim noktası olarak kullanılacağını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99e0c-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="99e0c-146">Denetim noktası, bir çalışanın Karşılaştırma Oranı hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="99e0c-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="99e0c-147">**Kontrol noktası** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="99e0c-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99e0c-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="99e0c-149">Sabit ücret planı için uygunluk kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="99e0c-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="99e0c-150">Yeni sabit ücret planı, plan için Uygunluk kuralları tanımlanana kadar bir çalışana atanamaz.</span><span class="sxs-lookup"><span data-stu-id="99e0c-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="99e0c-151">**Uygunluk kurallarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="99e0c-152">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-152">Select **New**.</span></span>

3. <span data-ttu-id="99e0c-153">**Uygunluk** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="99e0c-154">**Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="99e0c-155">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="99e0c-156">Hem Sabit hem de Değişken ücret planları uygunluk kurallarını kullanılır.</span><span class="sxs-lookup"><span data-stu-id="99e0c-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="99e0c-157">**Tür** alanında plan türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="99e0c-158">**Plan** alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="99e0c-159">Bir çalışanın ücret planına uygun olması için karşılaması gereken ölçütü seçin.</span><span class="sxs-lookup"><span data-stu-id="99e0c-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="99e0c-160">Ölçütler şunlar olabilir:</span><span class="sxs-lookup"><span data-stu-id="99e0c-160">Criteria can include:</span></span>

    - <span data-ttu-id="99e0c-161">**Departman**</span><span class="sxs-lookup"><span data-stu-id="99e0c-161">**Department**</span></span>
    - <span data-ttu-id="99e0c-162">**Sendika**</span><span class="sxs-lookup"><span data-stu-id="99e0c-162">**Labor union**</span></span>
    - <span data-ttu-id="99e0c-163">**Konum** (**Ücret bölgesi**)</span><span class="sxs-lookup"><span data-stu-id="99e0c-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="99e0c-164">**İş**</span><span class="sxs-lookup"><span data-stu-id="99e0c-164">**Job**</span></span>
    - <span data-ttu-id="99e0c-165">**İşlev**</span><span class="sxs-lookup"><span data-stu-id="99e0c-165">**Function**</span></span>
    - <span data-ttu-id="99e0c-166">**İş türü**</span><span class="sxs-lookup"><span data-stu-id="99e0c-166">**Job type**</span></span>
    - <span data-ttu-id="99e0c-167">**Tazminat düzeyi**</span><span class="sxs-lookup"><span data-stu-id="99e0c-167">**Compensation level**</span></span>
    
    <span data-ttu-id="99e0c-168">Bir çalışanın ücret planına uygun olması için belirtilen tüm ölçütleri karşılaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="99e0c-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="99e0c-169">Herhangi bir ölçüt seçilmezse, tüm çalışanlar ücret planı için uygun olur.</span><span class="sxs-lookup"><span data-stu-id="99e0c-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="99e0c-170">Bir çalışanın uygunluk kuralında belirtilen ölçüte uymuyorsa veya ücret planı için uygunluk kuralı belirtilmediyse, ücret planı bir çalışan için Sabit ücret kaydı oluşturma sırasında arama yapıldığında görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="99e0c-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="99e0c-171">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99e0c-171">Close the page.</span></span>

8. <span data-ttu-id="99e0c-172">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99e0c-172">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]