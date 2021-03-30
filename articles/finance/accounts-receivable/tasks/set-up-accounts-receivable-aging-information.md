---
title: Alacak hesapları yaşlandırma bilgilerini ayarlama ve oluşturma
description: Bu kılavuz, yaşlandırma dönemi tanımı yapmanıza, müşteri bakiyelerini yaşlandırmanıza, Yaşlandırılmış bakiye listesinde ve Tahsilatlar sayfasında bakiyeleri görüntülemenize yardımcı olur.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b21fe217aacd11821ff8d5cf7c7682b2181e36c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220095"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="65d59-103">Alacak hesapları yaşlandırma bilgilerini ayarlama ve oluşturma</span><span class="sxs-lookup"><span data-stu-id="65d59-103">Set up and generate accounts receivable aging information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65d59-104">Bu kılavuz, yaşlandırma dönemi tanımı yapmanıza, müşteri bakiyelerini yaşlandırmanıza, Yaşlandırılmış bakiye listesinde ve Tahsilatlar sayfasında bakiyeleri görüntülemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="65d59-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="65d59-105">Bu kayıtta USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="65d59-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="65d59-106">Yaşlandırma dönemi tanımı oluşturun</span><span class="sxs-lookup"><span data-stu-id="65d59-106">Create an aging period definition</span></span>
1. <span data-ttu-id="65d59-107">**Gezinti bölmesinde Modüller > Alacak ve tahsilatlar > Kurulum > Yaşlandırma dönemi tanımları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="65d59-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Aging period definitions**.</span></span>
2. <span data-ttu-id="65d59-108">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="65d59-108">Click **New**.</span></span>
3. <span data-ttu-id="65d59-109">**Yaşlandırma dönemi tanımı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="65d59-109">In the **Aging period definition** field, type a value.</span></span>
4. <span data-ttu-id="65d59-110">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="65d59-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="65d59-111">Yeni yaşlandırma dönemi eklemek için **Alta ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="65d59-111">Click **Add below** to insert a new aging period.</span></span>
6. <span data-ttu-id="65d59-112">**Dönem** alanına, yaşlandırma raporlarını göstermek için açıklamayı girin.</span><span class="sxs-lookup"><span data-stu-id="65d59-112">In the **Period** field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="65d59-113">**Birim** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="65d59-113">In the **Unit** field, enter a number.</span></span>
8. <span data-ttu-id="65d59-114">**Aralık** alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="65d59-114">In the **Interval** field, select an option.</span></span> <span data-ttu-id="65d59-115">Genel muhasebe dönemi, genel muhasebe takviminize denk gelir.</span><span class="sxs-lookup"><span data-stu-id="65d59-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="65d59-116">Gün, hafta, ay, üç aylık dönem ve yıl, tarih türüne aralığın boyutunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="65d59-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="65d59-117">Sınırsız seçeneği, dönemin ilk veya son dönem olmasına bağlı olarak, önceki veya sonraki hareketlerin tümünü seçer.</span><span class="sxs-lookup"><span data-stu-id="65d59-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="65d59-118">**Yaşlandırma göstergesi** alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="65d59-118">In the **Aging indicator** field, select an option.</span></span>
10. <span data-ttu-id="65d59-119">Kılavuzun en üstündeki dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="65d59-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="65d59-120">Yaşlandırma dönemi tanımındaki en eski dönemi belirtmek için açıklamayı güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="65d59-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="65d59-121">**Dönem** alanına, yaşlandırma döneminin yeni açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="65d59-121">In the **Period** field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="65d59-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="65d59-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="65d59-123">Bakiyeleri yaşlandırın</span><span class="sxs-lookup"><span data-stu-id="65d59-123">Age the balances</span></span>
1. <span data-ttu-id="65d59-124">**Alacak ve tahsilatlar > Dönemsel görevler > Müşteri bakiyelerini yaşlandır**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="65d59-124">Go to **Credit and collections > Periodic tasks > Age customer balances**.</span></span>
2. <span data-ttu-id="65d59-125">**Yaşlandırma dönemi tanımı** alanında, oluşturduğunuz yaşlandırma dönemi tanımını seçin.</span><span class="sxs-lookup"><span data-stu-id="65d59-125">In the **Aging period definition** field, select the aging period definition that you created.</span></span>
    + <span data-ttu-id="65d59-126">Her yaşlandırma dönemi için birer etkin anlık görüntü alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65d59-126">You can have one active snapshot for each aging period definition.</span></span>  
    + <span data-ttu-id="65d59-127">Tüm müşteriler varsayılan olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="65d59-127">All customers are processed by default.</span></span> <span data-ttu-id="65d59-128">Tek bir müşteri tahsilatları havuzu hesaplamak için bu seçimi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65d59-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    + <span data-ttu-id="65d59-129">Yaşlandırma için kullanacağınız hareketten tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="65d59-129">Select the date from the transaction that you will use for the aging.</span></span>  
    + <span data-ttu-id="65d59-130">Yaşlandırma için bir "başlangıç" tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="65d59-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="65d59-131">Varsayılan değer bugündür, ancak bu alanı Seçili tarih olarak değiştirirseniz, istediğiniz tarihi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65d59-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="65d59-132">Toplu işlem için, Bugünün tarihi'ni kullanın.</span><span class="sxs-lookup"><span data-stu-id="65d59-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="65d59-133">**Şirket** aralığını genişletin.</span><span class="sxs-lookup"><span data-stu-id="65d59-133">Expand the **Company** range.</span></span> <span data-ttu-id="65d59-134">Anlık görüntüye dahil edilecek şirketleri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65d59-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="65d59-135">Geçerli şirket varsayılan olarak seçilidir.</span><span class="sxs-lookup"><span data-stu-id="65d59-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="65d59-136">Anlık görüntüyü işlemek için **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="65d59-136">Click **Ok** to process the snapshot.</span></span> <span data-ttu-id="65d59-137">Bu işlem biraz zaman alır, bu nedenle sürgünün kaybolmasını bekleyin ve mesaj merkezinde mesaj görüntülenip görüntülenmediğini kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="65d59-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="65d59-138">Tahsilat sayfasında Yaşlandırılmış bakiyeler listesini görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="65d59-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="65d59-139">**Alacak ve tahsilatlar > Tahsilatlar > Yaşlandırılmış bakiyeler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="65d59-139">Go to **Credit and collections > Collections > Aged balances**.</span></span> <span data-ttu-id="65d59-140">Liste sayfası müşteri bakiyelerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="65d59-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="65d59-141">Yaşlandırma simgesi, en eski hareketin yaşlandırma dönemini gösterir.</span><span class="sxs-lookup"><span data-stu-id="65d59-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="65d59-142">Bakiyesi olan bir müşteri seçin.</span><span class="sxs-lookup"><span data-stu-id="65d59-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="65d59-143">Yaşlandırılmış bakiyeleri görüntülemek için **Yaşlandırma bilgi** kutusu alanını genişletin.</span><span class="sxs-lookup"><span data-stu-id="65d59-143">Expand the **Aging fact** box area to view the aged balances.</span></span> <span data-ttu-id="65d59-144">Bilgi kutusu için yaşlandırma dönemi tanımı, parametrelerde belirtilmiş varsayılan yaşlandırma dönem tanımından alınır.</span><span class="sxs-lookup"><span data-stu-id="65d59-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="65d59-145">Bunu, Toplama menüsünü kullanarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65d59-145">You can change it using the Collect menu.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]