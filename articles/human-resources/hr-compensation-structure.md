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
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abdca618aa544e32b68f4bbf2578afb9ef1a5905
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052901"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="3368a-103">Ücret yapısı geliştirme</span><span class="sxs-lookup"><span data-stu-id="3368a-103">Develop a compensation structure</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3368a-104">Bu makale, bir Sabit ücret planı oluşturma ve çalışanların uygunluk kuralları aracılığıyla plana kaydedilmesini sağlama konusunda sizi yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="3368a-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="3368a-105">Bu makale USMF demo verilerini kullanır ve ücret ve sosyal haklar yöneticilerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3368a-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="3368a-106">Sabit ücret planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="3368a-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="3368a-107">**Ücret Yönetimi** seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="3368a-108">**Sabit ücret planları** seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="3368a-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-109">Select **New**.</span></span>

4. <span data-ttu-id="3368a-110">**Plan** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3368a-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="3368a-111">**Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3368a-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="3368a-112">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="3368a-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="3368a-113">**Tür** alanında, sabit ücret planının bir **Bant**, **Derece** veya **Adım** planı olup olmadığını seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="3368a-114">**İzin verilen öneri onay kutusu**, İşlem olayı sırasında bu plana eklenen tüm eylemler için varsayılan değer olarak işlev görür.</span><span class="sxs-lookup"><span data-stu-id="3368a-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="3368a-115">Önerilere izin vermek, ücreti işlerken hesaplanan kılavuz tutarı geçersiz kılmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="3368a-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="3368a-116">**Aralık dışında toleransı**, belirli bir düzey için belirtilen ücret yapısı aralığının dışında kalan ücret tutarlarının nasıl ele alınacağını belirtmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3368a-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="3368a-117">**Aralık dışı tolerans** alanını **yok** olarak ayarlamak, herhangi bir maaş tutarını kullanmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="3368a-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="3368a-118">**Yumuşak tolerans**, ücret tutarı bu düzeye ilişkin minimum referans noktası tutarından düşük olduğunda veya bu düzeye ilişkin maksimum tutardan yüksek olduğunda kullanıcıyı uyarır.</span><span class="sxs-lookup"><span data-stu-id="3368a-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="3368a-119">Kullanıcı uyarıyı yok sayıp devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="3368a-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="3368a-120">**Sert tolerans**, bir çalışanın ücreti düzeye ilişkin minimum ve maksimum referans noktalarının dışında olacak şekilde ayarlandığında hata verir ve çalışanın ücretini bu aralıkta olacak şekilde otomatik olarak düzenler.</span><span class="sxs-lookup"><span data-stu-id="3368a-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="3368a-121">**İşe alma kuralı** alanı bir çalışanın işlem olayı sırasında maaşına karşılık hesaplar.</span><span class="sxs-lookup"><span data-stu-id="3368a-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="3368a-122">**İşe alma kuralı** **Yüzdesi**, çalışanın istihdam edildiği süreye eşit oranda dağıtılan artışı hesaplar.</span><span class="sxs-lookup"><span data-stu-id="3368a-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="3368a-123">**Para birimi** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3368a-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="3368a-124">**Ödeme oranı dönüştürme** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="3368a-125">**Aralık kullanım matrisi** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3368a-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="3368a-126">İsteğe bağlı olarak, çalışanların orta noktadaki ödemeye daha hızlı ulaşmalarını ve kendi ücret aralıklarındaki maksimum kademeye daha yavaş ulaşmalarını sağlamak için ücret kademesi kullanım kayıtları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3368a-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="3368a-127">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-127">Select **Save**.</span></span> <span data-ttu-id="3368a-128">Bu, **maaş ayarla** düğmesini etkinleştirir ve plan için maaş yapınızı tanımlamaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="3368a-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="3368a-129">**Ücret ayarlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-129">Select **Set up compensation**.</span></span> <span data-ttu-id="3368a-130">Ücret yapısı bu üç yöntemlerden birini kullanarak oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="3368a-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="3368a-131">Bir referans noktası kümesi seçip kendi yapınızı oluşturmak için düzeyler ekleyerek tamamen yeni bir yapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3368a-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="3368a-132">Başlangıç noktası olarak mevcut bir plandan ücret yapısını kopyalayın ve bunu yeni plan için değiştirin.</span><span class="sxs-lookup"><span data-stu-id="3368a-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="3368a-133">Mevcut bir ücret kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-133">Select an existing compensation grid.</span></span> <span data-ttu-id="3368a-134">Ücret kılavuzu başka bir plan tarafından kullanılıyorsa, kılavuzda yapılan değişiklikler diğer plana da yansır.</span><span class="sxs-lookup"><span data-stu-id="3368a-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="3368a-135">**Mevcut maaş matrisinden yeni oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="3368a-136">**Izgaradan kopyala** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="3368a-137">İsteğe bağlı olarak, seçilen kılavuzun kopyası olarak oluşturulacak yeni ücret kılavuzunun adını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3368a-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="3368a-138">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-138">Select **OK**.</span></span>

19. <span data-ttu-id="3368a-139">**Toplu değişiklik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-139">Select **Mass change**.</span></span> <span data-ttu-id="3368a-140">**Toplu değiştirme**, bir veya daha fazla düzeye ve/veya referans noktasına bir yüzde veya sabit tutar artışı uygulayarak ücret matrisi tutarlarını korumanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3368a-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="3368a-141">**Ayarlama tutarı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3368a-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="3368a-142">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="3368a-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="3368a-143">**Kılavuza uygula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3368a-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="3368a-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3368a-144">Close the page.</span></span> <span data-ttu-id="3368a-145">Ücret yapısı oluşturulduktan veya seçildikten sonra, Sabit ücret planı için hangi referans noktalarının Denetim noktası olarak kullanılacağını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3368a-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="3368a-146">Denetim noktası, bir çalışanın Karşılaştırma Oranı hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3368a-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="3368a-147">**Kontrol noktası** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="3368a-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3368a-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="3368a-149">Sabit ücret planı için uygunluk kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="3368a-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="3368a-150">Yeni sabit ücret planı, plan için Uygunluk kuralları tanımlanana kadar bir çalışana atanamaz.</span><span class="sxs-lookup"><span data-stu-id="3368a-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="3368a-151">**Uygunluk kurallarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="3368a-152">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-152">Select **New**.</span></span>

3. <span data-ttu-id="3368a-153">**Uygunluk** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3368a-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="3368a-154">**Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3368a-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="3368a-155">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="3368a-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="3368a-156">Hem Sabit hem de Değişken ücret planları uygunluk kurallarını kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3368a-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="3368a-157">**Tür** alanında plan türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="3368a-158">**Plan** alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="3368a-159">Bir çalışanın ücret planına uygun olması için karşılaması gereken ölçütü seçin.</span><span class="sxs-lookup"><span data-stu-id="3368a-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="3368a-160">Ölçütler şunlar olabilir:</span><span class="sxs-lookup"><span data-stu-id="3368a-160">Criteria can include:</span></span>

    - <span data-ttu-id="3368a-161">**Departman**</span><span class="sxs-lookup"><span data-stu-id="3368a-161">**Department**</span></span>
    - <span data-ttu-id="3368a-162">**Sendika**</span><span class="sxs-lookup"><span data-stu-id="3368a-162">**Labor union**</span></span>
    - <span data-ttu-id="3368a-163">**Konum** (**Ücret bölgesi**)</span><span class="sxs-lookup"><span data-stu-id="3368a-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="3368a-164">**İş**</span><span class="sxs-lookup"><span data-stu-id="3368a-164">**Job**</span></span>
    - <span data-ttu-id="3368a-165">**İşlev**</span><span class="sxs-lookup"><span data-stu-id="3368a-165">**Function**</span></span>
    - <span data-ttu-id="3368a-166">**İş türü**</span><span class="sxs-lookup"><span data-stu-id="3368a-166">**Job type**</span></span>
    - <span data-ttu-id="3368a-167">**Tazminat düzeyi**</span><span class="sxs-lookup"><span data-stu-id="3368a-167">**Compensation level**</span></span>
    
    <span data-ttu-id="3368a-168">Bir çalışanın ücret planına uygun olması için belirtilen tüm ölçütleri karşılaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3368a-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="3368a-169">Herhangi bir ölçüt seçilmezse, tüm çalışanlar ücret planı için uygun olur.</span><span class="sxs-lookup"><span data-stu-id="3368a-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="3368a-170">Bir çalışanın uygunluk kuralında belirtilen ölçüte uymuyorsa veya ücret planı için uygunluk kuralı belirtilmediyse, ücret planı bir çalışan için Sabit ücret kaydı oluşturma sırasında arama yapıldığında görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="3368a-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="3368a-171">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3368a-171">Close the page.</span></span>

8. <span data-ttu-id="3368a-172">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3368a-172">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]