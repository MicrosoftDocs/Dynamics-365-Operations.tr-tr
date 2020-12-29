---
title: Üretim talebine bağlı olarak konsinye stok sahipliğini değiştirme
description: Bu yordam üretimde stok için bir talep olduğunda, konsinye stoğun sahibini satıcıdan tüzel kişiliğinize değiştirmeyi gösterir.
author: perlynne
manager: tfehr
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c50affa05b8df53d31660854f4d1ead6aeff820
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439568"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="0609d-103">Üretim talebine bağlı olarak konsinye stok sahipliğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="0609d-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0609d-104">Bu yordam üretimde stok için bir talep olduğunda, konsinye stoğun sahibini satıcıdan tüzel kişiliğinize değiştirmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="0609d-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="0609d-105">Bu sahiplik değişikliği bir stok sahipliği değişiklik günlüğü oluşturup bunu deftere naklederek yapılır.</span><span class="sxs-lookup"><span data-stu-id="0609d-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="0609d-106">Sahiplik değişikliği günlük satırları el ile veya bu kayıtta gösterildiği gibi, var olan üretim talebine göre oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="0609d-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="0609d-107">Genellikle, bu görevi bir atölye gözetmeni gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="0609d-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="0609d-108">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0609d-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="0609d-109">Kendi verilerinizi kullanıyorsanız şu önkoşullara sahip olduğunuzdan emin olun: stok sahibi değişikliği için ayarlanmış bir stok günlüğü adı, fiziksel olarak kaydedilmiş satıcıya ait eldeki maddeler ve malzeme için bir veya daha fazla üretim emri satırı.</span><span class="sxs-lookup"><span data-stu-id="0609d-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="0609d-110">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="0609d-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="0609d-111">Giden konsinye işlemleri kullanıma hazır olarak desteklenmez ve otomatik sahiplik günlüğü işlemi desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="0609d-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="0609d-112">Stok sahipliği günlüğü oluşturma</span><span class="sxs-lookup"><span data-stu-id="0609d-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="0609d-113">Stok yönetimi > Günlük girişleri > Maddeler > Stok sahipliği değişikliği'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="0609d-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="0609d-114">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0609d-114">Click New.</span></span>
    * <span data-ttu-id="0609d-115">Stok sahipliği değişiklik günlüğü konsinye stoğun sahibini satıcıdan geçerli tüzel kişiliğe değiştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0609d-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="0609d-116">Bu sahiplik değişikliği, satıcının sahibi olduğu eldeki stoğu serbest bırakıp bu stoğu geçerli tüzel kişilik tarafına alarak gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="0609d-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="0609d-117">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0609d-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="0609d-118">Yalnızca Sahiplik değişikliği günlük türüne sahip stok günlüğü adlarını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0609d-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="0609d-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0609d-119">Click OK.</span></span>
5. <span data-ttu-id="0609d-120">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0609d-120">Click Functions.</span></span>
6. <span data-ttu-id="0609d-121">Üretim emirlerinden günlük satırları oluştur öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0609d-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="0609d-122">Sahipliği değiştirme işlemine hammaddenin tüketimi için talebi olan tüm üretim satırlarını sorgulayarak başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0609d-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="0609d-123">Eklenecek stok sorunu durumları alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0609d-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="0609d-124">Bu seçenek, stok hareketlerinin çıkış durumuna göre filtre uygulamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0609d-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="0609d-125">Örneğin, Malzeme çekildi ve Rezerve fiziksel durumlarına sahip stok için günlük satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0609d-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="0609d-126">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="0609d-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="0609d-127">Bu bölüm daha fazla filtre uygulamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0609d-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="0609d-128">Örneğin, belirli bir hammadde tarihi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0609d-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="0609d-129">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0609d-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="0609d-130">Stok sahipliği değişikliği günlüğünü deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="0609d-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="0609d-131">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0609d-131">Click Post.</span></span>
    * <span data-ttu-id="0609d-132">Günlük deftere nakledildiğinde, satıcıya ait stok bir "Sahiplik değişikliği" referansı kullanılarak yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="0609d-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="0609d-133">Daha sonra stok satınalma siparişi ürün girişi ile güncelleştirilen bir stok hareket kullanılarak elde olarak alınır.</span><span class="sxs-lookup"><span data-stu-id="0609d-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="0609d-134">Yalnızca deftere nakledilen günlükle ilgili hareketlerin oluşturulduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="0609d-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="0609d-135">Beklenen stok hareketleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="0609d-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="0609d-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0609d-136">Click OK.</span></span>
3. <span data-ttu-id="0609d-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0609d-137">Close the page.</span></span>

