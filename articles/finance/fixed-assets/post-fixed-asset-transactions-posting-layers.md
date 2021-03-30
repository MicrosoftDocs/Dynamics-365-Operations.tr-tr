---
title: Sabit kıymet hareketlerini deftere nakil katmanlarında deftere nakletme
description: Bu makalede sabit kıymet hareketleri için katman işlevlerinin deftere nakline genel bir bakış sunulmuştur.
author: moaamer
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a52374d52b3dcd435c79033d462a2982316a68b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240870"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="29999-103">Sabit kıymet hareketlerini deftere nakil katmanlarında deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="29999-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29999-104">Bu makalede sabit kıymet hareketleri için katman işlevlerinin deftere nakline genel bir bakış sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="29999-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="29999-105">Bir sabit kıymet genellikle farklı amaçlarla ve farklı şekillerde amortize edilir.</span><span class="sxs-lookup"><span data-stu-id="29999-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="29999-106">Vergi nedeniyle yapılan amortisman, vergiler için mümkün olan en yüksek amortismanı oluşturmak amacıyla geçerli vergi kuralları kullanılarak hesaplanır, ancak raporlama amacıyla yapılan amortismanlar muhasebe kanun ve standartlarına göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="29999-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="29999-107">Çeşitli amortisman türleri ayrı ayrı hesaplanır ve nakil katmanlarına ayrı ayrı kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="29999-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="29999-108">Sabit bir değere bağlı her defter genel amortisman amacını içeren belirli bir nakil katmanı için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="29999-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="29999-109">On tür deftere nakil katmanı vardır: Cari, İşlemler, Vergi ve yedi Özel Katman.</span><span class="sxs-lookup"><span data-stu-id="29999-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="29999-110">Ayrıca Defter için genel muhasebeye nakil işlemini, Genel muhasebeye naklet alanını Hayır olarak ayarlayarak devre dışı bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29999-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="29999-111">Ardından Deftere nakil katmanı alanı otomatik olarak Hiçbiri olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="29999-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="29999-112">Normalde, genel muhasebeye nakledilmeyen defterler vergi raporlama amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="29999-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="29999-113">Bu yaklaşım, genel muhasebeye taahhütte bulunulmadığından kıymet defterine ait geçmiş hareketleri silmek için ek esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="29999-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="29999-114">Sabit kıymet günlükleri Genel muhasebe > Günlük ayarı > Günlük adları konumunda Günlük adları sayfası kullanılarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="29999-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="29999-115">Amortisman nakledebileceğiniz her günlük, yalnızca bir nakil katmanı için günlük adı ile tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="29999-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="29999-116">Günlükte deftere nakil katmanı değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="29999-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="29999-117">Bu kısıtlama her deftere nakil katmanı için hareketlerin ayrı tutulmasını garantiye almaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="29999-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="29999-118">Her nakil katmanı için en az bir günlük adı oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="29999-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="29999-119">Genel muhasebeye nakledilmeyen defterler kullanıyorsanız ayrıca deftere nakil katmanı Hiçbiri olarak ayarlanan bir günlük de oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="29999-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="29999-120">Sabit kıymet hareketleri için Sabit kıymet nakil profilleri sayfasında genel muhasebe hesapları atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29999-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="29999-121">Her deftere nakil profili için ilgili hareket tipini ve defteri seçmeli ve ardından genel muhasebe kayıtlarını belirlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="29999-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="29999-122">Her defter için genel muhasebeye nakleden bir deftere nakil profili kaydı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="29999-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

<span data-ttu-id="29999-123">Sabit varlık yalnızca **Geçerli** deftere nakit katmanını destekleyen belgelere girilir (ör. **Satın alma siparişi**, **Bekleyen satıcı faturası**, **Satış siparişi** veya **Serbest metinli fatura**).</span><span class="sxs-lookup"><span data-stu-id="29999-123">The fixed asset can be entered in documents that only support the **Current** posting layer, like **Purchase order**, **Pending vendor invoice**, **Sales order**, or **Free text invoice**.</span></span> <span data-ttu-id="29999-124">Bu belgelerden herhangi birinde sabit varlık kimliğini seçerken varlık defteri **Geçerli** deftere nakil katmanına sahip defterle filtrelenir ve sistem, sabit varlık deftere nakil katmanının **Geçerli** olduğunu doğruladığında bu kimlik deftere nakil sırasında otomatik olarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="29999-124">While selecting a fixed asset ID in any of those documents the asset book is filtered to the book with **Current** posting layer, and will be filled in automatically, during posting when the system validates that the fixed asset posting layer is **Current**.</span></span> <span data-ttu-id="29999-125">Bu doğrulama tamamlanamazsa deftere nakil işlemi durdurulur.</span><span class="sxs-lookup"><span data-stu-id="29999-125">If that validation can't be completed, the posting process will be stopped.</span></span> 

> [!NOTE] 
> <span data-ttu-id="29999-126">Türetilmiş defterleri kullanarak hareketleri aynı anda farklı nakil katmanlarında deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29999-126">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="29999-127">Birincil defterin hareketleri bir günlükte veya nakil katmanı deftere nakil katmanına karşılık gelen bir kaynak belgede oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="29999-127">The transactions of the primary book are created in a journal or source document where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="29999-128">Deftere nakil sırasında türetilmiş defter hareketleri uygun deftere nakil katmanlarına nakledilecektir.</span><span class="sxs-lookup"><span data-stu-id="29999-128">During posting, the derived book transactions will be posted to the appropriate posting layers.</span></span> 


<span data-ttu-id="29999-129">Daha fazla bilgi için bkz. [Türetilmiş defterler](derived-books.md) ve [Türetilen defterlerle deftere nakletme](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="29999-129">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]