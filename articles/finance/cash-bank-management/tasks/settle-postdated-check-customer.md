---
title: Müşterinin ileri tarih atılmış çekini kapatma
description: Çek, banka tarafından tahsil edildikten sonra vadeli çek kapatılabilir.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc6f90e7adb3facdfa1facb50fecb0de4ccb04d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448878"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="422b2-103">Müşterinin ileri tarih atılmış çekini kapatma</span><span class="sxs-lookup"><span data-stu-id="422b2-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="422b2-104">Çek, banka tarafından tahsil edildikten sonra vadeli çek kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="422b2-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="422b2-105">Bu mali işlem ayrıca vadeli çek için köprü hesabı hareketini de kapatmaktadır.</span><span class="sxs-lookup"><span data-stu-id="422b2-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="422b2-106">Buna başlamadan önce aşağıdaki görevlerin tamamlanması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="422b2-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="422b2-107">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="422b2-107">Set up postdated checks</span></span>

2) <span data-ttu-id="422b2-108">Müşteri için ileri tarih atılmış çeki kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="422b2-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="422b2-109">Bu görevin rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="422b2-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="422b2-110">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="422b2-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="422b2-111">Kredi ve Tahsilatlar > Sorguları ve raporları > Ödemeler > Müşteri vadeli çekleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="422b2-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="422b2-112">Kapatma'yı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="422b2-112">Click Settle.</span></span>
3. <span data-ttu-id="422b2-113">Kliring girişlerini kapat'a tıkla.</span><span class="sxs-lookup"><span data-stu-id="422b2-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="422b2-114">Çek hareketi için müşteri hesabını kapatın.</span><span class="sxs-lookup"><span data-stu-id="422b2-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="422b2-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="422b2-115">Close the page.</span></span>
5. <span data-ttu-id="422b2-116">Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="422b2-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="422b2-117">Göster alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="422b2-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="422b2-118">Sadece kullanıcı tarafından oluşturulmuş onay kutusunu temizleyin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="422b2-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="422b2-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="422b2-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="422b2-120">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="422b2-120">Click Lines.</span></span>
10. <span data-ttu-id="422b2-121">Fiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="422b2-121">Click Voucher.</span></span>
11. <span data-ttu-id="422b2-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="422b2-122">Close the page.</span></span>

