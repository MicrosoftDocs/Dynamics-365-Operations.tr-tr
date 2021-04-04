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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d66caa83df693445c1b1d40ffdc11e8d10cf7426
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239639"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="7a493-103">Satıcının ileri tarih atılmış çekini kapatma</span><span class="sxs-lookup"><span data-stu-id="7a493-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a493-104">Banka, çekin vadesi geçtikten ve çeki ödedikten sonra çek hareketini kapattığında satıcıya ileri tarihe atılmış bir çek çıkarın.</span><span class="sxs-lookup"><span data-stu-id="7a493-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="7a493-105">Bu yordama başlamadan önce aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="7a493-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="7a493-106">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a493-106">Set up postdated checks</span></span>

2) <span data-ttu-id="7a493-107">Satıcı için ileri tarih atılmış çeki kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="7a493-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="7a493-108">Bu yordamın rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="7a493-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="7a493-109">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7a493-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="7a493-110">Borç hesapları > Ödemeler > Vadeli satıcı çekleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7a493-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="7a493-111">Kapatma'yı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a493-111">Click Settle.</span></span>
3. <span data-ttu-id="7a493-112">Kliring girişlerini kapat'a tıkla.</span><span class="sxs-lookup"><span data-stu-id="7a493-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="7a493-113">Çek hareketi için satıcı hesabını kapatmak.</span><span class="sxs-lookup"><span data-stu-id="7a493-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="7a493-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7a493-114">Close the page.</span></span>
5. <span data-ttu-id="7a493-115">Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="7a493-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="7a493-116">Göster alanında 'Hepsi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7a493-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="7a493-117">Sadece kullanıcı tarafından oluşturulmuş onay kutusunu temizleyin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7a493-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="7a493-118">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7a493-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7a493-119">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7a493-119">Click Lines.</span></span>
10. <span data-ttu-id="7a493-120">Fiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a493-120">Click Voucher.</span></span>
11. <span data-ttu-id="7a493-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7a493-121">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]