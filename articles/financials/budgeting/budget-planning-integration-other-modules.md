---
title: "Diğer modüllerle bütçe planlama tümleştirmesi"
description: "Bütçe planları aşağıdaki çeşitli farklı kaynaklardan oluşturulabilir. Periyodik işlemin temel unsurları tüm kaynaklar için aynıdır."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 311a5cbd3768d8ecc7e7430717369193e60c3e57
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="budget-planning-integration-with-other-modules"></a><span data-ttu-id="562dd-104">Diğer modüllerle bütçe planlama tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="562dd-104">Budget planning integration with other modules</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="562dd-105"> Bütçe planları aşağıdaki çeşitli farklı kaynaklardan oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="562dd-105"> Budget plans can be generated from several, different resources.</span></span> <span data-ttu-id="562dd-106">Periyodik işlemin temel unsurları tüm kaynaklar için aynıdır.</span><span class="sxs-lookup"><span data-stu-id="562dd-106">The basic elements of the periodic process is the same for all resources.</span></span> 



<a name="periodic-processes-for-generating-budget-plans"></a><span data-ttu-id="562dd-107">Bütçe planları oluşturmaya yönelik periyodik işlemler</span><span class="sxs-lookup"><span data-stu-id="562dd-107">Periodic processes for generating budget plans</span></span>
----------------------------------------------

<span data-ttu-id="562dd-108">Bütçe planları aşağıdaki kaynaklardan oluşturulabilir:</span><span class="sxs-lookup"><span data-stu-id="562dd-108">Budget plans can be generated from the following resources:</span></span>

-   <span data-ttu-id="562dd-109">Genel muhasebe hareketleri</span><span class="sxs-lookup"><span data-stu-id="562dd-109">General ledger transactions</span></span>
-   <span data-ttu-id="562dd-110">Sabit kıymetler</span><span class="sxs-lookup"><span data-stu-id="562dd-110">Fixed assets</span></span>
-   <span data-ttu-id="562dd-111">Tahmin pozisyonları</span><span class="sxs-lookup"><span data-stu-id="562dd-111">Forecast positions</span></span>
-   <span data-ttu-id="562dd-112">Proje tahminleri</span><span class="sxs-lookup"><span data-stu-id="562dd-112">Project forecasts</span></span>
-   <span data-ttu-id="562dd-113">Tedarik tahminleri</span><span class="sxs-lookup"><span data-stu-id="562dd-113">Supply forecasts</span></span>
-   <span data-ttu-id="562dd-114">Talep tahminleri</span><span class="sxs-lookup"><span data-stu-id="562dd-114">Demand forecasts</span></span>
-   <span data-ttu-id="562dd-115">Bütçe kayıt girişleri</span><span class="sxs-lookup"><span data-stu-id="562dd-115">Budget register entries</span></span>
-   <span data-ttu-id="562dd-116">Diğer bütçe planları</span><span class="sxs-lookup"><span data-stu-id="562dd-116">Other budget plans</span></span>

<span data-ttu-id="562dd-117">Periyodik işlemin temel unsurları tüm işlemlerde aynıdır.</span><span class="sxs-lookup"><span data-stu-id="562dd-117">The basic elements of the periodic process are the same for all the processes.</span></span> <span data-ttu-id="562dd-118">Sekmeler, size verilerin kaynağını, hedef (bütçe planı) öznitelikleri ve işlemi bir toplu işlem olarak arka planda çalıştırmaya yönelik seçenekleri tanımlama olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="562dd-118">Tabs let you define the source of the data, the target (budget plan) attributes, and options to run the process in the background as a batch process.</span></span> <span data-ttu-id="562dd-119">Bu makalenin sonraki bölümlerinde, her işlemde görüntülenmeyebilecek öğeleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="562dd-119">Later sections of this article describe items that might not be apparent in each process.</span></span>

### <a name="actions"></a><span data-ttu-id="562dd-120">Eylemler</span><span class="sxs-lookup"><span data-stu-id="562dd-120">Actions</span></span>

<span data-ttu-id="562dd-121">Her oluşturma işlemi için üç eylem uygulanabilir:</span><span class="sxs-lookup"><span data-stu-id="562dd-121">For each generation process, three actions are available:</span></span>

-   <span data-ttu-id="562dd-122">**Yeni bir bütçe planı oluşturmak**, **Hedef bölümünde **seçilen özniteliklere sahip yeni bir plan oluşturur.</span><span class="sxs-lookup"><span data-stu-id="562dd-122">**Create a new budget plan** creates a new plan that has the attributes that are selected in the **Target **section.</span></span> <span data-ttu-id="562dd-123">Bu özniteliklerin benzersiz olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="562dd-123">These attributes don't have to be unique.</span></span> <span data-ttu-id="562dd-124">Bu nedenle, iki planın adları ve diğer değerleri aynı olabilir.</span><span class="sxs-lookup"><span data-stu-id="562dd-124">Therefore, two plans can have the same name and other values.</span></span>
-   <span data-ttu-id="562dd-125">**Var olan bütçe planı senaryosunu değiştirmek** seçilen bütçe planı senaryosunda hedef bütçe planındaki tüm verileri siler ve seçilen kaynak verilerini kullanan yeni satırlar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="562dd-125">**Replace the existing budget plan scenario** deletes all data in the target budget plan in the selected budget plan scenario and creates new lines that use the selected source data.</span></span>
-   <span data-ttu-id="562dd-126">**Var olan bütçe planı senaryosunu güncelleştirmek ve yeni veriler eklemek** hedef planda kaynak satırlarla eşleşen mevcut satırları günceller ve yeni veriler için yeni satırlar ekler.</span><span class="sxs-lookup"><span data-stu-id="562dd-126">**Update the existing budget plan scenario, and append new data** updates existing lines in the target plan that match the source lines and adds new lines for new data.</span></span> <span data-ttu-id="562dd-127">Eşleşme, genel muhasebe hesabına, tarihe, bütçe sınıfına ve diğer muhtelif alanlara dayanır.</span><span class="sxs-lookup"><span data-stu-id="562dd-127">The matching is based on the ledger account, date, budget class, and various other fields.</span></span> <span data-ttu-id="562dd-128">Örneğin, tahmin konumlarından bütçe planlarını oluştururken, konum numarası önemli bir alandır.</span><span class="sxs-lookup"><span data-stu-id="562dd-128">For example, when you generate budget plans from forecast positions, the position number is an important field.</span></span> <span data-ttu-id="562dd-129">Kaynak konum numarasıyla eşleşen bir konum numarası olan tüm satırlar, kaynaktan yeni satırlar ile değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="562dd-129">All lines that have a position number that matches the source position number are replaced with the new lines from the source.</span></span>

### <a name="source"></a><span data-ttu-id="562dd-130">Kaynak</span><span class="sxs-lookup"><span data-stu-id="562dd-130">Source</span></span>

<span data-ttu-id="562dd-131">Tüm işlemler için **Kaynak** sekmesi veriyi **Filtrele** düğmesini kullanarak filtrelemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="562dd-131">For all processes, the **Source** tab lets you filter data by using the **Filter** button.</span></span> <span data-ttu-id="562dd-132">Varsayılan olarak, her işlem için filtreye belirli alanlar eklenir.</span><span class="sxs-lookup"><span data-stu-id="562dd-132">By default, specific fields are added to the filter for each process.</span></span> <span data-ttu-id="562dd-133">Örneğin, **Genel muhasebeden bütçe planı oluştur** işleminde, **Genel muhasebe hesabı** ve **Ana hesap** kategorileri kullanılabilir ve oluşturma sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="562dd-133">For example, for the **Generate budget plan from general ledger** process, the **Ledger account** and **Main account** categories are available, and appear on the generation page.</span></span> <span data-ttu-id="562dd-134">Filtreye eklediğiniz her alan, eklediğiniz her kriterle birlikte sayfaya da eklenir.</span><span class="sxs-lookup"><span data-stu-id="562dd-134">Any fields that you add to the filter are also added to the page, together with with any criteria that you add.</span></span>

### <a name="target"></a><span data-ttu-id="562dd-135">Hedef</span><span class="sxs-lookup"><span data-stu-id="562dd-135">Target</span></span>

<span data-ttu-id="562dd-136">**Hedef** öğesindeki **Geçmiş** seçeneği size bütçe planında yürürlük tarihi olarak kaynak verilerden tarihleri kullanma olanağı verir.</span><span class="sxs-lookup"><span data-stu-id="562dd-136">The **Historical** option on the **Target** tab lets you use the dates from the source data as the effective date in the budget plan.</span></span> <span data-ttu-id="562dd-137">Genellikle, yürürlük tarihi planın bütçe döngüsü içinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="562dd-137">Typically, the effective date must be within the plan’s budget cycle.</span></span> <span data-ttu-id="562dd-138">**Geçmiş** seçeneğini **Evet** olarak ayarlarsanız, kaynağı tarihi (hatta yılı) kullanılır, böylece geçmiş verileri karşılaştırma için temel olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-138">When you set the **Historical** option to **Yes**, the date (even the year) of the source is used, so that you can use past data as a basis for comparison.</span></span> <span data-ttu-id="562dd-139">Bütçe planında geçmiş verileri değiştiremezsiniz ve plan onaylı bir iş akışı durumuna ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="562dd-139">You can't modify historical data in the budget plan, and the plan is set to an approved workflow status.</span></span> <span data-ttu-id="562dd-140">Ancak, plandaki diğer senaryoları değiştirmeniz gerekirse, durumu sıfırlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-140">However, you can reset the status if you must other scenarios in the plan require changes.</span></span>

<span data-ttu-id="562dd-141">Sayfanın üstündeki **Toplama göre toplam** alanı da kullanılan tarihi belirler.</span><span class="sxs-lookup"><span data-stu-id="562dd-141">The **Aggregate total by** field at the top of the page also determines the date that is used.</span></span> <span data-ttu-id="562dd-142">Bu alan tutarları toplar ve yürürlük tarihini isteğe bağlı olarak mali yılın veya mali dönemin ilk gününe ayarlar.</span><span class="sxs-lookup"><span data-stu-id="562dd-142">This field totals amounts, and optionally sets the effective date to the first day of the fiscal year or fiscal period.</span></span> 

<span data-ttu-id="562dd-143">**Hedef** öğesindeki alanların çoğu seçtiğiniz eyleme bağlı olarak düzenlenebilir veya salt okunur olabilir.</span><span class="sxs-lookup"><span data-stu-id="562dd-143">Many of the fields on the **Target** tab become editable or read-only, depending on the action that you select.</span></span> <span data-ttu-id="562dd-144">Yeni bir bütçe planı oluşturmaktan mevcut bir planı güncellemeye geçtiğinizde, **Bütçe planı adı** kullanılamaz olur ve mevcut bir planı seçmekle ilgili alanlar kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="562dd-144">When you change from creating a new budget plan to updating an existing plan, the **Budget plan name** field becomes unavailable, and the fields that are related to selecting an existing plan become available.</span></span> <span data-ttu-id="562dd-145">Hem **Hedef** sekmesinde hem de **Kaynak *sekmesinde, **Genel muhasebe** alanı her zaman kullanılamaz, çünkü değer seçili bütçe planlama süreci ile belirlenir.</span><span class="sxs-lookup"><span data-stu-id="562dd-145">On both the **Target** tab and the **Source **tab, the **Ledger** field is always unavailable, because the value is determined by the selected budget planning process.</span></span> 

<span data-ttu-id="562dd-146">**Bütçe sınıfı** alanı size bütçe planı satırlarını masraf hareketleri veya gelir hareketleri olarak ayarlama olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="562dd-146">The **Budget class** field lets you set the budget plan lines as either expense transactions or revenue transactions.</span></span> <span data-ttu-id="562dd-147">Genellikle gelir hareketleri bir genel muhasebe hesabına geçirilir ve bu nedenle negatif tutarlar olarak saklanır.</span><span class="sxs-lookup"><span data-stu-id="562dd-147">Usually, revenue transactions are credits to a ledger account and are therefore stored as negative amounts.</span></span> <span data-ttu-id="562dd-148">Genellikle, bu hareketler bütçe planında da negatif tutarlar olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="562dd-148">Typically, these transactions also appear as negative amounts in the budget plan.</span></span> <span data-ttu-id="562dd-149">Ancak, bütçe sınıfını plan düzeninde bir alan olarak ekleyerek, gelirin pozitif tutarlar olarak görünmesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-149">However, by adding the budget class as a field in the plan layout, you can enable revenue to appear as positive amounts.</span></span>

### <a name="generation-rules"></a><span data-ttu-id="562dd-150">Oluşturma kuralları</span><span class="sxs-lookup"><span data-stu-id="562dd-150">Generation rules</span></span>

<span data-ttu-id="562dd-151">Üç alan ek işlevsellik sağlar: **Faktör**, **Minimum** ve **Yuvarlama** **kuralı**.</span><span class="sxs-lookup"><span data-stu-id="562dd-151">Three fields provide additional functionality: **Factor**, **Minimum**, and **Rounding** **rule**.</span></span> 

<span data-ttu-id="562dd-152">**Faktör** alanındaki değer, bütçe planındaki tutarı ayarlamak için kaynak tutarı ile çarpılır.</span><span class="sxs-lookup"><span data-stu-id="562dd-152">The value in the **Factor** field is multiplied by the source amount to set the amount in the budget plan.</span></span> <span data-ttu-id="562dd-153">Bütçe planı satırları oluşturduğunuzda, ayarlamalar yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-153">You can then make adjustments when you create budget plan lines.</span></span> <span data-ttu-id="562dd-154">Örneğin, yüzde 3'lük bir artış için **1,03** girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-154">For example, you can enter **1.03** for a 3 percent increase.</span></span> <span data-ttu-id="562dd-155">Faktör pozitif bir sayı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="562dd-155">The factor must be a positive number.</span></span> 

<span data-ttu-id="562dd-156">**Minimum** alanı size bir bütçe planı satırı oluşturmak için eşik tutarını belirleme olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="562dd-156">The **Minimum** field lets you set the threshold amount for creating a budget plan line.</span></span> <span data-ttu-id="562dd-157">Kaynak tutarı bu sayıdan az ise, bütçe planı satırı oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="562dd-157">If the source amount is less than this number, the budget plan line isn't created.</span></span> <span data-ttu-id="562dd-158">Bir **0,00** değeri, tüm tutarlara izin verir ancak satırları pozitif tutarlara kısıtlamaz.</span><span class="sxs-lookup"><span data-stu-id="562dd-158">A value of **0.00** allows all amounts but doesn't limit lines to positive amounts.</span></span> <span data-ttu-id="562dd-159">(Pozitif tutarlara değer kısıtlama satırları yok.</span><span class="sxs-lookup"><span data-stu-id="562dd-159">(No value limits lines to positive amounts.</span></span> <span data-ttu-id="562dd-160">Negatif tutarlar her zaman dahildir ve genellikle alacak girişlerini temsil eder.)</span><span class="sxs-lookup"><span data-stu-id="562dd-160">Negative amounts are always included and usually represent credit entries.)</span></span>

<span data-ttu-id="562dd-161">**Yuvarlama kuralı** alanı oluşturulan bütçe planı satırlarının kesinliğini ayarlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="562dd-161">The **Rounding rule** field lets you set the precision of the budget plan lines that are created.</span></span> <span data-ttu-id="562dd-162">Tutarları para biriminin en yakın 1,00, 10,00, 100,00 vb değerlerine yuvarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-162">You can round amounts to the nearest 1.00, 10.00, 100.00, and so on, of currency.</span></span>

## <a name="notes-for-specific-processes"></a><span data-ttu-id="562dd-163">Belirli işlemler için Notlar</span><span class="sxs-lookup"><span data-stu-id="562dd-163">Notes for specific processes</span></span>
### <a name="generate-budget-plan-from-general-ledger"></a><span data-ttu-id="562dd-164">Genel muhasebeden bütçe planı oluştur</span><span class="sxs-lookup"><span data-stu-id="562dd-164">Generate budget plan from general ledger</span></span>

<span data-ttu-id="562dd-165">Genel muhasebe verilerinden bir bütçe planı oluşturduğunuzda, **Geçmiş** seçeneği **Hayır** olarak ayarlanmış ise, **Toplama göre toplam** alanını **Mali yıl** olarak ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="562dd-165">When you create a budget plan from general ledger data, you must set the **Aggregate total by** field to **Fiscal year** if the **Historical** option is set to **No**.</span></span> <span data-ttu-id="562dd-166">Kaynaktaki dönemler ve tarihler hedef tarihlerdeki dönemlerle eşleşmeyebilir.</span><span class="sxs-lookup"><span data-stu-id="562dd-166">The periods and dates in the source might not match the periods in dates in the target.</span></span> <span data-ttu-id="562dd-167">İşlemin bu değerleri eşleştirmek için güvenilir bir yolu olmadığı için, işlemi yılın ilk günü olarak sınırlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="562dd-167">Because the process has no reliable way to map these values, you must limit the process to the first of the year.</span></span> 

<span data-ttu-id="562dd-168">Hedefte, **Bütçe sınıfı** alanı **Gider** veya **Gelir** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="562dd-168">In the target, the **Budget class** field is set to either **Expense** or **Revenue**.</span></span> <span data-ttu-id="562dd-169">Bu ayar, bir satırdaki ana hesap **Gelir** veya **Gider** türü olmadığında, oluşturulan satırlar için **Bütçe türü** özniteliğini seçmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="562dd-169">This setting is used to select the **Budget type** attribute for lines that are created, when the main account on a line isn't of the **Revenue** or **Expense** type.</span></span>

### <a name="generate-budget-plan-from-fixed-assets"></a><span data-ttu-id="562dd-170">Sabit kıymetlerden bütçe planı oluştur</span><span class="sxs-lookup"><span data-stu-id="562dd-170">Generate budget plan from fixed assets</span></span>

<span data-ttu-id="562dd-171">**Sabit kıymetlerden bütçe planı oluştur** işleminde döneme veya güne göre toplam alma seçeneği yoktur.</span><span class="sxs-lookup"><span data-stu-id="562dd-171">The **Generate budget plan from fixed assets** process has no option for aggregating by period or day.</span></span> <span data-ttu-id="562dd-172">Bir planı tarihsel olarak ayarlamak için bir seçenek yoktur.</span><span class="sxs-lookup"><span data-stu-id="562dd-172">There is also no option for setting the plan as historical.</span></span> <span data-ttu-id="562dd-173">Bu periyodik işlemi, sabit varlıklar için öngörülen hareketleri bütçe planlamanıza dahil etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-173">You can use this periodic process to include projected transactions for fixed assets in your budget planning.</span></span>

### <a name="generate-budget-plan-from-forecast-positions"></a><span data-ttu-id="562dd-174">Tahmin konumlarından bütçe planı oluştur</span><span class="sxs-lookup"><span data-stu-id="562dd-174">Generate budget plan from forecast positions</span></span>

<span data-ttu-id="562dd-175">**Tahmin konumlarından bütçe planı oluştur** işlemi, kaynak tahmin konumunu bütçe plan satırına atar.</span><span class="sxs-lookup"><span data-stu-id="562dd-175">The **Generate budget plan from forecast positions** process assigns the source forecast position to the budget plan line.</span></span> <span data-ttu-id="562dd-176">Tahmin konumunu bütçe planı düzeninde bir satır olarak eklemek veya **Bütçe planı satırları** sorgulamasını kullanmak suretiyle konumu görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-176">You can view the position by adding the forecast position as a row in the budget plan layout or by using the **Budget plan lines** inquiry.</span></span> <span data-ttu-id="562dd-177">Tahmin konumunun bütçe planı satırlarına atanmasını istemiyorsanız, **Konumu bütçe planı satırına ekle** seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="562dd-177">If you don't want the forecast position to be assigned to budget plan lines, set the **Include position in budget plan line** option to **No**.</span></span>

<span data-ttu-id="562dd-178">Bütçe planındaki satırlar genel muhasebe hesabı ve konumuna göre toplanır.</span><span class="sxs-lookup"><span data-stu-id="562dd-178">Lines in the budget plan are aggregated by ledger account and position.</span></span> <span data-ttu-id="562dd-179">Ancak, satırların yalnızca genel muhasebe hesabına göre toplanması için konum numarasını hariç bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-179">However, you can exclude the position number, so that lines are aggregated by ledger account only.</span></span> <span data-ttu-id="562dd-180">**Hedef** öğesinde, **Konumu bütçe planına ekle** seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="562dd-180">On the **Target** tab, set the **Include position in budget plan** option to **No**.</span></span>

<span data-ttu-id="562dd-181">**Bütçe planı FTE senaryosu** alanında, bütçe planında tam zamanlı eşdeğerlerin (FTE'ler) sayısını eklemek için bir senaryo seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-181">In the **Budget plan FTE scenario** field, you can select a scenario to include the number of full-time equivalents (FTEs) in the budget plan.</span></span> <span data-ttu-id="562dd-182">Bu alan, hedef bütçe plan düzeninde bulunan miktar türü senaryolar ile sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="562dd-182">This field is limited to quantity-type scenarios that are included in the layout of the target budget plan.</span></span> <span data-ttu-id="562dd-183">Bir FTE senaryosu seçerseniz, ayrıca FTE ana hesabını da seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="562dd-183">If you select an FTE scenario, you must also select an FTE main account.</span></span> <span data-ttu-id="562dd-184">Bu hesap miktar bütçe planı satırları oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="562dd-184">This account is used to create the quantity budget plan lines.</span></span> 

<span data-ttu-id="562dd-185">Kaynakta seçilen bütçe planlama süreci ve bütçe planı senaryosu, hedef senaryo bütçe planlama sürecini ve senaryosunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="562dd-185">The budget planning process and budget plan scenario that are selected in the source set the target scenario budget planning process and scenario.</span></span> <span data-ttu-id="562dd-186">Bu öznitelikler tahmin konumlarına atandığı için, bütçe planı ile eşleşmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="562dd-186">Because these attributes are assigned to forecast positions, they must match the budget plan.</span></span> <span data-ttu-id="562dd-187">Bu nedenle, bu öznitelikler hedefte değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="562dd-187">Therefore, these attributes can't be modified on the target.</span></span>

### <a name="generate-budget-plan-from-project-forecasts"></a><span data-ttu-id="562dd-188">Proje tahminlerinden bütçe planı oluştur</span><span class="sxs-lookup"><span data-stu-id="562dd-188">Generate budget plan from project forecasts</span></span>

<span data-ttu-id="562dd-189">**Proje tahminlerinden bütçe planı oluştur** işleminde, **Tahmin konumlarından bütçe planı oluştur** işlemi gibi, bir miktar senaryosuna proje miktarları (saatler, giderler ve öğeler) ekleme seçeneği vardır.</span><span class="sxs-lookup"><span data-stu-id="562dd-189">The **Generate budget plan from project forecasts** process, like the **Generate budget plan from forecast positions** process, has an option to include project quantities (hours, expenses, and items) in a quantity scenario.</span></span> <span data-ttu-id="562dd-190">İki işlemde de bütçe plan düzenindeki sütunlar için benzer filtreler bulunur.</span><span class="sxs-lookup"><span data-stu-id="562dd-190">The two process also have similar filters for the columns in the budget plan layout.</span></span> 

<span data-ttu-id="562dd-191">**Kaynak** öğesinde, **Bildirim ekle** bölümündeki üç seçenek hangi bütçe planı satırlarının oluşturulduğunu belirler.</span><span class="sxs-lookup"><span data-stu-id="562dd-191">On the **Source** tab, three options in the **Include statement** section determine which budget plan lines are created.</span></span> <span data-ttu-id="562dd-192">Bu seçenekler, doğrudan proje tahminlerinden bütçe kayıt girişleri oluştururken kullanılabilen seçenekler ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="562dd-192">These options are the same as the options that are available when you create budget register entries directly from project forecasts.</span></span> <span data-ttu-id="562dd-193">Maliyet ve gelir satırları oluşturmak için, **Kâr ve zarar** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="562dd-193">Set the **Profit and loss** option to **Yes** to create lines for costs and for revenues.</span></span> <span data-ttu-id="562dd-194">Süren iş girişleri oluşturmak için, **Süren İş** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="562dd-194">Set the **WIP** option to **Yes** to create work in process entries.</span></span> <span data-ttu-id="562dd-195">Saat hareketlerine ilişkin bordro mahsup hesap satırları oluşturmak için **Bordro tahsisatı** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="562dd-195">Set the **Payroll allocation** option to **Yes** to create lines for the payroll offset accounts for hour transactions.</span></span> 

<span data-ttu-id="562dd-196">**Bütçe sınıfı** alanı yoktur, çünkü bütçe sınıfı (**Gider** veya **Gelir**) kaynak tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="562dd-196">There is no **Budget class** field, because the budget class (**Expense** or **Revenue**) is determined by the source.</span></span> 

<span data-ttu-id="562dd-197">Proje bütçelerini, proje bütçe tutarlarını içeren tahmin modelini seçerek, bir kaynak olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-197">You can use project budgets as a source by selecting the forecast model that contains the project budget amounts.</span></span> <span data-ttu-id="562dd-198">Proje bütçelerinin onaylanır onaylanmaz proje tahmin girişleri oluşturduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="562dd-198">Remember that project budgets create project forecast entries as they are approved.</span></span>

<span data-ttu-id="562dd-199">Bütçe planı satırlarına ilişkin olarak yalnızca maliyetleri veya gelirleri seçmek için, **Bütçe güncelleştirmeleri: Tutar türü = Maliyet** seçeneğini seçmek üzere filtreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="562dd-199">To select only costs or revenues for budget plan lines, use the filter to select **Budget updates: Amount type = Cost**.</span></span> <span data-ttu-id="562dd-200">Yalnızca bir tahmin türü seçmek için, **Bütçe güncelleştirmeleri: Hareket türü = *xxx*** seçeneğini seçmek üzere filtreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="562dd-200">To select only one type of forecast, use the filter to select **Budget updates: Transaction type = *xxx***.</span></span> 

<span data-ttu-id="562dd-201">Bir bütçe planı senaryosu oluşturmak için yalnızca bir tahmin modeli kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="562dd-201">Only one forecast model can be used to generate a budget plan scenario.</span></span> <span data-ttu-id="562dd-202">Bir tahmin modeli sürecini yürütüyorsanız ve daha sonra güncelleştirme yapıp başka bir model belirlemeye çalışırsanız, aynı proje ve genel muhasebe hesapları geçerli olduğu takdirde, ilk modelin üzerine yazılacaktır.</span><span class="sxs-lookup"><span data-stu-id="562dd-202">If you run the process for one forecast model, and then do an update and try to specify another model, the first model will be overwritten if the same project and ledger accounts apply.</span></span> <span data-ttu-id="562dd-203">Birden fazla tahmin modelinden bir bütçe planı senaryosu oluşturmak için, farklı bütçe planı senaryoları oluşturun ve bunları başka bir senaryoda birbirine eklemek için tahsisat seçeneklerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="562dd-203">To generate a budget plan scenario from more than one forecast model, generate into different budget plan scenarios, and use allocation options to add them together in another scenario.</span></span> 

<span data-ttu-id="562dd-204">**Proje tahminlerinden bütçe planı oluştur** işlemi de kaynak projeyi bütçe planı satırına atar.</span><span class="sxs-lookup"><span data-stu-id="562dd-204">The **Generate budget plan from project forecasts** process also assigns the source project to the budget plan line.</span></span>

### <a name="generate-budget-plan-from-supply-forecast"></a><span data-ttu-id="562dd-205">Tedarik tahmininden bütçe planı oluştur</span><span class="sxs-lookup"><span data-stu-id="562dd-205">Generate budget plan from supply forecast</span></span>

<span data-ttu-id="562dd-206">**Tedarik tahmininden bütçe planı oluştur** işlemindeki kaynak filtre seçenekleri, işlem ve işlev arasındaki benzerliklerden dolayı **Satınalma bütçesini genel muhasebeye aktar** işlevindeki seçeneklerden sonra modellenmiştir.</span><span class="sxs-lookup"><span data-stu-id="562dd-206">The source filter options in the **Generate budget plan from supply forecast** process were modeled after options in the **Transfer purchase budget to ledger** function, because of similarities between the process and the function.</span></span>

### <a name="generate-budget-plan-from-demand-forecast"></a><span data-ttu-id="562dd-207">Talep tahmininden bütçe planı oluştur</span><span class="sxs-lookup"><span data-stu-id="562dd-207">Generate budget plan from demand forecast</span></span>

<span data-ttu-id="562dd-208">**Talep tahmininden bütçe planı oluştur** işleminde, bütçe planında gelir satırları oluşturmak için **Satış siparişi** seçeneğini **Evet** olarak; gider satırları oluşturmak için **Tüketim** seçeneğini **Evet** olarak; veya her iki seçeneği **Evet** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-208">For the **Generate budget plan from demand forecast** process, you can set the **Sales order** option to **Yes** to generate revenue lines in the budget plan, set the **Consumption** to **Yes** to create expense lines, or set both options to **Yes**.</span></span>

### <a name="generate-budget-plan-from-budget-register-entries"></a><span data-ttu-id="562dd-209">Bütçe kaydı girişlerinden bütçe planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="562dd-209">Generate budget plan from budget register entries</span></span>

<span data-ttu-id="562dd-210">**Bütçe kayıt girişlerinden bütçe planı oluştur** işleminde, kaynak bir alt model, bir bütçe kodu ve bir giriş numarası belirtmelidir.</span><span class="sxs-lookup"><span data-stu-id="562dd-210">For the **Generate budget plan from budget register entries** process, the source must specify one submodel, one budget code, and one entry number.</span></span> <span data-ttu-id="562dd-211">Diğer bir deyişle, bir kerede yalnızca bir bütçe kayıt girişi için bütçe planı satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-211">In other words, you can create budget plan lines for only one budget register entry at a time.</span></span> <span data-ttu-id="562dd-212">İşlemi her kaynak girişi için bir kez yürüterek, aynı bütçe planında ilave girişler kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-212">You can use additional entries in the same budget plan by running the process one time for each source entry.</span></span>

### <a name="generate-budget-plan-from-budget-plan"></a><span data-ttu-id="562dd-213">Bütçe planından bütçe planı oluştur</span><span class="sxs-lookup"><span data-stu-id="562dd-213">Generate budget plan from budget plan</span></span>

<span data-ttu-id="562dd-214">**Bütçe planından bütçe planı oluştur** işleminde, **Hedef** öğesindeki ilave seçenekler kümesi, yeni mali boyutlar atamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="562dd-214">For the **Generate budget plan from budget plan** process, an additional set of options on the **Target** tab lets you assign new financial dimensions.</span></span> <span data-ttu-id="562dd-215">Mali boyut seçili ise, bu değer tüm bütçe planı satırları için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="562dd-215">If a financial dimension is selected, that value will be used for all budget plan lines.</span></span> <span data-ttu-id="562dd-216">Bu nedenle, bir bütçe planını diğer bütçe planları için temel olarak kullanabilir, aynı zamanda, örneğin, farklı bir departman veya maliyet merkezini yeni bütçe planlarına atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-216">Therefore, you can use one budget plan as the basis for other budget plans, but can also assign, for example, a different department or cost center to the new budget plans.</span></span>

## <a name="looking-back-from-the-budget-plan"></a><span data-ttu-id="562dd-217">Bütçe planından geriye bakış</span><span class="sxs-lookup"><span data-stu-id="562dd-217">Looking back from the budget plan</span></span>
### <a name="budget-plans-by-dimension-set-inquiry"></a><span data-ttu-id="562dd-218">Boyut kümesine göre bütçe planları sorgulaması</span><span class="sxs-lookup"><span data-stu-id="562dd-218">Budget plans by dimension set inquiry</span></span>

<span data-ttu-id="562dd-219">**Boyut kümesine göre bütçe planları** sorgulaması bütçe planı verilerinin kaynağını belirlemeye yardımcı olması için bir sorgu yürütmenize olanak sağlayan çeşitli seçenekler içerir.</span><span class="sxs-lookup"><span data-stu-id="562dd-219">The **Budget plans by dimension set** inquiry includes several options that let you run a query to help identify the source of the budget plan data.</span></span> 

<span data-ttu-id="562dd-220">Bir satırı seçin ve **Bütçe planı satırları** sorgulamasını çalıştırmak için **Bütçe planı satırları** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="562dd-220">Select a line and click the **Budget plan lines** button to run the **Budget plan lines** query.</span></span> <span data-ttu-id="562dd-221">Sonuçları seçili satırın boyut değerleri için filtrelenir.</span><span class="sxs-lookup"><span data-stu-id="562dd-221">The results are filtered for the dimension values of the selected line.</span></span> <span data-ttu-id="562dd-222">Daha sonra ek parametreler uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562dd-222">You can then apply additional parameters.</span></span> 

<span data-ttu-id="562dd-223">Bu sorgulamaları yürütmek için **Tedarik tahmini** ve **Talep tahmini** düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="562dd-223">Use the **Supply forecast** and **Demand forecast** buttons run these queries.</span></span> <span data-ttu-id="562dd-224">Her iki durumda da, sorgulama bütçe planı satırları oluşturmuş olabilecek tahmin satırlarını arar.</span><span class="sxs-lookup"><span data-stu-id="562dd-224">In both cases, the query searches for forecast lines that could have created the budget plan lines.</span></span> 

<span data-ttu-id="562dd-225">Mevcut ek raporlar **Bütçe planına göre tahmin konumları** raporunu içerir.</span><span class="sxs-lookup"><span data-stu-id="562dd-225">Additional reports that are available include the **Forecast positions by budget plan** report.</span></span> <span data-ttu-id="562dd-226">Bu rapor bilhassa bir konumun bütçe planlarına doğru şekilde tahsis edilip edilmediğini belirlemek istediğinizde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="562dd-226">This report is especially useful when you want to determine whether a position has been correctly allocated to budget plans.</span></span>



