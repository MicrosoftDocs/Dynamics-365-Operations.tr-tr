---
title: Kuruluş hiyerarşilerini ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te organizasyon hiyerarşilerinin nasıl ayarlanacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 29d4b686cbb66715196fca06e4642fbb8a337ace
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113863"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="b4a91-103">Kuruluş hiyerarşilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="b4a91-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b4a91-104">Bu konuda, Microsoft Dynamics 365 Commerce'te organizasyon hiyerarşilerinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b4a91-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b4a91-105">Özet</span><span class="sxs-lookup"><span data-stu-id="b4a91-105">Overview</span></span>

<span data-ttu-id="b4a91-106">Kanalları oluşturmadan önce, organizasyon hiyerarşilerinizi ayarlandığınızdan emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4a91-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="b4a91-107">İşlerinize farklı perspektiflerden bakmak ve raporlamak için organizasyon hiyerarşilerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4a91-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="b4a91-108">Örneğin, vergi, hukuki veya yasal raporlamaya yönelik bir hiyerarşi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4a91-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="b4a91-109">Ardından, yasal olarak gerekmeyen ama dahili raporlama için kullanılan mali bilgileri raporlamak için başka bir hiyerarşi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4a91-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="b4a91-110">Bir organizasyon hiyerarşisi oluşturmadan önce organizasyonları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4a91-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="b4a91-111">Daha fazla bilgi için bkz. [Tüzel kişilikleri oluşturma](channels-legal-entities.md) veya [İşletme birimlerini oluşturma](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)".</span><span class="sxs-lookup"><span data-stu-id="b4a91-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="b4a91-112">Daha fazla bilgi edinmek için aşağıdaki konulara bakın.</span><span class="sxs-lookup"><span data-stu-id="b4a91-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="b4a91-113">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="b4a91-113">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="b4a91-114">Organizasyon hiyerarşinizi planlama</span><span class="sxs-lookup"><span data-stu-id="b4a91-114">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="b4a91-115">Kuruluş hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4a91-115">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="b4a91-116">Kuruluş hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4a91-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="b4a91-117">Bir organizasyon hiyerarşisi oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b4a91-118">Gezinti bölmesinde **Modüller \> Retail and commerce \> Kanal Kurulumu \> Organizasyon hiyerarşileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="b4a91-119">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b4a91-120">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="b4a91-121">**Amaç** bölümünde, **Amaç ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="b4a91-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="b4a91-123">Organizasyon hiyerarşinize atanacak bir amaç seçin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="b4a91-124">**Atanan hiyerarşiler** bölümünde, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="b4a91-125">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-125">In the list, mark the selected row.</span></span> <span data-ttu-id="b4a91-126">Yeni oluşturduğunuz hiyerarşiyi bulun.</span><span class="sxs-lookup"><span data-stu-id="b4a91-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="b4a91-127">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-127">Select **OK**.</span></span>

<span data-ttu-id="b4a91-128">Aşağıdaki resimde, hayali "Adventure Works" mağazaları kümesi için oluşturulmuş örnek bir organizasyon hiyerarşisi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b4a91-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Örnek organizasyon hiyerarşisi oluşturma](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="b4a91-130">Hiyerarşiye organizasyonlar ekleme</span><span class="sxs-lookup"><span data-stu-id="b4a91-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="b4a91-131">Bir hiyerarşiye organizasyonlar eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b4a91-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="b4a91-133">Hiyerarşinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="b4a91-134">Eylem bölmesinde, **Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="b4a91-135">Gerekirse kuruluşlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="b4a91-136">Bir organizasyon eklemek için **Düzenle**'yi ve ardından **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b4a91-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="b4a91-137">Değişiklikleri tamamladıktan sonra bir taslak kaydedebilir ve değişiklikleri yayımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4a91-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="b4a91-138">Aşağıdaki resimde, "Mall", "Outlet", "Çevrimiçi" ve "Çağrı Merkezi" kanalları için dört maliyet merkezi yer alan hiyerarşi köküne eklenmiş bir tüzel kişilik gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b4a91-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="b4a91-139">Bunun ardından, çeşitli perakende ve çağrı merkezi kanalları ve çevrimiçi kanallar her birine eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="b4a91-139">Various retail, call center and online channels can then be added to each.</span></span>

![Örnek hiyerarşi tasarımcısı](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="b4a91-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b4a91-141">Additional resources</span></span>

[<span data-ttu-id="b4a91-142">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="b4a91-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="b4a91-143">Kuruluş hiyerarşinizi planlama</span><span class="sxs-lookup"><span data-stu-id="b4a91-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="b4a91-144">Tüzel kişilik oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4a91-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="b4a91-145">Çalışma birimleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4a91-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="b4a91-146">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="b4a91-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="b4a91-147">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="b4a91-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
