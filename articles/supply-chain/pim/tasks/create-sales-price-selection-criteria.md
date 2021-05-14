---
title: Satış fiyatı seçim ölçütü oluşturma
description: Bu yordam, öznitelik tabanlı satış fiyat modelleri için satış fiyatı seçim ölçütlerinin nasıl oluşturulacağını gösterir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920543"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="8c6fe-103">Satış fiyatı seçim ölçütü oluşturma</span><span class="sxs-lookup"><span data-stu-id="8c6fe-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c6fe-104">Bu yordam, öznitelik tabanlı satış fiyat modelleri için satış fiyatı seçim ölçütlerinin nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="8c6fe-105">Bu yordam için kullanılabilir en az bir satış fiyatı modeli olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="8c6fe-106">Bu örnek için, USMF demo veri şirketinde Hoparlör çözümü satış fiyatı modeli için fiyat modeli kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="8c6fe-107">Genel olarak bu yordamı bir ürün yöneticisi kullanır.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="8c6fe-108">Mevcut satış fiyatı modeli için yeni bir ölçüt ekleme</span><span class="sxs-lookup"><span data-stu-id="8c6fe-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="8c6fe-109">**Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="8c6fe-110">Listede, Hoparlör çözümü ürün modeli için satır seçin ancak model adı bağlantısını seçmeyin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="8c6fe-111">Eylem Bölmesinde, **Model**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="8c6fe-112">**Fiyat modeli ölçütleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="8c6fe-113">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-113">Select **New**.</span></span>
1. <span data-ttu-id="8c6fe-114">**Ad** alanına "Müşteri grubu 10" yazın.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="8c6fe-115">Fiyat modeli ölçütünün adı, temel alınan seçim ölçütlerinin tanımlanmasına yardımcı olmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="8c6fe-116">**Fiyat modeli** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="8c6fe-117">**Sipariş türü** alanında *Satış siparişi*'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="8c6fe-118">Sipariş türü seçim sorgusu için kullanılacak veri tabanı alanlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="8c6fe-119">**Geçerlilik başlangıcı** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="8c6fe-120">**Geçerlilik sonu** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="8c6fe-121">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="8c6fe-122">Seçim ölçütleri için sorgu oluşturma</span><span class="sxs-lookup"><span data-stu-id="8c6fe-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="8c6fe-123">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-123">Select **Edit**.</span></span>
2. <span data-ttu-id="8c6fe-124">**Tablo** alanında, *Müşteriler*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="8c6fe-125">**Alan** alanında *Müşteri grubu*'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="8c6fe-126">Bu örnekte, seçim ölçütü için belirli bir müşteri grubu kullanacağız.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="8c6fe-127">**Ölçütler** alanında *Müşteri grubu 10*'u seçin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="8c6fe-128">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]