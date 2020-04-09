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
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141592"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="25d6a-103">Müşterinin ileri tarih atılmış çekini kapatma</span><span class="sxs-lookup"><span data-stu-id="25d6a-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25d6a-104">Çek, banka tarafından tahsil edildikten sonra vadeli çek kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="25d6a-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="25d6a-105">Bu mali işlem ayrıca vadeli çek için köprü hesabı hareketini de kapatmaktadır.</span><span class="sxs-lookup"><span data-stu-id="25d6a-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="25d6a-106">Buna başlamadan önce aşağıdaki görevlerin tamamlanması gerekmektedir: 1) Vadeli çekleri hazırlayın 2) Bir müşteriye vadeli bir çeki kaydedin ve kayda alın.</span><span class="sxs-lookup"><span data-stu-id="25d6a-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="25d6a-107">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="25d6a-107">Set up postdated checks</span></span>

2) <span data-ttu-id="25d6a-108">Müşteri için ileri tarih atılmış çeki kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="25d6a-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="25d6a-109">Bu görevin rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="25d6a-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="25d6a-110">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="25d6a-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="25d6a-111">Kredi ve Tahsilatlar > Sorguları ve raporları > Ödemeler > Müşteri vadeli çekleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="25d6a-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="25d6a-112">Kapatma'yı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="25d6a-112">Click Settle.</span></span>
3. <span data-ttu-id="25d6a-113">Kliring girişlerini kapat'a tıkla.</span><span class="sxs-lookup"><span data-stu-id="25d6a-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="25d6a-114">Çek hareketi için müşteri hesabını kapatın.</span><span class="sxs-lookup"><span data-stu-id="25d6a-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="25d6a-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="25d6a-115">Close the page.</span></span>
5. <span data-ttu-id="25d6a-116">Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="25d6a-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="25d6a-117">Göster alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="25d6a-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="25d6a-118">Sadece kullanıcı tarafından oluşturulmuş onay kutusunu temizleyin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="25d6a-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="25d6a-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="25d6a-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="25d6a-120">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="25d6a-120">Click Lines.</span></span>
10. <span data-ttu-id="25d6a-121">Fiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="25d6a-121">Click Voucher.</span></span>
11. <span data-ttu-id="25d6a-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="25d6a-122">Close the page.</span></span>

