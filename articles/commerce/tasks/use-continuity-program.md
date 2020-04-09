---
title: Süreklilik programı kullanma
description: Bu yordam, süreklilik programının satılmasını ve ilgili satış siparişlerinin işlenmesini gösterir.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2baf0127a35cc62952fd78daaf8204d35ec8d2b3
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141166"
---
# <a name="using-continuity-program"></a><span data-ttu-id="602fe-103">Süreklilik programı kullanma</span><span class="sxs-lookup"><span data-stu-id="602fe-103">Using continuity program</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="602fe-104">Bu yordam, süreklilik programının satılmasını ve ilgili satış siparişlerinin işlenmesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="602fe-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="602fe-105">Bu yordamı tamamlamak için kullanıcının bir çağrı merkezi kullanıcısı olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="602fe-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="602fe-106">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="602fe-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="602fe-107">Perakende ve Ticaret > Müşterileri > Müşteri hizmetlerine gidin.</span><span class="sxs-lookup"><span data-stu-id="602fe-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="602fe-108">SearchText alanına 'Karen' yazın ve ardından Sekme tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="602fe-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="602fe-109">Gelişmiş arama iletişim kutusu açılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="602fe-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="602fe-110">Açılmazsa bu alanının sağındaki Ara'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="602fe-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="602fe-111">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="602fe-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="602fe-112">Karen Berg'i gösteren yalnızca bir satır bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="602fe-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="602fe-113">Tablonun en solunda yer alan onay işareti sütununa tıklayarak satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="602fe-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="602fe-114">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="602fe-114">Click Select.</span></span>
5. <span data-ttu-id="602fe-115">Yeni satış siparişine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="602fe-115">Click New sales order.</span></span>
    * <span data-ttu-id="602fe-116">Satış siparişi numarasını not etmek iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="602fe-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="602fe-117">Bu yordamda daha sonra gerekir.</span><span class="sxs-lookup"><span data-stu-id="602fe-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="602fe-118">Madde numarası alanına "88000" yazın ve ardından Sekme tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="602fe-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="602fe-119">Bu, USRT demo verilerinde bir süreklilik öğesidir.</span><span class="sxs-lookup"><span data-stu-id="602fe-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="602fe-120">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="602fe-120">Click Complete.</span></span>
8. <span data-ttu-id="602fe-121">Ödeme yöntemi alanına "Visa" yazın.</span><span class="sxs-lookup"><span data-stu-id="602fe-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="602fe-122">Kredi kartı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="602fe-122">Click Add credit card.</span></span>
    * <span data-ttu-id="602fe-123">Gerekli kredi kartı bilgilerini bu sayfada girin.</span><span class="sxs-lookup"><span data-stu-id="602fe-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="602fe-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="602fe-124">Click OK.</span></span>
11. <span data-ttu-id="602fe-125">Ödeme bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="602fe-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="602fe-126">Çağrı merkezi siparişi göndermek için sipariş için ödemelerin girilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="602fe-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="602fe-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="602fe-127">Click OK.</span></span>
13. <span data-ttu-id="602fe-128">Gönder'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="602fe-128">Click Submit.</span></span>
    * <span data-ttu-id="602fe-129">Yeni bir süreklilik siparişi oluşturmaya hazırsınız.</span><span class="sxs-lookup"><span data-stu-id="602fe-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="602fe-130">Ardından, süreklilik siparişlerini işlemek için kullanılan iki toplu işlemi çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="602fe-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="602fe-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="602fe-131">Close the page.</span></span>
15. <span data-ttu-id="602fe-132">Perakende ve Ticaret > Süreklilik > Süreklilik ödemelerini işle'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="602fe-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="602fe-133">Süreklilik maddesi alanına "88000" yazın ve ardından Sekme tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="602fe-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="602fe-134">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="602fe-134">Click OK.</span></span>
18. <span data-ttu-id="602fe-135">Perakende ve Ticaret > Süreklilik > Süreklilik alt siparişleri oluştur'a gidin.</span><span class="sxs-lookup"><span data-stu-id="602fe-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="602fe-136">Bu işlem, süreklilik programlarınızın ayarlarına dayanarak yeni satış siparişleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="602fe-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="602fe-137">Süreklilik maddesi alanına "88000" yazın ve ardından Sekme tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="602fe-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="602fe-138">Madde "88000", USRT demo verilerinde bir süreklilik öğesidir.</span><span class="sxs-lookup"><span data-stu-id="602fe-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="602fe-139">Satış siparişi alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="602fe-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="602fe-140">Bu yordamda daha önce not ettiğiniz satış siparişi numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="602fe-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="602fe-141">Bu, bu yordam için işlem süresini minimumda tutar.</span><span class="sxs-lookup"><span data-stu-id="602fe-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="602fe-142">Satış siparişi alanı isteğe bağlıdır: Tek bir programda tüm siparişleri işleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="602fe-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="602fe-143">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="602fe-143">Click OK.</span></span>

