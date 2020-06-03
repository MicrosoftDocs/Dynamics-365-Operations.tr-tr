---
title: Yeni bir ticari sözleşme oluşturma
description: Bu yordam belirli bir müşteri ile üzerinde anlaştığınız yeni bir ürün satış fiyatını kaydetmek için bir ticari sözleşmenin nasıl oluşturulacağını gösterir.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1642da7b06363d1f704e51276b5cb36823707231
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383446"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="ab1e6-103">Yeni bir ticari sözleşme oluşturma</span><span class="sxs-lookup"><span data-stu-id="ab1e6-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab1e6-104">Bu yordam belirli bir müşteri ile üzerinde anlaştığınız yeni bir ürün satış fiyatını kaydetmek için bir ticari sözleşmenin nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="ab1e6-105">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="ab1e6-106">Eğer kendi verilerinizi kullanıyorsanız, bu kılavuz başlamadan önce varsayılan ilişkisi "Fiyat (satış)" olarak ayarlanan bir ticari sözleşmenin günlük adının var olduğundan emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="ab1e6-107">Yeni bir ticari sözleşme günlüğü oluşturun ve deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="ab1e6-108">**Gezinti bölmesi > Modüller > Satış ve pazarlama > Fiyatlar ve indirimler > Ticari sözleşme günlükleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="ab1e6-109">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-109">Click **New**.</span></span>
3. <span data-ttu-id="ab1e6-110">**Ad** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ab1e6-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ab1e6-112">**Eylem Bölmesi**'nde, **Satırlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-112">On **Action Pane**, click **Lines**.</span></span>
6. <span data-ttu-id="ab1e6-113">**Hesap kodu** alanında "Tablo" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="ab1e6-114">Bu örnekte, belirli bir müşteri için fiyat güncelleştirmesi yapıyorsunuz bu yüzden de Tablo seçmeniz lazım.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="ab1e6-115">Ürünün liste fiyatını güncelleştiriyor olsaydınız yeni fiyatın tüm müşteriler için geçerli olmasını sağlamak için "Tümü" seçeneğini seçecektiniz.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="ab1e6-116">Müşteri segmentleri arasında fiyat farklılaştırması yapacak olsaydınız, Grup seçeneğini seçmeniz gerekirdi.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="ab1e6-117">Grup'u seçmek için müşteri fiyat grupları ayarlamış olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="ab1e6-118">**Hesap seçimi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ab1e6-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="ab1e6-120">**Madde kodu** alanında "Tablo" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="ab1e6-121">"Fiyat (satışlar)" türünde bir ticari anlaşmaya girecek olduğunuzda, **Item code** alanında sadece "Tablo" seçeneğini seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="ab1e6-122">Bunun sebebi bir fiyatın mutlak değerde olmasıdır ve tüm ürünler veya ürün grupları için aynı olamayışıdır.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="ab1e6-123">**Madde ilişkisi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ab1e6-124">Listede, sözleşmeye dahil etmek istediğiniz ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="ab1e6-125">Hangi ürünü seçtiğinizi not alın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="ab1e6-126">**Başlangıç** alanında bir minimum miktar girin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="ab1e6-127">Müşterinin yeni fiyata hak kazanmadan önce sipariş etmesi gereken minimum bir miktar varsa, bu miktarı burada belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="ab1e6-128">Anlaşması fiyatının daha fazlasında geçerli olmayacağı bir maksimum miktar belirtmek için **Bitiş** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="ab1e6-129">Fiyatlar ve indirimleri temel alan birden fazla miktar kırılması sunacaksanız her miktar aralığını bir çift minimum ve maksimum miktar olarak **Başlangıç** ve **Bitiş** alanları ile belirtin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="ab1e6-130">**Para birimi cinsinden tutar alanına** bir fiyat girin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="ab1e6-131">**Ayrıntılar** bölümünün altındaki **Başlangıç tarihi** alanına bu anlaşmanın geçerliliğinin başlayacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="ab1e6-132">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-132">Click **Save**.</span></span>
16. <span data-ttu-id="ab1e6-133">**Doğrula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-133">Click **Validate**.</span></span>
17. <span data-ttu-id="ab1e6-134">**Seçilen satırları doğrula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="ab1e6-135">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-135">Click **OK**.</span></span>
19. <span data-ttu-id="ab1e6-136">**Naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-136">Click **Post**.</span></span>
20. <span data-ttu-id="ab1e6-137">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="ab1e6-138">Bir ürün için ticari sözleşmeleri görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="ab1e6-138">View trade agreements for a product</span></span>
1. <span data-ttu-id="ab1e6-139">**Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="ab1e6-140">Listede, fiyatını az önce güncelleştirdiğiniz ürünü bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="ab1e6-141">**Eylem bölmesi**'nde, **Satış**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="ab1e6-142">**Ticaret anlaşmalarını görüntüle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="ab1e6-143">Yeni oluşturduğunuz fiyat ticari sözleşmesinin ayrıntılarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-143">Review the details of the price trade agreement you have just created.</span></span>    

5. <span data-ttu-id="ab1e6-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab1e6-145">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ab1e6-145">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="ab1e6-146">Topluluk blogları</span><span class="sxs-lookup"><span data-stu-id="ab1e6-146">Community blogs</span></span>
- [<span data-ttu-id="ab1e6-147">Dynamics 365 for Finance and Operations içindeki satış fiyatları</span><span class="sxs-lookup"><span data-stu-id="ab1e6-147">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
