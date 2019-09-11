---
title: Onay günlüğü kullanarak fatura verilerini borç hesaplarına girme
description: Bu konu, fatura kaydını fatura oluşturmak için nasıl kullanacağınızı ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınızı açıklar.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: fb690769a33f88e63ab8f54cec69a5e927fd324c
ms.sourcegitcommit: 6545bef4584d72dd7789f2d3935cf00ac8f489b0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2019
ms.locfileid: "1871017"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="9f3f3-103">Onay günlüğü kullanarak fatura verilerini borç hesaplarına girme</span><span class="sxs-lookup"><span data-stu-id="9f3f3-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f3f3-104">Bu konu, fatura kaydını fatura oluşturmak için nasıl kullanacağınızı ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınızı açıklar.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="9f3f3-105">Fatura oluşturun ve nakledin</span><span class="sxs-lookup"><span data-stu-id="9f3f3-105">Create and post and invoice</span></span>
1. <span data-ttu-id="9f3f3-106">Gezinti bölmesinde **Modüller > Borç hesapları > Faturalar > Fatura kaydı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="9f3f3-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-107">Select **New**.</span></span>
3. <span data-ttu-id="9f3f3-108">Kullanmak istediğiniz fatura kaydının adını seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="9f3f3-109">Defteri açıp gider satırlarını girmek için **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="9f3f3-110">Bir satıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-110">Select a vendor.</span></span> <span data-ttu-id="9f3f3-111">Örneğin, `US-104` girin veya seçin</span><span class="sxs-lookup"><span data-stu-id="9f3f3-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="9f3f3-112">**Fatura** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="9f3f3-113">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="9f3f3-114">**Alacak** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="9f3f3-115">**Onaylanan** alanında, açılır menüden bir onaylayan belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="9f3f3-116">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="9f3f3-117">Fatura onaylayın</span><span class="sxs-lookup"><span data-stu-id="9f3f3-117">Approve an invoice</span></span>
1. <span data-ttu-id="9f3f3-118">Gezinti bölmesinde **Modüller > Borç hesapları > Faturalar > Fatura onayı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="9f3f3-119">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-119">Select **New**.</span></span>
3. <span data-ttu-id="9f3f3-120">Kullanmak istediğiniz fatura onayı günlüğünün adını seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="9f3f3-121">Onaylamak istediğiniz faturaları seçebileceğiniz bir sayfayı görüntülemek için **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="9f3f3-122">Onaya hazır olan faturaların tümünü görüntülemek için **Fişleri bul**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="9f3f3-123">Oluşturduğunuz faturayı işaretleyin ve **Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="9f3f3-124">Yukarıda seçtiğiniz fişler, seçiminizden sonra bu listeye taşınır.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="9f3f3-125">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-125">Select **OK**.</span></span>
8. <span data-ttu-id="9f3f3-126">Faturaya bir gider hesabı eklemek için **Hesap numarası** alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="9f3f3-127">Hesap numarası girin ve sekme tuşuyla alandan çıkın.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="9f3f3-128">Örneğin `600120` yazın.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="9f3f3-129">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-129">Select **Post**.</span></span>
11. <span data-ttu-id="9f3f3-130">Nakledilen girişleri görüntülemek için **Fiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="9f3f3-131">Onay Bekleyen Fatura hesabı ters kaydedilir ve yerine gerçek gider hesabı geçirilir.</span><span class="sxs-lookup"><span data-stu-id="9f3f3-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

