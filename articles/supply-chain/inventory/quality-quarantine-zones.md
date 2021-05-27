---
title: Uygunsuzluklar için karantina bölgeleri
description: Bu konu, uygunsuzluklar için karantina bölgelerinin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f4b9dfc7882af4570bf1908784b8d114396402
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021816"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="0caba-103">Uygunsuzluklar için karantina bölgeleri</span><span class="sxs-lookup"><span data-stu-id="0caba-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0caba-104">Bu konu, uygunsuzluklar için karantina bölgelerinin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0caba-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="0caba-105">Uygunsuzluklara atanabilecek bölgeleri tanımlamak için **Karantina bölgeleri** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="0caba-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="0caba-106">Uygunsuzluk oluşturduğunuz zaman, **Uygunsuzluklar** sayfasının **Genel** sekmesindeki **Karantina bölgesi** ve **Karantina türü** alanlarını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0caba-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="0caba-107">**Karantina bölgesi** alanı, genellikle maddenin bulunduğu alanı veya konumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0caba-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="0caba-108">**Karantina türü** alanı, maddeyi *Kısıtlı kullanım* veya *Kullanılamaz* olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0caba-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="0caba-109">,Uygunsuzluk için uygunsuzluk veya düzeltme raporu yazdırdığınızda, maddenin bulunduğu karantina bölgesini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0caba-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="0caba-110">Uyum yapılamayan bir etiketi de yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0caba-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="0caba-111">Bu rapor, kusurlu malzemelerin nasıl işlenmesi gerektiği hakkında kılavuz sağlamak için, atanan karantina bölgesini ve kullanım hakkında bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="0caba-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="0caba-112">Karantina bölgeleri, envanter konumlarına veya operasyon kaynaklarına karşılık gelebilir.</span><span class="sxs-lookup"><span data-stu-id="0caba-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="0caba-113">Karantina bölgelerine örnekler</span><span class="sxs-lookup"><span data-stu-id="0caba-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="0caba-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0caba-114">Example 1</span></span>

<span data-ttu-id="0caba-115">Televizyon, hoparlör ve medya oynatıcı üreten ve dağıtan bir elektronik üretim şirketinde çalışıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="0caba-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="0caba-116">Bu durumda, her bir ürün türünü temsil edecek bir karantina bölgesi yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0caba-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="0caba-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0caba-117">Example 2</span></span>

<span data-ttu-id="0caba-118">Uygunsuz maddeleri depolamak için üç bölme ve iki raf kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0caba-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="0caba-119">Bu durumda, her bir bölme ve raf için olmak üzere beş karantina bölgesi yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0caba-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="0caba-120">Karantina bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0caba-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="0caba-121">**Stok yönetimi \> Kurulum \> Kalite yönetimi \> Karantina bölgeleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="0caba-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="0caba-122">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0caba-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="0caba-123">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="0caba-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="0caba-124">**Karantina bölgesi** – Karantina bölgesi için benzersiz bir kod veya ad girin.</span><span class="sxs-lookup"><span data-stu-id="0caba-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="0caba-125">**Açıklama** – Karantina bölgesinin detaylı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="0caba-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="0caba-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0caba-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0caba-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0caba-127">Additional resources</span></span>

- [<span data-ttu-id="0caba-128">Kalite yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="0caba-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="0caba-129">Kalite ve uygunsuzluk yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0caba-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="0caba-130">Uygunsuzlukları onaylamaktan sorumlu çalışanlar</span><span class="sxs-lookup"><span data-stu-id="0caba-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="0caba-131">Uygunsuzluklar için sorun türleri</span><span class="sxs-lookup"><span data-stu-id="0caba-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="0caba-132">Uygunsuzluklar için tanılama türleri</span><span class="sxs-lookup"><span data-stu-id="0caba-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="0caba-133">Uygunsuzluklar için kalite masrafları</span><span class="sxs-lookup"><span data-stu-id="0caba-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="0caba-134">Uygunsuzluklar için işlemler</span><span class="sxs-lookup"><span data-stu-id="0caba-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="0caba-135">Ambar işlemleri için kalite yönetimi</span><span class="sxs-lookup"><span data-stu-id="0caba-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
