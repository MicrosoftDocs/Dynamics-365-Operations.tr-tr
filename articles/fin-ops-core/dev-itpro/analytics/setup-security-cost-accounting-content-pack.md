---
title: Maliyet muhasebesi analizi Power BI içeriğinin güvenliğini ayarlama
description: Bu konuda, Maliyet muhasebesindeki erişim düzeyinde güvenliği, Microsoft Power BI'daki satır düzeyinde güvenliğe nasıl yayabileceğiniz açıklanmaktadır. Bu işlevsellik, kullanıcıların yalnızca erişim izni verilen Power BI verilerini görmelerini garantilemeye yardımcı olur.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b0f7dffd85dc1c7a58a3e1f55eaa26ecbf6e8360
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185187"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="e4be0-104">Maliyet muhasebesi analizi Power BI içeriğinin güvenliğini ayarlama</span><span class="sxs-lookup"><span data-stu-id="e4be0-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4be0-105">Bu konuda, Maliyet muhasebesindeki erişim düzeyinde güvenliği, Microsoft Power BI'daki satır düzeyinde güvenliğe nasıl yayabileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e4be0-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="e4be0-106">Bu işlevsellik, kullanıcıların yalnızca erişim izni verilen Power BI verilerini görmelerini garantilemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e4be0-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="e4be0-107">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="e4be0-107">Overview</span></span>

<span data-ttu-id="e4be0-108">**Maliyet muhasebesi analizi** Microsoft Power BI içeriği, kullanıcının erişimini sınırlamak için Power BI'ın satır düzeyinde güvenliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e4be0-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="e4be0-109">Güvenlik, Maliyet muhasebesi parametrelerinde ayarlanan erişim düzeyinde organizasyon hiyerarşisine dayanır.</span><span class="sxs-lookup"><span data-stu-id="e4be0-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="e4be0-110">**Maliyet muhasebesi analizi** Power BI içeriği hakkında daha fazla bilgi edinmek için bkz. [Maliyet muhasebesi Power BI içeriği](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="e4be0-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="e4be0-111">Ayarlar</span><span class="sxs-lookup"><span data-stu-id="e4be0-111">Setup</span></span>
<span data-ttu-id="e4be0-112">Erişim düzeyinde güvenliği Power BI'ya yaymak için, Power BI içeriği sahibinin bu adımları izlemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="e4be0-113">**Maliyet muhasebesi analizi** Power BI içeriğini yayımlayan kullanıcı otomatik olarak sahip yapılır.</span><span class="sxs-lookup"><span data-stu-id="e4be0-113">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="e4be0-114">Power BI'da güvenliği yalnızca bir sahip ayarlayabilir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="e4be0-115">Ayrıca, bir sahip PowerBI.com'a başka kullanıcılar ekleyene kadar **Maliyet muhasebesi analizi** Power BI içeriğindeki verileri sahibi dışında kimse göremez.</span><span class="sxs-lookup"><span data-stu-id="e4be0-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="e4be0-116">Tanım dosyasını Power BI'da yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="e4be0-116">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="e4be0-117">PowerBI.com adresinde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="e4be0-117">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="e4be0-118">**Maliyet muhasebesi analizi** Power BI içeriği için veri kümesini bulun.</span><span class="sxs-lookup"><span data-stu-id="e4be0-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="e4be0-119">Güvenlik sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="e4be0-119">Open the security page.</span></span>

    ![Güvenlik sayfasını açma](./media/CA-picture-1.png)

5. <span data-ttu-id="e4be0-121">**Maliyet nesne denetleyicisi** rolü zaten oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="e4be0-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="e4be0-122">Maliyet muhasebesi erişim düzeyi organizasyon hiyerarşisinin bir parçası olan diğer üyeleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e4be0-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Üyeleri ekleme](./media/CA-picture-2.png)

<span data-ttu-id="e4be0-124">**Maliyet nesnesi denetleyicisi** rolüne eklenen kullanıcılar, Maliyet muhasebesi erişim düzeyi organizasyon hiyerarşisindeki tanıma göre yalnızca görmelerine izin verilen verileri görecektir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="e4be0-125">Power BI'dan katıştırılan kutucuklara ve raporlara satır düzeyinde güvenlik uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e4be0-125">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="e4be0-126">Güvenliği güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e4be0-126">Updating security</span></span>
<span data-ttu-id="e4be0-127">Maliyet muhasebesinde erişim düzeyinde güvenlikte güncelleştirmeler yapıldıysa ve Power BI'ın bu güncelleştirmeleri yansıtmasını istiyorsanız **Maliyet muhasebesi analizi** Power BI içeriğinin tüm varlık deposunu güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="e4be0-128">Varlık deposu güncelleştirmesini tamamladıktan sonra PowerBI.com'daki yapıları güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-128">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="e4be0-129">Bir varlık deposunun nasıl güncelleştirileceği hakkında daha fazla bilgi için bkz. [Varlık deposunu güncelleme](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="e4be0-129">For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="e4be0-130">**Maliyet muhasebesi analizi** Power BI içeriğinin sahibi, organizasyon hiyerarşisinde yeni kullanıcılara erişim verildiği zaman da bir varlık deposu güncelleştirmesi yapmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e4be0-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="e4be0-131">Ayrıca, sahibin yeni kullanıcıları PowerBI.com'daki **Maliyet nesnesi denetleyicisi** rolüne eklemesi, böylece onlara satır düzeyinde güvenlik uygulanmasını sağlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="e4be0-132">Güvenliği devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="e4be0-132">Disabling security</span></span>
<span data-ttu-id="e4be0-133">Kuruluşunuzun veri erişimini kısıtlamak istediğini varsayalım.</span><span class="sxs-lookup"><span data-stu-id="e4be0-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="e4be0-134">Maliyet muhasebesini çalıştırdığınız zaman bazı nedenlerle güvenlik parametreleri devre dışı bırakılıyorsa, sahibin kullanıcıları Power BI'da **Maliyet muhasebesici** rolüne eklemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="e4be0-135">Güvenliği etkinleştirilmiş durumdan devre dışı duruma değiştirirseniz kullanıcıları **Maliyet nesnesi denetleyicisi** rolünden kaldırmak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-135">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="e4be0-136">Ve güvenliği yeniden etkinleştirdiğinizde de kullanıcıların eklenmesi de tavsiye edilir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="e4be0-137">Kullanıcılar her iki role ait olabilir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-137">Users can belong to both roles.</span></span> <span data-ttu-id="e4be0-138">Birleşik erişim, her iki rolün birleşimidir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="e4be0-139">**Maliyet muhasebesi analizi** Power BI içeriğinde, birleşik erişimi olan kullanıcılar verilere sınırsız erişebilir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="e4be0-140">Amacınız sınırlı erişim uygulamaksa, kullanıcıların yalnızca **Maliyet nesnesi denetleyicisi** rolüne atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="e4be0-141">Bu satır düzeyinde güvenlik güncelleştirmeleri hemen uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e4be0-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="e4be0-142">Etkilenen kullanıcıların tarayıcılarını yenilemeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4be0-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4be0-143">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e4be0-143">Additional resources</span></span>
<span data-ttu-id="e4be0-144">Power BI'ın satır düzeyinde güvenliği hakkında daha fazla bilgi için bkz. [Power BI'daki modelinizde güvenliği yönetme](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="e4be0-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
