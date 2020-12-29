---
title: Varlıkları taşıma, değiştirme ve yükleme
description: Bu konuda Varlık Yönetimi'nde varlıkların nasıl taşınacağı, değiştirileceği ve yükleneceği açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec150adb35eb0600844245b14cbec9e9632ab337
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439355"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="c30cd-103">Varlıkları taşıma, değiştirme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="c30cd-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c30cd-104">Bu konuda Varlık Yönetimi'nde varlıkların nasıl taşınacağı, değiştirileceği ve yükleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c30cd-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="c30cd-105">Başka varlıklarla ilişkisi olmayan bağımsız varlıklar oluşturabilir veya bir üst varlık (en üst düzey varlık) ve ilgili alt varlıklar (alt varlıklar) içeren bir varlık yapısı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c30cd-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="c30cd-106">Varlık Yönetiminde, bir varlığın yerleşimini taşımak ve değiştirmek için üç yaklaşım vardır:</span><span class="sxs-lookup"><span data-stu-id="c30cd-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="c30cd-107">**Taşı**: Varlığı başka bir varlık yapısına veya aynı varlık yapısındaki başka bir yerleşime taşıyın.</span><span class="sxs-lookup"><span data-stu-id="c30cd-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="c30cd-108">**Değiştir**: Bir varlığı onarılması veya yenilenmesi için bir varlık yapısından geçici olarak kaldırın ve yenilenen varlığı daha sonra varlık yapısına geri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="c30cd-109">Alternatif olarak, kullanılan varlığı kalıcı olarak yeni bir varlıkla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="c30cd-110">**Yükle**: İşlem yapılacak yerleşime bir üst varlık ve ilgili alt varlıkları yükleyin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="c30cd-111">Taşıdığınız, değiştirdiğiniz veya yüklediğiniz varlık başka bir işlem yapılacak yerleşimle ilişkili olabilir.</span><span class="sxs-lookup"><span data-stu-id="c30cd-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="c30cd-112">Bu durumda, varlık işlem yapılacak yerleşimin mali boyutlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="c30cd-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="c30cd-113">**İşlem yapılacak yerleşim türleri** sayfasında, işlem yapılacak yerleşimlerdeki mali boyutların işlenmesini ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="c30cd-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="c30cd-114">Varlığı taşı</span><span class="sxs-lookup"><span data-stu-id="c30cd-114">Move asset</span></span>

<span data-ttu-id="c30cd-115">Varlığı başka bir varlık yapısına veya aynı varlık yapısındaki başka bir yerleşime taşımak için **Varlığı taşı** işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c30cd-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="c30cd-116">Ayrıca, bir varlığı varlık yapısının dışına taşıyarak yapı ilişkileri içermeyen bağımsız bir varlık haline gelmesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c30cd-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="c30cd-117">Varlıklar onarılıyorsa veya geçici olarak değiştiriliyorsa bu işlevi kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="c30cd-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="c30cd-118">Bunun yerine, bu konunun ilerleyen kısımlarında açıklanan **Varlığı değiştir** işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c30cd-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="c30cd-119">**Varlık yönetimi** \> **Genel** \> **Varlıklar** \> **Tüm varlıklar** veya **Etkin varlıklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="c30cd-120">Listede, taşınacak varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-120">In the list, select the asset to move.</span></span> <span data-ttu-id="c30cd-121">Varlığın alt varlıkları varsa, bu varlıkları da taşırsınız.</span><span class="sxs-lookup"><span data-stu-id="c30cd-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="c30cd-122">**Varlığı taşı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="c30cd-123">Varlığı bir varlık yapısının parçası olacak şekilde taşımak için **Üst varlık** alanında yeni üst varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="c30cd-124">Bir alt varlığı taşıyorsanız ve bunu yapı ilişkileri bulunmayan bağımsız bir varlık yapmak istiyorsanız, **Üst varlık** alanını boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="c30cd-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="c30cd-125">Varsayılan olarak **Etkin** alanı mevcut tarih ve saate ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c30cd-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="c30cd-126">Ancak, varlık taşıma geçerlilik başlangıcı olarak farklı bir tarih ve saat seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c30cd-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="c30cd-127">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="c30cd-128">Varlığı değiştir</span><span class="sxs-lookup"><span data-stu-id="c30cd-128">Replace asset</span></span>

<span data-ttu-id="c30cd-129">Onarımlar, yenileme veya aşınmış bir varlığın yeni bir varlıkla kalıcı şekilde değiştirilmesiyle ilgili olarak **Varlığı değiştir** işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c30cd-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="c30cd-130">Bu işlev, bir varlık yapısındaki alt varlıkları değiştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c30cd-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="c30cd-131">Üst varlıklar için (henüz bir üst varlığı bulunmayan varlıklardır), bu değişiklik işlem yapılacak yerleşimde yapılır.</span><span class="sxs-lookup"><span data-stu-id="c30cd-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="c30cd-132">Alt varlıkların işlem yapılacak yerleşimde nasıl değiştirileceği hakkında daha fazla bilgi için bkz. [Varlıkları işlem yapılacak yerleşimlere yükleme](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="c30cd-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c30cd-133">Onarım atölyesi üretim departmanınızla ilişkiliyse, varlıkların onarımı ve değişimini gerçekleştirmek için **Onarım**, **Hurda** ve **Depolama** gibi işlem yapılacak yerleşimler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c30cd-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="c30cd-134">**Varlık yönetimi** \> **Genel** \> **Varlıklar** \> **Tüm varlıklar** veya **Etkin varlıklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="c30cd-135">Listede, değiştirilecek alt varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="c30cd-136">Varlığın alt varlıkları varsa, bu varlıkları da değiştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c30cd-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="c30cd-137">**Varlığı değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="c30cd-138">**Yapı değiştirme** alanı, seçilen varlıkların ve ilgili alt varlıkların varlık yapısında taşındığı son tarihi ve saati gösterir.</span><span class="sxs-lookup"><span data-stu-id="c30cd-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="c30cd-139">**Seçili varlık** bölümünde, **Hedef işlem yapılacak yerleşim** alanında, varlığın taşınacağı işlem yapılacak yerleşimi seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="c30cd-140">Örneğin, **Onarım** veya **Iskarta** yerleşimini seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="c30cd-141">**Üst varlık** bölümünde, **Etkin** alanı üst varlığın ve ilgili alt varlıkların geçerli işlem yapılacak yerleşime yüklendiği veya taşındığı son tarih ve saati gösterir.</span><span class="sxs-lookup"><span data-stu-id="c30cd-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="c30cd-142">**Yeni varlık** bölümünde, **Varlık** alanında, seçili varlık için geçici veya kalıcı değişiklik olarak eklenecek varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="c30cd-143">Bu varlık halihazırda **Depolama** gibi başka bir işlem yapılacak yerleşimde bulunuyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="c30cd-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="c30cd-144">**Yürürlük başlangıcı** bölümünde, **Etkin** alanı varsayılan olarak geçerli tarihe ve saate ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c30cd-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="c30cd-145">Ancak, varlık değiştirme geçerlilik başlangıcı olarak farklı bir tarih ve saat seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c30cd-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="c30cd-146">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="c30cd-147">Varlık yükle</span><span class="sxs-lookup"><span data-stu-id="c30cd-147">Install asset</span></span>

<span data-ttu-id="c30cd-148">Bir işlem yapılacak yerleşime varlık yapısı yüklemek için **Varlık yükle** işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c30cd-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="c30cd-149">Her zaman bir üst varlık seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-149">Always select a parent asset.</span></span> <span data-ttu-id="c30cd-150">Üst varlık ve ilgili alt varlıklar seçili işlem yapılacak yerleşime taşınır.</span><span class="sxs-lookup"><span data-stu-id="c30cd-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="c30cd-151">**Varlık yönetimi** \> **Genel** \> **Varlıklar** \> **Tüm varlıklar** veya **Etkin varlıklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="c30cd-152">Listede, başka bir işlem yapılacak yerleşime yüklenecek üst varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="c30cd-153">**Varlık yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-153">Select **Install asset**.</span></span>

    <span data-ttu-id="c30cd-154">**Öznitelikler** bölümü üst varlık üzerinde ayarlanan varlık özniteliklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c30cd-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="c30cd-155">**İşlem yapılacak yerleşim** alanında, yeni yerleşimi seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="c30cd-156">Varsayılan olarak **Etkin** alanı mevcut tarih ve saate ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c30cd-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="c30cd-157">Ancak, varlık yapısına yapılan yüklemenin geçerlilik başlangıcı olarak farklı bir tarih ve saat seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c30cd-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="c30cd-158">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c30cd-158">Select **OK**.</span></span>
