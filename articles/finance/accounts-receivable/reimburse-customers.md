---
title: Müşterilere tediye
description: Bu makalede bir müşteri grubu için iade hareketlerinin nasıl oluşturulacağı açıklanmaktadır. Bir müşterinin alacak bakiyesi varsa, müşteriye bakiye tutarı için iade yapabilirsiniz.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
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
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97982dec140ed440682ae507f40557670ebccd3e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180389"
---
# <a name="reimburse-customers"></a><span data-ttu-id="e930b-104">Müşterilere tediye</span><span class="sxs-lookup"><span data-stu-id="e930b-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e930b-105">Bu makalede bir müşteri grubu için iade hareketlerinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e930b-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="e930b-106">Bir müşterinin alacak bakiyesi varsa, müşteriye bakiye tutarı için iade yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e930b-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="e930b-107">Başlamadan önce yerine getirilmesi gereken önkoşullar aşağıdaki tabloda gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e930b-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="e930b-108">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="e930b-108">Prerequisite</span></span>                                                            | <span data-ttu-id="e930b-109">Açıklama</span><span class="sxs-lookup"><span data-stu-id="e930b-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e930b-110">Tüzel kişilik için minimum para iadesi tutarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e930b-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="e930b-111">**Borç hesapları parametreleri** sayfasındaki **Genel** altındaki **Minimum para iadesi** alanında müşterilerin fazla ödemeleri için para iadesi yapılabilecek minimum tutarı girin.</span><span class="sxs-lookup"><span data-stu-id="e930b-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="e930b-112">İsteğe bağlı: Para iadesi yapılabilecek her bir müşteri için bir satıcı hesabı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e930b-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="e930b-113">**Müşteriler** sayfasındaki **Muhtelif bilgiler** hızlı sekmesindeki **Satıcı hesabı** alanından müşteri için satıcı hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="e930b-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="e930b-114">Para iadesi hareketleri oluşturduğunuzda borç bakiyesi miktarı için bir satıcı faturası oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e930b-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="e930b-115">Para iadesi işlemi, müşteri hesabı için borç bakiyesini kaldırır ve müşteriye karşılık gelen satıcı hesabı için bir borç bakiyesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e930b-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="e930b-116">Alacak hesapları altından **Para iadesi** işlemini yürütün.</span><span class="sxs-lookup"><span data-stu-id="e930b-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="e930b-117">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="e930b-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="e930b-118">Belirli müşteri hesaplarına para iadesi yapmak için **Seç** düğmesini tıklayın ve ilgili müşteri hesaplarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e930b-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="e930b-119">Tüm müşteri hesaplarını iade etmek için **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e930b-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="e930b-120">Borç tutarları, müşterilerin satıcı hesaplarına transfer edilir ve normal ödemeler olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="e930b-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="e930b-121">Müşteri bir satıcı hesabına sahip değilse müşteri için otomatik olarak tek seferlik bir satıcı hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e930b-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="e930b-122">Oluşturulan para iadesi hareketlerini görmek için, **Para iadesi** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="e930b-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="e930b-123">Borç hesaplarında para iadesi işlemi tarafından oluşturulan satıcı faturaları için bir ödeme oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e930b-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>




