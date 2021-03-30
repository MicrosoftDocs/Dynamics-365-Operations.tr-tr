---
title: Değer modelleri ayarlama
description: Bu yordam, yeni bir sabit kıymet defterini nasıl oluşturacağınızı ve bir sabit kıymet grubuyla nasıl ilişkilendireceğinizi gösterir.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88c6ee10fa0a208f0946cf0f4e6bb73cb61203a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213544"
---
# <a name="set-up-value-models"></a><span data-ttu-id="fc056-103">Değer modelleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="fc056-103">Set up value models</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc056-104">Bu yordam, yeni bir sabit kıymet defterini nasıl oluşturacağınızı ve bir sabit kıymet grubuyla nasıl ilişkilendireceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc056-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="fc056-105">Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="fc056-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="fc056-106">Defter oluşturma</span><span class="sxs-lookup"><span data-stu-id="fc056-106">Create a book</span></span>
1. <span data-ttu-id="fc056-107">Sabit kıymetler > Kurulum > Defterler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="fc056-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="fc056-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc056-108">Click New.</span></span>
3. <span data-ttu-id="fc056-109">Defter alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="fc056-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="fc056-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="fc056-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="fc056-111">Amortismanı hesapla seçilirse, ilişkili kıymet defteri amortisman tekliflerine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="fc056-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="fc056-112">Seçilmezse, kıymet defterine otomatik olarak amortisman uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="fc056-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="fc056-113">Amortisman hesapla alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fc056-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="fc056-114">Amortisman profili alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="fc056-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="fc056-115">Alternatif bir amortisman profili de aynı zamanda amortisman geçiş yöntemi olarak bilinir.</span><span class="sxs-lookup"><span data-stu-id="fc056-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="fc056-116">Alternatif profil, varsayılan amortisman profilininkine eşit veya ondan büyük bir amortisman tutarı hesaplarsa, amortisman teklifi bu profile geçer.</span><span class="sxs-lookup"><span data-stu-id="fc056-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="fc056-117">Olağandışı durumlarda bir kıymetin ek amortismanı için Olağandışı amortisman profili kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fc056-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="fc056-118">Örneğin bunu doğal felaketlerden kaynaklanan amortismanı kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fc056-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="fc056-119">Temel düzeltmeler bulunan amortisman düzeltmeleri oluştur seçilirse, kıymetin değeri güncelleştirildiği zaman otomatik olarak amortisman düzeltmeleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="fc056-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="fc056-120">Seçilmezse, güncelleştirilmiş kıymet değeri yalnızca ilerideki amortisman hesaplamalarını etkiler.</span><span class="sxs-lookup"><span data-stu-id="fc056-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="fc056-121">Temel düzeltmeler bulunan Amortisman düzeltmeleri oluştur alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fc056-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="fc056-122">Varsayılan olarak, sabit kıymet defteri hareketlerini genel muhasebeye nakleder.</span><span class="sxs-lookup"><span data-stu-id="fc056-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="fc056-123">Defter için genel muhasebeye nakil işlemini, Genel muhasebeye naklet alanını Hayır olarak ayarlayarak devre dışı bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fc056-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="fc056-124">Genel muhasebeye nakledilmeyen defterler genellikle vergi raporlama amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fc056-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="fc056-125">Bu, genel muhasebeye taahhütte bulunulmadığından kıymet defterine ait geçmiş hareketleri silmek için size ek bir esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="fc056-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="fc056-126">Defter genel muhasebeye nakledilirse deftere nakil katmanı, Geçerli katmanın varsayılan değeri olur ve genel muhasebeye nakledilmezse Hiçbiri olur.</span><span class="sxs-lookup"><span data-stu-id="fc056-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="fc056-127">Bu defter için hareketlerin başka bir katmana nakledilmesi gerekiyorsa Deftere nakil katmanını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="fc056-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="fc056-128">Takvim alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fc056-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="fc056-129">Türetilmiş defterler hareketleri aynı anda farklı defterlere nakleder.</span><span class="sxs-lookup"><span data-stu-id="fc056-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="fc056-130">Hareketleri birincil defter ile oluşturursunuz ve deftere nakletme sırasında hareketin tam bir kopyası türev defterine nakledilir.</span><span class="sxs-lookup"><span data-stu-id="fc056-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="fc056-131">Türev defteri hareketleriyle yeniden hesaplama olmaz, bu nedenle amortisman hareketlerinde kullanılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="fc056-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="fc056-132">Defteri bir sabit kıymet grubuyla ilişkilendirin</span><span class="sxs-lookup"><span data-stu-id="fc056-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="fc056-133">Sabit kıymet grupları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc056-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="fc056-134">Sabit kıymet grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="fc056-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="fc056-135">Servis ömrü alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="fc056-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="fc056-136">Amortisman dönemlerinin, Servis ömrü ayarlandıktan sonra hesaplandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="fc056-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="fc056-137">Amortisman yöntemini, vergi amaçları için gerektiği şekilde ayarlama olanağınız vardır.</span><span class="sxs-lookup"><span data-stu-id="fc056-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]