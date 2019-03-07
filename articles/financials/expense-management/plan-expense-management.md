---
title: Gider yönetimini yapılandır
description: Bu makalede, Microsoft Dynamics 365 for Finance and Operations'te Gider yönetimini yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ac9959a4ee66e52ead5050897403602e407ca10
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "322042"
---
# <a name="configure-expense-management"></a><span data-ttu-id="22ccc-103">Gider yönetimini yapılandır</span><span class="sxs-lookup"><span data-stu-id="22ccc-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22ccc-104">Bu konuda, Microsoft Dynamics 365 for Finance and Operations'te Gider yönetimini yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="22ccc-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="22ccc-105">Gider yönetiminde, ödeme yöntemleri, seyahat talepleri, gider raporları, ilkeler vb. hakkındaki bilgileri saklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22ccc-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="22ccc-106">Gider yönetiminizin yapılandırmasını planlarken aldığınız pek çok karar kuruluşunuzun hiyerarşisi ve mali yapısına dayandığından, bu alanlar için planlama belgelerine başvurmalısınız.</span><span class="sxs-lookup"><span data-stu-id="22ccc-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="22ccc-107">Şirketlerarası giderler</span><span class="sxs-lookup"><span data-stu-id="22ccc-107">Intercompany expenses</span></span>

<span data-ttu-id="22ccc-108">Şirketlerarası giderleri etkinleştirdiğinizde, kuruluşunuz içindeki istihdam tüzel kişiliğine ve çalışanlara, kuruluşunuzdaki başka tüzel kişilikler adına masraf yapma ve ödeme tahsil etme izni verirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22ccc-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="22ccc-109">Örneğin, tüzel kişilik A içindeki bir çalışan, tüzel kişilik B için bir projeyi tamamlar ve proje, seyahate ilişkin giderlerde ortaya çıkarır.</span><span class="sxs-lookup"><span data-stu-id="22ccc-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="22ccc-110">Şirketlerarası giderler etkinleştirilmişse, çalışan gideri tüzel kişilik B'ye nakledecek bir gider raporu oluşturabilir ve gider tüzel varlık A tarafından ödenmelidir. Eğer kuruluşunuzun çok sayıda tüzel kişiliği yoksa, şirketlerarası giderleri etkinleştirmenize ihtiyaç yoktur.</span><span class="sxs-lookup"><span data-stu-id="22ccc-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="22ccc-111">**Karar:** Şirketlerarası giderleri etkinleştirmek istiyor musunuz?</span><span class="sxs-lookup"><span data-stu-id="22ccc-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="22ccc-112">Mali yönetim</span><span class="sxs-lookup"><span data-stu-id="22ccc-112">Financial management</span></span>

<span data-ttu-id="22ccc-113">Gider Yönetimi, organizasyonunuzun mali yönetimi ile sıkı sıkıya tümleşiktir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="22ccc-114">Gider yönetimi yapılandırmanızın pek çoğu, kuruluşunuzun mali yapısı hakkında almış olduğunuz kararları temel alır.</span><span class="sxs-lookup"><span data-stu-id="22ccc-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="22ccc-115">Aşağıdaki bölümler kuruluşunuzun mali kararları ve liderlik ekibinizin yönlendirmesi ile planlamaya ve karar almaya ihtiyaç duyulan çeşitli alanları açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="22ccc-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="22ccc-116">Harcırahlar</span><span class="sxs-lookup"><span data-stu-id="22ccc-116">Per diems</span></span>

<span data-ttu-id="22ccc-117">Kuruluşunuzun sağladığı çalışan harcırahlarını tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="22ccc-118">Harcırahlar genellikle yemek, konaklama ve diğer arızi giderler gibi giderleri karşılamak için kullanıldığından, kuruluşunuzun sunduğu harcırah tahsisatları için kurallar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22ccc-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="22ccc-119">harcırah oranları seyahatin yılın hangi döneminde yapıldığı, seyahat yeri veya her ikisine dayanarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="22ccc-120">Bir harcırah kuralı tanımlarken, harcırahın çalışana ek yemek veya hizmetler sunulduğunda stopaj uygulanacak bir yüzdesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22ccc-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="22ccc-121">Ayrıca, çalışan seyahat ettiği durumlarda uygulanacak, harcırahın sağlanacağı minimum ve maksimum saatler için harcırah katmanları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22ccc-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="22ccc-122">**Kararlar:**</span><span class="sxs-lookup"><span data-stu-id="22ccc-122">**Decisions:**</span></span>

- <span data-ttu-id="22ccc-123">İlk ve son günler için varsayılan harcırah kuralları:</span><span class="sxs-lookup"><span data-stu-id="22ccc-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="22ccc-124">Çalışanın bir gün için talep edebileceği ve yine de harcırah alabileceği en az saat sayısı kaçtır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="22ccc-125">Yemek için ilk gün ve son günde teklif edilen tutarda bir düşüş var mıdır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="22ccc-126">Bir azaltma varsa, azaltmanın yüzdesi nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="22ccc-127">Otel için ilk gün ve son günde teklif edilen tutarda bir düşüş var mıdır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="22ccc-128">Bir azaltma varsa, azaltmanın yüzdesi nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="22ccc-129">İlk günde ve son günde oluşabilecek diğer masraflar için tutarda yapılacak bir düşüş var mıdır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="22ccc-130">Bir azaltma varsa, azaltmanın yüzdesi nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="22ccc-131">Varsayılan harcırah kuralları:</span><span class="sxs-lookup"><span data-stu-id="22ccc-131">Default per diem rules:</span></span>

    - <span data-ttu-id="22ccc-132">Örneğin yemek ücretsiz ise, her bir öğün için harcırahta yapılacak bir indirim yüzdesi mevcut mudur?</span><span class="sxs-lookup"><span data-stu-id="22ccc-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="22ccc-133">Bir azaltma varsa, her bir öğün için azaltmanın yüzdesi nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="22ccc-134">Yiyecek indirimi günlük, seyahat başına veya günlük öğün sayısına göre mi hesaplanır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="22ccc-135">Harcırah tutarları normal biçimde mi yukarı mı yuvarlanacaktır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="22ccc-136">Harcırahlar 24 saatlik dönemlere göre mi takvim gününe göre mi hesaplanır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="22ccc-137">Konuma bağlı harcırah kuralları:</span><span class="sxs-lookup"><span data-stu-id="22ccc-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="22ccc-138">Harcırah oranlarını konuma göre farklılık gösterir mi?</span><span class="sxs-lookup"><span data-stu-id="22ccc-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="22ccc-139">Hangi konumlar dahildir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-139">What locations are included?</span></span>
    - <span data-ttu-id="22ccc-140">Harcırah oranları konuma göre değişiyorsa, her konum için, aşağıdaki türde maliyetler için hangi yüzde tutarı sağlanır:</span><span class="sxs-lookup"><span data-stu-id="22ccc-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="22ccc-141">Yemekler</span><span class="sxs-lookup"><span data-stu-id="22ccc-141">Meals</span></span>
        - <span data-ttu-id="22ccc-142">Otel</span><span class="sxs-lookup"><span data-stu-id="22ccc-142">Hotel</span></span>
        - <span data-ttu-id="22ccc-143">Diğer giderler</span><span class="sxs-lookup"><span data-stu-id="22ccc-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="22ccc-144">Gider yönetimi günlükleri ve hesapları</span><span class="sxs-lookup"><span data-stu-id="22ccc-144">Expense management journals and accounts</span></span>

<span data-ttu-id="22ccc-145">Gider Yönetimi birden fazla günlükler ve hesaplar kullanmanızı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="22ccc-146">Örneğin nakit avanslar veya kredi kartı anlaşmazlıkları için aynı hesabın mı kullanılacağına karar vermeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="22ccc-147">**Kararlar:**</span><span class="sxs-lookup"><span data-stu-id="22ccc-147">**Decisions:**</span></span>

- <span data-ttu-id="22ccc-148">Hangi genel muhasebe günlükleri gider raporlarının nakledilmesi için onaylanmıştır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="22ccc-149">Nakit avanslar için hangi hesap kullanılır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="22ccc-150">Nakit avanslar deftere hemen nakledilmeli mi?</span><span class="sxs-lookup"><span data-stu-id="22ccc-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="22ccc-151">Ödeme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="22ccc-151">Payment methods</span></span>

<span data-ttu-id="22ccc-152">Çalışanlarınızın işletmeniz adına giderde bulunmasına izin verirseniz, çalışanlarınızın kullanabileceği ödeme yöntemlerini tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="22ccc-153">Örneğin, çalışanların nakit veya şirket kredi kartını kullanmasına izin verebilir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="22ccc-154">Ayrıca çalışanların kişisel kredi kartları kullanıp bunları geri ödemesini daha sonra almalarına da izin verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22ccc-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="22ccc-155">İzin verdiğininiz her ödeme yöntemi için aşağıdaki kararları almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="22ccc-156">**Kararlar:**</span><span class="sxs-lookup"><span data-stu-id="22ccc-156">**Decisions:**</span></span>

- <span data-ttu-id="22ccc-157">Hangi ödeme yöntemlerine izin verilir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="22ccc-158">Ödeme yöntemi giderlerine kim sahiptir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="22ccc-159">Mahsup hesap türü var mıdır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-159">Is there an offset account type?</span></span> <span data-ttu-id="22ccc-160">Mahsup hesap türü varsa, hesap nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="22ccc-161">Mahsup hesap varsa, hesap nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="22ccc-162">Ödeme yöntemi kredi kartı ise, ödeme yöntemi sadece içe aktarılan hareketler ile mi kullanılacaktır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="22ccc-163">Gider kategorileri ve paylaşılan kategoriler</span><span class="sxs-lookup"><span data-stu-id="22ccc-163">Expense categories and shared categories</span></span>

<span data-ttu-id="22ccc-164">Çalışanlar bir gider raporu oluşturduklarında, kaydettikleri her gider bir gider kategorisi ile ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="22ccc-165">Gider kategorileri, kuruluşunuzdaki tüzel kişilikler arasında paylaşılabilen paylaşımlı kategorilerden türetilmiştir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="22ccc-166">Bu kategoriler ayrıca Proje yönetimi ve muhasebede de paylaşılmış olabilir, kuruluşunuzun nasıl tanımlı olduğuna bağlı olarak.</span><span class="sxs-lookup"><span data-stu-id="22ccc-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="22ccc-167">Kuruluşunuzun tanımına ve uygulama ekibinin rehberliği doğrultusunda, Gider yönetiminde kullanılan kategorilerin sadece Gider yönetimi için mi yoksa Proje yönetimi ve muhasebe ve Gider yönetimi ile paylaşımlı olarak mı kullanılacağını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="22ccc-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="22ccc-168">Bu kategorilerin Proje ve Gider veya Proje ve Üretim arasında paylaşılmış olabileceğini unutmayın, Gider ve Üretim arasında değil.</span><span class="sxs-lookup"><span data-stu-id="22ccc-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="22ccc-169">Her gider kategorisi için aşağıdaki kararları almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="22ccc-170">**Kararlar:**</span><span class="sxs-lookup"><span data-stu-id="22ccc-170">**Decisions:**</span></span>

- <span data-ttu-id="22ccc-171">Gider kategorisi nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-171">What is the expense category?</span></span> <span data-ttu-id="22ccc-172">Örneklere uçuşlar, otel ve mesafe kategorileri dahildir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="22ccc-173">Gider kategorisi ayrıca Proje yönetimi ve muhasebede de kullanılabilir mi?</span><span class="sxs-lookup"><span data-stu-id="22ccc-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="22ccc-174">Gider türü nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-174">What is the expense type?</span></span>
- <span data-ttu-id="22ccc-175">Gider kategorisi için varsayılan ödeme yöntemi nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="22ccc-176">Gider kategorisindeki maliyetlerin maddeleştirilmesi gerekiyor mu?</span><span class="sxs-lookup"><span data-stu-id="22ccc-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="22ccc-177">Gider kategorisi için ana varsayılan hesap nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="22ccc-178">Gider kategorisi için varsayılan madde satış vergi grubu nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="22ccc-179">Gider kategorisi için ek ödeme yöntemlerine izin verilir mi?</span><span class="sxs-lookup"><span data-stu-id="22ccc-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="22ccc-180">Ek ödeme yöntemlerine izin veriliyorsa, bunlar nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="22ccc-181">Bu gider kategorisinde alt kategoriler var mıdır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="22ccc-182">Alt kategoriler varsa, aşağıdaki kararları vermeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="22ccc-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="22ccc-183">Herhangi bir alt kategori vergiden düşmeye hariç midir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="22ccc-184">Alt kategorilerin madde satış vergi grubu nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="22ccc-185">Gider kategorisi ayrıca Proje yönetimi ve muhasebede de kullanılıyorsa, kalan soruları da yanıtlayın.</span><span class="sxs-lookup"><span data-stu-id="22ccc-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="22ccc-186">Aksi taktirde, sonraki bölüme geçin.</span><span class="sxs-lookup"><span data-stu-id="22ccc-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="22ccc-187">Aşağıdaki giderler için hangi maliyet hesapları kullanılacaktır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="22ccc-188">Maliyet</span><span class="sxs-lookup"><span data-stu-id="22ccc-188">Cost</span></span>
    - <span data-ttu-id="22ccc-189">Bordro tahsisatı</span><span class="sxs-lookup"><span data-stu-id="22ccc-189">Payroll allocation</span></span>
    - <span data-ttu-id="22ccc-190">Süren iş - maliyet değeri</span><span class="sxs-lookup"><span data-stu-id="22ccc-190">WIP-cost value</span></span>
    - <span data-ttu-id="22ccc-191">Maliyet-madde</span><span class="sxs-lookup"><span data-stu-id="22ccc-191">Cost-item</span></span>
    - <span data-ttu-id="22ccc-192">Süren iş - maliyet değeri - madde</span><span class="sxs-lookup"><span data-stu-id="22ccc-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="22ccc-193">Tahakkuk eden zarar</span><span class="sxs-lookup"><span data-stu-id="22ccc-193">Accrued loss</span></span>
    - <span data-ttu-id="22ccc-194">Süren iş - tahakkuk eden zarar</span><span class="sxs-lookup"><span data-stu-id="22ccc-194">WIP-accrued loss</span></span>

- <span data-ttu-id="22ccc-195">Aşağıdakiler için hangi gelir hesapları kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="22ccc-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="22ccc-196">Faturalanmış gelir</span><span class="sxs-lookup"><span data-stu-id="22ccc-196">Invoiced revenue</span></span>
    - <span data-ttu-id="22ccc-197">Tahakkuk eden gelir - satış değeri</span><span class="sxs-lookup"><span data-stu-id="22ccc-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="22ccc-198">Süren iş - satış değeri</span><span class="sxs-lookup"><span data-stu-id="22ccc-198">WIP-sales value</span></span>
    - <span data-ttu-id="22ccc-199">Tahakkuk eden gelir - üretim</span><span class="sxs-lookup"><span data-stu-id="22ccc-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="22ccc-200">Süren iş - üretim</span><span class="sxs-lookup"><span data-stu-id="22ccc-200">WIP-production</span></span>
    - <span data-ttu-id="22ccc-201">Tahakkuk eden gelir - kar</span><span class="sxs-lookup"><span data-stu-id="22ccc-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="22ccc-202">Süren iş - kar</span><span class="sxs-lookup"><span data-stu-id="22ccc-202">WIP-profit</span></span>
    - <span data-ttu-id="22ccc-203">Tahakkuk eden gelir - abonelik</span><span class="sxs-lookup"><span data-stu-id="22ccc-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="22ccc-204">Süren iş - abonelik</span><span class="sxs-lookup"><span data-stu-id="22ccc-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="22ccc-205">Vergiler</span><span class="sxs-lookup"><span data-stu-id="22ccc-205">Taxes</span></span>

<span data-ttu-id="22ccc-206">Giderlerle ilgili vergiler için, gider raporlarına nelerin dahil edileceğini veya etkinleştirileceğini belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="22ccc-207">**Kararlar:**</span><span class="sxs-lookup"><span data-stu-id="22ccc-207">**Decisions:**</span></span>

- <span data-ttu-id="22ccc-208">Gider tutarlarına satış vergisi dahil midir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="22ccc-209">Giderler üzerinde vergiden düşme etkinleştirilecek midir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="22ccc-210">Genel muhasebeyi planladığınızda, ABD satış vergisi ve kullanım vergisi kurallarını uygulamaya karar verdiyseniz, giderler üzerinde vergiden düşmeyi etkinleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="22ccc-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="22ccc-211">(ABD satış vergisi ve kullanım vergisi kurallarını uygulamak için **Satış vergisi vergilendirme kuralları uygula** seçeneğini **Evet** olarak ayarlayın.)</span><span class="sxs-lookup"><span data-stu-id="22ccc-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="22ccc-212">İlkeler</span><span class="sxs-lookup"><span data-stu-id="22ccc-212">Policies</span></span>

<span data-ttu-id="22ccc-213">Gider raporu ilkeleri oluşturarak kuruluşunuzun, çalışanlar kendisi adına giderler oluşturduklarında vakit ve paradan tasarruf etmesine yardımcı olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22ccc-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="22ccc-214">İlkeler çalışanların bir bütçeye sadık kalmalarını, gerekli tüm bilgileri sağlamalarını ve sadece gerektiğinde para harcamalarını garanti etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="22ccc-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="22ccc-215">Her bir gider raporu ilkesini ve gider raporu onay ilkesini oluşturduğunuzda aşağıdaki kararları almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="22ccc-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="22ccc-216">**Kararlar:**</span><span class="sxs-lookup"><span data-stu-id="22ccc-216">**Decisions:**</span></span>

- <span data-ttu-id="22ccc-217">İlkenin adı nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-217">What is the name of the policy?</span></span>
- <span data-ttu-id="22ccc-218">Gider ilkesi ne içindir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-218">What is the expense policy for?</span></span>
- <span data-ttu-id="22ccc-219">Eğer daha önceden şirketlerarası giderleri etkinleştirme kararı aldıysanız, bu ilke kuruluşunuzdaki hangi şirketlere uygulanır?</span><span class="sxs-lookup"><span data-stu-id="22ccc-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="22ccc-220">İlke zaman etkili olur?</span><span class="sxs-lookup"><span data-stu-id="22ccc-220">When does the policy become effective?</span></span>
- <span data-ttu-id="22ccc-221">İlke ne zaman sona?</span><span class="sxs-lookup"><span data-stu-id="22ccc-221">When does the policy expire?</span></span>
- <span data-ttu-id="22ccc-222">İlke kuralı nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-222">What is the policy rule?</span></span>
- <span data-ttu-id="22ccc-223">İlke kuralının sonucu nedir?</span><span class="sxs-lookup"><span data-stu-id="22ccc-223">What is the outcome of the policy rule?</span></span>
