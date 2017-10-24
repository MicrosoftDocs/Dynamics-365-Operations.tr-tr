---
title: "Üretim talebine bağlı olarak konsinye stok sahipliğini değiştirme"
description: "Bu yordam üretimde stok için bir talep olduğunda, konsinye stoğun sahibini satıcıdan tüzel kişiliğinize değiştirmeyi gösterir."
author: perlynne
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5925f5423d596adc4326dfff4734de2afd80b5a8
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="72a98-103">Üretim talebine bağlı olarak konsinye stok sahipliğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="72a98-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72a98-104">Bu yordam üretimde stok için bir talep olduğunda, konsinye stoğun sahibini satıcıdan tüzel kişiliğinize değiştirmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="72a98-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="72a98-105">Bu sahiplik değişikliği bir stok sahipliği değişiklik günlüğü oluşturup bunu deftere naklederek yapılır.</span><span class="sxs-lookup"><span data-stu-id="72a98-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="72a98-106">Sahiplik değişikliği günlük satırları el ile veya bu kayıtta gösterildiği gibi, var olan üretim talebine göre oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="72a98-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="72a98-107">Genellikle, bu görevi bir atölye gözetmeni gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="72a98-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="72a98-108">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72a98-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="72a98-109">Kendi verilerinizi kullanıyorsanız şu önkoşullara sahip olduğunuzdan emin olun: stok sahibi değişikliği için ayarlanmış bir stok günlüğü adı, fiziksel olarak kaydedilmiş satıcıya ait eldeki maddeler ve malzeme için bir veya daha fazla üretim emri satırı.</span><span class="sxs-lookup"><span data-stu-id="72a98-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="72a98-110">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="72a98-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="72a98-111">Stok sahipliği günlüğü oluşturma</span><span class="sxs-lookup"><span data-stu-id="72a98-111">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="72a98-112">Stok yönetimi > Günlük girişleri > Maddeler > Stok sahipliği değişikliği'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="72a98-112">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="72a98-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72a98-113">Click New.</span></span>
    * <span data-ttu-id="72a98-114">Stok sahipliği değişiklik günlüğü konsinye stoğun sahibini satıcıdan geçerli tüzel kişiliğe değiştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="72a98-114">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="72a98-115">Bu sahiplik değişikliği, satıcının sahibi olduğu eldeki stoğu serbest bırakıp bu stoğu geçerli tüzel kişilik tarafına alarak gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="72a98-115">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="72a98-116">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="72a98-116">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="72a98-117">Yalnızca Sahiplik değişikliği günlük türüne sahip stok günlüğü adlarını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72a98-117">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="72a98-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72a98-118">Click OK.</span></span>
5. <span data-ttu-id="72a98-119">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="72a98-119">Click Functions.</span></span>
6. <span data-ttu-id="72a98-120">Üretim emirlerinden günlük satırları oluştur öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72a98-120">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="72a98-121">Sahipliği değiştirme işlemine hammaddenin tüketimi için talebi olan tüm üretim satırlarını sorgulayarak başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72a98-121">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="72a98-122">Eklenecek stok sorunu durumları alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="72a98-122">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="72a98-123">Bu seçenek, stok hareketlerinin çıkış durumuna göre filtre uygulamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="72a98-123">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="72a98-124">Örneğin, Malzeme çekildi ve Rezerve fiziksel durumlarına sahip stok için günlük satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72a98-124">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="72a98-125">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="72a98-125">Expand the Records to include section.</span></span>
    * <span data-ttu-id="72a98-126">Bu bölüm daha fazla filtre uygulamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="72a98-126">This section lets you apply additional filtering.</span></span> <span data-ttu-id="72a98-127">Örneğin, belirli bir hammadde tarihi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72a98-127">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="72a98-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72a98-128">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="72a98-129">Stok sahipliği değişikliği günlüğünü deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="72a98-129">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="72a98-130">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72a98-130">Click Post.</span></span>
    * <span data-ttu-id="72a98-131">Günlük deftere nakledildiğinde, satıcıya ait stok bir "Sahiplik değişikliği" referansı kullanılarak yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="72a98-131">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="72a98-132">Daha sonra stok satınalma siparişi ürün girişi ile güncelleştirilen bir stok hareket kullanılarak elde olarak alınır.</span><span class="sxs-lookup"><span data-stu-id="72a98-132">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="72a98-133">Yalnızca deftere nakledilen günlükle ilgili hareketlerin oluşturulduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="72a98-133">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="72a98-134">Beklenen stok hareketleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="72a98-134">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="72a98-135">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72a98-135">Click OK.</span></span>
3. <span data-ttu-id="72a98-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="72a98-136">Close the page.</span></span>

