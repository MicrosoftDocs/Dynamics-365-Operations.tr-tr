---
title: Satınalma girişlerinde proje maliyet tahakkuku
description: Bu konuda satın alma girişlerinden tahakkuk eden proje maliyetlerinin Microsoft Dynamics 365 Finance'da nasıl izlenebileceği açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9200b0e4bc3862abdb3ecacb6539f7ba0d619b2f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189626"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="4bd79-103">Satınalma girişlerinde proje maliyet tahakkuku</span><span class="sxs-lookup"><span data-stu-id="4bd79-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bd79-104">Bu konuda satın alma girişlerinden tahakkuk eden proje maliyetlerinin Microsoft Dynamics 365 Finance'da nasıl izlenebileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4bd79-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="4bd79-105">Bir proje için fatura genellikle mallar ve hizmetler teslim edildikten daha sonra gelir; bu durumun projenin temel performans göstergeleri (KPI'ler) üzerinde önemli bir etkisi olabilir.</span><span class="sxs-lookup"><span data-stu-id="4bd79-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="4bd79-106">Bu hareketleri hem mali hem de proje raporlarından izleyebilmek önemlidir.</span><span class="sxs-lookup"><span data-stu-id="4bd79-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="4bd79-107">Aşağıdaki örnek senaryoda bu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4bd79-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="4bd79-108">Contoso Danışmanlık yeni bir bulut dağıtım projesi başlatmıştır.</span><span class="sxs-lookup"><span data-stu-id="4bd79-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="4bd79-109">Proje için bir bilgisayar satın almak üzere bir satınalma siparişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4bd79-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="4bd79-110">Bilgisayar maliyeti $1500 ve yükleme hizmetleri maliyeti $150 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4bd79-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="4bd79-111">Satıcı bilgisayarı teslim eder ve kurulumunu yapar ancak fatura henüz Contoso Danışmalığa ulaşmamıştır.</span><span class="sxs-lookup"><span data-stu-id="4bd79-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="4bd79-112">Proje yöneticisi, fatura teslim edilmeden önce tahakkuk eden $1650 tutarındaki proje maliyetini görmek ister.</span><span class="sxs-lookup"><span data-stu-id="4bd79-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="4bd79-113">Bu maliyetin şirketin ay sonu mali tablosuna da yansıtılması gerekmetedir.</span><span class="sxs-lookup"><span data-stu-id="4bd79-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="4bd79-114">Tahakkuk eden maliyetin hem mali düzeyde hem de raporlama amacıyla proje düzeyinde kaydedilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bd79-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="4bd79-115">Ürün girişinin mali güncelleştirmesi, madde ve tedarik kategorileri için izlenebilir.</span><span class="sxs-lookup"><span data-stu-id="4bd79-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="4bd79-116">Maddeler için **Borç hesapları parametreleri** sayfasında, **Ürün girişlerini genel muhasebeye naklet** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="4bd79-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="4bd79-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="4bd79-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="4bd79-118">Tedarik kategorileri için **Kategori ilke kuralı** sayfasında, **Satınalma** ilkelerini ve ardından her tedarik kategorisi için **Satınalma alış irsaliyesindeki gideri tahakkuk et** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4bd79-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="4bd79-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="4bd79-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="4bd79-120">**Deftere nakil ayarı**'ndaki **Faturalanmamış satınalma harcaması** ve **Satınalma tahakkuk** ürün girişiyle ilgili fişler deftere nakledildiğinde kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="4bd79-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="4bd79-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="4bd79-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="4bd79-122">Bu aynı senaryoyu kullanarak, bir ürün girişini deftere nakletmenin Genel muhasebeyi ve Proje bilgilerini nasıl etkileyeceğini görelim.</span><span class="sxs-lookup"><span data-stu-id="4bd79-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="4bd79-123">**Adım 1:** Bilgisayar satın alma için $1500 ve kurulum hizmetleri için $150 kaydetmek üzere proje için yeni bir satınalma siparişi oluşturun ve kaydedin.</span><span class="sxs-lookup"><span data-stu-id="4bd79-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="4bd79-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="4bd79-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="4bd79-125">Satınalma siparişi teyit edildiğinde, proje için taahhüt edilen maliyet hareketleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4bd79-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="4bd79-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="4bd79-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="4bd79-127">Taahhüt edilen maliyet hareketlerinin **Hareket Kaynağı** alanı **Satınalma Siparişi** olarak ayarlanmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4bd79-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="4bd79-128">Bir satınalma siparişi oluşturma ve onaylama proje için hareketler oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="4bd79-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="4bd79-129">**Adım 2:** Mallar ve hizmetler teslim edilir ve ürün girişi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="4bd79-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="4bd79-130">Ürün girişini deftere nakletmek bir fiş oluşturur ve fişi genel muhasebe defterine nakleder.</span><span class="sxs-lookup"><span data-stu-id="4bd79-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="4bd79-131">Fiş borç satınalma harcamasını, faturalanmamış hesabını borçlandırır ve satınalma tahakkuk hesabını alacaklandırır.</span><span class="sxs-lookup"><span data-stu-id="4bd79-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="4bd79-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="4bd79-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="4bd79-133">Bir ürün girişini deftere nakletme işlemi, proje kategorileri için deftere nakil ayarını değil tedarik kategorileri ve ürünler için deftere nakil ayarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="4bd79-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="4bd79-134">Satınalma tahakkukların mali etkisini doğru biçimde yansıtmak için bu kurulum uyumlu hale getirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bd79-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="4bd79-135">**Tedarik kategorisi** sayfasında tedaril kategorilerini proje kategorileriyle eşleştirmek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="4bd79-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="4bd79-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="4bd79-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="4bd79-137">**Adım 3:** Taslak bir satıcı faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="4bd79-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="4bd79-138">Ürün girişinin deftere nakledilmesi proje bilgilerini etkilemez.</span><span class="sxs-lookup"><span data-stu-id="4bd79-138">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="4bd79-139">Geçici bir çözüm olarak, satınalma girişini deftere naklettikten sonra taslak bir satıcı faturası oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4bd79-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="4bd79-140">**Satınalma Siparişi** sayfasında &gt; **Fatura sekmesi** &gt; **Generate** &gt; **Fatura** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="4bd79-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="4bd79-141">Bu, proje bilgilerini güncelleştiren bir bekleyen fatura belgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bd79-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="4bd79-142">Taslak satıcı faturası oluşturma bekleyen proje hareketleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bd79-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="4bd79-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="4bd79-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="4bd79-144">**Taahhüt edilen maliyet** sayfasında, 1. adımda oluşturulan kayıtlar kapatılır ve bekleyen satıcı faturasından gelen maliyet taahhüdünü yansıtmak üzere yeni kayıtlar oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4bd79-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="4bd79-145">Taahhüt edilen maliyet için **Hareket kaynağı** alanı **Satıcı faturası** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4bd79-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="4bd79-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="4bd79-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="4bd79-147">Satıcı faturası gerçek satıcı faturası gelene kadar bekleme durumunda kalır.</span><span class="sxs-lookup"><span data-stu-id="4bd79-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



