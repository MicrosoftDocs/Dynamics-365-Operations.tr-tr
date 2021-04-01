---
title: Satış fiyatı seçim ölçütü oluşturma
description: Bu yordam, öznitelik tabanlı satış fiyat modelleri için satış fiyatı seçim ölçütlerinin nasıl oluşturulacağını gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84cef2cbf6f9783f0629fe068a4779a99dca9711
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258602"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="f33bf-103">Satış fiyatı seçim ölçütü oluşturma</span><span class="sxs-lookup"><span data-stu-id="f33bf-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f33bf-104">Bu yordam, öznitelik tabanlı satış fiyat modelleri için satış fiyatı seçim ölçütlerinin nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f33bf-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="f33bf-105">Bu yordam için kullanılabilir en az bir satış fiyatı modeli olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f33bf-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="f33bf-106">Bu örnek için, USMF demo veri şirketinde Hoparlör çözümü satış fiyatı modeli için fiyat modeli kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f33bf-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="f33bf-107">Genel olarak bu yordamı bir ürün yöneticisi kullanır.</span><span class="sxs-lookup"><span data-stu-id="f33bf-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="f33bf-108">Mevcut satış fiyatı modeli için yeni bir ölçüt ekleme</span><span class="sxs-lookup"><span data-stu-id="f33bf-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="f33bf-109">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f33bf-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="f33bf-110">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f33bf-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="f33bf-111">Listede, Hoparlör çözümü ürün modeli için satır seçin ancak model adı bağlantısına tıklamayın.</span><span class="sxs-lookup"><span data-stu-id="f33bf-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="f33bf-112">Eylem Bölmesinde,Model öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f33bf-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="f33bf-113">Fiyat modeli ölçütlerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f33bf-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="f33bf-114">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f33bf-114">Click New.</span></span>
7. <span data-ttu-id="f33bf-115">Ad alanına "Müşteri grubu 10" yazın.</span><span class="sxs-lookup"><span data-stu-id="f33bf-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="f33bf-116">Fiyat modeli ölçütünün adı, temel alınan seçim ölçütlerinin tanımlanmasına yardımcı olmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f33bf-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="f33bf-117">Fiyat modeli alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f33bf-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="f33bf-118">Sipariş türü alanında Satış siparişi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f33bf-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="f33bf-119">Sipariş türü seçim sorgusu için kullanılacak veri tabanı alanlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="f33bf-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="f33bf-120">Geçerlilik başlangıcı alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="f33bf-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="f33bf-121">Geçerlilik sonu alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="f33bf-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="f33bf-122">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f33bf-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="f33bf-123">Seçim ölçütleri için sorgu oluşturma</span><span class="sxs-lookup"><span data-stu-id="f33bf-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="f33bf-124">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f33bf-124">Click Edit.</span></span>
2. <span data-ttu-id="f33bf-125">Tablo alanında, Müşteriler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f33bf-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="f33bf-126">Alan alanında Müşteri grubu'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="f33bf-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="f33bf-127">Bu örnekte, seçim ölçütü için belirli bir müşteri grubu kullanacağız.</span><span class="sxs-lookup"><span data-stu-id="f33bf-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="f33bf-128">Ölçütler alanında Müşteri grubu 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="f33bf-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="f33bf-129">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f33bf-129">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]