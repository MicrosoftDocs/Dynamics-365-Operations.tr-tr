---
title: Borç hesaplarından kıymetler oluşturup alın
description: Bu görev kılavuzu size satınalma işlemiyle sabit kıymet oluşturma ve alımını gösterecek.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6c36338cc67855c79ec97d88bb8b633417b85c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562473"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="da7b6-103">Borç hesaplarından kıymetler oluşturup alın</span><span class="sxs-lookup"><span data-stu-id="da7b6-103">Create and acquire assets from Accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da7b6-104">Bu görev kılavuzu size satınalma işlemiyle sabit kıymet oluşturma ve alımını gösterecek.</span><span class="sxs-lookup"><span data-stu-id="da7b6-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="da7b6-105">Kılavuzda Muhasebeci, Borç hesabı memurları ve demo USMF şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="da7b6-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="da7b6-106">Sabit kıymet parametrelerini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="da7b6-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="da7b6-107">Sabit kıymetler > Kurulum > Sabit kıymet parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="da7b6-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="da7b6-108">Satınalma siparişleri bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="da7b6-109">Satınalmadan kıymet alımına izin ver onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="da7b6-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="da7b6-110">Ürün girişi veya fatura deftere nakil işlemi sırasında kıymet oluştur onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="da7b6-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="da7b6-111">Yeni bir satıcı faturası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="da7b6-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="da7b6-112">Borç hesapları > Çalışma alanları > Satıcı faturası girişi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="da7b6-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="da7b6-113">Yeni satıcı faturası'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="da7b6-114">Fatura hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="da7b6-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="da7b6-116">Numara alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="da7b6-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="da7b6-117">Deftere nakil tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="da7b6-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="da7b6-118">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-118">Click Add line.</span></span>
8. <span data-ttu-id="da7b6-119">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="da7b6-120">Sabit kıymet alımı için ya stoğu olmayan maddeler veya tedarik kategorileri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="da7b6-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="da7b6-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="da7b6-122">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="da7b6-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="da7b6-123">Bir fatura satırı, miktarı ne olursa olsun tek bir sabit kıymet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da7b6-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="da7b6-124">Fatura miktarı alanı değeri, sabit kıymet miktarına aktarılır.</span><span class="sxs-lookup"><span data-stu-id="da7b6-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="da7b6-125">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="da7b6-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="da7b6-126">Satır ayrıntıları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="da7b6-127">Sabit kıymetler sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="da7b6-128">Yeni bir sabit kıymet oluştur onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="da7b6-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="da7b6-129">Sabit kıymet grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="da7b6-130">Listede, yeni sabit kıymet oluşturulurken kullanılacak sabit kıymet grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="da7b6-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="da7b6-131">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="da7b6-132">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da7b6-132">Click Post.</span></span>
    * <span data-ttu-id="da7b6-133">Sabit kıymet oluşturulur ve fatura deftere nakledildiğinde alınır.</span><span class="sxs-lookup"><span data-stu-id="da7b6-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

