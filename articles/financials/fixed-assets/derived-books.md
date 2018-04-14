---
title: "Türetilen defterler"
description: "Bu makale, türetilmiş defter işlevselliğine genel bir bakış sağlar."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 23b17c577fd2e0dfa6183929c86ed1950db8c50b
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="derived-books"></a><span data-ttu-id="d34d8-103">Türetilen defterler</span><span class="sxs-lookup"><span data-stu-id="d34d8-103">Derived books</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d34d8-104">Bu makale, türetilmiş defter işlevselliğine genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="d34d8-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="d34d8-105">Türetilmiş kitapların amacı, düzenli aralıklarla planlanan sabit kıymet kitap hareketlerinin nakledilmesini kolaylaştırmaktır.</span><span class="sxs-lookup"><span data-stu-id="d34d8-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="d34d8-106">Bir kitabı birincil kitap olarak seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d34d8-106">You choose one book as the primary book.</span></span> <span data-ttu-id="d34d8-107">Bu, genellikle amortisman muhasebesi için kullanılan defterdir.</span><span class="sxs-lookup"><span data-stu-id="d34d8-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="d34d8-108">Ardından, hareketleri birincil defterle aynı aralıklarda nakletmek için kurulan diğer defterlere eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="d34d8-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="d34d8-109">Vergi amortisman defterleri genellikle türetilmiş defterler olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d34d8-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="d34d8-110">Türetilmiş defterlere nakletmek için ayarlanan en yaygın hareketler alımlar, alım düzeltmeleri ve çıkışlardır.</span><span class="sxs-lookup"><span data-stu-id="d34d8-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="d34d8-111">Örnek</span><span class="sxs-lookup"><span data-stu-id="d34d8-111">Example</span></span>

<span data-ttu-id="d34d8-112">Defter B ve defter C, Alım hareket türü için defter A'nın türetilmiş defterleri olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d34d8-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="d34d8-113">Defter A'da, kıymet 123 için alım hareketi olarak 1.500,00 girin.</span><span class="sxs-lookup"><span data-stu-id="d34d8-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="d34d8-114">Hareket nakledildiğinde, defter B için kıymet 123 içinde bir alım hareketi oluşturulur ve nakledilir. Defter C için kıymet 123 içinde 1.500,00 tutarında bir alım hareketi oluşturulur ve nakledilir.</span><span class="sxs-lookup"><span data-stu-id="d34d8-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="d34d8-115">Birincil defterin hareketlerini sabit kıymet günlüğüne nakletmek için hazırladığınızda, ayrıca türetilmiş defterlerin hareketlerini de görüntüleyebilir ve değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d34d8-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="d34d8-116">Birincil defter hareketlerini başka günlükte hazırlarsanız türetilmiş değer hareketleri görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="d34d8-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="d34d8-117">Ancak, birincil defter hareketlerini naklettiğinizde uygun hesaplara ve nakil katmanlarına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="d34d8-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="d34d8-118">Birincil defter aralıkları dışındaki aralıklarda hareketleri nakletmek için oluşturulan defterler türetilmiş defterler olarak değil, ayrı defterler olarak sabit kıymete eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="d34d8-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="d34d8-119">Daha fazla bilgi için bkz: [Türetilmiş defterlerle deftere nakil](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="d34d8-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>




