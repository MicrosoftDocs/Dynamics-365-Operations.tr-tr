---
title: Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodları
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodlarıyla nasıl çalışılacağı açıklanmaktadır
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941894"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="01683-103">Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodları</span><span class="sxs-lookup"><span data-stu-id="01683-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01683-104">Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodları, sevk edilebilecek maddeleri sınıflandırmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="01683-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="01683-105">NMFC kodu, emtiaları gruplamak için kullanılan bir atamadır.</span><span class="sxs-lookup"><span data-stu-id="01683-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="01683-106">Taşıma şirketlerinin, kamyonu alanı, yükleme sorunları, işleme sorunları ve bozulabilirlik gibi konulara göre maddeleri sınıflandırarak sevk edilecek malları değerlendirmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="01683-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="01683-107">Emtialar, 50 ile 500 arasında bir sayı aralığı kullanılarak 18 navlun sınıfından biri olarak gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="01683-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="01683-108">Bir emtianın gruplandırıldığı sınıf, dört taşıma özelliği değerlendirmesine dayanır: yoğunluk, stoklanabilirlik, idare ve yükümlülük.</span><span class="sxs-lookup"><span data-stu-id="01683-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="01683-109">Birlikte, bu özellikler emtianın taşınabilirliğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01683-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="01683-110">NMFC kodu, tüm kamyon yükünden az (LTL) sevk maddesiyle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="01683-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="01683-111">Örneğin, bir dizüstü bilgisayara 2,5 olarak sınıflandırılmış bir NMFC atanırken elektrik kablolarına 65 olarak sınıflandırılmış bir NMFC atanabilir.</span><span class="sxs-lookup"><span data-stu-id="01683-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="01683-112">Bu özellik, çalışanların LTL sevkiyat maddelerini sınıflandırmak için NMFC kodlarını kullanmasına yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="01683-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="01683-113">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="01683-113">Here are some examples:</span></span>

- <span data-ttu-id="01683-114">Şirketinizde konşimento (BOL) üzerinde bir navlun açıklaması varsa, taşıyıcının navlunun ne olduğuna dair bir fikri olacaktır.</span><span class="sxs-lookup"><span data-stu-id="01683-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="01683-115">Birçok taşımacılık şirketi, iş modellerini sevk edilen navlun türlerine dayandırdığı için navlun önemli bir sınıflandırmadır.</span><span class="sxs-lookup"><span data-stu-id="01683-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="01683-116">Belirli bir yükün maliyetini belirlemek için kullanıldığından, bu sınıflandırma şirketiniz için gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="01683-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="01683-117">Şirketiniz, bir LTL lojistik ve taşımacılık şirketinin karlılığını tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="01683-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="01683-118">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta NMFC kodlarıyla nasıl çalışılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="01683-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="01683-119">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="01683-119">Prerequisites</span></span>

<span data-ttu-id="01683-120">NMFC kodlarını oluşturabilmeniz için önce kendileriyle eşleştirilmesi gereken tüm LTL navlun sınıflarını ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="01683-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="01683-121">LTL navlun sınıfları maddelerin kategorilerini temsil ederken, NMFC kodları 18 navlun sınıfındaki belirli emtialarla ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="01683-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="01683-122">LTL sınıflarıyla nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Kamyon yükünden az (LTL) sınıfları](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="01683-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="01683-123">Bir NMFC kodu oluşturma</span><span class="sxs-lookup"><span data-stu-id="01683-123">Create an NMFC code</span></span>

<span data-ttu-id="01683-124">Bir NMFC kodu oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="01683-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="01683-125">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="01683-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="01683-126">**Ambar yönetimi \> Kurulum \> Stok \> NMFC kodları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="01683-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="01683-127">**Taşımacılık yönetimi \> Kurulum \> Taşıma standartları \> NMFC kodları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="01683-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="01683-128">Bir NMFC kodu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="01683-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="01683-129">Ardından aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="01683-129">Then set the following fields:</span></span>

    - <span data-ttu-id="01683-130">**NMFC kodu** – Emtia türü için NMFC kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="01683-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="01683-131">**Ad** – NMFC kodu için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="01683-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="01683-132">**LTL sınıfı** – NMFC koduyla ilişkilendirilmiş LTL sınıfını seçin.</span><span class="sxs-lookup"><span data-stu-id="01683-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="01683-133">**BOL işleme birimi** – Sevkiyatın varsayılan işleme türünü tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="01683-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="01683-134">Örnek: NMFC kodlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="01683-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="01683-135">Aşağıdaki örnekte, farklı ürünlerle kullanabileceğiniz iki farklı NMFC kodunun nasıl ayarlanacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="01683-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="01683-136">**Ambar yönetimi \> Kurulum \> Stok \> NMFC kodları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="01683-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="01683-137">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="01683-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="01683-138">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="01683-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="01683-139">**NMFC kodu:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="01683-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="01683-140">**Ad:** *Bilgisayarlar*</span><span class="sxs-lookup"><span data-stu-id="01683-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="01683-141">**LTL sınıfı:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="01683-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="01683-142">**BOL işleme birimi:** *Birim*</span><span class="sxs-lookup"><span data-stu-id="01683-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="01683-143">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="01683-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="01683-144">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="01683-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="01683-145">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="01683-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="01683-146">**NMFC kodu:** *125*</span><span class="sxs-lookup"><span data-stu-id="01683-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="01683-147">**Ad:** *Telefonlar*</span><span class="sxs-lookup"><span data-stu-id="01683-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="01683-148">**LTL sınıfı:** *125*</span><span class="sxs-lookup"><span data-stu-id="01683-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="01683-149">**BOL işleme birimi:** *Birim*</span><span class="sxs-lookup"><span data-stu-id="01683-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="01683-150">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="01683-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01683-151">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="01683-151">Additional resources</span></span>

- [<span data-ttu-id="01683-152">Kamyon yükünden az (LTL) sınıfları</span><span class="sxs-lookup"><span data-stu-id="01683-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="01683-153">Konşimento oluşturma</span><span class="sxs-lookup"><span data-stu-id="01683-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
