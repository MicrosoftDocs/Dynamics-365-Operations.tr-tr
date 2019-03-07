---
title: Üretilen ya da temin edilen ürünleri ayarlama
description: Ürünler çeşitli şekillerde bulunabilir - üretilebilir (mamul) veya tedarik edilebilir (satın alınan). Bu makalede birden fazla kaynak kullanımının desteklenmesi için ürünlerin nasıl yapılandırılacağı ile ilgili bazı genel hususlar açıklanmıştır.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a910b5782c8f15cfdd4cf93ea883bc28a5ce8e1a
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2019
ms.locfileid: "338464"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="a17ff-104">Üretilen ya da temin edilen ürünleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="a17ff-104">Set up products that can be produced or procured</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a17ff-105">Ürünler çeşitli şekillerde bulunabilir - üretilebilir (mamul) veya tedarik edilebilir (satın alınan).</span><span class="sxs-lookup"><span data-stu-id="a17ff-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="a17ff-106">Bu makalede birden fazla kaynak kullanımının desteklenmesi için ürünlerin nasıl yapılandırılacağı ile ilgili bazı genel hususlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a17ff-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="a17ff-107">Çoklu kaynak, genellikle arada sırada üretilen satın alınmış bir ürün için ya da esas olarak üretilen bir ürün esasen satın alınan bir ürün haline gelecek şekilde değiştirildiğinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a17ff-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="a17ff-108">Ürün, ürün reçetesi ve rota bilgilerinin tanımlanabilmesi ve ürünün üretim emirlerinin desteklenmesi için önce üretilen ürün olarak belirlenir.</span><span class="sxs-lookup"><span data-stu-id="a17ff-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="a17ff-109">Üretim türü, **Ürün reçetesi** (ya da süreç üretimi için **Formül** veya **Ortak ürün**) şeklinde ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a17ff-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="a17ff-110">Standard maliyet kullandığınızda, üretilen ürün için ürün maliyet kaydı hesaplanabilir.</span><span class="sxs-lookup"><span data-stu-id="a17ff-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="a17ff-111">Ancak, ürün maliyeti kaydı satın alma amaçlarıyla istediğiniz standart maliyet ile eşleşmeyebilir.</span><span class="sxs-lookup"><span data-stu-id="a17ff-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="a17ff-112">Bu durumda, istediğiniz standart maliyet ürün maliyet kaydı için el ile girilmeli ve etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a17ff-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="a17ff-113">Maliyet hesaplaması için, zaman içinde ortaya çıkan farkları minimize etmek için bir mali dönem boyunca ürünün tedarik karmasını gösteren özel bir ürün reçetesi ve rota kullanmayı düşünün.</span><span class="sxs-lookup"><span data-stu-id="a17ff-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="a17ff-114">Ek olarak, bir tesiste üretilen bir ürün başka bir tesise aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="a17ff-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="a17ff-115">Bu nedenle, ürünün maliyeti el ile girilmeli ve transfer edildiği tesis için etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a17ff-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="a17ff-116">Üretilmiş bir ürünü daha üst düzeylerdeki ürünler için bir bileşen olarak kullandığınızda, satınalınan bir ürün olarak ele alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a17ff-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="a17ff-117">Bu kılavuz, bileşenin maliyetinin hesaplanıp hesaplanmadığına veya el ile girilip girilmediğine bakılmaksızın geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="a17ff-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="a17ff-118">Diğer bir deyişle, Ürün reçetesi hesaplaması ürünün maliyetini maliyetleri hesaplamak amacıyla ürünün ürün reçetesini ve rota bilgileri kullanmak yerine satın alınan bir bileşen olarak ele almalıdır.</span><span class="sxs-lookup"><span data-stu-id="a17ff-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="a17ff-119">Hesaplamanın gerçekleşmesini önlemek için, ürüne atanan ürün reçetesi hesaplama grubunda gömülü **Açılımı durdur** bayrağını seçin.</span><span class="sxs-lookup"><span data-stu-id="a17ff-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="a17ff-120">Master planlama hesaplamalarının ürün üzerinden gereksinimleri açmasını önlemek için ürün açılımı ya da ürün açılımı grubunda açılım dilimini 0 (sıfır) gün olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a17ff-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="a17ff-121">Master planlama hesaplaması, ürünü satın alınan bir ürün olarak ele alacaktır ve ürünün ürün reçetesi ve rota bilgileri için daha fazla hesaplama gerçekleştirmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="a17ff-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>





