---
title: Kamyon yükünden az (LTL) sınıfları
description: Bu konu, kamyon yükünden az (LTL) sınıflarının ne olduğunu açıklar ve Microsoft Dynamics 365 Supply Chain Management'ta bunların nasıl ayarlanacağını açıklar .
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941822"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="7870f-103">Kamyon yükünden az (LTL) sınıfları</span><span class="sxs-lookup"><span data-stu-id="7870f-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7870f-104">Kamyon yükünden az (LTL) sınıfı, sevk edilebilecek maddeleri sınıflandırmak için kullanılan bir navlun sevkiyat sınıfıdır.</span><span class="sxs-lookup"><span data-stu-id="7870f-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="7870f-105">Genellikle, her ürün veya emtia türü, LTL sevkiyatları için belirli bir navlun sınıfı numarasına karşılık gelen bir Ulusal Motorlu Navlun Sınıflandırması (NMFC) koduna sahiptir.</span><span class="sxs-lookup"><span data-stu-id="7870f-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="7870f-106">LTL navlun sınıfları maddelerin kategorilerini temsil ederken, NMFC kodları 18 navlun sınıfındaki belirli emtialarla ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="7870f-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="7870f-107">Bu özellik, sisteminizi kullanarak aşağıdaki görevleri yerine getirmenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="7870f-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="7870f-108">Şirketinizde kullanılan LTL navlun sınıflarını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="7870f-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="7870f-109">Her LTL sınıfını **NMFC kodları** sayfasındaki bir NMFC koduna atayın.</span><span class="sxs-lookup"><span data-stu-id="7870f-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="7870f-110">Daha fazla bilgi için bkz. [Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodları](nmfc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7870f-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="7870f-111">**Ürünler** sayfasındaki her ürüne bir NMFC kodu (ve böylece ilişkilendirilmiş LTL kodu) atayın.</span><span class="sxs-lookup"><span data-stu-id="7870f-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="7870f-112">Bir NMFC kodunun atandığı her ürünün LTL sınıfını doğru şekilde değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="7870f-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="7870f-113">Uluslararası LTL standartlarını denetleyerek her LTL sınıfı için ambalaj gereksinimlerini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7870f-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="7870f-114">Bu şekilde, ürünlerinizin iyi korunması ve güvenle sevk edilmesini güvence altına alırsınız.</span><span class="sxs-lookup"><span data-stu-id="7870f-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="7870f-115">Her bir ürün için LTL navlun sınıfına göre doğru sevkiyat tahminleri elde edin.</span><span class="sxs-lookup"><span data-stu-id="7870f-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="7870f-116">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta LTL sınıfları oluşturma yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7870f-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="7870f-117">LTL sınıfı oluşturma</span><span class="sxs-lookup"><span data-stu-id="7870f-117">Create an LTL class</span></span>

<span data-ttu-id="7870f-118">LTL sınıfı oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7870f-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="7870f-119">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="7870f-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="7870f-120">**Ambar yönetimi \> Kurulum \> Stok \> LTL sınıfları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="7870f-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="7870f-121">**Taşımacılık yönetimi \> Kurulum \> Taşıma standartları \> LTL sınıfları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="7870f-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="7870f-122">Eylem bölmesinde, bir LTL sınıfı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7870f-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="7870f-123">Ardından aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="7870f-123">Then set the following fields:</span></span>

    - <span data-ttu-id="7870f-124">**LTL sınıfı** – Şirketinizin emtia türü için dahili LTL sınıf tanımlayıcısını (ID) girin.</span><span class="sxs-lookup"><span data-stu-id="7870f-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="7870f-125">Birçok şirket uluslararası standardı kullanır.</span><span class="sxs-lookup"><span data-stu-id="7870f-125">Most companies use the international standard.</span></span> <span data-ttu-id="7870f-126">Bu durumda, bu alanın değeri **Sınıf** alanındaki değerle eşleşecektir .</span><span class="sxs-lookup"><span data-stu-id="7870f-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="7870f-127">Ancak, şirketiniz kendi standardını kullanıyorsa, o standarda uyan bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="7870f-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="7870f-128">**Ad** – Her bir NMFC kodu için doğru LTL sınıfını seçme konusunda size ve diğer kullanıcılara yardımcı olacak açıklayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="7870f-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="7870f-129">**Sınıf** – Emtia türü için uluslararası standart LTL sınıf kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="7870f-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="7870f-130">Buraya gireceğiniz kod, resmi standarda uygun olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7870f-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="7870f-131">Örnek: LTL sınıflarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="7870f-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="7870f-132">Aşağıdaki örnekte, farklı ürün türleriyle kullanabileceğiniz iki farklı LTL sınıfının nasıl ayarlanacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7870f-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="7870f-133">**Ambar yönetimi \> Kurulum \> Stok \> LTL sınıfları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="7870f-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="7870f-134">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7870f-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7870f-135">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="7870f-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="7870f-136">**LTL sınıfı:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="7870f-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="7870f-137">**Ad:** *Bilgisayarlar, monitörler, soğutucular*</span><span class="sxs-lookup"><span data-stu-id="7870f-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="7870f-138">**Sınıf:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="7870f-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="7870f-139">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7870f-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="7870f-140">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7870f-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7870f-141">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="7870f-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="7870f-142">**LTL sınıfı:** *125*</span><span class="sxs-lookup"><span data-stu-id="7870f-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="7870f-143">**Ad:** *Küçük ev aletleri*</span><span class="sxs-lookup"><span data-stu-id="7870f-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="7870f-144">**Sınıf:** *125*</span><span class="sxs-lookup"><span data-stu-id="7870f-144">**Class:** *125*</span></span>

1. <span data-ttu-id="7870f-145">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7870f-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7870f-146">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7870f-146">Additional resources</span></span>

- [<span data-ttu-id="7870f-147">Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodları</span><span class="sxs-lookup"><span data-stu-id="7870f-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="7870f-148">Konşimento oluşturma</span><span class="sxs-lookup"><span data-stu-id="7870f-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
