---
title: Uygunsuzlukları onaylamaktan sorumlu çalışanlar
description: Bu konuda, uygunsuzlukları onaylamaktan sorumlu çalışanları yapılandırma yöntemi açıklanmıştır.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d3f647de2c188661c2c9c5f31e2642c3f8ca0b5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021792"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="1d948-103">Uygunsuzlukları onaylamaktan sorumlu çalışanlar</span><span class="sxs-lookup"><span data-stu-id="1d948-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d948-104">Bu konuda, uygunsuzlukları onaylamaktan sorumlu çalışanları yapılandırma yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1d948-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="1d948-105">Kullanıcılar düzeltme veya işlemler gibi ayrıntıları girmeye başlamadan önce uygunsuzluklar onaylanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1d948-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="1d948-106">Kullanıcılar uygunsuzlukları onaylayabilmeden veya reddetmeden önce, kullanıcı kimliklerinin (kullanıcı kaydı) bir çalışan kaydıyla bağlantılı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d948-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="1d948-107">İsteğe bağlı olarak, kaliteden sorumlu çalışanları yapılandırabilir ve bir çalışanın başka bir çalışanın adına işi onaylamasına izin verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d948-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="1d948-108">Bir kullanıcıyı uygunsuzluk işleme için etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="1d948-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="1d948-109">Bir kullanıcı uygunsuzlukları onaylayabilmeden veya reddetmeden önce, kullanıcı kimliklerini (kullanıcı kaydı) bir çalışan kaydıyla bağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d948-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="1d948-110">Böylece, onay alanları otomatik olarak ayarlanabilir ve geçerli kullanıcı, zaman çizelgesi için otomatik olarak doldurulabilir.</span><span class="sxs-lookup"><span data-stu-id="1d948-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="1d948-111">Kullanıcı belge notlarını kullanabilmeden önce kullanıcı seçeneklerinde belge işleme seçeneğini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d948-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="1d948-112">**Sistem yönetimi \> Kullanıcılar \> Kullanıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="1d948-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="1d948-113">Uygunsuzlukları onaylayabilmek veya reddetme iznine sahip olacak kullanıcıyı bulun ve açın.</span><span class="sxs-lookup"><span data-stu-id="1d948-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="1d948-114">**Kişi** alanını, geçerli kullanıcı kaydıyla ilişkili çalışanın adı olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1d948-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="1d948-115">Eylem Bölmesinde, **Kullanıcı seçenekleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="1d948-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="1d948-116">Geçerli kullanıcı kaydının **Seçenekler** sayfasında **Tercihler** sekmesinde, **Belge işlemeyi etkinleştir** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1d948-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="1d948-117">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="1d948-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="1d948-118">Kaliteden sorumlu çalışanları tanımlama</span><span class="sxs-lookup"><span data-stu-id="1d948-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="1d948-119">**Stok yönetimi \> Kurulum \> Kalite kontrol \> Kaliteden sorumlu çalışanlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="1d948-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="1d948-120">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d948-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="1d948-121">**Çalışan** alanında, kalite verilerini giren çalışanı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d948-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="1d948-122">**Sorumlu çalışan** alanında, seçili çalışanın adına işleri girdiği çalışanı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d948-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="1d948-123">Uygunsuzluklar oluşturulup güncelleştirilirken bu çalışan, **Çalışan** alanlarına varsayılan olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="1d948-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d948-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1d948-124">Additional resources</span></span>

- [<span data-ttu-id="1d948-125">Kalite yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="1d948-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="1d948-126">Kalite ve uygunsuzluk yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="1d948-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="1d948-127">Kalite giderleri</span><span class="sxs-lookup"><span data-stu-id="1d948-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="1d948-128">Uygunsuzluklar için karantina bölgeleri</span><span class="sxs-lookup"><span data-stu-id="1d948-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="1d948-129">Uygunsuzluklar için tanılama türleri</span><span class="sxs-lookup"><span data-stu-id="1d948-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="1d948-130">Uygunsuzluklar için kalite masrafları</span><span class="sxs-lookup"><span data-stu-id="1d948-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="1d948-131">Uygunsuzluklar için işlemler</span><span class="sxs-lookup"><span data-stu-id="1d948-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="1d948-132">Ambar işlemleri için kalite yönetimi</span><span class="sxs-lookup"><span data-stu-id="1d948-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
