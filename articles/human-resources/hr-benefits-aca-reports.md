---
title: Uygun Bakım Yasası (ACA) raporları oluşturma
description: Ekonomik Bakım Yasası (ACA) raporlaması, Ekonomik Bakım Yasası'nın **İşveren İçin Zorunlu** kısmını desteklemek için 1095-B ve 1095-C formlarını oluşturur.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1091460ee1996b944b760f3771007bd2a26666a9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053213"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="8b153-103">ACA raporları oluşturma</span><span class="sxs-lookup"><span data-stu-id="8b153-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8b153-104">Ekonomik Bakım Yasası (ACA) raporlaması, Ekonomik Bakım Yasası'nın **İşveren İçin Zorunlu** kısmını desteklemek için 1095-B ve 1095-C formlarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b153-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="8b153-105">ACA raporlaması yalnızca ABD'deki tüzel kişiler için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8b153-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="8b153-106">Başlarken</span><span class="sxs-lookup"><span data-stu-id="8b153-106">Getting started</span></span>

<span data-ttu-id="8b153-107">1095-B ve 1095-C formlarının bilgilerini izlemek için önce bir veya daha fazla Ekonomik bakım kapsamı grubu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8b153-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="8b153-108">Ekonomik Bakım kapsamı grupları şunları gösterir:</span><span class="sxs-lookup"><span data-stu-id="8b153-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="8b153-109">Bir çalışan için kapsam teklifi</span><span class="sxs-lookup"><span data-stu-id="8b153-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="8b153-110">Maliyet federal yoksulluk sınırının üzerindeyse, çalışanın en düşük maliyetli aylık prim payı</span><span class="sxs-lookup"><span data-stu-id="8b153-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="8b153-111">Varsa işveren tarafından kullanılan Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="8b153-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="8b153-112">Ekonomik Bakım kapsamı grupları, koşulların aynı olduğu her çalışan kaydını değiştirmeden bu alanların bilgilerini yönetmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="8b153-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="8b153-113">Sayfadaki **Toplu atama** seçeneğini kullanarak bir veya daha fazla çalışana Ekonomik Bakım karşılama gruplarını kolayca atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="8b153-114">Bir kapsama grubunun birden fazla sürümünü tutmak</span><span class="sxs-lookup"><span data-stu-id="8b153-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="8b153-115">Bir kapsama grubunun birden fazla sürümünü tutabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="8b153-116">Bu işlevsellik, yeni bir grup oluşturmanıza ve çalışanları yeniden atamanıza gerek kalmadan değişiklik yapmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="8b153-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="8b153-117">ACA kapsama grupları oluşturduktan sonra, **Toplu atama** seçeneğiyle grupları çalışanlara toplu olarak atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="8b153-118">Ayrıca, ACA bilgilerinin izlenip izlenmeyeceğini ve raporlanıp raporlanmayacağını, bir çalışanın Ekonomik Bakım kapsamı grubuna atanıp atanmayacağını ayrı ayrı belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="8b153-119">Yarı zamanlı çalışanlar gibi bazı ACA kapsam bilgilerini izlemeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="8b153-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="8b153-120">Bu durumda, **Rapor kapsamı** alanını **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8b153-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="8b153-121">İzlenebilir ACA bilgilerine sahip her çalışanı Ekonomik Bakım kapsama grubuna atamanız gerekse de aşağıdaki seçenekleri aylar için farklı değerlerle değiştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="8b153-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="8b153-122">**Kapsam teklifi**</span><span class="sxs-lookup"><span data-stu-id="8b153-122">**Offer of coverage**</span></span>
- <span data-ttu-id="8b153-123">**Personel maliyet payı**</span><span class="sxs-lookup"><span data-stu-id="8b153-123">**Employee share of cost**</span></span>
- <span data-ttu-id="8b153-124">**Güvenli Liman**</span><span class="sxs-lookup"><span data-stu-id="8b153-124">**Safe Harbor**</span></span>

<span data-ttu-id="8b153-125">Ekonomik Bakım kapsamı grubu değerleri için özel durumlar girmek üzere, **İstihdam sekmesindeki** **Ek bilgiler** bölümünün altındaki **Çalışan ayrıntısı** sayfasında **Ekonomik Bakım Kapsamı** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="8b153-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="8b153-126">Sağlık bakımı kapsamasını raporlama</span><span class="sxs-lookup"><span data-stu-id="8b153-126">Reporting health care coverage</span></span>

<span data-ttu-id="8b153-127">Tam zamanlı çalışanlara sunulan sağlık sigortası kapsamını izlemenin yanı sıra işveren, çalışanın kayıtlı olduğu işveren destekli kendi kaynaklarından teminat ayırmayla sigortalı sağlık kapsamı sunuyorsa (istihdam durumlarının tam zamanlı veya yarı zamanlı olmasına bakılmaksızın), 1095-C hakkında ek bilgilerin bildirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="8b153-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="8b153-128">İşveren tarafından desteklenen kazanç planları tarafından kapsanan her personelin (bakmakla yükümlü olduğu kişi dahil), kapsanmış oldukları aylar için rapora dahil edilmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="8b153-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="8b153-129">**ACA raporlanabilir** onay kutusunu seçerek her yan hak planının raporlanıp raporlanmayacağını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="8b153-130">Ayrıca, çalışanlar bakmakla yükümlü olduğu kişilerden herhangi birinin bir sosyal hak kapsamında olmasını seçtiyse, yükümlü oldukları her çalışan için kapsadığı tarihleri **Sosyal hakları koru** sayfasında belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="8b153-131">Bakmakla yükümlü olunan kişinin sosyal hak altında olduğunu belirtmek için **Bakılmakla Yükümlü Olunan Kişiler** hızlı sekmesinin eylem bölmesinde **Düzenle** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8b153-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="8b153-132">**Bakılmakla yükümlü kapsama veri yöneticisi** sayfası üzerinde, bakılmakla yükümlü kişinin kazanç tarafından kapsandığı tarihi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="8b153-133">Bu sayfaya tarihler girmek, **Kazançları koru** sayfası üzerindeki **Kapsanan** onay kutusunu otomatik seçer.</span><span class="sxs-lookup"><span data-stu-id="8b153-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="8b153-134">1095-B ve 1095-C formları oluşturma</span><span class="sxs-lookup"><span data-stu-id="8b153-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="8b153-135">Ayrıca ürünün içinden 1095-B ve 1095-C formları oluşturabilir ve bunları çalışanlarınızın her birine dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="8b153-136">Sistem ayrıca elektronik olarak 1095-C formları ve 1094-C IRS iletim dosyaları üretebilir.</span><span class="sxs-lookup"><span data-stu-id="8b153-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="8b153-137">1095-C formunu oluştururken, uygun vergi yılını girin ve sosyal güvenlik numaralarının maskelenip maskelenmemesi gerektiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8b153-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="8b153-138">500'den fazla çalışan için 1095-C formları yazdırıyorsanız birden fazla PDF dosyası alırsınız.</span><span class="sxs-lookup"><span data-stu-id="8b153-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="8b153-139">**Belge yönetimi parametreleri** penceresindeki **Maksimum dosya boyutu**'nu 150 MB'a artırmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="8b153-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="8b153-140">Görüntüleme bilgisi</span><span class="sxs-lookup"><span data-stu-id="8b153-140">Viewing information</span></span>

<span data-ttu-id="8b153-141">**Çalışan Ekonomik Bakım kapsamı** sayfasını, hangi personellerin her bir kapsama grubuna atandığını, hangi personellerin bir rapora dahil edilmesi gerekmediğini ve hangi personellerin atanmamış olduğunu görmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="8b153-142">Ekonomik Bakım kapsama grubundaki varsayılan değerlerden herhangi biri geçersiz kılınmışsa değiştirilen değerin yanında bir yıldız işareti görünür.</span><span class="sxs-lookup"><span data-stu-id="8b153-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="8b153-143">12 ayın tamamı için değerler aynı ise ve geçersiz kılınmamışsa, değer **Tüm 12 ay** sütununda yazdırılır.</span><span class="sxs-lookup"><span data-stu-id="8b153-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="8b153-144">Ayrıca, hangi çalışanların ACA raporuna dahil edilemeyecek olarak işaretlendiğini anlamak için sorgulama penceresini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="8b153-145">Kapsamın kendilerine sunulup sunulmadığını izlemenize gerek yoktur ve yıl sonunda onlara 1095-C yayınlamanıza gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="8b153-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="8b153-146">1095-C almayan tüm çalışanların listesini oluşturmak için **Filtreleme ölçütü** alanında **Raporlanabilir Değil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8b153-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="8b153-147">Ayrıca, atanmamış (**ACA Raporu kapsamı** alanı boş) veya **Yıl** alanında seçilen yıl için süresi dolmuş bir Ekonomik Bakım kapsama grubuna atanmış çalışanları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="8b153-148">Filtreleme seçeneklerinden herhangi birini kullanarak oluşturulan personel listelerini Excel'e aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="8b153-149">Kendi kaynaklarından teminat ayırmayla sigorta kapsamı sağladığınız için kapsanan kişileri bildirmeniz gerekiyorsa **ACA raporlanabilir** olarak işaretlenmiş sosyal hak planları kapsamındaki bakılmakla yükümlü olunan kişileri görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b153-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="8b153-150">Eylem bölmesinde **Bakılmakla yükümlü olunan kişi kapsamını görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b153-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="8b153-151">Sorgulama penceresinde yalnızca **ACA raporlanabilir** olarak işaretlenmiş sosyal hak planları görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="8b153-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]