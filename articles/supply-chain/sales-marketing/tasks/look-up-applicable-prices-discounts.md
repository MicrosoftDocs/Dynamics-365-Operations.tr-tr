--- 
title: "Uygulanabilir fiyatları ve iskontoları arama"
description: "Bu yordam, bir satış siparişi oluşturmak zorunda kalmadan belirli bir müşteri için geçerli olan ürün fiyat ve iskonto bulmayı gösterir."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: 7ef63151f352b3664bccd7a59e7417dfddc7470b
ms.contentlocale: tr-tr
ms.lasthandoff: 11/02/2017

---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="e9a3a-103">Uygulanabilir fiyatları ve iskontoları arama</span><span class="sxs-lookup"><span data-stu-id="e9a3a-103">Look up applicable prices and discounts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e9a3a-104">Bu yordam, bir satış siparişi oluşturmak zorunda kalmadan belirli bir müşteri için geçerli olan ürün fiyat ve iskonto bulmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="e9a3a-105">Bu yordam belirli bir örneği adım adım izler ve örneği takip ederken gerekli değerleri seçebilmek için USMF demo şirketini kullanmanız gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="e9a3a-106">Uygulanabilir fiyatı bulun</span><span class="sxs-lookup"><span data-stu-id="e9a3a-106">Find the applicable price</span></span>
1. <span data-ttu-id="e9a3a-107">Sales and marketing > Prices and discounts > Find prices (Satış ve pazarlama > Fiyatlar ve iskontolar > Fiyatları bul) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="e9a3a-108">Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e9a3a-109">Listede, müşteri US-001'i bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="e9a3a-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e9a3a-111">Madde numarası alanına 'T0004' girin.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="e9a3a-112">Miktar alanı varsayılan olarak 1'e ayarlıdır.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="e9a3a-113">Fakat, söz konusu ürün için müşterinin vermek istediği siparişin boyutunu biliyorsanız, yerine bu değeri girin.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="e9a3a-114">Bu bilgiler, müşteri ile olan ticari anlaşmalarının miktar kırılması varsa, yani ürünün fiyatı satın alınan minimum miktara bağlıysa, ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="e9a3a-115">Tarih alanına, sipariş verebilmek için müşterinin beklediği bir tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="e9a3a-116">Tarih bugünün tarihi ya da gelecekteki herhangi bir tarih olabilir.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="e9a3a-117">Sistem şimdi belirtilen miktarla seçilen tarihte, seçilen müşteri tarafından satın alınan, seçilen ürün miktarı için geçerli olan fiyatı getirir.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="e9a3a-118">Bu örnekte, müşteri US-001 bugün T0004 ürününden 1 birim satın aldıysa, 350 Kanada doları ücretlendirilir.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="e9a3a-119">Bu fiyat müşteri ile mevcut bulunan ve etkin olan ticari sözleşmeden ileri gelmektedir.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="e9a3a-120">Sayfadaki diğer alanlar, ürün hakkında fiyat, ürün maliyeti (eğer ana ürün üzerinde ayarlandıysa) ve hesaplanmış karlılık gibi bilgiler verir.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="e9a3a-121">İlgili ürün çeşitlerini göster seçeneği işaretliyse bu, ürün çeşitleri ile ilgili başka ticari sözleşmeler olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="e9a3a-122">İlgili ürün çeşitlerini göster onay kutusuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="e9a3a-123">Boyutları hakkında bilgi verilen, ürün çeşitlerinin bir listesi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="e9a3a-124">Listede, Beyaz rengi temsil eden çizgiyi işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="e9a3a-125">Ürün fiyatının, boyut belirtilmemiş olduğunda önceden görüntülenenden farklı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="e9a3a-126">Satış fiyatlarını görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-126">Click View sales prices.</span></span>
    * <span data-ttu-id="e9a3a-127">Fiyat (satış) sayfası, ürün ve türevleri de dahil olmak üzere, ilgili tüm ticari sözleşmeleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="e9a3a-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="e9a3a-129">Uygulanabilir indirimi bulun</span><span class="sxs-lookup"><span data-stu-id="e9a3a-129">Find the applicable discount</span></span>
    * <span data-ttu-id="e9a3a-130">Müşteri hesabı alanının müşteri numarası US-001'i içerdiğinden emin olun </span><span class="sxs-lookup"><span data-stu-id="e9a3a-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="e9a3a-131">Madde numarası alanına 'T0012' girin.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="e9a3a-132">Miktar alanının 1'e ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="e9a3a-133">Gösterilen ürün T0012 için aşağıdaki fiyatlandırma ayrıntıları bir veya daha fazla ticari sözleşmeden ileri gelmektedir: Birim fiyatı 1.000 Kanada doları ve iskonto yüzde 5.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="e9a3a-134">Miktarı '20' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="e9a3a-135">Artan sipariş miktarı, müşteriye sunulan satır iskontosunun yüzde 5'ten 7'ye çıkmasına sebep olur.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="e9a3a-136">Net tutar, birim tutarı, iskonto ve toplam miktara göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="e9a3a-137">Satır iskontolarını görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-137">Click View line discount.</span></span>
    * <span data-ttu-id="e9a3a-138">Ürün T0012 için iki indirim sözleşmesi vardır; 1 il 10 arasında sipariş satırı miktarı içi yüzde 5 ve 10 üzerinde sipariş miktarlar için yüzde 7 indirim.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="e9a3a-139">Bir indirimin bir grup ürüne uygulandığını (bu örnekteki ürün T0012'nin bir parçası olduğu Grup kodu 01) unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="e9a3a-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e9a3a-140">Close the page.</span></span>


