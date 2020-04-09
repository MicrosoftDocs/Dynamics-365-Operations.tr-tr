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
ms.openlocfilehash: ee66bdb93d1252486efc7be25adeb6ee7cc6ce05
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144265"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="3e4ee-103">Satıcının ileri tarih atılmış çekini kapatma</span><span class="sxs-lookup"><span data-stu-id="3e4ee-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e4ee-104">Banka, çekin vadesi geçtikten ve çeki ödedikten sonra çek hareketini kapattığında satıcıya ileri tarihe atılmış bir çek çıkarın.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="3e4ee-105">Bu yordama başlamadan önce aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="3e4ee-106">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="3e4ee-106">Set up postdated checks</span></span>

2) <span data-ttu-id="3e4ee-107">Satıcı için ileri tarih atılmış çeki kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="3e4ee-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="3e4ee-108">Bu yordamın rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="3e4ee-109">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="3e4ee-110">Borç hesapları > Ödemeler > Vadeli satıcı çekleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="3e4ee-111">Kapatma'yı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-111">Click Settle.</span></span>
3. <span data-ttu-id="3e4ee-112">Kliring girişlerini kapat'a tıkla.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="3e4ee-113">Çek hareketi için satıcı hesabını kapatmak.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="3e4ee-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-114">Close the page.</span></span>
5. <span data-ttu-id="3e4ee-115">Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="3e4ee-116">Göster alanında 'Hepsi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="3e4ee-117">Sadece kullanıcı tarafından oluşturulmuş onay kutusunu temizleyin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="3e4ee-118">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3e4ee-119">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-119">Click Lines.</span></span>
10. <span data-ttu-id="3e4ee-120">Fiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-120">Click Voucher.</span></span>
11. <span data-ttu-id="3e4ee-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3e4ee-121">Close the page.</span></span>

