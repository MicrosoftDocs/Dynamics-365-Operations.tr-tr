---
title: Sevkiyat konteynerleri
description: Bu konuda, Varış yeri maliyeti modülü için sevkiyat konteynerlerinin nasıl ayarlanacağı açıklanmaktadır.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2f7e9435aa3d0d06e1cc51457a6343b807d76dc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833725"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="1d8a8-103">Sevkiyat konteyneri kurulumu</span><span class="sxs-lookup"><span data-stu-id="1d8a8-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d8a8-104">Bu konuda, **Varış yeri maliyeti** modülü için sevkiyat konteynerlerinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="1d8a8-105">Sevkiyat konteyneri türlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1d8a8-105">Set up shipping container types</span></span>

<span data-ttu-id="1d8a8-106">Sevkiyat konteyneri türleri, sevkiyat ve seyahat sırasında kullanılabilen sevkiyat konteyneri türlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="1d8a8-107">Sevkiyat konteyneri türleriyle çalışmak için **Varış yeri maliyeti \> Konteyner kurulumu \> Sevkiyat konteyneri türleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="1d8a8-108">Burada, konteyner türlerinizin kayıtlarını görüntüleyebilir, ekleyebilir ve kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="1d8a8-109">Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1d8a8-110">Alan</span><span class="sxs-lookup"><span data-stu-id="1d8a8-110">Field</span></span> | <span data-ttu-id="1d8a8-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d8a8-111">Description</span></span> |
|---|---|
| <span data-ttu-id="1d8a8-112">Sevkiyat konteyneri türü</span><span class="sxs-lookup"><span data-stu-id="1d8a8-112">Shipping container type</span></span> | <span data-ttu-id="1d8a8-113">Sevkiyat konteyneri türü için benzersiz bir tanımlama adı/numarası girin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="1d8a8-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d8a8-114">Description</span></span> | <span data-ttu-id="1d8a8-115">Sevkiyat konteyneri türü için açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="1d8a8-116">Hacim</span><span class="sxs-lookup"><span data-stu-id="1d8a8-116">Volume</span></span> | <span data-ttu-id="1d8a8-117">Bu tür sevkiyat konteynerlerinde izin verilen maksimum hacmi girin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="1d8a8-118">Ağırlık</span><span class="sxs-lookup"><span data-stu-id="1d8a8-118">Weight</span></span> | <span data-ttu-id="1d8a8-119">Bu tür nakliye konteynerlerinde izin verilen maksimum ağırlığı girin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="1d8a8-120">İade edilebilir</span><span class="sxs-lookup"><span data-stu-id="1d8a8-120">Returnable</span></span> | <span data-ttu-id="1d8a8-121">Bu tür sevkiyat konteynerlerinin bir seyahat sırasında kullanıldıktan sonra satıcıya iade edilip edilmeyeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="1d8a8-122">Bu seçenek *Evet* olarak ayarlanırsa bu tür sevkiyat konteynerlerinin çıkış limanına iadesi için ek maliyetler uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="1d8a8-123">Sevkiyat konteynerlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1d8a8-123">Set up shipping containers</span></span>

<span data-ttu-id="1d8a8-124">Seyahatler sırasında kullandığınız her konteyneri tanımlamak için sevkiyat konteyneri kayıtlarını kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="1d8a8-125">Bir seyahat oluşturduğunuzda, burada tanımladığınız tüm sevkiyat konteyneri kayıtları listesinde bunun için belirli bir konteyner seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="1d8a8-126">Bu özellik özellikle şirketiniz kendi sevkiyat konteynerlerine sahipse kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="1d8a8-127">Yalnızca bir kez kullanılacak sevkiyat konteynerleri için sevkiyat konteyneri numaraları girmeniz gerekmemektedir.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="1d8a8-128">Bunun yerine, bir seyahat oluşturduğunuzda sevkiyat konteyneri numarası ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="1d8a8-129">Sevkiyat konteyneri kayıtları yalnızca Varış yeri maliyetinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="1d8a8-130">Bunlar standart **Taşıma yönetimi** modülünde (TMS) mevcut değildir.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="1d8a8-131">Sevkiyat konteynerleriyle çalışmak için **Varış yeri maliyeti \> Konteynerleri ayarlama \> Sevkiyat konteynerleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="1d8a8-132">Burada, sevkiyat konteynerlerinizin kayıtlarını görüntüleyebilir, ekleyebilir ve kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="1d8a8-133">Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1d8a8-134">Alan</span><span class="sxs-lookup"><span data-stu-id="1d8a8-134">Field</span></span> | <span data-ttu-id="1d8a8-135">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d8a8-135">Description</span></span> |
|---|---|
| <span data-ttu-id="1d8a8-136">Sevkiyat konteyneri</span><span class="sxs-lookup"><span data-stu-id="1d8a8-136">Shipping container</span></span> | <span data-ttu-id="1d8a8-137">Sevkiyat konteyneri için benzersiz bir tanımlama adı/numarası girin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="1d8a8-138">Sevkiyat konteyneri türü</span><span class="sxs-lookup"><span data-stu-id="1d8a8-138">Shipping container type</span></span> | <span data-ttu-id="1d8a8-139">Sevkiyat konteyneri türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-139">Select the type of shipping container.</span></span> <span data-ttu-id="1d8a8-140">Daha fazla bilgi için bu konuda daha önce ele alınan [Sevkiyat konteyneri türlerini ayarlama](#shipping-container-types) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="1d8a8-141">Sevkiyat konteyneri kurulumu isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-141">The shipping container setup is optional.</span></span> <span data-ttu-id="1d8a8-142">Genellikle, yalnızca şirketiniz kendi sevkiyat konteynerlerine sahipse veya genellikle aynı sevkiyat konteynerlerini yeniden kullanıyorsa kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="1d8a8-143">Sevkiyat konteyneri numaraları için hiçbir denetleme basamağı hesaplanmaz.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="1d8a8-144">Birim türlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1d8a8-144">Set up unit types</span></span>

<span data-ttu-id="1d8a8-145">Birim türleri, sevkiyat konteynerleri için ek gruplandırmalar ve tanımlama yöntemleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="1d8a8-146">Birim türü genellikle paletler veya variller gibi malların paketli olduğu konteyner türünü tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="1d8a8-147">**Tüm sevkiyat konteynerleri** sayfasında bir konteyner ayarlarken bir birim türü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="1d8a8-148">Birim türleri yalnızca Varış yeri maliyetinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="1d8a8-149">TMS'de mevcut değildir.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-149">They aren't available in TMS.</span></span>

<span data-ttu-id="1d8a8-150">Birim türleriyle çalışmak için **Varış yeri maliyeti \> Konteynerleri ayarlama \> Birimi türleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="1d8a8-151">Burada, birim türlerinizin kayıtlarını görüntüleyebilir, ekleyebilir ve kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="1d8a8-152">Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1d8a8-153">Alan</span><span class="sxs-lookup"><span data-stu-id="1d8a8-153">Field</span></span> | <span data-ttu-id="1d8a8-154">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d8a8-154">Description</span></span> |
|---|---|
| <span data-ttu-id="1d8a8-155">Birim türü</span><span class="sxs-lookup"><span data-stu-id="1d8a8-155">Unit type</span></span> | <span data-ttu-id="1d8a8-156">Birim türü için benzersiz bir tanımlama adı/numarası girin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="1d8a8-157">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d8a8-157">Description</span></span> | <span data-ttu-id="1d8a8-158">Birim türü için açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="1d8a8-159">Soğutma türlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1d8a8-159">Set up refrigeration types</span></span>

<span data-ttu-id="1d8a8-160">Soğutma türleri, sevkiyat konteynerleri (genellikle soğutmalı konteynerler) için ek gruplandırmalar ve tanımlama yöntemleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="1d8a8-161">**Tüm sevkiyat konteynerleri** sayfasında bir konteyner ayarlarken bir soğutma türü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="1d8a8-162">Soğutma türleriyle çalışmak için **Varış yeri maliyeti \> Konteynerleri ayarlama \> Soğutma türleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="1d8a8-163">Burada, soğutma türlerinizin kayıtlarını görüntüleyebilir, ekleyebilir ve kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="1d8a8-164">Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1d8a8-165">Alan</span><span class="sxs-lookup"><span data-stu-id="1d8a8-165">Field</span></span> | <span data-ttu-id="1d8a8-166">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d8a8-166">Description</span></span> |
|---|---|
| <span data-ttu-id="1d8a8-167">Soğutma türü</span><span class="sxs-lookup"><span data-stu-id="1d8a8-167">Refrigeration type</span></span> | <span data-ttu-id="1d8a8-168">Soğutma türü için benzersiz bir tanımlama adı/numarası girin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="1d8a8-169">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d8a8-169">Description</span></span> | <span data-ttu-id="1d8a8-170">Soğutma türü için açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-170">Enter a description of the refrigeration type.</span></span> |
