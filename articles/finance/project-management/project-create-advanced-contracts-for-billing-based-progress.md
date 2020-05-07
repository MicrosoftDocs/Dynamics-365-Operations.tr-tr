---
title: İlerlemeye göre faturalama için gelişmiş sözleşmeler oluşturma
description: Bu konu, tamamlanan çalışmanın yüzdesine göre müşteriler için fatura oluşturabilmek amacıyla proje sözleşmelerinin nasıl oluşturulacağını açıklar.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282853"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="209d1-103">İlerlemeye göre faturalama için gelişmiş sözleşmeler oluşturma</span><span class="sxs-lookup"><span data-stu-id="209d1-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="209d1-104">Bu konu, tamamlanan çalışmanın yüzdesine göre müşteriler için fatura oluşturabilmek amacıyla proje sözleşmelerinin nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="209d1-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="209d1-105">Fatura tutarları, proje için ayarladığınız çalışmanın bütçe kategorileri için otomatik olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="209d1-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="209d1-106">Fatura zamanlaması, müşteriyle proje sözleşmesini görüşmeniz sırasında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="209d1-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="209d1-107">Bu konudaki yordamları bir sözleşme, ilişkili proje ve proje için ayarladığınız çalışmanın bütçe kategorileri için fatura tutarlarını hesaplamakta kullanılan faturalama kurallarını ayarlamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="209d1-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="209d1-108">Sözleşmeyi ve projeyi oluşturduktan sonra, projenin ayrıntılarını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="209d1-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="209d1-109">Örneğin, faaliyetleri tanımlayabilir ve projeye çalışan atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="209d1-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="209d1-110">Örnek</span><span class="sxs-lookup"><span data-stu-id="209d1-110">Example</span></span>

<span data-ttu-id="209d1-111">Kuruluşunuz bir yazılım geliştirme firması.</span><span class="sxs-lookup"><span data-stu-id="209d1-111">Your organization is a software development firm.</span></span> <span data-ttu-id="209d1-112">Bir müşteri için, 20.000 ABD Doları (USD) toplam ücret karşılığında bir muhasebe bordro paketi geliştirmeyi kabul ediyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="209d1-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="209d1-113">Kuruluşunuz, projenin belirli yüzdelerini tamamladığınızda, müşteriye fatura yapmayı kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="209d1-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="209d1-114">İş için aşağıdaki proje kategorilerini ayarlarsınız, böylece bunları faturalandırma sürecinde kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="209d1-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="209d1-115">Danışmanlık</span><span class="sxs-lookup"><span data-stu-id="209d1-115">Consulting</span></span>
- <span data-ttu-id="209d1-116">Tasarla</span><span class="sxs-lookup"><span data-stu-id="209d1-116">Design</span></span>
- <span data-ttu-id="209d1-117">Yükleme</span><span class="sxs-lookup"><span data-stu-id="209d1-117">Installation</span></span>

<span data-ttu-id="209d1-118">Her kategori için tamamlanan proje çalışma yüzdesi için fatura tutarlarını otomatik olarak hesaplayacak faturalama kurallarını da ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="209d1-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="209d1-119">Bütçe yöneticisi proje kategorileri için bir bütçe oluşturur.</span><span class="sxs-lookup"><span data-stu-id="209d1-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="209d1-120">Tamamlanan çalışmanın tutarı otomatik olarak, bütçelenen tutarlarla karşılaştırılan fiili çalışma yüzdesi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="209d1-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="209d1-121">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="209d1-121">Prerequisites</span></span>

<span data-ttu-id="209d1-122">Faturalama kuralları kullanan bir proje oluşturmadan önce, fatura kuralları için numara serilerini ve hak ediş bazında faturalamayı deftere nakletmek için kullanılan bir ücret günlüğü ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="209d1-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="209d1-123">**Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="209d1-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="209d1-124">**Proje yönetimi ve muhasebe parametreleri** sayfasında, **Numara serileri** sekmesinde, ödeme kuralları oluşturulurken kullanmak istediğiniz numara sırasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="209d1-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="209d1-125">**Proje yönetimi ve muhasebe** \> **Günlükler** \> **Ücret**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="209d1-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="209d1-126">**Ücret günlüğü** sayfasında, **Yeni**'yi seçin ve günlük adını girin.</span><span class="sxs-lookup"><span data-stu-id="209d1-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="209d1-127">Hak ediş bazında faturalama için sözleşme oluşturma</span><span class="sxs-lookup"><span data-stu-id="209d1-127">Create a contract for progress billings</span></span>

<span data-ttu-id="209d1-128">Sabit fiyatlı bir proje için proje sözleşmesi oluşturmak için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="209d1-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="209d1-129">Projedeki tamamlanan iş belirtilen yüzdeye ulaştığında proje faturası oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="209d1-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="209d1-130">**Proje yönetimi ve muhasebe** \> **Projeler** \> **Proje sözleşmeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="209d1-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="209d1-131">**Proje sözleşmeleri** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="209d1-132">**Yeni proje sözleşmesi** iletişim kutusunda, aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="209d1-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="209d1-133">**Dosya Adı**</span><span class="sxs-lookup"><span data-stu-id="209d1-133">**Name**</span></span>
    - <span data-ttu-id="209d1-134">**Finansman türü**</span><span class="sxs-lookup"><span data-stu-id="209d1-134">**Funding type**</span></span>
    - <span data-ttu-id="209d1-135">**Finansman kaynağı**</span><span class="sxs-lookup"><span data-stu-id="209d1-135">**Funding source**</span></span>
    - <span data-ttu-id="209d1-136">**Satış para birimi** – Varsayılan olarak bu para birimi proje sözleşmesiyle ilişkilendirilen müşteri faturaları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="209d1-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="209d1-137">Ancak, belirli bir müşteri faturasındaki satış para birimini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="209d1-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="209d1-138">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-138">Select **OK**.</span></span> <span data-ttu-id="209d1-139">Bilgiler **Proje sözleşmeleri** sayfasının başlığına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="209d1-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="209d1-140">**Proje sözleşmeleri** sayfasında, proje için gerekli olan diğer bilgileri doldurun.</span><span class="sxs-lookup"><span data-stu-id="209d1-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="209d1-141">Hak ediş bazında faturalama için proje oluşturma</span><span class="sxs-lookup"><span data-stu-id="209d1-141">Create a project for progress billings</span></span>

<span data-ttu-id="209d1-142">Proje sözleşmesiyle ilişkili proje ve alt projeler oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="209d1-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="209d1-143">**Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="209d1-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="209d1-144">**Tüm projeler** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="209d1-145">**Yeni proje** iletişim kutusunda **Proje türü** alanında, **Zaman ve malzeme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="209d1-146">Proje grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-146">Select a project group.</span></span> <span data-ttu-id="209d1-147">Proje grubu, gruba atanan projelerle ilgili deftere nakil bilgilerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="209d1-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="209d1-148">**Proje oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-148">Select **Create project**.</span></span>
6. <span data-ttu-id="209d1-149">Proje oluşturulduktan sonra, proje aşamasını **Sürüyor** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="209d1-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="209d1-150">Proje için bütçe oluşturma</span><span class="sxs-lookup"><span data-stu-id="209d1-150">Create a budget for a project</span></span>

<span data-ttu-id="209d1-151">Bütçe kategorileri, her kategori için tamamlanan çalışma yüzdesi için fatura tutarlarını otomatik olarak hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="209d1-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="209d1-152">Tahmini maliyetler için bütçe kategorileri oluşturmak üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="209d1-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="209d1-153">**Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="209d1-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="209d1-154">**Tüm projeler** sayfasında, istediğiniz projeyi seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="209d1-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="209d1-155">**Projeler** sayfasında, Eylem bölmesinde, **Plan** sekmesinde, **Bütçe** grubunda **Proje bütçesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="209d1-156">**Proje bütçesi** sayfasında, projedeki her kategori için tahmini bir maliyet girin.</span><span class="sxs-lookup"><span data-stu-id="209d1-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="209d1-157">Hak ediş bazında faturalama için fatura kuralları oluşturma</span><span class="sxs-lookup"><span data-stu-id="209d1-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="209d1-158">**Proje yönetimi ve muhasebe** \> **Projeler** \> **Proje sözleşmeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="209d1-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="209d1-159">**Proje sözleşmeleri** sayfasında, bir proje sözleşmesi seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="209d1-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="209d1-160">Proje sözleşmesi sayfasında, **Faturalama kuralları** hızlı sekmesinde, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="209d1-161">**Faturalama kuralı** sayfasında, **Satır türü** alanında, **İlerleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="209d1-162">**Faturalama kuralı satırı ayrıntıları** hızlı sekmesinde, **Sözleşme değeri** alanına sözleşmenin toplam değerini girin.</span><span class="sxs-lookup"><span data-stu-id="209d1-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="209d1-163">**Kategori** alanında, ücret hareketini deftere nakletmek için kategoriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="209d1-164">**Proje** alanında, bu fatura kuralını kullanan projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="209d1-165">İsteğe bağlı: Faturalama kuralını ek projelere atayın.</span><span class="sxs-lookup"><span data-stu-id="209d1-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="209d1-166">**Proje** hızlı sekmesinde, **Kullanılabilir projeler** bölümünde bir proje seçin ve sonra projeyi **Seçili projeler** bölümüne eklemek için sağ ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="209d1-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="209d1-167">İsteğe bağlı: Müşterinin bir faturadaki ödemeler üzerinden tuttuğu yüzde tutarını hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="209d1-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="209d1-168">**Ödeme bekletme koşulları** hızlı sekmesinde, finansman kaynağını seçin ve **Bekletme yüzdesi** alanına bekletme yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="209d1-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="209d1-169">Proje sözleşmesi için ek faturalama kuralları oluşturmak üzere bu adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="209d1-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
