---
title: Kuruluş hiyerarşilerini ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te organizasyon hiyerarşilerinin nasıl ayarlanacağı açıklanmaktadır.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4238d1aa277bf2f1df30825ef20dbf3095d13ebc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800579"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="5680b-103">Kuruluş hiyerarşilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="5680b-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5680b-104">Bu konuda, Microsoft Dynamics 365 Commerce'te organizasyon hiyerarşilerinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5680b-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5680b-105">Kanalları oluşturmadan önce, organizasyon hiyerarşilerinizi ayarlandığınızdan emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5680b-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="5680b-106">İşlerinize farklı perspektiflerden bakmak ve raporlamak için organizasyon hiyerarşilerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5680b-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="5680b-107">Örneğin, vergi, hukuki veya yasal raporlamaya yönelik bir hiyerarşi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5680b-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="5680b-108">Ardından, yasal olarak gerekmeyen ama dahili raporlama için kullanılan mali bilgileri raporlamak için başka bir hiyerarşi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5680b-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="5680b-109">Bir organizasyon hiyerarşisi oluşturmadan önce organizasyonları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5680b-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="5680b-110">Daha fazla bilgi için bkz. [Tüzel kişilikleri oluşturma](channels-legal-entities.md) veya [İşletme birimlerini oluşturma](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)".</span><span class="sxs-lookup"><span data-stu-id="5680b-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="5680b-111">Daha fazla bilgi edinmek için aşağıdaki konulara bakın.</span><span class="sxs-lookup"><span data-stu-id="5680b-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="5680b-112">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="5680b-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="5680b-113">Organizasyon hiyerarşinizi planlama</span><span class="sxs-lookup"><span data-stu-id="5680b-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="5680b-114">Kuruluş hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="5680b-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="5680b-115">Kuruluş hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="5680b-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="5680b-116">Bir organizasyon hiyerarşisi oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5680b-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5680b-117">Gezinti bölmesinde **Modüller \> Retail and commerce \> Kanal Kurulumu \> Organizasyon hiyerarşileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5680b-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="5680b-118">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5680b-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5680b-119">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5680b-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="5680b-120">**Amaç** bölümünde, **Amaç ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5680b-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="5680b-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5680b-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="5680b-122">Organizasyon hiyerarşinize atanacak bir amaç seçin.</span><span class="sxs-lookup"><span data-stu-id="5680b-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="5680b-123">**Atanan hiyerarşiler** bölümünde, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5680b-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="5680b-124">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="5680b-124">In the list, mark the selected row.</span></span> <span data-ttu-id="5680b-125">Yeni oluşturduğunuz hiyerarşiyi bulun.</span><span class="sxs-lookup"><span data-stu-id="5680b-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="5680b-126">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5680b-126">Select **OK**.</span></span>

<span data-ttu-id="5680b-127">Aşağıdaki resimde, hayali "Adventure Works" mağazaları kümesi için oluşturulmuş örnek bir organizasyon hiyerarşisi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5680b-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Örnek organizasyon hiyerarşisi oluşturma](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="5680b-129">Hiyerarşiye organizasyonlar ekleme</span><span class="sxs-lookup"><span data-stu-id="5680b-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="5680b-130">Bir hiyerarşiye organizasyonlar eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5680b-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5680b-131">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5680b-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="5680b-132">Hiyerarşinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="5680b-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="5680b-133">Eylem bölmesinde, **Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5680b-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="5680b-134">Gerekirse kuruluşlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5680b-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="5680b-135">Bir organizasyon eklemek için **Düzenle**'yi ve ardından **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5680b-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="5680b-136">Değişiklikleri tamamladıktan sonra bir taslak kaydedebilir ve değişiklikleri yayımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5680b-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="5680b-137">Aşağıdaki resimde, "Mall", "Outlet", "Çevrimiçi" ve "Çağrı Merkezi" kanalları için dört maliyet merkezi yer alan hiyerarşi köküne eklenmiş bir tüzel kişilik gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5680b-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="5680b-138">Bunun ardından, çeşitli perakende ve çağrı merkezi kanalları ve çevrimiçi kanallar her birine eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="5680b-138">Various retail, call center and online channels can then be added to each.</span></span>

![Örnek hiyerarşi tasarımcısı](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="5680b-140">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5680b-140">Additional resources</span></span>

[<span data-ttu-id="5680b-141">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="5680b-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5680b-142">Kuruluş hiyerarşinizi planlama</span><span class="sxs-lookup"><span data-stu-id="5680b-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5680b-143">Tüzel kişilik oluşturma</span><span class="sxs-lookup"><span data-stu-id="5680b-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="5680b-144">Çalışma birimleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="5680b-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5680b-145">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="5680b-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5680b-146">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="5680b-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
