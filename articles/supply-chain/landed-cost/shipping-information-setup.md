---
title: Sevkiyat bilgileri kurulumu
description: Bu konuda, Varış yeri maliyeti modülü için sevkiyat bilgilerinin nasıl ayarlanacağı açıklanmaktadır.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 5093e42b0b5247c24c271ad50c80889516586d58
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020899"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="c1d82-103">Sevkiyat bilgileri kurulumu</span><span class="sxs-lookup"><span data-stu-id="c1d82-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1d82-104">Bu konuda, **Varış yeri maliyeti** modülü için sevkiyat bilgilerinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c1d82-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="c1d82-105">Malların açıklaması</span><span class="sxs-lookup"><span data-stu-id="c1d82-105">Description of goods</span></span>

<span data-ttu-id="c1d82-106">Malların açıklamaları bir seyahatin, sevkiyat konteynerinin veya mal folyosunun ve içinde bulunan malların tanımlanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c1d82-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="c1d82-107">Sevkiyat konteyneri başlığında veya folyo başlığında malların açıklamasını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d82-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="c1d82-108">Malların açıklamalarıyla çalışmak için, **Varış yeri maliyeti \> Sevkiyat bilgileri kurulumu \> Malların açıklaması**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="c1d82-109">Burada, malların açıklamaları için kayıtları görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d82-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="c1d82-110">Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1d82-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="c1d82-111">Alan</span><span class="sxs-lookup"><span data-stu-id="c1d82-111">Field</span></span> | <span data-ttu-id="c1d82-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1d82-112">Description</span></span> |
|---|---|
| <span data-ttu-id="c1d82-113">Malların açıklaması</span><span class="sxs-lookup"><span data-stu-id="c1d82-113">Description of goods</span></span> | <span data-ttu-id="c1d82-114">Bu açıklamayı kullanacak mal türü için benzersiz bir kimlik adı/numarası girin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="c1d82-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1d82-115">Description</span></span> | <span data-ttu-id="c1d82-116">Bu kategorideki malların türünün açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="c1d82-117">Tekneler</span><span class="sxs-lookup"><span data-stu-id="c1d82-117">Vessels</span></span>

<span data-ttu-id="c1d82-118">Gemi, bir sevkiyat şirketinin veya acentesinin kullandığı bir geminin benzersiz adıdır.</span><span class="sxs-lookup"><span data-stu-id="c1d82-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="c1d82-119">Bir seyahat oluşturduğunuzda, her zaman bunun için bir gemi seçmeli veya girmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d82-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="c1d82-120">Sık sık aynı gemileri kullanıyorsanız her biri için bir gemi kaydı oluşturarak yeni bir seyahat oluşturmayı daha hızlı ve kolay hale getirebilirsiniz; böylece kullanıcıların her seferinde adı veya numarayı el ile girmeleri yerine gemiyi bir listeden seçmelerini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d82-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="c1d82-121">Gemilerle çalışmak için, **Varış yeri maliyeti \> Sevkiyat bilgileri kurulumu \> Gemiler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="c1d82-122">Burada, gemiler için kayıtları görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d82-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="c1d82-123">Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1d82-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="c1d82-124">Alan</span><span class="sxs-lookup"><span data-stu-id="c1d82-124">Field</span></span> | <span data-ttu-id="c1d82-125">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1d82-125">Description</span></span> |
|---|---|
| <span data-ttu-id="c1d82-126">Tekne</span><span class="sxs-lookup"><span data-stu-id="c1d82-126">Vessel</span></span> | <span data-ttu-id="c1d82-127">Bir seyahatte mal taşımak için kullanılacak gemi için benzersiz bir kimlik adı/numarası girin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="c1d82-128">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1d82-128">Description</span></span> | <span data-ttu-id="c1d82-129">Gemi için açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-129">Enter a description of the vessel.</span></span> <span data-ttu-id="c1d82-130">Genellikle, bu açıklama geminin ve sevkiyat şirketinin/acentesinin adını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c1d82-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="c1d82-131">Teslimat şekli</span><span class="sxs-lookup"><span data-stu-id="c1d82-131">Mode of delivery</span></span> | <span data-ttu-id="c1d82-132">Geminin kullandığı teslimat modunu seçin _(Hava yolu_, _Deniz yolu_ veya _Demir yolu_ gibi).</span><span class="sxs-lookup"><span data-stu-id="c1d82-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="c1d82-133">İhracatçılar</span><span class="sxs-lookup"><span data-stu-id="c1d82-133">Exporters</span></span>

<span data-ttu-id="c1d82-134">Her ihracatçı kaydı, bir seyahat için satıcı olarak tanımlanabilecek bir satıcı veya ihracatçı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c1d82-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="c1d82-135">İhracatçı bir seyahatle ilişkilendirilebilir ve raporlama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c1d82-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="c1d82-136">İhracatçılarla çalışmak için **Varış yeri maliyeti \> Sevkiyat bilgileri kurulumu \> Gemiler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="c1d82-137">Burada, ihracatçılar için kayıtları görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d82-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="c1d82-138">Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1d82-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="c1d82-139">Alan</span><span class="sxs-lookup"><span data-stu-id="c1d82-139">Field</span></span> | <span data-ttu-id="c1d82-140">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1d82-140">Description</span></span> |
|---|---|
| <span data-ttu-id="c1d82-141">İhracatçı</span><span class="sxs-lookup"><span data-stu-id="c1d82-141">Exporter</span></span> | <span data-ttu-id="c1d82-142">Bir seyahatte taşınan malların ihracatçısı için benzersiz bir kimlik adı/numarası girin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="c1d82-143">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1d82-143">Description</span></span> | <span data-ttu-id="c1d82-144">İhracatçı için açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-144">Enter a description of the exporter.</span></span> <span data-ttu-id="c1d82-145">Genellikle, bu açıklama sevkiyat şirketinin/acentesinin tam adını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c1d82-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="c1d82-146">Emtia kodları</span><span class="sxs-lookup"><span data-stu-id="c1d82-146">Commodity codes</span></span>

<span data-ttu-id="c1d82-147">Gümrük tanımlamasına ve bir seyahatteki mallar için vergi oranlarının hesaplanmasına yardımcı olmak için emtia kodlarını kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="c1d82-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="c1d82-148">Emtia kodlarını **Serbest bırakılan ürünler** sayfasından seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d82-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="c1d82-149">Emtia kodlarıyla çalışmak için **Varış yeri maliyeti \> Sevkiyat bilgileri kurulumu \> Emtia kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="c1d82-150">Burada, emtia kodları için kayıtları görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d82-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="c1d82-151">Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1d82-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="c1d82-152">Alan</span><span class="sxs-lookup"><span data-stu-id="c1d82-152">Field</span></span> | <span data-ttu-id="c1d82-153">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1d82-153">Description</span></span> |
|---|---|
| <span data-ttu-id="c1d82-154">Emtia kodu</span><span class="sxs-lookup"><span data-stu-id="c1d82-154">Commodity code</span></span> | <span data-ttu-id="c1d82-155">Bu tür emtialar için benzersiz bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="c1d82-156">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1d82-156">Description</span></span> | <span data-ttu-id="c1d82-157">Emtia türü için açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="c1d82-158">Gümrük açıklaması</span><span class="sxs-lookup"><span data-stu-id="c1d82-158">Customs description</span></span>

<span data-ttu-id="c1d82-159">Gümrük açıklamaları, gümrük amacıyla malların tanımlanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c1d82-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="c1d82-160">**Serbest bırakılan ürünler** sayfasında veya satın alma siparişi satırlarında bir gümrük açıklaması seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d82-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="c1d82-161">Gümrük açıklamalarıyla çalışmak için **Varış yeri maliyeti \> Sevkiyat bilgileri kurulumu \> Gümrük açıklaması**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="c1d82-162">Burada, gümrük açıklamaları için kayıtları görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d82-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="c1d82-163">Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1d82-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="c1d82-164">Alan</span><span class="sxs-lookup"><span data-stu-id="c1d82-164">Field</span></span> | <span data-ttu-id="c1d82-165">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1d82-165">Description</span></span> |
|---|---|
| <span data-ttu-id="c1d82-166">Gümrük açıklaması</span><span class="sxs-lookup"><span data-stu-id="c1d82-166">Customs description</span></span> | <span data-ttu-id="c1d82-167">Bu tür gümrük sınıflandırması için benzersiz bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="c1d82-168">Genellikle, bu kod malların tanımı ve nitel değeri için bir gümrük idaresi tarafından sağlanan resmi açıklama olur.</span><span class="sxs-lookup"><span data-stu-id="c1d82-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="c1d82-169">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1d82-169">Description</span></span> | <span data-ttu-id="c1d82-170">Gümrük sınıflandırması için açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c1d82-170">Enter a description of the customs classification.</span></span> |
