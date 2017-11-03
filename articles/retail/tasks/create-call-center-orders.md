--- 
title: " Çağrı merkezi siparişleri oluşturma"
description: "Bu yordam bir müşteri arama, yeni bir sipariş oluşturma, bir ürün arama ve müşteriden ödeme tahsil etme için kılavuzluk sağlar."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f702690f72b3e299f6c2744da326a23d5753eb5d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-call-center-orders"></a><span data-ttu-id="e50b2-103"> Çağrı merkezi siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="e50b2-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e50b2-104">Bu yordam bir müşteri arama, yeni bir sipariş oluşturma, bir ürün arama ve müşteriden ödeme tahsil etme için kılavuzluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="e50b2-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="e50b2-105">Bu yordam, USRT demo veri şirketini kullanır ve Satış Siparişi Memurlarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="e50b2-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="e50b2-106">Ön koşullar: Yordamı tamamlayan kullanıcı Çağrı merkezi kullanıcısı olarak ayarlanır ve en az bir Kaynak kodla Fabrikam Yarı Yıllık Kataloğu yayınlanır.</span><span class="sxs-lookup"><span data-stu-id="e50b2-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="e50b2-107">Perakende ve ticaret > Müşterileri > Müşteri hizmetlerine gidin.</span><span class="sxs-lookup"><span data-stu-id="e50b2-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="e50b2-108">SearchText alanında müşteri aramak için arama ölçütü girin.</span><span class="sxs-lookup"><span data-stu-id="e50b2-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="e50b2-109">Bu örnek yordam için 'karen' yazın ve sekme tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="e50b2-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="e50b2-110">Ara'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e50b2-110">Click Search.</span></span>
    * <span data-ttu-id="e50b2-111">Demo veride Karen adında tek bir müşteri olduğundan otomatik olarak seçililer.</span><span class="sxs-lookup"><span data-stu-id="e50b2-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="e50b2-112">Yeni satış siparişine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e50b2-112">Click New sales order.</span></span>
5. <span data-ttu-id="e50b2-113">Satış siparişi başlığı bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="e50b2-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="e50b2-114">Katalog için kaynak kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="e50b2-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="e50b2-115">Hiçbir etkin Kaynak kodu yoksa, Kaynak alanını kapatıp bu adımı atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e50b2-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="e50b2-116">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e50b2-116">Click Add line.</span></span>
8. <span data-ttu-id="e50b2-117">Madde numarası alanına madde arama terimini girin.</span><span class="sxs-lookup"><span data-stu-id="e50b2-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="e50b2-118">Bu örnek yordamda "8111" kısmi madde numarasını girin ve sekme tuşuna basın. Bu madde arama penceresinin açılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="e50b2-118">For this sample procedure enter a partial item number of '8111' and press tab. This will pop up the item search window.</span></span>  
9. <span data-ttu-id="e50b2-119">Satış siparişine eklenecek ürünü seçin</span><span class="sxs-lookup"><span data-stu-id="e50b2-119">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="e50b2-120">Satış miktarını girin.</span><span class="sxs-lookup"><span data-stu-id="e50b2-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="e50b2-121">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e50b2-121">Click Create.</span></span>
12. <span data-ttu-id="e50b2-122">Müşteri ödemesi yakalamayı tamamla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e50b2-122">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="e50b2-123">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e50b2-123">Click Add.</span></span>
    * <span data-ttu-id="e50b2-124">Ekle bağlantısı Ödemeler sekmesinde bulunur. Daraltılmışsa Ödemeler sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="e50b2-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="e50b2-125">Ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="e50b2-125">Select the payment method.</span></span>
    * <span data-ttu-id="e50b2-126">Bu yordam için nakit ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="e50b2-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="e50b2-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e50b2-127">Close the page.</span></span>
16. <span data-ttu-id="e50b2-128">Tutarı girin.</span><span class="sxs-lookup"><span data-stu-id="e50b2-128">Enter the amount.</span></span>
    * <span data-ttu-id="e50b2-129">Bu yordam için, tutar alanının sol tarafındaki Satış siparişi özet sayfasında görebileceğiniz sipariş bakiyesine eşit bir tutar girin.</span><span class="sxs-lookup"><span data-stu-id="e50b2-129">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="e50b2-130">Siparişi tamamen ödenmiş olarak tamamlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="e50b2-130">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="e50b2-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e50b2-131">Click OK.</span></span>
18. <span data-ttu-id="e50b2-132">Gönder'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e50b2-132">Click Submit.</span></span>

