---
title: Uygunsuzluklar için sorun türleri
description: Bu konu, uygunsuzluklar için sorun türlerinin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 742edec8570610efe41a2c627efd1df586e0733e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022168"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="7cad5-103">Uygunsuzluklar için sorun türleri</span><span class="sxs-lookup"><span data-stu-id="7cad5-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cad5-104">Bu konu, uygunsuzluklar için sorun türlerinin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="7cad5-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="7cad5-105">Çeşitli uygunsuzluk türleri için karşılaşabileceğiniz kalite sorunlarıyla ilgili bir sınıflandırma tanımlamak için **Sorun türleri** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="7cad5-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="7cad5-106">Oluşturduğunuz her sorun türü için, sorun türünün kullanılabileceği uygunsuzlukları belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7cad5-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="7cad5-107">Aşağıdaki uygunsuzluk türlerini ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7cad5-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="7cad5-108">**Dahili** – Bu tip uygunsuzluklar, eldeki stokla ilgilidir (örneğin, kalite emirleri veya karantina emirleri).</span><span class="sxs-lookup"><span data-stu-id="7cad5-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="7cad5-109">**Müşteri** – Bu tip uygunsuzluklar, satış siparişleriyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="7cad5-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="7cad5-110">**Satıcı** – Bu tip uygunsuzluklar, satınalma siparişleriyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="7cad5-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="7cad5-111">**Hizmet talebi** – Bu tip uygunsuzluklar, hizmet siparişleriyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="7cad5-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="7cad5-112">**Üretim** – Bu tip uygunsuzluklar, toplu siparişler veya üretim emirleriyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="7cad5-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="7cad5-113">**Ortak ürün üretimi** – Bu tip uygunsuzluklar, toplu siparişler veya ortak ürünlerle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="7cad5-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="7cad5-114">Yeni bir sorun türü oluşturduğunuzda, sorun türü için yetkili olan bir veya daha fazla uygunsuzluk türünün listesini oluşturmak Için, Eylem Bölmesinde **Uygunsuzluk türleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7cad5-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="7cad5-115">Örneğin, bir koduyla ilgili bir sorun tipi, tüm uygunsuzluk tipleri için geçerli olabilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7cad5-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="7cad5-116">Ancak, müşteri şikayetleriyle ilgili bir sorun türü yalnızca **Müşteri** ve **Hizmet talebi** uygunsuzluk türlerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="7cad5-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="7cad5-117">Sorun türlerine örnekler</span><span class="sxs-lookup"><span data-stu-id="7cad5-117">Examples of problem types</span></span>

<span data-ttu-id="7cad5-118">Aşağıda, farklı uygunsuzluk tipleri ile kullanılabilecek sorun türleri için bazı senaryo örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="7cad5-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="7cad5-119">**Müşteri:** Bir müşteri şikayette bulundu, müşteri bir iade yaptı veya kalite gereksinimleri karşılanmadı.</span><span class="sxs-lookup"><span data-stu-id="7cad5-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="7cad5-120">**Satıcı:** Ürün zarar görmüş, kalite gereksinimleri karşılanmamış veya yanlış ürün alınmış.</span><span class="sxs-lookup"><span data-stu-id="7cad5-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="7cad5-121">**Hizmet talebi:** Kalite gereksinimleri karşılanmadı, müşteri bir şikayette bulundu veya makineye bakım yapılması gerekti.</span><span class="sxs-lookup"><span data-stu-id="7cad5-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="7cad5-122">**Üretim:** Kalite gereksinimleri karşılanmadı, makineye bakım yapılması gerekti veya ürün hasarlıydı.</span><span class="sxs-lookup"><span data-stu-id="7cad5-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="7cad5-123">**Ortak ürün üretimi:** Kalite gereksinimleri karşılanmadı, makineye bakım yapılması gerekti veya ürün hasarlıydı.</span><span class="sxs-lookup"><span data-stu-id="7cad5-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="7cad5-124">Sorun türü oluşturma ve bunu uygunsuzluk türlerine atama</span><span class="sxs-lookup"><span data-stu-id="7cad5-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="7cad5-125">**Stok yönetimi \> Kurulum \> Kalite yönetimi \> Problem türleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="7cad5-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="7cad5-126">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7cad5-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="7cad5-127">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="7cad5-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7cad5-128">**Sorun türü** – Sorun türünün benzersiz tanımlayıcı kodunu veya adını girin.</span><span class="sxs-lookup"><span data-stu-id="7cad5-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="7cad5-129">**Açıklama** – Sorun türünün detaylı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="7cad5-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="7cad5-130">Yeni satır seçiliyken, Eylem Bölmesinde **Uygunsuzluk türleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7cad5-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="7cad5-131">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7cad5-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="7cad5-132">Daha sonra yeni satır için, **Uygunsuzluk türü** alanını, sorunlu tür için izin vermek istediğiniz uygunsuzluk türüne ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7cad5-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="7cad5-133">Sorun türü için yetkilendirmek istediğiniz her ek uygunsuzluk türü için önceki adımı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="7cad5-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="7cad5-134">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="7cad5-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7cad5-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7cad5-135">Additional resources</span></span>

- [<span data-ttu-id="7cad5-136">Kalite yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="7cad5-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="7cad5-137">Kalite ve uygunsuzluk yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7cad5-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="7cad5-138">Uygunsuzlukları onaylamaktan sorumlu çalışanlar</span><span class="sxs-lookup"><span data-stu-id="7cad5-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="7cad5-139">Uygunsuzluklar için karantina bölgeleri</span><span class="sxs-lookup"><span data-stu-id="7cad5-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="7cad5-140">Uygunsuzluklar için tanılama türleri</span><span class="sxs-lookup"><span data-stu-id="7cad5-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="7cad5-141">Uygunsuzluklar için kalite masrafları</span><span class="sxs-lookup"><span data-stu-id="7cad5-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="7cad5-142">Uygunsuzluklar için işlemler</span><span class="sxs-lookup"><span data-stu-id="7cad5-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="7cad5-143">Ambar işlemleri için kalite yönetimi</span><span class="sxs-lookup"><span data-stu-id="7cad5-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
