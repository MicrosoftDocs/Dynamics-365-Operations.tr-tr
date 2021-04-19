---
title: Ürün yaşam döngüsü durumunu serbest bırakılan bir ana ürüne atama
description: Bu yordam, serbest bırakılan bir ana ürüne ve onun ürün çeşitlerine nasıl ürün yaşam döngüsü durumu atanacağını açıklar.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66859c7f7f5be6eaadd9470fd9b792daa28ce33d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807900"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="e8b3a-103">Ürün yaşam döngüsü durumunu serbest bırakılan bir ana ürüne atama</span><span class="sxs-lookup"><span data-stu-id="e8b3a-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8b3a-104">Bu yordam, serbest bırakılan bir ana ürüne ve onun ürün çeşitlerine nasıl ürün yaşam döngüsü durumu atanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="e8b3a-105">Önkoşul: Bu görev kılavuzunu oynatabilmek için önce "Yeni ürün yaşam döngüsü durumu oluşturma" görev kılavuzunu oynatarak en az bir ürün yaşam döngüsü durumu oluşturmuş olduğunuzdan emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="e8b3a-106">Serbest bırakılan bir ana ürünü bulma</span><span class="sxs-lookup"><span data-stu-id="e8b3a-106">Find a released product master</span></span>
1. <span data-ttu-id="e8b3a-107">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="e8b3a-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="e8b3a-109">Bir ana üründe Ürün alt türü Ana ürün bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="e8b3a-110">Yaşam döngüsü durumunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e8b3a-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="e8b3a-111">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-111">Click Edit.</span></span>
2. <span data-ttu-id="e8b3a-112">Ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="e8b3a-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-113">Click Save.</span></span>
4. <span data-ttu-id="e8b3a-114">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="e8b3a-115">Evet seçilirse, serbest bırakılan ana ürünle aynı orijinal duruma sahip serbest bırakılmış tüm ilgili ürün çeşitleri de yeni ürün yaşam döngüsü durumuna güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="e8b3a-116">Hayır seçilirse tüm ürün çeşitlerinin geçerli durumları korunur.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="e8b3a-117">Serbest bırakılan ana üründen farklı ürün yaşam döngüsü durumuna sahip ürün çeşitleri güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="e8b3a-118">Ürün çeşitlerinin yaşam döngüsü durumunu doğrulama</span><span class="sxs-lookup"><span data-stu-id="e8b3a-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="e8b3a-119">Serbest bırakılan ürün çeşitleri'ne tıklayın</span><span class="sxs-lookup"><span data-stu-id="e8b3a-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="e8b3a-120">Tüm ürün çeşitlerinin seçilen yaşam döngüsü durumunu serbest bırakılan ana üründen devraldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="e8b3a-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="e8b3a-122">Ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e8b3a-122">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]