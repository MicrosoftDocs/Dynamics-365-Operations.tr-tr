--- 
title: "Onay günlüğü kullanarak fatura verilerini AP sistemine girme"
description: "Bu görev kılavuzu, fatura kaydını fatura oluşturmak için nasıl kullanacağınızı ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınızı gösterecek."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="ccd00-103">Onay günlüğü kullanarak fatura verilerini AP sistemine girme</span><span class="sxs-lookup"><span data-stu-id="ccd00-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ccd00-104">Bu görev kılavuzu, fatura kaydını fatura oluşturmak için nasıl kullanacağınızı ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınızı gösterecek.</span><span class="sxs-lookup"><span data-stu-id="ccd00-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="ccd00-105">Fatura oluşturun ve nakledin</span><span class="sxs-lookup"><span data-stu-id="ccd00-105">Create and post and invoice</span></span>
1. <span data-ttu-id="ccd00-106">Borç hesapları > Faturalar > Fatura kaydı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ccd00-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="ccd00-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-107">Click New.</span></span>
3. <span data-ttu-id="ccd00-108">Kullanmak istediğiniz fatura kaydının adını seçin.</span><span class="sxs-lookup"><span data-stu-id="ccd00-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="ccd00-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ccd00-110">Defteri açıp gider satırlarını girmek için Satırlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="ccd00-111">Bir satıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="ccd00-111">Select a vendor.</span></span> <span data-ttu-id="ccd00-112">Örneğin, ABD-104'ü girin veya seçin</span><span class="sxs-lookup"><span data-stu-id="ccd00-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="ccd00-113">Fatura alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ccd00-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="ccd00-114">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ccd00-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="ccd00-115">Alacak alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ccd00-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="ccd00-116">Onaylayan alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ccd00-117">Bir onaylayanı vurgulayın ve o onaylayanı seçmek için Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="ccd00-118">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-118">Click Post.</span></span>
13. <span data-ttu-id="ccd00-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-119">Close the page.</span></span>
14. <span data-ttu-id="ccd00-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="ccd00-121">Fatura onaylayın</span><span class="sxs-lookup"><span data-stu-id="ccd00-121">Approve an invoice</span></span>
1. <span data-ttu-id="ccd00-122">Borç hesapları > Faturalar > Fatura onayı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ccd00-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="ccd00-123">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-123">Click New.</span></span>
3. <span data-ttu-id="ccd00-124">Kullanmak istediğiniz fatura onayı günlüğünün adını seçin.</span><span class="sxs-lookup"><span data-stu-id="ccd00-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="ccd00-125">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ccd00-126">Onaylamak istediğiniz faturaları seçebileceğiniz bir sayfayı görüntülemek için Satırlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="ccd00-127">Onaya hazır olan faturaların tümünü görüntülemek için Fişleri bul'u seçin.</span><span class="sxs-lookup"><span data-stu-id="ccd00-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="ccd00-128">Oluşturduğunuz faturayı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ccd00-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="ccd00-129">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-129">Click Select.</span></span>
    * <span data-ttu-id="ccd00-130">Yukarıda seçtiğiniz fişler, seçiminizden sonra bu listeye taşınır.</span><span class="sxs-lookup"><span data-stu-id="ccd00-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="ccd00-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-131">Click OK.</span></span>
10. <span data-ttu-id="ccd00-132">Faturaya bir gider hesabı eklemek için Hesap numarası alanına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="ccd00-133">Hesap numarası girin ve sekme tuşuyla alandan çıkın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="ccd00-134">Örneğin, 600120 girin.</span><span class="sxs-lookup"><span data-stu-id="ccd00-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="ccd00-135">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-135">Click Post.</span></span>
13. <span data-ttu-id="ccd00-136">Nakledilen girişleri görüntülemek için Fiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ccd00-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="ccd00-137">Onay Bekleyen Fatura hesabı ters kaydedilir ve yerine gerçek gider hesabı geçirilir.</span><span class="sxs-lookup"><span data-stu-id="ccd00-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  


