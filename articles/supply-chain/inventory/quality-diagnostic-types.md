---
title: Uygunsuzluklar için tanılama türleri
description: Bu konu, uygunsuzluklar ile kullanılabilecek tanılama türlerinin nasıl kullanılacağını ve oluşturulacağını açıklar.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022288"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="73059-103">Uygunsuzluklar için tanılama türleri</span><span class="sxs-lookup"><span data-stu-id="73059-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73059-104">Bu konu, uygunsuzluklar ile kullanılabilecek tanılama türlerinin nasıl kullanılacağını ve oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="73059-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="73059-105">Tanılama işlemleri için bir sınıflandırma tanımlamak için **Tanılama türleri** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="73059-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="73059-106">Daha sonra, uygunsuzluk için bir düzeltme oluşturduğunuzda bir tanı seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="73059-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="73059-107">Bir düzeltme, onaylanan bir uyumsuzluk için hangi türde tanılama işleminin yürütülmesi ve bu işlemin kimin tarafından gerçekleştirilmesi gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="73059-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="73059-108">Ayrıca, istenen tamamlanma tarihi ve planlanan tamamlanma tarihini belirtir.</span><span class="sxs-lookup"><span data-stu-id="73059-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="73059-109">Tanılama türlerine örnekler</span><span class="sxs-lookup"><span data-stu-id="73059-109">Examples of diagnostic types</span></span>

<span data-ttu-id="73059-110">Bir üretim şirketi için çalışıyorsunuz ve birkaç maddenin kalite testi başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="73059-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="73059-111">Bu maddeler, karantina alanına taşınır ve uygunsuz ürün olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="73059-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="73059-112">Microsoft Dynamics 365 Supply Chain Management'ta sorun çözme yoluyla ayrıntıları izlemek için bir uygunsuzluk kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="73059-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="73059-113">Bu durumda; kalite sorunları, maddeleri paketleyen makinedeki rulmanlar bozuk olduğundan ve aşırı ısındığından ortaya çıkmıştır.</span><span class="sxs-lookup"><span data-stu-id="73059-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="73059-114">Bu sorunla ilgili düzeltme, makine parçalarını değiştirmektir.</span><span class="sxs-lookup"><span data-stu-id="73059-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="73059-115">Tanılama türlerini yapılandırdığınızda, birden fazla kayıt oluşturabilirsiniz ve bunlardan her biri makinenin sahip olabileceği farklı türde bir sorunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="73059-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="73059-116">Alternatif olarak, makine onarımını temsil eden genel bir tanılama türü oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73059-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="73059-117">Tanılama türü oluşturma</span><span class="sxs-lookup"><span data-stu-id="73059-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="73059-118">**Stok yönetimi \> Kurulum \> Kalite yönetimi \> Tanı türleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="73059-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="73059-119">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="73059-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="73059-120">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="73059-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="73059-121">**Tanılama** – Tanılama türünün benzersiz tanımlayıcı kodunu veya adını girin.</span><span class="sxs-lookup"><span data-stu-id="73059-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="73059-122">**Açıklama** – Tanılama türünün detaylı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="73059-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="73059-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="73059-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73059-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="73059-124">Additional resources</span></span>

- [<span data-ttu-id="73059-125">Kalite yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="73059-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="73059-126">Kalite ve uygunsuzluk yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="73059-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="73059-127">Uygunsuzlukları onaylamaktan sorumlu çalışanlar</span><span class="sxs-lookup"><span data-stu-id="73059-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="73059-128">Uygunsuzluklar için karantina bölgeleri</span><span class="sxs-lookup"><span data-stu-id="73059-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="73059-129">Uygunsuzluklar için sorun türleri</span><span class="sxs-lookup"><span data-stu-id="73059-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="73059-130">Uygunsuzluklar için kalite masrafları</span><span class="sxs-lookup"><span data-stu-id="73059-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="73059-131">Uygunsuzluklar için işlemler</span><span class="sxs-lookup"><span data-stu-id="73059-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="73059-132">Ambar işlemleri için kalite yönetimi</span><span class="sxs-lookup"><span data-stu-id="73059-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
