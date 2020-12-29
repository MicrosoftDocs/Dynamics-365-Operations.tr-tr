---
title: Bir kanalı kanal gezinme hiyerarşisini kullanacak şekilde yapılandırma
description: Bu konu, Microsoft Dynamics 365 Commerce'te bir kanal gezinme hiyerarşisi kullanmak üzere bir kanalın nasıl yapılandırılacağını açıklamaktadır.
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
ms.openlocfilehash: 7b5041d35d310125c314ab2cb77d3cc40cdb7113
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416330"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="b406f-103">Bir kanalı kanal gezinme hiyerarşisini kullanacak şekilde yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b406f-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b406f-104">Bu konu, Microsoft Dynamics 365 Commerce'te bir kanal gezinme hiyerarşisi kullanmak üzere bir kanalın nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b406f-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b406f-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="b406f-105">Overview</span></span>

<span data-ttu-id="b406f-106">Kanal gezinme hiyerarşileri, ürünleri kategoriler halinde düzenleyerek ürünlere bir e-ticaret sitesinde veya satış noktasında (POS) göz atılabilmesini sağlanır.</span><span class="sxs-lookup"><span data-stu-id="b406f-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="b406f-107">Perakende ve çevrimiçi kanallar kanal gezinme hiyerarşileriyle yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b406f-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="b406f-108">Kanalı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b406f-108">Configure the channel</span></span>

<span data-ttu-id="b406f-109">Kanal gezinme hiyerarşisini kullanacak şekilde kanalı yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b406f-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b406f-110">Gezinti bölmesinde, **Modüller \> Retail and commerce \> Kanal kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b406f-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="b406f-111">Yapılandırılacak kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="b406f-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="b406f-112">Eylem bölmesinde, **Öznitelik meta verileri ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b406f-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="b406f-113">**Kategori hiyerarşisi** açılır listesinde, uygun kanal gezinme hiyerarşisini seçin.</span><span class="sxs-lookup"><span data-stu-id="b406f-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="b406f-114">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b406f-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="b406f-115">**Öznitelik grubu** altında, tüm düğümler için genel öznitelikler olacak olan öznitelik gruplarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b406f-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="b406f-116">Aşağıdaki resimde, bir kanalın kanal gezinme hiyerarşisini kullanacak şekilde nasıl yapılandırıldığı gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="b406f-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Örnek kanalı yapılandırması](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="b406f-118">Öznitelik meta verileri ayarla</span><span class="sxs-lookup"><span data-stu-id="b406f-118">Set attribute metadata</span></span>

<span data-ttu-id="b406f-119">Öznitelik meta verilerinin ayarlanması, her bir düğümdeki özniteliklerin yapılandırılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="b406f-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="b406f-120">Öznitelik meta verilerini ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b406f-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="b406f-121">Eylem bölmesinde, **Öznitelik meta verileri ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b406f-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="b406f-122">Her bir düğüm için **Kanal ürün öznitelikleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b406f-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="b406f-123">Kanalda düzelticileri etkinleştirmek için **Özniteliği kanalda göster** ayarını **Evet** ve **İyileştirilebilir** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="b406f-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="b406f-124">**Eylem bölmesinde** her düğümü istenildiği gibi yapılandırdıktan sonra, kaydetmek için **Kaydet** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b406f-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="b406f-125">Bu ekrandan çıkıp **Kanal kategorileri ve ürün öznitelikleri** sayfasına dönmek için sağ üst köşedeki **X**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b406f-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="b406f-126">Aşağıdaki resimde, bir kanal kategori düğümünde yapılandırılmış kanal ürün öznitelikleri kümesi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="b406f-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Kanal kategori düğümündeki kanal öznitelikleri](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="b406f-128">Değişiklikleri yayımlama</span><span class="sxs-lookup"><span data-stu-id="b406f-128">Publish changes</span></span>

<span data-ttu-id="b406f-129">Değişikliklerin yürürlüğe girmesi için, değişiklikleri yayımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b406f-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="b406f-130">Değişiklikleri yayımlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b406f-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="b406f-131">Eylem bölmesinde, **Kanal güncelleştirmelerini yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b406f-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="b406f-132">**Kanal güncelleştirmelerini yayınla** bölmesinde **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b406f-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="b406f-133">Aşağıdaki resimde, kanal güncelleştirmelerinin nasıl yayımlanacağı gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="b406f-133">The following image shows how to publish channel updates.</span></span>

![Kanal güncelleştirmelerini yayınla](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="b406f-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b406f-135">Additional resources</span></span>

[<span data-ttu-id="b406f-136">Kanal gezinme hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b406f-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)


