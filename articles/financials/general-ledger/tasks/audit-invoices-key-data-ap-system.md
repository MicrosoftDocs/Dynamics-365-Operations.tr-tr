--- 
title: "Borç hesaplarındaki faturaları ve önemli verileri denetleme"
description: "Satınalma siparişindeki mal ve hizmetler için satıcıdan bir fatura aldığınızda, iş süreçleri faturanın ödeme onayı alabilmesi için mal veya hizmetlerin alınmış olmasını gerektirebilir."
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5cd9448c95b7ec0c4a82aca3d21d961259dfb109
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="6d46e-103">Borç hesaplarındaki faturaları ve önemli verileri denetleme</span><span class="sxs-lookup"><span data-stu-id="6d46e-103">Audit invoices and key data in accounts payable</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d46e-104">Satınalma siparişindeki mal ve hizmetler için satıcıdan bir fatura aldığınızda, iş süreçleri faturanın ödeme onayı alabilmesi için mal veya hizmetlerin alınmış olmasını gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="6d46e-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="6d46e-105">Başlamadan önce Fatura eşleştirme yapılandırma anahtarının seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="6d46e-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="6d46e-106">Borç hesapları parametreleri sayfasında Fatura eşleştirme doğrulaması seçeneğinin işaretlendiğinden, Uyuşmazlıkları olan faturayı deftere naklet alanı ayarının Onay gerektir yapıldığından ve Satır eşleme ilkesi ayarının Üç yönlü eşleştirme yapıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="6d46e-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="6d46e-107">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6d46e-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="6d46e-108">Bu adımları borç hesapları yöneticisi veya muhasebe müdürü rolü gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="6d46e-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="6d46e-109">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6d46e-109">Create a purchase order</span></span>
1. <span data-ttu-id="6d46e-110">Tüm satınalma siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6d46e-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="6d46e-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-111">Click New.</span></span>
3. <span data-ttu-id="6d46e-112">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6d46e-113">Satıcı hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6d46e-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="6d46e-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-114">Click OK.</span></span>
6. <span data-ttu-id="6d46e-115">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-115">Click Add line.</span></span>
7. <span data-ttu-id="6d46e-116">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6d46e-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="6d46e-117">Eylem Bölmesinde, Satınalma öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="6d46e-118">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="6d46e-119">Ürün girişini deftere nakledin</span><span class="sxs-lookup"><span data-stu-id="6d46e-119">Post a product receipt</span></span>
1. <span data-ttu-id="6d46e-120">Eylem Bölmesinde, Al öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="6d46e-121">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-121">Click Product receipt.</span></span>
3. <span data-ttu-id="6d46e-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6d46e-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6d46e-123">Ürün girişi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6d46e-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="6d46e-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="6d46e-125">Satıcı faturasını kaydedin ve bir ürün girişiyle eşleyin</span><span class="sxs-lookup"><span data-stu-id="6d46e-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="6d46e-126">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="6d46e-127">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-127">Click Invoice.</span></span>
3. <span data-ttu-id="6d46e-128">Numara alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6d46e-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="6d46e-129">Varsayılan başlangıç: Sipariş miktarı'na tıklayarak açılır iletişim kutusunu açın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="6d46e-130">Satırlar için varsayılan miktar alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="6d46e-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="6d46e-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-131">Click OK.</span></span>
7. <span data-ttu-id="6d46e-132">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-132">Click Yes.</span></span>
8. <span data-ttu-id="6d46e-133">Ürün girişlerini eşleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="6d46e-134">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-134">Click OK.</span></span>
10. <span data-ttu-id="6d46e-135">Eylem Bölmesinde, Gözden geçir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="6d46e-136">Eşleşme ayrıntıları öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d46e-136">Click Matching details.</span></span>


