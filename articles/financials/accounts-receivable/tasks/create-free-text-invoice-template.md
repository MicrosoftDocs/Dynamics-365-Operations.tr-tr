--- 
title: "Serbest metin fatura şablonu oluşturma"
description: "Bu kayıtta USMF demo şirketi kullanılmaktadır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d785922d1c6775d95ad5697eb6a872434e59c8e4
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="cb643-103">Serbest metin fatura şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="cb643-103">Create a free text invoice template</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb643-104">Bu kayıtta USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="cb643-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="cb643-105">Bu kayıt, alacak hesapları faturalarının yönetiminden ve işlenmesinden sorumlu kullanıcılara yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="cb643-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="cb643-106">Alacak hesapları > Faturalar > Yinelenen faturalar > Serbest metin faturası şablonları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="cb643-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="cb643-107">Fatura satırlarını, masrafları, bir muhasebe dağılım şablonu ve genel muhasebe hesabı bilgilerini içerebilen serbest metin faturası şablonları oluşturmak için bu formu kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb643-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="cb643-108">Yeni bir serbest metin faturası şablonu oluşturmak için "Yeni"ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb643-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="cb643-109">Şablon adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="cb643-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="cb643-110">"Şablon adı" serbest metin faturası şablonunu benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="cb643-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="cb643-111">İki şablon aynı "Şablon adı"nı taşıyamaz.</span><span class="sxs-lookup"><span data-stu-id="cb643-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="cb643-112">Açıklama alanına şablon grubu için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="cb643-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="cb643-113">Fatura satırları sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="cb643-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="cb643-114">Açıklama alanına, fatura satırı için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="cb643-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="cb643-115">Ana hesap alanında bir gelir hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="cb643-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="cb643-116">Toplam fatura tutarı için müşteri alacağının mahsup hareket hesabını Müşteri deftere nakil profilleri sayfasında seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb643-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="cb643-117">Satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="cb643-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cb643-118">Geçerli fatura satırı için satış vergisi grubu, müşteri hesabının satış vergisi grubu varsayılan değeridir.</span><span class="sxs-lookup"><span data-stu-id="cb643-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="cb643-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb643-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="cb643-120">Madde vergisi grubu alanında, geçerli fatura satırının madde satış vergisi grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="cb643-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="cb643-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb643-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="cb643-122">Birim fiyatı alanında, fatura satırının birim başına fiyatını girin veya görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="cb643-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="cb643-123">Bu tutar, fatura satırı tutarını belirlemek için, Miktar alanındaki değerle çarpılır.</span><span class="sxs-lookup"><span data-stu-id="cb643-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="cb643-124">Serbest metin faturası şablonuna yeni satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cb643-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="cb643-125">Açıklama alanına, fatura satırı için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="cb643-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="cb643-126">Ana hesap alanında bir gelir hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="cb643-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="cb643-127">Toplam fatura tutarı için müşteri alacağının mahsup hareket hesabını Müşteri deftere nakil profilleri sayfasında seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb643-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="cb643-128">Satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="cb643-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cb643-129">Geçerli fatura satırı için satış vergisi grubu, müşteri hesabının satış vergisi grubu varsayılan değeridir.</span><span class="sxs-lookup"><span data-stu-id="cb643-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="cb643-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb643-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="cb643-131">Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="cb643-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cb643-132">Geçerli fatura satırı için madde satış vergisi grubu.</span><span class="sxs-lookup"><span data-stu-id="cb643-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="cb643-133">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb643-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="cb643-134">Fatura satırı için birim sayısını girin veya görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="cb643-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="cb643-135">Bu sayı, fatura satırı tutarını belirlemek için, Birim fiyatı alanındaki değerle çarpılır.</span><span class="sxs-lookup"><span data-stu-id="cb643-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="cb643-136">Fatura satırı için birim başına fiyatı girin veya görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="cb643-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="cb643-137">Bu tutar, fatura satır tutarını belirlemek için, Miktar alanındaki değerle çarpılır.</span><span class="sxs-lookup"><span data-stu-id="cb643-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="cb643-138">Tek bir satır ve tüm alt satırları için muhasebe dağılımlarını görüntüleyin veya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="cb643-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="cb643-139">Muhasebe dağılımları, bir tutarın, örneğin gelirin, verginin veya masrafların bir serbest metin faturasında nasıl hesaba katılacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="cb643-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="cb643-140">Seçili fatura satırı için muhasebe dağılımlarını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="cb643-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="cb643-141">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb643-141">Click Close.</span></span>


