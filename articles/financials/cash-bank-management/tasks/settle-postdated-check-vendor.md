--- 
title: "Satıcının ileri tarih atılmış çekini kapatma"
description: "Banka, çekin vadesi geçtikten ve çeki ödedikten sonra çek hareketini kapattığında satıcıya ileri tarihe atılmış bir çek çıkarın."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 7520f587f5fb05937047b814570c00f8212bad82
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="560a4-103">Satıcının ileri tarih atılmış çekini kapatma</span><span class="sxs-lookup"><span data-stu-id="560a4-103">Settle a postdated check for a vendor</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="560a4-104">Banka, çekin vadesi geçtikten ve çeki ödedikten sonra çek hareketini kapattığında satıcıya ileri tarihe atılmış bir çek çıkarın.</span><span class="sxs-lookup"><span data-stu-id="560a4-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="560a4-105">Bu yordama başlamadan önce aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="560a4-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="560a4-106">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="560a4-106">Set up postdated checks</span></span>

2) <span data-ttu-id="560a4-107">Satıcı için ileri tarih atılmış çeki kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="560a4-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="560a4-108">Bu yordamın rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="560a4-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="560a4-109">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="560a4-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="560a4-110">Borç hesapları > Ödemeler > Vadeli satıcı çekleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="560a4-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="560a4-111">Kapatma'yı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="560a4-111">Click Settle.</span></span>
3. <span data-ttu-id="560a4-112">Kliring girişlerini kapat'a tıkla.</span><span class="sxs-lookup"><span data-stu-id="560a4-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="560a4-113">Çek hareketi için satıcı hesabını kapatmak.</span><span class="sxs-lookup"><span data-stu-id="560a4-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="560a4-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="560a4-114">Close the page.</span></span>
5. <span data-ttu-id="560a4-115">Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="560a4-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="560a4-116">Göster alanında 'Hepsi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="560a4-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="560a4-117">Sadece kullanıcı tarafından oluşturulmuş onay kutusunu temizleyin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="560a4-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="560a4-118">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="560a4-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="560a4-119">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="560a4-119">Click Lines.</span></span>
10. <span data-ttu-id="560a4-120">Fiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="560a4-120">Click Voucher.</span></span>
11. <span data-ttu-id="560a4-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="560a4-121">Close the page.</span></span>


