---
title: Ürün çeşidi başına ölçü birimi dönüşümü
description: Bu konuda, ürün çeşitleri için ölçü birimi dönüştürmelerinin nasıl ayarlanacağı açıklanmaktadır. Bir kurulum örneği içerir.
author: johanhoffmann
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: ed28928b0f07833d5906a68f780e3bb5bbe0bfe9
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921229"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="113b6-104">Ürün çeşidi başına ölçü birimi dönüşümü</span><span class="sxs-lookup"><span data-stu-id="113b6-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="113b6-105">Bu konuda, farklı ürün çeşitleri için ölçü birimi dönüştürmelerinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="113b6-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="113b6-106">Korunması gereken birden fazla ayrı ürün oluşturmak yerine tek bir ürünün çeşitlerini oluşturmak için ürün çeşitlerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="113b6-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="113b6-107">Örneğin, belirli bir boyut ve renkteki tişört bir ürün çeşidi olabilir.</span><span class="sxs-lookup"><span data-stu-id="113b6-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="113b6-108">Önceden, birim dönüştürmeleri yalnızca ana ürün üzerinde ayarlanabilirdi.</span><span class="sxs-lookup"><span data-stu-id="113b6-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="113b6-109">Bu nedenle, tüm ürün çeşitleri aynı birim dönüştürme kurallarına sahipti.</span><span class="sxs-lookup"><span data-stu-id="113b6-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="113b6-110">Ancak, *Ürün çeşitleri için ölçü birimi dönüştürmeleri* özelliği etkinleştirildiğinde; tişörtleriniz kutularda satılıyorsa ve bir kutuda paketlenebilecek tişörtlerin sayısı boyutlarına bağlıysa artık farklı tişört boyutları ve paketleme için kullanılan kutular arasında birim dönüştürmeleri ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="113b6-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="113b6-111">Sisteminizdeki özelliği etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="113b6-111">Turn on the feature in your system</span></span>

<span data-ttu-id="113b6-112">Sisteminizde bu özelliği henüz görmüyorsanız [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) konusuna gidin ve *Ürün çeşitleri için ölçü birimi dönüştürmeleri* özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="113b6-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="113b6-113">Çeşit başına birim dönüşümü için bir ürün ayarla</span><span class="sxs-lookup"><span data-stu-id="113b6-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="113b6-114">Ürün çeşitleri, yalnızca ana ürünler için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="113b6-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="113b6-115">Daha fazla bilgi için [Bir ana ürün oluşturma](tasks/create-product-master.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="113b6-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="113b6-116">*Ürün çeşitleri için ölçü birimi dönüştürmeleri* özelliği, fiili ağırlık işlemleri için ayarlanmış ürünlerde kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="113b6-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="113b6-117">Ana ürünü, birim dönüştürmeyi her çeşit için destekleyecek şekilde yapılandırmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="113b6-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="113b6-118">**Ürün bilgi yönetimi \> Ürünler \> Ana ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="113b6-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="113b6-119">Ana ürünün **Ürün ayrıntıları** sayfasına gitmek için bir ana ürün oluşturun veya açın.</span><span class="sxs-lookup"><span data-stu-id="113b6-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="113b6-120">**Ölçü birimi dönüştürmelerini etkinleştir** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="113b6-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="113b6-121">Eylem Bölmesi'nde, **Ürün** sekmesindeki **Ayar** gurubunda **Birim dönüştürmeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="113b6-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="113b6-122">**Birim dönüştürmeleri** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="113b6-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="113b6-123">Aşağıdaki sekmelerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="113b6-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="113b6-124">**Sınıf içi dönüştürmeler**: Aynı birim sınıfına ait birimler arasında dönüştürme yapmak için bu sekmeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="113b6-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="113b6-125">**Sınıflar arası dönüştürmeler**: Farklı birim sınıflarına ait birimler arasında dönüştürme yapmak için bu sekmeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="113b6-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="113b6-126">Yeni bir birim dönüştürme eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="113b6-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="113b6-127">**Dönüştürme oluştur** alanını aşağıdaki değerlerden birine ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="113b6-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="113b6-128">**Ürün**: Bu değeri seçerseniz ana ürün için birim dönüştürme ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="113b6-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="113b6-129">Bu birim dönüştürme, birim dönüştürmenin tanımlanmadığı tüm ürün çeşitleri için geri dönüş olarak kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="113b6-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="113b6-130">**Ürün çeşidi**: Bu değeri seçerseniz belirli bir ürün çeşidi için birim dönüştürme ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="113b6-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="113b6-131">Ürün çeşidini seçmek için **Ürün çeşidi** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="113b6-131">Use the **Product variant** field to select the variant.</span></span>

    <span data-ttu-id="113b6-132">![Yeni bir birim dönüştürme ekleme](media/uom-new-conversion.png "Yeni bir birim dönüştürme ekleme")</span><span class="sxs-lookup"><span data-stu-id="113b6-132">![Adding a new unit conversion](media/uom-new-conversion.png "Adding a new unit conversion")</span></span>

1. <span data-ttu-id="113b6-133">Birim dönüştürmenizi ayarlamak için sağlanan diğer alanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="113b6-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="113b6-134">Yeni birim dönüştürmeyi kaydetmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="113b6-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="113b6-135">Ürün veya ürün çeşidi için **Birim dönüştürmeleri** sayfasını aşağıdaki sayfalardan herhangi birinden açabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="113b6-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="113b6-136">Ürün ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="113b6-136">Product details</span></span>
> - <span data-ttu-id="113b6-137">Serbest bırakılan ürünlerin ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="113b6-137">Released products details</span></span>
> - <span data-ttu-id="113b6-138">Serbest bırakılan ürün çeşitleri</span><span class="sxs-lookup"><span data-stu-id="113b6-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="113b6-139">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="113b6-139">Example scenario</span></span>

<span data-ttu-id="113b6-140">Bu senaryoda bir şirket küçük, orta, büyük ve çok büyük ebatlarda tişörtler satmaktadır.</span><span class="sxs-lookup"><span data-stu-id="113b6-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="113b6-141">Tişört, bir ürün olarak ve farklı ebatları, ürünün çeşitleri olarak tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="113b6-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="113b6-142">Tişörtler, kutularda paketlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="113b6-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="113b6-143">Küçük, orta ve büyük ebatlar için her kutuda beş tişört olabilir.</span><span class="sxs-lookup"><span data-stu-id="113b6-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="113b6-144">Ancak, çok büyük ebat için her kutuda sadece dört tişörtlük yer vardır.</span><span class="sxs-lookup"><span data-stu-id="113b6-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="113b6-145">Şirket, farklı ürün çeşitlerini *Adet* biriminde izlemek istemektedir ancak ürünleri *Kutular* biriminde satmaktadır.</span><span class="sxs-lookup"><span data-stu-id="113b6-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="113b6-146">Küçük, orta ve büyük ebatlar için stok birimi ile satış birimi arasındaki dönüştürme 1 Kutu = 5 Adettir.</span><span class="sxs-lookup"><span data-stu-id="113b6-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="113b6-147">Çok büyük ebat için dönüştürme 1 Kutu = 4 Adettir.</span><span class="sxs-lookup"><span data-stu-id="113b6-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="113b6-148">**Tişört** ürününün **Serbest bırakılan ürün ayrıntıları** sayfasından **Birim dönüştürmeleri** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="113b6-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="113b6-149">**Birim dönüştürmeleri** sayfasında, serbest bırakılan ürün çeşidi **Çok büyük** için aşağıdaki birim dönüştürmeyi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="113b6-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="113b6-150">Alan</span><span class="sxs-lookup"><span data-stu-id="113b6-150">Field</span></span>                 | <span data-ttu-id="113b6-151">Ayar</span><span class="sxs-lookup"><span data-stu-id="113b6-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="113b6-152">Dönüşüm formu oluştur</span><span class="sxs-lookup"><span data-stu-id="113b6-152">Create conversion for</span></span> | <span data-ttu-id="113b6-153">Ürün varyantı</span><span class="sxs-lookup"><span data-stu-id="113b6-153">Product variant</span></span>         |
    | <span data-ttu-id="113b6-154">Ürün varyantı</span><span class="sxs-lookup"><span data-stu-id="113b6-154">Product variant</span></span>       | <span data-ttu-id="113b6-155">Tişört : : X-Large : :</span><span class="sxs-lookup"><span data-stu-id="113b6-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="113b6-156">İlk birim</span><span class="sxs-lookup"><span data-stu-id="113b6-156">From unit</span></span>             | <span data-ttu-id="113b6-157">Kutular</span><span class="sxs-lookup"><span data-stu-id="113b6-157">Boxes</span></span>                   |
    | <span data-ttu-id="113b6-158">Katsayı</span><span class="sxs-lookup"><span data-stu-id="113b6-158">Factor</span></span>                | <span data-ttu-id="113b6-159">4</span><span class="sxs-lookup"><span data-stu-id="113b6-159">4</span></span>                       |
    | <span data-ttu-id="113b6-160">Son Birim</span><span class="sxs-lookup"><span data-stu-id="113b6-160">To Unit</span></span>               | <span data-ttu-id="113b6-161">Parça</span><span class="sxs-lookup"><span data-stu-id="113b6-161">Pieces</span></span>                  |

1. <span data-ttu-id="113b6-162">**Küçük**, **Orta** ve **Büyük** ürün çeşitlerinin tümü, *Kutu* ile *Adet* birimleri arasında aynı birim dönüştürmeye sahip olduğu için onların aşağıdaki birim dönüştürmesini ana ürün üzerinden tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="113b6-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="113b6-163">Alan</span><span class="sxs-lookup"><span data-stu-id="113b6-163">Field</span></span>                 | <span data-ttu-id="113b6-164">Ayar</span><span class="sxs-lookup"><span data-stu-id="113b6-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="113b6-165">Dönüşüm formu oluştur</span><span class="sxs-lookup"><span data-stu-id="113b6-165">Create conversion for</span></span> | <span data-ttu-id="113b6-166">Ürün</span><span class="sxs-lookup"><span data-stu-id="113b6-166">Product</span></span> |
    | <span data-ttu-id="113b6-167">Ürün</span><span class="sxs-lookup"><span data-stu-id="113b6-167">Product</span></span>               | <span data-ttu-id="113b6-168">Tişört</span><span class="sxs-lookup"><span data-stu-id="113b6-168">T-Shirt</span></span> |
    | <span data-ttu-id="113b6-169">İlk birim</span><span class="sxs-lookup"><span data-stu-id="113b6-169">From unit</span></span>             | <span data-ttu-id="113b6-170">Kutular</span><span class="sxs-lookup"><span data-stu-id="113b6-170">Boxes</span></span>   |
    | <span data-ttu-id="113b6-171">Katsayı</span><span class="sxs-lookup"><span data-stu-id="113b6-171">Factor</span></span>                | <span data-ttu-id="113b6-172">5</span><span class="sxs-lookup"><span data-stu-id="113b6-172">5</span></span>       |
    | <span data-ttu-id="113b6-173">Son Birim</span><span class="sxs-lookup"><span data-stu-id="113b6-173">To Unit</span></span>               | <span data-ttu-id="113b6-174">Parça</span><span class="sxs-lookup"><span data-stu-id="113b6-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="113b6-175">Birim dönüştürmelerini güncelleştirmek için Excel kullanmak</span><span class="sxs-lookup"><span data-stu-id="113b6-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="113b6-176">Bir üründe, farklı birim dönüştürmeleri olan birçok ürün çeşidi varsa birim dönüştürmelerini bir Microsoft Excel çalışma kitabına aktarmak, güncelleştirmek ve ardından tekrar Dynamics 365 Supply Chain Management uygulamasına yayımlamak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="113b6-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="113b6-177">Birim dönüştürmelerini Excel'e aktarmak için **Birim dönüştürmeleri** sayfasında, Eylem Bölmesi'nde **Microsoft Office uygulamasında aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="113b6-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="113b6-178">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="113b6-178">Additional resources</span></span>

[<span data-ttu-id="113b6-179">Ölçü birimlerini yönetme</span><span class="sxs-lookup"><span data-stu-id="113b6-179">Manage units of measure</span></span>](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]