---
title: Ürünleri Master planlama dışında tutmak için bir ürün yaşam döngüsü durumu oluşturma
description: Bu yordam, ürünleri Master planlama ve ürün reçetesi düzeyinde hesaplama dışında tutan yeni bir ürün yaşam döngüsü durumunun nasıl oluşturulacağını açıklar.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bb18f876e7d279624f60f01c5fbf4e449e9ab27
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986891"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="a8cb5-103">Ürünleri Master planlama dışında tutmak için bir ürün yaşam döngüsü durumu oluşturma</span><span class="sxs-lookup"><span data-stu-id="a8cb5-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8cb5-104">Bu yordam, ürünleri Master planlama ve ürün reçetesi düzeyinde hesaplama dışında tutan yeni bir ürün yaşam döngüsü durumunun nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="a8cb5-105">Geçersiz bir durum oluşturma</span><span class="sxs-lookup"><span data-stu-id="a8cb5-105">Create an obsolete state</span></span>
1. <span data-ttu-id="a8cb5-106">Ürün bilgileri yönetimi > Kurulum > Ürün yaşam döngüsü durumu seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="a8cb5-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-107">Click New.</span></span>
3. <span data-ttu-id="a8cb5-108">Durum alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="a8cb5-109">Planlama için etkin alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="a8cb5-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="a8cb5-111">Serbest bırakılan bir ürünle geçersiz durumunu ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="a8cb5-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="a8cb5-112">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-112">Close the page.</span></span>
2. <span data-ttu-id="a8cb5-113">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="a8cb5-114">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a8cb5-115">Örneğin, Ad ara alanına bir 'M00' değeriyle filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="a8cb5-116">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-116">Click Edit.</span></span>
5. <span data-ttu-id="a8cb5-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="a8cb5-118">Ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a8cb5-118">In the Product lifecycle state field, enter or select a value.</span></span>

