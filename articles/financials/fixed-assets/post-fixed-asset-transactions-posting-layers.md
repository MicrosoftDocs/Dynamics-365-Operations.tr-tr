---
title: "Sabit kıymet hareketlerini deftere nakil katmanlarında deftere nakletme"
description: "Bu makalede sabit kıymet hareketleri için katman işlevlerinin deftere nakline genel bir bakış sunulmuştur."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe92e2f0d57a1daeb2c20da91e1b60b2308dce6a
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="f6540-103">Sabit kıymet hareketlerini deftere nakil katmanlarında deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="f6540-103">Post fixed asset transactions to posting layers</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f6540-104">Bu makalede sabit kıymet hareketleri için katman işlevlerinin deftere nakline genel bir bakış sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="f6540-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="f6540-105">Bir sabit kıymet genellikle farklı amaçlarla ve farklı şekillerde amortize edilir.</span><span class="sxs-lookup"><span data-stu-id="f6540-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="f6540-106">Vergi nedeniyle yapılan amortisman, vergiler için mümkün olan en yüksek amortismanı oluşturmak amacıyla geçerli vergi kuralları kullanılarak hesaplanır, ancak raporlama amacıyla yapılan amortismanlar muhasebe kanun ve standartlarına göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="f6540-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="f6540-107">Çeşitli amortisman türleri ayrı ayrı hesaplanır ve nakil katmanlarına ayrı ayrı kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="f6540-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="f6540-108">Sabit bir değere bağlı her defter genel amortisman amacını içeren belirli bir nakil katmanı için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="f6540-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="f6540-109">On tür deftere nakil katmanı vardır: Cari, İşlemler, Vergi ve yedi Özel Katman.</span><span class="sxs-lookup"><span data-stu-id="f6540-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="f6540-110">Ayrıca Defter için genel muhasebeye nakil işlemini, Genel muhasebeye naklet alanını Hayır olarak ayarlayarak devre dışı bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6540-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="f6540-111">Ardından Deftere nakil katmanı alanı otomatik olarak Hiçbiri olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="f6540-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="f6540-112">Normalde, genel muhasebeye nakledilmeyen defterler vergi raporlama amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f6540-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="f6540-113">Bu yaklaşım, genel muhasebeye taahhütte bulunulmadığından kıymet defterine ait geçmiş hareketleri silmek için ek esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="f6540-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="f6540-114">Sabit kıymet günlükleri Genel muhasebe > Günlük ayarı > Günlük adları konumunda Günlük adları sayfası kullanılarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="f6540-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="f6540-115">Amortisman nakledebileceğiniz her günlük, yalnızca bir nakil katmanı için günlük adı ile tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="f6540-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="f6540-116">Günlükte deftere nakil katmanı değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="f6540-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="f6540-117">Bu kısıtlama her deftere nakil katmanı için hareketlerin ayrı tutulmasını garantiye almaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="f6540-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="f6540-118">Her nakil katmanı için en az bir günlük adı oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f6540-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="f6540-119">Genel muhasebeye nakledilmeyen defterler kullanıyorsanız ayrıca deftere nakil katmanı Hiçbiri olarak ayarlanan bir günlük de oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f6540-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="f6540-120">Sabit kıymet hareketleri için Sabit kıymet nakil profilleri sayfasında genel muhasebe hesapları atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6540-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="f6540-121">Her deftere nakil profili için ilgili hareket tipini ve defteri seçmeli ve ardından genel muhasebe kayıtlarını belirlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f6540-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="f6540-122">Her defter için genel muhasebeye nakleden bir deftere nakil profili kaydı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f6540-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="f6540-123">Türetilmiş defterleri kullanarak hareketleri aynı anda farklı nakil katmanlarında deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6540-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="f6540-124">Birincil defterin hareketlerini bir günlükte oluşturabilirsiniz. Burada nakil katmanı deftere nakil katmanına karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="f6540-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="f6540-125">Deftere nakil sırasında türetilmiş defter hareketleri ilgili deftere nakil katmanlarına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="f6540-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="f6540-126">Daha fazla bilgi için bkz. [Türetilmiş defterler](derived-books.md) ve [Türetilmiş defterlerle deftere nakil](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="f6540-126">For more information see, [Derived books](derived-books.md) and [Posting with derived books](post-derived-value-models.md).</span></span>




