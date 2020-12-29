---
title: Müşterilere tediye
description: Bu makalede bir müşteri grubu için iade hareketlerinin nasıl oluşturulacağı açıklanmaktadır. Bir müşterinin alacak bakiyesi varsa, müşteriye bakiye tutarı için iade yapabilirsiniz.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65ee884fb22c1a38e2d3022085fed7e3e6077d1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644549"
---
# <a name="reimburse-customers"></a><span data-ttu-id="e0b11-104">Müşterilere tediye</span><span class="sxs-lookup"><span data-stu-id="e0b11-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0b11-105">Bu makalede bir müşteri grubu için iade hareketlerinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e0b11-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="e0b11-106">Bir müşterinin alacak bakiyesi varsa, müşteriye bakiye tutarı için iade yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e0b11-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="e0b11-107">Başlamadan önce yerine getirilmesi gereken önkoşullar aşağıdaki tabloda gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e0b11-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="e0b11-108">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="e0b11-108">Prerequisite</span></span>                                                            | <span data-ttu-id="e0b11-109">Açıklama</span><span class="sxs-lookup"><span data-stu-id="e0b11-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="e0b11-110">Tüzel kişilik için minimum para iadesi tutarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e0b11-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="e0b11-111">**Borç hesapları parametreleri** sayfasındaki **Genel** altındaki **Minimum para iadesi** alanında müşterilerin fazla ödemeleri için para iadesi yapılabilecek minimum tutarı girin.</span><span class="sxs-lookup"><span data-stu-id="e0b11-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="e0b11-112">İsteğe bağlı: Para iadesi yapılabilecek her bir müşteri için bir satıcı hesabı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e0b11-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="e0b11-113">**Müşteriler** sayfasındaki **Muhtelif bilgiler** hızlı sekmesindeki **Satıcı hesabı** alanından müşteri için satıcı hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="e0b11-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="e0b11-114">Para iadesi hareketleri oluşturduğunuzda borç bakiyesi miktarı için bir satıcı faturası oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e0b11-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="e0b11-115">Para iadesi işlemi, müşteri hesabı için borç bakiyesini kaldırır ve müşteriye karşılık gelen satıcı hesabı için bir borç bakiyesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0b11-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="e0b11-116">Alacak hesaplarında **Para iadesi** işlemini çalıştırın (**Alacak hesapları \> Periyodik görevler \> Para iadesi**).</span><span class="sxs-lookup"><span data-stu-id="e0b11-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="e0b11-117">Genel muhasebe boyutlarına bakılmaksızın, tüm hareketleri gruplandırmak için **Müşteriyi özetle** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e0b11-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="e0b11-118">Yalnızca benzer defter boyutları olan hareketleri gruplandırmak için, seçeneği **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e0b11-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="e0b11-119">Kapatılmayan borç tutarları olan müşterileri seçmek için **Bekleyen borç hareketleri olan müşterileri dahil et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e0b11-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="e0b11-120">Belirli müşteri hesaplarına para iadesi yapmak için **Dahil edilecek kayıtlar** hızlı sekmesinde **Filtre**'yi seçin ve ardından sorguda müşteri hesaplarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e0b11-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="e0b11-121">Borç tutarları, müşterilerin satıcı hesaplarına transfer edilir ve normal ödemeler olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="e0b11-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="e0b11-122">Müşteri bir satıcı hesabına sahip değilse müşteri için otomatik olarak tek seferlik bir satıcı hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0b11-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="e0b11-123">Oluşturulan para iadesi hareketlerini görüntülemek için **Para iadesi** raporunu kullanın (**Alacak Hesapları \> Sorgular ve raporlar \> Para iadesi raporu**).</span><span class="sxs-lookup"><span data-stu-id="e0b11-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="e0b11-124">Borç hesaplarında para iadesi işlemi tarafından oluşturulan satıcı faturaları için bir ödeme oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e0b11-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="e0b11-125">Satıcılara nasıl ödeme yapıalcak hakkında bilgi için bkz. [Satıcı ödemesine genel bakış](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="e0b11-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>
