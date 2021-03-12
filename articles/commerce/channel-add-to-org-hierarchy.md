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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 297bd34f9bde23d5cc7de266b8e8f49b1a752662
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993714"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="7aa97-103">Organizasyon hiyerarşisine kanal ekleme</span><span class="sxs-lookup"><span data-stu-id="7aa97-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7aa97-104">Bu konuda, Microsoft Dynamics 365 Commerce'te bir organizasyon hiyerarşisine nasıl kanal ekleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7aa97-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7aa97-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="7aa97-105">Overview</span></span>

<span data-ttu-id="7aa97-106">Kanalların bir veya daha fazla organizasyon hiyerarşiyle ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="7aa97-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="7aa97-107">Kanalları oluşturmadan önce, organizasyon hiyerarşilerinizin ayarlandığını onaylamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7aa97-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="7aa97-108">Organizasyon hiyerarşilerinin nasıl oluşturulacağı hakkında daha ayrıntılı bilgi için bkz. [Organizasyon hiyerarşileri](channels-org-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="7aa97-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="7aa97-109">Hiyerarşi seçme</span><span class="sxs-lookup"><span data-stu-id="7aa97-109">Select a hierarchy</span></span>

<span data-ttu-id="7aa97-110">Hiyerarşi seçmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7aa97-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="7aa97-111">Gezinti bölmesinde **Modüller \> Retail and commerce \> Kanal Kurulumu \> Organizasyon hiyerarşileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7aa97-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="7aa97-112">Listeden, kanalı ekleyeceğiniz organizasyon hiyerarşisini seçin.</span><span class="sxs-lookup"><span data-stu-id="7aa97-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="7aa97-113">Eylem bölmesinde hiyerarşi ayrıntılarını görüntülemek için **Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7aa97-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="7aa97-114">Aşağıdaki resim, seçili hiyerarşinin organizasyon hiyerarşisi ayrıntılarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="7aa97-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Seçili hiyerarşinin organizasyon hiyerarşisi ayrıntıları](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="7aa97-116">Bir hiyerarşi düğümüne kanal ekleme</span><span class="sxs-lookup"><span data-stu-id="7aa97-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="7aa97-117">Bir hiyerarşi düğümüne kanal eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7aa97-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="7aa97-118">Eylem bölmesinde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7aa97-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="7aa97-119">Kanalın eklenmesini istediğiniz hiyerarşi düğümünü seçin ve **Ekle** açılır listesinden **Perakende Kanalı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="7aa97-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="7aa97-120">Eklenecek kanalı ve ardından **Tamam** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7aa97-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="7aa97-121">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7aa97-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="7aa97-122">Eylem bölmesinde, **Yayımla** 'yı seçin ve bu eylemin hemen yürürlüğe girmesini sağlamak için geçmiş bir **Yürürlük tarihi** girin.</span><span class="sxs-lookup"><span data-stu-id="7aa97-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="7aa97-123">Aşağıdaki resimde, hiyerarşi düğümüne eklenecek kanalın nasıl seçildiği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="7aa97-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Hiyerarşi düğümüne eklenecek kanalı seçme](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="7aa97-125">Aşağıdaki resim, çeşitli kanalların ekli olduğu bir hiyerarşiyi gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="7aa97-125">The following image shows a hierarchy with various channels added.</span></span>

![Çeşitli kanalların eklendiği bir hiyerarşi](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="7aa97-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7aa97-127">Additional resources</span></span>

[<span data-ttu-id="7aa97-128">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="7aa97-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7aa97-129">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="7aa97-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7aa97-130">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="7aa97-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7aa97-131">Kuruluş hiyerarşinizi planlama</span><span class="sxs-lookup"><span data-stu-id="7aa97-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7aa97-132">Organizasyon hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="7aa97-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="7aa97-133">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="7aa97-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="7aa97-134">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="7aa97-134">Set up an online channel</span></span>](channel-setup-online.md)
