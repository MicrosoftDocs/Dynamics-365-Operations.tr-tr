---
title: " Çağrı merkezi siparişleri oluşturma"
description: Bu yordam bir müşteri arama, yeni bir sipariş oluşturma, bir ürün arama ve müşteriden ödeme tahsil etme için kılavuzluk sağlar.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d8dc9e19ecd6b835569ba80563bce33134895cb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791667"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="b0e01-103"> Çağrı merkezi siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b0e01-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0e01-104">Bu yordam bir müşteri arama, yeni bir sipariş oluşturma, bir ürün arama ve müşteriden ödeme tahsil etme için kılavuzluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="b0e01-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="b0e01-105">Bu yordam, USRT demo veri şirketini kullanır ve Satış Siparişi Memurlarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="b0e01-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="b0e01-106">Ön koşullar: Yordamı tamamlayan kullanıcı Çağrı merkezi kullanıcısı olarak ayarlanır ve en az bir Kaynak kodla Fabrikam Yarı Yıllık Kataloğu yayınlanır.</span><span class="sxs-lookup"><span data-stu-id="b0e01-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="b0e01-107">**Perakende ve Ticaret \> Müşteriler \> Müşteri hizmetlerine gidin**.</span><span class="sxs-lookup"><span data-stu-id="b0e01-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="b0e01-108">**SearchText** alanında müşteri aramak için arama ölçütü girin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-108">For **SearchText**, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="b0e01-109">Bu örnek yordam için "Karen" yazın ve **Sekme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="b0e01-110">Ara'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-110">Select Search.</span></span>
    * <span data-ttu-id="b0e01-111">Demo veride "Karen" adında tek bir müşteri olduğundan sonuç otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="b0e01-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="b0e01-112">**Yeni satış siparişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="b0e01-113">**Satış siparişi** başlığı bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="b0e01-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="b0e01-114">Katalog için kaynak kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="b0e01-115">Hiçbir etkin kaynak kodu yoksa bu adımı atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0e01-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="b0e01-116">**Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-116">Select **Add line**.</span></span>
8. <span data-ttu-id="b0e01-117">**Madde numarası** alanına madde arama terimini girin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-117">For **Item number**, enter the item search term.</span></span>
    * <span data-ttu-id="b0e01-118">Bu örnek yordamda '8111' kısmi madde numarasını girin ve Tab tuşuna basın. Bu eylem arama penceresinin açılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="b0e01-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="b0e01-119">Satış siparişine eklenecek ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="b0e01-120">Satış miktarını girin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="b0e01-121">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-121">Select **Create**.</span></span>
12. <span data-ttu-id="b0e01-122">Müşteri ödemesini yakalamak için **Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="b0e01-123">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-123">Select **Add**.</span></span>
    * <span data-ttu-id="b0e01-124">Ekle bağlantısı Ödemeler sekmesinde bulunur. Daraltılmışsa Ödemeler sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="b0e01-125">Ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-125">Select the payment method.</span></span>
    * <span data-ttu-id="b0e01-126">Bu yordam için nakit ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="b0e01-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b0e01-127">Close the page.</span></span>
16. <span data-ttu-id="b0e01-128">Tutarı girin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-128">Enter the amount.</span></span>
    * <span data-ttu-id="b0e01-129">Bu yordam için, tutar alanının sol tarafındaki Satış siparişi özet sayfasında görebileceğiniz sipariş bakiyesine eşit bir tutar girin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="b0e01-130">Bu eylem siparişi tamamen ödenmiş olarak tamamlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="b0e01-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="b0e01-131">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-131">Select **OK**.</span></span>
18. <span data-ttu-id="b0e01-132">**Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b0e01-132">Select **Submit**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0e01-133">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b0e01-133">Additional resources</span></span>

[<span data-ttu-id="b0e01-134">Teslimat şekline göre işlem tabanlı e-postaları özelleştirme</span><span class="sxs-lookup"><span data-stu-id="b0e01-134">Customize transactional emails by mode of delivery</span></span>](../customize-email-delivery-mode.md)

[<span data-ttu-id="b0e01-135">Satış noktasında teslimat şeklini değiştirme</span><span class="sxs-lookup"><span data-stu-id="b0e01-135">Change mode of delivery in POS</span></span>](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]