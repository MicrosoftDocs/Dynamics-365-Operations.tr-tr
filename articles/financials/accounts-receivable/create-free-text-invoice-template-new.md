--- 
title: "Serbest metin fatura şablonu oluşturma"
description: "Bu prosedürde, serbest metin faturası şablonunun nasıl oluşturulduğu gösterilmektedir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d617302e020c21a7a7fb077e4ce9481b6c80b796
ms.openlocfilehash: 80eb886c70e3bfde3a9eff87be48498aa48d7234
ms.contentlocale: tr-tr
ms.lasthandoff: 08/06/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="ebfb1-103">Serbest metin fatura şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ebfb1-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebfb1-104">Bu örnek için USMF demo şirketini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="ebfb1-105">Bu prosedür, alacak hesapları faturalarının yönetiminden ve işlenmesinden sorumlu kullanıcılara yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="ebfb1-106">Şablon oluştur</span><span class="sxs-lookup"><span data-stu-id="ebfb1-106">Create a template</span></span>

1. <span data-ttu-id="ebfb1-107">Alacak hesapları > Faturalar > Yinelenen faturalar > Serbest metin faturası şablonları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="ebfb1-108">Fatura satırlarını, masrafları, bir muhasebe dağılım şablonu ve genel muhasebe hesabı bilgilerini içerebilen serbest metin faturası şablonları oluşturmak için bu formu kullanın.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="ebfb1-109">Yeni bir serbest metin faturası şablonu oluşturmak için "Yeni"ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="ebfb1-110">Şablon adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="ebfb1-111">"Şablon adı" serbest metin faturası şablonunu benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="ebfb1-112">İki şablon aynı "Şablon adı"nı taşıyamaz.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="ebfb1-113">Açıklama alanına şablon grubu için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="ebfb1-114">Fatura satırları sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="ebfb1-115">Açıklama alanına, fatura satırı için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="ebfb1-116">Ana hesap alanında bir gelir hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="ebfb1-117">Toplam fatura tutarı için müşteri alacağının mahsup hareket hesabını Müşteri deftere nakil profilleri sayfasında seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="ebfb1-118">Satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ebfb1-119">Geçerli fatura satırı için satış vergisi grubu, müşteri hesabının satış vergisi grubu varsayılan değeridir.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="ebfb1-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ebfb1-121">Madde vergisi grubu alanında, geçerli fatura satırının madde satış vergisi grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="ebfb1-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="ebfb1-123">Birim fiyatı alanında, fatura satırının birim başına fiyatını girin veya görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="ebfb1-124">Bu tutar, fatura satırı tutarını belirlemek için, Miktar alanındaki değerle çarpılır.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="ebfb1-125">Serbest metin faturası şablonuna yeni satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="ebfb1-126">Açıklama alanına, fatura satırı için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="ebfb1-127">Ana hesap alanında bir gelir hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="ebfb1-128">Toplam fatura tutarı için müşteri alacağının mahsup hareket hesabını Müşteri deftere nakil profilleri sayfasında seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="ebfb1-129">Satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ebfb1-130">Geçerli fatura satırı için satış vergisi grubu, müşteri hesabının satış vergisi grubu varsayılan değeridir.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="ebfb1-131">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="ebfb1-132">Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ebfb1-133">Geçerli fatura satırı için madde satış vergisi grubu.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="ebfb1-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="ebfb1-135">Fatura satırı için birim sayısını girin veya görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="ebfb1-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="ebfb1-136">Bu sayı, fatura satırı tutarını belirlemek için, Birim fiyatı alanındaki değerle çarpılır.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="ebfb1-137">Fatura satırı için birim başına fiyatı girin veya görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="ebfb1-138">Bu tutar, fatura satır tutarını belirlemek için, Miktar alanındaki değerle çarpılır.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="ebfb1-139">Tek bir satır ve tüm alt satırları için muhasebe dağılımlarını görüntüleyin veya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="ebfb1-140">Muhasebe dağılımları, bir tutarın, örneğin gelirin, verginin veya masrafların bir serbest metin faturasında nasıl hesaba katılacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="ebfb1-141">Seçili fatura satırı için muhasebe dağılımlarını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="ebfb1-142">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="ebfb1-143">Bir serbest metin faturasını şablon olarak kaydetme</span><span class="sxs-lookup"><span data-stu-id="ebfb1-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="ebfb1-144">Mevcut bir serbest metin faturasını şablon olarak da kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="ebfb1-145">Fatura sekmesinden "Şablona kaydet"i seçtiğiniz zaman şablon için bir ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="ebfb1-146">Aynı adı taşıyan bir şablon varsa, bu adda bir şablonun zaten var olduğuna ilişkin bir bildirim görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="ebfb1-147">Yine de, Tamam'a tıklayarak şablonun yerine yenisini geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ebfb1-147">You can still click on Ok to replace it.</span></span> 

