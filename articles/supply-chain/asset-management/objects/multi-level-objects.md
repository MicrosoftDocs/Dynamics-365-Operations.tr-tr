---
title: Çok düzeyli kıymetler
description: Bu konuda, çok düzeyli kıymetleri oluşturma ve silme açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd4da57c3849095909226db53c23b3c25301acdc
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021334"
---
# <a name="multi-level-assets"></a><span data-ttu-id="1ef4d-103">Çok düzeyli kıymetler</span><span class="sxs-lookup"><span data-stu-id="1ef4d-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1ef4d-104">Bu konuda, çok düzeyli kıymetleri oluşturma ve silme açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="1ef4d-105">Hiyerarşik ağaç yapısında kıymetler ve ilgili alt kıymetler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="1ef4d-106">Bu şekilde kıymetler arasındaki ilişkileri ve bağımlılıkları gösterebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="1ef4d-107">Bakım işleri, ağaç yapısının tüm düzeyleriyle ilgili olabilir.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="1ef4d-108">İstatistikler tek bir düzey veya tüm alt kıymet düzeylerinin toplamı olarak da oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="1ef4d-109">**Tüm Kıymetler** listesi sayfasında (**Kıymet yönetimi** \> **Ortak** \> **Kıymetler** \> **Tüm kıymetler**), **Kıymet** sütunu kıymetleri hiyerarşik düzende listeler.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="1ef4d-110">**Üst Öğe** sütunu ilgili üst öğe gösterilir.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="1ef4d-111">Ayrıca kıymetler ve alt kıymetler zaten oluşturulmuşsa **İlgili bilgiler** bölmesindeki **Kıymet ağacı** bölümü kıymetleri bir ağaç yapısında gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="1ef4d-112">Bir kıymet oluşturma hakkında bilgi için bkz. [Kıymet oluşturma](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="1ef4d-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="1ef4d-113">Bir alt kıymet oluşturmak için **Genel** hızlı sekmesinin **Üst Öğe** alanındaki üst kıymeti seçin.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="1ef4d-114">Kıymeti veya kıymet yapısını kopyalama</span><span class="sxs-lookup"><span data-stu-id="1ef4d-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="1ef4d-115">Şirketinizde birkaç benzer kıymet yapısı varsa, bunları hızla oluşturmak için Kıymet Yönetimi'ndeki Kopyala işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="1ef4d-116">**Kıymet yönetimi** \> **Ortak** \> **Kıymetler** \> **Tüm kıymetler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="1ef4d-117">**Tüm kıymetler** listesi sayfasında kopyalanacak kıymeti seçin.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="1ef4d-118">Örneğin alt kıymetler dahil olmak üzere tüm kıymet yapısını kopyalamak istiyorsanız bir üst kıymeti seçin.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="1ef4d-119">**Kıymeti kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-119">Select **Copy asset**.</span></span> <span data-ttu-id="1ef4d-120">**Kopyalama kaynağı** bölümünde, **Kıymet** alanı liste sayfasında seçtiğiniz kıymete ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="1ef4d-121">**Kopyalama hedefi** bölümündeki **Kıymet** alanında yeni kıymetin adını girin.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="1ef4d-122">Oluşturduğunuz kıymet mevcut kıymet yapısının parçasıysa **Üst kıymet** bölümündeki **Kıymet** alanında bir üst kimlik seçin.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="1ef4d-123">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-123">Select **OK**.</span></span> <span data-ttu-id="1ef4d-124">Yeni kıymet yapısı **Tüm kıymetler** listesi sayfasında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="1ef4d-125">Kopyaladığını kıymetle ilgili tüm kıymet öznitelikleri, bakım planları ve bakım sıraları yeni kıymete veya kıymet yapısına aktarılır.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="1ef4d-126">Bir kıymet yapısını kopyaladığınızda yeni yapıdaki alt kıymetler kopyaladığınız alt kıymetlerle aynı ada sahip olur.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="1ef4d-127">Kopyalama işlemi tamamlandıktan sonra bir kıymetin adını ve diğer ayarlarını kolayca değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="1ef4d-128">**Tüm kıymetler** listesi sayfasındaki kıymeti ve ardından **Düzenle** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="1ef4d-129">Bir kıymeti veya kıymet yapısını kopyaladığınızda yeni kıymetlerin yaşam döngüsü durumu kıymetler için ilk yaşam döngüsü durumu olarak tanımladığınız duruma sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="1ef4d-130">İşlem yapılacak yerleşim varsayılan işlem yapılacak yerleşime sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="1ef4d-131">Kıymeti veya kıymet yapısını silme</span><span class="sxs-lookup"><span data-stu-id="1ef4d-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="1ef4d-132">Bir kıymetin ilgili alt kıymetleri varsa kıymetler üzerinde kayıtlı bakım talepleri, iş emri işleri, arıza kayıtları veya koşul değerlendirmeleri yoksa kıymeti silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="1ef4d-133">**Tüm kıymetler** listesi sayfasında silinecek kıymeti seçin.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="1ef4d-134">**Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="1ef4d-135">Bir kıymeti bu yordamı kullanarak silemezseniz silme işlemini gerçekleştirmenin bir diğer yolu da bir kıymet yaşam döngüsü durumunu bu amaçla ayarlamaktır.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="1ef4d-136">Örneğin **Kıymet yaşam döngüsü durumlar** sayfasında **Iskarta** veya **Silindi** yaşam döngüsü durumu ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ef4d-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
