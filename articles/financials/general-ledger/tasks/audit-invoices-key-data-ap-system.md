---
title: AP sistemindeki denetim faturaları ve anahtar veriler
description: Satınalma siparişindeki mal ve hizmetler için satıcıdan bir fatura aldığınızda, iş süreçleri faturanın ödeme onayı alabilmesi için mal veya hizmetlerin alınmış olmasını gerektirebilir.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 946076d682a10becdc2c4a8baff7f52de7893119
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "331541"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="b54c8-103">AP sistemindeki denetim faturaları ve anahtar veriler</span><span class="sxs-lookup"><span data-stu-id="b54c8-103">Audit invoices and key data in AP system</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b54c8-104">Satınalma siparişindeki mal ve hizmetler için satıcıdan bir fatura aldığınızda, iş süreçleri faturanın ödeme onayı alabilmesi için mal veya hizmetlerin alınmış olmasını gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="b54c8-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="b54c8-105">Başlamadan önce Fatura eşleştirme yapılandırma anahtarının seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="b54c8-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="b54c8-106">Borç hesapları parametreleri sayfasında Fatura eşleştirme doğrulaması seçeneğinin işaretlendiğinden, Uyuşmazlıkları olan faturayı deftere naklet alanı ayarının Onay gerektir yapıldığından ve Satır eşleme ilkesi ayarının Üç yönlü eşleştirme yapıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="b54c8-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="b54c8-107">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b54c8-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="b54c8-108">Bu adımları borç hesapları yöneticisi veya muhasebe müdürü rolü gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="b54c8-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="b54c8-109">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b54c8-109">Create a purchase order</span></span>
1. <span data-ttu-id="b54c8-110">**Tüm satınalma siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b54c8-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="b54c8-111">**Yeni**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-111">Click **New**.</span></span>
3. <span data-ttu-id="b54c8-112">**Satıcı hesabı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b54c8-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="b54c8-113">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-113">Click **OK**.</span></span>
5. <span data-ttu-id="b54c8-114">**Satır ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-114">Click **Add line**.</span></span>
6. <span data-ttu-id="b54c8-115">**Madde numarası** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b54c8-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="b54c8-116">Eylem Bölmesinde, **Satınalma** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="b54c8-117">**Onayla**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="b54c8-118">Ürün girişini deftere nakledin</span><span class="sxs-lookup"><span data-stu-id="b54c8-118">Post a product receipt</span></span>
1. <span data-ttu-id="b54c8-119">Eylem Bölmesinde, **Teslim al** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="b54c8-120">**Ürün girişi** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="b54c8-121">**Ürün girişi** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b54c8-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="b54c8-122">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="b54c8-123">Satıcı faturasını kaydedin ve bir ürün girişiyle eşleyin</span><span class="sxs-lookup"><span data-stu-id="b54c8-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="b54c8-124">Eylem Bölmesinde, **Fatura > Fatura** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="b54c8-125">**Numara** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b54c8-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="b54c8-126">**Varsayılan başlangıç: Sipariş miktarı**'na tıklayarak açılır iletişim kutusunu açın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="b54c8-127">**Satırlar için varsayılan miktar** alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="b54c8-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="b54c8-128">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-128">Click **OK**.</span></span>
6. <span data-ttu-id="b54c8-129">**Evet** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-129">Click **Yes**.</span></span>
7. <span data-ttu-id="b54c8-130">**Ürün girişlerini eşleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="b54c8-131">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-131">Click **OK**.</span></span>
9. <span data-ttu-id="b54c8-132">Eylem Bölmesinde, **Gözden geçir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="b54c8-133">**Eşleşme ayrıntıları** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b54c8-133">Click **Matching details**.</span></span>

