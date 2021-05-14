---
title: Boyut tabanlı yapılandırmalar oluşturma
description: Bu prosedürde bir boyut tabanlı ürün için bir yapılandırmanın nasıl tanımlanacağı açıklanmıştır.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 584bb558ee0afeaffaeb003e9f1d1b0bca42d19d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920693"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="fecc4-103">Boyut tabanlı yapılandırmalar oluşturma</span><span class="sxs-lookup"><span data-stu-id="fecc4-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fecc4-104">Bu prosedürde bir boyut tabanlı ürün için bir yapılandırmanın nasıl tanımlanacağı açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="fecc4-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="fecc4-105">Bu prosedür, boyut tabanlı yapılandırma kombinasyonlarının nasıl oluşturacağını açıklayan serinin son prosedürüdür.</span><span class="sxs-lookup"><span data-stu-id="fecc4-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="fecc4-106">Bu prosedürün uygulanması önceki yedi kayıtta oluşturulan verilere bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fecc4-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="fecc4-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="fecc4-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="fecc4-108">Boyut tabanlı ürün mastarını bulma</span><span class="sxs-lookup"><span data-stu-id="fecc4-108">Find the dimension-based product master</span></span>

1. <span data-ttu-id="fecc4-109">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="fecc4-110">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fecc4-111">Bu 8 kayıtlı dizinde ilk kayıtta oluşturduğunuz boyut tabanlı ürün mastarını seçin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-111">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="fecc4-112">Yapılandırmalar oluşturma</span><span class="sxs-lookup"><span data-stu-id="fecc4-112">Create configurations</span></span>

1. <span data-ttu-id="fecc4-113">**Mühendislik** Eylem Bölmesi'nde, **Yapılandırmaları koru**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-113">On the **Engineering** Action Pane, select **Maintain configurations**.</span></span>
1. <span data-ttu-id="fecc4-114">**Yapılandır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-114">Select **Configure**.</span></span>
1. <span data-ttu-id="fecc4-115">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-115">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="fecc4-116">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-116">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="fecc4-117">İlk yapılandırma grubundaki maddelerden herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-117">Select any of the items in the first configuration group.</span></span>  
1. <span data-ttu-id="fecc4-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-118">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="fecc4-119">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-119">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="fecc4-120">İkinci yapılandırma grubundan herhangi bir maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-120">Select any item from the second configuration group.</span></span>  
1. <span data-ttu-id="fecc4-121">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-121">Select **OK**.</span></span>
1. <span data-ttu-id="fecc4-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-122">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="fecc4-123">**Yapılandırma** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="fecc4-123">In the **Configuration** field, type a value.</span></span>
    * <span data-ttu-id="fecc4-124">Yapılandırmayı kolayca tanımlamanıza yardımcı olacak bir yapılandırma adı girin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-124">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
1. <span data-ttu-id="fecc4-125">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-125">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="fecc4-126">İçeriğini açıklamak için bir yapılandırma açıklaması girin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-126">Enter a description of the configuration to explain what it contains.</span></span>  
1. <span data-ttu-id="fecc4-127">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fecc4-127">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]