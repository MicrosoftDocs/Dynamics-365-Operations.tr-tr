--- 
title: "Yeni bir ticari sözleşme oluşturma"
description: "Bu yordam belirli bir müşteri ile üzerinde anlaştığınız yeni bir ürün satış fiyatını kaydetmek için bir ticari sözleşmenin nasıl oluşturulacağını gösterir."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 134642ff2eed988c137e7d0ecc8b0da77684f8c7
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="19711-103">Yeni bir ticari sözleşme oluşturma</span><span class="sxs-lookup"><span data-stu-id="19711-103">Create a new trade agreement</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="19711-104">Bu yordam belirli bir müşteri ile üzerinde anlaştığınız yeni bir ürün satış fiyatını kaydetmek için bir ticari sözleşmenin nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19711-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="19711-105">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19711-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="19711-106">Eğer kendi verilerinizi kullanıyorsanız, bu kılavuz başlamadan önce varsayılan ilişkisi "Fiyat (satış)" olarak ayarlanan bir ticari sözleşmenin günlük adının var olduğundan emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="19711-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="19711-107">Yeni bir ticari sözleşme günlüğü oluşturun ve deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="19711-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="19711-108">Sales and marketing > Prices and discounts > Trade agreement journals (Satış ve pazarlama > Fiyatlar ve iskontolar > Ticari anlaşma günlükleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="19711-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="19711-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-109">Click New.</span></span>
3. <span data-ttu-id="19711-110">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="19711-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="19711-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="19711-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="19711-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="19711-113">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-113">Click Lines.</span></span>
7. <span data-ttu-id="19711-114">Hesap kodu alanında 'Tablo'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="19711-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="19711-115">Bu örnekte, belirli bir müşteri için fiyat güncelleştirmesi yapıyorsunuz bu yüzden de Tablo seçmeniz lazım.</span><span class="sxs-lookup"><span data-stu-id="19711-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="19711-116">Ürünün liste fiyatını güncelleştiriyor olsaydınız, yeni fiyatın tüm müşteriler için geçerli olmasını sağlamak için, Tümü seçeneğini seçecektiniz.</span><span class="sxs-lookup"><span data-stu-id="19711-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="19711-117">Müşteri segmentleri arasında fiyat farklılaştırması yapacak olsaydınız, Grup seçeneğini seçmeniz gerekirdi.</span><span class="sxs-lookup"><span data-stu-id="19711-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="19711-118">Grup'u seçmek için müşteri fiyat grupları ayarlamış olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="19711-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="19711-119">Hesap seçimi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="19711-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="19711-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="19711-121">Madde kodu alanında 'Tablo'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="19711-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="19711-122">"Fiyat (satışlar)" türünde bir ticari anlaşmaya girecek olduğunuzda, madde kodu alanında sadece Tablo'yu seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="19711-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="19711-123">Bunun sebebi bir fiyatın mutlak değerde olmasıdır ve tüm ürünler veya ürün grupları için aynı olamayışıdır.</span><span class="sxs-lookup"><span data-stu-id="19711-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="19711-124">Madde ilişkisi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="19711-125">Listede, sözleşmeye dahil etmek istediğiniz ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="19711-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="19711-126">Hangi ürünü seçtiğinizi not alın.</span><span class="sxs-lookup"><span data-stu-id="19711-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="19711-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="19711-128">Başlangıç alanında bir minimum miktar girin.</span><span class="sxs-lookup"><span data-stu-id="19711-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="19711-129">Eğer müşterinin yeni bir fiyata hak kazanmadan önce sipariş etmesi gereken minimum bir miktar varsa, bu miktarı burada belirtin.</span><span class="sxs-lookup"><span data-stu-id="19711-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="19711-130">Anlaşması fiyatının daha fazlasında geçerli olmayacağı bir maksimum miktar belirtmek için Bitiş alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="19711-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="19711-131">Fiyatlar ve indirimleri temel alan birden fazla miktar kırılması sunacaksanız, her miktari aralığını bir çift minimum ve maksimum miktar olarak 'Başlangıç' ve 'Bitiş' alanları ile belirtin.</span><span class="sxs-lookup"><span data-stu-id="19711-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="19711-132">Para birimi miktarı alanına bir fiyat girin.</span><span class="sxs-lookup"><span data-stu-id="19711-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="19711-133">Başlangıç tarihi alanına bu sözleşmenin geçerliliğin başlayacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="19711-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="19711-134">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-134">Click Save.</span></span>
18. <span data-ttu-id="19711-135">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-135">Click Validate.</span></span>
19. <span data-ttu-id="19711-136">Seçilen satırları doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="19711-137">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-137">Click OK.</span></span>
21. <span data-ttu-id="19711-138">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-138">Click Post.</span></span>
22. <span data-ttu-id="19711-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="19711-140">Bir ürün için ticari sözleşmeleri görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="19711-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="19711-141">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="19711-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="19711-142">Listede, fiyatını az önce güncelleştirdiğiniz ürünü bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="19711-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="19711-143">Eylem Bölmesinde, Satış'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="19711-144">Ticari sözleşmeleri görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="19711-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="19711-145">Yeni oluşturduğunuz fiyat ticari sözleşmesinin ayrıntılarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="19711-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="19711-146">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="19711-146">Close the page.</span></span>


