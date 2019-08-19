---
title: Ürün çeşidi başına ölçü birimi dönüşümü
description: Bu konu, ürün çeşitlerinde ölçü birimi dönüşümlerinin nasıl ayarlanabileceğini açıklar.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 36fc98c44625cce03945d76973de67021d53353e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844381"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="18b72-103">Ürün çeşidi başına ölçü birimi dönüşümü</span><span class="sxs-lookup"><span data-stu-id="18b72-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="18b72-104">Bu konu, ürün çeşitlerinde ölçü birimi dönüşümlerinin nasıl ayarlanabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="18b72-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="18b72-105">Bir kurulum örneği içerir.</span><span class="sxs-lookup"><span data-stu-id="18b72-105">It includes an example of the setup.</span></span>

<span data-ttu-id="18b72-106">Bu özellik, şirketlerin aynı ürün üzerindeki farklı çeşitler için farklı birim dönüştürmeleri tanımlamalarına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="18b72-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="18b72-107">Aşağıdaki örnek bu konuda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="18b72-107">The following example is used in this topic.</span></span> <span data-ttu-id="18b72-108">Bir şirket, Küçük, Medium, Large ve X-Large ebatlarında tişörtler satmaktadır.</span><span class="sxs-lookup"><span data-stu-id="18b72-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="18b72-109">Tişört, bir ürün olarak tanımlanmıştır ve farklı ebatları ürünün çeşitleri olarak tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="18b72-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="18b72-110">Tişörtler, bir kutuda beş tişört olabileceği şekilde paketlenmiştir, yalnızca dört tişört için yer olan X-Large beden hariç.</span><span class="sxs-lookup"><span data-stu-id="18b72-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="18b72-111">Şirket, **Adet** biriminde tişörtlerin farklı türlerini izlemek istemektedir ancak tişörtleri **Kutu** biriminde satmaktadır.</span><span class="sxs-lookup"><span data-stu-id="18b72-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="18b72-112">Stok birimi ve satış birimi için dönüşüm, X-Large ürün çeşidi için 1 Kutu = 4 Adet olduğu durum dışında 1 Kutu = 5 Adettir.</span><span class="sxs-lookup"><span data-stu-id="18b72-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="18b72-113">Ayarlar</span><span class="sxs-lookup"><span data-stu-id="18b72-113">Setup</span></span>

<span data-ttu-id="18b72-114">**Tüm işlemler** veya yalnızca **Ambar işlemleri** için etkinleştirilmiş ürünler için parametreleri özelliği kullanarak, **Ölçü birimi dönüşümlerini**, **Ürün bilgi parametreleri** sayfasında kullanarak yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18b72-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="18b72-115">Çeşit başına birim dönüşümü için bir ürün ayarla</span><span class="sxs-lookup"><span data-stu-id="18b72-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="18b72-116">Ürün çeşitleri, yalnızca **Ürün alt türü**: **Ana Ürün** ürünleri için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="18b72-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="18b72-117">Daha fazla bilgi için [Bir ana ürün oluşturma](tasks/create-product-master.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="18b72-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="18b72-118">Bu özellik fiili ağırlık işlemler için ayarlanmış olan ürünler için etkin değildir.</span><span class="sxs-lookup"><span data-stu-id="18b72-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="18b72-119">Bir ana ürün birimi ölçü dönüşümünü **Ölçü dönüşümleri birimi etkinleştir** seçeneğini **Ürün ayrıntıları** sayfasında kullanarak etkinleştirirken.</span><span class="sxs-lookup"><span data-stu-id="18b72-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="18b72-120">Ana ürün, serbest bırakılan ürün çeşitleri ile oluşturulursa, çeşit başına ölçü dönüşümü ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="18b72-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="18b72-121">Bir ürün veya ürün çeşidi bağlamında ölçü birimi dönüştürme sayfası için menü öğesini, aşağıdaki sayfalarda bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18b72-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="18b72-122">**Ürün ayrıntıları** sayfası</span><span class="sxs-lookup"><span data-stu-id="18b72-122">**Product details** page</span></span>
-   <span data-ttu-id="18b72-123">**Serbest bırakılan ürünlerin ayrıntıları** sayfası</span><span class="sxs-lookup"><span data-stu-id="18b72-123">**Released products details** page</span></span>
-   <span data-ttu-id="18b72-124">**Serbest bırakılan ürün çeşitleri** sayfası</span><span class="sxs-lookup"><span data-stu-id="18b72-124">**Released product variants** page</span></span>

<span data-ttu-id="18b72-125">**Birim dönüştürme** sayfasını, bir ana ürün veya serbest bırakılmış ürün çeşidi bağlamında açtığınızda, biri dönüştürmeyi ürün mü yoksa ürün çeşidi mi için ayarlamak istediğinizi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18b72-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="18b72-126">Bun **Ürün çeşidi** veya **Ürün**'ü, **Dönüşüm ayarla** alanında seçerek yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="18b72-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="18b72-127">Ürün çeşidi</span><span class="sxs-lookup"><span data-stu-id="18b72-127">Product variant</span></span>

<span data-ttu-id="18b72-128">**Ürünü çeşidi** seçerseniz, hangi çeşit için ürün dönüşümünü ayarlayacağınızı **Ürün çeşidi** alanında seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18b72-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="18b72-129">Ürün</span><span class="sxs-lookup"><span data-stu-id="18b72-129">Product</span></span>

<span data-ttu-id="18b72-130">**Ürün** seçerseniz, ana ürün için bir birim dönüştürme ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18b72-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="18b72-131">Bu birim dönüştürme, tanımlanmış bir birim dönüştürmeye sahip olmayan tüm ürün çeşitlerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="18b72-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="18b72-132">Örnek</span><span class="sxs-lookup"><span data-stu-id="18b72-132">Example</span></span>

<span data-ttu-id="18b72-133">Bir ana ürün, **Tişört**, serbest bırakılmış dört çeşide sahiptir, Küçük, Medium, Large ve X-Large.</span><span class="sxs-lookup"><span data-stu-id="18b72-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="18b72-134">Tişörtler, bir kutuda beş tişört olabileceği şekilde paketlenmiştir, yalnızca dört tişört için yer olan X-large beden hariç.</span><span class="sxs-lookup"><span data-stu-id="18b72-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="18b72-135">İlk olarak **Birim dönüştürme** sayfasını, **Tişört** için serbest bırakılmış ürün ayrıntıları sayfasından seçin.</span><span class="sxs-lookup"><span data-stu-id="18b72-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="18b72-136">**Birim dönüştürme** sayfasında, serbest bırakılmış ürün çeşidi X-Large için birim dönüştürmeyi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="18b72-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="18b72-137">**Alan**</span><span class="sxs-lookup"><span data-stu-id="18b72-137">**Field**</span></span>             | <span data-ttu-id="18b72-138">**Ayar**</span><span class="sxs-lookup"><span data-stu-id="18b72-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="18b72-139">Dönüşüm formu oluştur</span><span class="sxs-lookup"><span data-stu-id="18b72-139">Create conversion for</span></span> | <span data-ttu-id="18b72-140">Ürün çeşidi</span><span class="sxs-lookup"><span data-stu-id="18b72-140">Product variant</span></span>         |
| <span data-ttu-id="18b72-141">Ürün çeşidi</span><span class="sxs-lookup"><span data-stu-id="18b72-141">Product variant</span></span>       | <span data-ttu-id="18b72-142">Tişört : : X-Large : :</span><span class="sxs-lookup"><span data-stu-id="18b72-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="18b72-143">İlk birim</span><span class="sxs-lookup"><span data-stu-id="18b72-143">From unit</span></span>             | <span data-ttu-id="18b72-144">Kutular</span><span class="sxs-lookup"><span data-stu-id="18b72-144">Boxes</span></span>                   |
| <span data-ttu-id="18b72-145">Katsayı</span><span class="sxs-lookup"><span data-stu-id="18b72-145">Factor</span></span>                | <span data-ttu-id="18b72-146">4</span><span class="sxs-lookup"><span data-stu-id="18b72-146">4</span></span>                       |
| <span data-ttu-id="18b72-147">Son Birim</span><span class="sxs-lookup"><span data-stu-id="18b72-147">To Unit</span></span>               | <span data-ttu-id="18b72-148">Parça</span><span class="sxs-lookup"><span data-stu-id="18b72-148">Pieces</span></span>                  |

<span data-ttu-id="18b72-149">Serbest bırakılan ürün çeşitleri Küçük, Medium ve Large, Kutu ve Adet arasında aynı birim dönüştürmeye sahiptir, bu da bu ürünler için birim dönüştürmeyi ana ürün üzerinde ayarlayabileceğiniz anlamına gelmektedir.</span><span class="sxs-lookup"><span data-stu-id="18b72-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="18b72-150">**Alan**</span><span class="sxs-lookup"><span data-stu-id="18b72-150">**Field**</span></span>             | <span data-ttu-id="18b72-151">**Ayar**</span><span class="sxs-lookup"><span data-stu-id="18b72-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="18b72-152">Dönüşüm formu oluştur</span><span class="sxs-lookup"><span data-stu-id="18b72-152">Create conversion for</span></span> | <span data-ttu-id="18b72-153">Ürün</span><span class="sxs-lookup"><span data-stu-id="18b72-153">Product</span></span>     |
| <span data-ttu-id="18b72-154">Ürün</span><span class="sxs-lookup"><span data-stu-id="18b72-154">Product</span></span>               | <span data-ttu-id="18b72-155">Tişört</span><span class="sxs-lookup"><span data-stu-id="18b72-155">T-Shirt</span></span>     |
| <span data-ttu-id="18b72-156">İlk birim</span><span class="sxs-lookup"><span data-stu-id="18b72-156">From unit</span></span>             | <span data-ttu-id="18b72-157">Kutular</span><span class="sxs-lookup"><span data-stu-id="18b72-157">Boxes</span></span>       |
| <span data-ttu-id="18b72-158">Katsayı</span><span class="sxs-lookup"><span data-stu-id="18b72-158">Factor</span></span>                | <span data-ttu-id="18b72-159">5</span><span class="sxs-lookup"><span data-stu-id="18b72-159">5</span></span>           |
| <span data-ttu-id="18b72-160">Son Birim</span><span class="sxs-lookup"><span data-stu-id="18b72-160">To Unit</span></span>               | <span data-ttu-id="18b72-161">Parça</span><span class="sxs-lookup"><span data-stu-id="18b72-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="18b72-162">Birim dönüştürmelerini güncelleştirmek için Excel kullanmak</span><span class="sxs-lookup"><span data-stu-id="18b72-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="18b72-163">Bir ürün, farklı birim dönüştürmelerine sahip çok sayıda ürün çeşidine sahipse, birim dönüştürmeyi **Birim dönüştürme** sayfasından bir Excel elektronik tablosuna dışa aktarmak, dönüşümleri güncelleştirmek ve daha sonra Finance and Operations'a geri yayınlamak iyi bir fikir olabilir.</span><span class="sxs-lookup"><span data-stu-id="18b72-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="18b72-164">Excel'e dışa aktarma ve düzenlemeleri Finance and Operations'a yayınlama, **Birim dönüştürme** sayfasındaki **Microsoft Office'te aç** menü öğesinde etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="18b72-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
