---
title: Organizasyon hiyerarşisine kanal ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te bir organizasyon hiyerarşisine nasıl kanal ekleneceği açıklanmaktadır.
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
ms.openlocfilehash: 701c90e8e28b4419422cddde698e9c9862a588a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416389"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="143ef-103">Organizasyon hiyerarşisine kanal ekleme</span><span class="sxs-lookup"><span data-stu-id="143ef-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="143ef-104">Bu konuda, Microsoft Dynamics 365 Commerce'te bir organizasyon hiyerarşisine nasıl kanal ekleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="143ef-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="143ef-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="143ef-105">Overview</span></span>

<span data-ttu-id="143ef-106">Kanalların bir veya daha fazla organizasyon hiyerarşiyle ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="143ef-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="143ef-107">Kanalları oluşturmadan önce, organizasyon hiyerarşilerinizin ayarlandığını onaylamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="143ef-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="143ef-108">Organizasyon hiyerarşilerinin nasıl oluşturulacağı hakkında daha ayrıntılı bilgi için bkz. [Organizasyon hiyerarşileri](channels-org-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="143ef-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="143ef-109">Hiyerarşi seçme</span><span class="sxs-lookup"><span data-stu-id="143ef-109">Select a hierarchy</span></span>

<span data-ttu-id="143ef-110">Hiyerarşi seçmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="143ef-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="143ef-111">Gezinti bölmesinde **Modüller \> Retail and commerce \> Kanal Kurulumu \> Organizasyon hiyerarşileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="143ef-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="143ef-112">Listeden, kanalı ekleyeceğiniz organizasyon hiyerarşisini seçin.</span><span class="sxs-lookup"><span data-stu-id="143ef-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="143ef-113">Eylem bölmesinde hiyerarşi ayrıntılarını görüntülemek için **Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="143ef-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="143ef-114">Aşağıdaki resim, seçili hiyerarşinin organizasyon hiyerarşisi ayrıntılarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="143ef-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Seçili hiyerarşinin organizasyon hiyerarşisi ayrıntıları](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="143ef-116">Bir hiyerarşi düğümüne kanal ekleme</span><span class="sxs-lookup"><span data-stu-id="143ef-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="143ef-117">Bir hiyerarşi düğümüne kanal eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="143ef-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="143ef-118">Eylem bölmesinde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="143ef-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="143ef-119">Kanalın eklenmesini istediğiniz hiyerarşi düğümünü seçin ve **Ekle** açılır listesinden **Perakende Kanalı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="143ef-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="143ef-120">Eklenecek kanalı ve ardından **Tamam** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="143ef-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="143ef-121">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="143ef-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="143ef-122">Eylem bölmesinde, **Yayımla** 'yı seçin ve bu eylemin hemen yürürlüğe girmesini sağlamak için geçmiş bir **Yürürlük tarihi** girin.</span><span class="sxs-lookup"><span data-stu-id="143ef-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="143ef-123">Aşağıdaki resimde, hiyerarşi düğümüne eklenecek kanalın nasıl seçildiği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="143ef-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Hiyerarşi düğümüne eklenecek kanalı seçme](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="143ef-125">Aşağıdaki resim, çeşitli kanalların ekli olduğu bir hiyerarşiyi gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="143ef-125">The following image shows a hierarchy with various channels added.</span></span>

![Çeşitli kanalların eklendiği bir hiyerarşi](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="143ef-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="143ef-127">Additional resources</span></span>

[<span data-ttu-id="143ef-128">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="143ef-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="143ef-129">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="143ef-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="143ef-130">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="143ef-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="143ef-131">Kuruluş hiyerarşinizi planlama</span><span class="sxs-lookup"><span data-stu-id="143ef-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="143ef-132">Organizasyon hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="143ef-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="143ef-133">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="143ef-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="143ef-134">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="143ef-134">Set up an online channel</span></span>](channel-setup-online.md)
