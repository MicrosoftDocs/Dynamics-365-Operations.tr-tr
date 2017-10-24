--- 
title: "Satış sözleşmelerini girme"
description: "Bu yöntem, müşterilerinizden birini üzerinde anlaşılan belirli bir zaman zarfı içinde ürün satın alması karşılığında özel indirimlere hak kazanmasını sağlayacak bir satış anlaşmasını nasıl yaratacağınızı gösterir."
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
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8c11164f7edb8e05b93f3c58b9707c0bf2482228
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="cd986-103">Satış sözleşmelerini girme</span><span class="sxs-lookup"><span data-stu-id="cd986-103">Enter sales agreements</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd986-104">Bu yordam, müşterilerinizden birini onaylanan bir süre için, özel indirimler karşılığında bir ürünü satın almaya</span><span class="sxs-lookup"><span data-stu-id="cd986-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an</span></span>

<span data-ttu-id="cd986-105">özel bir tutar ile anlaşmasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd986-105">agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="cd986-106">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd986-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="cd986-107">Satış sözleşmesi üstbilgisi ayarla</span><span class="sxs-lookup"><span data-stu-id="cd986-107">Set up sales agreement header</span></span>
1. <span data-ttu-id="cd986-108">Sales and marketing > Sales agreements > Sales agreements (Satış ve pazarlama > Satış anlaşmaları > Satış anlaşmaları) menüsüne gidin</span><span class="sxs-lookup"><span data-stu-id="cd986-108">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="cd986-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cd986-109">Click New.</span></span>
3. <span data-ttu-id="cd986-110">Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cd986-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cd986-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cd986-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cd986-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cd986-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cd986-113">Satış sözleşmeleri sınıflandırması alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cd986-113">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cd986-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cd986-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cd986-115">Genel bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="cd986-115">Expand the General section.</span></span>
9. <span data-ttu-id="cd986-116">'Ürün değeri taahhüdü' seçeneğini varsayılan taahhüt alanında seçin.</span><span class="sxs-lookup"><span data-stu-id="cd986-116">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="cd986-117">Bağlılık türü, anlaşma sözleşmesinin nasıl karşılanacağını tanımlamak için anlaşmaya atanması zorunlu bir ölçüttür.</span><span class="sxs-lookup"><span data-stu-id="cd986-117">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="cd986-118">Önceden tanımlanmış bu dört tür, müşteri bağlılık hedefini, bir miktar veya değer olarak ifade edilecek şekilde ayarlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="cd986-118">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="cd986-119">Miktar bağlılık türü belirli yalnızca belirli bir ürüne uygulanabilir, ancak değer temelindeki türler belirli ve belirsiz ürünlerin satışında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="cd986-119">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="cd986-120">Sona erme tarihi alanında, Anlaşma süresinin dolmasını istediğiniz ileri bir tarihe ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cd986-120">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="cd986-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cd986-121">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="cd986-122">Ürün değeri taahhüt satırları ayarla</span><span class="sxs-lookup"><span data-stu-id="cd986-122">Set up product value commitment lines</span></span>
1. <span data-ttu-id="cd986-123">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cd986-123">Click Add line.</span></span>
2. <span data-ttu-id="cd986-124">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="cd986-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cd986-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cd986-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cd986-126">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cd986-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cd986-127">Anlaşma için seçmiş olduğunuz bağlılık türü, anlaşmanın satırlarına girebileceğiniz bilginin türünü etkiler.</span><span class="sxs-lookup"><span data-stu-id="cd986-127">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="cd986-128">Örneğin, değer temelli bir anlaşmada, müşterinin sizden satın alma taahhüdünde bulunduğu malların toplam net tutarını (anlaşılmış olan para biriminde) belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cd986-128">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="cd986-129">Bu örnekte, satırdaki Miktar ve Birim alanları, müşterinin anlaşmada belirli bir değerdeki ürünü satın alması üzerine oluşturmakta olduğunuz için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="cd986-129">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="cd986-130">Net tutar alanında, müşterinin satın alma taahhüdünde bulunduğu parasal tutarı girin.</span><span class="sxs-lookup"><span data-stu-id="cd986-130">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="cd986-131">İskonto yüzdesi alanında müşterinin bu anlaşmaya bağlı satış siparişi satırlarında geçerli olacak bir yüzdelik değer girin.</span><span class="sxs-lookup"><span data-stu-id="cd986-131">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="cd986-132">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="cd986-132">Expand the Line details section.</span></span>
8. <span data-ttu-id="cd986-133">Maksimum zorunlu alanda Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cd986-133">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="cd986-134">Maksimum'un Zorlanması seçimi, taahhüdün tüm satış emri satırlarının toplam tutarının taahhüdün özel fiyatlarının, iskontolarının ve/veya ödeme şartlarının, taahhüt üzerinde belirtilen tutarı aşmaması gerektiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="cd986-134">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="cd986-135">Minimum ve maksimum satış tutarları, seçilen anlaşmayı kullanan her satış emrinde satılması gereken değerlerin aralığını belirler.</span><span class="sxs-lookup"><span data-stu-id="cd986-135">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="cd986-136">Satış sözleşmesi üstbilgi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="cd986-136">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="cd986-137">Sözleşmenin durumu Etkili'ye ayarlanmadığı sürece satış emirleri, anlaşma ile ilişkili olamaz ve dolayısıyla bu sözleşmenin yerine getirilmesinde katkıda bulunamaz.</span><span class="sxs-lookup"><span data-stu-id="cd986-137">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="cd986-138">Bu aşamada durumu manüel olarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd986-138">You can change the status manually at this stage.</span></span> <span data-ttu-id="cd986-139">Fakat durum genellikle, anlaşmayı müşteri için onaylamakta olduğunuzda değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="cd986-139">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="cd986-140">Eylem Bölmesinde, Satış anlaşması'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cd986-140">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="cd986-141">Onay'a tıklayın</span><span class="sxs-lookup"><span data-stu-id="cd986-141">Click Confirmation.</span></span>
    * <span data-ttu-id="cd986-142">Anlaşmanın etkin olması seçeneğinin Evet olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="cd986-142">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="cd986-143">Baskı rapor alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cd986-143">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="cd986-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cd986-144">Click OK.</span></span>
14. <span data-ttu-id="cd986-145">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cd986-145">Close the page.</span></span>
    * <span data-ttu-id="cd986-146">Anlaşma şimdi etkindir ve müşterinin siparişlerini, taahhüt edilen hedefe göre mahsup etmek için anlaşmaya bağlamaya başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd986-146">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


