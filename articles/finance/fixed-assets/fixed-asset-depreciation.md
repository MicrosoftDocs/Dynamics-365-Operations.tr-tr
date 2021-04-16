---
title: Sabit kıymet amortismanı
description: Bu konuda sabit kıymetlerin amortismanına genel bir bakış sunulmuştur.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ec8544b885485781b0b9c0a59ec47f90fdceb6b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826894"
---
# <a name="fixed-asset-depreciation"></a><span data-ttu-id="ca719-103">Sabit kıymet amortismanı</span><span class="sxs-lookup"><span data-stu-id="ca719-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca719-104">Bu konuda sabit kıymetlerin amortismanına genel bir bakış sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="ca719-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="ca719-105">Amortisman, normalde sabit varlığın değerini bilançoda düşüren periyodik bir harekettir ve kâr-zarar hesabından bir masraf olarak düşülür.</span><span class="sxs-lookup"><span data-stu-id="ca719-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="ca719-106">Bu nedenle ana hesap bilançoda genellikle periyodik amortismanı alacaklandırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ca719-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="ca719-107">Mahsup hesap, hesap planının kâr ve zarar bölümündeki bir hesaptır.</span><span class="sxs-lookup"><span data-stu-id="ca719-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="ca719-108">Amortisman Düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="ca719-108">Depreciation adjustment</span></span>
<span data-ttu-id="ca719-109">Genellikle, yalnızca deftere nakledilmiş bir amortisman hareketine yönelik düzeltmeler bir amortisman düzeltmesi şeklinde deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="ca719-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="ca719-110">Bu nedenle ana hesap ve mahsup hesap tıpkı amortisman hesapları gibi ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ca719-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="ca719-111">Amortisman düzeltmesi olumlu veya olumsuz bir tutar olabilir, ancak ana hesabın (bir bilanço hesabı olarak) ve mahsup hesabın (genellikle bir kar ve zarar hesabı olarak) işlevselliği aynı kalır.</span><span class="sxs-lookup"><span data-stu-id="ca719-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="ca719-112">Olağandışı amortisman</span><span class="sxs-lookup"><span data-stu-id="ca719-112">Extraordinary depreciation</span></span>
<span data-ttu-id="ca719-113">Olağandışı amortisman, temel amortisman gibi çalışır.</span><span class="sxs-lookup"><span data-stu-id="ca719-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="ca719-114">Bu nedenle, bir ana hesap bilançoya amortisman tutarını alacaklandırmak ve sabit kıymetin değerini azaltmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ca719-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="ca719-115">Mahsup hesap, mali dönem için hesaplanan amortismanın bir harcama olarak kaydedildiği kâr-zarar hesabıdır.</span><span class="sxs-lookup"><span data-stu-id="ca719-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="ca719-116">Olağandışı amortisman, temel amortismandan bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="ca719-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="ca719-117">Olağandışı amortismanı ayrı bir hareket türü olarak kullanarak olağandışı amortismanı temel amortismandan farklı olarak deftere nakledebilir ve raporlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca719-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="ca719-118">Özel amortisman payı</span><span class="sxs-lookup"><span data-stu-id="ca719-118">Special depreciation allowance</span></span>
<span data-ttu-id="ca719-119">Kıymetin servise konulduğu ve amortismana ayrıldığı ilk yıl süresince fazladan amortisman tutarları almak için özel amortisman paylarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca719-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="ca719-120">Özel amortisman paylarının diğer her türlü amortisman hesaplamasından önce alınması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca719-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="ca719-121">Özel amortisman payları genellikle sabit kıymetin servis ömrünün ileriki zamanlarına kadar bilinmediğinden bu amortisman türünü genel muhasebeye nakledilmeyen bir defter ile kullanmak en iyisidir.</span><span class="sxs-lookup"><span data-stu-id="ca719-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="ca719-122">Bu defterlerin hareket geçmişlerini, Genel muhasebe defterine nakledilmeyen hareketleri sil periyodik işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca719-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="ca719-123">Ardından sabit kıymet defteri için amortisman geçmişini silebilir, bilindiği zaman özel amortisman payını deftere nakledebilir ve ardından yıl için kalan amortisman hareketlerini deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca719-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="ca719-124">Sınırsız sayıda özel amortisman payı kaydı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca719-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="ca719-125">Bu kayıtları, bir kıymet grubu defterine atadıktan sonra kıymet defterine uygulanırlar.</span><span class="sxs-lookup"><span data-stu-id="ca719-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="ca719-126">Özel amortisman payı yüzde veya sabit bir tutar olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="ca719-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="ca719-127">Amortisman tekliflerini naklettiğinizde, özel amortisman payı hareketleri amortisman hareketlerinden bağımsız hareketler olarak deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="ca719-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="ca719-128">Amortisman takvimleri</span><span class="sxs-lookup"><span data-stu-id="ca719-128">Depreciation calendars</span></span>
<span data-ttu-id="ca719-129">Her defterin sabit kıymetlere amortisman ayırırken kullanılan bir takvimi vardır.</span><span class="sxs-lookup"><span data-stu-id="ca719-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="ca719-130">Varsayılan olarak, defterde bir takvim belirtmezseniz defter, muhasebe mali takvimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ca719-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="ca719-131">Defter ile ilişkili amortisman profili bir mali amortisman yılını kullandığında defter için bir mali takvim seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca719-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="ca719-132">Genel muhasebe defterinde **Mali takvimler** sayfasını kullanarak paylaşılan takvimler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca719-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="ca719-133">Daha fazla bilgi için bkz: [Amortisman yöntemleri ve kuralları](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="ca719-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]