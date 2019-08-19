---
title: Onay günlüğü kullanarak fatura verilerini AP sistemine girme
description: Bu görev kılavuzu, fatura kaydını fatura oluşturmak için nasıl kullanacağınızı ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınızı gösterecek.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0faece510cc85fd86113d8b62d54b71f3014b1db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837063"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="41806-103">Onay günlüğü kullanarak fatura verilerini AP sistemine girme</span><span class="sxs-lookup"><span data-stu-id="41806-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41806-104">Bu görev kılavuzu, fatura kaydını fatura oluşturmak için nasıl kullanacağınızı ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınızı gösterecek.</span><span class="sxs-lookup"><span data-stu-id="41806-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="41806-105">Fatura oluşturun ve nakledin</span><span class="sxs-lookup"><span data-stu-id="41806-105">Create and post and invoice</span></span>
1. <span data-ttu-id="41806-106">Borç hesapları > Faturalar > Fatura kaydı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="41806-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="41806-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-107">Click New.</span></span>
3. <span data-ttu-id="41806-108">Kullanmak istediğiniz fatura kaydının adını seçin.</span><span class="sxs-lookup"><span data-stu-id="41806-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="41806-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="41806-110">Defteri açıp gider satırlarını girmek için Satırlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="41806-111">Bir satıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="41806-111">Select a vendor.</span></span> <span data-ttu-id="41806-112">Örneğin, ABD-104'ü girin veya seçin</span><span class="sxs-lookup"><span data-stu-id="41806-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="41806-113">Fatura alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="41806-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="41806-114">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="41806-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="41806-115">Alacak alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="41806-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="41806-116">Onaylayan alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="41806-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="41806-117">Bir onaylayanı vurgulayın ve o onaylayanı seçmek için Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="41806-118">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-118">Click Post.</span></span>
13. <span data-ttu-id="41806-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="41806-119">Close the page.</span></span>
14. <span data-ttu-id="41806-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="41806-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="41806-121">Fatura onaylayın</span><span class="sxs-lookup"><span data-stu-id="41806-121">Approve an invoice</span></span>
1. <span data-ttu-id="41806-122">Borç hesapları > Faturalar > Fatura onayı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="41806-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="41806-123">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-123">Click New.</span></span>
3. <span data-ttu-id="41806-124">Kullanmak istediğiniz fatura onayı günlüğünün adını seçin.</span><span class="sxs-lookup"><span data-stu-id="41806-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="41806-125">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="41806-126">Onaylamak istediğiniz faturaları seçebileceğiniz bir sayfayı görüntülemek için Satırlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="41806-127">Onaya hazır olan faturaların tümünü görüntülemek için Fişleri bul'u seçin.</span><span class="sxs-lookup"><span data-stu-id="41806-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="41806-128">Oluşturduğunuz faturayı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="41806-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="41806-129">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-129">Click Select.</span></span>
    * <span data-ttu-id="41806-130">Yukarıda seçtiğiniz fişler, seçiminizden sonra bu listeye taşınır.</span><span class="sxs-lookup"><span data-stu-id="41806-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="41806-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-131">Click OK.</span></span>
10. <span data-ttu-id="41806-132">Faturaya bir gider hesabı eklemek için Hesap numarası alanına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="41806-133">Hesap numarası girin ve sekme tuşuyla alandan çıkın.</span><span class="sxs-lookup"><span data-stu-id="41806-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="41806-134">Örneğin, 600120 girin.</span><span class="sxs-lookup"><span data-stu-id="41806-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="41806-135">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-135">Click Post.</span></span>
13. <span data-ttu-id="41806-136">Nakledilen girişleri görüntülemek için Fiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41806-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="41806-137">Onay Bekleyen Fatura hesabı ters kaydedilir ve yerine gerçek gider hesabı geçirilir.</span><span class="sxs-lookup"><span data-stu-id="41806-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

