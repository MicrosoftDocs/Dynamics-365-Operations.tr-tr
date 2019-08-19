---
title: Satıcının ileri tarih atılmış çekini kapatma
description: Banka, çekin vadesi geçtikten ve çeki ödedikten sonra çek hareketini kapattığında satıcıya ileri tarihe atılmış bir çek çıkarın.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d935ec24d97ca76a088cbe41d57c12c6e8a6689
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841837"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="27110-103">Satıcının ileri tarih atılmış çekini kapatma</span><span class="sxs-lookup"><span data-stu-id="27110-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="27110-104">Banka, çekin vadesi geçtikten ve çeki ödedikten sonra çek hareketini kapattığında satıcıya ileri tarihe atılmış bir çek çıkarın.</span><span class="sxs-lookup"><span data-stu-id="27110-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="27110-105">Bu yordama başlamadan önce aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="27110-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="27110-106">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="27110-106">Set up postdated checks</span></span>

2) <span data-ttu-id="27110-107">Satıcı için ileri tarih atılmış çeki kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="27110-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="27110-108">Bu yordamın rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="27110-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="27110-109">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="27110-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="27110-110">Borç hesapları > Ödemeler > Vadeli satıcı çekleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="27110-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="27110-111">Kapatma'yı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27110-111">Click Settle.</span></span>
3. <span data-ttu-id="27110-112">Kliring girişlerini kapat'a tıkla.</span><span class="sxs-lookup"><span data-stu-id="27110-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="27110-113">Çek hareketi için satıcı hesabını kapatmak.</span><span class="sxs-lookup"><span data-stu-id="27110-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="27110-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27110-114">Close the page.</span></span>
5. <span data-ttu-id="27110-115">Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="27110-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="27110-116">Göster alanında 'Hepsi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="27110-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="27110-117">Sadece kullanıcı tarafından oluşturulmuş onay kutusunu temizleyin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="27110-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="27110-118">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="27110-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="27110-119">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27110-119">Click Lines.</span></span>
10. <span data-ttu-id="27110-120">Fiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27110-120">Click Voucher.</span></span>
11. <span data-ttu-id="27110-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27110-121">Close the page.</span></span>

