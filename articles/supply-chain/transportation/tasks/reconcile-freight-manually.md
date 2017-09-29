--- 
title: "El ile navlun mutabakatı sağlama"
description: "Bu yordam navlunun el ile nasıl mutabık kılınacağını gösterir."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 15148725664d839694ede8419213d881c7be83dd
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="af2dd-103">El ile navlun mutabakatı sağlama</span><span class="sxs-lookup"><span data-stu-id="af2dd-103">Reconcile freight manually</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af2dd-104">Bu yordam navlunun el ile nasıl mutabık kılınacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af2dd-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="af2dd-105">Bu genellikle taşımacılık düzenleyicisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="af2dd-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="af2dd-106">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af2dd-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="af2dd-107">Mutabık kılınacak yükü seçme</span><span class="sxs-lookup"><span data-stu-id="af2dd-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="af2dd-108">Taşıma yönetimi > Planlama > Yük planlama çalışma ekranına gidin.</span><span class="sxs-lookup"><span data-stu-id="af2dd-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="af2dd-109">Sevk edileni ve teslim alınanı gizle onay kutusunu temizleyin.</span><span class="sxs-lookup"><span data-stu-id="af2dd-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="af2dd-110">Listede yük kimliği 00006 olan yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="af2dd-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="af2dd-111">Taşıyıcı faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="af2dd-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="af2dd-112">Navlunu el ile mutabık kılarsanız ve taşıyıcı faturasını otomatik olarak almazsanız navlun faturasına göre bir fatura oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af2dd-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="af2dd-113">İlgili bilgiler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af2dd-113">Click Related information.</span></span>
2. <span data-ttu-id="af2dd-114">Navlun faturası ayrıntıları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af2dd-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="af2dd-115">Navlun faturası oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af2dd-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="af2dd-116">Fatura alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="af2dd-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="af2dd-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af2dd-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="af2dd-118">Fatura için mutabakat sağlama</span><span class="sxs-lookup"><span data-stu-id="af2dd-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="af2dd-119">Taşıyıcı faturasını ve navlun faturasını mutabık kıldığınızda bu işlem satır satır yapılır.</span><span class="sxs-lookup"><span data-stu-id="af2dd-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="af2dd-120">Navlun faturaları ile faturaları eşleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af2dd-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="af2dd-121">Fatura ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="af2dd-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="af2dd-122">Eşleştirilmeyen navlun fatura ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="af2dd-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="af2dd-123">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="af2dd-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="af2dd-124">Eşleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af2dd-124">Click Match.</span></span>
6. <span data-ttu-id="af2dd-125">Eşleştirilen navlun faturası ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="af2dd-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="af2dd-126">Faturayı onay için gönder</span><span class="sxs-lookup"><span data-stu-id="af2dd-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="af2dd-127">Onay için gönder'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af2dd-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="af2dd-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="af2dd-128">Close the page.</span></span>
3. <span data-ttu-id="af2dd-129">Onaylananı gizle onay kutusunu temizleyin.</span><span class="sxs-lookup"><span data-stu-id="af2dd-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="af2dd-130">Satıcı fatura günlükleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af2dd-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="af2dd-131">Referans günlük numarası alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af2dd-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="af2dd-132">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af2dd-132">Click Lines.</span></span>


