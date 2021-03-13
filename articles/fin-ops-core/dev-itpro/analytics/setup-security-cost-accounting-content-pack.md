---
title: Maliyet muhasebesi analizi Power BI içeriğinin güvenliğini ayarlama
description: Bu konuda, Maliyet muhasebesindeki erişim düzeyinde güvenliği, Microsoft Power BI'daki satır düzeyinde güvenliğe nasıl yayabileceğiniz açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d54ced21de112288c2f98c0bc895ca0d49c217e3
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093367"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="927e7-103">Maliyet muhasebesi analizi güvenliğini ayarlama Power BI içeriği</span><span class="sxs-lookup"><span data-stu-id="927e7-103">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="927e7-104">Bu konuda, Maliyet muhasebesindeki erişim düzeyinde güvenliği, Microsoft Power BI'daki satır düzeyinde güvenliğe nasıl yayabileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="927e7-104">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="927e7-105">Bu işlevsellik, kullanıcıların yalnızca erişim izni verilen Power BI verilerini görmelerini garantilemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="927e7-105">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="927e7-106">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="927e7-106">Overview</span></span>

<span data-ttu-id="927e7-107">**Maliyet muhasebesi analizi** Microsoft Power BI içeriği, kullanıcının erişimini sınırlamak için Power BI'ın satır düzeyinde güvenliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="927e7-107">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="927e7-108">Güvenlik, Maliyet muhasebesi parametrelerinde ayarlanan erişim düzeyinde organizasyon hiyerarşisine dayanır.</span><span class="sxs-lookup"><span data-stu-id="927e7-108">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="927e7-109">**Maliyet muhasebesi analizi** Power BI içeriği hakkında daha fazla bilgi edinmek için bkz. [Maliyet muhasebesi Power BI içeriği](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="927e7-109">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="927e7-110">Ayarlar</span><span class="sxs-lookup"><span data-stu-id="927e7-110">Setup</span></span>
<span data-ttu-id="927e7-111">Erişim düzeyinde güvenliği Power BI'ya yaymak için, Power BI içeriği sahibinin bu adımları izlemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="927e7-111">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="927e7-112">**Maliyet muhasebesi analizi** Power BI içeriğini yayımlayan kullanıcı otomatik olarak sahip yapılır.</span><span class="sxs-lookup"><span data-stu-id="927e7-112">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="927e7-113">Power BI'da güvenliği yalnızca bir sahip ayarlayabilir.</span><span class="sxs-lookup"><span data-stu-id="927e7-113">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="927e7-114">Ayrıca, bir sahip PowerBI.com'a başka kullanıcılar ekleyene kadar **Maliyet muhasebesi analizi** Power BI içeriğindeki verileri sahibi dışında kimse göremez.</span><span class="sxs-lookup"><span data-stu-id="927e7-114">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="927e7-115">Tanım dosyasını Power BI'da yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="927e7-115">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="927e7-116">PowerBI.com adresinde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="927e7-116">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="927e7-117">**Maliyet muhasebesi analizi** Power BI içeriği için veri kümesini bulun.</span><span class="sxs-lookup"><span data-stu-id="927e7-117">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="927e7-118">Güvenlik sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="927e7-118">Open the security page.</span></span>

    ![Güvenlik sayfasını açma](./media/CA-picture-1.png)

5. <span data-ttu-id="927e7-120">**Maliyet nesne denetleyicisi** rolü zaten oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="927e7-120">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="927e7-121">Maliyet muhasebesi erişim düzeyi organizasyon hiyerarşisinin bir parçası olan diğer üyeleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="927e7-121">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Üyeleri ekleme](./media/CA-picture-2.png)

<span data-ttu-id="927e7-123">**Maliyet nesnesi denetleyicisi** rolüne eklenen kullanıcılar, Maliyet muhasebesi erişim düzeyi organizasyon hiyerarşisindeki tanıma göre yalnızca görmelerine izin verilen verileri görecektir.</span><span class="sxs-lookup"><span data-stu-id="927e7-123">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="927e7-124">Power BI'dan katıştırılan kutucuklara ve raporlara satır düzeyinde güvenlik uygulanır.</span><span class="sxs-lookup"><span data-stu-id="927e7-124">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="927e7-125">Güvenliği güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="927e7-125">Updating security</span></span>
<span data-ttu-id="927e7-126">Maliyet muhasebesinde erişim düzeyinde güvenlikte güncelleştirmeler yapıldıysa ve Power BI'ın bu güncelleştirmeleri yansıtmasını istiyorsanız **Maliyet muhasebesi analizi** Power BI içeriğinin tüm varlık deposunu güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="927e7-126">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="927e7-127">Varlık deposu güncelleştirmesini tamamladıktan sonra PowerBI.com'daki yapıları güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="927e7-127">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="927e7-128">Bir varlık deposunun nasıl güncelleştirileceği hakkında daha fazla bilgi için bkz. [Varlık deposu ile Power BI tümleştirmesi](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="927e7-128">For more information about how to do an entity store update, see [Power BI integration with Entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="927e7-129">**Maliyet muhasebesi analizi** Power BI içeriğinin sahibi, organizasyon hiyerarşisinde yeni kullanıcılara erişim verildiği zaman da bir varlık deposu güncelleştirmesi yapmalıdır.</span><span class="sxs-lookup"><span data-stu-id="927e7-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="927e7-130">Ayrıca, sahibin yeni kullanıcıları PowerBI.com'daki **Maliyet nesnesi denetleyicisi** rolüne eklemesi, böylece onlara satır düzeyinde güvenlik uygulanmasını sağlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="927e7-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="927e7-131">Güvenliği devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="927e7-131">Disabling security</span></span>
<span data-ttu-id="927e7-132">Kuruluşunuzun veri erişimini kısıtlamak istediğini varsayalım.</span><span class="sxs-lookup"><span data-stu-id="927e7-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="927e7-133">Maliyet muhasebesini çalıştırdığınız zaman bazı nedenlerle güvenlik parametreleri devre dışı bırakılıyorsa, sahibin kullanıcıları Power BI'da **Maliyet muhasebesici** rolüne eklemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="927e7-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="927e7-134">Güvenliği etkinleştirilmiş durumdan devre dışı duruma değiştirirseniz kullanıcıları **Maliyet nesnesi denetleyicisi** rolünden kaldırmak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="927e7-134">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="927e7-135">Ve güvenliği yeniden etkinleştirdiğinizde de kullanıcıların eklenmesi de tavsiye edilir.</span><span class="sxs-lookup"><span data-stu-id="927e7-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="927e7-136">Kullanıcılar her iki role ait olabilir.</span><span class="sxs-lookup"><span data-stu-id="927e7-136">Users can belong to both roles.</span></span> <span data-ttu-id="927e7-137">Birleşik erişim, her iki rolün birleşimidir.</span><span class="sxs-lookup"><span data-stu-id="927e7-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="927e7-138">**Maliyet muhasebesi analizi** Power BI içeriğinde, birleşik erişimi olan kullanıcılar verilere sınırsız erişebilir.</span><span class="sxs-lookup"><span data-stu-id="927e7-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="927e7-139">Amacınız sınırlı erişim uygulamaksa, kullanıcıların yalnızca **Maliyet nesnesi denetleyicisi** rolüne atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="927e7-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="927e7-140">Bu satır düzeyinde güvenlik güncelleştirmeleri hemen uygulanır.</span><span class="sxs-lookup"><span data-stu-id="927e7-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="927e7-141">Etkilenen kullanıcıların tarayıcılarını yenilemeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="927e7-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="927e7-142">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="927e7-142">Additional resources</span></span>
<span data-ttu-id="927e7-143">Power BI'ın satır düzeyinde güvenliği hakkında daha fazla bilgi için bkz. [Power BI'daki modelinizde güvenliği yönetme](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="927e7-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
