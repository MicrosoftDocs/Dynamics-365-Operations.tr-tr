---
title: Konsinyeyi ayarlama
description: "Bu konu gelen konsinye stok operasyonlarının nasıl yapılandırılacağını açıklar."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 758ea8b658693910edeada3a4c27c34ae187b28c
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-consignment"></a><span data-ttu-id="d8d8b-103">Konsinyeyi ayarlama</span><span class="sxs-lookup"><span data-stu-id="d8d8b-103">Set up consignment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d8d8b-104">Bu konu gelen konsinye stok operasyonlarının nasıl yapılandırılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="d8d8b-105">Konsinye stok, satıcıya ait olan ancak tesisinizde depolanan stoktur.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="d8d8b-106">Stoğu tüketmeye veya kullanmaya hazır olduğunuzda stoğun sahipliği size geçer.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="d8d8b-107">Bu konu, konsinye işlemlerini etkinleştirmek için gerekli ayarları açıklar.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="d8d8b-108">Konsinye işlemleri hakkında daha fazla bilgi için bkz. [Konsinye](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="d8d8b-108">For more information about consignment processes, see [Consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="d8d8b-109">Stok sahipleri</span><span class="sxs-lookup"><span data-stu-id="d8d8b-109">Inventory owners</span></span>
<span data-ttu-id="d8d8b-110">Fiziksel gelen konsinye stoğu kaydetmek için bir satıcı sahibi tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="d8d8b-111">Bu **Stok sahibi** sayfasında yapılır.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="d8d8b-112">**Satıcı hesabı**'nı seçtiğinizde bu **Ad** ve **Sahip** alanları için varsayılan değerleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="d8d8b-113">**Sahip** alanındaki değer satıcıya görünür olacaktır, bu nedenle satıcı hesabı adlarınız şirket dışı insanların tanımaları için kolay değilse değiştirmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="d8d8b-114">**Sahip** alanını yalnızca **Stok sahibi** kaydını kaydettiğiniz zamana kadar düzenlemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="d8d8b-115">**Ad** alanı satıcı hesabının ilişkilendirildiği tarafın adıyla doldurulur ve değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="d8d8b-116">[![stok-sahipleri](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="d8d8b-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="d8d8b-117">İzleme boyut grubu</span><span class="sxs-lookup"><span data-stu-id="d8d8b-117">Tracking dimension group</span></span>
<span data-ttu-id="d8d8b-118">Konsinye işlemlerinde kullanılacak maddeler **Sahip** boyutunun **Etkin** olarak ayarlandığı bir **İzleme boyut grubu** ile ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="d8d8b-119">Sahip boyutunda her zaman **Fiziksel stok** ve **Mali stok** seçenekleri seçili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="d8d8b-120">**Boyuta göre tedarik planı** kesinlikle seçilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="d8d8b-121">[![izleme-boyut-grubu](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="d8d8b-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="d8d8b-122">Stok sahipliği değişiklik günlüğü</span><span class="sxs-lookup"><span data-stu-id="d8d8b-122">Inventory ownership change journal</span></span>
<span data-ttu-id="d8d8b-123">Konsinye stoğun sahipliğinin satıcıdan konsinye stoğu tüketecek tüzel kişiliğe transferini kaydetmek için **Stok sahipliği değişiklik** günlüğü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="d8d8b-124">Diğer stok günlükleri gibi bir stok günlüğü adı ile tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="d8d8b-125">Bu adlar **Stok günlüklerinin adları** sayfasında oluşturulur ve **Günlük türü**, **Sahiplik değişikliği** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="d8d8b-126">[![stok-sahiplik-değiştirme-günlüğü](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="d8d8b-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="d8d8b-127">Konsinye işlemlerdeki satıcı iş birliği</span><span class="sxs-lookup"><span data-stu-id="d8d8b-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="d8d8b-128">Satıcılar, satıcı iş birliği arabirimini kullanıyorsa bunu, tesisinizdeki stoğun tüketimini izlemek için kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="d8d8b-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="d8d8b-129">Satıcı iş birliğini kullanmak için satıcıların yapılandırması hakkında daha fazla bilgi için bkz. [Satıcı iş birliği kullanıcıları için güvenlik yapılandırması](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="d8d8b-129">For more information about setting up vendors to use vendor collaboration, see [Configuration of security for vendor collaboration users](../procurement/configure-security-vendor-portal-users.md).</span></span>

