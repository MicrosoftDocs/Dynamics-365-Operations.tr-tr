---
title: Mali boyutlar
description: "Bu konu, çeşitli mali boyut türlerini ve nasıl ayarlandıklarını açıklar."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3e9f00fdc32feda0a62f71a92e503a677dce35cc
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="financial-dimensions"></a><span data-ttu-id="647da-103">Mali boyutlar</span><span class="sxs-lookup"><span data-stu-id="647da-103">Financial dimensions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="647da-104">Bu konu, çeşitli mali boyut türlerini ve nasıl ayarlandıklarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="647da-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="647da-105">Hesap planları içim hesap segmentleri olarak kullanabileceğiniz mali boyutlar oluşturmak için **Mali boyutlar** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="647da-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="647da-106">İki tür mali boyut vardır: özel boyutlar ve varlığa dayalı boyutlar.</span><span class="sxs-lookup"><span data-stu-id="647da-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="647da-107">Özel boyutlar tüzel kişilikler tarafından paylaşılır ve değerler kullanıcılar tarafından girilir ve korunur.</span><span class="sxs-lookup"><span data-stu-id="647da-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="647da-108">Varlığa dayalı boyutlar için sistemin herhangi başka bir bölümünde tanımlanan değerler, örneğin Müşteriler veya Mağaza varlıkları.</span><span class="sxs-lookup"><span data-stu-id="647da-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as Customers or Stores entities.</span></span> <span data-ttu-id="647da-109">Bazı varlığa dayalı boyutlar tüzel kişilikler tarafından paylaşılırken, diğer varlıklar şirkete özel boyutlar olur.</span><span class="sxs-lookup"><span data-stu-id="647da-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span> 

<span data-ttu-id="647da-110">Mali boyutları oluşturduktan sonra, her mali boyuta ek özellikler atamak için **Mali boyut değerleri** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="647da-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span> 

<span data-ttu-id="647da-111">Tüzel kişileri temsil etmek için mali boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="647da-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="647da-112">Tüzel varlıkları Microsoft Dynamics 365 for Finance and Operations içinde oluşturmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="647da-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="647da-113">Bununla birlikte, mali boyutlar, tüzel varlıkların operasyon veya iş gereksinimlerini karşılayacak şekilde tasarlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="647da-113">However, financial dimensions aren’t designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="647da-114">Finance and Operations'daki birimlerarası muhasebe işlevi, yalnızca her hareket tarafından oluşturulan muhasebe girişlerini karşılamak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="647da-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span> 

<span data-ttu-id="647da-115">Mali boyutları tüzel kişilikler olarak ayarlamadan önce, bu ayarın kuruluşunuz için uygun olup olmadığını belirlemek üzere iş süreçlerini aşağıdaki alanlarda değerlendirin:</span><span class="sxs-lookup"><span data-stu-id="647da-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="647da-116">Stok</span><span class="sxs-lookup"><span data-stu-id="647da-116">Inventory</span></span>
- <span data-ttu-id="647da-117">Mali boyutlar ile tüzel kişilikler arasındaki satışlar ve satınalmalar</span><span class="sxs-lookup"><span data-stu-id="647da-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="647da-118">Satış vergisi hesaplama ve bildirme</span><span class="sxs-lookup"><span data-stu-id="647da-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="647da-119">Operasyonel raporlama</span><span class="sxs-lookup"><span data-stu-id="647da-119">Operational reporting</span></span>

<span data-ttu-id="647da-120">Kısıtlamaların bazıları şunlardır:</span><span class="sxs-lookup"><span data-stu-id="647da-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="647da-121">Satış vergisi işlevini yalnızca tüzel kişiliklerle kullanabilirsiniz; mali boyutlarla birlikte kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="647da-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="647da-122">Bazı raporlar finansal boyutlar içermez.</span><span class="sxs-lookup"><span data-stu-id="647da-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="647da-123">Bu nedenle, finansal boyuta göre bildirmek için raporları değiştirmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="647da-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="647da-124">Özel boyutlar</span><span class="sxs-lookup"><span data-stu-id="647da-124">Custom dimensions</span></span>

<span data-ttu-id="647da-125">Kullanıcı tanımlı bir mali boyut oluşturmak için, **Kullanılan değerin kaynağı** alanından, **&lt; Özel boyut &gt;**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="647da-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt; Custom dimension &gt;**.</span></span> <span data-ttu-id="647da-126">Boyut değerleri için girebileceğiniz bilgi miktarını ve türünü sınırlamak üzere bir hesap maskesi de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="647da-126">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span> <span data-ttu-id="647da-127">Harf veya tire (-) gibi her boyut değeri için aynı kalan karakter girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="647da-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="647da-128">Bir boyut değeri her oluşturulduğunda değişen harfler ve sayılar için yer tutucular olan sayı işaretleri (\#) ve 've' işaretleri (&) de girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="647da-128">You can also enter number signs (\#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="647da-129">Bir sayının yer tutucusu olarak sayı işareti (\#) ve bir harfin yer tutucusu olarak ve işareti (&) kullanın.</span><span class="sxs-lookup"><span data-stu-id="647da-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="647da-130">Biçim maskesi için alan, yalnızca **&lt; Özel boyut &gt;**'u, **Kullanılan değerlerin kaynağı** alanından seçerseniz kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="647da-130">The field for the format mask is available only when you select **&lt; Custom dimension &gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="647da-131">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="647da-131">**Example**</span></span>

<span data-ttu-id="647da-132">Boyutu CC" harfleri ve üç sayıyla sınırlamak için biçim maskesi olarak **CC-\#\#\#** girin.</span><span class="sxs-lookup"><span data-stu-id="647da-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="647da-133">Varlığa dayalı boyutlar</span><span class="sxs-lookup"><span data-stu-id="647da-133">Entity-backed dimensions</span></span>

<span data-ttu-id="647da-134">Varlığa dayalı boyut oluşturmak için, **Kullanılacak değerlerin kaynağı** alanından, mali boyuta temel alınacak bir sistem tanımlı varlık seçin.</span><span class="sxs-lookup"><span data-stu-id="647da-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="647da-135">Mali boyut değerleri daha sonra o varlıktan oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="647da-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="647da-136">Örneğin, projeler için boyut değerleri oluşturmak üzere **Projeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="647da-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="647da-137">Daha sonra her proje adı için bir boyut değeri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="647da-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="647da-138">**Mali boyut değerleri** sayfası, varlık için değerleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="647da-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="647da-139">Bu değerler şirkete özelse, sayfa şirketi de gösterir.</span><span class="sxs-lookup"><span data-stu-id="647da-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="647da-140">Boyutları etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="647da-140">Activating dimensions</span></span>

<span data-ttu-id="647da-141">Bir mali boyutu etkinleştirdiğinizde, tablo mali boyutun adını da içermek üzere güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="647da-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="647da-142">Silinen boyutlar kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="647da-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="647da-143">Bir mali boyutu etkinleştirmeden önce boyut değerini girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="647da-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="647da-144">Ancak, bir mali boyut etkinleştirilene kadar hiçbir yerde tüketilemez.</span><span class="sxs-lookup"><span data-stu-id="647da-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="647da-145">Örneğin, mali boyut etkinleştirilene kadar bir hesap yapısına bir mali boyut ekleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="647da-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="647da-146">**Etkinleştir** üzerine tıkladığınızda, tüm boyutlar güncelleştirilir ve gösterme durumu değiştir.</span><span class="sxs-lookup"><span data-stu-id="647da-146">When you click **Activate**, all dimensions are updated and show status changes.</span></span> 

## <a name="translations"></a><span data-ttu-id="647da-147">Çeviriler</span><span class="sxs-lookup"><span data-stu-id="647da-147">Translations</span></span>

<span data-ttu-id="647da-148">**Metin çevirisi** sayfası üzerinde, seçili mali boyutlar için çeşitli dillerde metin girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="647da-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="647da-149">**Ana hesap çevirisi** sayfası üzerinde, ana hesap için çeşitli dillerde metin girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="647da-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="647da-150">Tüzel varlık geçersiz kılmaları</span><span class="sxs-lookup"><span data-stu-id="647da-150">Legal entity overrides</span></span>

<span data-ttu-id="647da-151">Her tüzel varlık için tüm boyutlar geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="647da-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="647da-152">Ek olarak, bazı boyutlar yalnızca belirli bir dönem için geçerli olabilir.</span><span class="sxs-lookup"><span data-stu-id="647da-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="647da-153">Bu durumlarda, **Tüzel varlık geçersiz kılmaları** bölümünü, boyutun askıya alınacağı şirketleri, sahibini ve boyutun etkin olacağı dönemi belirlemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="647da-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="647da-154">Mali boyutları silmek</span><span class="sxs-lookup"><span data-stu-id="647da-154">Deleting financial dimensions</span></span>

<span data-ttu-id="647da-155">Verinin referans tutarlılığını korumaya yardımcı olmak amacıyla, mali boyutlar nadiren silinebilir.</span><span class="sxs-lookup"><span data-stu-id="647da-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="647da-156">Bir mali boyutu silmeye çalışırsanız, aşağıdaki kriterler değerlendirilir:</span><span class="sxs-lookup"><span data-stu-id="647da-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="647da-157">Mali boyut, nakledilmiş veya nakledilmemiş hareketler veya boyut değeri kombinasyonu üzerinde kullanılmış mıdır?</span><span class="sxs-lookup"><span data-stu-id="647da-157">Has the financial dimension been used on any posted or unposted transactions, or any type of dimension value combination?</span></span>
- <span data-ttu-id="647da-158">Mali boyut, herhangi bir etkin hesap yapısında, gelişmiş kural yapısında veya mali boyut kümesinde kullanılıyor mu?</span><span class="sxs-lookup"><span data-stu-id="647da-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="647da-159">Mali boyut, bir varsayılan mali boyut tümleştirme biçiminin parçası mı?</span><span class="sxs-lookup"><span data-stu-id="647da-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="647da-160">Mali boyut, bir varsayılan mali boyut olarak ayarlanmış mı?</span><span class="sxs-lookup"><span data-stu-id="647da-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="647da-161">Kriterlerden herhangi biri karşılanıyorsa, mali boyutu silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="647da-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>


<span data-ttu-id="647da-162">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="647da-162">For more information, see the following topics:</span></span>
- [<span data-ttu-id="647da-163">Mali boyutları tanımlama</span><span class="sxs-lookup"><span data-stu-id="647da-163">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="647da-164">Mali boyut varsayılan şablonlarını koruma</span><span class="sxs-lookup"><span data-stu-id="647da-164">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)

