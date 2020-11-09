---
title: El ile navlun mutabakatı sağlama
description: Bu yordam navlunun el ile nasıl mutabık kılınacağını gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc4fc51955544df4d0156a4c83bcc5b5a0e13df3
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016989"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="a5917-103">El ile navlun mutabakatı sağlama</span><span class="sxs-lookup"><span data-stu-id="a5917-103">Reconcile freight manually</span></span>

<span data-ttu-id="a5917-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="a5917-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="a5917-105">Bu yordam navlunun el ile nasıl mutabık kılınacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5917-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="a5917-106">Bu genellikle taşımacılık düzenleyicisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="a5917-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="a5917-107">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5917-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="a5917-108">Mutabık kılınacak yükü seçme</span><span class="sxs-lookup"><span data-stu-id="a5917-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="a5917-109">Taşıma yönetimi > Planlama > Yük planlama çalışma ekranına gidin.</span><span class="sxs-lookup"><span data-stu-id="a5917-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="a5917-110">Sevk edileni ve teslim alınanı gizle onay kutusunu temizleyin.</span><span class="sxs-lookup"><span data-stu-id="a5917-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="a5917-111">Listede yük kimliği 00006 olan yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="a5917-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="a5917-112">Taşıyıcı faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="a5917-112">Create a carrier invoice</span></span>
<span data-ttu-id="a5917-113">Navlunu el ile mutabık kılarsanız ve taşıyıcı faturasını otomatik olarak almazsanız navlun faturasına göre bir fatura oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5917-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="a5917-114">İlgili bilgiler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5917-114">Click Related information.</span></span>
2. <span data-ttu-id="a5917-115">Navlun faturası ayrıntıları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5917-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="a5917-116">Navlun faturası oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5917-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="a5917-117">Fatura alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a5917-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="a5917-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5917-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="a5917-119">Fatura için mutabakat sağlama</span><span class="sxs-lookup"><span data-stu-id="a5917-119">Reconcile the invoice</span></span>
<span data-ttu-id="a5917-120">Taşıyıcı faturasını ve navlun faturasını mutabık kıldığınızda bu işlem satır satır yapılır.</span><span class="sxs-lookup"><span data-stu-id="a5917-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="a5917-121">Navlun faturaları ile faturaları eşleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5917-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="a5917-122">Fatura ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a5917-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="a5917-123">Eşleştirilmeyen navlun fatura ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a5917-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="a5917-124">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a5917-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="a5917-125">Eşleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5917-125">Click Match.</span></span>
6. <span data-ttu-id="a5917-126">Eşleştirilen navlun faturası ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a5917-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="a5917-127">Faturayı onay için gönder</span><span class="sxs-lookup"><span data-stu-id="a5917-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="a5917-128">Onay için gönder'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5917-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="a5917-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a5917-129">Close the page.</span></span>
3. <span data-ttu-id="a5917-130">Onaylananı gizle onay kutusunu temizleyin.</span><span class="sxs-lookup"><span data-stu-id="a5917-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="a5917-131">Satıcı fatura günlükleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5917-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="a5917-132">Referans günlük numarası alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5917-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="a5917-133">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5917-133">Click Lines.</span></span>

