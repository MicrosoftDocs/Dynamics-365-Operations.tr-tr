--- 
title: "Müşterinin ileri tarih atılmış çekini kapatma"
description: "Çek, banka tarafından tahsil edildikten sonra vadeli çek kapatılabilir."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9cb6064a83e02ddf1fea2de7928965773d08bbc9
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="c077f-103">Müşterinin ileri tarih atılmış çekini kapatma</span><span class="sxs-lookup"><span data-stu-id="c077f-103">Settle a postdated check from a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c077f-104">Çek, banka tarafından tahsil edildikten sonra vadeli çek kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="c077f-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="c077f-105">Bu mali işlem ayrıca vadeli çek için köprü hesabı hareketini de kapatmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c077f-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="c077f-106">Buna başlamadan önce aşağıdaki görevlerin tamamlanması gerekmektedir: 1) Vadeli çekleri hazırlayın 2) Bir müşteriye vadeli bir çeki kaydedin ve kayda alın.</span><span class="sxs-lookup"><span data-stu-id="c077f-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="c077f-107">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="c077f-107">Set up postdated checks</span></span>

2) <span data-ttu-id="c077f-108">Müşteri için ileri tarih atılmış çeki kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="c077f-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="c077f-109">Bu görevin rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="c077f-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="c077f-110">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c077f-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="c077f-111">Kredi ve Tahsilatlar > Sorguları ve raporları > Ödemeler > Müşteri vadeli çekleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="c077f-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="c077f-112">Kapatma'yı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c077f-112">Click Settle.</span></span>
3. <span data-ttu-id="c077f-113">Kliring girişlerini kapat'a tıkla.</span><span class="sxs-lookup"><span data-stu-id="c077f-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="c077f-114">Çek hareketi için müşteri hesabını kapatın.</span><span class="sxs-lookup"><span data-stu-id="c077f-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="c077f-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c077f-115">Close the page.</span></span>
5. <span data-ttu-id="c077f-116">Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="c077f-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="c077f-117">Göster alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="c077f-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="c077f-118">Sadece kullanıcı tarafından oluşturulmuş onay kutusunu temizleyin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c077f-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="c077f-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c077f-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="c077f-120">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c077f-120">Click Lines.</span></span>
10. <span data-ttu-id="c077f-121">Fiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c077f-121">Click Voucher.</span></span>
11. <span data-ttu-id="c077f-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c077f-122">Close the page.</span></span>


