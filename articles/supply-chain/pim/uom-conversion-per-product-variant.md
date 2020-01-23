---
title: Ürün çeşidi başına ölçü birimi dönüşümü
description: Bu konu, ürün çeşitlerinde ölçü birimi dönüşümlerinin nasıl ayarlanabileceğini açıklar.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935111"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="071fd-103">Ürün çeşidi başına ölçü birimi dönüşümü</span><span class="sxs-lookup"><span data-stu-id="071fd-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="071fd-104">Bu konu, ürün çeşitlerinde ölçü birimi dönüşümlerinin nasıl ayarlanabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="071fd-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="071fd-105">Bir kurulum örneği içerir.</span><span class="sxs-lookup"><span data-stu-id="071fd-105">It includes an example of the setup.</span></span>

<span data-ttu-id="071fd-106">Bu özellik, şirketlerin aynı ürün üzerindeki farklı çeşitler için farklı birim dönüştürmeleri tanımlamalarına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="071fd-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="071fd-107">Aşağıdaki örnek bu konuda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="071fd-107">The following example is used in this topic.</span></span> <span data-ttu-id="071fd-108">Bir şirket, Küçük, Medium, Large ve X-Large ebatlarında tişörtler satmaktadır.</span><span class="sxs-lookup"><span data-stu-id="071fd-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="071fd-109">Tişört, bir ürün olarak tanımlanmıştır ve farklı ebatları ürünün çeşitleri olarak tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="071fd-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="071fd-110">Tişörtler, bir kutuda beş tişört olabileceği şekilde paketlenmiştir, yalnızca dört tişört için yer olan X-Large beden hariç.</span><span class="sxs-lookup"><span data-stu-id="071fd-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="071fd-111">Şirket, **Adet** biriminde tişörtlerin farklı türlerini izlemek istemektedir ancak tişörtleri **Kutu** biriminde satmaktadır.</span><span class="sxs-lookup"><span data-stu-id="071fd-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="071fd-112">Stok birimi ve satış birimi için dönüşüm, X-Large ürün çeşidi için 1 Kutu = 4 Adet olduğu durum dışında 1 Kutu = 5 Adettir.</span><span class="sxs-lookup"><span data-stu-id="071fd-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="071fd-113">Çeşit başına birim dönüşümü için bir ürün ayarla</span><span class="sxs-lookup"><span data-stu-id="071fd-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="071fd-114">Ürün çeşitleri, yalnızca **Ürün alt türü**: **Ana Ürün** ürünleri için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="071fd-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="071fd-115">Daha fazla bilgi için [Bir ana ürün oluşturma](tasks/create-product-master.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="071fd-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="071fd-116">Bu özellik fiili ağırlık işlemler için ayarlanmış olan ürünler için etkin değildir.</span><span class="sxs-lookup"><span data-stu-id="071fd-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="071fd-117">Ana ürün, serbest bırakılan ürün çeşitleri ile oluşturulursa, çeşit başına ölçü dönüşümü ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="071fd-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="071fd-118">Bir ürün veya ürün çeşidi bağlamında ölçü birimi dönüştürme sayfası için menü öğesini, aşağıdaki sayfalarda bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="071fd-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="071fd-119">**Ürün ayrıntıları** sayfası</span><span class="sxs-lookup"><span data-stu-id="071fd-119">**Product details** page</span></span>
-   <span data-ttu-id="071fd-120">**Serbest bırakılan ürünlerin ayrıntıları** sayfası</span><span class="sxs-lookup"><span data-stu-id="071fd-120">**Released products details** page</span></span>
-   <span data-ttu-id="071fd-121">**Serbest bırakılan ürün çeşitleri** sayfası</span><span class="sxs-lookup"><span data-stu-id="071fd-121">**Released product variants** page</span></span>

<span data-ttu-id="071fd-122">**Birim dönüştürme** sayfasını, bir ana ürün veya serbest bırakılmış ürün çeşidi bağlamında açtığınızda, biri dönüştürmeyi ürün mü yoksa ürün çeşidi mi için ayarlamak istediğinizi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="071fd-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="071fd-123">Bun **Ürün çeşidi** veya **Ürün**'ü, **Dönüşüm ayarla** alanında seçerek yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="071fd-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="071fd-124">Ürün çeşidi</span><span class="sxs-lookup"><span data-stu-id="071fd-124">Product variant</span></span>

<span data-ttu-id="071fd-125">**Ürünü çeşidi** seçerseniz, hangi çeşit için ürün dönüşümünü ayarlayacağınızı **Ürün çeşidi** alanında seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="071fd-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="071fd-126">Ürün</span><span class="sxs-lookup"><span data-stu-id="071fd-126">Product</span></span>

<span data-ttu-id="071fd-127">**Ürün** seçerseniz, ana ürün için bir birim dönüştürme ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="071fd-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="071fd-128">Bu birim dönüştürme, tanımlanmış bir birim dönüştürmeye sahip olmayan tüm ürün çeşitlerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="071fd-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="071fd-129">Örnek</span><span class="sxs-lookup"><span data-stu-id="071fd-129">Example</span></span>

<span data-ttu-id="071fd-130">Bir ana ürün, **Tişört**, serbest bırakılmış dört çeşide sahiptir, Küçük, Medium, Large ve X-Large.</span><span class="sxs-lookup"><span data-stu-id="071fd-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="071fd-131">Tişörtler, bir kutuda beş tişört olabileceği şekilde paketlenmiştir, yalnızca dört tişört için yer olan X-large beden hariç.</span><span class="sxs-lookup"><span data-stu-id="071fd-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="071fd-132">İlk olarak **Birim dönüştürme** sayfasını, **Tişört** için serbest bırakılmış ürün ayrıntıları sayfasından seçin.</span><span class="sxs-lookup"><span data-stu-id="071fd-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="071fd-133">**Birim dönüştürme** sayfasında, serbest bırakılmış ürün çeşidi X-Large için birim dönüştürmeyi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="071fd-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="071fd-134">**Alan**</span><span class="sxs-lookup"><span data-stu-id="071fd-134">**Field**</span></span>             | <span data-ttu-id="071fd-135">**Ayar**</span><span class="sxs-lookup"><span data-stu-id="071fd-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="071fd-136">Dönüşüm formu oluştur</span><span class="sxs-lookup"><span data-stu-id="071fd-136">Create conversion for</span></span> | <span data-ttu-id="071fd-137">Ürün çeşidi</span><span class="sxs-lookup"><span data-stu-id="071fd-137">Product variant</span></span>         |
| <span data-ttu-id="071fd-138">Ürün çeşidi</span><span class="sxs-lookup"><span data-stu-id="071fd-138">Product variant</span></span>       | <span data-ttu-id="071fd-139">Tişört : : X-Large : :</span><span class="sxs-lookup"><span data-stu-id="071fd-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="071fd-140">İlk birim</span><span class="sxs-lookup"><span data-stu-id="071fd-140">From unit</span></span>             | <span data-ttu-id="071fd-141">Kutular</span><span class="sxs-lookup"><span data-stu-id="071fd-141">Boxes</span></span>                   |
| <span data-ttu-id="071fd-142">Katsayı</span><span class="sxs-lookup"><span data-stu-id="071fd-142">Factor</span></span>                | <span data-ttu-id="071fd-143">4</span><span class="sxs-lookup"><span data-stu-id="071fd-143">4</span></span>                       |
| <span data-ttu-id="071fd-144">Son Birim</span><span class="sxs-lookup"><span data-stu-id="071fd-144">To Unit</span></span>               | <span data-ttu-id="071fd-145">Parça</span><span class="sxs-lookup"><span data-stu-id="071fd-145">Pieces</span></span>                  |

<span data-ttu-id="071fd-146">Serbest bırakılan ürün çeşitleri Küçük, Medium ve Large, Kutu ve Adet arasında aynı birim dönüştürmeye sahiptir, bu da bu ürünler için birim dönüştürmeyi ana ürün üzerinde ayarlayabileceğiniz anlamına gelmektedir.</span><span class="sxs-lookup"><span data-stu-id="071fd-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="071fd-147">**Alan**</span><span class="sxs-lookup"><span data-stu-id="071fd-147">**Field**</span></span>             | <span data-ttu-id="071fd-148">**Ayar**</span><span class="sxs-lookup"><span data-stu-id="071fd-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="071fd-149">Dönüşüm formu oluştur</span><span class="sxs-lookup"><span data-stu-id="071fd-149">Create conversion for</span></span> | <span data-ttu-id="071fd-150">Ürün</span><span class="sxs-lookup"><span data-stu-id="071fd-150">Product</span></span>     |
| <span data-ttu-id="071fd-151">Ürün</span><span class="sxs-lookup"><span data-stu-id="071fd-151">Product</span></span>               | <span data-ttu-id="071fd-152">Tişört</span><span class="sxs-lookup"><span data-stu-id="071fd-152">T-Shirt</span></span>     |
| <span data-ttu-id="071fd-153">İlk birim</span><span class="sxs-lookup"><span data-stu-id="071fd-153">From unit</span></span>             | <span data-ttu-id="071fd-154">Kutular</span><span class="sxs-lookup"><span data-stu-id="071fd-154">Boxes</span></span>       |
| <span data-ttu-id="071fd-155">Katsayı</span><span class="sxs-lookup"><span data-stu-id="071fd-155">Factor</span></span>                | <span data-ttu-id="071fd-156">5</span><span class="sxs-lookup"><span data-stu-id="071fd-156">5</span></span>           |
| <span data-ttu-id="071fd-157">Son Birim</span><span class="sxs-lookup"><span data-stu-id="071fd-157">To Unit</span></span>               | <span data-ttu-id="071fd-158">Parça</span><span class="sxs-lookup"><span data-stu-id="071fd-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="071fd-159">Birim dönüştürmelerini güncelleştirmek için Excel kullanmak</span><span class="sxs-lookup"><span data-stu-id="071fd-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="071fd-160">Bir ürün, farklı birim dönüştürmelerine sahip çok sayıda ürün çeşidine sahipse, birim dönüştürmeyi **Birim dönüştürme** sayfasından bir Excel elektronik tablosuna dışa aktarmak, dönüşümleri güncelleştirmek ve daha sonra Supply Chain Mangement'ta yeniden yayınlamak iyi bir fikir olabilir.</span><span class="sxs-lookup"><span data-stu-id="071fd-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="071fd-161">Excel'e dışa aktarma ve düzenlemeleri Supply Chain Mangement'ta yeniden yayınlama seçeneği, **Birim dönüştürme** sayfasının Eylem Bölmesindeki **Microsoft Office'te aç** menü öğesinden etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="071fd-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
