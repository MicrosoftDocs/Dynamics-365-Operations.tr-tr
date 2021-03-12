---
title: Satış noktasında (POS) stok arama
description: Bu konu (POS) satış noktasındaki stok bilgilerini görüntülemek için kullanılabilir seçenekleri açıklar.
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: f08906c14f80b07368d88d820acae83cf1157e6c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969963"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="4c4b3-103">Satış noktasında (POS) stok arama</span><span class="sxs-lookup"><span data-stu-id="4c4b3-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4c4b3-104">Satış notasında (POS) stok araması perakendecilerin gerçek zamanlı işlem başarısına ulaşmasına ve mağazalara, POS'a ve arka ofise bağlanarak öngörüler edinmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="4c4b3-105">Bu işlev, mağazalar ve dağıtım merkezleri arasında ürün stoğunun doğru ve gerçek zamanlı görünümünü sağlar.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="4c4b3-106">Ayrıca, stok planlamasını gerçek zamanlı geliştirerek perakendecilerin ek verimlilik ve maliyet tasarrufu sağlamasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="4c4b3-107">Bir kuruluştaki stoğun doğru ve gerçek zamanlı görünümü mağaza görevlilerinin zamanında, üst seviye müşteri hizmeti sunmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="4c4b3-108">En önemli olan zaman müşterinin satın alma kararını vermeye hazır olduğu andır.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="4c4b3-109">Mağazadaki kasiyerlerin gerçek zamanı bilgileri parmaklarının ucunda bulması çok önemlidir; böylece ürün teslimatı ve alınması için doğru şekilde taahhütte bulunabilirler.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="4c4b3-110">**Stok araması** sayfasını **Retail Modern POS** çalışma alanından veya **Retail Cloud POS** çalışma alanından açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![POS ana sayfasında stok araması kutucuğu](media/POSHomepage.png)

<span data-ttu-id="4c4b3-112">**Stok araması** sayfasında, ürün numarasını girmek için sayısal bir klavye kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="4c4b3-113">Daha sonra birden çok mağaza veya ambar için eldeki miktarı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Standart stok arama sayfası](media/InventoryLookUp.png)

<span data-ttu-id="4c4b3-115">**Ayrılmış** ve **Sipariş edilmiş** miktarlar da her yerleşim için gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="4c4b3-116">**Ayrılmış** – Bu miktar, yerleşimde belirtilen ürün numarası için arka ofisteki **Fiziksel rezerve** değerine başvuruda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="4c4b3-117">**Sipariş edilmiş** – Bu miktar, yerleşimde belirtilen ürün numarası için arka ofisteki **Toplam sipariş edilen** değerine başvuruda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="4c4b3-118">Stok kullanılabilirlik bilgisinin gösterildiği yerleşimler</span><span class="sxs-lookup"><span data-stu-id="4c4b3-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="4c4b3-119">Yerleşimlerin listesi iki varlık türünü içerir:</span><span class="sxs-lookup"><span data-stu-id="4c4b3-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="4c4b3-120">**Mağazalar** – Liste Headquarters'da geçerli mağaza için mağaza bulucu grubunu kullanarak yapılandırılan mağazalar listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-120">**Stores** – The list shows stores that are configured by using the store locator group for the current store in the Headquarters.</span></span>
- <span data-ttu-id="4c4b3-121">**Dağıtım merkezleri** – Çeşitli dağıtım merkezi türleri (ambarlar gibi) Commerce'de yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Commerce.</span></span> <span data-ttu-id="4c4b3-122">Bununla birlikte, liste stok kullanılabilirlik bilgisini yalnızca **standart** varsayılan türündeki dağıtım merkezleri için gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4c4b3-123">Stok kullanılabilirlik bilgileri POS'ta **Transit**, **karantina** ve **Rotadaki Mallar** türündeki ambarlar için gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="4c4b3-124">**Stok arama** sayfasında, eldeki geçerli miktarların, rezerve edilen miktarların ve sipariş edilen miktarların yanı sıra her mağaza için karşılanabilir miktar (ATP) miktarlarını da görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="4c4b3-125">ATP bilgilerini görmek için mağaza seçin ve ardından **Mağaza kullanılabilirliğini göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ATP miktarları](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="4c4b3-127">Tüm ürün çeşitlerini görmek için Boyut tabanlı matrisi açma</span><span class="sxs-lookup"><span data-stu-id="4c4b3-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="4c4b3-128">Ana ürünün **Ürün ayrıntıları** sayfasında veya **Stok arama** sayfasında, sayfanın altındaki uygulama çubuğundan **Tüm ürün çeşitlerini görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="4c4b3-129">Bu sayfalardan ilk başlatma için **Boyut tabanlı matris** görünümü geçerli mağaza için bir ürünün tüm çeşitlerine ilişkin stok kullanılabilirlik bilgisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="4c4b3-130">**Tüm ürün çeşitlerini görüntüle** düğmesi yalnızca ürün çeşitleri bulunan madde ana ürünleri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="4c4b3-131">Bağımsız ürünler veya setler için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-131">It isn't available for standalone products or kits.</span></span>

![Stok arama sayfasındaki tüm ürün çeşitlerini görüntüle düğmesi](media/StandardToMatrix.png)

<span data-ttu-id="4c4b3-133">Bir ana ürünün **Ürün ayrıntıları** sayfasında **Tüm ürün çeşitlerini görüntüle**'yi seçin veya **Stok arama** sayfasında, bir yerleşim seçmeden **Boyut tabanlı matris** görünümüne giderek geçerli mağaza için bir ürünün tüm çeşitlerinin stok kullanılabilirlik bilgisini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Stok arama sayfası için boyut tabanlı matris görünümü](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="4c4b3-135">Önceki örnekte boyutların görüntülenme sırası alfabetikti çünkü boyutların görüntülenme sırası seçilen ürün için yapılandırılmamıştı.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="4c4b3-136">**Boyut tabanlı matris** görünümünde, ürün çeşitlerine ait hücreler alt sağ köşede bir eldeki değer içerir.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="4c4b3-137">Aşağıdaki tablo çeşitli değerlerin anlamını açıklar.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="4c4b3-138">Eldeki değer</span><span class="sxs-lookup"><span data-stu-id="4c4b3-138">On-hand value</span></span>                            | <span data-ttu-id="4c4b3-139">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c4b3-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="4c4b3-140">0 (sıfır)'dan büyük olan sayısal değer</span><span class="sxs-lookup"><span data-stu-id="4c4b3-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="4c4b3-141">Seçili yerleşime bir ürün çeşidi serbest bırakılmıştır ve hücrede ek eylemler gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="4c4b3-142">(Bu eylemler, bu konuda daha ayrıntılı açıklanacaktır.)</span><span class="sxs-lookup"><span data-stu-id="4c4b3-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="4c4b3-143">**0** (sıfır)</span><span class="sxs-lookup"><span data-stu-id="4c4b3-143">**0** (zero)</span></span>                             | <span data-ttu-id="4c4b3-144">Bir ürün çeşidi seçili yerleşime serbest bırakılır ancak madde seçili yerleşimde kullanılabilir değildir.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="4c4b3-145">Bununla birlikte, hücrede ek eylemler gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="4c4b3-146">(Bu eylemler, bu konuda daha ayrıntılı açıklanacaktır.)</span><span class="sxs-lookup"><span data-stu-id="4c4b3-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="4c4b3-147">**yok** veya etkin olmayan bir hücre</span><span class="sxs-lookup"><span data-stu-id="4c4b3-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="4c4b3-148">Seçili yerleşime bir ürün çeşidi serbest bırakılmamıştır ve hücrede ek eylemler gerçekleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="4c4b3-149">Kullanmak üzere yeni bir boyut seçerek boyutlar için pivotu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span>

![Pivotu değiştirme](media/ChangePivot.png)

![Pivot değiştirildi](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="4c4b3-152">Önceki örneklerde , seçili ürün için boyutları görüntüleme sırası özeldir (alfabetik değildir).</span><span class="sxs-lookup"><span data-stu-id="4c4b3-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="4c4b3-153">Arka ofiste ayarlanan boyut görüntüleme sırasını temel alır.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="4c4b3-154">Ayrıca, **Boyut tabanlı matris** görünümde, bir mağaza çalışanının verimliliği artırmasına yardımcı olacak başka eylemler gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="4c4b3-155">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="4c4b3-155">Here are some examples:</span></span>

- <span data-ttu-id="4c4b3-156">Diğer yerleşimlerdeki tüm ürün çeşitlerinin stok kullanılabilirliğine bakmak için mağaza yerleşimini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="4c4b3-157">Bu yerleşimler mağaza bulucu grubundaki diğer mağazaları ve **Standart** varsayılan türündeki dağıtım merkezlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="4c4b3-158">Bir müşteriye bağımsız bir ürün çeşidini peşin alışveriş, mağazadan alma veya adrese sevkiyat kullanarak satın.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="4c4b3-159">Belirli bir yerleşimdeki bağımsız ürün çeşidi için müşteriye ATP bilgisini verin.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Ürün çeşidi kutularındaki ek eylemler](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="4c4b3-161">Önceki örnekte boyutların görüntülenme sırası alfabetikti çünkü boyutların görüntülenme sırası seçilen ürün için yapılandırılmamıştı.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="4c4b3-162">Aşağıdaki tablo kullanılabilen ek eylemler hakkında daha fazla bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-162">The following table provides more information about the additional actions that are available.</span></span>

| <span data-ttu-id="4c4b3-163">Eylem</span><span class="sxs-lookup"><span data-stu-id="4c4b3-163">Action</span></span>               | <span data-ttu-id="4c4b3-164">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c4b3-164">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="4c4b3-165">Şimdi sat</span><span class="sxs-lookup"><span data-stu-id="4c4b3-165">Sell now</span></span>             | <span data-ttu-id="4c4b3-166">Seçili madde ürün çeşidini harekete ekleyin ve kullanıcıyı hareket ekranına yönlendirin.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="4c4b3-167">(Bu eylem seçili yerleşim bir dağıtım merkezi olduğunda kullanılamaz.)</span><span class="sxs-lookup"><span data-stu-id="4c4b3-167">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="4c4b3-168">Mağazadan alma</span><span class="sxs-lookup"><span data-stu-id="4c4b3-168">Pick up in store</span></span>     | <span data-ttu-id="4c4b3-169">Seçilen yerleşimden alınacak ürün çeşidi için bir müşteri siparişi oluşturun ve kullanıcıyı hareket ekranına yönlendirin.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="4c4b3-170">(Bu eylem seçili yerleşim bir dağıtım merkezi olduğunda kullanılamaz.)</span><span class="sxs-lookup"><span data-stu-id="4c4b3-170">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="4c4b3-171">Ürün sevk et</span><span class="sxs-lookup"><span data-stu-id="4c4b3-171">Ship product</span></span>         | <span data-ttu-id="4c4b3-172">Seçilen yerleşimden sevk edilecek ürün çeşidi için bir müşteri siparişi oluşturun ve kullanıcıyı hareket ekranına yönlendirin.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span> |
| <span data-ttu-id="4c4b3-173">Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="4c4b3-173">Availability</span></span>         | <span data-ttu-id="4c4b3-174">Seçili yerleşim için seçilen ürün çeşidi birleşimine ilişkin ATP bilgisini gösterin.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-174">Show the ATP information for the selected variant combination for the selected location.</span></span> |
| <span data-ttu-id="4c4b3-175">Tüm yerleşimleri göster</span><span class="sxs-lookup"><span data-stu-id="4c4b3-175">Show all locations</span></span>   | <span data-ttu-id="4c4b3-176">Standart stok arama görünüme geçin ve mağaza bulucu grubundaki tüm mağazalarda ve **Standart/Varsayılan** türündeki dağıtım merkezlerinde madde ürün çeşidi için stok kullanılabilirlik bilgilerini vurgulayın.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the **Standard/Default** type.</span></span> |
| <span data-ttu-id="4c4b3-177">Ürün ayrıntılarını görüntüle</span><span class="sxs-lookup"><span data-stu-id="4c4b3-177">View product details</span></span> | <span data-ttu-id="4c4b3-178">Kullanıcıyı ilişkili ana ürünün **Ürün ayrıntıları** sayfasına yönlendirin.</span><span class="sxs-lookup"><span data-stu-id="4c4b3-178">Redirect the user to the **Product details** page of the associated product master.</span></span> |
